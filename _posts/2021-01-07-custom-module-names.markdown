---
layout: post
title:  "Instalando pacotes node com nome customizado"
date:   2021-01-07 14:22:25
categories: general
tags: node, npm
---
Um dia desses precisei instalar um pacote com seu nome diferente do original. 
Pois tive que usar 2 versões diferentes do mesmo módulo para fins de testes.
<br/>Claro, é um cenário muito específico e raramente temos que fazer isso,
mas caso necessite aqui vai a dica.
<p>Por Exemplo.: Temos o módulo "axios" e queremos fazer um require da versao  0.19 e também da versão 0.21</p>
<p>Podemos fazer da seguinte forma:</p>
>npm i --save old-axios@npm:axios@0.19.0
<br/>
>npm i --save new-axios@npm:axios@0.21.1