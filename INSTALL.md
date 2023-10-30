## Experimental Setup
We executed the proposed system on Google Colaboratory which facilitates the execution of arbitrary Python code with GPU back-end. The compute resources used in this study consist of a Nvidia K80 GPU with a memory of 12 GB. A total disk space of 358 GB was utilized to handle the data with 12 GB of RAM. The GPU memory clock was utilized at 0.82 GHz with a performance of 4.1 TFLOPS.
The IP addresses are given in string format in the dataset. To use them as our feature data, we converted them into int or float data types. First, we have converted the Source and Destination IPs into integer format using the IP address library. After that feature values are assigned to label values as both of them are present in different containers. After that, we converted different categories of Cat columns into numbers for which we used dummy libraries to divide each category into different columns. Then we merged those converted categories with the input table and dropped the column of the category that contains string values.

## Execution:
1.	To execute the code, first download the data cleaning file which performs all the necessary operations preprocessing operations on the dataset. This includes label encoding and checking the distribution of different types of attacks in the dataset. The attacks are categorized into three major groups. This code generates a .csv file that contains the cleaned dataset.
   
   ![image](https://github.com/yg14uv/Software-Impact/assets/54506745/2b512b13-ce06-485b-be11-ff99c19f5eed)
  	
  ![image](https://github.com/yg14uv/Software-Impact/assets/54506745/7e01abdf-4271-4126-9b94-e209891805d5)
  
2.	The second step is to perform the data balancing method. The data generated from the previous file is balanced against all the classes. SMOTE oversampling is performed for data balancing and this code generates a resultant CSV file with balanced data.
   
   ![image](https://github.com/yg14uv/Software-Impact/assets/54506745/13151d0b-3ec2-4ba0-aabf-c9b3fdf72962)
  	
3.	This balanced dataset generated from the previous file further undergoes the feature selection phase.
   
   ![image](https://github.com/yg14uv/Software-Impact/assets/54506745/2ed046af-5974-416a-be48-f9b6a9db2d79)
  	![image](https://github.com/yg14uv/Software-Impact/assets/54506745/9dced97c-af6a-4ad9-9809-ae022c8562ac)

4.	After the dataset is prepared, the first tier applies the machine learning-based classifiers including the decision tree, naïve Bayes, and SVM to classify between normal and anomaly data.
5. The second tier applies the hybrid deep learning model for anomaly type detection and classification. 
