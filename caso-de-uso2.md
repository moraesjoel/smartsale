# Smart Sale

## Especificação de Caso de Uso: Avaliar produtos informados pelo cliente.

Este caso de uso tem por finalidade documentar os fluxos necessários para antendar a funcionalidade de avaliação dos produtos informados pelo cliente para serem posteriomente utilizados no ranqueamento.

| Versão | Comentário      |
| ------ | --------------- |
| 1.0    | Versão inicial. |

## Pré-condições

O cliente precisa estar logado no sistema

## Fluxo de eventos

### Fluxo Básico

### A. Incluir produtos

|     | Ação do ator                                         | Resposta do sistema                                                                    |
| --- | ---------------------------------------------------- | -------------------------------------------------------------------------------------- |
| 1   | O cliente acessa a opção de incluir produtos para avaliação.    | O sistema solicita um código para o grupo de produto que o usuário deseja inserir.                              |
| 2   | O cliente informa o código de grupo de produto.                 | O sistema valida as entradas de acordo com o dado inserido e pede a confirmação do cliente. |
| 3   | O cliente confirma os dados informados.              | O sistema possibilita ao cliente inserir um número limitado de produtos e disponibiliza campos para inserção    |
| 4   | O cliente informa os dados nos campos e seleciona a opção de salvar | O sistema valida as entradas do cliente                       |
| 5   |                                                      | O sistema emite uma mensagem de confirmação dos dados inseridos.                            |
| 6   | O cliente confirma os dados informados               | O sistema informa que a inclusão de produtos no código de grupo foi realizada com sucesso.                            |
| Fim |                                                      |                                                                                        |

### Fluxos Alternativos

### A. Usuário cancela o cadastro

|     | Ação do ator                                         | Resposta do sistema                                                                    |
| --- | ---------------------------------------------------- | -------------------------------------------------------------------------------------- |
| 1   | O cliente acessa a opção de cadastro de clientes.    | O sistema solicita os dados de e-mail do cliente e senha.                              |
| 2   | O cliente informa os dados solicitados corretamente. | O sistema valida as entradas de acordo com cada campo e pede a confirmação do cliente. |
| 3   | O cliente **não** confirma os dados informados.      | O sistema informa que o cadastro será cancelado.                                       |
| 3.1 |                                                      | O sistema fecha o cadastro de cliente.                                                 |
| Fim |  

### B. Usuário deleta o cadastro
#### Pré-condições

O cliente precisa estar cadastrado e logado.

|     | Ação do ator                                             | Resposta do sistema                                                                |
|-----|----------------------------------------------------------|------------------------------------------------------------------------------------|
| 1   | O cliente acessa o menu de assinaturas.                  | O sistema abre a página de assinaturas do sistema Smart Sale.                      |
| 2   | O cliente seleciona a assinatura atual.                  | O sistema abre a página de detalhes da assinatura.                                 |
| 3   | O cliente seleciona a opção configurações da assinatura. | O sistema abre a página de configurações da assinatura.                            |
| 4   | O cliente seleciona a opção de cancelar assinatura.      | O sistema pede a confirmação da ação.                                              |
| 4.1 | O cliente confirma o cancelamento da sua assinatura.     | O sistema envia ao cliente um e-mail de confirmação do cancelamento da assinatura. |
| 4.2 |                                                          | O sistema altera as informações da assinatura para cancelada.                      |
| 4.3 |                                                          | O sistema cancela as operações de cobrança.                                        |
| 4.4 |                                                          | O sistema informa que o cancelamento foi realizado com sucesso.                    |
| Fim |                                                          |                                                                                    |

### Fluxos de Exceção

### A. Usuário informa dados incorretos

|     | Ação do ator                                                   | Resposta do sistema                                           |
| --- | -------------------------------------------------------------- | ------------------------------------------------------------- |
| 1   | O cliente acessa a opção de cadastro de clientes.              | O sistema solicita os dados de e-mail do cliente e senha.     |
| 2   | O cliente informa os dados solicitados com um e-mail inválido. | O sistema valida as entradas de acordo com cada campo.        |
| 2.1 |                                                                | O sistema informa o cliente que o e-mail informado é inválido |
| Fim |

### B. Usuário previamente cadastrado

|     | Ação do ator                                                        | Resposta do sistema                                                   |
| --- | ------------------------------------------------------------------- | --------------------------------------------------------------------- |
| 1   | O cliente acessa a opção de cadastro de clientes.                   | O sistema solicita os dados de e-mail do cliente e senha.             |
| 2   | O cliente informa os dados solicitados com um e-mail já cadastrado. | O sistema valida as entradas de acordo com cada campo.                |
| 2.1 |                                                                     | O sistema informa o cliente que o e-mail informado já está cadastrado |
| Fim |

## Pontos de Extensão

## Pós-condições

## Requisitos Especiais

## Observações
