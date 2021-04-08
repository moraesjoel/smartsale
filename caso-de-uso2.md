# Smart Sale

## Especificação de Caso de Uso: Avaliar produtos informados pelo cliente.

Este caso de uso tem por finalidade documentar os fluxos necessários para antendar a funcionalidade de avaliação dos produtos informados pelo cliente para serem posteriomente utilizados no ranqueamento.

| Versão | Comentário      |
| ------ | --------------- |
| 1.0    | Versão inicial. |

## Pré-condições

O cliente precisa estar logado no sistema

## Fluxo de eventos

### A. Fluxo Básico

### Incluir produtos

|     | Ação do ator                                         | Resposta do sistema                                                                    |
| --- | ---------------------------------------------------- | -------------------------------------------------------------------------------------- |
| 1   | O cliente solicita a opção de incluir produtos para avaliação. (B2) | O sistema solicita um código para o grupo de produto que o usuário deseja inserir.        |
| 2   | O cliente informa o código de grupo de produto.                 | O sistema valida as entradas de acordo com o dado inserido e pede a confirmação do cliente. |
| 3   | O cliente confirma os dados informados.              | O sistema possibilita ao cliente inserir um número limitado de produtos e disponibiliza campos para inserção.  |
| 4   | O cliente informa os dados nos campos e seleciona a opção de salvar | O sistema valida as entradas do cliente.                       |
| 5   |                                                      | O sistema emite uma mensagem de confirmação dos dados inseridos.                       |
| 6   | O cliente confirma os dados informados. (B1)         | O sistema informa que a inclusão de produtos no código de grupo foi realizada com sucesso.       |
| Fim |                                                      |                                                                                        |

### B. Fluxos Alternativos

### B1. Usuário cancela a inclusão de produtos

|     | Ação do ator                                         | Resposta do sistema                                                                    |
| --- | ---------------------------------------------------- | -------------------------------------------------------------------------------------- |
| 1   | No passo A.6, o cliente não confirma os dados informados.   | O sistema informa que o cadastramento de produtos foi cancelado.                |
| 2   | O cliente confirma a leitura da mensagem.                   | O sistema retorna para o passo 'Fim' de A. |
| Fim |  

### B2. Usuário deleta grupo de produtos cadastrados 

|     | Ação do ator                                             | Resposta do sistema                                                                |
|-----|----------------------------------------------------------|------------------------------------------------------------------------------------|
| 1   | No passo A.1, o cliente solicita a exclusão de produtos. | O sistema solicita o código de grupo de produto que o usuário deseja remover.      |
| 2   | O cliente insere o código solicitado.                    | O sistema valida a entrada do cliente.                                             |
| 3   |                                                          | O sistema emite uma mensagem pedindo a confirmação da ação.                        |
| 4   | O cliente confirma a leitura da mensagem e da ação.      | O sistema remove o grupo de produto informado a partir do código.                  |
| 5   |                                                          | O sistema informa que a remoção foi realizada com sucesso.                         |
| 6   |                                                          | O sistema retorna para o passo 'Fim' de A.                                         |
| Fim |                                                          |                                                                                    |

### C. Fluxos de Exceção

### C1. Usuário informa dados incorretos

|     | Ação do ator                                                   | Resposta do sistema                                           |
| --- | -------------------------------------------------------------- | ------------------------------------------------------------- |
| 1   | O cliente acessa a opção de cadastro de clientes.              | O sistema solicita os dados de e-mail do cliente e senha.     |
| 2   | O cliente informa os dados solicitados com um e-mail inválido. | O sistema valida as entradas de acordo com cada campo.        |
| 2.1 |                                                                | O sistema informa o cliente que o e-mail informado é inválido |
| Fim |

### C2. Usuário previamente cadastrado

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
