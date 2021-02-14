# picoservo
A small class for controlling servos using micropython on the Raspberry Pi Pico.

## Usage
Create a Servo object for every servo you want to control and use the provided functions (mainly `goto()`) to change the servo's position.

### Example

```python
import utime
from servo import Servo

s1 = Servo(0)       # initialize servo on GPIO pin 0

while True:
    s1.goto(0)      # move arm all the way to one side
    utime.sleep(1)
    s1.goto(1024)   # move arm all the way to the other side
    utime.sleep(1)
```