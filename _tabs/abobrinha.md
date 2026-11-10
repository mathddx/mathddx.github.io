---
title: Minha Tela
icon: fas fa-tv
order: 5
---

<div id="player-tela" style="
  background-color: #1a1a1a; 
  background-image: url('{{ "/assets/img/icons/standby.jpg" | relative_url }}'); 
  background-size: cover; 
  background-position: center; 
  max-width: 800px; 
  aspect-ratio: 16/9; 
  margin: 0 auto;
  border-radius: 8px;
  overflow: hidden;
  position: relative;
">
  <iframe 
    src="https://vdo.ninja/?view=nandinho&transparent=1&clean=1&autostart=1" 
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none; background: transparent !important;" 
    allow="autoplay; fullscreen; display-capture"
    allowtransparency="true">
  </iframe>
</div>

<div style="text-align: center; margin-top: 20px; display: flex; justify-content: center; gap: 15px; flex-wrap: wrap;">
  <a href="https://vdo.ninja/?push=nandinho&screenshare" target="_blank" style="
    display: inline-block;
    padding: 10px 20px; 
    background-color: #d9534f; 
    color: white; 
    text-decoration: none; 
    border-radius: 5px; 
    font-weight: bold;
    font-family: sans-serif;
  ">
    <i class="fas fa-video"></i> Iniciar Compartilhamento
  </a>

  <button onclick="document.getElementById('player-tela').requestFullscreen()" style="
    padding: 10px 20px; 
    background-color: #5bc0de; 
    color: white; 
    border: none;
    border-radius: 5px; 
    font-weight: bold;
    font-family: sans-serif;
    cursor: pointer;
  ">
    <i class="fas fa-expand"></i> Tela Cheia
  </button>
</div>
