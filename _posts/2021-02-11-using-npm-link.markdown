---
layout: post
title:  "Usando npm link"
date:   2021-02-11 08:50:25
categories: general
tags: node, npm, yarn, package, npm link, yarn
---
Hoje é praticamente impossível criar uma aplicação node sem que você use ou instale algum pacote que pode facilitar muito a vida do desenvolvedor pelos mais variados motivos. 
Seja para usar um framework de testes, se conectar com os mais variados protocolos de rede, usar o SDK de uma API, manipular determinados tipos de arquivos, e assim segue uma lista quase que sem fim.

<p>E no caso dos desenvolvedores que criam tais pacotes ou até mesmo em casos que você está debugando um pacote em específico, existe um comando muito útil na hora de testar/debugar seus pacotes, e existe tanto para o npm quanto para o yarn, que é o "link".

O "npm link" ou o "yarn link" faz um link simbólico entre a pasta do pacote que você está debugando/testando e a aplicação que importa este pacote. Dessa forma, a aplicação que usa o pacote em questão não estará mais apontando para o pacote dentro de node_modules e sim para a pasta que você está indicando através do "link".

Por exemplo, você tem o pacote "the-wesdias-package" e quer importá-lo no projeto the-wesdias-project, 
você pode rodar o seguinte comando a partir da pasta do pacote pelo terminal: npm link

Em seguida, você deve rodar o seguinte comando no terminal a partir da pasta the-wesdias-project: npm link the-wesdias-package

Atenção, pois deve ser o nome do pacote indicado no package.json da dependência;
Outro detalhe, especialmente para aqueles que usam gerenciadores de versão para o node (como o nvm ou asdf), ambos os comandos devem ser executados usando a mesma versão do node.