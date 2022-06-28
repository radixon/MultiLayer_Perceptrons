# XOR
The mean squared error loss function is chosen to simplify this example; however, MSE usually is not an appropriate cost function for modeling binary data. The MSE loss function is <br />
                              &emsp;   𝐽(𝜽)= 14Σ(𝑓∗(𝒙)−𝑓(𝒙;𝜽))2𝒙∈𝕏 <br /> <br />
                                 
The form of the model, 𝑓(𝒙;𝜽), is chosen to be linear, with 𝜽 consisting of 𝝎 and 𝑏. Thus the model is defined to be <br />
                                 𝑓(𝒙;𝒘,𝑏)=𝒙𝑇𝝎 +𝑏 <br /> <br />
                                 
Minimize 𝐽(𝜃) in closed form with respect to 𝝎 and 𝑏 using the normal equations. Solving the normal equations obtains 𝝎 =0 and 𝑏 = 12⁄ as shown here:<br />
![MLP](https://user-images.githubusercontent.com/59415488/176250162-d17a2d7a-a147-4a0d-ab5f-18a769bffd52.jpg)

The XOR feedforward network has one hidden layer containing two hidden units. The feedforward network has a vector of hidden units 𝒉 that are computed by a function 𝑓(1)(𝒙;𝑾,𝒄). The values of these hidden units are then used as the input for a second layer, which is the output layer of this network. The output layer is applied to 𝒉 rather than to 𝒙. The network now contains two functions chained together:<br /> 
                                 𝒉 = 𝑓(1)(𝒙;𝑾,𝒄) and 𝑦 = 𝑓(2)(𝒉;𝝎,𝑏)<br /> <br />

with the complete model being<br /> 
                                 𝑓(𝒙;𝑾,𝒄,𝝎,𝑏) = 𝑓(2)(𝑓(1)(𝒙)) <br /> <br />
                                
A nonlinear function must be used to describe the features. The majority of neural networks do so using an affine transformation controlled by learned parameters, followed by a fixed, nonlinear function called an activation function. In modern neural networks, the default recommendation is to use the rectified linear unit or ReLU defined by the activation function 𝑔(𝑧)=max {0,𝑧}. Now the complete network is specified as <br /> 
                                𝑓(𝒙;𝑾,𝒄,𝝎,𝑏) = 𝝎𝑇max{0,𝑾𝑇𝒙 +𝑐}+𝑏 <br /> <br />
                                
![MLP 02](https://user-images.githubusercontent.com/59415488/176252289-a58aeac7-0463-460d-b12d-0f8387f0079e.jpg)
