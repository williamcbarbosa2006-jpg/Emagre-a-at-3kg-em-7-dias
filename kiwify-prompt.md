# Prompt para Claude no navegador — Setup Kiwify

Cole esse prompt no Claude com acesso ao navegador (computer use).

---

## PROMPT

Você vai me ajudar a criar 3 produtos na Kiwify e montar o funil completo. Siga exatamente a ordem abaixo. Confirme cada etapa antes de avançar para a próxima.

---

### CONTEXTO DO FUNIL

- **Produto Principal** → R$ 29,90
- **Order Bump** (na página de checkout do principal) → R$ 9,90
- **Upsell** (após confirmação de pagamento) → R$ 19,90

---

### ETAPA 1 — LOGIN

Acesse kiwify.com.br e faça login na conta.
Confirme que está no dashboard antes de continuar.

---

### ETAPA 2 — CRIAR PRODUTO PRINCIPAL

Vá em **Produtos → Criar Produto**.

Preencha:

| Campo | Valor |
|-------|-------|
| Nome do produto | Emagreça até 3kg em 7 Dias |
| Tipo | E-book / Produto Digital |
| Descrição curta | Protocolo alimentar de 7 dias para perder até 3kg, desinchar e recuperar energia — sem academia, sem passar fome e sem contar caloria. |
| Preço | R$ 29,90 |
| Métodos de pagamento | PIX + Cartão de Crédito |
| Parcelamento cartão | Até 3x sem juros (ou à vista) |
| Página de vendas | https://emagreca-ate-3kg-7dias.vercel.app/ |

Em **Conteúdo / Entrega**:
- Tipo de entrega: Upload de arquivo (PDF — será enviado depois)
- Mensagem de entrega por e-mail: padrão da Kiwify por enquanto

Em **Checkout**:
- Ativar: sim
- Nome no checkout: "Emagreça até 3kg em 7 Dias — Protocolo Completo"

Salve o produto. Copie e anote o **link de checkout gerado** (formato: pay.kiwify.com.br/XXXXXX).

---

### ETAPA 3 — CRIAR ORDER BUMP

Vá em **Produtos → Criar Produto** novamente.

Preencha:

| Campo | Valor |
|-------|-------|
| Nome do produto | Kit Substituições & Rótulos |
| Tipo | E-book / Produto Digital |
| Descrição curta | Tabela de 30+ substituições alimentares + Guia de leitura de rótulos para não sabotarem o protocolo. PDF enviado junto com o produto principal. |
| Preço | R$ 9,90 |
| Métodos de pagamento | Mesmo do produto principal (PIX + Cartão) |

Em **Conteúdo / Entrega**:
- Tipo de entrega: Upload de arquivo (PDF — será enviado depois)

Salve o produto. Anote o ID ou nome para usar na próxima etapa.

---

### ETAPA 4 — CRIAR UPSELL

Vá em **Produtos → Criar Produto** novamente.

Preencha:

| Campo | Valor |
|-------|-------|
| Nome do produto | Receitas Anti-inchaço: 5 Prontas em 15 Minutos |
| Tipo | E-book / Produto Digital |
| Descrição curta | 5 receitas anti-inflamatórias prontas em menos de 15 minutos, desenvolvidas especificamente para as fases do Protocolo 7 Dias. Ingredientes simples de supermercado. |
| Preço | R$ 19,90 |
| Métodos de pagamento | Mesmo do produto principal |

Em **Conteúdo / Entrega**:
- Tipo de entrega: Upload de arquivo (PDF — será enviado depois)

Salve o produto.

---

### ETAPA 5 — CONFIGURAR ORDER BUMP no produto principal

Volte ao produto **"Emagreça até 3kg em 7 Dias"**.

Vá na aba **Checkout** ou **Order Bump**.

Adicione o order bump:
- Produto do bump: **Kit Substituições & Rótulos**
- Posição: abaixo dos dados de pagamento, antes do botão de finalizar

Texto do bump (copie exatamente):

> **Adicione por apenas R$ 9,90 — antes de finalizar**
>
> A **Tabela de Substituições** com mais de 30 trocas alimentares + o **Guia de Leitura de Rótulos** para nunca mais levar para casa um alimento que trava o seu metabolismo. Dois PDFs. Um clique.

Salve.

---

### ETAPA 6 — CONFIGURAR UPSELL pós-compra

Ainda no produto principal, vá na aba **Upsell** ou **Funil**.

Configure o upsell:
- Produto do upsell: **Receitas Anti-inchaço: 5 Prontas em 15 Minutos**
- Gatilho: logo após confirmação do pagamento
- Tipo de página: página de upsell da Kiwify (one-click upsell)

Texto da página de upsell (copie exatamente):

**Título:**
> Parabéns — seu protocolo está chegando no seu e-mail.

**Subtítulo:**
> Mas antes de você ir, uma oferta exclusiva que expira nessa tela:

**Corpo:**
> O maior risco de quem começa o protocolo é enjoar do cardápio no Dia 3 e improvisar — e aí o resultado vai junto.
>
> Criei **5 receitas anti-inchaço prontas em menos de 15 minutos**, com ingredientes simples de supermercado, encaixadas nas fases do protocolo. Cada uma com ingredientes, modo de preparo e variações para adaptar ao seu gosto.
>
> Normalmente R$ 37,00. Por ser complemento direto do que você acabou de comprar: **R$ 19,90 — só nessa tela.**

**Botão aceitar:** "Sim, quero as receitas por R$ 19,90"
**Botão recusar:** "Não, obrigada" (link para página de obrigado padrão)

Salve.

---

### ETAPA 7 — VERIFICAR FUNIL COMPLETO

Confirme que está tudo conectado:

- [ ] Produto principal criado com preço R$ 29,90
- [ ] Link de checkout do principal copiado
- [ ] Order bump configurado (Kit R$ 9,90) aparecendo na página de checkout
- [ ] Upsell configurado (Receitas R$ 19,90) ativado pós-compra
- [ ] Página de vendas do produto principal = https://emagreca-ate-3kg-7dias.vercel.app/

Faça uma **compra-teste** no modo sandbox/teste se disponível, ou simule o fluxo para confirmar que bump e upsell aparecem corretamente.

---

### ETAPA 8 — COPIAR LINK DE CHECKOUT

Copie o link de checkout do produto principal
(formato: **pay.kiwify.com.br/XXXXXX**)

Me informe esse link — vou precisar dele para inserir na landing page.

---

### OBSERVAÇÕES

- Não faça upload dos PDFs ainda — eles serão gerados e enviados separadamente
- Não altere nenhum campo além dos listados acima
- Se a Kiwify pedir categoria do produto, selecione: **Saúde e Bem-estar**
- Se pedir público-alvo, selecione: **Feminino / Adulto**
- Se pedir imagem de capa, pode deixar em branco por agora
