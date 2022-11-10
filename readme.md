# AUTO-CTE

## Problema atual:
Ao ser gerada nota fiscal de venda, deve-se gerar o CTE (Conhecimento de Transporte Eletrônico) manualmente, pois o sistema não gera automaticamente.
***
## 3 Caracterização do sistema
### Caracteristicas do sistema AUTO-CTE
AUTO-CTE - O CTE é um documento fiscal eletrônico, emitido por transportadores de cargas, que tem como finalidade comprovar a prestação de serviço de transporte de cargas. O CTE é um documento fiscal que substitui o conhecimento tradicional de transporte rodoviário de cargas.

### Objetivo:
O sistema de AUTO-CTE deve ser capaz de gerar o CTE de forma automática e integrada com o atual sistema de NF, caso a venda seja gerada por nota fiscal, dessa forma não será necessário mão de obra dedicada para tal operação. No caso a venda seja gerada por pedido de venda, será possivel o preenchimento e geração do CTE de forma manual.
Em Ambos os casos, o envio para o(s) orgão(s) fiscais e demais responsáveis, será feito de forma totalmente automática.

### Beneficios:
- Redução de custos com mão de obra
- Redução de erros humanos
- Redução de tempo de geração do CTE
- Redução de tempo de envio do CTE para o cliente
- Redução de tempo de envio do CTE para o transportador
- Redução de tempo de envio do CTE para a receita federal
- Redução de tempo de envio do CTE para a prefeitura
- Redução de tempo de envio do CTE para a SEFAZ

### Escopo do Sistema:
- Geração do CTE de forma automática e integrada com o sistema de NF
- Geração do CTE de forma manual
- Envio do CTE para o cliente
- Envio do CTE para o transportador
- Envio do CTE para a receita federal
- Envio do CTE para a prefeitura
- Envio do CTE para a SEFAZ
- Não será capaz de gerar o CTE de forma automática e integrada com o sistema de pedido de venda, pois o sistema de pedido de venda não possui integração com o sistema de NF.
- Não será capaz de corrigir erros fiscais reportados pelos orgãos responsáveis, porém será capaz de gerar um novo CTE com as correções necessárias, reportando aos responsáveis pela correção na forma de email.

### Terminologia:
- CTE: Conhecimento de Transporte Eletrônico
- NF: Nota Fiscal
- PDV: Pedido de Venda

### Funcionamento do Sistema atual:
O sistema atual necessita de mão de obra dedicada para a geração do CTE, pois o sistema não gera automaticamente. O sistema atual gera o CTE de forma manual, ou seja, o usuário deve preencher os dados necessários para a geração do CTE, e em seguida enviar o CTE para o cliente, transportador, receita federal, prefeitura e SEFAZ.
? Tem se como requisito, caso a venda seja proveniente de NF, o arquivo XML de NF

### Entradas e Saídas do sistema:
- Entrada: Dados da NF (provenientes do sistema de NF ou informados manualmente)
- Saída: Arquivo XML do CTE (implicitamente enviado aos responsáveis, porém permitindo a visualização/exportação do mesmo)

### Problemas e pontos críticos do sistema atual:
- Mão de obra dedicada para a geração do CTE
- Erros humanos
- Tempo de geração do CTE
- Tempo de envio do CTE para o cliente
- Tempo de envio do CTE para o transportador
- Tempo de envio do CTE para a receita federal
- Tempo de envio do CTE para a prefeitura
- Tempo de envio do CTE para a SEFAZ

### Definição de Requisitos:
- O sistema deve ser capaz de gerar o CTE de forma automática e integrada com o sistema de NF, caso a venda seja gerada por nota fiscal.
- O sistema deve ser capaz de gerar o CTE de forma manual, caso a venda seja gerada por pedido de venda.
- O sistema deve ser capaz de enviar o CTE para o cliente
- O sistema deve ser capaz de enviar o CTE para o transportador
- O sistema deve ser capaz de enviar o CTE para a receita federal
- O sistema deve ser capaz de enviar o CTE para a prefeitura
- O sistema deve ser capaz de enviar o CTE para a SEFAZ
- O sistema deve possibilitar a visualização e exportação do CTE

### Atores:
- Usuário
    - Ator responsável por gerar o CTE de forma manual, caso a venda seja gerada por pedido de venda, ou pela correção de erros reportados pelos orgãos responsáveis.
- Sistema de NF
    - Ator responsável por gerar o CTE de forma automática, caso a venda seja gerada por nota fiscal. (Será outro sistema, portanto não será considerado como ator e seus processos atuais não deverão ser alterados)
- Cliente, Transportador, Receita Federal, Prefeitura, SEFAZ
    - São atores que recebem o CTE, e interagem caso encontrem algum problema no mesmo. O conhecimento necessário deverá ser básico, apenas apontando o problema encontrado e a identificação do CTE, e o sistema deverá ser capaz de alertar os responsáveis internos.# ies100-CTE
