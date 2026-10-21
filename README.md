# nermin-s-animation-
my first ever animtion :p
```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>My Unconscious ~ Conscious</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background: #100b16;
    color: #f5d9ed;
    font-family: Georgia, serif;
    min-height: 100vh;
    overflow-x: hidden;
}

.universe {
    position: relative;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    padding: 40px 20px;
}

.stars {
    position: absolute;
    inset: 0;
    pointer-events: none;
    background-image:
        radial-gradient(2px 2px at 20% 30%, #fff 50%, transparent 100%),
        radial-gradient(1px 1px at 70% 20%, #f5c6ed 50%, transparent 100%),
        radial-gradient(2px 2px at 80% 70%, #fff 50%, transparent 100%),
        radial-gradient(1px 1px at 30% 80%, #e7a8df 50%, transparent 100%),
        radial-gradient(1px 1px at 50% 50%, #fff 50%, transparent 100%);
    background-size: 240px 240px;
    animation: starsMove 35s linear infinite;
}

@keyframes starsMove {
    from { transform: translateY(0); }
    to { transform: translateY(-240px); }
}

.moon {
    position: relative;
    width: 100px;
    height: 100px;
    border-radius: 50%;
    background: #f8e7ee;
    box-shadow: 0 0 25px #e9a8db, 0 0 70px #a45caa;
    margin-bottom: 40px;
    animation: moonFloat 5s ease-in-out infinite;
}

.moon::after {
    content: "";
    position: absolute;
    width: 90px;
    height: 90px;
    border-radius: 50%;
    background: #100b16;
    top: -12px;
    left: 30px;
}

@keyframes moonFloat {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-14px); }
}

h1 {
    position: relative;
    text-align: center;
    font-size: clamp(2rem, 6vw, 4rem);
    font-weight: normal;
    letter-spacing: 3px;
    text-shadow: 0 0 20px #c47dbd;
    margin-bottom: 15px;
}

.subtitle {
    position: relative;
    text-align: center;
    color: #c7a5c7;
    font-size: 1rem;
    letter-spacing: 3px;
    margin-bottom: 50px;
}

.orbit {
    position: relative;
    width: 220px;
    height: 220px;
    border: 1px solid #775178;
    border-radius: 50%;
    animation: rotate 18s linear infinite;
    margin-bottom: 45px;
}

.orbit::before,
.orbit::after {
    content: "";
    position: absolute;
    border: 1px solid #49334e;
    border-radius: 50%;
}

.orbit::before {
    inset: 20px -20px;
}

.orbit::after {
    inset: -20px 20px;
}

@keyframes rotate {
    to { transform: rotate(360deg); }
}

.hare {
    position: absolute;
    top: -20px;
    left: calc(50% - 15px);
    font-size: 32px;
    filter: drop-shadow(0 0 10px #f1b7e8);
    animation: counterRotate 18s linear infinite;
}

@keyframes counterRotate {
    to { transform: rotate(-360deg); }
}

.core {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 45px;
    animation: pulse 3s ease-in-out infinite;
    filter: drop-shadow(0 0 15px #df8fd1);
}

@keyframes pulse {
    0%, 100% { opacity: 0.65; transform: translate(-50%, -50%) scale(1); }
    50% { opacity: 1; transform: translate(-50%, -50%) scale(1.2); }
}

.message {
    position: relative;
    max-width: 520px;
    text-align: center;
    line-height: 2;
    color: #d5bfd8;
    font-size: 1.05rem;
    margin-bottom: 35px;
}

button {
    position: relative;
    background: transparent;
    color: #f2c9e9;
    border: 1px solid #b77bb2;
    padding: 13px 24px;
    font-family: Georgia, serif;
    font-size: 1rem;
    cursor: pointer;
    letter-spacing: 1px;
    transition: 0.4s;
}

button:hover {
    background: #b77bb2;
    color: #100b16;
    box-shadow: 0 0 25px #b77bb2;
}

#secret {
    position: relative;
    max-width: 500px;
    text-align: center;
    margin-top: 25px;
    line-height: 1.8;
    color: #f5c9ed;
    opacity: 0;
    transition: opacity 1.5s;
}

#secret.show {
    opacity: 1;
}

footer {
    position: relative;
    margin-top: 55px;
    font-size: 0.8rem;
    color: #826887;
    letter-spacing: 2px;
    text-align: center;
}
</style>
</head>

<body>
<div class="universe">
    <div class="stars"></div>

    <div class="moon"></div>

    <h1>My Unconscious ~ Conscious</h1>
    <p class="subtitle">A SMALL UNIVERSE OF THINGS UNSEEN</p>

    <div class="orbit">
        <div class="hare">🐇</div>
        <div class="core">✧</div>
    </div>

    <p class="message">
        Somewhere between equations and dreams,<br>
        between the things I know and the things I seek,<br>
        there is a universe that belongs only to me.
    </p>

    <button onclick="reveal()">Discover what lies beneath ✧</button>

    <p id="secret">
        I am not only what happened to me,<br>
        nor what I have yet to become.<br><br>
        I am the questions I keep asking,<br>
        the worlds I have not seen,<br>
        the knowledge I have not found,<br>
        and the life I have yet to discover.
    </p>

    <footer>STILL BECOMING · STILL EXPLORING</footer>
</div>

<script>
function reveal() {
    document.getElementById("secret").classList.toggle("show");
}
</script>
</body>
</html>
```

