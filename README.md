# Workshop UFU — Code Together: Fork, Code e Pull Request

> Repositório oficial do workshop de colaboração com GitHub.  
> Bacharelado em Sistemas de Informação — Universidade Federal de Uberlândia

---

## Sobre este repositório

Este repositório contém uma página web simples desenvolvida com **HTML e CSS** que possui **problemas visuais e estruturais inseridos propositalmente**.

A dinâmica simula um fluxo real de contribuição open source: cada grupo recebe issues para resolver, trabalha no próprio fork e envia um Pull Request para os Maintainers avaliarem. Nem todo Pull Request será aceito — assim como acontece em projetos reais.

---

## Estrutura do projeto

```
workshop-web/
├── index.html   ← estrutura HTML da página
├── style.css    ← estilos da página (com problemas propositais)
└── README.md    ← este arquivo
```

Para visualizar a página: abra o arquivo `index.html` diretamente no navegador. Nenhuma instalação é necessária.

---

##  Issues abertas

Cada issue representa um problema real na página que deve ser corrigido. Acesse a aba **Issues** deste repositório para ver a descrição completa e os critérios de aceite de cada uma.

| # | Problema | Grupos responsáveis |
|---|----------|---------------------|
| [#1](../../issues/1) | Corrigir o plano de fundo da página | A e B |
| [#2](../../issues/2) | Corrigir a tipografia e fonte dos textos | A e D |
| [#3](../../issues/3) | Organizar o layout com Flexbox | B e E |
| [#4](../../issues/4) | Aumentar o contraste e legibilidade dos textos | C e D |
| [#5](../../issues/5) | Adicionar informações e seções faltantes no HTML | C e F |
| [#6](../../issues/6) | Melhorar a aparência geral com CSS Grid e estilos visuais | E e F |

> Cada issue pode ser resolvida por dois grupos ao mesmo tempo — mas apenas **uma solução** será aceita pelos Maintainers.

---

## Organização dos grupos

| Grupo | Issues atribuídas |
|-------|-------------------|
| A | #1 e #2 |
| B | #1 e #3 |
| C | #4 e #5 |
| D | #2 e #4 |
| E | #3 e #6 |
| F | #5 e #6 |

---

## Etapa 1 — Fork

O Fork cria uma cópia deste repositório na sua conta do GitHub. É nessa cópia que o grupo vai trabalhar — **ninguém pode editar este repositório diretamente**.

**Como fazer o Fork:**

1. No canto superior direito desta página, clique no botão **`Fork`**

   ![Botão Fork no GitHub](https://docs.github.com/assets/cb-40142/mw-1440/images/help/repository/fork-button.webp)

2. Selecione a sua conta pessoal como destino do fork

3. Aguarde o GitHub criar a cópia — você será redirecionado automaticamente para o seu fork

> Agora você tem o endereço `https://github.com/SEU-USUARIO/workshop-web` — este é o repositório do seu grupo.

---

##  Etapa 2 — Code (desenvolvimento)

Com o fork criado, é hora de baixar o código e resolver as issues atribuídas ao grupo.

### 2.1 — Clone o seu fork

Abra o terminal e execute:

```bash
git clone https://github.com/SEU-USUARIO/workshop-web.git
cd workshop-web
```

> Substitua `SEU-USUARIO` pelo seu nome de usuário do GitHub.

### 2.2 — Crie uma branch para cada issue

Nunca edite diretamente na branch `main`. Crie uma branch com um nome descritivo:

```bash
# Exemplo para a issue #1
git checkout -b fix/issue-1-fundo-pagina

# Exemplo para a issue #3
git checkout -b fix/issue-3-flexbox-layout
```

O padrão recomendado para o nome da branch é:

```
fix/issue-NUMERO-descricao-curta
```

### 2.3 — Faça as alterações nos arquivos

Edite o `index.html` e/ou o `style.css` conforme a issue do seu grupo.  
Abra o `index.html` no navegador para testar visualmente as alterações.

### 2.4 — Registre as alterações com commit

Após salvar as alterações, registre-as com uma mensagem clara:

```bash
git add .
git commit -m "fix: corrige fundo da página (#1)"
```

**Boas mensagens de commit:**
- `fix: corrige cor de fundo do body (#1)`
- `feat: adiciona rodapé com informações de contato (#5)`
- `style: aplica flexbox no cabeçalho e botões (#3)`

**Evite mensagens vagas como:** `alterações feitas`, `corrigido`, `css`

### 2.5 — Envie para o seu fork

```bash
git push origin fix/issue-1-fundo-pagina
```

---

##  Etapa 3 — Pull Request

O Pull Request é o pedido formal para que as suas alterações sejam incorporadas ao repositório original. Os Maintainers irão ler, revisar e decidir se aceitam ou não.

**Como abrir o Pull Request no GitHub:**

1. Acesse o **seu fork** em `https://github.com/SEU-USUARIO/workshop-web`

2. O GitHub vai exibir um aviso amarelo com o botão **`Compare & pull request`** — clique nele

3. Verifique se o Pull Request está apontando de:
   - **base repository:** `[usuario-do-professor]/workshop-web` → branch `main`
   - **head repository:** `SEU-USUARIO/workshop-web` → sua branch de fix

4. Preencha o título e a descrição do Pull Request seguindo o modelo abaixo:

---

###  Modelo de descrição do Pull Request

```
## Issues resolvidas
- Closes #1

## O que foi alterado
- Arquivo `style.css`: adicionada propriedade `background-color` no seletor `body`

## O que melhorou na página
O fundo branco foi substituído por uma cor neutra e agradável visualmente,
dando mais identidade à interface e melhorando o conforto de leitura.

## Por que esta solução deve ser aceita
A solução é simples, direta e não afeta nenhum outro elemento da página.
A cor escolhida mantém bom contraste com os textos existentes.
```

---

>  Usar `Closes #1` na descrição faz o GitHub fechar a issue automaticamente quando o PR for aceito.

5. Clique em **`Create pull request`** para enviar

---

##  Etapa 4 — Revisão dos Maintainers

Os **3 Maintainers** são responsáveis por analisar todos os Pull Requests recebidos.

Para cada Pull Request, eles podem tomar uma das seguintes decisões:

| Decisão | O que significa |
|---------|-----------------|
| **Approve** | Pull Request aceito — o código será incorporado ao projeto |
|  **Request changes** | O grupo precisa fazer ajustes antes da aprovação |
| **Close** | Pull Request rejeitado — a solução não será incorporada |

Quando dois grupos resolvem a mesma issue, os Maintainers comparam as duas soluções e escolhem apenas a melhor.

>  Assim como em projetos reais, **nem todo Pull Request é aceito automaticamente**. A qualidade, clareza e aderência aos critérios da issue fazem diferença na decisão.

---
