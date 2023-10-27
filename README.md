<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Webpage</title>
    
    <style>
        body {
            background-color:purple;
        }
		h1 {
            color:black;
        }
        h2 {
            color:black; 
        }
		Main{
		color:white;
		}
        footer {
            color:white; 
        }
    </style>
</head>
<body>
    <header>
        <h1>Sharon Cheptoo</h1>
        <h2>SCT 222-0174/2021</h2>
    </header>
    <main>
        <p>How are you, your welcome to my webpage!</p>
        <img src="C:\Users\USER\Pictures\picture.jpg"width="430" height="440">
        <button id="setColorRed">Set Background Red</button>
        <button id="setColorGreen">Set Background Green</button>
        <button id="setColorBlue">Set Background Blue</button>
		<button id="setColorpurple">Set Background Blue</button>
		
    </main>
    <footer>
        <p>oops nothing much to see here still working on my bio.</p>
    </footer>
    <script>
        function setColorAndStore(color) {
            document.body.style.backgroundColor = color;
            localStorage.setItem("backgroundColor", color);
        }
        function applyStoredColor() {
            const storedColor = localStorage.getItem("backgroundColor");
            if (storedColor) {
                document.body.style.backgroundColor = storedColor;
            }
        }
        document.getElementById("setColorRed").addEventListener("click", function () {
            setColorAndStore("red");
        });

        document.getElementById("setColorGreen").addEventListener("click", function () {
            setColorAndStore("green");
        });

        document.getElementById("setColorBlue").addEventListener("click", function () {
            setColorAndStore("blue");
        });
		document.getElementById("setColor").addEventListener("click", function () {
            setColorAndStore("blue");
        });
        applyStoredColor();
    </script>
</body>
</html>
