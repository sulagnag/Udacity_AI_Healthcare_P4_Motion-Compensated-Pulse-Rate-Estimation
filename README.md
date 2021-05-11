# Udacity_AI_Healthcare_P4_Motion-Compensated-Pulse-Rate-Estimation
Estimate heart rate in BPM from motion compensated PPG data

## The problem desctiption
This project has 2 main parts.

1. Develop a Pulse Rate Algorithm on the given training data. Then Test Your Algorithm and see that it has met the success criteria.
2. Apply the Pulse Rate Algorithm on a Clinical Application and compute more clinically meaningful features and discover healthcare trends.

## PPG signal
The heart beating is not the only phenomenon that modulates the PPG signal. Blood in the wrist is fluid, and arm movement will cause the blood to move correspondingly. During exercise, like walking or running, we see another periodic signal in the PPG due to this arm motion. Our pulse rate estimator has to be careful not to confuse this periodic signal with the pulse rate.

## The Data
Two-channel PPG signals, three-axis acceleration signals, and one-channel ECG signals were simultaneously recorded from subjects with age from 18 to 35. For each subject, the PPG signals were recorded from wrist by two pulse oximeters with green LEDs (wavelength: 515nm). Their distance (from center to center) was 2 cm. The acceleration signal was also recorded from wrist by a three-axis accelerometer. Both the pulse oximeter and the accelerometer were embedded in a wristband, which was comfortably worn. The ECG signal was recorded simultaneously from the chest using wet ECG sensors. All signals were sampled at 125 Hz and sent to a nearby computer via Bluetooth.

Each dataset with the similar name 'DATA_01_TYPE01' contains a variable 'sig'. It has 6 rows. The first row is a simultaneous recording of ECG, which is recorded from the chest of each subject. The second row and the third row are two channels of PPG, which are recorded from the wrist of each subject. The last three rows are simultaneous recordings of acceleration data (in x-, y-, and z-axis). During data recording, each subject ran on a treadmill with changing speeds. For datasets with 
names containing 'TYPE01', the running speeds changed as follows:

 rest(30s) -> 8km/h(1min) -> 15km/h(1min) -> 8km/h(1min) -> 15km/h(1min) -> rest(30s)
For datasets with names containing 'TYPE02', the running speeds changed as follows:
 rest(30s) -> 6km/h(1min) -> 12km/h(1min) -> 6km/h(1min) -> 12km/h(1min) -> rest(30s) 

For each dataset with the similar name 'DATA_01_TYPE01', the ground-truth of heart rate can be
calculated from the simultaneously recorded ECG signal (i.e. the first row of the variable 'sig'). For
convenience, we also provide the calculated ground-truth heart rate, stored in the datasets with the
corresponding name, say 'REF_01_TYPE01'. In each of this kind of datasets, there is a variable 'BPM0',
which gives the BPM value in every 8-second time window. Note that two successive time windows
overlap by 6 seconds. Thus the first value in 'BPM0' gives the calcualted heart rate ground-truth in
the first 8 seconds, while the second value in 'BPM0' gives the calculated heart rate ground-truth
from the 3rd second to the 10th second. 

## Citations and copyright
All datasets have copyrights. But you can freely use them for the Signal Processing Cup or your own academic research, as long as you suitably cite the data in your works. Please do not cite this competition website, because it may not be available after this competition. Instead, please cite the following paper, since all training datasets come from it:
Z. Zhang, Z. Pi, B. Liu, TROIKA: A general framework for heart rate monitoring using wrist-type photoplethysmographic signals during intensive physical exercise, IEEE Transactions on Biomedical Engineering, vol. 62, no. 2, pp. 522-531, February 2015, DOI: 10.1109/TBME.2014.2359372 
