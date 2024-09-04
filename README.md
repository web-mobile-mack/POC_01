# POC_01
### Estrutura Básica

Para começar a usar o Flexbox, você precisa definir um contêiner flexível. Isso é feito aplicando `display: flex` ao elemento pai. Os elementos filhos dentro desse contêiner se tornam itens flexíveis.

```css
.container {
  display: flex;
}
```

### Propriedades do Contêiner (Elemento Pai)

1. **flex-direction**: Define a direção dos itens no contêiner.
   - `row` (padrão): Alinha os itens em uma linha horizontal.
   - `row-reverse`: Alinha os itens em uma linha horizontal, mas na ordem inversa.
   - `column`: Alinha os itens em uma coluna vertical.
   - `column-reverse`: Alinha os itens em uma coluna vertical, mas na ordem inversa.

   ```css
   .container {
     flex-direction: row;
   }
   ```

2. **justify-content**: Alinha os itens ao longo do eixo principal.
   - `flex-start`: Alinha os itens no início do contêiner.
   - `flex-end`: Alinha os itens no final do contêiner.
   - `center`: Centraliza os itens.
   - `space-between`: Distribui os itens com espaço igual entre eles.
   - `space-around`: Distribui os itens com espaço igual ao redor deles.

   ```css
   .container {
     justify-content: center;
   }
   ```

3. **align-items**: Alinha os itens ao longo do eixo transversal.
   - `flex-start`: Alinha os itens no início do eixo transversal.
   - `flex-end`: Alinha os itens no final do eixo transversal.
   - `center`: Centraliza os itens.
   - `baseline`: Alinha os itens na linha de base do texto.
   - `stretch`: Estica os itens para preencher o contêiner.

   ```css
   .container {
     align-items: stretch;
   }
   ```

4. **flex-wrap**: Define se os itens devem quebrar ou não para a próxima linha.
   - `nowrap` (padrão): Todos os itens ficam em uma única linha.
   - `wrap`: Os itens quebram para a próxima linha se necessário.
   - `wrap-reverse`: Os itens quebram para a próxima linha na ordem inversa.

   ```css
   .container {
     flex-wrap: wrap;
   }
   ```

### Propriedades dos Itens (Elementos Filhos)

1. **flex-grow**: Define a capacidade de um item crescer em relação aos outros.
   - Um valor maior que 0 permite que o item cresça.

   ```css
   .item {
     flex-grow: 1;
   }
   ```

2. **flex-shrink**: Define a capacidade de um item encolher em relação aos outros.
   - Um valor maior que 0 permite que o item encolha.

   ```css
   .item {
     flex-shrink: 1;
   }
   ```

3. **flex-basis**: Define o tamanho inicial de um item antes de o espaço disponível ser distribuído.
   - Pode ser um valor em pixels, porcentagem, etc.

   ```css
   .item {
     flex-basis: 100px;
   }
   ```

4. **align-self**: Permite que um item se alinhe de forma diferente dos outros itens ao longo do eixo transversal.
   - `auto`, `flex-start`, `flex-end`, `center`, `baseline`, `stretch`.

   ```css
   .item {
     align-self: center;
   }
   ```

### Exemplo Completo

Aqui está um exemplo completo que utiliza várias dessas propriedades:

```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
</div>
```

```css
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}

.item {
  flex-grow: 1;
  flex-basis: 100px;
  align-self: flex-start;
}
```
Para praticar e aprender mais sobre Flexbox de uma maneira divertida, você pode usar o [Flexbox Froggy](https://flexboxfroggy.com/)¹. É um jogo interativo onde você ajuda um sapinho a chegar ao seu destino escrevendo código CSS. É uma ótima maneira de reforçar os conceitos de Flexbox enquanto se diverte!

Para mais detalhes, você pode conferir [este guia completo sobre Flexbox](https://www.alura.com.br/artigos/css-guia-do-flexbox)² e [a documentação do MDN](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts_of_flexbox)³.
![flexfroggy](https://github.com/user-attachments/assets/072e7a68-c13a-440d-aa1d-45a18ab1d8f9)


(1) Site Interativo de flexbox: Treino de sintaxe e posição horizontal. 
(2) Flexbox CSS: guia completo, elementos e exemplos | Alura. https://www.alura.com.br/artigos/css-guia-do-flexbox.
(4) Conceitos básicos de flexbox - CSS | MDN - MDN Web Docs. https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts_of_flexbox.
(5) Guia completo de Flexbox - display: flex. https://triangulo.dev/posts/guia-completo-flexbox/.
(6) Aligning Items in a Flex Container - CSS | MDN - MDN Web Docs. https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_flexible_box_layout/Aligning_items_in_a_flex_container.
(7) CSS Flexbox - Um Guia Interativo (Parte 1 - Containers). https://www.treinaweb.com.br/blog/css-flexbox-um-guia-interativo-parte-1-containers/.
(6) github.com. https://github.com/bellshade/HTML-CSS/tree/7d58607325dedb7e3772b21b65adc3aaebdffad7/CSS%2F057%20CSS%20Grid%2FREADME.md.
