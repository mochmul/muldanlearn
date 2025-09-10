<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link
        href="https://fonts.googleapis.com/css2?family=Nunito+Sans:ital,opsz,wght@0,6..12,200..1000;1,6..12,200..1000&family=Raleway:ital,wght@0,100..900;1,100..900&display=swap"
        rel="stylesheet">
    <link href="style.css" rel="stylesheet" />

    <title>My test page</title>

    <script async src="scripts/main.js"></script>

    html {
    font-size: 10px;
    font-family: "Nunito Sans", sans-serif;
    background-color: #829fb9;
}

body {
    width: 600px;
    margin: 0 auto;
    background-color: #ff9500;
    padding: 0 20px 20px 20px;
    border: 5px solid black;
}

h1 {
    margin: 0;
    padding: 20px 0;
    color: #829fb9;
    text-shadow: 3px 3px 1px black;
    font-size: 60px;
    text-align: center;
}

img {
    display: block;
    margin: 0 auto;
    max-width: 100%;
}

p,
li {
    font-size: 16px;
    line-height: 2;
    letter-spacing: 1px;
}

const myImage = document.querySelector("img");

myImage.addEventListener("click", () => {
    const mySrc = myImage.getAttribute("src");
    if (mySrc === "images/icon_2.png") {
        myImage.setAttribute("src", "images/icon.png");
    } else {
        myImage.setAttribute("src", "images/icon_2.png");
    }
});

let myButton = document.querySelector("button");
let myHeading = document.querySelector("h1");

function setUserName() {
    const myName = prompt("Please enter your name.");
    if (!myName) {
        setUserName();
    } else {
        localStorage.setItem("name", myName);
        myHeading.textContent = `Color is cool, ${myName}`;
    }
}

if (!localStorage.getItem("name")) {
    setUserName();
} else {
    const storedName = localStorage.getItem("name");
    myHeading.textContent = `Color is cool, ${storedName}`;
}

myButton.addEventListener("click", () => {
    setUserName();
});
</head>

<body>
    <h1>Coloring Is Freedom</h1>

    <img src="images/icon.png" alt="My test image" />
    <p>At Color, something of freedom coloring of</p>

    <ul>
        <li>red</li>
        <li>blue</li>
        <li>yellow</li>
        <li>green</li>
        <li>and so on</li>
    </ul>

    <p>Coloring making everything colorfully, look likes your imagine. And these are making by God, and God is one just
        Allah.</p>

    <p>everything <a
            href="https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.yec.co.id%2Finggris%2Fnama-nama-warna-dalam-bahasa-inggris%2F&psig=AOvVaw2aZvXPFX7434KAL5C96MRN&ust=1757404093598000&source=images&cd=vfe&opi=89978449&ved=0CBEQjRxqFwoTCPDirc7WyI8DFQAAAAAdAAAAABAE">Coloring,
        </a>human, animals, plants and so on</p>

        <button>Change user</button>
</body>

</html>
