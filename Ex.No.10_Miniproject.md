# Ex.No: 10  Implementation of 2D Catch the Falling Apple Game 
### DATE:  22/10/2025                                                                        
### REGISTER NUMBER : 212224110060
### AIM: 
To develop a game Cube Catcherin Unity 
### Algorithm:
```
1. Initialize player, spawner, cube prefab, and score variables.

2. Move the player left or right based on keyboard input.

3. Spawn cubes at random X positions at fixed time intervals.

4. Detect collision between player and cubes to increase score.

5. End or reset the game when a cube touches the ground.
```  
### Program:
```
1.cube catcher

using UnityEngine;

public class CubeCatcher : MonoBehaviour
{
    public int score = 0;

    void OnTriggerEnter(Collider other)
    {
        if (other.CompareTag("Cube"))
        {
            score++;
            Destroy(other.gameObject);
            Debug.Log("Score: " + score);
        }
    }
}

2.Player control

using UnityEngine;

public class PlayerController : MonoBehaviour
{
    public float speed = 10f;

    void Update()
    {
        float move = Input.GetAxis("Horizontal") * speed * Time.deltaTime;
        transform.Translate(move, 0, 0);
    }
}

```
### Output:
<img width="894" height="421" alt="Screenshot 2025-10-24 141504" src="https://github.com/user-attachments/assets/7b4ea21e-1cfb-4ef9-b0e2-a69d62474f6d" />
<img width="912" height="396" alt="image" src="https://github.com/user-attachments/assets/f84442e7-95ab-41b6-b1dc-5445235d17ca" />


### Result:
Thus the game was developed using Unity and adopted AI technology.
