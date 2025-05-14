# Ex.No: 4  Implementation of Kinematic movement -seek behavior in Unity
### DATE: 08-03-2025                                                                           
### REGISTER NUMBER : 212223040184
### AIM: 
To write a program to simulate the process of seek behavior in Unity 
### Algorithm:
1. Create a New Unity Project by Open the  Unity Hub and create a new 3D Project,Name the project (e.g., SeekBehaviorDemo).
2. Create the Moving Object
   In the Hierarchy, right-click → 3D Object → Cube (or Sphere).
   Rename it to Seeker and Reset its position:Select the Seeker, go to Inspector → Transform → Set Position to (0,0,0).
3. Create the Target Object
   Right-click in the Hierarchy → 3D Object → Sphere (or any other shape).
   Rename it to Target. Move it away from Seeker, e.g., set Position to (5, 0, 5).
   Select the Target, add a Material, and change the color. (if needed) 
4. Adding the Seek Behavior Script
   Create the Script-In the Project Window, go to the Assets folder.
   Right-click → Create → C# Script.
5. Write a script for seek behavior and save it
6. Attach the Script
   Select Seeker in the Hierarchy - Drag & Drop the SeekBehavior script onto the Inspector Panel.
   Drag & Drop the Target from the Hierarchy into the "Target" field in the script component.
12. Run the game 
13. Stop the program
    
### Program:
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.AI;  // Ensure UnityEngine.AI is included

public class SeekBehavior : MonoBehaviour
{
    public NavMeshAgent agent;  // Corrected declaration
    public float speed;
    public Transform target;

    void Start()
    {
        agent = GetComponent<NavMeshAgent>();
    }

    void Update()
    {
        if (agent != null && target != null)  
        {
            agent.SetDestination(target.position);  // Correct method name
        }
    }
}

```
### Output:
![Screenshot 2025-03-17 111820](https://github.com/user-attachments/assets/2a85f209-c4b3-4d47-8cb8-0dcde0c46985)

![Screenshot 2025-03-17 111837](https://github.com/user-attachments/assets/ce1af74d-2c1b-40fb-984d-f8857c510a1e)

### Result:
Thus the simple seek behavior was implemented successfully.
