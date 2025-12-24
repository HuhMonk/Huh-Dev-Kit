# Huh-Dev-Kit
A devloper kit with some stuff thats mostly just a QOL things to unity

# Documentation

Make sure to add using
```csharp
using HuhDevKit;
```

## Scripting Define Symbols
```csharp
#if HUHDEVKIT
#if HUHDEVKIT.UNITYEXTENSIONS
#if HUHDEVKIT.EDITORTOOLS
```

## Unity Extensions (W.I.P)

### GetCorners can be used to get corners of bounds
```csharp
void Update()
{
    Bounds bounds;
    Vector3[] Corners = new Vector3[8];
    bounds.GetCorners(Corners)
}
```

### GetVelocity can be used to recieve velocity from a transform
```csharp
public Transform LeftLeg;

void Update()
{
    float _LeftLegVelocity = LeftLeg.GetVelocity();
}
```

### IsVisible gets a bool value if source transform is visible else it will be false
```csharp
public Transform Source;
public Collider SourceBox;
public Camera PlayerCam;

void Update()
{
    bool Visible = Source.IsVisible(PlayerCam, SourceBox);
}
```

### MoveTo used to move a transform to a specefic position with a set speed
```csharp
public Transform Platform;
public Transform EndPosition;
public float Speed = 4f;

void Update()
{
    Platform.MoveTo(EndPosition, Speed);
}
```

### RoundToNearest can be used to round a vector3's axis to nearest full number
```csharp
public Vector3 Position;
public Transform Block;

void Update()
{
    Position = Block.position.RoundToNearest();
}
```

### GetRandomColor can be used to get a random color
```csharp
public Color color;

void Update()
{
    color = Color.GetRandomColor();
}
```

### DistanceTo can be used to get a random color
```csharp
public Transform Player;
public Transform Monster;
public float Distance = 0f;

void Update()
{
    Distance = Player.DistanceTo(Monster);
}
```

### ResetLocal can be used to get a random color
```csharp
public Transform Cube;

void Update()
{
    Cube.ResetLocal();
}
```

### ResetGlobal can be used to get a random color
```csharp
public Color Cube;

void Update()
{
    Cube.ResetGlobal();
}
```

### MatchOtherTransform can be used to get a random color
```csharp
public Transform _Transform;
public Transform Target;

void Update()
{
    _Transform = _Transform.MatchOtherTransform(Target);
}
```
# W.I.P
