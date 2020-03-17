# When things matter: A survey on data-centric internet of things

### Resumo
- avancos em RFID
- Custo baixo em sensores wireless
- IOT ganha um espaco cada vez maior no dia a dia
    - integrar entidades fisicas e digitais
- permite uma nova classe de aplicacoes e servicos
- Um desafio esta na gestao dos dados
    - sao tipicamentes produzidos dinamicamente
    - volateis
    - pouco volume e em pequena escala
    - continuo
    - ruidoso
- introduzir processamento de stream de dados
- data storage
- event processing 
- searching in IOT


### Introducao


- A internet prove servicos para bilhoes de usuarios mundialmente
- IOT enfatiza os objetos ao invez dos computadores (Ashton,2009)
    - conectar objetos do dia a dia a internet
    - permitir a comunicacao e interacao entre esses objetos
- Existem varias definicoes sobre IOT de diferentes perspectivas
    - Servicos : “a world where things can automatically communicate to computers and each other providing services to the benefit of the human kind” (CASAGRAS, 2000)
    - Conectividade : “from anytime, anyplace connectivity for anyone, we will now have connectivity for anything” (ITU, 2005).
    - Comunicacao : “a world-wide network of interconnected objects uniquely addressable, based on standard communication protocols” (INFSO, 2008).
    - Networking : “from a network of interconnected computers to a network of interconnected objects” (European Commission, 2009). ( the internet evolved.)
- O foco do estudo eh a perspectiva segundo o dado
    - o dado eh processado de forma diferente em IOT se comparado com a internet tradicional
    - o consumidor dos dados IOT sao tantos os humanos quando os produtores de dados
    - no contexto da internet das coisas, os compostos interligados sao os maiores consumidores e produtores de dados, os computadores serao capazes de aprender e ganhar informacoes para resolver problemas do mundo real utilizando diretamente dos dados colhidos pelos compomentes. Como objetivo a tecnologia IOT sera capaz de sentir e reagir ao mundo real para os humanos


### Iot data taxonomy

- Data generation
    - Velocity 
         - quanto dado consigo gerar por tempo
    - Scalability
        - IoT  geram dados continuamente, pode ser esperado uma grande quantidade de dados 
    - Dynamics
        - muitas coisas podem ser moveis, elas podem ser movidas para ambientes diferentes, afetando assim seus dados
        - muitas coisas sao frageis, estao sujeitas a fakhas 
        - a conexcao pode ser intermitente
    - Heterogeneity
        - existe uma variedade de objetos conectadas com a internet e isso afeta na geracao de dados em diferentes formatos utilizando vocabulos diferentes

- Data Quality
    - Uncertainty
        - reprodutibilidade de uma medida
        - acuracia
    - Redundancy
        - leituras duplicadas 
        - grupo de sensores em uma area proxima que produzem dados simlares
        - sensores com taxas de amostragem altas    
    - Ambiguity
        - O dado produzido por um conjunto de objetos pode ser interpretado de formas diferentes devido a necessidade de cada consumidor do dado
    - Inconsistency
        - Erro de leitura
        - packet loss
        - acuracia e precisao

- Data interoperability
    - Incompletness
        - como os dados sao gerados de forma distribuida, eh possivel verificar uma imcompletude nos dados quando se necessita processar os dados em tempo real
    - semantics
        - permitir que outros objetos entendam e processem os dados produzidos por objetos
        
### Data streams

- Um stream de dados pode ser gerado continuamente em grande quantidade
- suas caracteristicas tipicas
    - continua recepcao de objetos de dados
    - recepcao de dados desordenado
    - potencialmente sem limite
    - sem percistencia apos o processamento
    - variacao na disrtibuicao normal de dados previamente nao conhecidos
- Existe uma demanda para algoritimos de processamento de dados eficientes para sistemas de sensores devido ao poder computacional e a existencia de erros e leituras tendenciosas do sensor.
    - agregate queries
    - join queries
    - top-k monitoring
    - Continuous queries
- Ao realizar a query sob um dado provindo de uma stream nos temos que focar mais nas relacoes de incerteza, inconsistencia e ambifuidade. 
    - como podemos fazer de forma eficiente join sob dados incertos com ambiguidade ou incompletude?
    - como identificar os valores top-k entre milhoes de dados heterogeneos e incompleto?
- Stream mining pode ser util para extrair regras/informacoes do dado.
    - Clustering
    - Classification
    - Outlier and anomaly detection
    - Frequent itemset mining
- 3.2 exemplifica alguns algoritimos de tratamento de dados provindos de sensores RFID
- 3.3 exemplifica alguns algoritimos para tratamento do processamento de triple stream

### Data storage models

- Tradicional Database Management Systems (DBMSs)
    - write-optimized or read-optmized
    - row store architecture or column store achiteture
-  Large-scale storage in distributed environments
    - replicar o dado pode ser uma aboradagem, sendo preferivel uma estrategia de replica seletiva para melhorar work balance dos datacenters
    - Consistencia
    - Disponibilidade
    - Tolerancia a fragmentacao 
    - Contudo, um distributed storage system nao consegue satisfazer os 3 requisitos ao mesmo tempo (Gilbert and Lynch - 2002)
- Storage on resource-constrained devices
    - for exemple in sensor networks, communication activity plays a more important role than storage

### Search techniques

- innovative ways of managing and searching from dynamic data
- Deep web and Semantic web
- Web search
- keywords based search of things

### Open issues

- Data quality and uncertainty
-  Co-space data:
- Transaction handling
-  Frequently Updated Timestamped Structured (FUTS) data
- Distributed and mobile data
- Semantic enrichment and semantic event processing
- Mining
- Knowledge discovery
- Security
- Privacy 
- Social concerns
