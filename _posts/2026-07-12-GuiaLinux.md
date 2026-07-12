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

Depois disso acredito que é só configurar coisas simples tipo atalhos para trocar de área de trabalho, mas boa parte fiz a partir desse [vídeo](https://youtu.be/FIxfPwjlElM?si=rjq_4QgjlG5z2oqa).

## Sway   

Pra o sway, já tem boa parte dos arquivos de config salvos no pendrive, futuramente serão adicionados aqui (quando eu aprender a colocar arquivos para download no site), mas novamente, é so seguir os passos desse [vídeo](https://youtu.be/QAmTUkzpIiM?si=EL7lntQo0MLtZx9h), deve ser mais simples pois já está tudo configurado nos dotfiles, a única coisa que imagino que seja necessária para configuração seja a fonte pa ra que os ícones apareçam, e os pacotes para configuração de wifi e opções de log-out. 

## Konsave

Para o KDE, tentarei utilizar uma ferramenta chamada Konsave, a ideia é que ele consiga importar todas as minhas configurações para a nova instalação do KDE Plasma, apartir [disso]({{"/assets/downloads/tpad.knsv" | relative_url}}).
Após baixar o konsave novamente, via Yay, basta fazer o seguinte:

```sh
konsave -i tpad.knsv 
konsave -a
```

Para atualizar o konsave, basta seguir esse [vídeo](https://www.youtube.com/watch?v=jEVcrPMfXGU&t=80s).

Agora, é só simplesmente formatar o thinkpad de novo, ou então tentar desfazer o btrfs device add, mas não deu certo das últimas vezes.

## Conclusão
No fim, o que foi feito foi adicionar um hd de 1tb, sem misturar ambos pelo btrfs add, pois iria diminuir a velocidade do sistema em geral. 
Sendo assim, foi criada uma pasta no HD

1. Criação da pasta no HD:
```bash
mkdir -p /mnt/dados/pacman/pkg
```
Depois, esse caminho foi adicionado no /etc/pacman.conf
```bash
CacheDir = /mnt/dados/pacman/pkg/ /var/cache/pacman/pkg/
```
2. Analogamente para o Yay:
```bash
mkdir -p /mnt/dados/yay_cache
```
```bash
yay --save --builddir /mnt/dados/yay_cache
```

Ainda não tenho certeza se o sistema irá funcionar tranquilamente, ou se acontecerá algum problema. Em todo caso, todos os arquivos importantes são salvos online e são facilmente recuperáveis!!
Próximo passo é tentar instalar o Quartus utilizando o wine.
