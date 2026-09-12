# Hardware / Embedded Security

1. **Task 0 - ESP32 Project**

    Build any ESP32 project of your choice using [Wokwi](https://wokwi.com/).  
    Get comfortable with embedded programming and components.

2. **Task 1A - Embedded Security Research**
    
    Do *any two or more* of these:
    
    1. Debug interfaces and physical access (UART, JTAG, SWD)
    2. Peripheral bus security and physical sniffing (SPI, I2C, CAN)
    3. Memory safety in embedded systems (Buffer overflows, pointer corruption, stack smashing)
    4. Firmware concurrency and shared state (Interrupt handling, race conditions, atomic operations)
    5. Non-volatile storage and flash extraction (External flash dumping, hardcoded secrets, EEPROM extraction)
    6. Firmware integrity and secure boot (Cryptographic signatures, eFuses, hardware root of trust)
    7. Side-channel analysis and signal leakage (Power analysis SPA/DPA, timing attacks, EM emissions)
    8. Fault injection and hardware glitching (Voltage/clock glitching, instruction skipping, EMFI)
    9. Memory integrity and physical disturbance (Rowhammer, bit hammering, cold boot attacks)
    
    *This is a research task only. You do NOT need any physical hardware and you do NOT need to reproduce or perform any real attack.*
    
    For each topic you choose, learn about:
    
    - What it is and what it does
    - Its security flaws and risks
    - Possible attacks and impact
    - How it can be protected

3. **Task 1B - Operation CERBERUS (Optional)**

    Try the [CERBERUS challenge](https://wokwi.com/projects/474344625217808385).

    Investigate the prototype firmware and find as many significant security or reliability issues as you can.

    For the issues you find:
    - Reproduce them
    - Identify the root cause
    - Explain the impact
    - Patch them

4. **Task 2 - Driver Cooking (Bonus)**

    Write a driver for the **DS1307 NVRAM** in Wokwi without using third-party device libraries.

    Use only native Arduino `Wire.h` primitives:
    `Wire.beginTransmission()`, `Wire.write()`, `Wire.endTransmission()`, `Wire.requestFrom()`, and `Wire.read()`.

    Your driver should support:
    - Byte read/write
    - Buffer read/write
    - Boundary protection

    The DS1307 memory layout is:

    ```text
    0x00 - 0x07    Timekeeping registers
    0x08 - 0x3F    User NVRAM
    ```
    [DS1307 Datasheet](https://www.analog.com/media/en/technical-documentation/data-sheets/DS1307.pdf)
   
   [Template and Tester](https://wokwi.com/projects/474409440043071489)

    User memory operations must not read from or modify the timekeeping registers.

6. **Task 3 - Timing Analysis (Bonus)**

    Using [Wokwi](https://wokwi.com/), design a small experiment to investigate whether observable timing differences can reveal information about a program's execution.

    Use GPIO signals and the Wokwi logic analyzer to collect and compare timings.

    Explain your observations and what they could mean from a security perspective.

## Deliverables

   Submit one report containing your work for all completed tasks, along with links to your code/simulation. The report should document your approach, observations, vulnerabilities identified, exploitation/demonstration steps, fixes/mitigations, and what you learned.

   Make sure you understand and know everything you did.

## Submission
**No physical hardware is required to complete any of the tasks..** All tasks can be completed using Wokwi, research, and software-based resources.

You may use any resources available to you, including online documentation, articles, research papers, tutorials, and other references.

**Deadline:** 22 SEPT 11:59 PM

[Submission Form](https://forms.gle/wac3aLq2FV1u14No9)
