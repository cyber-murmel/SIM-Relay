#Description
The board fullfills two tasks: Making the SIM card run by proving a clock and adapting the RX and TX signal of the UART to the one I/O line of the SIM card (transmit and receive to transceive).
The first part is done by connecting the in- and outputs of an inverter over a crystal that resonates with the desired frequency. This is stabilized by some passive components and then buffered by another inverter.
The transceiver part is done for the once direction by connecting the I/O line of the SIM card to the RX of the USB-UART converter. For the other direction, we pull up the I/O line by a resistor and connect the TX of the USB-UART converter through an inverter to a transistor, that can pull the line down (thereby the signal is double inverted).
Doing so, we prevent short circuiting that could occure if e.g. the SIM card pulls up and the USB-UART pulls down.
#Getting your own
I have the board uploaded to [OSH Park](https://oshpark.com/shared_projects/abhypSsD) if you want to order some.

<img src="./img/brd.png" alt="Board" width="40%"/>
<img src="./img/sch.png" alt="Schematic" width="40%"/>

|Part(s) |Value |
|---|---|
| C1, C2 | according to crystal (e.g. 15pF) |
| C3 | 1uF |
| C4 | 100uF |
| IC1 | 74AC04D |
| Q1 | NPN SOT23 BEC (e.g. MMBT2222A) |
| R1 | 1 Meg |
| R2, R3 | 1K |
| R4, R5 | 10K |
| SIM1| C707-10M006-136-2 |
| X1 | 3.686 MHz|
