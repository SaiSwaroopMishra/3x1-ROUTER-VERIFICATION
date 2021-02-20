# 3x1-ROUTER-VERIFICATION

Router is a networking device which routes the incoming packet from a source network to one of the destination network among the three, based on the address available in the packet.

### Block Diagram
![](https://github.com/SaiSwaroopMishra/3x1-ROUTER-VERIFICATION/blob/main/photos/block%20diagram.PNG)

### Packet Structure
![](https://github.com/SaiSwaroopMishra/3x1-ROUTER-VERIFICATION/blob/main/photos/packet.PNG)

### Input Protocol
![](https://github.com/SaiSwaroopMishra/3x1-ROUTER-VERIFICATION/blob/main/photos/Router%20input%20protocol.PNG)

### Output Protocol
![](https://github.com/SaiSwaroopMishra/3x1-ROUTER-VERIFICATION/blob/main/photos/output%20protocol.PNG)

### TestBench Architecture
![](https://github.com/SaiSwaroopMishra/3x1-ROUTER-VERIFICATION/blob/main/photos/TB%20Architecture.PNG)

### Features to be verified

- The packet should reach all the destinations properly as per channel address.
- All the three destinations should receive packet of all the possible payload lengths.
- When the data is corrupted, error signal should go high.
- When data is not read within 30 cycles of valid out going high, soft reset should occur.

### Assertions
- Once pkt_vld goes high, busy should be asserted in the next cycle.
- When busy is high, data_in should be stable in the next cycle.
- Once valid_out is high, read_enable should be asserted within 30 cycles.
- Once pkt_vld is high, the respective vld_out should go high in the third cycle.
- If valid_out is low, then, in the next cycle read enable should be de-asserted.
