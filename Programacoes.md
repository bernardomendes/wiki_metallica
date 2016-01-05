# Programações

> [Página Inicial](Home) > [Telas](Telas)

![programacoes](/screens/programacoes.png)

* [Programação](#Programação)
* [Prensa](#Prensa)
* [Painel de Controle](#Painel de Controle)
* [Cabotagens](#Cabotagens)
* [Cabotagens - Destinatário](#Cabotagens---Destinatário)
* [Editar Meta](#Editar-Meta)

***

* **Detalhes:**
 * O usuário não consegue entrar na tela se não tiver permissão para visualizar a tela específica.

***
## Programação
![programacao](/screens/programacao.png)

**Regras de negócio:**
* S (Solicitado) = Transportes solicitados (Normais + Reprogramados + Antecipados);
* P (Programado) = Soma de indicadores (de acordo com a modalidade) dos transportes programados, é adionado um asterisco se existem transportes justificados no P;
* R (Realizado) = Soma de indicadores (de acordo com a modalidade) dos veículos para os transportes realizados, é adicionado um asterisco se existem transportes justificados no P ou no R;
* C (Confirmado) = Número de BRMs, obtido pela importação;
* Conf. (Confirmados) = Soma das quantidades dos materiais (obtido pela importação de BRM) / 1000;
* Meta Mês = Soma da quantidade de peso do detalhamento da meta (obtido por FOB(t) na importação de meta).

### Programação - Filtros
![programacao_filtros](/screens/programacao_filtros.png)

**Regras de negócio:**
* Por padrão, a _Data Início_ é o dia atual e a _Data Fim_ é o data início avançando 7 dias dentro do mês (cobrindo uma semana no mês);
* _Data Início_ e _Data Fim_ são obrigatórios;
* _Data Início_ e _Data Fim_ devem ser datas do mesmo mês/ano;
* Ao marcar _Exportar para Excel_ e clicar em _Filtrar_ é gerado um arquivo do excel com os dados.

### Programação - Inserir Fornecedor
![programacao_fornecedor](/screens/programacao_fornecedor.png)

**Regras de negócio:**
* _Fornecedor_ e _Destinatário_ são obrigatórios;
* _Prensa_ é opcional;
* Os registro _Fornecedor_ e Destinatário_ são únicos para o mês/ano referente;
* Poderá ser adicionado zero ou mais sucatas ao fornecimento, sendo o nome obigatório;
* Se não preencher o volume de uma sucata, por padrão, será gravado o valor zero;
* Para adicionar sucata a uma meta depois de criada, deve ser realizada na tela de [_Editar Meta_](#Editar-Meta).

### Programação - Incluir Prensa
![programacao_incluir_prensa](/screens/programacao_incluir_prensa.png "Incluir Prensa")

**Regras de negócio:**
* Poderá ser modificado a prensa de uma meta.

### Programação - Solicitar
![programacao_solicitar](/screens/programacao_solicitar.png "Solicitar")
![replicar_atendimento_normal](/screens/replicar_atendimento_normal.png "Replicar Atendimento Normal")

**Regras de negócio:**
* Somente poderá solicitar até no dia anterior da _Data do Solicitado_ às 15hs, exceto para o usuário que é administrador do sistema;
* Pode ser adicionado zero ou mais sucatas;
* Na solicitação, _Tipo de Sucata_ e _Transportes_ são obrigatórios;
* Ao selecionar _Replicar Atend. Normal_, os atendimentos normais são replicados para vários dias após a _Data do Solicitado_ com opções para incluir sabádo e domingo, sendo a _Data Início e Data Fim_ obrigatórios e do mesmo mês/ano da _Data do Solicitado_;
* _Solicitações em atraso_ é a quantidade de solicitações normais (até o dia anterior no mês) - quantidade de realizados (até o dia anterior no mês) - quantidade de solicitações reprogramadas (após o dia posterior no mês), considerando os indicadores de transporte e arrendondando para cima;
* Se o tipo de atendimento for _Reprogramado_, somente poderá solicitar até quantidade em atraso;
* Somente poderá reprogramar se existir a quantidade se solicitações normais para o tipo de sucata.

### Programação - Programar
![programacao_programar](/screens/programacao_programar.png "Programar")
![programacao_programar_rodoviario](/screens/programacao_programar_rodoviario.png "Programar rodoviário")
![programacao_programar_rodoviario2](/screens/programacao_programar_rodoviario2.png "Programar rodoviário")
![programacao_programar_cabotagem](/screens/programacao_programar_cabotagem.png "Programar cabotagem")

**Regras de negócio:**
* Somente poderá programar até o dia da _Data do Programado_ às 15hs, exceto para o usuário que é administrador do sistema;
* Poderá ser adicionado zero ou mais transportes;
* Para o transporte:
  * Se o _Tipo de Transporte_ for _Rodoviário_ e a _Opção_ for _Programar_, _Transportadora Filial_, _Tipo de Veículo_ e _Tipo de Sucata_ são obrigatórios;
  * Se o _Tipo de Transporte_ for _Rodoviário_ e a _Opção_ for _Justificar_, _Justificativa_ é obrigatório;
  * Se o _Tipo de Transporte_ for _Cabotagem_ e a _Opção_ for _Programar_, _Data Agendada_, _Hora Agendada_ , _Transportadora Filial_, _Tipo de Veículo_ e _Tipo de Sucata_ são obrigatórios;
* Ao selecionar _Replicar Rodoviário_ e/ou _Replicar Cabotagem_, os transportes de acordo com o tipo selecionado são replicados para vários dias após a _Data do Solicitado_ com opções para incluir sabádo e domingo, sendo a _Data Início e Data Fim_ obrigatórios e do mesmo mês/ano da _Data do Programado_;
* Ao clicar no link _Replicar_ no transporte, é replicado na tela a quantidade de transportes de acordo com a quantidade digitada, por padrão é "1";
* Se o transporte foi justificado no _Realizado_ não pode ser alterado.


### Programação - Realizar
![programacao_realizar_programados](/screens/programacao_realizar_programados.png)
![programacao_realizar_programados2](/screens/programacao_realizar_programados2.png)
![programacao_realizar_realizados](/screens/programacao_realizar_realizados.png)
![programacao_realizar_justificados](/screens/programacao_realizar_justificados.png)

**Regras de negócio:**
* Somente poderá realizar até o dia da _Data do Programado_ às 13:30hs, exceto para o usuário que é administrador do sistema;
* Na aba _Programados_: 
  * Os transportes programados que não foram realizados aparecerão nessa aba para ser realizado, inserindo a data no _Início Realizado_ com a opção de inserir uma observação, ou justificado inserindo uma _Justificativa_;
  * Poderá ser realizado ou justificado zero ou mais transportes (rodoviários) sem que tenha sido programado no P:
     * Se _Opção_ é _Realizado_, _Transportadora Filial_, _Tipo de Veículo_, _Tipo de Sucata_ e _Início Realizado_ são obrigatórios;
     * Se _Opção_ é _Justificado_, _Justificativa_ é obrigatório.
* Na aba _Realizados_: 
  * Exibe os transportes realizados;
  * Pode ser removido um realizado, caso seja do tipo rodoviário.
* Na aba _Justificados_:
  * Exibe as justificativas (do P e R) contabilizadas e não contabilizadas no atendimento;
  * Pode ser removido um justificado, caso tenha sido justificado no R.
  * Ao realizar distribui as justificativas da seguinte forma:
     * Máximo de justificativas contabilizadas = Quantidade de transportes solicitados (normais + reprogramados) - quantidade de transportes realizados;
     * Se as justificativas passarem o máximo de justificativas contabilizadas, são transformadas em justificativas não contabilizadas (sendo transformadas primeiro as de logística).

***
## Prensa
![prensa](/screens/prensa.png "Prensa")

**Regras de negócio:**
* Exibe somente as metas que tem prensa.

### Prensa - Filtros
![prensa_filtros](/screens/prensa_filtros.png "Filtros da Prensa")

**Regras de negócio:**
* Por padrão, a _Data Início_ é o dia atual e a _Data Fim_ é o data início avançando 7 dias dentro do mês (cobrindo uma semana no mês);
* _Data Início_ e _Data Fim_ são obrigatórios;
* _Data Início_ e _Data Fim_ devem ser datas do mesmo mês/ano;
* Ao marcar _Exportar para Excel_ e clicar em _Filtrar_ é gerado um arquivo do excel com os dados.

### Prensa - Inserir fornecedor
![prensa_fornecedor](/screens/prensa_fornecedor.png "Inserir Fornecedor")

**Regras de negócio:**
* _Fornecedor_, _Destinatário_ e _Prensa_ são obrigatórios;
* Os registro _Fornecedor_ e Destinatário_ são únicos para o mês/ano referente;
* Se existir uma meta sem prensa com fornecedor e destinatário informado para o mês/ano referente, apenas é adicionado a prensa no mesmo.

### Prensa - Solicitar
![prensa_solicitar](/screens/prensa_solicitar.png "Solicitar")

**Regras de negócio:**
  * Idem [Programação - Solicitar](#Programação---Solicitar).

### Prensa - Programar
![prensa_programar](/screens/prensa_programar.png "Programar")

**Regras de negócio:**
  * Idem [Programação - Programar](#Programação---Programar);
  * Não programa cabotagem.

### Prensa - Realizar
![prensa_realizar](/screens/prensa_realizar.png "Realizar")

**Regras de negócio:**
  * Idem [Programação - Realizar](#Programação---Realizar).

***
## Painel de Controle
![painel_de_controle](/screens/painel_de_controle.png)

**Regras de negócio:**
* Conf. = Soma das quantidades dos materiais (obtido pela importação de BRM) / 1000 (para o mês);
* Meta Mês = Soma da quantidade de peso do detalhamento da meta (obtido por FOB(t) na importação de meta).
* S = Solicitações normais (normal e prensado) + solicitações antecipadas (normal e prensado);
* P = Soma do valor dos indicadores de transportes programados (normal e prensado);
* R = Soma do valor dos indicadores de transportes realizados (normal e prensado);
* Just. Log. = Soma das justificativas do tipo logística (normal e prensado);
* Just. Log. = Soma das justificativas do tipo metálico (normal e prensado);
* C = Soma das quantidades dos materiais (obtido pela importação de BRM) / 1000;

### Filtros
![painel_de_controle_filtros](/screens/painel_de_controle_filtros.png "Filtros do Painel de Controle")

**Regras de negócio:**
* Por padrão, a _Data Início_ é o primeiro dia do mês atual e a _Data Fim_ é o último dia do mês atual;
* _Data Início_ e _Data Fim_ são obrigatórios;
* _Data Início_ e _Data Fim_ devem ser datas do mesmo mês/ano;
* Ao marcar _Exportar para Excel_ e clicar em _Filtrar_ é gerado um arquivo do excel com os dados.

### Incluir Prensa
![painel_de_controle_incluir_prensa](/screens/painel_de_controle_incluir_prensa.png)

**Regras de negócio:**
* Poderá ser modificado a prensa de uma meta.

***
## Cabotagens
![cabotagens](/screens/cabotagens.png)

**Regras de negócio:**
* Realizado quando Data de Chegada é preenchido e a cabotagem está ativa;
* Tempo de permanência = data de retirada - data de chegada;
* Data de Solicitação é resgatado da tela de Programação ao programar Cabotagem;
* A diária é resgatada do _Cadastro de Proposta_.

### Cabotagens - Filtros
![cabotagens_filtros](/screens/cabotagens_filtros.png)

**Regras de negócio:**
* Por padrão, _Tem BRM?_ é _Não_.

***
## Cabotagens - Destinatário
![cabotagens_destinatario](/screens/cabotagens_destinatario.png)

**Regras de negócio:**
* Saldo Transportadora = Data Saída Transportadora - Data Chegada Transportadora.

### Cabotagens - Destinatário - Filtros
**Regras de negócio:**
* Idem [Cabotagens - Filtros](#Cabotagens---Filtros).

***
## Editar Meta
![editar_meta](/screens/editar_meta.png)

**Regras de negócio:**
* Busca uma meta específica, edita e exclui.