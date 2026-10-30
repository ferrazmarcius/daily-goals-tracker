# 🎯 Daily Goals Tracker

> Sistema modular e escalável para rastreamento, cálculo e gestão analítica de metas diárias e hábitos.

![GitHub repo size](https://img.shields.io/github/repo-size/ferrazmarcius/daily-goals-tracker?style=for-the-badge)
![GitHub language count](https://img.shields.io/github/languages/count/ferrazmarcius/daily-goals-tracker?style=for-the-badge)
![Node.js Version](https://img.shields.io/badge/Node.js-18%2B-green?style=for-the-badge&logo=node.js)
![License](https://img.shields.io/github/license/ferrazmarcius/daily-goals-tracker?style=for-the-badge)

---

## 📌 Visão Geral

O **Daily Goals Tracker** foi projetado para solucionar a inconsistência no monitoramento de hábitos pessoais e profissionais. O foco do projeto reside na separação clara entre a **lógica de domínio** (cálculo de taxas de conclusão, persistência e streaks) e a **interface de interação**, aplicando princípios de código limpo e padrões arquiteturais modernos.

### Principais Funcionalidades
- ⏱️ **Registro Dinâmico:** Inclusão e monitoramento de metas em tempo real.
- 📊 **Métricas de Performance:** Cálculo automático de percentual diário concluído e streaks.
- 💾 **Persistência de Dados:** Armazenamento resiliente para histórico e consultas retroativas.
- 🧪 **Lógica Testável:** Separação estrita entre manipulação de dados e renderização.

---

## 🏗️ Arquitetura e Estrutura do Repositório

O repositório adota uma abordagem modularizada, separando regras de negócio de componentes utilitários:

```text
daily-goals-tracker/
├── src/
│   ├── core/            # Entidades e lógica de domínio (regras de negócio)
│   ├── services/        # Serviços de cálculo e validação
│   ├── storage/         # Camada de persistência local / adaptadores
│   └── index.js         # Ponto de entrada da aplicação
├── tests/               # Testes unitários e de integração
├── .github/             # Pipelines de CI/CD (GitHub Actions)
├── Dockerfile           # Imagem para execução em containers
├── package.json         # Dependências e scripts do ecossistema Node.js
└── README.md            # Documentação técnica
```

---

## 🛠️ Tecnologias Utilizadas

- **Runtime:** Node.js (v18+)
- **Linguagem:** JavaScript (ES6+ Modules)
- **Qualidade de Código:** ESLint, Prettier
- **Testes:** Vitest / Jest
- **Containerização:** Docker

---

## 🚀 Como Executar Localmente

### Pré-requisitos
- [Node.js](https://nodejs.org/) (versão 18 ou superior)
- [Git](https://git-scm.com/)
- [Docker](https://www.docker.com/) *(opcional para execução via container)*

### Passo a Passo

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/ferrazmarcius/daily-goals-tracker.git
   cd daily-goals-tracker
   ```

2. **Instale as dependências:**
   ```bash
   npm install
   ```

3. **Inicie a aplicação:**
   ```bash
   npm start
   ```

---

## 🧪 Testes e Qualidade de Código

Para garantir a confiabilidade da lógica de cálculo de metas, execute a suíte de testes unitários:

```bash
# Executar testes unitários
npm test

# Executar testes em modo watch (desenvolvimento contínuo)
npm run test:watch

# Análise estática de código (Linter)
npm run lint
```

---

## 🐳 Executando com Docker

Se preferir rodar a aplicação em um ambiente isolado:

```bash
# Construir a imagem Docker
docker build -t daily-goals-tracker .

# Executar o container
docker run -it --rm daily-goals-tracker
```

---

## 🗺️ Roadmap de Evolução

- [ ] Exportação de relatórios em CSV/JSON.
- [ ] Implementação de dashboard web responsivo.
- [ ] Módulo complementar em Python CLI para automações em servidores.
- [ ] Integração com webhooks de mensageria (Discord/Telegram).

---

## 📄 Licença

Distribuído sob a licença **MIT**. Consulte `LICENSE` para mais informações.

---

**Autor:** [Marcius Ferraz](https://github.com/ferrazmarcius)
