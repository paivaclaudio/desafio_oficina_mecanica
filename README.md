# Descrição do Desafio

## Modelagem para oficina mecânica

A partir da narrativa fornecida você será capaz de criar todas as entidades, relacionamentos e atributos. Caso encontre algo que não foi definido na narrativa, utilize a sua compreensão do contexto e deixe uma descrição no README do seu GitHub para verificação.


### Objetivo

Cria o esquema conceitual para o contexto de oficina com base na narrativa fornecida

### Narrativa:

- Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica
- Clientes levam veículos à oficina mecânica para serem consertados ou para passarem por revisões periódicas
- Cada veículo é designado a uma equipe de mecânicos que identifica os serviços a serem executados e preenche uma OS com data de entrega.
- A partir da OS, calcula-se o valor de cada serviço, consultando-se uma tabela de referência de mão-de-obra
- O valor de cada peça também irá compor a OS
- O cliente autoriza a execução dos serviços
- A mesma equipe avalia e executa os serviços
- Os mecânicos possuem código, nome, endereço e especialidade
- Cada OS possui: n°, data de emissão, um valor, status e uma data para conclusão dos trabalhos.

## 
### Observações da modelagem:

 - As entidades Servicos_a_executar e Necessidade_de_pecas possuem atributos para guardar o valor efetivo praticado, apesar de que as entidades Servico e Pecas possuam campos para preco_padrao. Isso se faz necessário pois o preco_padrao sofrerá alteração de valor ao longo do tempo e o preço efetivamente praticado em cada OS precisa ser guardado sem alterações para cálculos e/ou consultas futuras.
 - A entidade Avaliacao_execucao_OS possui um relacionamento 1:1 com a entidade Ordem_servico e poderiam ser unidas em uma única entidade para guardar os dados da OS, com campos opcionais para a parte de avaliação pela equipe.
