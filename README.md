# 🩺 Fundamentos de SQL para Bancos de Dados em Saúde

**Glossário Interativo — E-book de Consulta Rápida (3ª GRS Paraíba · UEPB)**

Um glossário técnico interativo, em uma única página HTML autossuficiente, reunindo os comandos essenciais de **SQL**, **Pandas** e **Matplotlib** aplicados a dados reais de saúde pública — da consulta ao banco de dados até a visualização de indicadores epidemiológicos.

Material de apoio do minicurso de ciência de dados aplicada à vigilância epidemiológica, construído sobre uma base real do DATASUS/SINAN com notificações de sífilis nos municípios da Paraíba.

---

## ✨ Funcionalidades

- **Busca em tempo real** — filtra os verbetes por nome de função, comando ou palavra-chave do contexto, sem recarregar a página.
- **Navegação por categoria** — botões de atalho (*Todos / SQL / Pandas / Matplotlib*) que rolam suavemente até a seção correspondente, com destaque automático do item ativo conforme a rolagem (scroll-spy).
- **Numeração automática** — cada verbete é numerado sequencialmente dentro da sua aba (via contador CSS), sem necessidade de manutenção manual.
- **Menu retrátil** — o botão ☰ mostra/esconde a barra de categorias em qualquer tamanho de tela.
- **Design responsivo** — testado e ajustado para não gerar rolagem horizontal em celulares, com blocos de código que quebram linha em vez de vazar da tela.
- **100% autossuficiente** — todo o CSS, JavaScript e os ícones (SVG inline) estão dentro do próprio arquivo. Não depende de internet, CDN ou build step: funciona até offline, com duplo clique.

## 📚 Estrutura do glossário

| Parte | Tema | Verbetes |
|---|---|---|
| 1 | **SQL** — SELECT, WHERE, JOIN, GROUP BY, funções de agregação, tratamento de nulos | 14 |
| 2 | **Pandas** — extração de dados, `merge`, `groupby`, manipulação de caminhos com `os.path` | 14 |
| 3 | **Matplotlib** — construção de gráficos, formatação, anotações e exportação | 21 |

Cada verbete segue o mesmo formato: nome da função/comando, explicação em linguagem simples, um bloco **"No contexto do SUS"** aplicando o conceito a um cenário real de vigilância epidemiológica, e um exemplo de código com destaque de sintaxe.

## 🛠️ Tecnologias

- **HTML5** semântico (landmarks ARIA, hierarquia de headings, `aria-labelledby`)
- **CSS3** puro (Grid, Flexbox, variáveis CSS, media queries) — sem frameworks
- **JavaScript vanilla** (sem dependências) — busca, navegação por filtros e scroll-spy via `IntersectionObserver`
- Ícones em **SVG inline** (sprite `<symbol>`/`<use>`), sem depender de bibliotecas externas de ícones

Paleta institucional: azul petróleo (`#0f4c5c`) e verde água (`#0a9396`).

## 🚀 Como usar

Não há instalação nem build. Basta abrir o arquivo:

```bash
# Clonar o repositório
git clone <url-do-repositorio>
cd <pasta-do-repositorio>

# Abrir diretamente no navegador
open glossario-sql-saude.html   # macOS
start glossario-sql-saude.html  # Windows
xdg-open glossario-sql-saude.html # Linux
```

Ou publique a pasta com **GitHub Pages** (Settings → Pages → Deploy from branch) para acesso via link, como neste projeto.

## 📁 Estrutura de arquivos

```
.
├── glossario-sql-saude.html   # Glossário completo (SQL + Pandas + Matplotlib)
├── capa-glossario-sql.html    # Página de capa/apresentação com link para o glossário
└── README.md                  # Este arquivo
```

## 🗃️ Sobre os dados

Os exemplos de código usam uma base real do **DATASUS/SINAN** (`sifilis_pb.db`), com notificações de sífilis nos municípios da Paraíba, organizadas em quatro tabelas relacionadas por código IBGE do município: cadastro de municípios, notificações por ano, distribuição por faixa etária e forma clínica dos casos.

## 👥 Desenvolvido por

Arthur Barbosa, Andrey Ferreira e Vívian Araújo
3ª GRS Paraíba · UEPB
