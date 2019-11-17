# PlanYourTravel


### **How to Run?**
Upload the _*PlanYourTravel.ipynb*_ file to Google Colab and simply run all the cells in order (top to bottom).

### **Results**

##### 1-D CNN Model

![Screenshot](../master/1D_CNN_Results.png?raw=true)

##### 2-D CNN Model

Window_size = 5, context_size = 3(3 words on either sides)

|                              | With Glove Embeddings        | With Keras embedding layer   |
|------------------------------|:----------------------------:|:----------------------------:|
| Past sequential CNN          | 91.05                        | 91.19                        |
| Future sequential CNN        | 90.49                        | 91.67                        |
| Bidirectional sequential CNN | 91.13                        | 92.74                        |

On an average, among all the experiments made, it has been observed that the future word information is not very useful for predicting the slot label. The past information comes in useful during prediction.

##### RNN Models

|                              | With Glove Embeddings        | With Keras embedding layer   |
|------------------------------|:----------------------------:|:----------------------------:|
| SimpleRNN                    | 90.12                        | 92.47                        |
| LSTM                         | 93.06                        | 92.35                        |
| Bidirectional LSTM           | 95.38                        | 95.49                        |
