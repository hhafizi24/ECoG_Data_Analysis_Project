Overview: This project explores the neural dynamics of finger movements using electrocorticography (ECoG) data collected from a human patient. The analysis involves various techniques, including time-domain analysis, frequency-domain analysis, event-related potentials (ERP), autocorrelation, and phase-amplitude coupling.

Ethics statement: All patients participated in a purely voluntary manner, after providing informed written consent, under experimental protocols approved by the Institutional Review Board of the University of Washington (#12193). All patient data was anonymized according to IRB protocol, in accordance with HIPAA mandate. These data originally appeared in the manuscript “Human Motor Cortical Activity Is Selectively Phase- Entrained on Underlying Rhythms” published in PLoS Computational Biology in 2012 [Reference].

Task: During the finger movement task, subjects were cued with a word displayed on a bedside monitor indicating which finger to move during 2- second movement trials. The subject performed self-paced movements in response to each of these cues, and they typically moved each finger 2–5 times during each trial, but some trials included many more movements. A 2-second rest trial (blank screen) followed each movement trial. There were 30 movement cues for each finger, and trials were interleaved randomly. Finger positions were recorded using a 5 degree-of-freedom dataglove sensor (5 dt, Irvine, CA). 

The basic datafiles (in MATLAB format) are named “##_fingerflex.mat” in the folder data/##, where ## denotes the 2 letter patient code.

Each datafile has 7 variables, the ones used in this project are:

"elec_regions" (number of channels x 1): A numerical code for the anatomical location of the associated channel. The code is as follows:
1 – dorsal M1
3 – dorsal S1
4 – ventral sensorimotor (M1+ S1) 
6 – frontal (non-rolandic) 
7 – parietal (non-rolandic)
8 – temporal 
9 – occipital

 "data" (time x number of channels): These are the data.
-	sampled at 1000Hz
-	scale factor: 1 amplifier unit = .0298 microvolts
-	built-in band pass 0.15 to 200 Hz, 
		- but a 1 pole band pass, so there is no sharp corner at 200Hz. 
		-The amplitude roll-off function is in the file “ns_1k_1_300_filt.mat”

"cue" (time x 1): Screen cue. This is the cue on the screen at each point in time (note that this might be different than the actual behavior). 
0 – Inter-stimulus interval
1 – thumb
2 – index finger
3 – middle finger 
4 – ring finger
5 – little finger


There is an additional file, are named “##_stim.mat” in the folder data/##, where ## denotes the 2 letter patient code. This file contains a variable “stim”, which are labeled epochs encasing the actual movement types. The code is as follows:
0 – Inter-stimulus interval
1 – thumb
2 – index finger
3 – middle finger 
4 – ring finger
5 – little finger


Data:
This project uses an open dataset from the Stanford Libraries, the link to the dataset is below. https://exhibits.stanford.edu/data/catalog/zk881ps0522
  
Analysis Steps:
1. Data Preprocessing:
   - ECoG data cleaning, filtering, and epoch extraction.

2. Time-Domain Analysis:
   - Visualized neural signals in the time domain, showcasing cue-related delays and finger-specific movement patterns.

3. Frequency-Domain Analysis:
   - Utilized time-frequency analysis to examine spectral dynamics during finger movements.

4. Event-Related Potentials (ERP):
   - Conducted ERP analysis to investigate distinct neural responses for each finger movement task.

5. Autocorrelation:
   - Explored temporal relationships across electrodes through autocorrelation analysis.

6. Phase-Amplitude Coupling:
   - Investigated theta-gamma coupling, demonstrating the orchestrated interplay of theta and gamma oscillations.

