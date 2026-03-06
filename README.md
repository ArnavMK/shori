![Screenshot 2026-03-06 163313.png](attachment:1b98f81b-bb30-43f6-9482-c47c0ccb010e:Screenshot_2026-03-06_163313.png)

**Shori PCB Layout:**

![Screenshot 2026-03-05 185120.png](attachment:f59b4c56-599e-4514-8698-dee8665a75e0:Screenshot_2026-03-05_185120.png)

### What is this project?

Shori is a custom digital fx processor pcb for electric guitars. This is the heart of the modular project i am building called Wave forge (a solid state guitar amplifier )
And this is the first revision of the board!

This project comprises of three different printed circuit boards
1. Main power amp, preamp and I/O board: Shoyu (To be started)
2. The Digital FX processor: Shori (Rev 1 finished) 
3. The Screen controller board: Gamen (to be started)

here is the link for waveforge: [Here](https://github.com/ArnavMK/WaveForge)

### How to use it?

This is just rev 1 and is not manufactured yet, but this is a part of much larger multi board system and hence it needs to be connected to the other boards, through the two main connectors
The main ribbon connector for power and guitar audio from Shoyu. And the JST connector for the UART communication between the screen and shori. The screen has UI for controlling the parameters the digital fx like wet time modulation for delay and chorus. The screen will also have a waveform visualizer which is also be generated through shori.

### Why I made it

I have been playing electric for the past 11 years and never thought to build my own amp untill i met a friend profound in electronics and hardware design who inspired me into making my own. This board is the first step into putting a massive dent in WaveForge and i cant wait to finish it. Linked posts do not know what's coming for them.

I am pretty much nuking half the board for rev 2 now, after some peer roasting and friendly fire

### Project Pictures

There is no 3D encloser cad for shori yet! because that is the amp. Layout and 3D cad given on top of this page.

---

### Bill of Materials (BOM) FOR REV 1 ONLY !

This bom does not include the extra amount for each component, this is for only one shori board with perfect amount of compoenents!

*(A full `shori.csv` is also included in the root directory of this repository).*

| Component | Part Number | Quantity | Link | Cost (euro) |
| --- | --- | --- | --- | --- |
| Microcontroller | STM32F405RGT6 | 1 | [Link](https://www.digikey.ie/en/products/detail/stmicroelectronics/STM32F405RGT6/2754208) | 10.4 |
| Audio Codec | TI PCM3060 | 1 | [Link](https://www.digikey.com/en/models/1900019?tab=snapmagic) | 5.78 |
| Dual Audio Op-Amp | NE5532 | 1 | [Link](https://www.digikey.com/en/products/detail/texas-instruments/NE5532DR/499499) | 0.43 |
| Crystal Oscillator | 7M-25.000MAAE-T | 1 | [Link](https://www.digikey.ie/en/products/detail/txc-corporation/7M-25-000MAAE-T/3674351) | 0.59 |
| 3.3V LDO Regulator | AP2112K-3.3 | 1 | [Link](https://www.digikey.ie/en/products/detail/diodes-incorporated/ap2112k-3-3trg1/4470746) | 0.22 |
| 0805 capacitors (10uF) | 0805B475K160CC | 6 | [Link](https://www.digikey.com/en/products/detail/nextgen-components/0805B475K160CC/22601960?s=N4IgjCBcpgLFoDGUBmBDANgZwKYBoQB7KAbXAAYAOAdlgCYQBdAgBwBcoQBlNgJwEsAdgHMQAXwJhqCEMkjps%2BIqRD06sMAFYmrDpG58hoiSDqaG0Waky4CxSGXV0AnGEo6Q7TjwEjxk50pnGTkFW2UHEHImEzpyWGDLUJslezJyADowAAIAVoAxEAJYDOo8wslyco8vfQBVQX42AHkUAFkcNCwAV14cfxAAWngk60U7FVcANnJpRhNB7VH5FInIiHmxMSA) | 0.34 |
| 0805 capacitors (100nF) | 0805B104K500BD | 11 | [Link](https://www.digikey.com/en/products/detail/nextgen-components/0805B104K500BD/15776052) | 0.078 |
| Custom PCB | 4-Layer FR4 | 5 | [Link](https://jlcpcb.com/) | 6.02 |
| JLCPCB shipping | DHL to ireland | - | [Link](https://jlcpcb.com/) | 26.95 |
| 0805 capacitors (2.2uF) | CL21B225KAFNNNE | 2 | [Link](https://www.digikey.com/en/products/detail/samsung-electro-mechanics/CL21B225KAFNNNE/3888612) | 0.12 |
| 0805 capacitors (1uF) | CL21B105KAFNNNE | 3 | [Link](https://www.digikey.com/en/products/detail/samsung-electro-mechanics/CL21B105KAFNNNE/3886724) | 0.10 |
| 0805 resistors (10K) | CR0805-FX-1002ELF | 7 | [Link](https://www.digikey.com/en/products/detail/bourns-inc/CR0805-FX-1002ELF/3593209) | 0.10 |

total price is around 78.64 euros.

### Notes for rev2

---

- Use the CS4272 audio codec for easier layout and routing with better top and bottom clipping range!
- Divide the main IDC connector into three sperate connectors for POWER (5V in), AUDIO_IN and AUDIO_OUT
- Add via fence and clear division between the analog and digital domains
- Add filtering for the audio input and output to the codec for optimal performance.

Thank you!
