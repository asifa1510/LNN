**LNN**
---
MY NOTES:


> *LNN also known as Liquid Neural Network, is a recurrent neural network which is very unlike the traditional neural networks that work on processing inputs in a fixed manner, LNNs use differental equations to update each neuron's state overtime which makes them more dynamic and adaptive with changes. (Considered with flexibility of liquid to adapt to shape of the contsiner its put in) This ability allows them to respond flexibly to changing inputs and environments with fewer parameters while remaining interpretable. LNNs are particularly powerful for tasks involving temporal or sequential data, such as robotics, autonomous driving, and time-series prediction, where adaptability in real time is crucial.*
  

---

**Key Points**
1. *Can adapt even with changes / perturbations in input.*  
2. *Requires fewer parameters while remaining interpretable.*  
3. *Well-suited for robotics, autonomous driving* (**RECEIVES CAMERA INPUT GENERATES STEERING ANGLES**), *and time-series prediction.*

<img width="500" height="400" alt="image" src="https://github.com/user-attachments/assets/5c9dabf5-13a4-4083-87dc-71dd1c1a3827" />

---

**ODE:**


<img width="350" height="130" alt="image" src="https://github.com/user-attachments/assets/1f7ad36a-be89-497a-a015-1f9c95352413" />


**Forward Pass:**


<img width="350" height="60" alt="image" src="https://github.com/user-attachments/assets/29eb8b6d-e79d-4c9f-9457-aaf0e95dd459" />


**Backward Pass:**
1) **LOSS FUNCTION:**

 
 *Adjoint Sensitivity Method*

   
<img width="350" height="86" alt="image" src="https://github.com/user-attachments/assets/328d9c4c-c946-4cf1-a931-934b3be3493d" />


2)

