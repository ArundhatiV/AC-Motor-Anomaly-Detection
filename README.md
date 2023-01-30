![image](https://user-images.githubusercontent.com/108016928/215590911-9ab5d42f-41c8-4631-9cee-97753848c372.png)

## **What is Motor Current Signature Analysis?**
Motor current signature analysis can be described as a technique that helps in determining the induction motor’s operating condition without disturbing production. In other words, it senses an electrical signal that has current components and identifies the faults in the initial stage. Therefore, it plays a pivotal role in preventing damage and diagnosing motor failure.

**Motor current signature analysis helps in detecting the following:**

•	Unbalance/ misalignment

•	Defective bearings

•	Rotor bar damage

•	Load issues

•	Dynamic eccentricity

•	Static eccentricity

## **How Does Motor Current Signature Analysis Detect Fault Frequencies?**

Let’s take an example of the current signal that you acquire from the motor supply without disturbing any operation of the machine. In motor current signature analysis, the frequency spectrum (aka current signature) is acquired by processing the current signal. In case there is a fault, the frequency spectrum becomes dissimilar to the healthy motor. 
   
   The fault detection of induction motor and condition monitoring is obtained through signal processing techniques because they are cost-effective, and implementing them is pretty easy. Moreover, implementing MCSA helps in getting an accurate analysis of fault.

  To identify the exclusive current signature patterns and give a wider dynamic range of different faults, there is the use of decibel (dB) versus frequency spectrum. It helps identify defects such as stator faults, rotor walks, bearing faults and eccentricity, or there could be a combination of these faults.


## **Faults MCSA Can Detect**

Here are the faults that motor current signature analysis can detect:

**1.	Bearing Faults:**

There are usually two rings of rolling element bearings. When the operating conditions are normal and there is a balance between good alignment and load, weariness failures typically start with small fissures. It means that they slowly spread to start creating noticeable vibrations and noise levels. Understandably, detecting motor bearings faults is not easy because of different reasons such as misalignments. This is where MCSA steps in to identify defects by detecting frequency components – f 0 (lower frequency) and f 1 (upper frequency).

**2.	Broken Rotor Bars**

We know that specific induction motors face the problem of broken rotor bars because of laborious duty cycles, but they do not cause the failure of the induction motor. However, they can lead to other damages. For instance, the fault mechanism can break parts and cause mechanical damage and winding failure, directly affecting production and leading to an expensive repair.

**3.	Air-Gap Eccentricity**   

This fault causes an air-gap length that does not remain constant to the stator circumference time and angle. This happens when there is no uniform air gap between the stator and the rotor. There are three types of air-gap eccentricity: Dynamic, static, and mixed eccentricity.
 
# **Objective:**

Write an ML model to detect anomalies in this data set. The model should learn, and predict future anomalies.

# **Problem Statement:**

Dataset contains real-time current readings of a 3-phase AC motor (3.2hp) motor current signature analysis and model-based VI analysis to be done to detect anomalies.
Detect anomaly and alert defects from an unstructured data pool received from current and voltage sensors of a 3-phase induction motor (Medium Voltage) at a rate of 10K - 15K instances per second.
Structure/process the data, create condition indicators, create an ML model, and create features to train the model.

# **Flow of the Project:**
This script appears to be implementing an auto encoder, a type of neural network used for unsupervised learning, for anomaly detection. The script reads in several text files from a specified directory, concatenates them into a single Data Frame, fills any missing values with 0, normalizes the data using the MinMaxScaler, and splits the data into training and test sets. The script then creates an auto encoder model with a specified number of neurons in the encoding layer and trains the model on the training data. The script then uses the model to make predictions on the test data, calculates the reconstruction error for each sample, and defines a threshold for the reconstruction error based on the 90th percentile of the mean squared error (MSE). The script then classifies samples as normal or anomalous based on whether their reconstruction error is greater than the threshold, and prints a confusion matrix, accuracy score, and classification report to evaluate the model's performance.

**To perform motor current signature analysis and model-based VI (Voltage and Current) analysis to detect anomalies in a 3-phase AC motor, you can following the steps below:**

1.	Pre-processing: Clean and preprocess the data to remove any missing values, outliers, or noise. This will ensure that the data is in the correct format for analysis.
2.	Data analysis: Plot the voltage and current signals of the 3-phase AC motor. This will help you understand the characteristics of the data and identify any patterns or anomalies.
3.	Model-based VI analysis: Use mathematical models to analyze the relationship between the voltage and current signals. This can include performing a Fourier Transform or a Wavelet Transform to extract features from the signals.
4.	Motor current signature analysis: This involves analyzing the motor current signature by computing the phase current harmonics, phase current unbalance, and line current unbalance. These parameters can help you detect anomalies in the motor, such as faults or vibrations.
5.	Anomaly detection: Use machine learning algorithms, such as clustering or classification, to detect anomalies in the motor current signature data. You can train the algorithms on the pre-processed data and use the trained models to classify new samples into normal or anomalous classes.
6.	Evaluation: Evaluate the performance of the anomaly detection model by using metrics such as accuracy, precision, recall, and F1 score. This will help you determine the effectiveness of the model in detecting anomalies in the 3-phase AC motor.
7.	Visualization: Visualize the results of the anomaly detection model by plotting the original signals, predicted labels, and anomalies. This will help you understand the results of the analysis and identify any trends or patterns in the data.

**To create condition indicators for the motor current signals, you can calculate specific metrics such as:**
1.	Slope: Slope of the current signals can indicate the stability of the motor. A steep slope can indicate an unstable motor and may be a sign of an anomaly.
2.	Roughness: Roughness of the current signals can indicate the smoothness of the motor operation. A high roughness can indicate a vibration or mechanical issue with the motor.
3.	Kurtosis: Kurtosis is a measure of the peakedness or flatness of the current signals. A high kurtosis value can indicate a motor fault, such as broken rotor bars.
4.	RMS (Root Mean Square) value: RMS value is a measure of the magnitude of the current signals. A high RMS value can indicate an overload on the motor, leading to increased heating and wear on the components.
5.	Crest Factor: Crest factor is a measure of the peakiness of the current signals. A high crest factor can indicate an overloading condition on the motor. 

#     **Conclusion:**

        Once these metrics have been calculated, they can be used as condition indicators to train an ML model to detect anomalies in the motor current signals. Here, in this project I have considered factor RMS (Root Mean Square) value. The script then uses the model to make predictions on the test data, calculates the reconstruction error for each sample, and defines a threshold for the reconstruction error based on the 90th percentile of the mean squared error (MSE). The script then classifies samples as normal or anomalous based on whether their reconstruction error is greater than the threshold, and prints a confusion matrix, accuracy score, and classification report to evaluate the model's performance. The scatter plot allows visualizing how the MSE values are distributed and how many samples have MSE values above the threshold, indicating the presence of anomalies in the data. (~=0.380)

