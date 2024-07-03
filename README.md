# Internet of Vehicles
The Internet of Vehicles (IoV) is an application of Internet of Things (IoT) in the context of intelligent transportation systems (ITS). The IoV has a similar architecture to the IoT and features a hierarchical structure that includes data source, edge, fog, and the cloud layers. Vehicles share information with other vehicles, pedestrians, intelligent infrastructure, and backbone networks to establish vehicle-to-vehicle, vehicle-to pedestrian, vehicle-to-infrastructure, and vehicle-to-network communication, thereby formulating vehicle-to-everything (V2X) communication. Figure 1 thus depicts the architecture of an IoV network. The main IoV communication node is a vehicle with an on-board unit (OBU) which can communicate with the Roadside Units (RSUs) and other vehicles in its proximity.  <br/><br/> ![A system architecture of the IoV.](Fig1.png)  Figure 1. A system architecture of the IoV. <br/><br/>
# Trust in the Internet of Vehicles
Due to the unique characteristics of IoV, i.e., openness, dynamic topology, and high mobility, it is susceptible to attacks; dishonest entities can modify legitimate security messages, spread forged information, or delay forwarding messages, thereby endangering human lives. Accordingly, researchers have proposed several solutions for handling the issues pertinent to IoV security. Nevertheless, a number of these solutions rely on conventional cryptographic-related schemes and, therefore, rely on the notions of digital signatures, certificates, and public key infrastructure. Moreover, conventional cryptographicrelated schemes are only capable of mitigating external attacks and are ineffective against internal network attacks. It is due to this reason that the paradigm of trust has been recently introduced in the research literature. Trust is generally referred to as the confidence of a trustor in a trustee. Here, trustor refers to a node that is in a position to ascertain the trust of the other node (trustee) in the network, whereas the trustee refers to a node whose trust is being ascertained. In the context of the proposed dataset, trust refers to the likelihood that a trustee can perform a particular operation within a specific situation at a specific time. It is also important to mention that trust computation primarily involves a weighted aggregation of both the direct trust and the indirect trust. Direct trust is ascertained as a result of direct interactions between a trustor and a trustee and is generally referred to as a trustor’s direct observation of a trustee. On the contrary, indirect trust is computed by taking into account the direct trust ascertained by the one-hop neighbors of a trustor pertinent to a trustee.<br/><br/>
# Data Description
The envisaged trust-based IoV dataset employs Java for designing an IoV-based simulator, whereas, Python for analyzing the simulation results. The traces in this particular dataset transpired as a result of a simulation carried out for a duration of *1* hour via the IoV-based simulator. The IoV simulator takes into account several interconnected road segments in order to mimic a road network encompassing vehicles traversing at random speeds in disparate directions. Vehicles, accordingly, interact with one another and exchange indispensable information in order to realize a number of safety and non-safety applications. Moreover, the proposed IoV-based simulator incorporates not only honest vehicles but also intelligent malicious ones that dynamically alternate between honest and dishonest behaviors while executing malicious acts to evade classification as threats by the IoV network.<br/><br/>
The proposed dataset comprises *79* vehicles engaging in a total of *96,707* interactions at different time instances. In total, we ascertained *9* trust parameter values, i.e., packet delivery rate, similarity, external similarity, internal similarity, familiarity, external familiarity, internal familiarity, reward/punishment, and context. These parameters not only depict the dynamic interactions among vehicles but also provide insights into the IoV network scenario within which the vehicles operate.<br/><br/>
**Trustor** - The trustor assumes the role of an evaluator within an IoV network to assess and ascertain the trustworthiness of a trustee. In our proposed dataset, there are *79* trustors listed in column *1* of the dataset.<br/><br/>
**Trustee** - The trustee, also referred to as a target node, is an entity that is evaluated by a trustor as either trustworthy or untrustworthy. In our proposed dataset, there are *79* trustees (listed in column *2* of the dataset) that have encountered *96,707* interactions with trustors. <br/><br/>
**Packet Delivery Rate (PDR)** - The Packet Delivery Rate (0=< PDR <=1) measures the degree of interaction between a trustor and a trustee at a time instance *t* within an IoV network, thereby providing a key understanding of their relationship (listed in column *3* of the dataset). <br/><br/>
**Similarity (Sim)** - The similarity (0=< Sim <=1) between a trustor and a trustee at a time instance *t* encompasses both external similarity (ES) and internal similarity (IS), and is a weighted amalgamation of the two, and is listed in column *4* of the dataset.<br/><br/>
**External Similarity (ES)** - The external similarity (0=< ES <=1) suggests the extent to which a trustor and a trustee access similar content at a time instance *t*, and is listed in column *5* of the dataset.<br/><br/>
**Internal Similarity (IS)** - The internal similarity (0=< IS <=1) manifests the degree of similarity in the positions (geographical locations), directions (travelling trajectories), speeds and accelerations of a trustor and trustee, and is depicted in column *6* of the dataset.<br/><br/>
**Familiarity (Fam)** - The familiarity (0=< Fam <=1) between a trustor and a trustee at a time instance *t* is also segregated into external familiarity (EF) and internal familiarity (IF), and is delineated in column *7* of the dataset.<br/><br/>
**External Familiarity (EF)** - The external familiarity (0=< EF <=1) quantifies the level of familiarity a trustor possesses towards a trustee, and is listed in column 
 *8* of the dataset. The value of EF is obtained by calculating the ratio between the number of common vehicles that interact with both trustor and trustee, and the total number of vehicles that interact with trustor over a given timestamp in an IoV network.<br/><br/>
**Internal Familiarity (IF)** - The internal familiarity (0=< IF <=1) denotes the extent of interaction frequency between trustor and trustee, and is recorded in column *9* of the dataset. <br/><br/>
**Reward / Punishment (RP)** - The reward and punishment (0=< RP <=1) is employed in order to ascertain the degree of a reward or a penalty allocated to a trustee *j* based on its conduct in an IoV network. Specifically, a trustee is rewarded by a trustor for exhibiting cooperation, honesty, and reporting critical events, whereas, is penalized for any sort of a misconduct, and is represented in column *10* of the dataset. <br/><br/>
**Context** - In the context (0=< context <=1) of this particular dataset, the context implies the network communication quality segregated into four classes implying poor, medium, good, and excellent, and is listed in column *11* of the dataset.<br/><br/>
# Partial Trust Values of the Trust Parameters
| Trustor | Trustee | Packet Delivery Rate  |Similarity | External Similarity| Internal Similarity |Familiarity | External Familiarity| Internal Familiarity |  Reward / Punishment | Context |
| :------: |  :----:  | :-------:| :------: | :----: | :------: |:------: | :----: | :-------: | :----: | :-------: |
|0|1|0.7182|0.2947|0|0.5894|0.1832|0.0061|0.3602|0.5418|0.4|
|0|10|0.4997|0.9072|1|0.8144|0.1134|0.0102|0.2166|0.3030|0.4|
|0|79|0.3513|0.7904|1|0.5808|0.1676|0.2353|0.0100|0.1836|0.0|
|.|.|.|.|.|.|.|.|.|.|.|
|5|9|0.4144|0.8706|1|0.7412|0.2788|0.0048|0.5529|0.2307|0.4|
|5|25|0.9578|0.2641|0|0.5282|0.2993|0.3474|0.2513|0.9182|0.6|
|5|65|0.6440|0.1237|0|0.2473|0.2774|0.4419|0.1138|0.4511|0.0|
|.|.|.|.|.|.|.|.|.|.|.|
|9|13|0.9377|0.1774|0|0.3548|0.5044|0.7887|0.2201|0.8810|0.6|
|9|37|0.2938|0.9444|1|0.8887|0.1269|0.1538|0.1000|0.1450|0.0|
|9|70|0.7108|0.8592|1|0.7184|0.1394|0.0556|0.2232|0.5323|0.4|
|.|.|.|.|.|.|.|.|.|.|.|
|17|20|0.9806|0.7351|1|0.4702|0.1819|0.0130|0.3508|0.9618|0.6|
|17|53|0.5914|0.2390|0|0.4781|0.2566|0.2292|0.2841|0.2930|0.0|
|17|59|0.4110|0.6918|1|0.3836|0.6316|0.9792|0.2841|0.2281|0.4|
|.|.|.|.|.|.|.|.|.|.|.|
|23|24|0.2439|0.8700|1|0.7400|0.5026|0.0052|1.0000|0.1145|0.4|
|23|61|0.5825|0.8982|1|0.7964|0.5500|1.0000|0.1000|0.3837|0.6|
|23|70|0.9638|0.1538|0|0.3075|0.3650|0.3784|0.3516|0.9295|0.6|
|.|.|.|.|.|.|.|.|.|.|.|
|27|40|0.8577|0.6657|1|0.3315|0.3207|0.0217|0.6196|0.7439|0.6|
|27|51|0.4107|0.6545|1|0.3089|0.3468|0.0200|0.6735|0.2278|0.4|
|27|74|0.5847|0.2025|0|0.4049|0.5444|0.5500|0.5388|0.3860|0.4|
|.|.|.|.|.|.|.|.|.|.|.|
|35|36|0.7220|0.8575|1|0.7419|0.1588|0.0202|0.2973|0.5468|0.4|
|35|37|0.9416|0.8973|1|0.7946|0.6115|0.4423|0.7807|0.8882|0.8|
|35|54|0.9183|0.8915|1|0.7830|0.1700|0.0187|0.3213|0.8463|0.6|
|.|.|.|.|.|.|.|.|.|.|.|
|50|52|0.2239|0.9414|1|0.8828|0.5048|0.0095|1.0000|0.1030|0.4|
|50|55|0.1016|0.8203|1|0.6406|0.6261|0.2530|1.0000|0.0414|0.0|
|50|62|0.9081|0.2947|0|0.5895|0.3864|0.4412|0.3317|0.8284|0.6|
|.|.|.|.|.|.|.|.|.|.|.|
|54|57|0.9246|0.9541|1|0.9081|0.5018|0.0036|1.0000|0.8575|0.8|
|54|61|0.1046|0.9062|1|0.8125|0.2122|0.0244|0.4000|0.0427|0.0|
|54|75|0.9722|0.7467|1|0.4928|0.1263|0.0476|0.2049|0.9455|0.6|
|.|.|.|.|.|.|.|.|.|.|.|
|60|61|0.6625|0.8816|1|0.7632|0.5071|0.0143|1.0000|0.4727|0.6|
|60|63|0.8160|0.1725|0|0.3449|0.3867|0.5152|0.2583|0.6789|0.4|
|60|66|0.9271|0.8837|1|0.7674|0.6660|0.3312|1.0000|0.8619|0.8|
|.|.|.|.|.|.|.|.|.|.|.|
|63|65|0.4089|0.8385|1|0.6769|0.5102|0.0204|1.0000|0.2264|0.4|
|63|67|0.9368|0.7212|1|0.4423|0.7564|0.5128|1.0000|0.8794|0.8|
|63|74|0.2897|0.8995|1|0.7995|0.3124|0.3750|0.2497|0.1424|0.4|
|.|.|.|.|.|.|.|.|.|.|.|
|70|71|0.5324|0.7289|1|0.4577|0.1137|0.0769|0.1505|0.3336|0.4|
|70|73|0.8472|0.7249|1|0.4479|0.4321|0.4706|0.3937|0.7272|0.6|
|70|75|0.2005|0.1383|0|0.2766|0.3134|0.4375|0.1853|0.0901|0.0|
|.|.|.|.|.|.|.|.|.|.|.|
|74|73|0.7138|0.7448|1|0.4896|0.3000|0.5000|0.1000|0.5361|0.4|
|74|77|0.8586|0.7843|1|0.5685|0.5304|0.0833|0.9775|0.7454|0.6|
|74|78|0.6516|0.2984|0|0.5969|0.7528|0.5056|1.0000|0.4559|0.4|
# Related Paper(s)
1. Wang Y, Mahmood A, Sabri MFM, Zen H, Kho LC. MESMERIC: Machine Learning-Based Trust Management Mechanism for the Internet of Vehicles. *Sensors*. 2024; 24(3):863.



