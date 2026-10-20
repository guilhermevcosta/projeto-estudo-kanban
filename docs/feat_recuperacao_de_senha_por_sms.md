# feat: implementar recuperacao de senha via token SMS

## Problema Identificado

Clientes sem acesso a senha precisam de atendimento manual para redefinir o acesso. Isso gera demora no atendimento, aumento de chamados no suporte e insatisfacao do usuario.

## Correcao Proposta

Criar um fluxo automatico de recuperacao de senha por SMS contendo as seguintes etapas:

1. O usuario solicita a recuperacao informando seu identificador.
2. O sistema envia um token numerico de uso unico por SMS com tempo limite de validade.
3. O usuario digita o token e o sistema valida as informacoes.
4. Apos a validacao, o usuario cadastra a nova senha.

## Criterios de Validacao

* Permite solicitar o token de recuperacao.
* O token possui prazo de validade definido.
* O sistema valida o token antes de liberar a redefinicao da senha.
* Existem testes automatizados para tokens validos, invalidos e expirados.
* Nenhuma informacao sensivel e exibida em mensagens de erro.