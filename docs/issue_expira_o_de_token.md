# Expiração e invalidacão de token de segurança

## Problema identificado
Tokens de segurança mantêm-se válidos indefinidamente ou permitem reutilização após o uso, expondo a conta do cliente bancário a acessos não autorizados.

## História de usuário
Como cliente bancário, desejo que meu token expire após um período definido e não possa ser reutilizado, para proteger minha conta.

## Correção proposta
- Definir um tempo limite de validade para os tokens de segurança.

- Invalidar o token imediatamente após o seu primeiro uso com sucesso.

- Rejeitar tentativas de acesso com tokens expirados ou reutilizados.

- Tratar e informar falhas sem expor dados sensíveis do cliente.


## Critérios de validação
- [ ] Confirmar que tokens expirados são rejeitados.

- [ ] Garantir que tokens utilizados não podem ser reutilizados.

- [ ] Verificar que o sistema informa falhas sem revelar dados sensíveis.

- [ ] Executar testes para expiração e reutilização do token.


## Observação
Este documento registra uma correção proposta para fins acadêmicos. A correção não foi implementada nem testada em um serviço real.