# Empirical Evaluation of Deep Autoencoders for Anomaly Detection in Electricity Consumption of Buildings

This repository contains additional material for the article "Empirical Evaluation of Deep Autoencoders for Anomaly Detection in Electricity Consumption of Buildings" authored by D. Azzalini, B. Flammini, C. A. Emanuele, A. Guadagno, E. Ragaini, and F. Amigoni, currently under major revision at IEEE Intelligent Systems.

## Related Work
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Paper&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;         | Year   | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Venue&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;                        |   AE&nbsp;Usage         | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Network&nbsp;Topology&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   |  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Dataset&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;                                                     |Regressors             | Uni&nbsp;or&nbsp;Multi     |Regularity                | Granularity           |Noise&nbsp;Level              |&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Anomaly&nbsp;Type&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Proprietary    
|----------------------------------|----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|---------------------|-------------------------------------------|---------------------------------------------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
|Himeur et al. [[1]](#1)           |2021|Applied Energy                                                                                                                                                                                              |Survey                                                           |                                                                                                                                         |                                                                                                                                                                 |       |                     |                                           |                                                   |                                       |                                                                                                                                                                                  |                                                                                                                                             |
|Malhotra et al. [[2]](#2)         |2016|ICML Anomaly Detection Workshop                                                                                                                                                                             |Anomaly Detection                                                |LSTM Encoder-Decoder                                                                                                                     |power demand, space shuttle, and ECG, and two real-world engine datasets with both predictive and unpredictable behavior                                         |no     |univariate           |Periodic                                   |15 min.                                            |low                                    |Unlabeled - Holidays                                                                                                                                                              |public http://www.cs.ucr.edu/~eamonn/discords/                                                                                               |          
|Fan et al. [[3]](#3)              |2018|Applied Energy                                                                                                                                                                                              |Anomaly Detection                                                |Ensamble of Fully connected feed- forward AE + 1D Convolutional AE                                                                       |electric consumption data from an educational building in Hong Kong                                                                                              |yes    |univariate           |daily                                      |30 min.                                            |different levels ranging from 0% to 20%|(1)anomalies due to atypical or rare operations; (2) anomalies due to transient operations; (3) anomalies due to improper control strategies (unlabeled)                          |private                                                                                                                                      |          
|Araya et al. [[4]](#4)            |2016|International Joint Conference on Neural Networks (IJCNN)                                                                                                                                                   |Anomaly Detection                                                |Vanilla AutoEncoder                                                                                                                      |HVAC consumption data of a School building                                                                                                                       |yes    |univariate           |daily                                      |5 min.                                             |low                                    |Unspecified (Unlabeled) real, Unspecified autogenerated                                                                                                                           |private                                                                                                                                      |          
|Araya et al. [[5]](#5)            |2017|Energy and Buildings                                                                                                                                                                                        |Anomaly Detection + Dimensionality Reduction                     |Ensamble of Methods included a vanilla AutoEncoder                                                                                       |HVAC consumption data of a School building                                                                                                                       |yes    |univariate           |daily                                      |5 min.                                             |low                                    |Unspecified (Unlabeled) real, Unspecified autogenerated                                                                                                                           |private                                                                                                                                      |          
|Tasfi et al. [[6]](#6)            |2017|IEEE International Conference on Internet of Things (iThings) and IEEE Green Computing and Communications (GreenCom) and IEEE Cyber, Physical and Social Computing (CPSCom) and IEEE Smart Data (SmartData) |Anomaly Detection                                                |model with two sub-networks: a convolutional autoencoder for the reconstruction of unlabelled data and a classifier for the labeled ones |electrical data of buildings                                                                                                                                     |no     |univariate           |daily, weekly                              |5 min.                                             |                                       |Unspecified (labelled) real, injected anomalies   (increase in usage over time for a small duration in periods with typical low usage)                                            |private                                                                                                                                      |          
|Pereira and Silveira [[7]](#7)     |2018|ICMLA                                                                                                                                                                                                       |Anomaly Detection                                                |variational Bi-LSTM autoen- coder with a variational self-attention mechanism                                                            |solar energy generation curves                                                                                                                                   |no     |univariate           |daily                                      |                                                   |low                                    |a brief shading, a fault, a spike anomaly, an example of a daily curve where snow covered the surface of the PV panel and a sequence corresponding to a cloudy day                |private                                                                                                                                      |          
|Dai et al. [[8]](#8)              |2022|4th International Conference on Intelligent Technologies and Applications                                                                                                                                   |Anomaly Detection                                                |variational LSTM autoencoder with a fully connected atten- tion mechanism                                                                |smart meter dataset about water supply temperature for district heating                                                                                          |yes?   |multivariate         |                                           |irregular minute-level                             |medium-low                             |                                                                                                                                                                                  |private                                                                                                                                      |          
|Castangia et al. [[9]](#9)        |2022|Sustain Energy, Grids and Netw                                                                                                                                                                              |Anomaly Detection                                                |variational convolutional autoencoder                                                                                                    |household appliances from 6 households in Switzerland                                                                                                            |no     |univariate           |periodic                                   |1 sec.                                             |medium                                 |Synthetic anomalies                                                                                                                                                               |public https://www.vs.inf.ethz.ch/res/show.html?what=eco-data                                                                                |          
|Lee et al. [[10]](#10)             |2022|ICCE                                                                                                                                                                                                        |Anomaly Detection                                                |Bi-LSTM autoencoder                                                                                                                      |data of electricity/water/heating/hot water from 985 households                                                                                                  |no     |univariate           |                                           |                                                   |low                                    |Unspecified (Unlabeled)                                                                                                                                                           |private                                                                                                                                      |          
|Weng et al. [[11]](#11)            |2018|IEEE Access                                                                                                                                                                                                 |Anomaly Detection                                                |LSTM AutoEncoder                                                                                                                         |consumption of electricity, natural gas and water from a Residential house                                                                                       |no     |univariate           |periodic                                   |1 min.                                             |low                                    |Dataset labelled through an ensamble-based method                                                                                                                                 |public https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/FIE0S4                                                       |          
|Yuan and Jia [[12]](#12)           |2015|International Conference on Intelligent Information Hiding and Multimedia Signal Processing                                                                                                                 |Feature Extraction                                               |Stacked sparse AutoEncoder + softmax for anomaly                                                                                         |alarm monitoring data, electricty monthly consumption data and basic information data                                                                            |yes    |univariate           |                                           |1 month                                            |low                                    |Labeled according to the alarm data                                                                                                                                               |private                                                                                                                                      |          
|Tsai et al. [[13]](#13)            |2022|Electronics - Special Issue Advances of Future IoE Wireless Network Technology                                                                                                                              |Feature Extraction                                               |Vanilla AutoEncoder                                                                                                                      |five residences randomly selected from 200 residential users who had installed energy management systems                                                         |yes    |univariate           |                                           |1 min.                                             |low                                    |Unlabeled - extreme power consumption behaviors such as sharp rises or falls                                                                                                      |private                                                                                                                                      |          
|Kaymakci et al. [[14]](#14)        |2021|54th CIRP CMS 2021 - Special Issue Towards Digitalized Manufacturing 4.0                                                                                                                                    |Anomaly Detection                                                |LSTM AutoEncoder                                                                                                                         |(1)supply electricity meter of a German metal processing company (2) electricity meter of a laser-punching machine                                               |no     |univariate           |periodic for the supply electricity measure|15 sec.                                            |medium                                 |Unlabeled - (1)anomalies are consequences of high solar power generation; (2) anomalies are  detected in case of significant deviations of the operating mode                     |private                                                                                                                                      |          
|Ullah et al. [[15]](#15)           |2020|MDPI Sensors                                                                                                                                                                                                |Feature Extraction                                               |Vanilla AutoEncoder (latent space dim > initial dim)                                                                                     |(1) energy consumption smart sensors data from residential buildings in a city (2) the data of a single house                                                    |       |univariate           |                                           |1) 1 month 2) 1 min.                               |                                       |                                                                                                                                                                                  |1) public https://data.openei.org/search?q= 2) public https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption|  
|Chahla et al. [[16]](#16)          |2019|International Conference on Pattern Recognition Applications and Methods                                                                                                                                    |?                                                                |                                                                                                                                         |                                                                                                                                                                 |       |                     |                                           |                                                   |                                       |                                                                                                                                                                                  |                                                                                                                                             |          
|Kardi et al. [[17]](#17)           |2021|IEEE Access                                                                                                                                                                                                 |Anomaly Detection                                                |LSTM AutoEncoder                                                                                                                         |electricity consumption                                                                                                                                          |yes    |univariate           |daily, weekly, yearly                      |1 hour                                             |low                                    |Unlabeled - unspecified                                                                                                                                                           |          
|Chahla et al. [[18]](#18)          |2020|Energy Efficiency                                                                                                                                                                                           |Anomaly Detection - to detect anomalous days                     |Vanilla AutoEncoder - not so important in the proposed method                                                                            |power utilization from 67 electronic devices in nearly 1000 houses                                                                                               |no     |univariate           |                                           |1 day                                              |low                                    |Unspecified (Unlabeled) - synthetic                                                                                                                                               |public https://dataport.pecanstreet.org                                                                                                      |          
|Zhao et al. [[19]](#19)            |2021|IEEE Internet of Things Journal                                                                                                                                                                             |Anomaly Detection - unsupervised case / denoise - supervised case|Vanilla AutoEncoder                                                                                                                      |power data for six different homes and high-frequency current/voltage data for the main power supply of two of these homes                                       |yes    |univariate           |periodic                                   |1 sec.                                             |medium-low                             |Unspecified (Unlabeled + labeled)                                                                                                                                                 |public http://redd.csail.mit.edu                                                                                                             |          
|Wang et al. [[20]](#20)            |2020|IEEE PES Innovative Smart Grid Technologies Europe                                                                                                                                                          |1) Anomaly Detection 2) Feature Extraction                       |1) Vanilla Autoencoder 2) Encoder of the AE                                                                                              |electricity consumption from 361 buildings of a university campus                                                                                                |yes    |univariate           |weekly                                     |15 min.                                            |low                                    |faulty smart meters and unusual consumption                                                                                                                                       |private                                                                                                                                      |          
|Wang et al. [[21]](#21)            |2022|IEEE Access                                                                                                                                                                                                 |Feature Extraction                                               |Vanilla AutoEncoder                                                                                                                      |electricity consumption of commercial buildings in three different Swedish cities                                                                                |no     |univariate           |according to hot / cold seasons            |1 hour                                             |low                                    |Labeled - unspecified                                                                                                                                                             |private                                                                                                                                      |          
|Park et al. [[22]](#22)            |2020|International Conference on Information and Communication Technology Convergence (ICTC)                                                                                                                     |Anomaly Detection                                                |LSTM AutoEncoder                                                                                                                         |power consumptions of lights, outlets, HVAC systems, elevator                                                                                                    |yes    |univariate           |daily, weekly                              |1 hour                                             |medium                                 |Unlabeled - synthetic anomalies                                                                                                                                                  |private                                                                                                                                      |          
|Himeur et al. [[23]](#23)          |2022|Sustainable Cities and Society                                                                                                                                                                              |Anomaly Detection                                                |Vanilla AutoEncoder                                                                                                                      |energy consumption                                                                                                                                               |hk     |univariate           |                                           |30 min.                                            |low                                    |Unlabeled - (1) excessive consumption; (2) consumption while outside                                                                                                           |public https://jack-kelly.com/data/                                                                                                          |          
|Himeur et al. [[24]](#24)          |2022|International Conference On Big Data and Internet of Things                                                                                                                                                 |Anomaly Detection                                                |Vanilla AutoEncoder                                                                                                                      |electricity consumption footprints of different appliances registered in a UK household                                                                          |hk     |univariate           |                                           |30 min.                                            |low                                    |Unlabeled - (1) excessive consumption; (2) consumption while outside                                                                                                           |public https://jack-kelly.com/data/                                                                                                          |          

## Network Parameters

### CNN AE

*	window = 672
*	stride = 4
*	latent_dim = 6
    <img align="right"  height="50%" width="50%" src="https://github.com/AGuadagno/Comparison_Autoencoders_Anomaly_Detection_Electricity_Consumption/blob/main/img/CONV_AE_REC_E.png"> 
*	epochs = 150
*	batch_size = 8
*	f = 7
*	First Conv Layer – 16 filters
*	Second Conv Layer – 32 filters
*	Third Conv Layer – 64 filters
*	First ConvTranspose Layer – 64 filters
*	Second ConvTranspose Layer – 32 filters
*	Third ConvTranspose Layer – 16 filters
*	Patience = 15
*	Learning rate = 10<sup>-3</sup>


### CNN VAE
*	window = 672
*	stride = 4
*	M = 200
*	latent_dim = 10
    <img align="right"  height="50%" width="50%" src="https://github.com/AGuadagno/Comparison_Autoencoders_Anomaly_Detection_Electricity_Consumption/blob/main/img/CONV_VAE_REC_E.png"> 
*	epochs = 150
*	batch_size = 8
*	f = 5
*	optimizer = adam
*	First Conv Layer – 16 filters
*	Second Conv Layer – 32 filters
*	Third Conv Layer – 64 filters
*	First ConvTranspose Layer – 64 filters
*	Second ConvTranspose Layer – 32 filters
*	Third ConvTranspose Layer – 16 filters
*	Patience = 15
*	Learning rate = 10<sup>-3</sup>

### LSTM AE
*	window = 672
*	stride = 4
*	latent_dim = 6
    <img align="right"  height="42%" width="42%" src="https://github.com/AGuadagno/Comparison_Autoencoders_Anomaly_Detection_Electricity_Consumption/blob/main/img/LSTM_AE_REC_E.png"> 
*	epochs = 150
*	batch_size = 8
*	optimizer = adam
*	First LSTM Layer (encoder) – 64 memory elements
*	Second LSTM Layer (encoder) – 6 memory elements
*	First LSTM Layer (decoder) – 64 memory elements
*	Patience = 10
*	Learning rate = 10<sup>-3</sup>

### LSTM VAE
*	window = 672
*	stride = 4
*	M = 200
    <img align="right"  height="50%" width="50%" src="https://github.com/AGuadagno/Comparison_Autoencoders_Anomaly_Detection_Electricity_Consumption/blob/main/img/LSTM_VAE_REC_E.png"> 
*	latent_dim = 10
*	epochs = 150
*	batch_size = 8
*	optimizer = adam
*	First LSTM Layer (encoder) – 64 memory elements
*	Second LSTM Layer (encoder) – 10 memory elements
*	First LSTM Layer (decoder) – 64 memory elements
*	Patience = 10
*	Learning rate = 10<sup>-3</sup>
 
### CNN VAE Rec Prob
*	window = 672
*	stride = 4
*	M = 200
*	latent_dim = 10
    <img align="right"  height="50%" width="50%" src="https://github.com/AGuadagno/Comparison_Autoencoders_Anomaly_Detection_Electricity_Consumption/blob/main/img/CONV_VAE_REC_P.png"> 
*	epochs = 150
*	batch_size = 8
*	f = 5
*	optimizer = adam
*	First Conv Layer – 16 filters
*	Second Conv Layer – 32 filters
*	Third Conv Layer – 64 filters
*	First ConvTranspose Layer – 64 filters
*	Second ConvTranspose Layer – 32 filters
*	Third ConvTranspose Layer – 16 filters
*	Patience = 15
*	Learning rate = 10<sup>-3</sup>

### LSTM VAE Rec Prob
*	window = 672
*	stride = 4
*	M = 200
    <img align="right"  height="50%" width="50%"  src="https://github.com/AGuadagno/Comparison_Autoencoders_Anomaly_Detection_Electricity_Consumption/blob/main/img/LSTM_VAE_REC_P.png"> 
*	latent_dim = 10
*	epochs = 150
*	batch_size = 8
*	optimizer = adam
*	First LSTM Layer (encoder) – 64 memory elements
*	Second LSTM Layer (encoder) – 10 memory elements
*	First LSTM Layer (decoder) – 64 memory elements
*	Patience = 10
*	Learning rate = 10<sup>-3</sup>
 
### LSTM VAE Self-Attention
*	window = 672
*	stride = 4
    <img align="right"  height="50%" width="50%" src="https://github.com/AGuadagno/Comparison_Autoencoders_Anomaly_Detection_Electricity_Consumption/blob/main/img/LSTM_ATT_REC_P.png"> 
*	M = 200
*	latent_dim = 10
*	epochs = 150
*	batch_size = 8
*	optimizer = adam
*	First LSTM Layer (encoder) – 64 memory elements
*	First LSTM Layer (decoder) – 64 memory elements
*	Patience = 10
*	Learning rate = 10<sup>-3</sup>



## References
<a id="1">[1]</a>  Himeur, Y., Ghanem, K., Alsalemi, A., Bensaali, F., & Amira, A. (2021). Artificial intelligence based anomaly detection of energy consumption in buildings: A review, current trends and new perspectives. Applied Energy, 287, 1-26.

<a id="2">[2]</a>  Malhotra, P., Ramakrishnan, A., Anand, G., Vig, L., Agarwal, P., & Shroff, G. (2016). LSTM-based encoder-decoder for multi-sensor anomaly detection. ICML Anomaly Detection Workshop

<a id="3">[3]</a>  Fan, C., Xiao, F., Zhao, Y., & Wang, J. (2018). Analytical investigation of autoencoder-based methods for unsupervised anomaly detection in building energy data. Applied energy, 211, 1123-1135.

<a id="4">[4]</a> Araya, D. B., Grolinger, K., ElYamany, H. F., Capretz, M. A., & Bitsuamlak, G. (2016). Collective contextual anomaly detection framework for smart buildings. In 2016 international joint conference on neural networks (IJCNN) (pp. 511-518). IEEE.

<a id="5">[5]</a> Araya, D. B., Grolinger, K., ElYamany, H. F., Capretz, M. A., & Bitsuamlak, G. (2017). An ensemble learning framework for anomaly detection in building energy consumption. Energy and Buildings, 144, 191-206.Tasfi, N. L., Higashino, W. A., Grolinger, K., & Capretz, M. A. (2017, June). Deep neural networks with confidence sampling for electrical anomaly detection. In 2017 IEEE International Conference on Internet of Things (iThings) and IEEE Green Computing and Communications (GreenCom) and IEEE Cyber, Physical and Social Computing (CPSCom) and IEEE Smart Data (SmartData) (pp. 1038-1045). IEEE.

<a id="6">[6]</a> Tasfi, N. L., Higashino, W. A., Grolinger, K., & Capretz, M. A. (2017). Deep neural networks with confidence sampling for electrical anomaly detection. In 2017 IEEE International Conference on Internet of Things (iThings) and IEEE Green Computing and Communications (GreenCom) and IEEE Cyber, Physical and Social Computing (CPSCom) and IEEE Smart Data (SmartData) (pp. 1038-1045). IEEE.

<a id="7">[7]</a> Pereira, J., & Silveira, M. (2018). Unsupervised anomaly detection in energy time series data using variational recurrent autoencoders with attention. In 2018 17th IEEE international conference on machine learning and applications (ICMLA) (pp. 1275-1282). IEEE.

<a id="8">[8]</a> Dai, W., Liu, X., Heller, A., & Nielsen, P. S. (2022). Smart Meter Data Anomaly Detection Using Variational Recurrent Autoencoders with Attention. In International Conference on Intelligent Technologies and Applications (pp. 311-324). Springer, Cham.

<a id="9">[9]</a> Castangia, M., Sappa, R., Girmay, A. A., Camarda, C., Macii, E., & Patti, E. (2022). Anomaly detection on household appliances based on variational autoencoders. Sustainable Energy, Grids and Networks, 32, 100823.

<a id="10">[10]</a> Lee, S., Jin, H., Nengroo, S. H., Doh, Y., Lee, C., Heo, T., & Har, D. (2022). Smart Metering System Capable of Anomaly Detection by Bi-directional LSTM Autoencoder. In 2022 IEEE International Conference on Consumer Electronics (ICCE) (pp. 1-6). IEEE.

<a id="11">[11]</a> Weng, Y., Zhang, N., & Xia, C. (2018). Multi-agent-based unsupervised detection of energy consumption anomalies on smart campus. IEEE Access, 7, 2169-2178.

<a id="12">[12]</a> Yuan, Y., & Jia, K. (2015). A distributed anomaly detection method of operation energy consumption using smart meter data. In 2015 international conference on intelligent information hiding and multimedia signal processing (IIH-MSP) (pp. 310-313). IEEE.

<a id="13">[13]</a> Tsai, C. W., Chiang, K. C., Hsieh, H. Y., Yang, C. W., Lin, J., & Chang, Y. C. (2022). Feature Extraction of Anomaly Electricity Usage Behavior in Residence Using Autoencoder. Electronics, 11(9), 1450.

<a id="14">[14]</a> Kaymakci, C., Wenninger, S., & Sauer, A. (2021). Energy Anomaly Detection in Industrial Applications with Long Short-term Memory-based Autoencoders. Procedia CIRP, 104, 182-187.

<a id="15">[15]</a> Ullah, A., Haydarov, K., Ul Haq, I., Muhammad, K., Rho, S., Lee, M., & Baik, S. W. (2020). Deep learning assisted buildings energy consumption profiling using smart meter data. Sensors, 20(3), 873.

<a id="16">[16]</a> Chahla, C., Snoussi, H., Merghem, L., & Esseghir, M. (2019). A Novel Approach for Anomaly Detection in Power Consumption Data. In ICPRAM (pp. 483-490).

<a id="17">[17]</a> Kardi, M., AlSkaif, T., Tekinerdogan, B., & Catalao, J. P. (2021). Anomaly Detection in Electricity Consumption Data using Deep Learning. In 2021 IEEE International Conference on Environment and Electrical Engineering and 2021 IEEE Industrial and Commercial Power Systems Europe (EEEIC/I&CPS Europe) (pp. 1-6). IEEE.

<a id="18">[18]</a> Chahla, C., Snoussi, H., Merghem, L., & Esseghir, M. (2020). A deep learning approach for anomaly detection and prediction in power consumption data. Energy Efficiency, 13(8), 1633-1651.

<a id="19">[19]</a> Zhao, Q., Chang, Z., & Min, G. (2021). Anomaly Detection and Classification of Household Electricity Data: A Time Window and Multilayer Hierarchical Network Approach. IEEE Internet of Things Journal, 9(5), 3704-3716.

<a id="20">[20]</a> Wang, L., Turowski, M., Zhang, M., Riedel, T., Beigl, M., Mikut, R., & Hagenmeyer, V. (2020). Point and contextual anomaly detection in building load profiles of a university campus. In 2020 IEEE PES Innovative Smart Grid Technologies Europe (ISGT-Europe) (pp. 11-15). IEEE.

<a id="21">[21]</a> Wang, D., Enlund, T., Trygg, J., Tysklind, M., & Jiang, L. (2022). Toward Delicate Anomaly Detection of Energy Consumption for Buildings: Enhance the Performance From Two Levels. IEEE Access, 10, 31649-31659.

<a id="22">[22]</a> Park, S., Jung, S., Hwang, E., & Rho, S. (2021). Variational AutoEncoder-Based Anomaly Detection Scheme for Load Forecasting. In Advances in Artificial Intelligence and Applied Cognitive Computing (pp. 833-839). Springer, Cham.

<a id="23">[23]</a> Nam, H. S., Jeong, Y. K., & Park, J. W. (2020). An anomaly detection scheme based on lstm autoencoder for energy management. In 2020 International Conference on Information and Communication Technology Convergence (ICTC) (pp. 1445-1447). IEEE.

<a id="24">[24]</a> Alsalemi, A., Himeur, Y., Bensaali, F., & Amira, A. (2022). An innovative edge-based Internet of Energy solution for promoting energy saving in buildings. Sustainable Cities and Society, 78, 103571.

<a id="25">[25]</a> Himeur, Y., Alsalemi, A., Bensaali, F., & Amira, A. (2022). Detection of appliance-level abnormal energy consumption in buildings using autoencoders and micro-moments. In International Conference On Big Data and Internet of Things (pp. 179-193). Springer, Cham.
