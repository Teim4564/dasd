<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>My Roblox Portfolio</title>
<style>
  /* Background gradient animation */
  @keyframes bgGradient {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
  }

  body {
    margin: 0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(270deg, #1e1e2f, #1e2e3f, #1e1e2f);
    background-size: 600% 600%;
    animation: bgGradient 20s ease infinite;
    color: #f0f0f0;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }

  /* Subtle floating animations */
  @keyframes floatSlow {
    0%, 100% { transform: translate(0, 0); }
    50% { transform: translate(0, -6px); }
  }

  @keyframes floatSideToSide {
    0%, 100% { transform: translateX(0); }
    50% { transform: translateX(5px); }
  }

  header {
    background-color: #202225;
    padding: 2rem;
    text-align: center;
    box-shadow: 0 4px 10px rgba(0, 191, 255, 0.3);
    animation: floatSlow 6s ease-in-out infinite;
  }

  header h1 {
    margin: 0;
    font-size: 2.8rem;
    color: #00bfff;
    text-shadow:
      0 0 6px #00bfff88,
      0 0 12px #00bfff44;
    animation: floatSideToSide 8s ease-in-out infinite;
  }

  header p {
    font-size: 1.2rem;
    margin-top: 0.5rem;
    color: #bbbbbb;
  }

  .projects {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    padding: 3rem;
    flex-grow: 1;
  }

  /* Project card with subtle glow and floating */
  @keyframes cardFloat {
    0%, 100% { transform: translate(0, 0); box-shadow: 0 0 10px rgba(0, 191, 255, 0.4); }
    50% { transform: translate(0, -8px); box-shadow: 0 0 15px rgba(0, 191, 255, 0.6); }
  }

  .project-card {
    background-color: #2c2f33;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 0 10px rgba(0, 191, 255, 0.4);
    transition: transform 0.2s ease, box-shadow 0.3s ease;
    animation: cardFloat 7s ease-in-out infinite;
  }

  .project-card:hover {
    transform: scale(1.04);
    /* keep glow subtle, no bigger glow on hover */
  }

  .project-info {
    padding: 1.5rem;
  }

  .project-info h2 {
    margin: 0 0 0.5rem;
    font-size: 1.7rem;
    color: #00bfff;
    text-shadow:
      0 0 4px #00bfff88,
      0 0 8px #00bfff44;
    animation: floatSideToSide 10s ease-in-out infinite;
  }

  .project-info p {
    color: #ccc;
  }

  /* Button shimmer effect */
  @keyframes shimmer {
    0% { background-position: -150% 0; }
    100% { background-position: 150% 0; }
  }

  .project-info a {
    display: inline-block;
    margin-top: 1rem;
    color: #ffffff;
    text-decoration: none;
    background: linear-gradient(270deg, #00bfff, #00ffff, #00bfff);
    background-size: 300% 100%;
    padding: 0.6rem 1.4rem;
    border-radius: 6px;
    transition: background-color 0.3s;
    animation: shimmer 4s linear infinite;
    box-shadow: 0 0 6px #00bfff88;
  }

  .project-info a:hover {
    background-color: #008ecc;
    animation-play-state: paused;
    box-shadow: 0 0 10px #008eccbb;
  }

  footer {
    background-color: #202225;
    text-align: center;
    padding: 1.5rem 0;
    font-size: 1.1rem;
    color: #66ccff;
    text-shadow:
      0 0 5px #66ccff66,
      0 0 10px #00bfff55;
    box-shadow: 0 -4px 12px rgba(0, 191, 255, 0.4);
    user-select: none;
    font-weight: 600;
    letter-spacing: 0.03em;
    animation: floatSlow 6s ease-in-out infinite;
  }

  @media (max-width: 800px) {
    .projects {
      grid-template-columns: 1fr;
    }
  }
</style>
</head>
<body>
  <header>
    <h1>My Roblox Portfolio</h1>
    <p>been scripting with lua for 1 year. Here are some of my released projects.</p>
  </header>

  <section class="projects">
    <div class="project-card">
      <div class="project-info">
        <h2>Steal a Toaster</h2>
        <p>A game inspired by "steal a brainrot" features the same mechanics (still unfinished)</p>
        <a href="https://www.roblox.com/games/94227299214228/Steal-a-toaster" target="_blank">View Game</a>
      </div>
    </div>

    <div class="project-card">
      <div class="project-info">
        <h2>Build a Pizza Tower to Heaven</h2>
        <p>This game you have to build a pizza tower to heaven features mobile support and uses a grid building system</p>
        <a href="https://www.roblox.com/games/91652572472344/Build-a-pizza-tower-to-heaven-Release" target="_blank">View Game</a>
      </div>
    </div>
  </section>

  <footer>
    What I don't do: I don't do physics based systems.
  </footer>
</body>
</html>
