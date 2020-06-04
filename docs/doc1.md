---
id: doc1
title: Introdução
sidebar_label: Introdução
---

O Sistema TGP é um sistema de workflow de aprovação para solicitação de exame de produto usado para controlar o processo de Garantia da Qualidade da TITAN.

O Registro das ocorrências é feito pelas revendedoras de pneus, através do sistema, que é disponibilizado aos clientes previamente cadastrados com perfil loja.

Algumas ações no sistema causam uma integração com o ERP LX (AS400). 

Após o preenchimento do formulário de reclamação, os usuários (TITAN) responsáveis pela análise do produto, com perfil de DAP Técnico, aguardam o recebimento do pneu para que seja feito a respectiva análise. Em alguns casos a análise poderá ser feita através de fotos, anexadas ao processo, que poderão ou não gerar créditos aos clientes. Alguns processos podem vir acompanhados de câmara e protetor que após análise também poderão ser incluídos no valor do crédito. 

A manutenção dos dados será efetuada pelos usuários do DAP Técnico (TITAN) no sistema, atualizando também o sistema LX. 

Os registros das informações também poderão ser feitos através de EDI (Revendas cadastradas), que após consistências são integradas nos sistemas TGP e LX através de um serviço Windows que faz a leitura dos dados do EDI e os grava nos respectivos bancos de dados. 

Com a chegada do pneu a fábrica é realizada a análise técnica, e com o laudo procedente, passa pela conferência de valores do departamento Planejamento Financeiro (TITAN) e após aprovação pelo DAP Faturamento (TITAN), os créditos são gerados em nome dos clientes, que ficam responsáveis pelo ressarcimento ao consumidor final. 

Quando o laudo não é procedente a garantia é rejeitada, e é enviado um e-mail para o DAP Logística (TITAN) providenciar a devolução do pneu. 

## Descrição da estrutura de parâmetros

O sistema possui telas de parametrização, que permitem configurações e cadastros de dados que o próprio sistema utiliza. 

## Descrição da estrutura do Controle de permissão de usuários do Tipo Loja 

As permissões de visualização das telas e status dos usuários são parametrizáveis. Para o tipo de usuários “Loja”, temos os seguintes controles: 

Usuários: onde todos os usuários de lojas deverão ser cadastrados; 

Lojas: onde todas as lojas deverão ser cadastradas. (As lojas são cadastradas no sistema LX, não tendo meio de inclusão ou alteração no TGP); 

Loja Usuário: onde todos os usuários deverão ser atrelados a uma loja; 

Grupo Lojas: onde os grupos deverão ser criados; 

Grupo Loja Item: onde são atreladas as lojas a um grupo de lojas; 

Gestor Grupo Loja: onde um ou mais usuários Loja serão atrelados a um Grupo Loja, para terem acesso a todos os processos de garantia cadastrados por qualquer usuário de qualquer uma das lojas atreladas ao grupo; 

## Descrição da estrutura do Controle de permissão de usuários do Tipo Titan 

As permissões de visualização das telas e status dos usuários são parametrizáveis. Para o tipo de usuários “Titan”, temos os seguintes controles: 

Usuários: onde todos os usuários de Titan deverão ser cadastrados; 

Grupo Usuários: onde os grupos deverão ser criados; 

Grupo Usuário Item: onde são atrelados os usuários a um grupo de usuários; 

Telas Grupo Usuário: onde as telas do sistema são atreladas a um grupo de usuários para que os usuários deste grupo tenham acesso à esta tela, possibilitando escolher em que menu esta tela será listada; 

Permissão Grupo: nesta tela é possível atrelar as funções pré-cadastradas no sistema aos grupos que devem ter acesso a estas funções. 

Permissão Grupo Status: nesta tela é possível atrelar os status pré-cadastrados no sistema aos grupos que devem ter acesso a estes status. 

## Descrição da estrutura do Fluxo de Processos 

O fluxo dos processos no sistema TGP é baseado em diferentes status. Para cada passo que o processo avança no sistema, um status diferente é apontado no processo. Grupos diferentes de usuários tem acesso aos processos que estão em determinados status, previamente cadastrados para seus grupos. 

Fluxo: 

1 – Usuário Loja ou DAP Técnico registram uma reclamação/processo; 

– Se termo de autorização de corte/destruição marcado como “Sim”, usuários do grupo DAP Logística recebem e-mail para tomar ciência de que produto está a caminho, de acordo com texto e assunto cadastrados na tela de “E-mail”; 

– Se ocorrência de vítimas marcada com “Sim”, usuários do grupo DAP Jurídico recebem e-mail para tomar ciência do processo, de acordo com texto e assunto cadastrados na tela de “E-mail”; 

– Usuários do grupo DAP Técnico recebem e-mail para tomar ciência do processo, de acordo com texto e assunto cadastrados na tela de “E-mail”; 

– Após a gravação do processo, o Status é “Análise Técnica”; 

2 – Usuário Loja ou Consumidor envia o produto (pneu) para análise; 

3 – Usuário do grupo DAP Logística recebe produto (pneu) e informa o sistema que foi “Recebido”; 

4 - Usuário do grupo DAP Técnico “Assume Processo” (Isso garante que a análise deste processo será de responsabilidade do usuário que o assumiu. Não impede que outro usuário do mesmo grupo o assuma, mas é necessário que o faça para poder ficar responsável pela análise e assim dar o seu parecer. Estas alterações ficam registradas em um LOG e podem ser visualizadas pelos usuários do Grupo DAP TI); 

5 - Usuário do grupo DAP Técnico realiza a análise técnica e dá seu parecer; 

5.1 – Se parecer aprovado, status é alterado para “Análise Financeira” e usuários do grupo DAP Financeiro recebem e-mail para tomar ciência do processo, de acordo com texto e assunto cadastrados na tela de “E-mail”; 

5.1.1 – No momento da aprovação o programa AS400 TGP017CL é executado para submeter o processo a uma validação, se o produto tem preço cadastrado para o cliente escolhido em questão; 

5.1.2 – Se a validação acima for positiva, o status na TTBAJH é alterado, juntamente com data e usuário da aprovação, então o programa AS400 TGP016CL é executado para calcular os valores e preencher a tabela TTBAJV; 

5.2 – Se parecer rejeitado, status é alterado para “Solicitação Rejeitada”; 

5.3 – Em ambos os casos de aprovação e rejeição, se termo de autorização de corte estiver marcado como “Não”, usuários do grupo DAP Faturamento e DAP Logística recebem e-mail para providenciarem a devolução do produto ao consumidor, de acordo com texto e assunto cadastrados na tela de “E-mail”; 

6 - Usuário do grupo DAP Financeiro realiza a análise financeira e dá seu parecer; 

6.1 – Se parecer aprovado, status é alterado para “Análise Faturamento” e usuários do grupo DAP Faturamento recebem e-mail para tomar ciência do processo, de acordo com texto e assunto cadastrados na tela de “E-mail”; 

6.2 – Se parecer escolhido for “Voltar para Técnico”, status retorna para “Análise Técnica” e usuários do grupo DAP Técnico recebem e-mail para tomar ciência da rejeição do processo pelo financeiro, de acordo com texto e assunto cadastrados na tela de “E-mail”; 

 

6.3 – Além do parecer, o Usuário do DAP Financeiro responsável pelo processo, também tem a opção de recalcular os valores gravados e exibidos na tela de parecer, quando for necessário alterar algo no sistema financeira; 

 

7 - Usuário do grupo DAP Faturamento realiza a análise financeira e dá seu parecer (executa a geração do crédito, ou não); 

7.1 – Se parecer aprovado, status é alterado para “Aprovado Faturamento” e usuários do grupo Gerencial recebem e-mail para tomar ciência do processo e seus valores, de acordo com texto e assunto cadastrados na tela de “E-mail”; 

7.2 – Se parecer escolhido for “Voltar para Financeiro”, status retorna para “Análise Financeira” e usuários do grupo DAP Financeiro recebem e-mail para tomar ciência da rejeição do processo pelo Faturamento, de acordo com texto e assunto cadastrados na tela de “E-mail”; 

8 – Tarefa de Finalização, que é um serviço Windows com possibilidade de configuração de intervalo entre execuções pelos usuários do grupo “TI”, na tela de Configurações, executa e faz a finalização automática de processos com crédito gerados, e status é alterado para “Finalizado”.