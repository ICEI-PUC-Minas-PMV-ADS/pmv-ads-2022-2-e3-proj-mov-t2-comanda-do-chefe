# Plano de Testes de Software

<span style="color:red">Pré-requisitos: <a href="2-Especificação do Projeto.md"> Especificação do Projeto</a></span>, <a href="3-Projeto de Interface.md"> Projeto de Interface</a>

Cenários de testes utilizados na realização dos testes da aplicação. De acordo com os requisitos funcionais e mostrando os critérios de êxito.

Casos de testes:
 
| **Caso de Teste** 	| CT-01 – Visualizar tela de login  	|
|:---:	|:---:	|
|	Requisito Associado 	| RF-01 - O aplicativo deve apresentar uma tela inicial de login para cada tipo de login o usuário deseja realizar. |
| Objetivo do Teste 	| Verificar se o aplicativo exibe todos os elementos requisitados. |
|   Passos | -                     -                 -    | 
|    1   	|    Acessar o Aplicativo                       |
|    2    |    Visualizar a página principal              |
|    3    |    Selecionar a opção de usuário              |
|    4    |    Visualizar a página inserção de dados      |
|                    |
|Critério de Êxito | Deve ser exibido uma tela de login para a entrada de usuários. |

<br>*

| **Caso de Teste** 	| CT-02 – Visualizar página de Acesso aos clientes.	|
| :---: | :---:|
|Requisito Associado | RF-03 - Na tela de entrada de dados devem haver campos solicitando algumas informações pessoais do cliente.    |
| Objetivo do Teste 	| Verificar se o aplicativo exibe uma página com campos de preenchimento para o usuário cadastrar os seus dados pessoais. |
| Passos |  -                -                         - |            
|    1   |     Acessar o aplicativo                      |
|    2   |     Visualizar a página principal             |
|    3   |     Selecionar a opção de usuário             |
|    4   |     Visualizar a página inserção de dados     |  
|    6   |     Cadastrar os dados solicitados            |
|                              
|                            
|                              
|Critério de Êxito |  Deve ser exibido após os dados preenchidos, uma página especifica direcionada ao menu de opções (Cardapio) do local.|

<br>*

| **Caso de Teste** 	| CT-03 – Visualizar página de menu de opções (Cardápio) do local.	|
| :---: | :---:|
|Requisito Associado | RF-04 - Na tela de menu, o aplicativo deverá exibir todas as opções de produtos disponíveis no cardápio.  |
| Objetivo do Teste 	| Verificar se o aplicativo exibe uma página com dados dos produtos, alterar, ver detalhes, excluir ou adicionar. |
| Passos   |     -                  -              - |
|     1    |    Acessar o aplicativo                 |
|     2    |    Visualizar a página principal        |
|     3    |    Selecionar a opção de usuário        |
|     4    |    Visualizar a página inserção de dados|  
|     5    |    Cadastrar os dados solicitados       |
|     6    |    Visualizar a página de menu de opções(Cardapio).   |
|          
|Critério de Êxito | Deve ser exibido após a exibição do menu, uma página especifica com os produtos selecionados pelo cliente.|
<br>*

| **Caso de Teste** 	| CT-04 – Visualizar página de Solicitação de Pedidos	|
| :---: | :---:|
|Requisito Associado | RF-04 -Na tela de gerenciamento o usuário será direcionado para esta página logo após selecionar seus produtos, sendo necessário escolher a quantidade desejada.  |
| Objetivo do Teste 	| Verificar se o aplicativo exibe uma página com dados dos produtos e alterar a solicitação. |
| Passos 	|  -              -                 -               |
|   1     |  Acessar o Aplicativo                             |
|   2     |  Visualizar a página principal                    | 
|   4     |  Selecionar a opção de usuário                    |
|   5     |  Visualizar a página inserção de dados            |
|   6     |  Cadastrar os dados solicitados                   |
|   7     |  Visualizar a página de menu de opções (Cardapio).|
|   8     |  Visualizar as opções de produtos                 |
|   9     |  Escolher a quantidade desejada                   |
|   10    |  Clicar em Alterar                                |
|   11    |  Informar o que deseja ser alterado               | 
|   12    |  Realizar pedido                                  |
|Critério de Êxito | Deve ser exibido na página especifica do gerenciamento de pedidos, a opção de alterar, informar o que deve ser alterado e realizar pedido.|

<br>*

| **Caso de Teste** 	| CT-05 – Visualizar página de Pagamento	|
| :---: | :---:|
|Requisito Associado | RF-06 -Na tela de gerenciamento do aplicativo, o aplicativo deve exibir a opção de “Formas de Pagamento |
| Objetivo do Teste 	| Verificar se o aplicativo exibe uma página com as opção de formas de pagamento: Cartão de crédito, Pix ou pagar no caixa. |
| Passos 	|        -         -             -                  |
|    1    |  Acessar o Aplicativo                             |                 
|    2    |  Visualizar a página principal                    |
|    3    |  Selecionar a opção de usuário                    |
|    4    |  Visualizar a página inserção de dados            | 
|    5    |  Visualizar a página de menu de opções (Cardapio).|       
|    6    |  Visualizar as opções de produtos                 |
|    7    |  Escolher a quantidade desejada                   |
|    8    |  Realizar pedido                                  |
|    9    |  Clicar na opção “Formas de pagamento”            |          
|    10   |  Solicitar os dados do cartão, sendo o pagamento por PIX , gerar o método de QR Code, sendo possível também pagar com o Copie e cole. |
|Critério de Êxito | Deve ser exibido na página especifica do gerenciamento de OS, a opção de Cartão de Crédito, Pix QR Code ou Link Copie cole.|
