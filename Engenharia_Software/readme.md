### Guilherme Sebin - Engenharia de Software FATEC São Carlos 2025
### Prof. Arnaldo Napolitano Sanchez

# App para Atendimento em Restaurantes 🥪🥝

Após ter trabalhado anos em bares e restaurantes, eu quis fazer algo simples que facilitasse a vida dos atendentes de restaurantes.
Já existem diversos apps e programas para gerenciamento e coordenação de pedidos para este tipo de atividade, porém sempre senti dificuldade em utilizar estas ferramentas.
Como exemplo, posso citar Colibri, Totvs, Abrahão, GrandChef. Todos possuem extensas utilidades para diversos fins. 
Temos que ter em mente que trabalhar em um restaurante não se resume apenas em realizar um pedido e entregá-lo.
É necessário ter registros, controle de estoque, emissão de notas fiscais e contabilidade, adição e personalização de itens a serem ofertados e muitas outras pequenas funções que podem facilitar a vida daqueles que gerenciam um ou mais estabelecimentos do gênero.
Porém, a cada novo restaurante pelo qual eu passava, a utilização dos sistemas se mostrava extremamente diferente e confusa.
Os programas citados acima permitem diversas customizações e utilizam esta "feature" como uma ideia de que quanto mais customizável, melhor. Eu discordo desta visão. Acredito que ter um esquema claro e direto sobre o uso dos sistemas para os atendentes deve ser a parte principal deste programa.
A gestão e aquele que gere o estabelecimento deve sim ter acesso à diversas funções que possam atender às diversas necessidades impostas no exercício da função, mas o atendente, ao meu ver, não deveria se preocupar com estes quesitos. Seu trabalho é atender de maneira rápida e eficiente, permitindo focar no cliente e dar maior atenção.
Em diversas ocasiões, o atendimento se torna mecânico e impessoal, como o auto-atendimento realizado pelo setor de Fast-Food. Alguns estabelecimentos requerem que a experiência seja esta, mas também discordo da visão. O setor de restaurantes é descrito como setor da *Hospitalidade*, ou seja estar aberto para receber, acolher e servir. A diferença entre ter seu pedido anotado e ser atendido é completamente diferente. Ter alguém que possa escutar e entender o que desejamos, faz clara diferença na experiência para o cliente. Não é à toa que existem as 'Estrelas Michelin', ou guias que realizam avaliações sobre estabelecimentos, pelos quais nos guiamos para escolher onde comer e ter boas experiências. 

Após esta declaração, faço das minhas visões e experiências, a ideia de adequação ao atendimento que possa facilitar o serviço do atendente e melhorar a visita do cliente ao estabelecimento.


-----------------------------------------------------------------
## Objetivo do projeto

- Criar um sistema simplificado para atendimento ao cliente em bares e restaurantes, dando espaço para o atendimento personalizado.
- Visão clara e ágil para os gestores focarem no background do estabelecimento.
- Ter menus simplificados e diretos, facilitando a escolha de items, customização com anotações sobre cada pedido e direcionamento para cada área específica.
- Permitir uso do app por celular ou computador, possibilitando usos diversos.



Link para página de desenvolvimento do projeto - https://github.com/users/GuilhermeSebin/projects/4

-------------------------------------------------------------------------

## Diagrama de Casos de Uso

<img width="3172" height="2644" alt="image" src="https://github.com/user-attachments/assets/477dad78-ed87-4f5c-b1bc-e7d6cb140885" />

-------------------------------------------------------------------------

## Diagrama de Sequência

![unnamed](https://github.com/user-attachments/assets/7c25f16b-aee1-45a4-89fa-6d780a9cbe80)

-------------------------------------------------------------------------

## Histórias de Usuário

### **Funcionalidade: Realização de Pedidos e Validação de Estoque**
**Como** atendente
**Quero** lançar pedidos no sistema e ser avisado se houver falta de insumos
**Para** garantir que a cozinha receba apenas pedidos que consegue preparar

#### **Cenário 1: Envio de pedido com sucesso **
> *(Em caso de Estoque OK)*
* **Dado** que o Atendente selecionou a mesa e os itens do pedido na Tela
* **Quando** ele confirmar o envio do pedido
* **Então** o Backend deve validar que há estoque disponível
* **E** a Cozinha deve receber a impressão da comanda ou visualização no KDS
* **E** a Tela do atendente deve exibir a mensagem "Pedido Enviado com Sucesso"

#### **Cenário 2: Tentativa de pedido com insumo indisponível (Fluxo de Exceção)**
> (Em caso de Insumo Indisponível)*
* **Dado** que o Atendente enviou um pedido de um prato específico
* **Quando** o Backend verificar que não há insumos suficientes no estoque
* **Então** o sistema deve retornar um erro "Sem Insumo" para a Tela
* **E** um popup de alerta deve aparecer para o Atendente
* **E** o pedido **não** deve ser enviado para a Cozinha
* **E** o Atendente deve solicitar a substituição do item ao Cliente

---

### **Funcionalidade: Preparo e Notificação de Entrega**
**Como** equipe da cozinha
**Quero** notificar o atendente assim que um prato estiver pronto
**Para** que o cliente receba a comida fresca e quente o mais rápido possível

#### **Cenário: Notificação de prato pronto**
* **Dado** que a Cozinha finalizou o preparo de um prato
* **Quando** a equipe marcar o item como "PRONTO" no display da Cozinha
* **Então** o Backend deve enviar uma Push Notification para o dispositivo do Atendente
* **E** a Tela do atendente deve emitir um alerta sonoro ou visual indicando "Mesa X - Pedido Pronto"
* **E** o Atendente deve se dirigir à cozinha para retirar e servir o pedido

---

### **Funcionalidade: Pagamento e Processamento Automático**
**Como** dono do restaurante
**Quero** que o fechamento da conta atualize automaticamente o financeiro e o estoque
**Para** evitar erros manuais e ter dados precisos em tempo real

#### **Cenário: Fechamento de conta e atualizações sistêmicas**
* **Dado** que o Atendente solicitou o fechamento da conta na Tela
* **E** o sistema retornou o resumo de valores corretamente
* **Quando** o Atendente confirmar o recebimento do pagamento (Cartão ou Dinheiro)
* **Então** o Backend deve emitir a Nota Fiscal (NFC-e) via API do Governo
* **E** simultaneamente deve deduzir os ingredientes consumidos do Estoque
* **E** creditar o valor da venda no módulo Financeiro
* **E** a Tela deve exibir a mensagem "Pagamento Aprovado"

---

### **Funcionalidade: Dashboard de Gestão**
**Como** dono do restaurante
**Quero** visualizar relatórios atualizados em tempo real
**Para** tomar decisões baseadas nas vendas e no nível de estoque atual

#### **Cenário: Visualização de métricas**
* **Dado** que o Dono acessou a área de Dashboard na Tela
* **Quando** a tela carregar
* **Então** o sistema deve buscar os dados mais recentes no Backend
* **E** exibir gráficos atualizados de Vendas do Dia e Níveis de Estoque

-------------------------------------------------------------------------

## Documentação: 5W e 2H

https://github.com/GuilhermeSebin/FATEC_Semestre2/blob/main/Engenharia_Software/Gerencia%20de%20Projetos/Gerenciamento_projetos.md

-------------------------------------------------------------------------

## Visão da interface (protótipo)

![unnamed](https://github.com/user-attachments/assets/40e7ddc5-9199-409c-a1cd-e5294b62a1f4)


--- 
### Visão de menu (comida)

![unnamed](https://github.com/user-attachments/assets/2759f200-fb3b-41fd-ac77-ca82ded5f1f4)

--- 
### Visão do menu de gestão acessível apenas pela gerência

![unnamed](https://github.com/user-attachments/assets/19239d30-d981-4b60-accc-90cb226de259)

---
### Visão de gerenciamento em PC (acesso geral à todas funções)

![unnamed](https://github.com/user-attachments/assets/7c506d6b-b2b9-4bac-9e9d-2b8058515bc7)


