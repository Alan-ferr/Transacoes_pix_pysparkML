# Transacoes_pix_pysparkML

## Case Final
Análise de Transações PIX
CRISP-DM - https://www.escoladnc.com.br/blog/data-science/metodologia-crisp-dm/

## Objetivos
Limpar e pré-processar os dados das transações PIX
Analisar padrões de uso do PIX, tais como os canais mais utilizados e os valores de transação mais comuns
Use o PySpark MLlib para treinar e avaliar um modelo de detecção de fraude
Avaliar o desempenho do modelo e fazer recomendações para melhorias futuras
## Dados
O conjunto de dados inclui as seguintes informações para cada transação:

Detalhes da transação: valor, tempo, remetente e receptor CPF/CNPJ, tipo
Etiqueta de fraude: uma variável binária que indica se a transação foi fraudulenta (1) ou não (0)
## Tarefas
Normalização dos dados:
O dataset que você lerá está em formato json.
{
  "id_transacao": inteiro,
  "valor": texto,
  "remetente": {
      "nome": texto,
      "banco": texto,
      "tipo": texto
  }, 
  "destinatario": {
      "nome": texto, 
      "banco":texto,
      "tipo": texto
  },          
  "categoria":texto,
  "chave_pix":texto,
  "transaction_date":texto,
  "fraude":inteiro,
}
Faça sua transformação para formato colunar
Análise Exploratória de Dados: Use o PySpark para analisar padrões de uso do PIX:
chaves pix mais usadas;
os valores de transação mais comuns;
distribuição dos valores de transação por hora e dia;
quais bancos receberam mais transferências por dia;
para qual tipo de pessoa (PF ou PJ) foram realizadas mais transações
Engenharia de Recursos: Apresentar novas características que podem ser úteis para a detecção de fraudes, tais como o número de transações feitas pelo mesmo remetente em um período de tempo específico.
## Modelagem: Use o PySpark MLlib para treinar e detectar possíveis transações que contenham fraude.
## Observação
É importante notar que este é um caso simplificado, e em cenários do mundo real você teria que lidar com dados mais complexos, usar técnicas mais avançadas como métodos de conjuntos e considerar o conhecimento de domínio, bem como leis e regulamentos das instituições financeiras no Brasil.

## Entendimento do Negócio
Você trabalha em um banco e o principal meio de pagamento utilizado no seu banco é o Pix.

Através da base de transações do pix o banco deseja entender qual é o perfil dos clientes que utilizam o pix, além de verificar possíveis transações que tenham fraude. Porém, eles tem um cliente específico que tem um relacionamento muito bom para o banco, por isso, você recebeu a base de transações de cliente dos últimos 2 anos e precisa a partir dela criar um relatório contendo as principais características das transações.

Então, resumindo, temos dois principais objetivos para esse case:

Obter valor a partir dos dados
Para qual banco esse cliente mais transfere?
Qual é a média de transferências por período que esse cliente faz?
Baseando-se no valor das transferências, poderia dar um aumento de crédito?
Para o que esse cliente mais usa as transferências?
Executar um algoritmo de machine learning que identifique possíveis transações com fraude.
Pós Processamento
Defina ao mínimo cinco métricas de qualidade para seus dados
Explique se os seus dados estão com uma boa qualidade
