
<html lang="en"> 
 <head> 
  <meta charset="UTF-8"> 
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
  <title>Sorry na, umuwi ka na Baby</title> 
  <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            width: 100vw;
            font-family: Times New Roman;
            background-color: pink; 
            position: relative; 
            margin: 0; 
        }
        img {
            width: 30%; 
            max-width: 300px;
            height: auto;
            align-items: center;
            justify-content: center;
        }
        button {
            margin: 10px;
            padding: 10px 20px;
            font-size: 2vw;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            background-color: black;
            color: white; 
            border: none;
            border-radius: 5px;
        }
        .no-button {
            background-color: red; 
            color: white; 
            position: absolute;
        }
        h1 {
            font-style: italic; 
            text-align: center; 
            font-size: 3vw; 
        }
    </style> 
 </head> 
 <body> 
  <img id="sadCat" src="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif" alt="Sad Cat"> 
  <h1>I’m sorry please forgive me my Love?</h1> <button id="yesButton">Yes</button> <button id="noButton">No</button> 
  <div id="noButtonsContainer"></div> 
  <script>
        const yesButton = document.getElementById('yesButton');
        const noButton = document.getElementById('noButton');

        yesButton.addEventListener('click', function() {
            document.body.innerHTML = `
                <img src="https://media1.tenor.com/m/xx3n8cnrnGYAAAAd/nyano-nyano-cat.gif" alt="Gif Image">
                <h1><i>Thank you so much for understanding Baby. I love you with all my heart, body, and soul. I regret my actions and will never let it happen again. My sincere apologies, I hope you're doing well right now. I love you wifey ko.</i></h1>
            `;
        });

        noButton.addEventListener('click', function() {
            const newNoButton = document.createElement('button');
            newNoButton.textContent = 'No';
            newNoButton.className = 'no-button'; // Add class for styling
            newNoButton.style.left = Math.random() * 80 + 'vw'; // Random horizontal position
            newNoButton.style.top = Math.random() * 80 + 'vh'; // Random vertical position

            newNoButton.addEventListener('click', function() {
                noButtonsContainer.appendChild(newNoButton.cloneNode(true));
                newNoButton.style.left = Math.random() * 80 + 'vw'; // Randomize position again
                newNoButton.style.top = Math.random() * 80 + 'vh'; // Randomize position again
            });

            document.body.appendChild(newNoButton); // Append new button to body
        });
    </script> 
 </body>
</html>
