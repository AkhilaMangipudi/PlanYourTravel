# PlanYourTravel

### **Team**
- Aditya Kumar (227008652)
- Anindita Mishra (527002315)
- Kamala Akhila Mangipudi (627005193)
- Patel Vihang (627006266)

### **How to Run?**
Upload the _*PlanYourTravel.ipynb*_ file to [Google Colab](https://colab.research.google.com/) and simply run all the cells in order (top to bottom).
Select Python 3 as the environment.

### **Dataset**
[Pickle file contatining the data - atis.pkl](https://github.com/AkhilaMangipudi/PlanYourTravel/blob/master/atis.pkl)

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

### References

- [Using Recurrent Neural Networks for Slot Filling in Spoken Language Understanding](https://ieeexplore.ieee.org/abstract/document/6998838)
- [Sequential Convolutional Neural Networks for Slot Filling in Spoken Language Understanding](https://arxiv.org/abs/1606.07783)
- Spoken Language Understanding Tutorial [Blog](https://chsasank.github.io/spoken-language-understanding.html) 
