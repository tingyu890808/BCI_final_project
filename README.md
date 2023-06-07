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
