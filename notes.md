# Solar ii proxy notes

Starting with imports

```python
# double check these, not 100% convinced
import apache
from math import sin, cos, asin, degrees, radians
```

Then working from the fact that scripted profiles has access to:

$$I_{hglob} = I_{hdiff}+I_{beam}\sin(\alpha)$$

Where:

$I_{hglob}$ is the total solar flux in W/m2 on the horizontal plane.

or
```python
self.context.weather.igh
```

$I_{hdiff}$ is the diffuse sky solar flux (W/m2) on the horizontal plane.

or
```python
self.context.weather.ifh
```

$I_{beam}$ is the solar flux (W/m2) measured perpendicular to the beam.

or
```python
self.context.weather.idn
```

$\alpha$ is the solar altitude.

## Steps
1. igh - ifh (gives us just the beam term)
2. 