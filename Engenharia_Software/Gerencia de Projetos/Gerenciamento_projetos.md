
***

# Roteiro de Gerenciamento de Projeto: Aplicativo de Pedidos para Restaurante

## 🧭 Princípio W5HH de Barry Boehm

O princípio W5HH de Barry Boehm é uma abordagem que guia o planejamento e visa garantir planejamentos simples para projetos simples, através de uma série de perguntas essenciais

| Pergunta | Resposta Aplicada ao Projeto (App de Pedidos) | Função no Planejamento (Conforme o Princípio) |
| :--- | :--- | :--- |
| **Why (Por que?)** | O objetivo é modernizar o processo de pedidos do restaurante para aumentar a **eficiência** do garçom, **reduzir erros** na comunicação com a cozinha e **acelerar o tempo** de atendimento ao cliente, visando a melhoria da experiência geral . | Avaliar a validade das razões comerciais para o desenvolvimento. |
| **What (O Quê?)** | Desenvolver um aplicativo móvel/tablet que permita ao garçom: 1) Receber o pedido do cliente. 2) Enviar o pedido eletronicamente à cozinha. 3) Monitorar o status (na cozinha, pronto). 4) Notificar o garçom quando o pedido estiver pronto para entrega . | Definir o conjunto de tarefas necessárias. |
| **When (Quando?)** | Definir um cronograma com marcos-chave (por exemplo, conclusão do protótipo em 4 semanas, teste beta em 8 semanas, lançamento final em 12 semanas) . | Definir o cronograma e os marcos (pontos de referência) . |
| **Who (Quem?)** | **Gerente de Projeto:** Liderança e coordenação. **Equipe de Desenvolvimento:** 2 Desenvolvedores (Front-end/Back-end). **Designers:** UI/UX. **Stakeholders:** Gerentes do restaurante, Garçons (usuários-chave), Clientes (usuários finais) . | Definir os papéis e responsabilidades. |
| **Where (Onde?)** | A equipe de desenvolvimento pode ser remota ou interna, mas a responsabilidade do uso final do aplicativo reside nos **garçons e na equipe de cozinha** do restaurante (posicionamento organizacional do uso) 52, . | Posicionamento organizacional das responsabilidades (incluindo clientes e usuários). |
| **How (Como?)** | Utilizar uma estratégia técnica de desenvolvimento nativo/híbrido e uma estratégia gerencial **Ágil** para permitir a rápida adaptação e o *feedback* frequente dos usuários (garçons). | Definir a estratégia técnica e gerencial. |
| **How much (Quanto?)** | Estimar custos de licenciamento de software, salários da equipe, custo de *hardware* (tablets) e manutenção contínua . | Estimar os recursos necessários . |

***

## 4 Ps do Gerenciamento

O gerenciamento eficiente concentra-se nos 4 Ps (Pessoas, Produto, Processo e Projeto), sendo essa ordem crucial para o sucesso .

### 1. Pessoas (Elemento-Chave)

As **Pessoas** são o elemento-chave e o fator de maior importância em todos os projetos de software, pois o trabalho consiste em esforço humano .

| Método para Melhorar as Pessoas Envolvidas | Descrição e Justificativa |
| :--- | :--- |
| **Formação de Equipe e Comunicação** | * **Equipe de Desenvolvimento:** Criar uma **equipe coesa**, auto-organizada e altamente motivada (Equipe Ágil), onde o todo é maior do que a soma das partes, e os membros são mais produtivos. * **Comunicação Garçom-Cozinha-Devs:** Utilizar métodos eficazes de coordenação e comunicação (formais e informais) para lidar com a incerteza e a interoperabilidade do software . |
| **Liderança e Gerenciamento do Desempenho** | * **Líder de Equipe (Devs/Garçons):** Selecionar um líder eficaz que adote um estilo de gerenciamento de **solução de problemas** e que deve **capacitar os outros a agir** (fomentar a colaboração e a confiança) e **inspirar e criar uma visão compartilhada** (motivando os membros). * **Treinamento:** Realizar um treinamento prático e contínuo. O People-CMM reconhece que as organizações devem aprimorar continuamente sua capacidade de atrair, desenvolver, motivar e reter a força de trabalho, sendo as práticas-chave a formação de equipe, comunicação, treinamento e gerenciamento do desempenho. |

***

### 2. Produto (Escopo)

O **Produto** (o software a ser construído) define o escopo do trabalho e a meta do projeto.

| Método para Definir o Escopo (Processo Rápido) | Descrição e Justificativa |
| :--- | :--- |
| **Estabelecer Objetivos e Escopo Quantitativo** | Antes de traçar um plano, é obrigatório estabelecer os objetivos e o escopo do produto. O escopo deve ser **quantitativamente** estabelecido (dados explícitos, restrições e limitações). Por exemplo, tempo de resposta do envio de pedido < 1 segundo, e taxa de redução de erros de pedidos em 90%. |
| **Definição de Escopo do Software (Três Elementos)** | O escopo é definido respondendo às questões sobre: **1. Contexto** (como o software se encaixa no sistema maior, ou seja, interface móvel integrada ao sistema de gestão). Objetivos da Informação** (dados de entrada e saída). Função e Desempenho** (funções principais e velocidade de operação). |
| **Decomposição do Problema** | Aplicar essa técnica na funcionalidade do app, transformando o problema complexo de "pedido completo" em questões menores e gerenciáveis: Seleção de mesa, Navegação de menu, Adição de itens e modificadores, Envio e Status. |
| **Inviabilidade do Planejamento** | Sem essa informação sólida de escopo (objetivos, restrições), é impossível definir estimativas de custo razoáveis, avaliação de riscos eficaz ou um cronograma gerenciável e realista. |

***

### 3. Processo (Metodologia)

O **Processo** de software fornece a metodologia pela qual o plano de projeto será estabelecido. Ele deve ser selecionado e adaptado para ser adequado às Pessoas e ao Produto.

| Processo Escolhido e Por Que | Descrição e Adaptação |
| :--- | :--- |
| **Processo Ágil (ex: Scrum ou Kanban)** | **Por que:** O Processo Ágil é ideal por enfatizar a **colaboração** e a **competência individual**, permitindo a **adaptação rápida** a mudanças de requisitos e a entrega de valor em incrementos curtos (necessário para um projeto que deve ser rapidamente realizado). |
| **Junção Produto e Processo** | O projeto começa com a junção do produto ao processo. Cada função principal do produto (ex: "Enviar Pedido") deve passar pelas atividades metodológicas genéricas: **Comunicação, Planejamento, Modelagem, Construção e Entrega**. |
| **Decomposição do Processo** | O coordenador do projeto adapta a metodologia (decomposição) para definir as tarefas concretas necessárias para preencher as atividades metodológicas (ex: definir "Codificar API de Pedido" como uma tarefa de **Construção** para a função "Enviar Pedido"). |

***

### 4. Projeto (Plano)

O **Projeto** é a atividade de planejamento, monitoramento e controle que utiliza as informações dos outros três Ps (Pessoas, Produto e Processo).

| Plano do Projeto (Documento Vivo) | Descrição |
| :--- | :--- |
| **Criação e Evolução do Plano** | Um plano de projeto é criado e evolui como um documento vivo, definindo o processo (Ágil), as tarefas, as pessoas que realizarão o trabalho e os mecanismos de avaliação de risco e qualidade. |
| **Definição de Papéis e Tarefas** | Utilizar o W5HH ("Quem") para identificar a equipe de desenvolvimento e os *stakeholders*  , e definir as tarefas específicas do *backlog* (derivadas da decomposição do produto e processo). |
| **Mecanismos de Qualidade e Monitoramento** | Incluir no plano práticas vitais como: **Gerenciamento de projeto baseado em métricas**, **Acompanhamento de valorização** (medir o progresso em relação ao valor comercial entregue) e **Acompanhamento de defeitos** em relação aos objetivos de qualidade. |
| **Avaliação de Risco** | O plano deve abordar riscos, evitando sinais de alerta comuns como escopo mal definido e prazos não realistas, utilizando **custos empíricos e estimativas de cronogramas** para garantir que o plano seja realista. |
