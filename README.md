# Unity-GetComponentAttribute
Automatically get components in the editor using an attribute.
</br> Fast, does not enumerate reflection fields.
</br> Uses Unity's property drawers.
</br> Use with [SerializeField] to save them.

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
![image](https://github.com/user-attachments/assets/061b634d-2b7e-4106-9151-955523183d6a)
