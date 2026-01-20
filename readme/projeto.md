
Trabalho realizado por Sara Pina.

Link do repositório: https://github.com/sararmpina-prog/Dashboard-Users.git


# Principais decisões tomadas e justificação da adequação

## Código 
O código (_main users.ts_ e _main tasks.ts_) segue de forma genérica o mesmo seguimento. 

Iniciei pela criação dos elementos (_Classe_, _Interface_ e _array_).

Seguidamente pelas funções de renderização de cada elemento individual `renderUserCard()` e `createSingleTask()` seguida pela função de renderização de todos os elementos `renderUtilizadores()` e `renderTasks()`.

Paralelamente, tentei manter o código limpo através da criação de funções com uma única funcionalidade (de forma genérica) para melhor legibilidade. 

Por exemplo, criei funções separadas para a criação de cada elemento botão, a título de exemplo, a função `createBtnActivateToggle()`, acompanhadas pela função que chamo subsequentemente, neste caso, `switchUserState()` após associado evento _click_ (`addEventListener`). 

O código apresenta o nome das funções em inglês, contudo algumas variáveis estão em português, sendo um dos aspectos que irei melhorar futuramente de forma a uniformizar o código. 
Similarmente, colocarei comentários no código para a legibilidade ser mais facilitada. 

Deixei comentada a função `renderDebugData()` assim como a respectiva tag HTML _footer_, para utilização futura na progressão do projecto, sendo que não tem usuabilidade na respetiva página em si. 

## Selecção das funcionalidades 

Para este projecto, o meu foco principal foi concretizar as funcionalidades solicitadas e as mesmas serem bem conseguidas. 

Neste sentido, o foco menor foi a nível de CSS e consequentemente a responsividade, que são aspectos que podem ser melhorados futuramente.

Ambos os sites estão construídos em inglês e tentei manter uniformização na estética e estrutura de ambas as páginas. 


## Tasks Dashboard

Nesta página apresento um dashboard com diferentes tarefas, que permite de um forma generalizada a apresentação e manipulação das mesmas (adição, remoção e aplicação de filtros). 

Ao iniciar a página, estão presentes as tarefas (objetos do tipo Classe Tarefa) que foram adicionadas ao array original _lista de Tarefas_.
A Classe Tarefa implementa ainda a interface Tarefa.

Utilizei para este efeito, a função `loadInitialTasks()` que recebe um array de dados (objetos) e automatiza, através de um ciclo que percorre o array, a criação de objetos do tipo Tarefa e adiciona ao array _listaTarefas_. 

No cabeçalho da página, existe uma opção para Users e outra para Tasks.
Ao clicar em cada uma destas opções, remete para a respectiva página.
Neste caso, User remete para o Users Dashboard aberto numa página à parte e a opção Tasks mantêm na mesma página. 

No topo da página, próximo do título "Tasks Dashboards", podemos ver o número de tarefas totais. Ao passar sobre o mesmo aparece a componente descritiva ("total number of tasks") através da colocação do atributo "title" na tag respectiva do html.

Entre as funcionalidades presentes na Tasks Dashboard estão as seguintes:
 - Adicionar uma nova tarefa (associando uma categoria);
 - Pesquisar uma tarefa (barra de pesquisa);
 - Filtrar as tarefas apresentadas através de duas opções:
   Remover todas as tarefas concluidas;
   Apresentar as tarefas presentes por ordem alfabética; 

Adicionalmente, em cada tarefa é possível:
- Remover a tarefa;
- Marcar como concluída (toggle check) através da classe _riscarTarefa_;
- Editar (se ainda não concluida); 
Na edição da tarefa, é possível alterar a tarefa inserida ou cancelar a edição (botões update e cancel, respectivamente).

As categorias são identificavéis pela atribuição de cor diferente consoante as categorias, e ainda através da colocação do nome da categoria associado à tarefa no dashboard. 


## Users Dashboard

Idêntico à página anterior de uma forma generalizada este dashboard apresenta a gestão dos usuários.

Ao iniciar a página vão ser exibidos os utilizadores que criei (objetos do tipo Classe Utilizador) que foram colocados no array _listaUtilizadores_. Esta Classe implementa interface Utilizador.
Os objetos do tipo Utilizador foram criados de forma idêntica à anterior com a função ` loadInitialUsers()`. 


No topo da página, apresento, similarmente, três identificadores que dão informação sobre o número de utilizadores activos; inactivos e totais. 
Estes identificadores mudam dinamicamente à medida que os utilizadores sofrem alterações (removidos, alterado o estado) ou inclusive são adicionados novos. 

Ainda é possível ver a percentagem de utilizadores activos a mudar dinamicamente. Fiz a opção de manter com 2 casas decimais (ver função `renderActiveUsersPercentage()` para mais informação).

Esta página permite as seguintes funcionalidades:
 - Adicionar um novo usuário (para verificação de email usada função regex); 
 - Filtrar os usuários através das seguintes opções:
   Ordenar alfabeticamente;
   Mostrar só os utilizadores activos (logged in);
   Pesquisar um usuário (barra de pesquisa);

Para tirar todos os filtros pode-se selecionar o botão "reset all filters" ou retirar os filtros pretendidos ao clicar (quando selecionado o filtro apresenta borda vermelha que é removida se filtro não está aplicado).

Em cada utilizador, é possível: 
- ativar toggle (permite alterar sessões, Logged in and logged out); 
- remover utilizador 
- ver mais (template com um pop-up que exibe informação adicional sobre cada respectivo utilizador). 


# Passos para executar as páginas

Neste momento, é possível executar as funcionalidades dentro de cada página (ainda não existe uma interligação directa entre cada utilizador e as suas tarefas) sem uma ordem necessariamente ímplicita. 

Neste sentido, não existe uma preferência no seguimento a que se dá na visualização de cada página. 

Ainda, as funcionalidades que trabalhei em cada página estão descritas na secção anterior e podem ser encontradas em cada página. 
