# Agent Carbon Workflow Trello

## Sobre o Projeto

O **Agent Carbon Workflow Trello** é um projeto desenvolvido em Python com o objetivo de simular um agente capaz de automatizar um fluxo de trabalho no Trello. A proposta é organizar etapas relacionadas à análise de pegada de carbono, criando uma estrutura em que tarefas podem ser acompanhadas por cards, listas e movimentações dentro de um board.

A ideia central do projeto é representar um cenário próximo ao mercado, no qual um agente automatizado auxilia na organização de demandas, no controle de etapas e na padronização de um processo. Em vez de depender apenas de anotações manuais, o fluxo passa a ser estruturado em um ambiente visual, permitindo maior clareza sobre o que precisa ser analisado, calculado, explicado e acompanhado.

Este projeto foi desenvolvido como parte de um desafio prático da DIO, com foco em agentes, automação de fluxos de trabalho, integração com API externa e boas práticas de organização de repositório.

## Objetivo

O objetivo do projeto é criar uma base de automação em Python capaz de se conectar ao Trello e apoiar um fluxo de trabalho organizado por etapas. No contexto deste projeto, o fluxo simula o acompanhamento de uma análise de pegada de carbono, desde a entrada das informações até a geração de recomendações e acompanhamento de metas.

O projeto também tem como objetivo demonstrar conhecimentos em autenticação de aplicações, consumo de API, uso de variáveis de ambiente, organização de código e documentação técnica.

## Problema Simulado

Em muitos processos corporativos, informações importantes ficam espalhadas em mensagens, planilhas, e-mails ou anotações manuais. Isso dificulta o acompanhamento das etapas, a priorização das tarefas e a visualização clara do progresso.

Neste projeto, o Trello é utilizado como ferramenta de apoio para organizar o fluxo de trabalho. Cada card pode representar uma solicitação, uma análise ou uma etapa do processo. O agente em Python atua como uma camada de automação para apoiar esse fluxo, reduzindo trabalho manual e tornando o processo mais rastreável.

## Fluxo Proposto

O fluxo de trabalho proposto pelo projeto é composto pelas seguintes etapas:

1. Registro de uma nova demanda relacionada à análise de pegada de carbono.
2. Criação ou organização de cards no Trello.
3. Classificação da solicitação dentro de uma etapa do processo.
4. Apoio à análise dos dados informados.
5. Organização das respostas, recomendações e próximos passos.
6. Acompanhamento do progresso por meio das listas do board.

Um exemplo de organização no Trello poderia conter listas como:

* Entrada
* Em análise
* Cálculo de impacto
* Recomendações
* Metas definidas
* Concluído

## Tecnologias Utilizadas

* Python
* Trello API
* py-trello
* python-dotenv
* Google ADK
* GitHub
* Variáveis de ambiente para proteção de credenciais

## Estrutura do Projeto

```text
agent-carbon-footprint/
├── agentCoder/
│   ├── agent.py
│   ├── __init__.py
│   └── .env.exemplo
├── agents/
│   ├── 00.agent-orquestrador.md
│   ├── 01.agent-carbon-Intake.md
│   ├── 02.agent-Carbon-Factorsmd
│   ├── 03.agent-Carbon-Calculator.md
│   ├── 04.agent-Carbon-Explainability.md
│   ├── 05.agent-Carbon-Advisor.md
│   ├── 06.agent-Carbon-Goal.md
│   └── agent04/
│       └── readme.md
└── README.md
```

## Agentes Conceituais

O projeto utiliza uma visão baseada em agentes especializados, cada um com uma responsabilidade dentro do fluxo.

O **agente orquestrador** é responsável por controlar o fluxo geral, entender a etapa atual da solicitação e direcionar o processo para o agente mais adequado.

O **agente de intake** representa a etapa de coleta inicial das informações. Ele é responsável por receber os dados da solicitação e identificar se há informações suficientes para prosseguir.

O **agente de fatores de carbono** representa a etapa de consulta ou organização dos fatores utilizados na análise.

O **agente calculador** representa a etapa responsável por realizar ou apoiar os cálculos relacionados à pegada de carbono.

O **agente de explicabilidade** tem o papel de transformar o resultado em uma explicação compreensível para a pessoa usuária.

O **agente advisor** representa a etapa de recomendação, sugerindo ações práticas com base no resultado da análise.

O **agente de metas** organiza possíveis objetivos de redução, acompanhamento e melhoria contínua.

## Configuração do Ambiente

Antes de executar o projeto, é recomendado criar um ambiente virtual Python.

No Windows:

```bash
python -m venv .venv
.venv\Scripts\activate
```

Em seguida, instale as dependências:

```bash
pip install -r requirements.txt
```

Caso o arquivo `requirements.txt` ainda não exista, ele pode ser criado com as seguintes dependências:

```text
google-adk
py-trello
python-dotenv
```

## Configuração das Credenciais

Para utilizar a integração com o Trello, é necessário registrar um aplicativo no Trello, obter uma API Key e gerar um token de autorização.

As credenciais devem ser armazenadas em um arquivo `.env`, que não deve ser enviado para o GitHub.

Exemplo de arquivo `.env`:

```env
GOOGLE_GENAI_USE_VERTEXAI=0
GOOGLE_API_KEY=sua-chave-google-aqui

TRELLO_API_KEY=sua-chave-trello-aqui
TRELLO_TOKEN=seu-token-trello-aqui
TRELLO_BOARD_ID=id-do-board-aqui
```

O repositório deve manter apenas um arquivo de exemplo, como `.env.exemplo`, para indicar quais variáveis são necessárias sem expor dados sensíveis.

## Segurança

As chaves de API e tokens de acesso não devem ser compartilhados publicamente. Por isso, o arquivo `.env` precisa ser mantido fora do versionamento.

Uma boa prática é utilizar um arquivo `.gitignore` contendo:

```text
.env
.venv/
__pycache__/
*.pyc
```

Essa prática evita o vazamento acidental de credenciais e mantém o repositório mais seguro e profissional.

## Possível Execução do Projeto

Após configurar as variáveis de ambiente e instalar as dependências, o projeto pode ser utilizado como base para execução de agentes e automações em Python.

Dependendo da configuração local e do ambiente utilizado, a execução pode ser feita a partir do arquivo principal do agente ou por meio das ferramentas do Google ADK.

Exemplo conceitual:

```bash
python agentCoder/agent.py
```

Caso o ambiente ADK esteja configurado, o projeto também pode ser adaptado para execução via interface do ADK.

## Aprendizados

Durante o desenvolvimento deste projeto, foram praticados conceitos importantes para criação de soluções modernas com Python e agentes:

* Registro e autorização de aplicação externa.
* Uso de API Key e token de acesso.
* Integração com Trello API.
* Organização de fluxo de trabalho em cards e listas.
* Estruturação de agentes com responsabilidades separadas.
* Uso de variáveis de ambiente.
* Boas práticas de segurança no GitHub.
* Documentação técnica para portfólio.

## Melhorias Futuras

Como próximos passos, o projeto pode evoluir para incluir criação automática de cards no Trello, movimentação de cards entre listas, leitura de informações de cards existentes, geração automática de recomendações e integração com outros serviços de automação.

Também seria possível adicionar logs, tratamento de erros, interface simples para interação com o usuário e testes automatizados para validar o comportamento das principais funções.

## Conclusão

O **Agent Carbon Workflow Trello** demonstra como Python, agentes e APIs externas podem ser combinados para automatizar um fluxo de trabalho real. Mesmo sendo um projeto educacional, ele representa uma aplicação prática de conceitos usados no mercado, como integração entre sistemas, organização de processos, automação de tarefas e proteção de credenciais.

Este projeto reforça a importância de documentar bem uma solução, explicar o problema resolvido e apresentar uma estrutura clara para que outras pessoas consigam entender, executar e evoluir a proposta.
