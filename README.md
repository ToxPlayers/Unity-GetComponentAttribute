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

    //errors
    [SerializeField, Get] float _speed;
    [SerializeField, Get] ScriptableObject _scriptableObject;
}
```

![cfc2916e6d02075182077b020f89b272](https://github.com/user-attachments/assets/e2896021-843f-4153-a035-a5f7dd15cf89)
