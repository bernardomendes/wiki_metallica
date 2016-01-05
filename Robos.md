# Robôs
> [Página Inicial](Home)

***
## Enviar e-mail de planejamento
**Funcionamento:** Envia programação do dia para os usuários que estão vinculados às transportadoras filiais.

**Executa em:** De segunda a sexta às 8, 10, 12 14, 16, 18 e 20 horas.

***
## Justificar não programados
**Funcionamento:**
* Verifica as solicitações normais e prensadas do dia;
* n = (transportes solicitados - transportes programados - transportes justificados);
* Se n for menor que zero, n será zero;
* Arredonda n para cima;
* Cria n vezes a justifiva _Logística não enviou caminhão_.

**Executa em:** Todos os dias às 17 horas.

***
## Verificar antecipados
**Funcionamento:**
* O dia considerado é o dia anterior (segunda a sexta) do dia atual.
* Se o dia considerado é o primeiro dia do mês, transforma todos as sucatas antecipadas do dia em sucatas normais e finaliza;
* O primeiro dia a se verificar é dois dias anteriores (somente segunda a sexta) do dia considerado;
* O último dia a se verificar é o dia anterior do dia considerado;
* _n_dias_: primeiro dia até o último dia a verificar;
* As solicitações a serem verificadas devem ter sucatas antecipadas no dia considerado;
* Para cada solicitação:
  * n_solicitacoes: sucatas das solicitações de n_dias, da mesma meta e do mesmo tipo (normal, prensado ou prensa);
  * n_realizados = Soma de indicadores de veículo (arrendondado a soma para cima) das solicitações de n_dias, da mesma meta e do mesmo tipo (normal, prensado ou prensa);
  * Se n_solicitacoes é menor ou igual a n_realizados, transforma todas as sucatas antecipadas da solicitação em sucatas normais;
  * Se n_realizados é maior que n_solicitacoes e o número de sucatas antecipadas da solicitação seja maior que (n_realizados - n_solicitações), transforma (n_realizados - n_solicitações) sucatas antecipadas em sucatas normais.

**Executa em:** Todos os dias às 14 horas.

***
## E-mail follow-up diário
**Funcionamento:**
* Lista de todos os transportes programados para o dia atual e agrupa pela observação do follow-up;
* Envia os dados consolidados para os seguintes perfis: "Logística Avançada", "Central Abastecimento", "Comprador (Gerência Metálicos)", "Gerência Metálicos", "Programador Metálicos"

**Executa em:** Todos os dias às 12 horas.

***
## Verificar justificativas aprovadas por data
**Funcionamento:**
* Lista todas as justificativas que não foram aprovadas/negadas e aprova automaticamente;
* No caso de alteração do destino da carga ou carregamento antecipado, cria novas solicitações

**Executa em:** Todos os dias às 0 horas.

***
## Enviar relatório dos compradores
**Funcionamento:**
* Envia o relatório de compradores para todos os compradores

**Executa em:** De segunda a sexta às 14 e 19 horas.

***
## Verificar antecipados (minério)
**Funcionamento:**
* Nega automaticamente todas as solicitações antecipadas com data inferior ou igual ao próximo dia útil

**Executa em:** Todos os dias às 18 horas.

## Verificar reprogramados (minério)
**Funcionamento:**
* Nega automaticamente todas as solicitações reprogramadas com data inferior ou igual ao próximo dia útil

**Executa em:** Todos os dias às 18 horas.

## Alerta para transportadora e usina (minério)
**Funcionamento:**
* Nega automaticamente todas as solicitações antecipadas com data inferior ao próximo dia útil

**Executa em:** De segunda a sexta às 14 e 19 horas.