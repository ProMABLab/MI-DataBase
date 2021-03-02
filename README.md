# MI-OpenBCI

This data set consists of electroencephalography (EEG) signals from 10 healthy subjects of a study published [here]( https://www.sciencedirect.com/science/article/pii/S240584402030270X).
The participants had no previous BCI experience. 
The BCI protocol consisted of two conditions, namely the kinesthetic imagination of grasping movement of the dominant hand and rest/idle condition.

    ID  Gender  Age  Dominant Hand
    S02  Male    28   Right 
    S03  Female  29   Right 
    S04  Male    30   Right 
    S05  Male    29   Right 
    S06  Male    30   Right 
    S07  Female  20   Right 
    S08  Male    25   Right 
    S09  Female  28   Right 
    S10  Female  22   Right 
    S12  Male    20   Right 
    mean age +/- SD 26.1 +/- 4

Description of data files:
The EEG data are stored in Matlab’s .mat-file format, one file per subject. Each file comprises a “DataEEG” struct array which contains the four fields detailed below:

    - DataEEG.x: 4 s filtered EEG data matrix (number of samples [501] × number of channels [15] × number of trials [160]). 
                 Note that due to technical problems for subject S01 one run was shorter yielding a total of 150 trials.
    - DataEEG.y: class labels vector (number of trials × 1), being 1 for MI class and 2 for RELAX.
    - DataEEG.s: sampling frequency [125].
    - DataEEG.c: channel names description (1 × number of channels)

For a detailed description: [here](https://github.com/MI-DataBase/MI-OpenBCI/blob/main/MI_Open_BCI_Dataset_Description.pdf)
