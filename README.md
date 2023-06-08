# BCI_final_project-slapjack
An EEG Hyperscanning study creat by Hao-Che (Howard) Hsu

# Experimental Environment

* Software based on [Unity](https://unity.com/cn) and [labstreaminglayer](https://github.com/sccn/labstreaminglayer)
* Using [Tobii eye tracker 5](https://gaming.tobii.com/product/eye-tracker-5/) as eye tracker
* Brainproduct [BrainAmp](https://www.brainproducts.com/solutions/brainamp/) as EEG device

# Experimental paradigms

* There are two sessions and three modes
    * Keyboard Session
    * Gaze Session

* **Both session have**
  * Single mode
  * Collaborative mode
  * Competitive mode

# Data processing
* Merged three modes .xdf files
* Separate the EEG signals of two people and two sessions
* Band-pass filter (1~50Hz)
* Resampple (1000 -> 250 Hz)
* Re-referece (TP9, TP10)
* ASR (k = 20)
* ICA
* ICLabel (keep brain and others)
* Extract epoch Keyboard session (-0.3 ~ 1.2s), Gaze session (-3 ~ 10s)

# ICA components (use ICLabel to classify)
<img width="808" alt="image" src="https://github.com/tingyu890808/BCI_final_project/assets/120452235/e13541ad-0c8d-4b6e-a617-69d7eca71e14">

# Literature review

   It is well known that "cooperation" and "competition" are common in hyperscanning research. Cooperation interaction occurs when individuals or groups collaborate and pool their efforts to achieve common goals. Our study also involves related content. The article titled "Hyperscanning: a valid method to study neural inter-brain underpinnings of social interaction" by A. Czeszumski et al. published in the journal "Frontiers in Human Neuroscience" in 2020 explores hyperscanning as a valid method for studying the neural mechanisms of social interaction. The article highlights that hyperscanning allows simultaneous measurement of brain activity from multiple individuals, enabling the investigation of real-time dynamic relationships between their brains. The significant advantage of hyperscanning is its ability to examine the internal and inter-brain neural relationships between two or more interacting brains. This technique provides a new approach to address the complexity of joint action, including its spontaneity, reciprocity, and multimodality, which pose significant challenges to neuroscience research. These findings are highly relevant to our study as we have a project specifically focused on exploring multi-brain neural activity.
   
   Since we are aware that our research involves the presence of two participants simultaneously, it is necessary to consider the interaction between different individuals. This article, titled "Analysis of the changes in communication and social interactions during the transformation of a traditional team into an agile team," was published in 2018 by I. E. Espinosa‐Curiel, J. Rodríguez‐Jacobo, E. Vázquez‐Alfaro, J. A. Fernández‐Zepeda, and D. Fajardo‐Delgado in the journal "Journal of Software: Evolution and Process." The authors investigated and analyzed the changes in communication and social interactions that occur during the transformation of a traditional team into an agile team. By observing and documenting the team's transformation process, the authors explored the impact of the agile team transformation on communication and social interactions among team members. Qualitative and quantitative methods were used to collect and analyze data, and by comparing team interactions at different stages, patterns and trends of change were revealed. The findings contribute to understanding the dynamic nature of interpersonal interactions during team transformations and provide guidance and recommendations for organizations implementing agile methods.
   
   Furthermore, it is necessary to combine the interaction between individuals with electroencephalogram (EEG). Therefore, this article, co-authored by M. Balconi and G. Fronda, was published in the journal "Culture and Brain" in 2022. Titled "Inter-brain EEG connectivity in hyperscanning for Italian and French gestures: the culture-related nonverbal language," the article explores the application of hyperscanning technique in studying the culture-related nonverbal communication of Italian and French gestures. The study utilized EEG hyperscanning method to investigate inter-brain connectivity during nonverbal communication between individuals. The research focused on gesture expressions in Italian and French cultures and explored the differences and similarities in nonverbal communication between different cultures. It is worth noting that during the experiment, participants engage in both verbal and nonverbal communication. For example, eye contact and gestures are common forms of nonverbal communication in social interactions, especially in hyperscanning studies. Therefore, exploring these factors is inevitable, and the integration of communication, gestures, and EEG activity in this article provides valuable insights and assistance for our research.

# Results
<img width="900" alt="image" src="https://github.com/tingyu890808/BCI_final_project/assets/120452235/805525fb-674a-471d-afd8-abd2dce4026c">

<img width="900" alt="image" src="https://github.com/tingyu890808/BCI_final_project/assets/120452235/c6ebf91e-3500-4164-a237-c0ea6a428235">

<img width="900" alt="image" src="https://github.com/tingyu890808/BCI_final_project/assets/120452235/a186af7d-bc1f-414c-ac14-c6ae5aa6b64d">

<img width="900" alt="image" src="https://github.com/tingyu890808/BCI_final_project/assets/120452235/ddbb65b6-bb14-4ec4-86f1-546b22433078">

<img width="900" alt="image" src="https://github.com/tingyu890808/BCI_final_project/assets/120452235/cd13da0d-78f2-4009-8fb5-33ffdb1d0206">
