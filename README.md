# Avaliação de Recuperação - Desenvolvimento Web II - 1º Trimestre

Esse é um projeto de avaliação de recuperação da disciplina de Desenvolvimento Web II do 1º Trimestre do curso Técnico em Informática para Internet integrado ao Ensino Médio do IFC - Campus Araquari.

## Objetivo

Foi desenvolvida uma aplicação modelo de um sistema de gerenciamento de tarefas. Uma versão funcional da aplicação pode ser acessada [aqui](https://modelo-recuperacao-2info-2024.surge.sh/). Você deve completar esse código disponível de forma a replicar o comportamento da aplicação modelo.

Para tal, você deve seguir as instruções detalhadas a seguir.

## Instruções

_Importante._

- Leia atentamente as instruções de cada questão.
- Leia todas as questões antes de começar a resolvê-las.

1. Instale os pacotes necessários para o projeto rodando o comando `npm install` no terminal.
2. No componente `ListarTarefas`, é necessária a definição de uma `prop` chamada `tarefas` que será um `array` obrigatório. Essa `prop` será responsável por passar as tarefas que serão exibidas na lista de tarefas. Adicione essa `prop` ao componente `ListarTarefas` e faça a sua tipagem.
3. No componente `AdicionarTarefa`, o botão de adicionar tarefa não está funcionando. Implemente a funcionalidade de adicionar tarefa ao clicar no botão, que pode ser similar ao evento de tecla `Enter` no campo de texto.
4. No componente `MainComp`, a tag `h1` está esperando uma variável com o nome `turma`. Esta variável não está definida. Defina a variável `turma` com o valor `1`, `2` ou `3` de acordo com a turma do aluno.
5. No componente `MainComp`, ao invocar o componente `AdicionarTarefa`, falta tratar o evento `adicionarTarefa`. Trate esse evento para que ele adicione a tarefa digitada no campo de texto ao clicar no botão ou ao pressionar a tecla `Enter`. Note que já existe uma função `adicionarTarefa` no componente `MainComp` que deve ser utilizada.
6. No componente `MainComp`, a tag `h2` com o título do `card` de tarefas em aberto, está esperando uma variável com o nome `tarefasEmAberto`. Esta variável não está definida. Defina a propriedade computada `tarefasEmAberto` com a quantidade de tarefas que ainda não foram concluídas.
7. No componente `MainComp`, no `card` de tarefas feitas, ao clicar em uma tarefa é chamada a função `reativarTarefa`, que não está definida. Implemente a função `reativarTarefa` que deve receber o `id` da tarefa a ser reativada e alterar o status `feita` da tarefa para `false`.
8. No component `App.vue`, o componente `<main-comp>` está sendo renderizado, mas ele não foi importado. Importe o componente `MainComp` que está em `src/components/MainComp.vue`.
9. Faça o deploy da aplicação no Surge ou no Vercel.
10. Envie o link do projeto no GitHub e o link do deploy da aplicação no SIGAA até o prazo estabelecido.
