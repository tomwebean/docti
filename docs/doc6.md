---
id: doc6
title: Tarefas
sidebar_label: Tarefas
---

## Logs 

Nesta tela é possível consultar todas as alterações de dados que ocorreram no sistema, e também quem foram os responsáveis por elas. Observe que temos vários filtros para ajudar na busca das informações desejadas. 

<img src="https://github.com/tomwebean/documentacao/blob/master/.png?raw=true">


## Nova Solicitação 

Nesta tela as lojas, gestores e usuários DAP Técnico irão cadastrar os processos de garantia. 

Os campos com <span style="color:red">*</span> são de preenchimento obrigatório. 

O campo série deve ter no mínimo 6 caracteres, onde os 4 últimos dígitos serão a semana e o ano de fabricação. Ex.: MXPH2JY3<span style="color:blue">25</span><span style="color:red">16</span> (<span style="color:blue">semana</span>–<span style="color:red">ano</span>) 

Fotos e documentos podem ser anexados ao processo de garantia. 

Você encontrará também o ícone de uma lupa à frente de alguns campos. Ao clicar nele abrirá uma janela popup na qual será possível pesquisar e escolher a informação desejada para o campo. 

<img src="https://github.com/tomwebean/documentacao/blob/master/.png?raw=true">

O campo referente à loja tem comportamento diferente de acordo com o usuário logado: 

Loja: Preenchido automaticamente com o nome da loja. 

<img src="https://github.com/tomwebean/documentacao/blob/master/.png?raw=true">

Gestor: Lista com as lojas cadastradas nos grupos do gestor, necessário escolher. 

<img src="https://github.com/tomwebean/documentacao/blob/master/.png?raw=true">

DAP Técnico: Ícone de lupa onde o usuário deverá pesquisar entre todas as lojas. 

<img src="https://github.com/tomwebean/documentacao/blob/master/.png?raw=true">

Os campos referentes à “Análise Titan” e “Caso Especial” estarão disponíveis apenas para DAP Técnico. 

<img src="https://github.com/tomwebean/documentacao/blob/master/.png?raw=true">

Após o preenchimento das informações, pressione o botão “Salvar” para registrar o processo de garantia. 

 
## Visualizar ou alterar processo 

Quando necessário os usuários poderão visualizar ou alterar as informações do processo, de acordo com suas permissões e fluxo, o acessando através das telas “Caixa de Entrada” ou “Consulta Processos”. 


## Formulário 

Ao abrir o processo de garantia para visualizar ou alterar o mesmo, estará disponível para todos os usuários no canto superior direito o ícone de um PDF. Clicando no mesmo o sistema abrirá uma nova aba ou janela – de acordo com a configuração do browser – exibindo o formulário para impressão, permitindo inclusive salvar como arquivo. 

<img src="https://github.com/tomwebean/documentacao/blob/master/grupolojaitem.png?raw=true">


## Anexos 

Ao clicar no link “Anexos” você será redirecionado para a tela a seguir. Apenas informe a descrição, escolha o arquivo e pressione o botão “Anexar” para vincular ao processo. 

Caso anexe um arquivo errado, é possível excluí-lo nesta mesma tela no grid que aparecerá em seguida. 

<img src="https://github.com/tomwebean/documentacao/blob/master/usuarios.png?raw=true">


## Caixa de Entrada 

Nesta tela é possível consultar todos os processos de garantia cadastrados no sistema, podemos observar as opções de filtro para ajudar na consulta. 

<img src="https://github.com/tomwebean/documentacao/blob/master/grupousuarios.png?raw=true">

Os processos estarão visíveis de acordo com o usuário logado: 

**Loja:** Vinculados à loja. 

**Gestor:** Vinculados às lojas cadastradas nos grupos do gestor. 

**DAPs:** De acordo com a configuração de permissões definidas pelo usuário de TI. Para os grupos DAP Jurídico e Logístico, temos um caso especial: 

* **DAP Jurídico:** Quando tiver vítima e ainda sem parecer do grupo. 

* **DAP Logístico:** Quando autoriza corte e ainda sem parecer do grupo. 

Para visualizar mais dados do processo de garantia, apenas dê duplo clique no registro desejado do grid e você será redirecionado para a mesma tela de nova solicitação com todos os campos preenchidos. 

Temos nesta tela ainda a possibilidade de assumir ou cancelar os processos de garantia. Os botões estarão disponíveis de acordo com as permissões também configuradas pelo usuário de TI. 

Observe no lado esquerdo um menu lateral de opções onde estarão exibidos os grupos de lojas, sendo mais um filtro dos processos de garantia. São visíveis de acordo com o usuário logado, sendo o primeiro item “inbox” disponível para todos. 


## Assumir 

Antes de efetuar qualquer operação no processo de garantia, é obrigatório assumir o mesmo. Para isso há 2 maneiras: 

**Caixa de Entrada:** Selecione os processos desejados no grid e clique no botão “Assumir Processos”. O sistema assumirá os processos permitidos para o usuário de acordo com o fluxo e mostrará abaixo as mensagens de retorno informando a situação de cada processo. 

<img src="https://github.com/tomwebean/documentacao/blob/master/grupousuarioitem.png?raw=true">

<img src="https://github.com/tomwebean/documentacao/blob/master/grupousuarioitem.png?raw=true">

**Tela de Processo:** Abra a tela de consulta do processo desejado e clique no botão “Assumir Processo” que se encontra no final da tela. 

<img src="https://github.com/tomwebean/documentacao/blob/master/grupousuarioitem.png?raw=true">

Após assumir o processo de garantia, o usuário terá a possibilidade de dar o seu parecer de acordo com o fluxo atual. O usuário DAP Técnico poderá ainda alterar os campos se necessário também de acordo com o fluxo. 


## Cancelar 

Caso necessário é possível cancelar o processo de garantia, impossibilitando os mesmos de continuar o fluxo. Para isso selecione os processos desejados no grid e clique no botão “Cancelar”. O sistema irá alterar o status dos processos permitidos e mostrará abaixo as mensagens de retorno informando a situação de cada processo. 

<img src="https://github.com/tomwebean/documentacao/blob/master/gestorgrupoloja.png?raw=true">

<img src="https://github.com/tomwebean/documentacao/blob/master/gestorgrupoloja.png?raw=true">


## Parecer 

Nesta tela os usuários DAPs devem dar o seu parecer no processo de garantia, acessada através do botão “Avançar” que se encontra ao final da tela do processo após o mesmo ser assumido.  

<img src="https://github.com/tomwebean/documentacao/blob/master/lojausuarios.png?raw=true">

O usuário responsável pelo fluxo atual deverá informar o seu parecer e outros dados se necessário de acordo com o seu grupo, permitindo assim que o fluxo continue, volte para o status anterior ou seja rejeitado. 

Para os usuários DAP Técnico e Financeiro, será possível também excluir o seu parecer caso tenham cometido algum erro e o DAP seguinte do fluxo não tenha assumido o processo ainda, conforme pode ver na imagem abaixo: 

<img src="https://github.com/tomwebean/documentacao/blob/master/lojausuarios.png?raw=true">


## Valores de crédito 

Após a aprovação do DAP Técnico, o sistema irá gerar os valores de crédito para o processo de garantia, que estarão visíveis nesta tela em forma de grid para os grupos do fluxo seguinte.  

<img src="https://github.com/tomwebean/documentacao/blob/master/permissoagrupostatus.png?raw=true">

Somente o usuário DAP Financeiro tem a possibilidade de recalcular esses valores gerados pelo sistema quando for necessário através do botão “Recalcular” disponível. 


## Consulta de Processos

Nesta tela os usuários DAPs poderão gerar relatórios no formato “xlsx” – visualizado no Excel ou programa similar – ou consultar todos os processos de garantia que estão cadastrados no sistema, independentemente dos status e permissões de visualização. Observe os diversos filtros disponíveis para que sua consulta seja mais objetiva e precisa de acordo com a necessidade. 

<img src="https://github.com/tomwebean/documentacao/blob/master/permissoagrupostatus.png?raw=true">

Os seguintes filtros têm como funcionalidade apenas exibir mais informações no relatório: “Parecer?”, “Anexo?” e “Caso Especial?”. 

Se a consulta for realizada na própria tela através do botão “Filtrar”, é possível ainda ver mais detalhes do processo dando duplo clique em sua linha de registro, assim será aberto a tela com todas as informações do mesmo modo que é feito na tela “Caixa de Entrada”, porém dessa vez apenas para visualização. 

<img src="https://github.com/tomwebean/documentacao/blob/master/permissoagrupostatus.png?raw=true">


## Serviço Windows 

Além do sistema Web, existe um serviço Windows responsável pela inclusão dos processos de garantia via EDI e também pela finalização dos mesmos quando estiverem com o fluxo concluído. 

<img src="https://github.com/tomwebean/documentacao/blob/master/permissoagrupostatus.png?raw=true">


Esta rotina executa a cada X minutos que são configurados na tela de parâmetros do sistema através do campo “Intervalo de minutos do serviço”. 