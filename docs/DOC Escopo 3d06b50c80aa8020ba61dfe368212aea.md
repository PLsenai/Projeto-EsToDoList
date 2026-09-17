# DOC Escopo

# **Documento de Escopo — EsToDoList**

## **1. Objetivo do Projeto**

O projeto **EsToDoList** tem como objetivo ajudar os alunos a manter suas atividades escolares organizadas em um só lugar. Através do EsToDoList, será possível registrar tarefas, alterar informações, excluir atividades e acompanhar o que já foi realizado. Assim, o estudante poderá ter mais controle sobre seu desenvolvimento escolar.

## **2. Requisitos Funcionais (RF)**

### **RF 01 — Cadastrar Tarefa**

O sistema permitirá que o usuário adicione uma nova tarefa. Para isso, ele deverá informar o **nome da tarefa**, a **data de entrega,** e se for necessário uma **descrição**. Depois de salvar, a tarefa será adicionada à lista.

### **RF 02 — Editar Tarefa**

O usuário poderá modificar uma tarefa que já foi cadastrada. Ao selecionar a opção **Editar**, poderá alterar informações como o nome, a data de entrega e a descrição da atividade.

### **RF 03 — Excluir Tarefa**

O usuário poderá remover uma tarefa da sua lista através da opção **Excluir**. Antes de excluir o sistema solicitará uma confirmação para evitar que uma tarefa seja apagada por engano.

### **RF 04 — Marcar Tarefa como Concluída**

Quando terminar uma atividade, o usuário poderá marcá-la como **concluída**. O sistema apresentará uma mudança visual, como colocar um risco sobre o nome da tarefa e mudando a tarefa de cor, para diferenciá-la das atividades que ainda estão pendentes.

### **RF 05 — Pesquisar/Filtrar Tarefas**

O sistema permitirá que o usuário encontre suas tarefas com mais facilidade. Ele poderá pesquisar pelo nome da atividade e utilizar filtros para visualizar tarefas **pendentes** ou **concluídas**.

## **3. Requisitos Não Funcionais (RNF)**

### **RNF 01 — Usabilidade**

O sistema possuirá uma interface simples, permitindo que um aluno consiga entender as principais funções sem precisar de muitas instruções.

**Por que é importante:** Isso facilita o uso do sistema e permite que o estudante consiga organizar suas tarefas rapidamente.

### **RNF 02 — Desempenho**

O sistema carregará rapidamente e ações realizadas pelo usuário como cadastrar ou salvar uma tarefa, não deverão demorar mais que **2 segundos**.

**Por que é importante:** Um sistema rápido evita que o aluno perca tempo esperando e proporciona uma experiência melhor durante o uso.

### **RNF 03 — Flexibilidade**

O sistema irá se adaptar a diferentes tamanhos de tela, funcionando em **computadores, tablets e celulares**.

**Por que é importante:** Os estudantes podem acessar suas tarefas utilizando diferentes dispositivos, então o sistema precisa funcionar adequadamente em todos eles.

### **RNF 04 — Armazenamento**

As tarefas cadastradas irão ser armazenadas **diretamente no navegador do usuário**, utilizando o armazenamento local.

**Por que é importante:** Isso permite que as informações continuem disponíveis mesmo depois que o usuário fechar e abrir novamente a página.

## **4. Fora de Escopo**

### **1. Notificações**

A primeira versão não terá notificações automáticas para avisar o usuário sobre tarefas próximas da data de entrega.

**Justificativa:** Essa função não é essencial para o funcionamento inicial do ToDoList.

### **2. Login e cadastro de usuários**

A primeira versão não terá sistema de criação de contas ou login.

**Justificativa:** Como os dados serão armazenados localmente no navegador, não será necessário criar um sistema de usuários nesta primeira versão.

### **3. Compartilhamento de tarefas**

O usuário não poderá compartilhar suas tarefas com outros estudantes.

**Justificativa:** O objetivo inicial é oferecer uma ferramenta de organização individual.

## Modelo Cascata — EsToDoList

| **Requisitos** | **Análise** | **Desenvolvimento** | **Testes** | **Implementação** |
| --- | --- | --- | --- | --- |
| Escrever o Documento de Escopo com todas as funcionalidades. | Desenhar as telas do aplicativo no Figma. | Escrever o código HTML da página principal. | Verificar se o aplicativo funciona corretamente nos navegadores Chrome e Firefox. | Publicar a versão final do site em um servidor online para que todos possam usar. |
| Entrevistar alunos para entender como eles organizam suas tarefas hoje. | Definir a paleta de cores e a fonte que serão usadas no site. | Programar a função em JavaScript que salva uma nova tarefa no navegador. | Tentar "quebrar" o campo de data, inserindo um texto em vez de uma data válida. | Corrigir um bug encontrado após o lançamento do sistema. |
| Definir exatamente o que precisa acontecer para que um requisito (como *RF 03 - Excluir Tarefa* com confirmação) seja considerado pronto. | Desenhar o fluxo que o aluno fará desde a abertura da página até a busca/filtragem de tarefas pendentes ou concluídas | Implementar as regras de estilo e *media queries* no CSS para garantir o cumprimento do *RNF 03 - Flexibilidade* em computadores, tablets e celulares. | Testar a navegação e o layout em diferentes tamanhos de tela e navegadores para validar os requisitos de usabilidade e flexibilidade (*RNF 01* e *RNF 03*). | Criar uma breve documentação de instrução ou seção de dúvidas frequentes para orientar os alunos sobre como usar a plataforma. |
| Especificar regras e validações como, por exemplo, proibir a criação de tarefas sem título ou proibir datas de entrega anteriores à data atual. | Especificar exatamente como o objeto de tarefas será modelado em JSON no armazenamento local do navegador. | Programar as funções que filtram e exibem na tela apenas as tarefas que correspondem ao campo de busca ou aos filtros de pendentes/concluídas (*RF 05*). | Garantir que ao cadastrar/editar tarefas, fechar o navegador e reabri-lo, os dados continuem salvos conforme o *RNF 04*. | Garantir a disponibilidade da página no servidor e verificar logs de erros após a publicação da aplicação. |

## Matriz de risco

![image.png](image.png)

| Risco (Descrição) | Probabilidade (Baixa/Alta) | Impacto (Baixo/Alto) | Plano de ação (O que faremos para prevenir) |
| --- | --- | --- | --- |
| E se todo o código desenvolvido em uma aula fosse perdido por que ninguém fez commit ou enviou o projeto para o Github. | Baixa | Alto | Começar a tornar o ato de salvamento como um habito, utilizando outras formas de salvar também, um exemplo é o pendrive. |
| Internet indisponível no momento da entrega/apresentação | Alto | Alto | Baixar os trabalhos ou salvar eles em um pendrive. |
| Durante o desenvolvimento do EsToDoList, os estudantes testaram o sistema gostaram da ideia e começaram a pedir um chat novo para conversar sobre as tarefas. | Alto | Baixo ou Alto depende da ocasião | Ver se realmente é necessário e se é possível realizar as modificações pedidas. |