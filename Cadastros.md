> [Página Inicial](Home) > [Telas](Telas)

![cadastros](/screens/cadastros.png)

* [Locais](#Locais)
* [Sistema](#Sistema)
* [Cabotagem](#Cabotagem)
* [Transportadoras](#Transportadoras)
* [Perfis](#Perfis)
* [Usuários](#Usuários)

***

* **Detalhes:**
 * O usuário não consegue entrar na tela se não tiver permissão para visualizar a tela específica; 
 * O usuário não visualiza o botão _Nova/Novo_ se não tiver permissão para criar gerência;
 * Exibe _Mostrar_ no lugar de _Editar_ se o usuário tiver permissão para visualizar a edição mas não editar;
 * Não exibe o _Editar / Mostrar_ se o usuário não tiver permissão para visualizar a edição e não tiver permissão para editar;
 * Não exibe _Apagar_ se o usuário não tiver permissão para excluir a gerência;
 * Não exibe _Log_ se o usuário não tiver permissão para visualizar log do sistema.



***
## Locais
![locais](/screens/locais.png)

* [Gerências](#Gerências)
* [Fornecedores](#Fornecedores)
* [Destinatários](#Fornecedores)

***
### Gerências

![gerencias](/screens/gerencias.png)

* **Detalhes:**
 * O filtro busca nome, sigla, sap ou responsável;
 * Não permitir a exclusão se estiver vinculado a fornecedores.

#### Nova Gerência / Editar Gerência
![nova_gerencia](/screens/nova_gerencia.png "Nova Gerência")
![editar_gerencia](/screens/editar_gerencia.png "Editar Gerência")

* **Detalhes:**
 * Nome, Sigla, SAP, UFs e Responsável são obrigatórios;
 * Nome é um registro único;
 * Sigla é um registro único;
 * SAP é um registro único.

***
### Fornecedores

![fornecedores](/screens/fornecedores.png)

* **Detalhes:**
 * O filtro busca razão social, SAP, município, UF, apelido, CNPJ, gerência ou tipo;
 * Não permitir a exclusão se estiver vinculado a metas.

#### Novo Fornecedor / Editar Fornecedor
![novo_fornecedor](/screens/novo_fornecedor.png "Novo Fornecedor")
![editar_fornecedor](/screens/editar_fornecedor.png "Editar Fornecedor")

* **Detalhes:**
 * Ativo não é exibido na tela de _Novo Fornecedor_, ao criar um fornecedor, por padrão, fica ativo;
 * Replicar R no S significa que deve replicar o R (Realizado) no S (Solicitado) caso crie um R (Realizado);
 * Razão Social, SAP, Munícípio e Apelido são obrigatórios;
 * SAP é um registro único.

***
### Destinatários
![destinatarios](/screens/destinatarios.png)

* **Detalhes:**
 * O filtro busca nome, município, UF, SAP, centro, CNPJ, local ou tipo;
 * Não permitir a exclusão se estiver vinculado a metas;
 * Não permitir a exclusão se estiver vinculado a usuários.

#### Novo Destinatário / Editar Destinatário
![novo_destinatario](/screens/novo_destinatario.png "Novo Destinatário")
![editar_destinatario](/screens/editar_destinatario.png "Editar Destinatário")

* **Detalhes:**
 * Nome, Tipo, Município e SAP são obrigatórios;
 * SAP é um registro único.

***
## Sistema
![sistema](/screens/sistema.png)

* [Prensas](#Prensas)
* [Justificativas](#Justificativas)
* [Indicadores de Veículo](#Indicadores de Veículo)
* [Veículos](#Veículos)
* [UFs](#UFs)
* [Regiões Geográficas](#Regiões Geográficas)
* [Mesorregiões](#Mesorregiões)
* [Municípios](#Municípios)

***
### Prensas
![prensas](/screens/prensas.png)

* **Detalhes:**
 * O filtro busca nome;
  * Não permitir a exclusão se estiver vinculado a metas.

#### Nova Prensa / Editar Prensa
![nova_prensa](/screens/nova_prensa.png "Nova Prensa")
![editar_prensa](/screens/editar_prensa.png "Editar Prensa")

* **Detalhes:**
  * Nome é obrigatório;
  * Nome é um registro único;
  * Nome deve ser um número de 2 algarismos + " - " + palavra, ex.: "01 - Porcina".

***
### Justificativas
![justificativas](/screens/justificativas.png)

* **Detalhes:**
 * O filtro busca nome, responsabilidade ou ativo;
 * Não permitir a exclusão se estiver vinculado a transportes.

#### Nova Justificativa / Editar Justificativa
![nova_justificativa](/screens/nova_justificativa.png "Nova Justificativa")
![editar_justificativa](/screens/editar_justificativa.png "Editar Justificativa")

* **Detalhes:**
  * Ativo não é exibido na tela de _Nova Justificativa_, ao criar uma justificativa, por padrão, fica ativo;
  * Motivo é obrigatório;
  * Motivo é um registro único.

***
### Indicadores de Veículo
![indicadores_de_veiculo](/screens/indicadores_de_veiculo.png)

* **Detalhes:**
  * O filtro busca nome ou valor;
  * Não permitir a exclusão se estiver vinculado a veículos.

#### Novo Indicador de Veículo / Editar Indicador de Veículo
![novo_indicador_veiculo](/screens/novo_indicador_veiculo.png "Novo Indicador de Veículo")
![editar_indicador_veiculo](/screens/editar_indicador_veiculo.png "Editar Indicador de Veículo")

* **Detalhes:**
  * Nome e Valor são obrigatórios;
  * Nome é um registro único.

***
### Veículos
![veiculos](/screens/veiculos.png)

* **Detalhes:**
  * O filtro busca nome, peso, SAP ou indicador de veículo;
  * Não permitir a exclusão se estiver vinculado a transportes.

#### Novo Veículo / Editar Veículo
![novo_veiculo](/screens/novo_veiculo.png "Novo Veículo")
![editar_veiculo](/screens/editar_veiculo.png "Editar Veículo")

* **Detalhes:**
  * Nome, Peso e SAP são obrigatórios;
  * SAP é um registro único;
  * Peso é um número inteiro.

***
### UFs
![ufs](/screens/ufs.png)

* **Detalhes:**
 * O filtro busca nome, sigla, IBGE, região geográfica, responsável logística ou responsável apoio;
 * Não é possível _Criar_ ou _Excluir_ uma UF.

#### Editar UF
![editar_uf](/screens/editar_uf.png "Editar UF")

* **Detalhes:**
  * Os únicos atributos editáveis são _Responsável Logística_ e _Responsável Apoio_.

***
### Regiões Geográficas
![regioes_geograficas](/screens/regioes_geograficas.png)

* **Detalhes:**
 * O filtro busca nome.
 * Somente é possível mostrar os dados da Região Geográfica.

#### Mostrar Região Geográfica
![mostrar_regiao_geografica](/screens/mostrar_regiao_geografica.png "Mostrar Região Geográfica")

***
### Mesorregiões
![mesorregioes](/screens/mesorregioes.png)

* **Detalhes:**
 * O filtro busca nome.
 * Somente é possível mostrar os dados da messoregião.

#### Mostrar Região Mesorregião
![mostrar_mesorregiao](/screens/mostrar_mesorregiao.png "Mostrar Região Mesorregião")

***
### Municípios
![mesorregioes](/screens/municipios.png)

* **Detalhes:**
 * O filtro busca nome, IBGE, latitude, longitude, UF, messoregião ou região geográfica.
 * Somente é possível mostrar os dados do município.

#### Mostrar Município
![mostrar_municipio](/screens/mostrar_municipio.png "Mostrar Município")

***
## Cabotagem
![cabotagem](/screens/cabotagem.png)

* [Modalidades de Transporte](#Modalidades de Transporte)
* [Portos](#Portos)
* [Tipos de Contêiner](#Tipos de Contêiner)
* [Cadastro de Propostas](#Cadastro de Propostas)

***
### Modalidades de Transporte
![modalidades_de_transporte](/screens/modalidades_de_transporte.png)

* **Detalhes:**
  * O filtro busca nome ou descrição;
  * Não permitir a exclusão se estiver vinculado a propostas;
  * Não permitir a exclusão se estiver vinculado a cabotagens.

#### Nova Modalidade de Transporte / Editar Modalidade de Transporte
![nova_modalidade_transporte](/screens/nova_modalidade_transporte.png "Nova Modalidade de Transporte")
![editar_modalidade_transporte](/screens/editar_modalidade_transporte.png "Editar Modalidade de Transporte")

* **Detalhes:**
  * Nome é obrigatório;
  * Nome é um registro único.

***
### Portos
![portos](/screens/portos.png)

* **Detalhes:**
  * O filtro busca nome ou UF ou município;
  * Não permitir a exclusão se estiver vinculado a propostas como porto de origem;
  * Não permitir a exclusão se estiver vinculado a propostas como porto de destino;
  * Não permitir a exclusão se estiver vinculado a cabotagens como porto de origem;
  * Não permitir a exclusão se estiver vinculado a cabotagens como porto de destino.

#### Novo Porto / Editar Porto
![novo_porto](/screens/novo_porto.png "Novo Porto")
![editar_porto](/screens/editar_porto.png "Editar Porto")

* **Detalhes:**
  * Nome é obrigatório;
  * Nome é um registro único.

***
### Tipos de Contêiner
![tipos_de_conteiner](/screens/tipos_de_conteiner.png)

* **Detalhes:**
  * O filtro busca por todos os atributos exibidos na tela;
  * Não permitir a exclusão se estiver vinculado a propostas;
  * Não permitir a exclusão se estiver vinculado a cabotagens.

#### Novo Tipo de Contêiner / Editar Tipo de Contêiner
![novo_tipo_container](/screens/novo_tipo_container.png "Novo Tipo de Contêiner")
![editar_tipo_container](/screens/editar_tipo_container.png "Editar Tipo de Contêiner")

* **Detalhes:**
  * Todos os atributos são obrigatórios;
  * Nome é um registro único.

***
### Cadastro de Propostas
![cadastro_de_propostas](/screens/cadastro_de_propostas.png)
![cadastro_de_propostas2](/screens/cadastro_de_propostas2.png)

* **Detalhes:**
  * O filtro busca por todos os atributos exibidos na tela;

#### Novo Cadastro de Proposta / Editar Cadastro de Proposta
![novo_cadastro_proposta](/screens/novo_cadastro_proposta.png "Novo Cadastro de Proposta")
![editar_cadastro_proposta](/screens/editar_cadastro_proposta.png "Editar Cadastro de Proposta")

* **Detalhes:**
  * Todos os atributos são obrigatórios;
  * O registro com Modalidade de Transporte, Tipo de Contêiner, Transportadora Filial, Porto (em Porto de Origem) e Porto (em Porto de Destino) é único. 

***
## Transportadoras
![transportadoras](/screens/transportadoras.png)

* **Detalhes:**
  * O filtro busca nome, apelido ou ativo;
  * Não permitir a exclusão se estiver vinculado a usuários;
  * Não permitir a exclusão da filial se estiver vinculado a transportes;
  * Não permitir a exclusão da filial se estiver vinculado a propostas;
  * Não permitir a exclusão da filial se estiver vinculado a usuários.

#### Nova Transportadora / Editar Transportadora
![nova_transportadora](/screens/nova_transportadora.png "Nova Transportadora")
![editar_transportadora](/screens/editar_transportadora.png "Editar Transportadora")
![editar_transportadora2](/screens/editar_transportadora2.png "Editar Transportadora")

* **Detalhes:**
  * Ativo não é exibido na tela de _Nova Transportadora_, ao criar uma transportadora, por padrão, fica ativo;
  * Razão Social e Apelido são obrigatórios;
  * Razão Social é um registro único;
  * Apelido é um registro único;
  * Nome, SAP e Município das filiais são obrigatórios;
  * SAP das filiais são registros únicos.

***
## Perfis
![perfis](/screens/perfis.png)

* **Detalhes:**
  * O filtro busca nome;
  * Não permitir a exclusão se estiver vinculado a usuários.

#### Novo Perfil / Editar Perfil
![novo_perfil](/screens/novo_perfil.png "Novo Perfil")
![editar_perfil](/screens/editar_perfil.png "Editar Perfil")

* **Detalhes:**
  * Nome é obrigatório;
  * Nome é um registro único.

***
## Usuários
![usuarios](/screens/usuarios.png)

* **Detalhes:**
  * O filtro busca nome, e-mail, telefone, perfil, SAP, transportadora ou logins;
  * Não permitir a exclusão se estiver vinculado a metas;
  * Não permitir a exclusão se estiver vinculado a solicitações;
  * Não permitir a exclusão se estiver vinculado a transportes;
  * Não permitir a exclusão se estiver vinculado a históricos;
  * Não permitir a exclusão se for responsável logística em UF;
  * Não permitir a exclusão se for responsável apoio em UF;
  * Não permitir a exclusão se for comprador em metas.

#### Novo Usuário / Editar Usuário
![novo_usuario](/screens/novo_usuario.png "Novo Usuário")
![editar_usuario](/screens/editar_usuario.png "Editar Usuário")

* **Detalhes:**
  * Ativo não é exibido na tela de _Novo Usuário_, ao criar um usuário, por padrão, fica ativo;
  * É exibido permissões personalizadas para o usuário;
  * Nome, E-mail e Nome são obrigatório;
  * E-mail é um registro único;
  * Deve ser verificado se é um e-mail válido;
  * Se o perfil têm gerências, o campo Gerências é obrigatório;
  * Se o perfil têm destinatários, o campo Destinatários é obrigatório;
  * Se o perfil é transportadora, o campo Transportadora é obrigatório.
