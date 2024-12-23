# DDMSL
The official code for DDSML.

Please enter this link to download the dataset and extract it into the DDMSL main folder: 
https://pan.baidu.com/s/1AZtwXE6fC7ZIET3yDu--Ug?pwd=x59d Extract code: x59d 

Due to the large size of the dataset, we will update other datasets later.

——————————————————————————————————————————————————————————————————————————————————————————————————————————————
File Structure：

——————————————————————————————DDMSL-main

——————————————-----dataset

——————————————-----model

——————————————-----model.py

——————————————-----model_test.py

——————————————-----SIR_train_release.py

——————————————-----Dll1.dll

———————————————————————————————————————————————————————————————————————————————————————————————————————————————

Dll1. DLL is a dynamic link library used to generate state transition matrices and can only run in the Windows environment.


Please run SIR_train_release.py first, the trained model will be stored in the model folder. And in the model_ Modify the corresponding file path in tset.py for testing.


2024.12.23
I have noticed the issue regarding DLL files and I apologize for any inconvenience caused during the reproduction.


The function of a DLL file is to input: the duration of each infection iteration (T), infection rate, recovery rate, number of runs, adjacency matrix, number of nodes, initial infected nodes (List), initial infected nodes, and number of parallel threads. Output a matrix of NX3, where N is the number of nodes and 3 represents the state probabilities of SIR.

Logic is to simulate the SIR process m times on the adjacency matrix aj, and calculate the frequency of each node in the SIR state during m times to approximate the probability of SIR state. The matrix will be saved as output. txt.


If necessary, please generate an output. txt according to the above logic. The source code for this section could not be saved due to work changes, and I will provide a version of this code in the future.
