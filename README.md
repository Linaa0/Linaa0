<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Linaa's Profile</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;700&display=swap');

  body {
    background-color: #0a0a0a;
    color: #e0e0e0;
    font-family: 'Fira Code', monospace;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 2rem;
    line-height: 1.6;
  }

  .glow-text {
    color: #1e3a8a; /* dark blue */
    text-shadow: 0 0 5px #1e3a8a, 0 0 10px #1e3a8a, 0 0 20px #1e3a8a;
    font-size: 2.2rem;
    font-weight: bold;
    margin-bottom: 1rem;
  }

  .typing {
    font-size: 1rem;
    color: #f5f5f5;
    border-right: 2px solid #1e3a8a;
    white-space: nowrap;
    overflow: hidden;
  }

  .quote {
    margin-top: 2rem;
    font-style: italic;
    color: #a0a0a0;
  }

  .skills {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-top: 1rem;
  }

  .skill {
    background-color: #111;
    color: #fff;
    padding: 0.3rem 0.6rem;
    border-radius: 0.3rem;
    font-size: 0.85rem;
    transition: 0.3s all;
  }

  .skill:hover {
    background-color: #1e3a8a;
    box-shadow: 0 0 5px #1e3a8a;
    cursor: default;
  }

  .socials {
    margin-top: 1.5rem;
    font-size: 0.9rem;
  }

  .socials span {
    margin-right: 1rem;
    color: #f5f5f5;
    text-decoration: underline;
  }
</style>
</head>
<body>

<div class="glow-text">Hey there! I'm Linaa</div>

<div class="typing" id="typing"></div>

<div class="skills">
  <div class="skill">HTML5</div>
  <div class="skill">CSS3</div>
  <div class="skill">JavaScript</div>
  <div class="skill">Bash Script</div>
  <div class="skill">PowerShell</div>
  <div class="skill">Windows Terminal</div>
  <div class="skill">PHP</div>
  <div class="skill">Apache</div>
  <div class="skill">Canva</div>
  <div class="skill">Figma</div>
  <div class="skill">Git</div>
  <div class="skill">GitHub</div>
  <div class="skill">Arduino</div>
  <div class="skill">XFCE</div>
</div>

<div class="socials">
  <span>Instagram</span>
  <span>Email</span>
</div>

<div class="quote">"Beware of bugs in the above code; I have only proved it correct, not tried it.” – Donald Knuth</div>

<script>
const texts = [
  "I'm a curious coder who loves turning ideas into reality.",
  "From writing clean, elegant code to exploring the latest in tech.",
  "I thrive on building projects that make life easier and more fun.",
  "I never shy away from a challenge—if it’s impossible, it's just another project waiting to happen."
];

let count = 0;
let index = 0;
let currentText = '';
let letter = '';

(function type(){
  if(count === texts.length){
    count = 0;
  }
  currentText = texts[count];
  letter = currentText.slice(0, ++index);
  document.getElementById('typing').textContent = letter;
  if(letter.length === currentText.length){
    count++;
    index = 0;
    setTimeout(type, 1500);
  } else {
    setTimeout(type, 70);
  }
})();
</script>

</body>
</html>
