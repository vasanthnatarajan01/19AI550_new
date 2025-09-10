# Ex.No: 3  Basic movements in Unity 
### DATE: 26/08/2025                                                                           
### REGISTER NUMBER : 212224110060
### AIM: 
 To learn the basic movements translation,scaling and rotation of game objects through code.
### Procedure:
1. Setup the Scene
2. Open Unity and create a 3D Scene.
3. Add three objects:Cube → Rename to Object1 (for movement),Sphere → Rename to Object2 (for rotation).Capsule → Rename to Object3 (for scaling).
4. Add the Script,Create a C# Script → Name it TransformOperations.cs.
5. Write the code for translation,scaling and rotation,save and close the script
6. Save the script
7. Select any empty GameObject (or create one: GameObject → Create Empty).
8. Attach the TransformOperations script to it.
9. In the Inspector, assign Object1 → Drag the Cube,Object2 → Drag the Sphere.Object3 → Drag the Capsule.
10. Run the Scene Press Play ▶️ in Unity
11. Stop the program.
### Program 
```
using UnityEngine;
public class TransformOperations : MonoBehaviour
{
    public Transform object1; // Object for translation
    public Transform object2; // Object for rotation
    public Transform object3; // Object for scaling

    public float moveSpeed = 2f;  // Speed of translation
    public float rotateSpeed = 50f; // Speed of rotation
    public float scaleSpeed = 0.5f; // Speed of scaling

    void Update()
    {
        // Translate (Move) object1 along the X-axis- Time.deltaTime to make movement smooth across all frame rates
        if (object1 != null)
        {
            object1.position += Vector3.right * moveSpeed * Time.deltaTime;
        }

        // Rotate object2 around the Y-axis
        if (object2 != null)
        {
            object2.Rotate(Vector3.up * rotateSpeed * Time.deltaTime);
        }

        // Scale object3 up and down
        if (object3 != null)
        {
            float scaleChange = Mathf.PingPong(Time.time * scaleSpeed, 1f) + 0.5f; // generates a value that moves back and forth between 0 and length
            object3.localScale = new Vector3(scaleChange, scaleChange, scaleChange);
        }
    }
}
```
### Output:
## The Capsule moves from left to right continuously.
<img width="1919" height="1141" alt="image" src="https://github.com/user-attachments/assets/b4df6f78-64a2-4ff2-be19-729f2d2cf07a" />

### The Cube rotates around its Y-axis.
<img width="1919" height="1139" alt="Screenshot 2025-09-10 142213" src="https://github.com/user-attachments/assets/97a1cdc9-6e6b-4624-a1c6-e8db9f07a53d" />



### The Cylinder scales up and down smoothly.

<img width="1919" height="1138" alt="Screenshot 2025-09-10 141603" src="https://github.com/user-attachments/assets/9f0afd37-c95a-402d-b4d1-638bf5ce35ff" />






### Result:
Thus the basic movement is learned through scripting


