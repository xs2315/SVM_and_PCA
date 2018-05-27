# SVM_and_PCA
Variables

Please put the mat files for different nonBrainThreshold as below:

test:
200  'sub-01/ses-test/func/fMRImask_200.mat'
300  'sub-01/ses-test/func/fMRImask_300.mat'
400  'sub-01/ses-test/func/fMRImask_400.mat'
500  'sub-01/ses-test/func/fMRImask.mat'
600  'sub-01/ses-test/func/fMRImask_600.mat'


retest:
200 'sub-01/ses-retest/func/fMRImask_200.mat'
300 'sub-01/ses-retest/func/fMRImask_300.mat'
400 'sub-01/ses-retest/func/fMRImask_400.mat'
500 'sub-01/ses-retest/func/fMRImask.mat'
600 'sub-01/ses-retest/func/fMRImask_600.mat'


Then after you have successfully run all the cells in this .ipynb, you can get the trail logs in .txt in the same directories.

Log record:
 
Ses-test:

SVM only:

Trail 1 : SVM(C = 90.0), gamma = 0.010000) , random state = 41 , brainmask(Threshold = 200)  Accuracy = 81.5217 % 

(Best)Trail 160 :SVM(C = 100.0), gamma = 0.100000), random state = 42, brainmask(Threshold = 600) Accuracy = 88.0435 % 
For the best trail (trail 160), Real Labels:[3 2 1 1 2 1 1 4 2 1 1 3 4 4 2 3 1 1 1 3 3 3 1 4 2 3 1 3 1 2 1 3 1 1 4 4 4
 4 4 4 1 2 4 3 1 4 1 1 1 1 2 1 1 1 1 4 1 1 2 1 1 4 2 2 1 3 1 1 1 2 1 1 1 2
 1 3 2 4 4 1 4 1 1 1 1 1 4 1 1 4 2 2], Predicted Labels: [3 1 1 2 1 1 1 4 2 1 1 3 4 4 2 3 1 1 1 3 3 3 1 4 2 3 1 3 1 2 1 3 2 1 4 4 4
 4 4 4 1 2 4 3 1 4 1 1 1 1 2 3 1 1 2 4 1 1 2 1 1 4 2 2 1 3 3 1 1 2 1 1 1 2
 1 3 1 4 4 1 4 1 3 2 1 2 4 1 1 4 2 2]

PCA+SVM:

Trail 1 : PCA(components = 50), SVM(C = 90.0), gamma = 0.010000), random state = 41 , brainmask(Threshold = 200)  Accuracy = 75.0000 % 

(Best)Trail 160 : PCA(components = 100), SVM(C = 100.0), gamma = 0.100000), random state = 42 , brainmask(Threshold = 600) Accuracy = 88.0435 % 
For the best trail (trail 160), Real Labels:[3 2 1 1 2 1 1 4 2 1 1 3 4 4 2 3 1 1 1 3 3 3 1 4 2 3 1 3 1 2 1 3 1 1 4 4 4
 4 4 4 1 2 4 3 1 4 1 1 1 1 2 1 1 1 1 4 1 1 2 1 1 4 2 2 1 3 1 1 1 2 1 1 1 2
 1 3 2 4 4 1 4 1 1 1 1 1 4 1 1 4 2 2], Predicted Labels: [3 1 1 2 1 1 1 4 2 1 1 3 4 4 2 3 1 1 1 3 3 3 1 4 2 3 1 3 1 2 1 3 2 1 4 4 4
 4 4 4 1 2 4 3 1 4 1 1 1 1 2 3 1 1 2 4 1 1 2 1 1 4 2 2 1 3 3 1 1 2 1 1 1 2
 1 3 1 4 4 1 4 1 3 2 1 2 4 1 1 4 2 2]


Ses-retest:

SVM only:

Trail 25 : SVM(C = 90.0), gamma = 0.010000) , random state = 42 , brainmask(Threshold = 200)  Accuracy = 67.3913 % 

(Best)Trail 240 :SVM(C = 110.0), gamma = 0.100000), random state = 41, brainmask(Threshold = 500) Accuracy = 77.1739 % 
For the best trail (trail 240), Real Labels:[4 1 3 1 1 4 1 3 1 4 2 4 1 3 1 4 1 1 1 4 1 3 2 1 1 1 3 4 2 2 3 1 1 1 1 4 1
 3 3 3 2 2 1 1 1 4 1 1 1 1 1 2 3 1 1 4 1 1 1 1 1 1 4 1 1 1 3 1 4 1 2 1 1 4
 2 4 3 3 4 3 2 1 2 1 1 4 2 1 4 3 1 1], Predicted Labels: [1 1 3 1 1 4 1 1 1 4 2 4 1 3 1 2 1 1 1 2 1 3 2 1 2 1 1 4 1 1 3 2 2 2 4 4 1
 1 3 1 2 2 1 1 1 4 1 1 1 1 1 2 3 1 1 4 1 1 1 1 1 1 4 1 1 1 3 1 4 1 2 2 1 1
 2 4 1 3 1 3 2 1 2 1 1 1 2 1 1 1 1 1]

PCA+SVM:

Trail 1 : PCA(components = 70), SVM(C = 90.0), gamma = 0.010000), random state = 41 , brainmask(Threshold = 200)  Accuracy = 73.9130 % 

(Best)Trail 240 : PCA(components = 100), SVM(C = 110.0), gamma = 0.100000), random state = 41 , brainmask(Threshold = 500) Accuracy = 78.2609 % 
For the best trail (trail 240), Real Labels:[4 1 3 1 1 4 1 3 1 4 2 4 1 3 1 4 1 1 1 4 1 3 2 1 1 1 3 4 2 2 3 1 1 1 1 4 1
 3 3 3 2 2 1 1 1 4 1 1 1 1 1 2 3 1 1 4 1 1 1 1 1 1 4 1 1 1 3 1 4 1 2 1 1 4
 2 4 3 3 4 3 2 1 2 1 1 4 2 1 4 3 1 1], Predicted Labels: [1 1 3 1 1 4 1 1 1 4 2 4 1 3 1 2 1 1 1 2 1 3 2 1 2 1 1 4 1 1 3 2 2 2 4 4 1
 1 3 1 2 2 1 1 1 4 1 1 1 1 1 2 3 1 1 4 1 1 1 1 1 1 4 1 1 1 3 1 4 1 2 2 1 1
 2 4 1 3 1 3 2 1 2 1 1 4 2 1 1 1 1 1]

Limitations

1. The SVM is a binary classifier. In this scenario, pair-wise classification should play a role, firstly classify the instance into (1,2) and (3,4) and then classify them respectively.

2. SVM is Computationally expensive, so I used multi-processes in python to improve the speed.


Description of the result

In this assignment, I implemented the SVM and SVM + PCA with several different parameters.

It is worth to notice that there are several combination of parameters can give us best accuracy among trails for both data sets as we can see from the log records. 

The best accuracy by using SVM only among all the trails for ses-test data set is 88.0435%.  It is achieved by trail 160 :SVM(C = 100.0), gamma = 0.100000), random state = 42, brainmask(Threshold = 600). And the best accuracy by using PCA+SVM among all the trails for ses-test data set is also 88.0435%. It is achieved by trail 160 : PCA(components = 100), SVM(C = 100.0), gamma = 0.100000), random state = 42 , brainmask(Threshold = 600).

The best accuracy by using SVM only among all the trails for ses-retest data set is 77.1739%, which is achieved by trail 240 :SVM(C = 110.0), gamma = 0.100000), random state = 41, brainmask(Threshold = 500). However, the best accuracy  by using PCA+SVM approach among all the trails for ses-retest data set is 78.2609%, which is achieved by trail 240 : PCA(components = 100), SVM(C = 110.0), gamma = 0.100000), random state = 41 , brainmask(Threshold = 500).

By comparing those two approaches(SVM only and PCA+SVM), we can see that wether or not PCA can affect the accuracy depends on the variance distribution of the input data. For ses-test data set, we can see that using SVM performed similar as using PCA and SVM, since both methods can achieve 88% accuracy. However, the PCA can enhance the accuracy in the ses-retest data set.
