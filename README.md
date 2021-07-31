# js30-day2
js30-day2
 
 JS clock 
 
 Css:       
              
            
              transform-origin: 100%;
              transform: rotate(90deg);
              transition: all 0.05s;
              transition-timing-function: cubic-bezier(0.1, 2.7, 0.58, 1);   
            
JS: 

          <script>
          const secondHand = document.querySelector('.second-hand');
          const minsHand = document.querySelector('.min-hand');
          const hourHand = document.querySelector('.hour-hand');

          function setDate() {
              const now = new Date();

              const seconds = now.getSeconds();
              const secondsDegrees = ((seconds / 60) * 360) + 90;
              secondHand.style.transform = `rotate(${secondsDegrees}deg)`;

              const mins = now.getMinutes();
              const minsDegrees = ((mins / 60) * 360) + 90;
              minsHand.style.transform = `rotate(${minsDegrees}deg)`;

              const hour = now.getHours();
              const hourDegrees = ((hour / 60) * 360) + 90;
              hourHand.style.transform = `rotate(${hourDegrees}deg)`;
          }
          setInterval(setDate, 1000);
      </script>
