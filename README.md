# Hi there 👋, I'm [Your Name] - AWS & DevOps Engineer

![AWS Architecture](https://media.giphy.com/media/3oEjI6SIIHBdRxXI40/giphy.gif)

Welcome to my GitHub portfolio! I build scalable cloud infrastructure and automate everything with DevOps tools.

---

## 🚀 Skills & Tools

| Skill          | GIF                                |
| -------------- | --------------------------------- |
| AWS            | ![AWS](https://media.giphy.com/media/xT9IgG50Fb7Mi0prBC/giphy.gif)  |
| Docker         | ![Docker](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExMTc4NWU4YTFjNzZjNjdkZDBmODk2YTNiZWVjOWUxMTdjN2U0YWEwMyZjdD1n/3o7qDEq2bMbcbPRQ2c/giphy.gif) |
| Kubernetes     | ![Kubernetes](https://media.giphy.com/media/9J7tdYltWyXIY/giphy.gif) |
| CI/CD Pipeline | ![CI/CD](https://media.giphy.com/media/l0MYt5jPR6QX5pnqM/giphy.gif) |
| GitHub Actions | ![GitHub Actions](https://media.giphy.com/media/l0MYGMCbzXtJk1v1K/giphy.gif) |

---

## 🛠️ Experience & Projects

![Infrastructure as Code](https://media.giphy.com/media/l3q2Q0BQp9nG4V7xu/giphy.gif)

- Automated cloud infrastructure deployment using Terraform & AWS CloudFormation.
- Implemented CI/CD pipelines with GitHub Actions, Jenkins & ArgoCD.
- Containerized microservices using Docker and deployed on Kubernetes clusters.
- Monitored applications with Prometheus, Grafana & AWS CloudWatch.

---

## 🎮 Fun Section - Play the Snake Game!

Click on the canvas and use arrow keys to play!

<details>
<summary>▶️ Expand to play</summary>

<script>
  // Snake game code adapted to run as a GitHub README embedded snippet
  var canvas = document.createElement('canvas');
  canvas.width = 300;
  canvas.height = 300;
  canvas.style.border = '1px solid #000';
  document.currentScript.parentNode.appendChild(canvas);
  var ctx = canvas.getContext('2d');
  var grid = 15;
  var count = 0;
  var snake = {
    x: 150,
    y: 150,
    dx: grid,
    dy: 0,
    cells: [],
    maxCells: 4
  };
  var apple = {
    x: 300,
    y: 300
  };
  
  function getRandomInt(min, max) {
    return Math.floor(Math.random() * (max - min)) + min;
  }
  
  document.addEventListener('keydown', function(e) {
    if (e.key === 'ArrowLeft' && snake.dx === 0) {
      snake.dx = -grid;
      snake.dy = 0;
    } else if (e.key === 'ArrowUp' && snake.dy === 0) {
      snake.dx = 0;
      snake.dy = -grid;
    } else if (e.key === 'ArrowRight' && snake.dx === 0) {
      snake.dx = grid;
      snake.dy = 0;
    } else if (e.key === 'ArrowDown' && snake.dy === 0) {
      snake.dx = 0;
      snake.dy = grid;
    }
  });
  
  function loop() {
    requestAnimationFrame(loop);
    if (++count < 4) {
      return;
    }
    count = 0;
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    snake.x += snake.dx;
    snake.y += snake.dy;
    
    if (snake.x < 0) {
      snake.x = canvas.width - grid;
    } else if (snake.x >= canvas.width) {
      snake.x = 0;
    }
    
    if (snake.y < 0) {
      snake.y = canvas.height - grid;
    } else if (snake.y >= canvas.height) {
      snake.y = 0;
    }
    
    snake.cells.unshift({x: snake.x, y: snake.y});
    if (snake.cells.length > snake.maxCells) {
      snake.cells.pop();
    }
    
    ctx.fillStyle = 'red';
    ctx.fillRect(apple.x, apple.y, grid-1, grid-1);
    
    ctx.fillStyle = 'green';
    snake.cells.forEach(function(cell, index) {
      ctx.fillRect(cell.x, cell.y, grid-1, grid-1);
      if (cell.x === apple.x && cell.y === apple.y) {
        snake.maxCells++;
        apple.x = getRandomInt(0, canvas.width/grid) * grid;
        apple.y = getRandomInt(0, canvas.height/grid) * grid;
      }
      for (var i = index + 1; i < snake.cells.length; i++) {
        if (cell.x === snake.cells[i].x && cell.y === snake.cells[i].y) {
          snake.x = 150;
          snake.y = 150;
          snake.cells = [];
          snake.maxCells = 4;
          snake.dx = grid;
          snake.dy = 0;
          apple.x = getRandomInt(0, canvas.width/grid) * grid;
          apple.y = getRandomInt(0, canvas.height/grid) * grid;
        }
      }
    });
  }
  
  requestAnimationFrame(loop);
</script>

</details>

---

Thanks for visiting my profile! Let's connect and build amazing cloud solutions together.  
[LinkedIn](https://www.linkedin.com/in/yourprofile) | [Twitter](https://twitter.com/yourhandle)

