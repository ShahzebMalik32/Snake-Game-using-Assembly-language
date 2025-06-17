Snake‑Game (Assembly)
A classic Snake game written in x86 real‑mode Assembly for DOS. It uses direct VGA text‑mode writes, BIOS timer interrupts for random food placement, and keyboard/DOS interrupts for input and control flow.

Interesting Techniques
Direct VGA Text‑Mode Writes
Writing characters and attributes directly to video memory at segment 0xB800 for ultra‑low‑level rendering.

BIOS Timer Interrupt (int 1Ah)
Generating pseudo‑random food positions by reading clock ticks since midnight.

Keyboard and DOS Interrupts
Using int 16h for immediate key detection and int 21h for program exit and control.

In‑Memory Linked List for Snake Body
Maintaining snake segments as a linked list of word‑sized offsets and updating them in place.

Non‑Obvious Technologies
NASM/YASM-Compatible Assembly
Assembled with any standard Intel‑syntax assembler.

Real‑Mode x86 Architecture
Runs under DOS or DOS‑emulators (DOSBox, DOSEMU).

VGA Text Mode (80×25, 16‑color)
Leverages attribute byte in each word for color control.

Project Structure
plaintext
/
├── snake.asm        # Main assembly source
└── README.md        # Project overview (this file)
snake.txt: Contains all game logic, rendering, input handling, and interrupt calls.
