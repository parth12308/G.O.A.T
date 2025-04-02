# G.O.A.T
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Global Organisation of Apple and Tobacco</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            padding: 20px;
        }
        #mainContent, #spinGame {
            display: none;
        }
        #mainContent {
            display: block;
        }
        #spinWheel {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            border: 5px solid black;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            background: conic-gradient(
                red 0deg 45deg, 
                yellow 45deg 90deg, 
                green 90deg 135deg, 
                blue 135deg 180deg, 
                orange 180deg 225deg, 
                purple 225deg 270deg, 
                pink 270deg 315deg, 
                cyan 315deg 360deg
            );
            margin: 50px auto;
            position: relative;
            cursor: pointer;
        }
        #message {
            font-size: 24px;
            font-weight: bold;
            margin-top: 20px;
        }
        .button {
            display: inline-block;
            padding: 10px 20px;
            font-size: 18px;
            font-weight: bold;
            color: white;
            background-color: #007BFF;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div id="mainContent">
        <h1>Global Organisation of Apple and Tobacco (G.O.A.T)</h1>
        <p>The Global Organisation of Apple and Tobacco (G.O.A.T) is an international regulatory body dedicated to managing and overseeing the production, distribution, and ethical concerns surrounding apple and tobacco industries. Established in 1892, G.O.A.T has played a crucial role in shaping policies that impact farmers, traders, and consumers worldwide.</p>
        <p>With headquarters in Switzerland, G.O.A.T ensures fair trade practices, promotes sustainable farming, and conducts research on the economic impact of both industries.</p>
        <p>Click below to explore more details about our mission and ongoing projects.</p>
        <button class="button" onclick="startSpinGame()">Click for More Info</button>
    </div>
    
    <div id="spinGame">
        <h1>Global Organisation of Apple and Tobacco (G.O.A.T)</h1>
        <p>Click anywhere to spin the wheel!</p>
        <div id="spinWheel">🎡 Click to Spin 🎡</div>
        <p id="message"></p>
    </div>
    
    <script>
        function startSpinGame() {
            document.getElementById("mainContent").style.display = "none";
            document.getElementById("spinGame").style.display = "block";
        }
        
        const names = ["Chesta", "Divya", "Adhrika", "Prabsimar", "Prishika", "Ms. Bindal", "Avleen"];
        
        document.body.onclick = function() {
            if (document.getElementById("spinGame").style.display === "block") {
                let randomIndex = Math.floor(Math.random() * names.length);
                let selectedName = names[randomIndex];
                document.getElementById("message").innerText = `"${selectedName}" - Rahene de bhaii, koi ni aa rahi`;
            }
        }
    </script>
</body>
</html>
