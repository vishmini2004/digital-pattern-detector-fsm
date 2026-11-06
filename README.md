# Digital Pattern Detector (1110)

A single synchronous digital system that generates a random 4-bit word, serialises it and detects the bit pattern **1110** with a finite state machine.

*Project for IE3004 Digital Systems Design, SLIIT.*

## How it works
1. **NE555 timer** provides the one common clock
2. **4-bit LFSR** (D flip-flops with XOR feedback) generates a pseudo-random word every clock (15 states)
3. **74LS93 counter** counts 0-15 and issues a LOAD pulse every 16 clocks
4. **PISO shift register** (built from flip-flops and NAND gates) loads the word and shifts the bits out serially
5. **3-flip-flop Mealy FSM** watches the stream and lights an LED when 1110 appears

The complete circuit uses 14 ICs.

## Files (Proteus 8)
`all4.pdsprj` integrated system, `randomgen.pdsprj` LFSR, `counter.pdsprj` counter / load control, `piso.pdsprj` shift register, `fsm.pdsprj` pattern detector

## Tech
Proteus, finite state machines, LFSR, shift registers, 555 timer

## Author
Vishmini Michel
