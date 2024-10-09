# Unity-GetComponentAttribute
Automatically get components in the editor using an attribute
Using property drawers

# Example
```c#
public class TestScript : MonoBehaviour
{
    [SerializeField, Get] Rigidbody _rb;
    [SerializeField, GetChild] Collider _childCollider;
    [SerializeField, GetParent] ParticleSystem _parentParticles;


    [SerializeField, Get] Canvas _nullComp; 
    [SerializeField, Get(Required = true)] Canvas _nullCompWithWarning; 

    //errors
    [SerializeField, Get] int _value;
    [SerializeField, GetChild] ScriptableObject _scriptable;
}
```
![image](https://github.com/user-attachments/assets/b6f51038-6294-439e-9c61-e1b553eba294)
