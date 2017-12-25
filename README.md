# Implementing the PowerSign and AddSign rule
The PowerSign and AddSign update rule are a gradient 
update rules found by Quoc V. Le's team and was 
reported in their paper "Neural Optimiser search with Reinforcment learning", which claimed that the optimiser found by their algorthim is better than adam and SGD for training neural networks. This repo tries to replicate their experiment for small CNNs in pytorch. I nickname my implementation of the PowerSign Rule NASoptimiser which stands for Neural Architectural Search optimiser. 

# How to use 
```
python CNN_with_NASoptim.py 
```

# Results 

## 160 Epochs 
![alt text](https://github.com/Neoanarika/Implementing-the-PowerSign-and-AddSign-rule/blob/master/img/160%20epochs.png)
| Optimiser     | Colour        |
| ------------- | ------------- |
| SGD           | Sky Blue      |
| Adam          | Red           |
| PowerSign     | Dark Blue     |
| AddSign       | Orange        |

## 300 Epochs
![alt text](https://github.com/Neoanarika/Implementing-the-PowerSign-and-AddSign-rule/blob/master/img/300%20epochs.png)
![alt text](https://github.com/Neoanarika/Implementing-the-PowerSign-and-AddSign-rule/blob/master/img/300%20epcohs%20time.png)

Both PowerSign and AddSign have high training accuracy but much lower test accuracy, which suggest Overfitting is a common problem in update rules found by the Algorthim. 

By halfing the number of epochs we were able to reduce overfitting in PowerSign, this suggest early stopping is a good strategy to manage overfitting for PowerSign and possibly even for AddSign. 

The next step will be to visualise the learning on
tensorboard while running 500 epochs.  

# Dependecies 
```
1. Python 3
2. Pytorch 
```

Make sure that the Pytorch can support GPU. 

Working on a tensorflow implementation soon
