# 🐍 Snake Arcade

## 📌 Sobre o Projeto

O **Snake Arcade** é um jogo inspirado no clássico jogo da cobrinha (*Snake Game*), desenvolvido com tecnologias web. O objetivo é controlar a cobra, coletar frutas para aumentar a pontuação e evitar colisões com as paredes ou com o próprio corpo.

O jogo possui uma interface moderna, com tema escuro, elementos visuais coloridos, placar de pontuação, recorde salvo no navegador e controles adaptados para computadores e dispositivos móveis.

O projeto foi desenvolvido utilizando **HTML5, CSS3 e JavaScript puro (Vanilla JavaScript)**, sem a necessidade de frameworks ou bibliotecas externas.

## 🎯 Objetivos do Projeto

- Desenvolver uma versão web do clássico jogo da cobrinha.
- Aplicar conceitos de lógica de programação e desenvolvimento web.
- Utilizar JavaScript para implementar as regras e a mecânica do jogo.
- Criar uma interface responsiva e intuitiva.
- Permitir a interação por teclado, botões e gestos de toque.
- Armazenar o recorde do jogador no navegador.

## 🛠️ Tecnologias Aplicadas

### 1. HTML5

O HTML5 é utilizado para estruturar a interface e os elementos do jogo.

Principais recursos utilizados:

- Estrutura semântica com elementos como `<main>`, `<h1>`, `<p>` e `<button>`.
- Elemento `<canvas>` para desenhar a área do jogo.
- Elementos HTML para exibir a pontuação e o recorde.
- Botões para iniciar, pausar e reiniciar a partida.
- Elementos de interface para exibir mensagens de estado do jogo.
- Atributos para identificação e manipulação dos elementos pelo JavaScript.

### 2. CSS3

O CSS3 é responsável pela aparência visual e pela organização dos elementos na tela.

Principais recursos utilizados:

- Layout com Flexbox para alinhamento e distribuição dos elementos.
- CSS Grid para organizar os controles direcionais.
- Design responsivo com dimensões flexíveis.
- Propriedade `aspect-ratio` para manter a proporção quadrada do tabuleiro.
- Cores personalizadas para a cobra, as frutas, os botões e a interface.
- Bordas arredondadas e espaçamentos para melhorar a experiência visual.
- Pseudoclasses como `:active` e `:focus-visible` para melhorar a interação com os botões.
- Mediação da interação por toque utilizando `touch-action`.

O layout foi desenvolvido para funcionar em diferentes tamanhos de tela, incluindo computadores e dispositivos móveis.

### 3. JavaScript (Vanilla JavaScript)

O JavaScript implementa a lógica e o funcionamento do jogo, controlando os movimentos da cobra, a geração das frutas, a pontuação e as condições de vitória ou derrota.

Principais recursos utilizados:

- Manipulação do DOM por meio de `document.getElementById()` e `document.querySelectorAll()`.
- Eventos de clique para controlar os botões.
- Eventos de teclado para movimentar a cobra e pausar o jogo.
- Eventos de toque para detectar gestos direcionais em dispositivos móveis.
- Estruturas condicionais para verificar colisões e estados do jogo.
- Arrays e objetos para representar a cobra e as direções.
- Funções para organizar a lógica e facilitar a manutenção do código.
- `Math.random()` para posicionar as frutas aleatoriamente.
- `localStorage` para armazenar o recorde do jogador.
- `requestAnimationFrame()` para executar o ciclo de atualização e renderização.
- `performance`-based timing fornecido pelo parâmetro de tempo do ciclo de animação para controlar a velocidade do jogo.

O código utiliza o modo estrito com `"use strict"`, ajudando a evitar determinados erros de programação.

### 4. HTML5 Canvas

O elemento `<canvas>` é utilizado para desenhar os elementos gráficos do jogo.

A renderização é realizada com a API Canvas 2D, acessada por meio de `getContext("2d")`.

O tabuleiro possui uma resolução lógica de 600 × 600 pixels, dividida em uma grade de 20 × 20 células. Cada célula possui 30 pixels.

Os elementos desenhados incluem:

- Fundo do tabuleiro.
- Linhas da grade.
- Corpo da cobra.
- Cabeça da cobra.
- Fruta que deve ser coletada.

O Canvas permite atualizar os elementos gráficos dinamicamente sem precisar criar um elemento HTML individual para cada segmento da cobra ou para cada fruta.

### 5. Web Storage API — LocalStorage

A API `localStorage` é utilizada para salvar o recorde do jogador no próprio navegador.

O recorde é armazenado com a chave `snakeRecord`.

Quando o jogo é carregado, o sistema tenta recuperar o valor salvo. Durante a partida, se a pontuação atual superar o recorde, o novo valor é armazenado automaticamente.

Esse mecanismo permite que o recorde continue disponível mesmo depois de atualizar ou fechar a página, desde que os dados do navegador não sejam removidos e o jogo seja acessado na mesma origem.

## 🎮 Como Jogar

### 1. Iniciando o Jogo

1. Abra a página do jogo no navegador.
2. Clique no botão **COMEÇAR JOGO**.
3. A cobra aparecerá no tabuleiro e começará a se movimentar.
4. Utilize os controles para direcionar a cobra até as frutas.

### 2. Objetivo

O objetivo é coletar o maior número possível de frutas e alcançar a maior pontuação.

Cada fruta coletada adiciona **10 pontos** à pontuação atual.

Ao comer uma fruta:
- A pontuação aumenta em 10 pontos.
- A cobra cresce.
- Uma nova fruta aparece em uma posição livre do tabuleiro.

Quanto mais frutas forem coletadas, maior será a cobra e mais difícil será evitar colisões.

### 3. Controles no Computador

A movimentação pode ser realizada utilizando as setas do teclado ou as teclas WASD.

| Ação | Teclas |
|---|---|
| Mover para cima | `↑` ou `W` |
| Mover para baixo | `↓` ou `S` |
| Mover para a esquerda | `←` ou `A` |
| Mover para a direita | `→` ou `D` |
| Pausar ou continuar | `Espaço` |

**Atenção:** não é permitido inverter diretamente a direção da cobra. Por exemplo, se ela estiver indo para a direita, não poderá virar imediatamente para a esquerda.

Essa regra evita movimentos diretamente contrários à direção atual.

### 4. Controles em Celulares e Tablets

O jogo oferece duas formas de movimentação em dispositivos com tela sensível ao toque.

**Botões direcionais:**
- ▲ Para cima.
- ▼ Para baixo.
- ◀ Para a esquerda.
- ▶ Para a direita.

**Gestos na tela:**

Também é possível deslizar o dedo sobre a área do tabuleiro para mudar a direção da cobra.

O jogo identifica se o movimento foi predominantemente horizontal ou vertical e determina a direção correspondente.

### 5. Pausar e Continuar

Para interromper temporariamente a partida:

1. Clique no botão **Pausar** ou pressione a tecla `Espaço`.
2. O jogo exibirá a tela de pausa.
3. Para continuar, clique em **CONTINUAR** ou utilize novamente o controle de pausa.

Enquanto estiver pausado, a cobra não continuará avançando.

### 6. Reiniciar a Partida

Para começar uma nova partida, clique no botão **Reiniciar**.

A pontuação atual será zerada, a cobra retornará à posição inicial e uma nova fruta será gerada.

O recorde salvo anteriormente será mantido.

### 7. Condições de Derrota

A partida termina quando a cobra colide com:

- Uma das bordas do tabuleiro.
- O próprio corpo.

Quando ocorre uma colisão, a tela de fim de jogo é exibida com a pontuação alcançada e o recorde atual.

Clique em **JOGAR NOVAMENTE** para iniciar outra partida.

### 8. Condição de Vitória

O jogador vence quando a cobra ocupa todas as posições disponíveis do tabuleiro, não restando nenhuma célula livre para gerar outra fruta.

Nesse caso, o jogo exibe a mensagem **VOCÊ VENCEU!**.

## ⚙️ Funcionamento Interno do Jogo

### Representação do Tabuleiro

O tabuleiro é representado por uma grade de 20 linhas e 20 colunas, totalizando 400 células.

Cada posição é representada por coordenadas `x` e `y`.

A cobra é armazenada em um array de objetos, no qual cada objeto representa um segmento do corpo.

Exemplo:

```javascript
let snake = [
    { x: 8, y: 10 },
    { x: 7, y: 10 },
    { x: 6, y: 10 }
];
```

O primeiro elemento representa a cabeça da cobra, enquanto os elementos seguintes representam o restante do corpo.

### Movimentação

A movimentação ocorre em etapas.

Em cada atualização, o jogo calcula a nova posição da cabeça com base na direção atual.

Se a movimentação for válida, a nova posição é adicionada ao início do array.

Quando a cobra não come uma fruta, o último segmento é removido, mantendo o tamanho do corpo.

Quando come uma fruta, o último segmento não é removido, fazendo com que a cobra cresça.

### Geração das Frutas

A fruta é posicionada aleatoriamente em uma célula que não esteja ocupada pela cobra.

O sistema percorre as posições do tabuleiro, identifica as células livres e seleciona uma delas aleatoriamente.

Isso evita que uma fruta apareça sobre o corpo da cobra.

### Detecção de Colisões

Antes de atualizar a posição da cobra, o jogo verifica se a nova posição da cabeça ultrapassa os limites do tabuleiro.

Também verifica se a cabeça colide com algum segmento do corpo.

Se uma dessas condições ocorrer, a partida é encerrada.

### Controle de Velocidade

A velocidade da cobra é ajustada de acordo com a pontuação.

A duração do intervalo entre os movimentos é calculada pela seguinte expressão:

```javascript
const speed = Math.max(75, 155 - score * 0.3);
```

À medida que a pontuação aumenta, o intervalo diminui e a cobra se movimenta mais rapidamente.

O intervalo mínimo é de 75 milissegundos.

Esse mecanismo aumenta progressivamente a dificuldade do jogo.

### Ciclo de Animação

A função `requestAnimationFrame()` é responsável por manter o ciclo de animação.

Durante esse ciclo, o jogo verifica seu estado, controla o tempo entre os movimentos, atualiza a lógica quando necessário e redesenha o tabuleiro.

Essa abordagem permite separar a atualização lógica da renderização visual.

### Estados do Jogo

O funcionamento é controlado pela variável `state`, que pode assumir os seguintes valores:

| Estado | Descrição |
|---|---|
| `ready` | O jogo está aguardando o início. |
| `playing` | A partida está em andamento. |
| `paused` | A partida está temporariamente pausada. |
| `over` | A partida foi encerrada. |

Essa organização permite controlar quando os movimentos são aceitos, quando a tela de pausa é exibida e quando uma nova partida pode ser iniciada.

## 📁 Estrutura do Projeto

O projeto é composto por um arquivo HTML que reúne a estrutura da página, os estilos CSS e o código JavaScript.

```text
snake-arcade/
└── index.html
```

### `index.html`

Arquivo principal do projeto. Contém:

- Estrutura HTML da interface.
- Estilos CSS incorporados na seção `<style>`.
- Lógica JavaScript incorporada na seção `<script>`.
- Tabuleiro de jogo baseado em Canvas.
- Controles de movimentação.
- Exibição da pontuação e do recorde.
- Gerenciamento dos estados da partida.

Como todos os recursos estão reunidos em um único arquivo, não é necessário configurar um processo de compilação ou instalar dependências para executar o jogo.

## ▶️ Como Executar o Projeto

### Método 1 — Abrir Diretamente no Navegador

1. Baixe ou copie o arquivo `index.html` para uma pasta do computador.
2. Localize o arquivo no explorador de arquivos.
3. Abra-o com um navegador moderno, como Google Chrome, Mozilla Firefox, Microsoft Edge ou Safari.
4. Clique em **COMEÇAR JOGO** para iniciar a partida.

### Método 2 — Utilizar o Visual Studio Code

1. Instale o Visual Studio Code, caso ainda não esteja instalado.
2. Abra a pasta que contém o arquivo `index.html`.
3. Abra o arquivo no editor.
4. Execute o arquivo utilizando um servidor local ou uma extensão de visualização, como o Live Server.
5. Acesse a página pelo navegador.

**Observação:** o projeto não utiliza backend, banco de dados ou serviços externos. A lógica do jogo é executada no próprio navegador.

## 📱 Responsividade e Experiência do Usuário

O jogo foi desenvolvido para oferecer uma experiência simples e intuitiva em diferentes dispositivos.

Entre os recursos implementados estão:

- Área de jogo com proporção quadrada.
- Layout centralizado e adaptável à largura da tela.
- Botões com áreas de interação adequadas para toque.
- Controles direcionais para dispositivos móveis.
- Detecção de gestos na área do jogo.
- Indicação visual de pausa e fim de partida.
- Destaque para a pontuação e o recorde.
- Pausa automática quando a página deixa de estar visível durante uma partida.

Esses recursos ajudam a tornar a experiência de jogo mais acessível e consistente.

## 🔒 Armazenamento e Privacidade

O jogo utiliza o armazenamento local do navegador para registrar o recorde.

Não há implementação de servidor, sistema de autenticação ou banco de dados remoto no código fornecido.

A pontuação da partida atual é mantida durante a execução, enquanto o recorde é persistido no `localStorage`.

O recorde não é sincronizado automaticamente entre diferentes navegadores ou dispositivos.

## 🚀 Possíveis Melhorias Futuras

O projeto pode ser expandido com novas funcionalidades, como:

- Efeitos sonoros para coleta de frutas e colisões.
- Diferentes níveis de dificuldade.
- Menu para selecionar a velocidade inicial.
- Temas visuais personalizáveis.
- Novos tipos de frutas e itens especiais.
- Sistema de recordes com histórico de partidas.
- Ranking de jogadores.
- Integração com backend para armazenamento remoto de pontuações.
- Animações adicionais.
- Opção para ativar ou desativar efeitos sonoros.
- Melhorias de acessibilidade.
- Testes automatizados para validar a lógica do jogo.

Essas melhorias são sugestões para futuras versões e não representam funcionalidades já implementadas.

## 📚 Conceitos Aplicados

O desenvolvimento do Snake Arcade envolve conceitos importantes da programação e do desenvolvimento web:

- **Estruturação de páginas:** organização de elementos com HTML5.
- **Estilização de interfaces:** utilização de CSS3 para definir o layout e a aparência visual.
- **Manipulação do DOM:** atualização de elementos da interface com JavaScript.
- **Programação orientada a eventos:** resposta a cliques, teclas e gestos.
- **Estruturas de dados:** utilização de arrays e objetos para representar a cobra e suas posições.
- **Lógica condicional:** verificação de colisões, pontuação e estados da partida.
- **Geração aleatória:** posicionamento das frutas.
- **Animação gráfica:** desenho e atualização do tabuleiro com Canvas 2D.
- **Controle temporal:** gerenciamento do intervalo entre os movimentos.
- **Persistência local:** armazenamento do recorde com `localStorage`.
- **Design responsivo:** adaptação da interface para diferentes tamanhos de tela.

## 🏁 Conclusão

O **Snake Arcade** é um projeto de jogo web que demonstra a aplicação prática de HTML5, CSS3 e JavaScript na criação de uma experiência interativa.

Apesar de sua estrutura simples, o projeto reúne conceitos relevantes, como renderização gráfica, controle de eventos, gerenciamento de estados, detecção de colisões, atualização dinâmica da interface e persistência de dados no navegador.

Sua arquitetura em um único arquivo facilita a execução, o estudo do código e a implementação de novas funcionalidades.

O projeto também serve como base para estudantes e desenvolvedores que desejam praticar lógica de programação e aprofundar seus conhecimentos em desenvolvimento web.
