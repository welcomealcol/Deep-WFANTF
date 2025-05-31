1.	Download the package from Baidu Cloud and unzip it:
Link：https://pan.baidu.com/s/1-FISC8f2qd7EaaY_1TuhiQ?pwd=nx1t
Code：nx1t
Multi.rar ---ADHD
Deep WSANTF.rar---Abide
2.	Before running the program, please make sure the following software is installed(requirement.txt):
[1].	CUDA Compilation Tools: Release 11.1, V11.1.74
Build: cuda_11.1.relgpu_drvr455TC455_06.29069683_0
[2].	JDK: 1.8.0_202
[3].	Python Version: 3.8.7
[4].	TensorFlow Version: 2.4.3
[5].	tkinter
[6].	pandas Version: 1.2.1
[7].	matplotlib Version: 3.5.2
[8].	Keras Version: 2.4.3
[9].	nibabel Version: 3.2.1
[10].	PIL (Pillow) Version: 8.4.0
[11].	SimpleITK Version: 2.1.1
[12].	scipy Version: 1.7.1
[13].	numpy Version: 1.19.5
[14].	scikit-learn Version: 1.0.1
[15].	hyperopt Version: 0.2.5
[16].	scikit-multilearn (skmultilearn)
3.	Please place the MRI data in the dist/rawdata/data directory, and the corresponding diagnostic information in the dist/participants.tsv file.
Note:
[1].	The participant_id must be in the second column, and
[2].	The dx_group (diagnostic group) must be in the fourth column.
All other columns are irrelevant and will not be used.
4.	Double click Deep_WSANTF.exe and wait to finish (about several hours)
 
Go into the path: “dist\processed_Deep_WSANTF”, which contains the extracted factor matrices.
5.	Open the CMD, go into the folder which contains the Deep_WSANTF.jar file, and run the following java command:
 
java -jar Deep_WSANTF.jar com.alcol.BuildDataset
Go into the path: “dist\processed_Deep_WSANTF”, you can find the four files: rows.csv, columns.csv, zs.csv and ncs.csv
Note: the version of jar file for multi-class-labels should be “Deep_WSANTF_mult.jar” and “dist/multi”. The executing way follows the same way with “single”. Please place the ADHD data in this directory and ensure that the file naming is consistent with that of "Abide".
6.	Copy the file “kerasmulti_final_5fold.py” to the folder: “dist\processed_Deep_WSANTF”, and run it:
Python kerasmulti_final_5fold.py
Note: you can run this test script for ABIDE (BNI: in “dist\processed_Deep_WSANTF”) and ADHD (NeuroImage: processed_Deep_WSANTF(NeuroImage))
Note: After processing a dataset, ensure to move/rename the processed dataset data (including processed, rawdata, and diagnostic files) to another directory.
Have fun and Enjoy it! Any issues please could you kindly contact me at hengjin.ke@whu.edu.cn

Please also refer to the readme.docx.



