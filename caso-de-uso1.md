# Smart Sale

## Especificação de Caso de Uso: Manter um Cadastro de Clientes

Este caso de uso tem como finalidade documentar os fluxos necessários para contemplar o cadastro de clientes no sistema Smart Sale.

| Versão | Comentário      |
| ------ | --------------- |
| 1.0    | Versão inicial. |

## Pré-condições

Nenhuma.

## Fluxo de eventos

### A. Fluxo Básico

### Incluir cliente

|     | Ação do ator                                                      | Resposta do sistema                                                                    |
| --- | ----------------------------------------------------              | -------------------------------------------------------------------------------------- |
| 1   | O cliente solicita a opção de cadastro para um novo cliente. (B2)(B3) | O sistema pede para que o usuário informe os dados de e-mail, telefone do cliente e senha.   |
| 2   | O cliente informa os dados solicitados pelo sistema.              | O sistema faz a validação das entradas de acordo com cada campo e pede pela confirmação do cliente.(C2) |
| 3   | O cliente faz a confirmação os dados.                             | O sistema salva os dados.                                                                           |
| 4   |                                                                   | O sistema envia ao cliente um e-mail com link para a confirmação do cadastro.                       |
| 5   | O cliente abre o link recebido por email e confirma cadastro      | O sistema informa que o cadastro foi realizado com sucesso.                                         |
| Fim |                                                                   |                                                                                                     |

### B. Fluxos Alternativos

### B1. Usuário consulta o seu cadastro
#### Pré-condições

O cliente precisa estar cadastrado e logado.

|     | Ação do ator                                             | Resposta do sistema                                                                |
|-----|----------------------------------------------------------|------------------------------------------------------------------------------------|
| 1   | No passo A.1, o cliente acessa o menu de assinatura.                   | O sistema abre a página de assinaturas.                                            |
| 2   | O cliente seleciona a assinatura atual.                  | O sistema abre a página de detalhes da assinatura.                                 |
| 3   | O cliente seleciona a opção configurações da assinatura. | O sistema abre a página de configurações da assinatura.                            |
| 4   | O cliente seleciona a opção de dados pessoais.           | O sistema informa o e-mail e telefone cadastrados                                  |
| 5   |                                                          | O sistema retorna para o passo 'Fim' de A.                                         |
| Fim |     

### B2. Usuário edita o e-mail cadastrado
#### Pré-condições

O cliente precisa estar cadastrado e logado.

|     | Ação do ator                                             | Resposta do sistema                                                                |
|-----|----------------------------------------------------------|------------------------------------------------------------------------------------|
| 1   | No passo A.1, o cliente acessa o menu de assinaturas.                  | O sistema abre a página de assinaturas do sistema Smart Sale.                      |
| 2   | O cliente seleciona a assinatura atual.                  | O sistema abre a página de detalhes da assinatura.                                 |
| 3   | O cliente seleciona a opção configurações da assinatura. | O sistema abre a página de configurações da assinatura.                            |
| 4   | O cliente seleciona a opção de editar assinatura.        | O sistema pede a confirmação da ação.                                              |
| 5   | O cliente confirma a ação.                               | O sistema informa os dados previamente cadastrados e permite edição do campo de e-mail, telefone e senha     |
| 6   | O cliente edita o campo de e-mail.                       | O sistema valida a entrada do dado e pede a confirmação do dado inserido. (C1)                               |
| 7   | O cliente faz a confirmação                              | O sistema envia ao cliente um e-mail com link para a confirmação da edição do e-mail.      |
| 8   | O cliente abre o link recebido por email e confirma      | O sistema informa que o e-mail cadastrado foi editado com sucesso.                 |  
| 9   |                                                          | O sistema retorna para o passo 'Fim' de A.                                         |
| Fim |                                                          |                                                                                    |

### C. Fluxos de Exceção

### C1. Usuário informa e-mail incorreto durante edição

|     | Ação do ator                                                   | Resposta do sistema                                           |
| --- | -------------------------------------------------------------- | ------------------------------------------------------------- |
| 1   |                                                                | No passo de resposta do sistema B2.6, o sistema não valida os dados do novo e-mail inserido|
| 2   |                                                                | O sistema emite uma mensagem que o e-mail inserido é inválido       |
| 3   | O cliente confirma a leitura da mensagem enviado pelo sistema. | Retorna para ação do autor no passo B2.6                            |
| Fim |

### C2. Usuário informa senha incorreta durante cadastro

|     | Ação do ator                                                        | Resposta do sistema                                                   |
| --- | ------------------------------------------------------------------- | --------------------------------------------------------------------- |
| 1   |                                                                     | No passo de resposta do sistema A.2, o sistema não valida os dados da senha escolhida.   |
| 2   |                                                                     | O sistema emite uma mensagem informando que a senha inserida é inválida e os requisitos de senha. |
| 3   | O cliente confirma a leitura da mensagem do sistema                 | O sistema retorna para ação do autor no passo A.2                    |
| Fim |

## Pontos de Extensão

## Pós-condições

## Requisitos Especiais

## Observações
