# 🍽️ Trindade Restaurante - Sistema de Ecommerce

<div align="center">

**[🌐 Visite o Site](https://blackthornethan23.github.io/site-trindade-restaurante/)**

</div>

---

## 📋 Sobre o Projeto

Trindade Restaurante é uma **plataforma de ecommerce moderna e intuitiva** desenvolvida para restaurantes que desejam oferecer serviço de pedidos online. O sistema foi projetado com foco em **experiência do usuário (UX)**, **responsividade mobile-first** e **facilidade de uso**.

A aplicação integra-se perfeitamente com o **WhatsApp Business**, permitindo que os pedidos sejam finalizados e entregues diretamente ao proprietário do restaurante através de uma conversa automatizada.

---

## ✨ Funcionalidades Principais

### 🛒 Gerenciamento de Carrinho
- ✅ Adicionar/remover itens do carrinho
- ✅ Ajustar quantidade de produtos
- ✅ Visualização em tempo real do total
- ✅ Animação visual ao adicionar produtos (efeito "voar" para o carrinho)
- ✅ Banner flutuante no mobile com acesso rápido ao carrinho

### 🍕 Catálogo de Produtos
- ✅ 6 categorias disponíveis (Pizzas, Massas, Lanches, Sobremesas, Bebidas)
- ✅ Filtragem por categoria
- ✅ Busca por nome ou descrição do prato
- ✅ Exibição responsiva em grid adaptativo
- ✅ 10 produtos de exemplo com imagens de alta qualidade

### 🚚 Opções de Entrega
- **Entrega Domiciliar**: Com cálculo de endereço (CEP, endereço completo)
- **Retirada na Loja**: Com agendamento de data e hora

### 💳 Formas de Pagamento
- ✅ PIX
- ✅ Cartão de Crédito
- ✅ Cartão de Débito
- ✅ Dinheiro (com opção de informar troco)

### 🎟️ Sistema de Cupons
- ✅ Validação de cupom promocional
- ✅ Desconto percentual
- ✅ Feedback visual de sucesso/erro
- ✅ Cupom padrão: `DESCONTO10` (10% de desconto)

### 📱 Design Responsivo
- ✅ Mobile-first
- ✅ Otimizado para tablets e desktops
- ✅ Interface adaptativa em todos os tamanhos de tela

### 🔍 Busca Inteligente
- ✅ Busca em tempo real por nome do prato
- ✅ Busca também na descrição do produto
- ✅ Filtragem integrada com categorias

---

## 🎨 Design e Cores

### Paleta de Cores
```
Cor Primária:      #b33a2f (Vermelho Quente)
Cor Secundária:    #2d201b (Marrom Escuro)
Cor de Destaque:   #f4a261 (Laranja Aquecido)
Texto Principal:   #2f241d (Marrom Escuro)
Fundo:             #f8f4ee (Bege Claro)
```

### Tipografia
- Font Family: `Segoe UI, Tahoma, Geneva, Verdana, sans-serif`
- Ícones: Font Awesome 6.5.1

---

## 📂 Estrutura de Arquivos

```
restaurante-ecommerce/
│
├── index.html          # Estrutura HTML principal
├── script.js           # Lógica JavaScript (interatividade)
├── style.css           # Estilos CSS (design e layout)
└── README.md           # Este arquivo
```

---

## 🚀 Como Usar

### 1️⃣ Abrir o Projeto
Simplesmente abra o arquivo `index.html` em seu navegador:
```bash
# Windows
start index.html

# macOS
open index.html

# Linux
xdg-open index.html
```

### 2️⃣ Navegar no Menu
- 🏠 **Logo**: Clique para voltar ao topo da página
- 🔍 **Busca**: Digite o nome do prato para filtrar
- 📂 **Categorias**: Clique nas abas para filtrar por tipo de comida
- 🛒 **Carrinho**: Veja seus itens selecionados

### 3️⃣ Fazer um Pedido
1. Escolha os pratos desejados
2. Ajuste as quantidades
3. Clique em "Ver Carrinho"
4. Selecione tipo de entrega (entrega ou retirada)
5. Preencha seus dados
6. Selecione forma de pagamento
7. (Opcional) Aplique cupom de desconto
8. Clique em "Finalizar Pedido" para enviar via WhatsApp

---

## 💻 Estrutura do Código

### JavaScript (script.js)

#### Principais Funções:
- `filtrarEMostrarProdutos()` - Filtra produtos por categoria/busca
- `adicionarAoCarrinho()` - Adiciona item ao carrinho com animação
- `atualizarCarrinho()` - Recalcula totais e atualiza UI
- `applyCoupon()` - Valida e aplica cupons de desconto
- `finalizarPedido()` - Gera mensagem e abre WhatsApp
- `abrirCarrinho()` / `fecharCarrinho()` - Controla visibilidade do carrinho

#### Dados de Produtos:
```javascript
{
  id: 1,
  nome: "Pizza Margherita",
  categoria: "pizzas",
  preco: 49.90,
  imagem: "url_da_imagem",
  descricao: "Descrição do prato"
}
```

#### Validação de Cupons:
```javascript
validCoupons = [
  { code: "DESCONTO10", type: "percentage", value: 10 }
]
```

### CSS (style.css)

#### Variáveis CSS Customizáveis:
```css
:root {
  --primary-color: #b33a2f;      /* Vermelho */
  --secondary-color: #2d201b;    /* Marrom */
  --accent-color: #f4a261;       /* Laranja */
  --text-color: #2f241d;         /* Texto */
  --light-gray: #f8f4ee;         /* Fundo */
  --border-color: #eadfd9;       /* Bordas */
  --success-color: #2e8b57;      /* Sucesso */
  --error-color: #d9480f;        /* Erro */
}
```

#### Classes Principais:
- `.products-container` - Grid de produtos responsivo
- `.cart-sidebar` - Menu do carrinho deslizante
- `.cart-overlay` - Overlay semitransparente
- `.product-card` - Card individual do produto

---

## 🔧 Personalização

### Adicionar Novos Produtos
Edite o array `produtos` em `script.js`:

```javascript
{
  id: 11,
  nome: "Seu Prato",
  categoria: "sua_categoria",
  preco: 29.90,
  imagem: "https://seu-link-da-imagem.jpg",
  descricao: "Descrição detalhada"
}
```

### Modificar Cores
Altere as variáveis CSS em `style.css`:

```css
:root {
  --primary-color: #seu_cor_aqui;
}
```

### Adicionar Cupons
Edite o array `validCoupons` em `script.js`:

```javascript
validCoupons = [
  { code: "PRIMEIRACOMPRA", type: "percentage", value: 15 },
  { code: "DESCONTO10", type: "percentage", value: 10 }
]
```

### Alterar Número WhatsApp
Localize a variável `numeroWhatsApp` em `script.js`:

```javascript
const numeroWhatsApp = "55XXXXXXXXXXXX"; // Seu número com código do país
```

---

## 📱 Responsividade

O projeto é totalmente **mobile-first** e otimizado para:
- 📱 Smartphones (320px+)
- 📱 Tablets (768px+)
- 💻 Desktops (1200px+)

#### Breakpoints Principais:
- **Mobile**: até 768px
- **Tablet**: 768px a 1024px
- **Desktop**: 1024px+

---

## 🎯 Fluxo de Pedido

```
Seleção de Produtos
    ↓
Adicionar ao Carrinho
    ↓
Visualizar Carrinho
    ↓
Escolher Tipo de Entrega
    ↓
Preencher Dados Pessoais
    ↓
Selecionar Forma de Pagamento
    ↓
(Opcional) Aplicar Cupom
    ↓
Finalizar Pedido
    ↓
Redirecionar para WhatsApp
    ↓
Restaurante Recebe Mensagem Formatada
```

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Versão | Propósito |
|-----------|--------|----------|
| **HTML5** | - | Estrutura |
| **CSS3** | - | Estilos e Layout |
| **JavaScript (Vanilla)** | ES6+ | Interatividade |
| **Font Awesome** | 6.5.1 | Ícones |
| **Unsplash API** | - | Imagens de Produtos |

---

## 📊 Resumo de Funcionalidades

### ✅ Totalmente Implementado
- [x] Sistema de carrinho com CRUD completo
- [x] Filtragem por categoria
- [x] Busca em tempo real
- [x] Entrega e retirada agendada
- [x] Múltiplas formas de pagamento
- [x] Sistema de cupons
- [x] Integração WhatsApp
- [x] Design responsivo
- [x] Animações suaves
- [x] Validação de formulários

---

## 🔐 Segurança e Validação

- ✅ Validação de campos obrigatórios
- ✅ Formatação de telefone
- ✅ Validação de CEP
- ✅ Confirmação de quantidade mínima no carrinho
- ✅ Feedback visual de erros
- ✅ Sanitização de entrada do usuário

---

## 🎬 Animações

- **Efeito Voar**: Imagem do produto "voa" para o ícone do carrinho
- **Deslizar**: Menu lateral do carrinho desliza suavemente
- **Transições**: Hover effects nos botões e cards
- **Fade**: Aparecer/desaparecer com suavidade

---

## 📞 Integração WhatsApp

O sistema envia mensagens formatadas para o WhatsApp Business com:
- ✅ Listagem completa de itens
- ✅ Quantidade de cada produto
- ✅ Subtotal e desconto aplicado
- ✅ Total final
- ✅ Dados de entrega ou retirada
- ✅ Forma de pagamento selecionada

---

## 🐛 Troubleshooting

### Carrinho não atualiza
- Verifique se JavaScript está ativado no navegador
- Limpe cache do navegador (Ctrl+Shift+Del)

### Imagens não carregam
- Verifique conexão com internet
- As imagens vêm da Unsplash API (requer internet)

### WhatsApp não abre
- Certifique-se de que o número está no formato internacional (55XXXXXXXXXX)
- Verifique se tem WhatsApp instalado ou acesso web

### Formulário não valida
- Preencha TODOS os campos obrigatórios (marcados com *)
- Nomes devem ter sobrenome

---

## 📈 Próximas Melhorias Sugeridas

- [ ] Integração com API de pagamento (Stripe, MercadoPago)
- [ ] Sistema de autenticação de usuários
- [ ] Histórico de pedidos
- [ ] Notificações push
- [ ] Admin painel para gerenciar produtos
- [ ] Dashboard de vendas
- [ ] Sistema de avaliação de produtos
- [ ] Integração com sistemas de entrega

---

## 📝 Licença

Projeto desenvolvido como portfólio de web development. Livre para uso e modificação.

---

## 👤 Créditos

**Desenvolvido com ❤️ para Trindade Restaurante**

---

## 📧 Contato e Suporte

Para dúvidas, sugestões ou relatórios de bugs, entre em contato através dos canais abaixo:

- 📱 WhatsApp: [Número do Restaurante]
- 📧 Email: [Email para suporte]
- 🌐 Site: [https://blackthornethan23.github.io/site-trindade-restaurante/](https://blackthornethan23.github.io/site-trindade-restaurante/)

---

<div align="center">

### ⭐ Se este projeto foi útil, considere deixar uma estrela!

**Desenvolvido com React a inovação e qualidade** 🚀

</div>
