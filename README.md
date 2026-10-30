# 🎯 Daily Goals Tracker

> Mecanismo em JavaScript para cálculo analítico, acompanhamento e persistência de metas e hábitos diários.

[![Node.js Version](https://img.shields.io/badge/Node.js-18%2B-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![License](https://img.shields.io/badge/Licença-MIT-blue?style=for-the-badge)](./LICENSE)

---

## 📌 Visão Geral

O **Daily Goals Tracker** é uma solução voltada para automação de métricas e controle de consistência em hábitos e rotinas diárias. O projeto centraliza regras de negócio voltadas a taxas de conclusão, identificação de desvios em relação a metas estipuladas e formatação analítica dos dados para consumo via CLI ou integração web.

### Principais Funcionalidades
- **Cálculo de Desempenho Diário:** Consolidação de percentuais atingidos com base em metas configuradas.
- **Análise Comparativa:** Identificação de métricas deficitárias e excedentes em relação ao alvo programado.
- **Estruturação de Dados:** Modelagem previsível de registros em JSON para facilidade de persistência.
- **Separação de Responsabilidades:** Funções puras de cálculo isoladas de fluxos de entrada e saída (I/O).

---

## 🏗️ Estrutura do Projeto

O projeto adota estrutura modular que unifica as versões de evolução da aplicação:

```text
daily-goals-tracker/
├── src/
│   ├── config/          # Definições de metas e limiares analíticos
│   ├── core/            # Regras de cálculo, somatórios e validações de progresso
│   ├── utils/           # Formatadores e manipuladores de data/saída
│   └── index.js         # Ponto de entrada e orquestração do tracker
├── tests/               # Asserções e testes unitários da lógica de cálculo
├── package.json         # Manifesto do projeto, dependências e scripts
└── README.md            # Documentação técnica de arquitetura e operação
```

---

## 🧠 Regras de Negócio e Lógica de Domínio

O núcleo da aplicação opera sobre estruturas normalizadas de metas diárias. Um exemplo da assinatura de dados e execução:

```javascript
// Exemplo de payload processado pelo core analítico
const dailyGoalPayload = {
  date: "2024-03-20",
  goals: [
    { id: "read-pages", target: 20, completed: 25, unit: "pages" },
    { id: "water-intake", target: 3000, completed: 2100, unit: "ml" },
    { id: "study-minutes", target: 60, completed: 60, unit: "minutes" }
  ]
};
```

### Métricas Calculadas:
1. **Taxa de Conclusão por Item:** $\text{Taxa} = \left(\frac{\text{Concluído}}{\text{Meta}}\right) \times 100$
2. **Índice de Consistência Global:** Média ponderada do cumprimento de todas as metas ativas do dia.
3. **Status de Cumprimento:** Classificação binária (`COMPLETED`, `PARTIAL`, `MISSED`) baseada em limites percentuais pré-configurados.

---

## 🚀 Como Executar Localmente

### Pré-requisitos
- [Node.js](https://nodejs.org/) versão 18.x ou superior
- Gerenciador de pacotes `npm` (incluso no runtime)

### Passo a Passo

1. **Clonar o repositório:**
   ```bash
   git clone https://github.com/ferrazmarcius/daily-goals-tracker.git
   cd daily-goals-tracker
   ```

2. **Instalar dependências (quando aplicável):**
   ```bash
   npm install
   ```

3. **Executar a aplicação:**
   ```bash
   npm start
   ```

---

## 🧪 Testes Automatizados

As rotinas de cálculo são validadas contra cenários de entrada de borda (metas zeradas, valores decimais e excesso de cumprimento):

```bash
# Execução da suíte de testes
npm test
```

---

## 🗺️ Histórico de Evolução e Roadmap

### Versões
- **v1.0.0:** Implementação dos primeiros algoritmos de soma e conferência linear de metas em script procedural.
- **v1.1.0:** Refatoração para funções reutilizáveis, suporte a metas numéricas flexíveis e estruturação de objetos de métricas.

### Próximos Passos
- [ ] Implementação de persistência persistente em banco relacional leve (SQLite).
- [ ] Exportação de relatórios consolidados em formatos CSV e Markdown.
- [ ] Interface visual para consulta e input de metas diárias.

---

## 📄 Licença

Este projeto é distribuído sob os termos da licença **MIT**. Consulte o arquivo [LICENSE](./LICENSE) para mais detalhes.

---

**Autor:** [Marcius Ferraz](https://github.com/ferrazmarcius)

---
> ℹ️ **Auditoria Técnica:** Este projeto passou por uma revisão automatizada de arquitetura e padrões. Consulte o relatório completo em [`AUDITORIA_GEMINI.md`](./AUDITORIA_GEMINI.md).
