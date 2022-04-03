## Gestão de Processos - BPM/ECM Essentials

### 1. Sobre Processos de negócio

O que é BPM?

BPM (Business Process Management ou Gerenciamento de Processos de Negócio) é um modelo que abrange a modelagem, automação, execução, controle e melhoria contínua de processos de negócio.

O que é ECM?

ECM(Enterprise Content Management ou Gestão de Conteúdo Empresarial) é uma combinação dinâmica de estratégias, métodos e ferramentas que são utilizados para capturar, gerenciar, armazenar, preservar e oferecer informações de apoio aos processos organizacionais durante seu ciclo de vida.

### O que é processo ?

* Uma sequência continuada de fatos ou operações 
* Um processo sempre tem o intuito de alcançar algum resultado
* Para que este resultado seja alcançado é necessário que sejam executadas tarefas (atividades)
* Essas atividades devem ter um fluxo como o workflow

##### Workflow: Em resumo, é o passo a passo mais eficiente e prático para a execução de um trabalho.
É o método usado para organizar o fluxo de trabalho em uma empresa. Ele consiste na disposição e realização das atividades em sequência lógica, preferencialmente de forma automatizada.

### Conhecendo as propriedades do processo com modelagem:

##### BPMN (Business Process Model and Notation ou Modelo de Processo de Negócios e Notação) é uma notação para modelagem de processos de negócio. Em outras palavras, o BPMN estabelece um padrão para representar os processos graficamente, por meio de diagramas.

🟩- Início
-Indica o início do processo
-Usuários que tiverem a permissão poderão iniciar o mesmo através da tela de inicialização de solicitações do fluig
-As permissões são definidas através do mecanismo de atribuição desta atividade
O fluig aceitará apenas uma única instância de objeto de Início comum por diagrama

🟥- Fim
-Indica o fim do processo

-Esta tarefa não é atribuída a nenhum usuário

-Não ocorrem processamentos após o final da solicitação(exceto via desenvolvimento)

-É possível ter um ou mais Finais comuns

-Neste componente podemos alterar o nome e marcar quais os usuários que serão notificados ao chegar nesta atividade.

⬜- Atividade comum
-É a unidade básica da separação de um processo em atividades
-Deverá ser executado por um usuário para dar andamento a solicitação

🟨- Automático (Gateway Exclusivo)
Irá decidir o destino de um processo através de programação que
será utilizada para mover o processo para a atividade relacionada
Apenas um caminho poderá ser percorrido utilizado este tipo de gateway.
 Além de alterar o nome de exibição, neste componente podemos definir quais as condições a serem validadas bem como as atividades de destino.

🟩- Fluxo Comum
-Padrão para movimentação de atividades
-Permite que uma atividade seja movimentada sem a possibilidade de retorno

🟥- Fluxo de Retorno
-Permite retorno para a atividade de origem

🟨- Fluxo Automático 
-Se o prazo da atividade for concluído sem que ela tenha sido movimentada, será movido automaticamente
-Obrigatório que a atividade de origem tenha um prazo definido e que uma tarefa agendada seja configurada (Fluxo automático)

🟦- Swinlane:
-Componente é utilizado para definir o escopo de cada processo  e possibilita identificar os papéis responsáveis pela execução 

📒- Documento
 -Permite anexar ao diagrama um documento previamente publicado no fluig a fim de que o mesmo possa ser consultado durante a fase de execução de um processo

📝- Anotação
 -Permite adicionar notas explicativas para facilitar o entendimento do processo por todos os envolvidos

🎗- Fork & Join:
 -Fork e Join indicam, respectivamente, o início e o fim das atividades paralelas
-Caso existam atividades paralelas pendentes, o processo fica posicionado no Join, até que todas as atividades sejam concluídas

⬜- Subprocesso:
-Alterar as características do componente e selecionar qual subprocesso será inicializado ao chegar nesta atividade.

⬛- Subprocesso Ad Hoc
-Criar lista de tarefas, definir o que será feito o responsável em executar a tarefa e qual o prazo. 


### O que são mecanismos de atribuição ? 

* Os Mecanismos de Atribuição permitem restringir as opções de usuários que podem receber ou assumir uma determinada atividade do processo

* Cada mecanismo permite que apenas determinado usuário ou usuários estabelecidos pela lógica interna do mecanismo tenham controle sobre a respectiva atividade

Atribuições: 

* Para um Papel (Pool) = Qualquer um dos usuários no papel escolhido pode assumir as tarefas para completá-las

* Para um Grupo (Pool) = Qualquer um dos usuários no grupo escolhido pode assumir as tarefas para completá-las

* Por Associação = Permite compor lógicas complexas de atribuição através da associação de vários mecanismos

* Por Campo de Formulário = Permite atribuir tarefas ao usuário informado em um campo do formulário do processo

### Regras nos campos de formulário:

Podemos adicionar regras nos campos do formulário para definir o comportamento dos campos em todas as atividades do processo.





