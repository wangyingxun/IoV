# Internet of Vehicles
The Internet of Vehicles (IoV) is an application of the Internet of Things (IoT) in the context of Intelligent Transportation Systems (ITS). The IoV has a similar architecture to the IoT and features a hierarchical structure that includes data source, edge, fog, and the cloud layers. Vehicles share information with other vehicles, pedestrians, intelligent roadside infrastructure, and backbone networks to establish vehicle-to-vehicle, vehicle-to pedestrian, vehicle-to-infrastructure, and vehicle-to-network communication, thereby formulating vehicle-to-everything (V2X) communication. Figure 1 portrays an IoV landscape. 


<figure>
  <div style="text-align:center;">
  <img
  src="fig1.png"
  alt="An IoV landscape."
  width="500"  >
  <figcaption>Figure 1:  An IoV landscape.</figcaption>
  </div>
</figure>

# Trust in the Internet of Vehicles
Due to the unique characteristics of IoV, i.e., openness, dynamic topology, and high mobility, it is susceptible to attacks; dishonest entities can modify legitimate security messages, spread forged information, or delay forwarding messages, thereby endangering human lives. Accordingly, researchers have proposed several solutions for handling the issues pertinent to IoV security. Nevertheless, a number of these solutions rely on conventional cryptographic-related schemes and, therefore, rely on the notions of digital signatures, certificates, and public key infrastructure. Moreover, conventional cryptographicrelated schemes are only capable of mitigating external attacks and are ineffective against internal network attacks. It is due to this reason that the paradigm of trust has been recently introduced in the research literature. Trust is generally referred to as the confidence of a trustor in a trustee. Here, trustor refers to a node that is in a position to ascertain the trust of the other node (trustee) in the network, whereas the trustee refers to a node whose trust is being ascertained. In the context of the proposed dataset, trust refers to the likelihood that a trustee can perform a particular operation within a specific situation at a specific time. It is also important to mention that trust computation primarily involves a weighted aggregation of both the direct trust and the indirect trust. Direct trust is ascertained as a result of direct interactions between a trustor and a trustee and is generally referred to as a trustor’s direct observation of a trustee. On the contrary, indirect trust is computed by taking into account the direct trust ascertained by the one-hop neighbors of a trustor pertinent to a trustee.<br/><br/>
# Data Description
The envisaged trust-based IoV dataset employs Java for designing an IoV-based simulator, whereas, Python for analyzing the simulation results. The traces in this particular dataset transpired as a result of a simulation carried out for a duration of *1* hour via the IoV-based simulator. The IoV simulator takes into account several interconnected road segments in order to mimic a road network encompassing vehicles traversing at random speeds in disparate directions. Vehicles, accordingly, interact with one another and exchange indispensable information in order to realize a number of safety and non-safety applications. Moreover, the proposed IoV-based simulator incorporates not only honest vehicles but also intelligent malicious ones that dynamically alternate between honest and dishonest behaviors while executing malicious acts to evade classification as threats by the IoV network.<br/><br/>
The proposed dataset comprises *79* vehicles engaging in a total of *96,707* interactions at different time instances. In total, we ascertained *9* trust parameter values, i.e., packet delivery ratio, similarity, external similarity, internal similarity, familiarity, external familiarity, internal familiarity, reward/punishment, and context. These parameters not only depict the dynamic interactions among vehicles but also provide insights into the IoV network scenario within which the vehicles operate.<br/><br/>
**Trustor** - The trustor assumes the role of an evaluator within an IoV network to assess and ascertain the trustworthiness of a trustee. In our proposed dataset, there are *79* trustors listed in column *1* of the dataset.<br/><br/>
**Trustee** - The trustee, also referred to as a target node, is an entity that is evaluated by a trustor as either trustworthy or untrustworthy. In our proposed dataset, there are *79* trustees (listed in column *2* of the dataset) that have encountered *96,707* interactions with trustors. <br/><br/>
**Packet Delivery Ratio (PDR)** - The Packet Delivery Ratio (0=< PDR <=1) measures the degree of interaction between a trustor and a trustee at a time instance *t* within an IoV network, thereby providing a key understanding of their relationship (listed in column *3* of the dataset). <br/><br/>
**Similarity (Sim)** - The similarity (0=< Sim <=1) between a trustor and a trustee at a time instance *t* encompasses both external similarity (ES) and internal similarity (IS), and is a weighted amalgamation of the two, and is listed in column *4* of the dataset.<br/><br/>
**External Similarity (ES)** - The external similarity (0=< ES <=1) suggests the extent to which a trustor and a trustee access similar content at a time instance *t*, and is listed in column *5* of the dataset.<br/><br/>
**Internal Similarity (IS)** - The internal similarity (0=< IS <=1) manifests the degree of similarity in the positions (geographical locations), directions (travelling trajectories), speeds and accelerations of a trustor and trustee, and is depicted in column *6* of the dataset.<br/><br/>
**Familiarity (Fam)** - The familiarity (0=< Fam <=1) between a trustor and a trustee at a time instance *t* is also segregated into external familiarity (EF) and internal familiarity (IF), and is delineated in column *7* of the dataset.<br/><br/>
**External Familiarity (EF)** - The external familiarity (0=< EF <=1) quantifies the level of familiarity a trustor possesses towards a trustee, and is listed in column 
 *8* of the dataset. The value of EF is obtained by calculating the ratio between the number of common vehicles that interact with both trustor and trustee, and the total number of vehicles that interact with trustor over a given timestamp in an IoV network.<br/><br/>
**Internal Familiarity (IF)** - The internal familiarity (0=< IF <=1) denotes the extent of interaction frequency between trustor and trustee, and is recorded in column *9* of the dataset. <br/><br/>
**Reward / Punishment (RP)** - The reward and punishment (0=< RP <=1) is employed in order to ascertain the degree of a reward or a penalty allocated to a trustee *j* based on its conduct in an IoV network. Specifically, a trustee is rewarded by a trustor for exhibiting cooperation, honesty, and reporting critical events, whereas, is penalized for any sort of a misconduct, and is represented in column *10* of the dataset. <br/><br/>
**Context** - In the context (0=< Context <=1) of this particular dataset, the context implies the network communication quality segregated into four classes implying poor, medium, good, and excellent, and is listed in column *11* of the dataset.<br/><br/>
# A snapshot of values pertinent to the trust parameters
| Trustor | Trustee | Packet Delivery Ratio  |Similarity | External Similarity| Internal Similarity |Familiarity | External Familiarity| Internal Familiarity |  Reward / Punishment | Context |
| :------: |  :----:  | :-------:| :------: | :----: | :------: |:------: | :----: | :-------: | :----: | :-------: |
|0|1|0.7113|0.6833|1|0.3666|0.6801|1.0000|0.3602|0.5329|0.6|
|0|10|0.9625|0.9047|1|0.8094|0.6083|1.0000|0.2166|0.9271|0.8|
|0|78|0.7849|0.2117|0|0.4235|0.6138|1.0000|0.2276|0.6330|0.4|
|.|.|.|.|.|.|.|.|.|.|.|
|5|9|0.7617|0.7646|1|0.5292|0.7765|1.0000|0.5529|0.6002|0.6|
|5|25|0.1275|0.7946|1|0.5892|0.6257|1.0000|0.2513|0.0533|0.4|
|5|65|0.9199|0.7658|1|0.5315|0.5569|1.0000|0.1138|0.8491|0.6|
|.|.|.|.|.|.|.|.|.|.|.|
|9|10|0.7832|0.4056|0|0.8112|1.0000|1.0000|1.0000|0.6305|0.6|
|9|37|0.1610|0.9599|1|0.9199|0.5500|1.0000|0.1000|0.0696|0.4|
|9|70|0.4428|0.8090|1|0.6581|0.6116|1.0000|0.2232|0.2536|0.4|
|.|.|.|.|.|.|.|.|.|.|.|
|17|21|0.2089|0.4289|0|0.8578|0.9807|1.0000|0.9614|0.0947|0.4|
|17|53|0.8233|0.7468|1|0.4935|0.6421|1.0000|0.2841|0.6900|0.6|
|17|59|0.6767|0.6915|1|0.3830|0.6421|1.0000|0.2841|0.4898|0.6|
|.|.|.|.|.|.|.|.|.|.|.|
|23|24|0.9312|0.8760|1|0.7519|1.0000|1.0000|1.0000|0.8693|0.8|
|23|67|0.3746|0.2880|0|0.5760|0.7328|1.0000|0.4656|0.2004|0.0|
|23|70|0.8733|0.7228|1|0.4456|0.6758|1.0000|0.3516|0.7694|0.6|
|.|.|.|.|.|.|.|.|.|.|.|
|27|40|0.9835|0.8466|1|0.6933|0.8098|1.0000|0.6196|0.9674|0.8|
|27|53|0.3995|0.1174|0|0.2348|0.7963|1.0000|0.5926|0.2191|0.0|
|27|74|0.7684|0.7259|1|0.4519|0.7694|1.0000|0.5388|0.6095|0.6|
|.|.|.|.|.|.|.|.|.|.|.|
|35|36|0.7692|0.1149|0|0.2298|0.6486|1.0000|0.2973|0.6107|0.4|
|35|37|0.5302|0.8996|1|0.7993|0.8904|1.0000|0.7807|0.3314|0.6|
|35|54|0.1979|0.7465|1|0.4929|0.6607|1.0000|0.3213|0.0887|0.4|
|.|.|.|.|.|.|.|.|.|.|.|
|50|52|0.4822|0.7346|1|0.4692|1.0000|1.0000|1.0000|0.2873|0.6|
|50|55|0.5339|0.8764|1|0.7527|1.0000|1.0000|1.0000|0.3350|0.6|
|50|62|0.7857|0.8393|1|0.6785|0.6659|1.0000|0.3317|0.6341|0.6|
|.|.|.|.|.|.|.|.|.|.|.|
|54|57|0.6790|0.8617|1|0.7237|1.0000|1.0000|1.0000|0.4926|0.6|
|54|61|0.5491|0.8709|1|0.7417|0.7000|1.0000|0.4000|0.3498|0.6|
|54|75|0.3732|0.6680|1|0.3360|0.6025|1.0000|0.2049|0.1944|0.4|
|.|.|.|.|.|.|.|.|.|.|.|
|60|61|0.6867|0.9094|1|0.8187|1.0000|1.0000|1.0000|0.5250|0.6|
|60|63|0.4465|0.8510|1|0.7020|0.6292|1.0000|0.2583|0.2567|0.4|
|60|75|0.3603|0.9066|1|0.8131|0.6722|1.0000|0.3444|0.1900|0.4|
|.|.|.|.|.|.|.|.|.|.|.|
|63|65|0.8792|0.7572|1|0.5145|1.0000|1.0000|1.0000|0.7792|0.8|
|63|67|0.6562|0.7231|1|0.4462|1.0000|1.0000|1.0000|0.4653|0.6|
|63|74|0.4972|0.9154|1|0.8307|0.6249|1.0000|0.2497|0.3007|0.4|
|.|.|.|.|.|.|.|.|.|.|.|
|70|71|0.5665|0.7666|1|0.5332|0.5753|1.0000|0.1505|0.3672|0.4|
|70|73|0.5879|0.7530|1|0.5059|0.6969|1.0000|0.3937|0.3893|0.6|
|70|76|0.9644|0.1530|0|0.3060|0.9343|1.0000|0.8685|0.9307|0.6|
|.|.|.|.|.|.|.|.|.|.|.|
|74|75|0.1220|0.7480|1|0.4960|0.5500|1.0000|0.1000|0.0507|0.0|
|74|77|0.5229|0.7413|1|0.4826|0.9888|1.0000|0.9775|0.3245|0.6|
|74|78|0.2091|0.7263|1|0.4526|1.0000|1.0000|1.0000|0.0948|0.4|
# Related Paper(s)
1. Wang Y, Mahmood A, Sabri MFM, Zen H, Kho LC. MESMERIC: Machine Learning-Based Trust Management Mechanism for the Internet of Vehicles. *Sensors*. 2024; 24(3):863.



