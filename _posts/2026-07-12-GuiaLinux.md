---
title: "Guia Rápido de setup do arch"
date: 2026-07-12
categories: [Código]
tags: [Tutorial]
#author: "Leo"
---

Primeiramente, para combinar os dois SSDs, apenas usei o lsblk pra ver qual era qual, e utilizei essa linha de código para combinar os dois

```sh
sudo btrfs device add /dev/sda /mnt
```

## KDE Plasma
Para transformar o KDE plasma em um tiling window manager, segui as orientações desse [vídeo](https://youtu.be/z-AzbWQM350?si=O3P66WLTeQmEhsQ4), mas vou deixar aqui pra ser mais simples:

- Começando com o KWin scripts e baixando o krohnkite, deixei tudo com espaçamento de 8px
- Removendo os controles superiores de cada página e instalando os plugins de Global Menu, Window Title Fork e Panel Spacer Extended
- Configurando os atalhos de Win+Q e Win+C para terminal e fechar aplicativos, e usando os wallpapers da pasta backup

Depois disso acredito que é só configurar coisas simples tipo atalhos para trocar de área de trabalho, mas boa parte fiz nesse [vídeo](https://youtu.be/FIxfPwjlElM?si=rjq_4QgjlG5z2oqa).

## Sway   

Pra o sway, já tem boa parte dos arquivos de config salvos no pendrive, futuramente serão adicionados aqui (quando eu aprender a colocar arquivos para download no site), mas novamnete, é so seguir os passos desse [vídeo](https://youtu.be/QAmTUkzpIiM?si=EL7lntQo0MLtZx9h), deve ser mais simples pois já está tudo configurado nos dotfiles, a única coisa que imagino que seja necessária para configuração seja a fonte para que os ícones apareçam, e os pacotes para configuração de wifi e opções de log-out. 