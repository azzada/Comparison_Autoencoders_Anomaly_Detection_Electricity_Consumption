## Literature Table
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Paper&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;         | Year   | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Venue&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;                        |   AE&nbsp;Usage         | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Network&nbsp;Topology&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   |  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Dataset&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;                                                     |Regressors             | Uni&nbsp;or&nbsp;Multi     |Regularity                | Granularity           |Noise&nbsp;Level              |&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Anomaly&nbsp;Type&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Proprietary    
|----------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|---------------------|-------------------------------------------|---------------------------------------------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
|Himeur et al. [[1]](#1)           |2021|Applied Energy                                                                                                                                                                                              |Survey                                                           |                                                                                                                                         |                                                                                                                                                                 |       |                     |                                           |                                                   |                                       |                                                                                                                                                                                  |                                                                                                                                             |
|Malhotra et al. [[2]](#1)         |2016|ICML Anomaly Detection Workshop                                                                                                                                                                             |Anomaly Detection                                                |LSTM Encoder-Decoder                                                                                                                     |power demand, space shuttle, and ECG, and two real-world engine datasets with both predictive and unpredictable behavior                                         |no     |univariate           |Periodic                                   |15 min.                                            |low                                    |Unlabeled - Holidays                                                                                                                                                              |public http://www.cs.ucr.edu/~eamonn/discords/                                                                                               |          
|Fan et al. [[3]](#1)              |2018|Applied Energy                                                                                                                                                                                              |Anomaly Detection                                                |Ensamble of Fully connected feed- forward AE + 1D Convolutional AE                                                                       |electric consumption data from an educational building in Hong Kong                                                                                              |yes    |univariate           |daily                                      |30 min.                                            |different levels ranging from 0% to 20%|(1)anomalies due to atypical or rare operations; (2) anomalies due to transient operations; (3) anomalies due to improper control strategies (unlabeled)                          |private                                                                                                                                      |          
|Araya et al. [[4]](#1)            |2016|International Joint Conference on Neural Networks (IJCNN)                                                                                                                                                   |Anomaly Detection                                                |Vanilla AutoEncoder                                                                                                                      |HVAC consumption data of a School building                                                                                                                       |yes    |univariate           |daily                                      |5 min.                                             |low                                    |Unspecified (Unlabeled) real, Unspecified autogenerated                                                                                                                           |private                                                                                                                                      |          
|Araya et al. [[5]](#1)            |2017|Energy and Buildings                                                                                                                                                                                        |Anomaly Detection + Dimensionality Reduction                     |Ensamble of Methods included a vanilla AutoEncoder                                                                                       |HVAC consumption data of a School building                                                                                                                       |yes    |univariate           |daily                                      |5 min.                                             |low                                    |Unspecified (Unlabeled) real, Unspecified autogenerated                                                                                                                           |private                                                                                                                                      |          
|Tasfi et al. [[6]](#1)            |2017|IEEE International Conference on Internet of Things (iThings) and IEEE Green Computing and Communications (GreenCom) and IEEE Cyber, Physical and Social Computing (CPSCom) and IEEE Smart Data (SmartData) |Anomaly Detection                                                |model with two sub-networks: a convolutional autoencoder for the reconstruction of unlabelled data and a classifier for the labeled ones |electrical data of buildings                                                                                                                                     |no     |univariate           |daily, weekly                              |5 min.                                             |                                       |Unspecified (labelled) real, injected anomalies   (increase in usage over time for a small duration in periods with typical low usage)                                            |private                                                                                                                                      |          
|Pereira and Silveira [[7]](#1)     |2018|ICMLA                                                                                                                                                                                                       |Anomaly Detection                                                |variational Bi-LSTM autoen- coder with a variational self-attention mechanism                                                            |solar energy generation curves                                                                                                                                   |no     |univariate           |daily                                      |                                                   |low                                    |a brief shading, a fault, a spike anomaly, an example of a daily curve where snow covered the surface of the PV panel and a sequence corresponding to a cloudy day                |private                                                                                                                                      |          
|Dai et al. [[8]](#1)              |2022|4th International Conference on Intelligent Technologies and Applications                                                                                                                                   |Anomaly Detection                                                |variational LSTM autoencoder with a fully connected atten- tion mechanism                                                                |smart meter dataset about water supply temperature for district heating                                                                                          |yes?   |multivariate         |                                           |irregular minute-level                             |medium-low                             |                                                                                                                                                                                  |private                                                                                                                                      |          
|Castangia et al. [[9]](#1)        |2022|Sustain Energy, Grids and Netw                                                                                                                                                                              |Anomaly Detection                                                |variational convolutional autoencoder                                                                                                    |household appliances from 6 households in Switzerland                                                                                                            |no     |univariate           |periodic                                   |1 sec.                                             |medium                                 |Synthetic anomalies                                                                                                                                                               |public https://www.vs.inf.ethz.ch/res/show.html?what=eco-data                                                                                |          
|Lee et al. [[10]](#1)             |2022|ICCE                                                                                                                                                                                                        |Anomaly Detection                                                |Bi-LSTM autoencoder                                                                                                                      |data of electricity/water/heating/hot water from 985 households                                                                                                  |no     |univariate           |                                           |                                                   |low                                    |Unspecified (Unlabeled)                                                                                                                                                           |private                                                                                                                                      |          
|Weng et al. [[11]](#1)            |2018|IEEE Access                                                                                                                                                                                                 |Anomaly Detection                                                |LSTM AutoEncoder                                                                                                                         |consumption of electricity, natural gas and water from a Residential house                                                                                       |no     |univariate           |periodic                                   |1 min.                                             |low                                    |Dataset labelled through an ensamble-based method                                                                                                                                 |public https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/FIE0S4                                                       |          
|Yuan and Jia [[12]](#1)           |2015|International Conference on Intelligent Information Hiding and Multimedia Signal Processing                                                                                                                 |Feature Extraction                                               |Stacked sparse AutoEncoder + softmax for anomaly                                                                                         |alarm monitoring data, electricty monthly consumption data and basic information data                                                                            |yes    |univariate           |                                           |1 month                                            |low                                    |Labeled according to the alarm data                                                                                                                                               |private                                                                                                                                      |          
|Tsai et al. [[13]](#1)            |2022|Electronics - Special Issue Advances of Future IoE Wireless Network Technology                                                                                                                              |Feature Extraction                                               |Vanilla AutoEncoder                                                                                                                      |five residences randomly selected from 200 residential users who had installed energy management systems                                                         |yes    |univariate           |                                           |1 min.                                             |low                                    |Unlabeled - extreme power consumption behaviors such as sharp rises or falls                                                                                                      |private                                                                                                                                      |          
|Kaymakci et al. [[14]](#1)        |2021|54th CIRP CMS 2021 - Special Issue Towards Digitalized Manufacturing 4.0                                                                                                                                    |Anomaly Detection                                                |LSTM AutoEncoder                                                                                                                         |(1)supply electricity meter of a German metal processing company (2) electricity meter of a laser-punching machine                                               |no     |univariate           |periodic for the supply electricity measure|15 sec.                                            |medium                                 |Unlabeled - (1)anomalies are consequences of high solar power generation; (2) anomalies are  detected in case of significant deviations of the operating mode                     |private                                                                                                                                      |          
|Ullah et al. [[15]](#1)           |2020|MDPI Sensors                                                                                                                                                                                                |Feature Extraction                                               |Vanilla AutoEncoder (latent space dim > initial dim)                                                                                     |(1) energy consumption smart sensors data from residential buildings in a city (2) the data of a single house                                                    |       |univariate           |                                           |1) 1 month 2) 1 min.                               |                                       |                                                                                                                                                                                  |1) public https://data.openei.org/search?q= 2) public https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption|  
|Chahla et al. [[16]](#1)          |2019|International Conference on Pattern Recognition Applications and Methods                                                                                                                                    |?                                                                |                                                                                                                                         |                                                                                                                                                                 |       |                     |                                           |                                                   |                                       |                                                                                                                                                                                  |                                                                                                                                             |          
|Kardi et al. [[17]](#1)           |2021|IEEE Access                                                                                                                                                                                                 |Anomaly Detection                                                |LSTM AutoEncoder                                                                                                                         |electricity consumption                                                                                                                                          |yes    |univariate           |daily, weekly, yearly                      |1 hour                                             |low                                    |Unlabeled - unspecified                                                                                                                                                           |          
|Chahla et al. [[18]](#1)          |2020|Energy Efficiency                                                                                                                                                                                           |Anomaly Detection - to detect anomalous days                     |Vanilla AutoEncoder - not so important in the proposed method                                                                            |power utilization from 67 electronic devices in nearly 1000 houses                                                                                               |no     |univariate           |                                           |1 day                                              |low                                    |Unspecified (Unlabeled) - synthetic                                                                                                                                               |public https://dataport.pecanstreet.org                                                                                                      |          
|Zhao et al. [[19]](#1)            |2021|IEEE Internet of Things Journal                                                                                                                                                                             |Anomaly Detection - unsupervised case / denoise - supervised case|Vanilla AutoEncoder                                                                                                                      |power data for six different homes and high-frequency current/voltage data for the main power supply of two of these homes                                       |yes    |univariate           |periodic                                   |1 sec.                                             |medium-low                             |Unspecified (Unlabeled + labeled)                                                                                                                                                 |public http://redd.csail.mit.edu                                                                                                             |          
|Wang et al. [[20]](#1)            |2020|IEEE PES Innovative Smart Grid Technologies Europe                                                                                                                                                          |1) Anomaly Detection 2) Feature Extraction                       |1) Vanilla Autoencoder 2) Encoder of the AE                                                                                              |electricity consumption from 361 buildings of a university campus                                                                                                |yes    |univariate           |weekly                                     |15 min.                                            |low                                    |faulty smart meters and unusual consumption                                                                                                                                       |private                                                                                                                                      |          
|Wang et al. [[21]](#1)            |2022|IEEE Access                                                                                                                                                                                                 |Feature Extraction                                               |Vanilla AutoEncoder                                                                                                                      |electricity consumption of commercial buildings in three different Swedish cities                                                                                |no     |univariate           |according to hot / cold seasons            |1 hour                                             |low                                    |Labeled - unspecified                                                                                                                                                             |private                                                                                                                                      |          
|Park et al. [[22]](#1)            |2020|International Conference on Information and Communication Technology Convergence (ICTC)                                                                                                                     |Anomaly Detection                                                |LSTM AutoEncoder                                                                                                                         |power consumptions of lights, outlets, HVAC systems, elevator                                                                                                    |yes    |univariate           |daily, weekly                              |1 hour                                             |medium                                 |Unlabeled - synthetic anomalies                                                                                                                                                  |private                                                                                                                                      |          
|Himeur et al. [[24]](#1)          |2022|Sustainable Cities and Society                                                                                                                                                                              |Anomaly Detection                                                |Vanilla AutoEncoder                                                                                                                      |energy consumption                                                                                                                                               |hk     |univariate           |                                           |30 min.                                            |low                                    |Unlabeled - (1) excessive consumption; (2) consumption while outside                                                                                                           |public https://jack-kelly.com/data/                                                                                                          |          
|Himeur et al. [[25]](#1)          |2022|International Conference On Big Data and Internet of Things                                                                                                                                                 |Anomaly Detection                                                |Vanilla AutoEncoder                                                                                                                      |electricity consumption footprints of different appliances registered in a UK household                                                                          |hk     |univariate           |                                           |30 min.                                            |low                                    |Unlabeled - (1) excessive consumption; (2) consumption while outside                                                                                                           |public https://jack-kelly.com/data/                                                                                                          |          

## Network parameters

DIRE CHE L'OPTIMIZER è ADAM PER TUTTI
CNN AE
*	window = 672
*	stride = 4
*	latent_dim = 6
•	epochs = 150
•	batch_size = 8
•	f = 7
•	First Conv Layer – 16 filters
•	Second Conv Layer – 32 filters
•	Third Conv Layer – 64 filters
•	First ConvTranspose Layer – 64 filters
•	Second ConvTranspose Layer – 32 filters
•	Third ConvTranspose Layer – 16 filters
•	Patience = 15
•	Learning rate = 10^(-3)

CNN VAE
•	window = 672
•	stride = 4
•	M = 200
•	latent_dim = 10
•	epochs = 150
•	batch_size = 8
•	f = 5
•	First Conv Layer – 16 filters
•	Second Conv Layer – 32 filters
•	Third Conv Layer – 64 filters
•	First ConvTranspose Layer – 64 filters
•	Second ConvTranspose Layer – 32 filters
•	Third ConvTranspose Layer – 16 filters
•	Patience = 15
•	Learning rate = 10^(-3)

LSTM AE
•	window = 672
•	stride = 4
•	latent_dim = 6
•	epochs = 150
•	batch_size = 8
•	First LSTM Layer (encoder) – 64 memory elements
•	Second LSTM Layer (encoder) – 6 memory elements
•	First LSTM Layer (decoder) – 64 memory elements
•	Patience = 10
•	Learning rate = 10^(-3)

LSTM VAE
•	window = 672
•	stride = 4
•	M = 200
•	latent_dim = 10
•	epochs = 150
•	batch_size = 8
•	First LSTM Layer (encoder) – 64 memory elements
•	Second LSTM Layer (encoder) – 10 memory elements
•	First LSTM Layer (decoder) – 64 memory elements
•	Patience = 10
•	Learning rate = 10^(-3)
 
CNN VAE Rec Prob
•	window = 672
•	stride = 4
•	M = 200
•	latent_dim = 10
•	epochs = 150
•	batch_size = 8
•	f = 5
•	First Conv Layer – 16 filters
•	Second Conv Layer – 32 filters
•	Third Conv Layer – 64 filters
•	First ConvTranspose Layer – 64 filters
•	Second ConvTranspose Layer – 32 filters
•	Third ConvTranspose Layer – 16 filters
•	Patience = 15
•	Learning rate = 10^(-3)

LSTM VAE Rec Prob
•	window = 672
•	stride = 4
•	M = 200
•	latent_dim = 10
•	epochs = 150
•	batch_size = 8
•	First LSTM Layer (encoder) – 64 memory elements
•	Second LSTM Layer (encoder) – 10 memory elements
•	First LSTM Layer (decoder) – 64 memory elements
•	Patience = 10
•	Learning rate = 10^(-3)
 
LSTM VAE Self-Attention
•	window = 672
•	stride = 4
•	M = 200
•	latent_dim = 10
•	epochs = 150
•	batch_size = 8
•	First LSTM Layer (encoder) – 64 memory elements
•	First LSTM Layer (decoder) – 64 memory elements
•	Patience = 10
•	Learning rate = 10^(-3)


## References
<a id="1">[1]</a>  Himeur, Yassine, et al. "Artificial intelligence based anomaly detection of energy consumption in buildings: A review, current trends and new perspectives." Applied Energy 287 (2021): 116601.

<a id="2">[2]</a>  Malhotra, Pankaj, et al. "LSTM-based encoder-decoder for multi-sensor anomaly detection." ICML Anomaly Detection Workshop

<a id="3">[3]</a>  Fan, Cheng, et al. "Analytical investigation of autoencoder-based methods for unsupervised anomaly detection in building energy data." Applied energy 211 (2018): 1123-1135.

<a id="4">[4]</a> 