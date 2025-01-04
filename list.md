Thoughts:<br>
1. Microcontroller will handle video storage, processing, and communication.<br>
2. Its SD card holds mp4. Video is downscaled to 64x36 and grayscaled.<br>
3. Communicates to FPGA via SPI (may switch to parallel in the future). Only need 3 GPIO pins (MOSI, CLK, CS). MISO not needed.<br>
4. FPGA manages LED Matrix, timing, refresh rate, turning LEDs on/off.<br>
5. FPGA uses multiplexers to select row/column, and will implement LED drivers instead (Microcontroler -> FPGA -> LED Drivers). They offer build in PWM control which would be perfect.<br>
6. Should include SRAM buffering.<br>
7. Must be white LEDs (~20mA). PCB and case should be black.
