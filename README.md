# Totem Interativo VerticalParts

Experiencia web vertical 9:16 criada para apresentacao institucional da VerticalParts em feiras, recepcoes, showrooms e pontos de atendimento comercial. O projeto entrega uma navegacao touch-first para telas de 42 polegadas, com foco em impacto visual, leitura rapida e exposicao organizada de produtos, diferenciais e obras entregues.

## Visao Geral

O totem funciona como uma vitrine digital autocontida. Ele abre em tela cheia, conduz o visitante por menus grandes e objetivos, exibe a proposta da VerticalParts e prepara uma galeria com 55 espacos de clientes para substituicao progressiva por obras reais.

O design foi pensado para o contexto de transporte vertical: contraste alto, amarelo institucional, tipografia direta, imagens em destaque e botoes dimensionados para interacao por toque.

## Proposta de Valor

- Apresentar a VerticalParts de forma profissional em eventos e ambientes comerciais.
- Reduzir dependencia de apresentacoes manuais durante atendimento em feira.
- Organizar produtos, diferenciais e cases em uma experiencia unica.
- Permitir atualizacao simples de fotos e textos sem alterar a estrutura principal.
- Operar como site estatico, facil de hospedar na Hostinger, GitHub Pages ou qualquer servidor web.

## Principais Recursos

- Layout vertical 9:16 com resolucao ideal de 1080 x 1920.
- Navegacao touch otimizada para totem de 42 polegadas.
- Tela inicial com chamada institucional e retorno automatico por inatividade.
- Menu com acesso a Produtos, Obras Entregues, Diferenciais e Contato.
- Galeria preparada para 55 clientes.
- Modal de detalhes para cada obra.
- Configuracao por arquivos JSON.
- Assets locais, sem dependencia de backend.
- Fallback visual caso imagens de cliente ainda nao tenham sido substituidas.

## Estrutura do Projeto

```text
.
|-- index.html
|-- LEIA-ME.txt
|-- config
|   |-- clientes.json
|   `-- totem.json
`-- assets
    |-- demo_escada_close.jpg
    |-- demo_escada_full.jpg
    `-- clientes
        |-- cliente_01
        |-- cliente_02
        |-- ...
        `-- cliente_55
```

## Conteudo Editavel

### Configuracao do Totem

O arquivo `config/totem.json` concentra informacoes gerais do projeto:

- nome da empresa;
- site institucional;
- timeout de inatividade;
- modo de uso;
- resolucao ideal.

### Cadastro de Clientes

O arquivo `config/clientes.json` controla os dados exibidos na galeria:

- identificador do cliente;
- nome;
- cidade e UF;
- categoria;
- escopo;
- descricao;
- imagem de capa;
- miniatura;
- imagens complementares.

Cada cliente possui uma pasta em `assets/clientes/cliente_XX`. A estrutura esperada e:

```text
assets/clientes/cliente_01/
|-- capa.jpg
|-- thumb.jpg
|-- 001.jpg
|-- 002.jpg
|-- 003.jpg
|-- metadata.json
`-- LEIA-ME.txt
```

## Como Executar Localmente

Por usar `fetch()` para carregar os arquivos JSON, o ideal e servir o projeto por HTTP em vez de abrir o `index.html` diretamente pelo explorador de arquivos.

Com Python:

```powershell
python -m http.server 8000
```

Depois acesse:

```text
http://localhost:8000
```

## Publicacao

O projeto pode ser publicado como site estatico. Na Hostinger, basta enviar todo o conteudo da raiz deste repositorio para a pasta publica do dominio ou subdominio.

Tambem pode ser usado com GitHub Pages apontando para:

- branch: `main`;
- pasta: `/`;
- arquivo principal: `index.html`.

## Personalizacao Recomendada

1. Substituir as imagens demonstrativas por fotos reais de obras.
2. Atualizar `config/clientes.json` com nomes, cidades, categorias e descricoes reais.
3. Trocar o QR Code demonstrativo por um QR oficial de WhatsApp, formulario ou pagina comercial.
4. Ajustar o tempo de retorno automatico em `config/totem.json`, se necessario.
5. Testar em monitor vertical 1080 x 1920 antes da feira.

## Contexto de Portifolio

Este projeto demonstra uma aplicacao institucional leve, visual e operacionalmente pronta para uso em ambiente fisico. A solucao combina front-end estatico, configuracao por dados externos e design orientado a interacao presencial, criando uma ferramenta comercial reutilizavel para eventos, apresentacoes e recepcao de clientes.

## Stack

- HTML5
- CSS3
- JavaScript vanilla
- JSON
- Arquitetura estatica

## Status

Versao inicial preparada com 55 slots de clientes, conteudo demonstrativo e estrutura pronta para personalizacao comercial da VerticalParts.
