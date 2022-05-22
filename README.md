# FraudDetection_NVIDIAChallenge
Desafio proposto pelo NVIDIA para desenvolver um projeto de detecção de fraude.

## Base de dados 
A base de dados que será utilizada para o desenvolvimento deste desafio contém aproximadamente 6,3 milhões de transações, sendo extremamente desbalanceado, com apenas 0.12% representando transações fraudulentas. Os dados contidos nesta base de dados são simulados, não sendo transações reais efetuadas em algum sistema financeiro, e compreendem 30 dias. Estas transações podem ser de diferentes tipos e representam transações executadas via mobile devices. 


As features contidas nesta base de dados são:

- step - Passo: representa o total de horas transcorrido desde o início da simulação. Esta feature vai variar entre 1 e 744 (30 dias);

- type - Tipo: tipo de transação (depósito, saque, débito, pagamento e transferência);

- amount - Quantia: total que foi transacionado;

- nameOrig - ClienteOrigem: cliente que iniciou a transação

- oldbalanceOrg - SaldoInicialOrigem: saldo da conta de origem antes da transação;

- newbalanceOrig - SaldoFinalOrigem: saldo da conta de origem após a transação;

- nameDest - ClienteDestino: cliente de destino da transação;

- oldbalanceDest - SaldoInicialDestino: saldo da conta de destino antes da transação;

- newbalanceDest - SaldoFinalDestino: saldo da conta de destino após a transação;

- isFraud - ÉFraude: flag que define se a transação é fraudulenta ou não. Nesta simulação o objetivo da fraude é assumir a conta do usuário, esvaziá-la transferindo para outra conta e então sacando o dinheiro.

- isFlaggedFraud - SinalizadaComoFraude: automaticamente marcadas pelo banco como fraude por tentarem transferir mais de 200.000 em uma única transação.

## Metodologia

A fim de otimizar a detecção de fraudes, o projeto terá as seguintes etapas:

1. Aquisição e tratamento dos dados em caso de:
    - Dados faltantes
    - Dados duplicados
    - Dados incorretamente preenchidos
2. Análise exploratória de dados 
3. Feature Engineering
4. Modelagem
    - Modelos baseline
        - Logistic Regression
        - KNN
        - Decision Tree
        - Random Forest
        - Gradient Boosting
        - XGBoost
    - Modelos baseline com manipulação do threshold
    - Modelos com Class Weight
    - Rebalanceamento com Undersampling
    - Rebalanceamento com Oversampling
    - Rebalanceamento com SMOTE
    - Rebalanceamento com ADASYN
