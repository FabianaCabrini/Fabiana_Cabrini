## Olá, eu sou a Fá💮


<div>
  <a href="https://github.com/FabianaCabrini">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=FabianaCabrini&show_icons=true&theme=dracula&include_all_commits=true&count_private=true"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=FabianaCabrini&layout=compact&langs_count=16&theme=dracula"/>

</div>

<div style="display: inline_block"><br>
  <img align="center" alt="Rafa-HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  <img align="center" alt="Rafa-CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
  <img align="center" alt="Rafa-Python" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
  <img align="center" alt="Rafa-Csharp" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg">
</div>
  
  ##
 
<div> 
 
  <a href="https://www.instagram.com/a_cabrini_/_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/fabiana-cabrini-2556001ba" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
  
</div>

### 🐍 Minhas contribuições

<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<title>Cobrinha</title>
<style>
  canvas { background: #000; display: block; margin: auto; }
</style>
</head>
<body>
<canvas id="snake" width="400" height="400"></canvas>
<script>
const canvas = document.getElementById("snake");
const ctx = canvas.getContext("2d");

let grid = 20;
let count = 0;
let snake = [{x:160, y:160}];
let dx = grid;
let dy = 0;
let food = {x:320, y:320};

function gameLoop() {
  requestAnimationFrame(gameLoop);
  if (++count < 4) return;
  count = 0;
  ctx.clearRect(0,0,canvas.width,canvas.height);
  
  // Mover a cobra
  let head = {x: snake[0].x + dx, y: snake[0].y + dy};
  snake.unshift(head);
  
  // Comer comida
  if (head.x === food.x && head.y === food.y) {
    food.x = Math.floor(Math.random()*20)*grid;
    food.y = Math.floor(Math.random()*20)*grid;
  } else {
    snake.pop();
  }

  // Desenhar comida
  ctx.fillStyle = "red";
  ctx.fillRect(food.x, food.y, grid-1, grid-1);
  
  // Desenhar cobra
  ctx.fillStyle = "lime";
  snake.forEach(part => ctx.fillRect(part.x, part.y, grid-1, grid-1));
}

// Controles
document.addEventListener("keydown", e => {
  if (e.key === "ArrowUp" && dy === 0) { dx = 0; dy = -grid; }
  if (e.key === "ArrowDown" && dy === 0) { dx = 0; dy = grid; }
  if (e.key === "ArrowLeft" && dx === 0) { dx = -grid; dy = 0; }
  if (e.key === "ArrowRight" && dx === 0) { dx = grid; dy = 0; }
});

requestAnimationFrame(gameLoop);
</script>
</body>
</html>

<img src="https://raw.githubusercontent.com/FabianaCabrini/FabianaCabrini/output/dist/snake.svg" alt="Snake animation" style="max-width:100%; height:auto;">




