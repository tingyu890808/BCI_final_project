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

# Video of data preprocessing
https://youtu.be/osBCvM-am-k

# The calculation of the mental workload
We used the band power of θ band of Fz and α band of Pz ratio.

# Literature review

* Literature related to hyperscanning
    * The article "Hyperscanning: a valid method to study neural inter-brain underpinnings of social interaction," published in 2020, discusses hyperscanning as an effective method for studying the neural mechanisms of social interaction. It elaborates on the applications and advantages of hyperscanning in studying social interaction. This article has provided us with valuable insights as our experiment also involves simultaneously recording the brain activity of multiple individuals.
    
    * The article "Hyperscanning neuroimaging technique to reveal the 'two-in-one' system" published in 2015, focuses on the application of hyperscanning techniques in studying the "two-in-one" system in social interactions. The authors believe that hyperscanning provides a unique method to understand the neural mechanisms of social interaction and reveal real-time dynamics of information exchange between individuals. This article has provided us with useful references for our experiment.
    
    * The article "Hyperscanning: simultaneous fMRI during linked social interactions," published in 2002, emphasizes the simultaneous acquisition of functional magnetic resonance imaging (fMRI) data from multiple individuals engaged in social interaction. The authors describe the technical aspects and experimental setup of their hyperscanning research, specifically studying brain activity during economic exchange games. As our experiment also involves observing participants' brain activity during game-playing, this article serves as a valuable reference.
    
    From an academic perspective, these articles collectively contribute to our understanding of hyperscanning as a valuable tool for studying dynamic neural processes during social interaction. For us, they highlight the importance of real-time measurement and the need for rigorous analysis and interpretation of hyperscanning data. These articles serve as excellent examples for our experiment.

*Communication during interaction
    *The article "Electrophysiological Indicators of Brain Activity in the Process of Verbal and Non-Verbal Communication during the Dialogue," published in 2019, discusses the electrophysiological indicators of brain activity during verbal and non-verbal communication in order to study the neural mechanisms underlying communication processes. This article contributes to our understanding of the neurophysiological basis of interpersonal communication and highlights the importance of considering both verbal and non-verbal communication in research and practical settings.
    *The article "Inter-brain EEG connectivity in hyperscanning for Italian and French gestures: the culture-related nonverbal language," published in 2022, explores the application of hyperscanning technology in studying culture-related non-verbal communication through Italian and French gestures. The study focuses on the expression of gestures in Italian and French cultures, which are essential actions during participant interactions. Therefore, this article provides us with valuable insights when observing participants in our study.
    *The article "Face-to-face vs. remote digital settings in job assessment interviews: A multilevel hyperscanning protocol for the investigation of interpersonal attunement," published in 2022, compares face-to-face and remote digital settings in job assessment interviews and utilizes a multilevel hyperscanning protocol to study interpersonal attunement. It provides insights into the differences in coordination and brain activity between face-to-face and remote environments, which are helpful for our research on interpersonal coordination in face-to-face settings.
    
    These articles contribute to the field of interpersonal communication by applying neuroscience techniques to study the process. They highlight the value of understanding the neural mechanisms of communication and have provided assistance in the design of our experiments by emphasizing different modes of communication.

# Results

We used Kfold(k = 10) to apply different models(LDA, Adaboost, Bagging, Random Forest, SVM),and repeated 10 times. Last, we averaged the confusion matrix and the accuracy score of each times.

First, we used the ERP data to classify.
0 respesent the "player" of **single mode** ; while 1 represent the "observer" of **single mode**.

<img width="900" alt="image" src="https://github.com/tingyu890808/BCI_final_project/assets/120452235/805525fb-674a-471d-afd8-abd2dce4026c">

<img width="900" alt="image" src="https://github.com/tingyu890808/BCI_final_project/assets/120452235/f4ca57e0-7fe5-4179-bb20-5310db4bbf12">

<img width="900" alt="image" src="https://github.com/tingyu890808/BCI_final_project/assets/120452235/a186af7d-bc1f-414c-ac14-c6ae5aa6b64d">

<img width="900" alt="image" src="https://github.com/tingyu890808/BCI_final_project/assets/120452235/ddbb65b6-bb14-4ec4-86f1-546b22433078">

<img width="900" alt="image" src="https://github.com/tingyu890808/BCI_final_project/assets/120452235/cd13da0d-78f2-4009-8fb5-33ffdb1d0206">

Second, we used the mental workload data to classify.

<img width="900" alt="image" src="https://github.com/tingyu890808/BCI_final_project/assets/120452235/45056ae5-a669-404b-96dd-5f4b760c181e">

<img width="900" alt="image" src="https://github.com/tingyu890808/BCI_final_project/assets/120452235/92cf1792-05f9-4020-96af-3d7525521155">

<img width="900" alt="截圖 2023-06-09 下午2 06 41" src="https://github.com/tingyu890808/BCI_final_project/assets/120452235/7569bdf5-f5d9-42bd-bd30-895f90fa3cae">

<img width="900" alt="image" src="https://github.com/tingyu890808/BCI_final_project/assets/120452235/40775996-71eb-4c09-8a9a-da107fdb167f">

<img width="900" alt="image" src="https://github.com/tingyu890808/BCI_final_project/assets/120452235/ef535168-f24d-4d0b-9b1e-cbe7b301196a">
