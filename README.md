LNN
---
MY NOTES:   
     
   
  
> *LNN also known as Liquid Neural Network, is a recurrent neural network which is very unlike the traditional neural networks that work on processing inputs in a fixed manner, LNNs use differental equations to update each neuron's state overtime which makes them more dynamic and adaptive with changes. (Considered with flexibility of liquid to adapt to shape of the container its put in) This ability allows them to respond flexibly to changing inputs and environments with fewer parameters while remaining interpretable. LNNs are particularly powerful for tasks involving temporal or sequential data, such as robotics, autonomous driving, and time-series prediction, where adaptability in real time is crucial.*
  

---  

**Key Points**
1. *Can adapt even with changes / perturbations in input.*  
2. *Requires fewer parameters while remaining interpretable.*  
3. *Well-suited for robotics, autonomous driving* (**RECEIVES CAMERA INPUT GENERATES STEERING ANGLES**), *and time-series prediction.*
4. *achieved this by using fewer but more expressive neurons—often as few as 19 for complex tasks like autonomous driving*

   > bio- inspired from small organisms like the nematode worm C. elegans, which has only 302 neurons but generates surprisingly complex behaviors

<img width="500" height="400" alt="image" src="https://github.com/user-attachments/assets/5c9dabf5-13a4-4083-87dc-71dd1c1a3827" />

---

**Neural ODE Training Process**

**ODE:**


<img width="350" height="130" alt="image" src="https://github.com/user-attachments/assets/1f7ad36a-be89-497a-a015-1f9c95352413" />


**Forward Pass:**


<img width="350" height="60" alt="image" src="https://github.com/user-attachments/assets/29eb8b6d-e79d-4c9f-9457-aaf0e95dd459" />


**Backward Pass:**
1) **LOSS FUNCTION:**

 
 *Adjoint Sensitivity Method*

   
<img width="350" height="86" alt="image" src="https://github.com/user-attachments/assets/328d9c4c-c946-4cf1-a931-934b3be3493d" />


ODE


<img width="350" height="83" alt="image" src="https://github.com/user-attachments/assets/9ae31beb-d240-4edd-b6e2-10020f54bd06" />


Adjoint State:


<img width="350" height="163" alt="image" src="https://github.com/user-attachments/assets/dab2cdac-fc7f-4944-bd9f-9b155f2623b0" />




> *Adjoint method creates a new state, an auxillary differential equation that connects the dynamics of the loss in respect to the state of the sytem later we can run the ODE backwards one step at a time to get the gradiants of the loss in respect to state of the system and also the gradient of the loss in respect to the parameters of the system.
This adjoint sensitivity method on the backward pass gives constant memory propagation, because it forgets the previous states.*


**BPTT**


Backpropagation through time


<img width="350" height="380" alt="image" src="https://github.com/user-attachments/assets/c38dfb15-c6e3-4605-acb0-51576460201a" />



-----
**LNN implementation:**

Refer:
[Liquid Time-Constant Networks](https://cdn.aaai.org/ojs/16936/16936-13-20430-1-2-20210518.pdf)



<img width="791" height="254" alt="image" src="https://github.com/user-attachments/assets/af53fe82-87dd-4328-997f-14a89f63d5cc" />


<img width="672" height="88" alt="image" src="https://github.com/user-attachments/assets/37d80b38-1380-4a12-bcd5-44f2225afdc5" />


<img width="577" height="133" alt="image" src="https://github.com/user-attachments/assets/56d7354a-484f-4aed-ac64-da82114c509e" />


<img width="783" height="266" alt="image" src="https://github.com/user-attachments/assets/a05991d2-df72-4676-a992-0af97766ec4f" />


<img width="771" height="216" alt="image" src="https://github.com/user-attachments/assets/b511c69c-a6b1-452c-bdfb-c27cfdcd5f71" />


<img width="699" height="275" alt="image" src="https://github.com/user-attachments/assets/66858fde-ddf6-4d18-a9ab-ea0b1358d50f" />


<img width="461" height="78" alt="image" src="https://github.com/user-attachments/assets/cf878709-935e-41c8-ae03-e95e3934e1c1" />


<img width="551" height="124" alt="image" src="https://github.com/user-attachments/assets/e440dcf1-9452-43a3-8a30-a4166aa5c636" />


