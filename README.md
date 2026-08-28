# 🧠 Miniguia de Estudos: Engenharia de Prompt com NotebookLM

Este repositório contém um guia prático e estruturado sobre **Engenharia de Prompt**, desenvolvido como projeto final para o Bootcamp **Michael Page - Criando Seu Primeiro Agente de IA** na [DIO](https://dio.me). 

O projeto foi construído utilizando a metodologia de **RAG (Retrieval-Augmented Generation)** através do **Google NotebookLM**, alimentado exclusivamente por fontes técnicas e oficiais de IA.

---

## 🎯 Objetivo do Projeto
Demonstrar a aplicação prática de técnicas de curadoria de conteúdo, engenharia de prompt e uso de IAs generativas modernas para construir um assistente de estudos altamente preciso, livre de alucinações e focado no aprendizado acelerado.

---

## 📚 Fontes Utilizadas (Curadoria)
Para garantir a confiabilidade técnica das informações, o NotebookLM foi alimentado com as seguintes referências oficiais:
1. [OpenAI Prompt Engineering Guide](https://platform.openai.com/docs/guides/prompt-engineering) - Boas práticas oficiais dos criadores do ChatGPT.
2. [Prompting Guide (DAIR.AI)](https://www.promptingguide.ai/) - O guia de código aberto mais completo do mercado.
3. [Anthropic Prompt Engineering Overview](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview) - Diretrizes oficiais para desenvolvimento com a família de modelos Claude.

---

## 📖 Resumo Estruturado de Engenharia de Prompt
*A Engenharia de Prompt é uma disciplina focada no desenvolvimento e na otimização de instruções para utilizar modelos de linguagem (LMs) de maneira eficiente em diversas aplicações e pesquisas
. Trata-se de um conjunto de habilidades para interagir, construir e compreender as capacidades e limitações dos modelos de linguagem em larga escala (LLMs)
. Como a geração de respostas pelos modelos é não-determinística, criar prompts eficazes envolve tanto arte quanto ciência
.
Abaixo, o resumo estruturado divide a Engenharia de Prompt:
### 1. Conceitos Básicos
**Definição de Instruções Eficazes:** Consiste em escrever diretrizes claras para que o modelo gere, de forma consistente, saídas alinhadas com os requisitos desejados
.
Papéis de Mensagem (Message Roles): Permitem fornecer instruções com diferentes níveis de autoridade
. Os principais papéis são:
Developer (desenvolvedor): Define as regras do sistema, o comportamento geral e as regras de negócios, sendo priorizado em relação às mensagens do usuário
. Funciona como a definição de uma função na programação
.
User (usuário): Contém as entradas e comandos fornecidos pelo usuário final, servindo como os argumentos que serão aplicados às regras estabelecidas pelo desenvolvedor
.
Assistant (assistente): Representa a resposta gerada pelo próprio modelo de linguagem
.
Formatação com Markdown e XML: A utilização de cabeçalhos e listas em Markdown ajuda a estruturar a hierarquia e as divisões lógicas do prompt
. As tags XML são usadas para definir limites claros de conteúdo (como demarcar documentos de referência ou exemplos) e adicionar metadados estruturados por meio de atributos
.
Estrutura de uma Mensagem do Desenvolvedor: Geralmente segue uma ordem lógica contendo: Identidade (estilo de comunicação e objetivos gerais), Instruções (regras do que o modelo deve e não deve fazer), Exemplos (demonstrações de entradas e saídas desejadas) e Contexto (informações e dados de suporte adicionais colocados preferencialmente no final)
.
Zero-shot Prompting: Uma técnica elementar na qual o modelo é instruído a realizar uma tarefa diretamente, sem receber exemplos adicionais fornecidos no prompt
.
### 2. Técnicas Intermediárias
**Few-Shot Prompting:** Técnica que direciona o modelo para uma nova tarefa incluindo um pequeno número de exemplos de entrada e saída diretamente no prompt
. Isso ajuda o LLM a "pegar" o padrão demonstrado e aplicá-lo à nova entrada sem a necessidade de realizar um ajuste fino (fine-tuning)
. Recomenda-se apresentar uma variedade diversa de exemplos para obter melhores resultados, normalmente inseridos na mensagem do desenvolvedor
.
Prompt Chaining (Encadeamento de Prompts): Envolve a divisão de tarefas complexas em uma sequência de prompts conectados, onde a saída de uma etapa serve como entrada para a próxima, ajudando a guiar o fluxo de geração de maneira mais controlada
.
### 3. Técnicas Avançadas
**Chain-of-Thought (Cadeia de Pensamento):** Técnica que orienta o modelo a gerar um processo de raciocínio intermediário antes de apresentar a resposta final
. Modelos de raciocínio (reasoning models) criam uma cadeia interna de pensamento, o que os torna muito superiores em tarefas complexas, lógica matemática e planejamento de etapas múltiplas
. Há variações como o Multimodal CoT
 e o LM-Guided CoT
.
Retrieval-Augmented Generation (RAG - Geração Aumentada de Recuperação): Consiste em fornecer dinamicamente dados proprietários ou recursos externos específicos diretamente no prompt
. Essa técnica amplia a base de conhecimento do modelo além de seus dados de treinamento, auxiliando na precisão da resposta e na redução de alucinações
.
Estruturas Complexas de Raciocínio: Métodos avançados de estruturação de prompts listados no guia, tais como Tree of Thoughts (Árvore de Pensamentos)
, Self-Consistency (Auto-consistência)
, Reflexion
, e ReAct (que integra raciocínio e execução de ações/ferramentas)
.
Prompting para Agentes de IA (AI Agents): Focado em tarefas de longa duração e sistemas autônomos
. Consiste em orientar o modelo a planejar extensivamente antes de interagir com ferramentas, refletir profundamente sobre os resultados obtidos a cada passo e persistir na execução de sub-tarefas até que o problema esteja totalmente resolvido
. O uso de rubricas de avaliação e ferramentas de controle de progresso (como listas TODO) é recomendado para gerenciar o fluxo de trabalho de forma estruturada*

---

## 📝 Glossário de Termos

- **Few-shot prompting (ou Few-shot learning):** É uma técnica que permite guiar um modelo de linguagem para uma nova tarefa ao incluir alguns exemplos de entrada e saída diretamente no prompt, sem a necessidade de realizar um ajuste fino (fine-tuning) no modelo. O modelo captura o padrão demonstrado nesses exemplos e o aplica à nova instrução.
- **Chain-of-Thought (Cadeia de Pensamento / CoT):** Processo pelo qual modelos de raciocínio (reasoning models) geram uma cadeia interna de pensamento para analisar o prompt de entrada. Essa abordagem faz com que o modelo se destaque na compreensão de tarefas complexas e no planejamento de múltiplas etapas.
- **System Prompt (Mensagem do Desenvolvedor / Instruções):** Refere-se às diretrizes fornecidas por meio do parâmetro de instruções da API ou por mensagens com o papel de "desenvolvedor" (developer). Elas definem as regras do sistema, o comportamento do assistente (como tom e objetivos) e a lógica de negócios.
- **Zero-shot prompting:** Embora as fontes tragam este termo listado como uma técnica fundamental de engenharia de prompt, elas não fornecem uma definição teórica explícita. No entanto, demonstram o conceito de forma prática ao citar que modelos avançados conseguem resolver tarefas complexas diretamente em um único prompt, sem a necessidade de exemplos.
- **Alucinação (Hallucination):** As fontes abordam a alucinação como um problema de factualidade que precisa ser mitigado para fortalecer as salvaguardas (guardrails) do sistema. A técnica de RAG (Retrieval-Augmented Generation), que adiciona dados de contexto relevantes ao prompt, auxilia ativamente na redução de alucinações.


---

## 🎙️ Audio Overview (Podcast de IA)

Como um dos diferenciais do projeto, utilizei o recurso nativo de geração de áudio do NotebookLM para criar um podcast interativo sobre os materiais.

<audio controls>
  <source src="audio/podcast.m4a" type="audio/mp4">
  Seu navegador não suporta o reprodutor de áudio nativo.
</audio>

---
*Caso o reprodutor acima não apareça no seu navegador, você pode ouvir ou baixar o arquivo diretamente aqui:*
👉 [🎙️ Ouvir o Podcast sobre Engenharia de Prompt (Formato .m4a)](audio/podcast.m4a)
---

## 🛠️ Tecnologias Utilizadas
*   **Google NotebookLM** (Ambiente de RAG e curadoria)
*   **Markdown** (Documentação)
*   **GitHub** (Hospedagem e portfólio)

---

Desenvolvido com dedicação para expandir os horizontes no estudo de Inteligência Artificial. 🚀
