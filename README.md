# Cardápio Digital Interativo 🍔🥤

Bem-vindo ao projeto de Cardápio Digital Interativo! Este repositório contém um sistema simples para pedidos online em um restaurante fast food, baseado nos princípios da norma **ISO 9241-110**, que trata da usabilidade e interação eficiente entre usuário e sistema.

## 📌 Sobre o Projeto

Este sistema visa facilitar a escolha e o pedido de alimentos via aplicativo ou site, garantindo uma experiência intuitiva e organizada.

### 🎯 Funcionalidades
✅ Organização dos itens em categorias (ex: Hambúrgueres, Salgados, Bebidas).  
✅ Exibição dos produtos com nome, descrição e preço.  
✅ Seleção de itens com checkboxes para um fluxo de pedido mais prático.  
✅ Escolha da quantidade de cada item.  
✅ Carrinho de compras dinâmico, com opções para adicionar ou remover itens.  
✅ Exibição do valor total do pedido em tempo real.  
✅ Opções de pagamento: Cartão (débito/crédito) ou Pix.  
✅ Confirmação dos dados de entrega antes da finalização do pedido.  

## 🛠️ Tecnologias Utilizadas
Este projeto foi desenvolvido utilizando as seguintes tecnologias:
- **HTML5**: Estrutura do sistema.
- **CSS3**: Estilização básica para melhorar a experiência do usuário.
- **JavaScript**: Implementação da interatividade e lógica do sistema.

## ⚙️ Como o Código foi Desenvolvido

Este projeto foi construído de maneira simples e modular, utilizando **HTML** para estruturar a página, **CSS** para estilizar os elementos e **JavaScript** para implementar a interatividade. A seguir, você encontrará uma explicação detalhada de cada parte do código:

### 1. Estrutura HTML 📄

- **Divisão da Página:**  
  A página foi organizada em três grandes seções:
  - **Menu de Seleção:**  
    Aqui, os itens do cardápio são apresentados e divididos em categorias (Hambúrgueres, Salgados e Bebidas). Cada produto possui um *checkbox* para seleção e um campo para informar a quantidade desejada.
  - **Carrinho de Compras:**  
    Nesta seção, os itens selecionados são exibidos com detalhes como nome, quantidade, preço unitário e subtotal de cada item, além do total do pedido.
  - **Finalização do Pedido:**  
    Permite que o usuário escolha a forma de pagamento (Cartão ou Pix) e informe os dados de entrega (nome e endereço), exibindo também um resumo do pedido para conferência.

- **Atributos Personalizados:**  
  Foram utilizados atributos `data-name` e `data-price` nos elementos de seleção para armazenar informações importantes dos produtos, facilitando a manipulação via JavaScript.

### 2. Estilização com CSS 🎨

- **Organização Visual:**  
  O CSS aplicado tem o objetivo de deixar a interface limpa e organizada. Foram definidas margens, bordas e espaçamentos que melhoram a leitura e a navegação do usuário.
  
- **Controle de Visibilidade:**  
  A classe `.hidden` é utilizada para alternar a exibição das seções (menu, carrinho e finalização), permitindo que apenas a parte relevante seja mostrada conforme a interação do usuário.

### 3. Interatividade com JavaScript 🚀

- **Função `adicionarCarrinho()`:**  
  - Percorre os itens do menu e verifica quais estão selecionados (checkbox marcado).
  - Coleta informações como nome, preço (usando os atributos `data-`) e quantidade, armazenando esses dados em um array chamado `carrinho`.
  - Caso nenhum item seja selecionado, exibe um alerta solicitando a seleção de pelo menos um item.
  - Ao finalizar a seleção, a função oculta a seção do menu e exibe o carrinho de compras.

- **Função `mostrarCarrinho()`:**  
  - Exibe os itens escolhidos, calculando o subtotal de cada um (multiplicando preço pela quantidade) e atualizando o total do pedido.
  - Cada item é adicionado a uma lista para que o usuário visualize claramente os detalhes do seu pedido.

- **Função `voltarMenu()`:**  
  - Permite que o usuário retorne ao menu de seleção, caso deseje adicionar ou alterar algum produto.

- **Função `finalizarPedido()`:**  
  - Prepara a etapa final do pedido, gerando um resumo com todos os itens e o total.
  - Exibe a seção de finalização, onde o usuário pode revisar os dados, escolher a forma de pagamento e inserir as informações de entrega.

- **Funções `confirmarPedido()`, `cancelarPedido()` e `resetarTudo()`:**  
  - **Confirmar Pedido:** Valida os dados de entrega (nome e endereço) e, se tudo estiver correto, exibe uma mensagem de confirmação com os detalhes do pedido.
  - **Cancelar Pedido:** Oferece a opção de cancelar o pedido, reiniciando o processo.
  - **Resetar Tudo:** Limpa o array do carrinho e reseta os campos de seleção e de dados do usuário, retornando à visualização inicial do menu.
