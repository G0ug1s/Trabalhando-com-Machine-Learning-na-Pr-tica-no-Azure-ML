# Trabalhando com Machine Learning na Prática no Azure ML

# Criando um Modelo de Previsão

acessando o a pagina do Azure "https://ml.azure.com" no diretoria padrão devemos criar um novo Workspace, e neste Workspace vamos criar um modelo de previsão.
Vamos para a aba "ML Automatizado" clicamos em "Novo trabalho de ML automatizado".

Na primeira etapa de "Configurações basicas"  editamos o nome do trabalho e novo nome do experimento, conforme o trabalho que iremo criar. Também pode preencher a descrição para detalhar melhor. No meu caso vou usar o exmplo do curso que se trata de uma previsão de aluguél de bicicletas, então temos o seguinte:

- Nome do trabalho: mslearn_bike_automl
- Novo nome do experimento: mslearn_bike_rental
- Descrição: Aprendizado de máquina automatizado para previsão de aluguél e bicicletas

Clicamos em avaçar.
Na segunda etapa de "Tipo de tarefa e dados", vamos selecionar o tipo de tarefa conforme o objetivo dado, que pode ser uma previção, uma identidicação de rótulo, etc..
No meu caso, no tipo da tarefa vou colocar "Regressão".

Abaixo vamos selecionar o conjunto de dados clicando em "Criar". Preencha com nome, descrição (opcional) e o tipo (no meu caso é Tabular). Em fonte de dados, selecionei "De arquivos da WEB", que é de onde vou pegar os dados que vou trabalhar, e clicamos em avançar. Em seguida inserimos a URL e avançar. Em configurações, em "Cabeçalhos de coluna" vou alterar para "Somente o primeiro arquivo tem cabeçalhos" clicamos em avançar e na parte de esquema não será necessário alterações, avançar também. E na parte de "Examinar" você vai apenas conferir se os dados inseridos estão corretos e clicar em avançar.

Agora vamos aguardar e atualizar, e depois de inseridos selecionamos os dados e clicamos em avançar. Nesta parte de "Configuração de Tarefas", vamos alterar o seguinte:

- Coluna de destino: Rentals (Integer)
- Exibir definições de configuração adicionais: Alteramos Métrica primária para "NormalizerRootMeanSquaredError", desmarcamos as 3 caixinhas e em modelos permitidos selecionamos "RandomForest" e "LightGBM", clica em salvar.
- Limites:
  - Máximo de avaliações: 3
  - Máximo de avaliações simultâneas: 3
  - Máximo de nós: 3
  - Limite de pontuação da métrica: 0,085
  - Tempo limite do experimento (minutos): 15
  - Tempo limite de iteração (minutos): 15
  - Marcar caixinha de "Habilitar encerramento antecipado"
  - Tipo de validação: Divisão de validação de treinamento
Clica em avançar.

Na parte de Computação pode deixar padrão e clicar em avançar.

Em Examinar você vai verificar se está tudo certo e se estiver correto clicar em "Enviar trabalho de treinamento".

Pronto, agora basta aguardar que o Status fique completo.

-Fim



