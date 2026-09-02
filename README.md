<img width="30%" src="https://github.com/user-attachments/assets/da53b374-07dc-4897-8608-5aa2fe1b3d33" />
<img width="30%" src="https://github.com/user-attachments/assets/a863ceed-a61f-45ae-8968-3c7fdfa3232b" />


👉 [Try it](https://bacionejs.github.io/autorun)

This project is a **procedural animation engine** that automatically **extracts geometric proportions** from a **legless** vector animal outline to construct and animate a **forward-kinematic skeleton** with **tapered bones**. It's not great, but maybe it will inspire something greater.


The program **centers and scales the animal** on the screen by mapping its outline to determine its overall height and torso proportions. It measures the **vertical distance between the belly and the back**, identifies the **front and back edges of the mid-body**, and tucks the **hip joints** neatly inward from those boundaries. Using these proportions, it constructs a **connected skeleton** featuring **upper and lower leg bones** that scale and taper proportionally, animating them with **synchronized swinging motions** and phase offsets.

However, this **heuristic-based approach** relies entirely on the assumption that the path has a clean, predictable geometry; if you alter the outline or introduce unexpected curves, the **center-slicing logic** can easily miscalculate the body bounds or latch onto stray points. It also deliberately simplifies the anatomy by rendering **only two legs instead of four**, a shortcut justified by the fact that during a fast run the visual difference is barely noticeable, even if it matters more during a slow walk. It also assumes the animal is oriented to the right. Furthermore, because the animation relies strictly on an open **forward kinematic** chain driven by **hardcoded sine waves and fixed phase offsets** rather than inverse kinematics or physics, the limbs lack any environmental awareness, meaning they will cheerfully clip through uneven ground or float in mid-air if the overall scale or posture shifts.

Legless Unicorn:  
https://bacionejs.github.io/vectorbay?m=0&p=[[1.9,-3.2,0,-1.6,0,-3.1],[2.9,-3.8,1.6,-3.5,1.6,-4.2],[3.9,-4.7,1.5,-4.5,1.6,-5.4],[2.6,-4.9,3.4,-6.7,2.6,-6.4],[3.8,-8.2,5,-6.1,4,-8.3],[5.8,-6.8,5.3,-8.4,6.2,-8.2],[6.5,-7.6,7,-7.6,7.5,-8.5],[7.3,-6.6,7.3,-6.9,9.6,-9.5],[8.4,-7.1,7.7,-6.4,8.2,-6],[8.1,-5.6,9,-4.4,9.1,-3.9],[9.4,-2.1,7.9,-2.2,8,-3.1],[7.5,-3.7,6.7,-3.6,6.5,-4.1],[5,0.2,6.2,-0.5,5.4,1.5],[-5.6,3.7,-5.3,0.6,-4.2,-2.3],[-5.7,-2.4,-5.9,1,-7.4,0.7],[-6.6,0.3,-6.3,-0.8,-6.8,-0.2],[-7.5,0.5,-8.7,1.2,-9.6,-1.7],[-9,-0.9,-7.6,-1,-8.4,-1.5],[-8.7,-1.7,-9,-1.9,-8.9,-2.2],[-7.3,-0.5,-6.1,-5.4,-3.8,-3],[-1.7,-4.7,-0.3,-2.5,1.9,-3.2]]
