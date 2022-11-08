# mbed_ES410_sensorcal
ES410 - Simple program for streaming the encoder output

```C++
#include "mbed.h"
#include "QEI.h"

QEI enc1(p24,p23,NC,800, QEI::X4_ENCODING); //Global Motor 800 cpr w x4 encoding

int main() {
    while(1) {
        int enc = enc1.getPulses(); //reads the current number of encoder pulses
        printf("%d  \r", enc);      //prints to the USB serial port (Default is 9600 baud);
    }
}
```
