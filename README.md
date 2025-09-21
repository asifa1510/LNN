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





<img width="730" height="104" alt="image" src="https://github.com/user-attachments/assets/828771d9-2ab6-40d2-8854-af382fbf1aa3" />


<img width="630" height="40" alt="image" src="https://github.com/user-attachments/assets/65ef5c52-9978-483b-8428-9844ad1c29a7" />






<img width="350" height="89" alt="image" src="https://github.com/user-attachments/assets/68684f0f-8dc8-4da3-ac43-de840ac3ccaa" />


<img width="639" height="66" alt="image" src="https://github.com/user-attachments/assets/583ac76e-f1d5-4aac-bcfc-6547bf095357" />


<img width="990" height="250" alt="image" src="https://github.com/user-attachments/assets/1d134459-6a64-4b0f-b2c7-027f35cfa18d" />



<img width="943" height="345" alt="image" src="https://github.com/user-attachments/assets/bd6eceea-5628-44f9-9975-400bc72b570f" />


<img width="771" height="216" alt="image" src="https://github.com/user-attachments/assets/b511c69c-a6b1-452c-bdfb-c27cfdcd5f71" />



<img width="785" height="171" alt="image" src="https://github.com/user-attachments/assets/20346d2a-cb0a-4cd3-a8fa-2a4e63925307" />



<img width="699" height="275" alt="image" src="https://github.com/user-attachments/assets/66858fde-ddf6-4d18-a9ab-ea0b1358d50f" />


<img width="461" height="78" alt="image" src="https://github.com/user-attachments/assets/cf878709-935e-41c8-ae03-e95e3934e1c1" />


<img width="551" height="124" alt="image" src="https://github.com/user-attachments/assets/e440dcf1-9452-43a3-8a30-a4166aa5c636" />


