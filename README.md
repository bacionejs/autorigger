<img width="30%" src="https://github.com/user-attachments/assets/85f6c9a9-ac60-49bb-9e72-cad3f68a33dc" />


<img width="30%" src="https://github.com/user-attachments/assets/85be668a-c0ac-4c66-ac9d-ed25b5b0a45d" />


👉 [Try it](https://bacionejs.github.io/autorigger) (you can also [create your own shape](https://github.com/bacionejs/vectorbay) and paste it into the html)

This project takes a **legless vector unicorn** and **automagically constructs and animates legs**. It's not great, but maybe it will inspire something greater.


It measures the **vertical distance between the belly and the back** at the unicorn's midpoint, identifies the **front and back edges of the mid-body**, and tucks the **hip joints** inward from those boundaries, constructing **portional legs**, and animating them.

However, this **heuristic-based approach** relies on assumptions for its **center-slicing logic**. Furthermore, because the animation relies strictly on an open **forward kinematic** chain rather than inverse kinematics or physics, the limbs lack any environmental awareness, meaning they will clip through uneven ground. It also deliberately simplifies the anatomy by rendering **only two legs instead of four**, a shortcut justified by the fact that during a gallop the visual difference is barely noticeable.

**Legless Unicorn**:  
https://bacionejs.github.io/vectorbay?m=0&p=[[1.9,-3.2,0,-1.6,0,-3.1],[2.9,-3.8,1.6,-3.5,1.6,-4.2],[3.9,-4.7,1.5,-4.5,1.6,-5.4],[2.6,-4.9,3.4,-6.7,2.6,-6.4],[3.8,-8.2,5,-6.1,4,-8.3],[5.8,-6.8,5.3,-8.4,6.2,-8.2],[6.5,-7.6,7,-7.6,7.5,-8.5],[7.3,-6.6,7.3,-6.9,9.6,-9.5],[8.4,-7.1,7.7,-6.4,8.2,-6],[8.1,-5.6,9,-4.4,9.1,-3.9],[9.4,-2.1,7.9,-2.2,8,-3.1],[7.5,-3.7,6.7,-3.6,6.5,-4.1],[5.4,-0.2,6,0,0.8,0.7],[-3.5,1.2,-4.4,-1.5,-4.2,-2.3],[-5.7,-2.4,-5.9,1,-7.4,0.7],[-6.6,0.3,-6.3,-0.8,-6.8,-0.2],[-7.5,0.5,-8.7,1.2,-9.6,-1.7],[-9,-0.9,-7.6,-1,-8.4,-1.5],[-8.7,-1.7,-9,-1.9,-8.9,-2.2],[-7.3,-0.5,-6.1,-5.4,-3.8,-3],[-1.7,-4.7,-0.3,-2.5,1.9,-3.2]]
