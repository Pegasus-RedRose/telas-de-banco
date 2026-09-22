# Fintech & Banking UI Kit

Um repositório open-source de templates e componentes de interface (UI) de alta fidelidade voltado para aplicações financeiras, internet banking, fintechs e plataformas de investimento.

---

## Sumário

- [Visão Geral](#visão-geral)
- [Funcionalidades e Princípios](#funcionalidades-e-princípios)
- [Telas Contempladas](#telas-contempladas)
- [Stack Tecnológica](#stack-tecnológica)
- [Estrutura do Repositório](#estrutura-do-repositório)
- [Como Executar](#como-executar)
- [Design System e Tokens](#design-system-e-tokens)
- [Contribuição](#contribuição)
- [Licença](#licença)

---

## Visão Geral

Este projeto fornece uma base estruturada de código e design para acelerar a criação de produtos financeiros digitais. Ele combina layouts responsivos, componentes modulares e boas práticas de usabilidade no segmento bancário.

Todos os dados utilizados nas interfaces são mockados localmente via JSON, dispensando a necessidade de conexão com APIs bancárias reais para rodar o projeto.

---

## Funcionalidades e Princípios

- **Data Masking (Privacidade):** Alternância global para ocultar ou exibir valores monetários e dados sensíveis com um clique.
- **Design Responsivo:** Adaptabilidade completa para dispositivos mobile, tablets e desktops.
- **Suporte a Dark / Light Mode:** Alternância nativa de temas estruturada via variáveis CSS e Tailwind.
- **Componentização Atômica:** Estruturação em átomos, moléculas e organismos para garantir reuso e fácil manutenção.
- **Acessibilidade (WCAG):** Foco visível, navegação por teclado e navegação estruturada para leitores de tela.

---

## Telas Contempladas

### 1. Dashboard Principal
- Card de saldo geral com alternância de visibilidade.
- Atalhos de ações rápidas (Pix, Transferência, Extrato, Cartões).
- Resumo do extrato com transações recentes.
- Widget de controle de fatura e limite de cartão de crédito.
- Gráfico consolidado de entradas e saídas mensais.

### 2. Portfólio de Investimentos
- Visão geral do patrimônio total e rentabilidade acumulada.
- Gráfico de distribuição de ativos por classe (Renda Fixa, Ações, FIIs, Cripto).
- Tabela detalhada de ativos em custódia com status de lucro/prejuízo.
- Fluxo visual de aplicação e resgate.

### 3. Home Broker / Renda Variável
- Book de ofertas de compra e venda em tempo real (simulado).
- Boleta de negociação para ordens a mercado, limitadas e stop loss.
- Ticker de cotação com variação percentual do dia.
- Histórico de ordens executadas e pendentes.

### 4. Extrato e Histórico Financeiro
- Agrupamento cronológico de transações.
- Filtros por categoria, período e tipo de movimentação.
- Busca textual por estabelecimento ou favorecido.
- Modal de comprovante com opção de exportação em PDF.

### 5. Gestão de Cartões
- Representação gráfica de cartões físicos e virtuais.
- Controle de limite ajustável via slider.
- Detalhamento de fatura aberta, fechada e histórico de parcelas.
- Ações de segurança: bloqueio temporário, aviso viagem e criação de cartão virtual.

### 6. Transferências e Pix
- Fluxo de envio de Pix por chave (CPF, E-mail, Telefone, Chave Aleatória).
- Leitor e gerador de QR Code / Pix Copia e Cola.
- Tela de confirmação e revisão de dados antes do envio.
- Lista de contatos e favorecidos frequentes.

---

## Stack Tecnológica

- **Core:** React / Next.js
- **Linguagem:** TypeScript
- **Estilização:** Tailwind CSS
- **Componentes Base:** Radix UI / Shadcn UI
- **Ícones:** Lucide React
- **Gráficos:** Recharts / Lightweight Charts

---

## Estrutura do Repositório

```text
.
├── public/
│   └── assets/             # Imagens estáticas e logotipos fictícios
├── src/
│   ├── components/
│   │   ├── ui/             # Componentes atômicos (Button, Input, Card, Modal)
│   │   ├── modules/        # Organismos de tela (Header, Sidebar, TransactionTable)
│   │   └── charts/         # Componentes de gráficos reutilizáveis
│   ├── data/               # Mocks de dados em formato JSON
│   ├── hooks/              # Custom hooks (useTheme, useDataMasking, useAuthMock)
│   ├── pages/              # Rotas e visões das telas do sistema
│   ├── styles/             # Variáveis globais, tokens e configurações do Tailwind
│   ├── types/              # Definições de interfaces TypeScript
│   └── utils/              # Funções utilitárias (formatação de moeda, datas, etc)
├── .eslintrc.json
├── tailwind.config.js
├── tsconfig.json
└── README.md
```

---

## Como Executar

### Pré-requisitos
- Node.js (versão 18.x ou superior)
- npm, yarn ou pnpm

### Passo a Passo

1. **Clonar o repositório:**
   ```bash
   git clone https://github.com/seu-usuario/fintech-ui-kit.git
   cd fintech-ui-kit
   ```

2. **Instalar as dependências:**
   ```bash
   npm install
   ```

3. **Executar o servidor de desenvolvimento:**
   ```bash
   npm run dev
   ```

4. **Acessar no navegador:**
   Abra `http://localhost:3000` para visualizar a aplicação.

---

## Design System e Tokens

O projeto utiliza uma paleta semântica configurada no arquivo `tailwind.config.js`:

| Categoria | Token | Uso |
| :--- | :--- | :--- |
| **Brand Primary** | `brand-600` | Botões principais, destaques da marca e elementos ativos |
| **Success** | `emerald-500` | Entradas de saldo, rendimentos positivos, confirmações |
| **Danger** | `rose-500` | Saídas, faturas, variações negativas de ativos |
| **Warning** | `amber-500` | Avisos de vencimento, pendências |
| **Neutral** | `slate-50` a `slate-900` | Superfícies, cards, textos e bordas em modo claro e escuro |

---

## Contribuição

Contribuições são bem-vindas. Para contribuir:

1. Faça um Fork do repositório.
2. Crie uma branch para a sua funcionalidade (`git checkout -b feature/nova-tela`).
3. Commit suas alterações (`git commit -m 'Adiciona template da tela X'`).
4. Envie para a branch (`git push origin feature/nova-tela`).
5. Abra um Pull Request detalhando as alterações.

---

## Licença

Este projeto está sob a licença MIT. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.
