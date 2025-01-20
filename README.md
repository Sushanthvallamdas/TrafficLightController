# TrafficLightController
 
The purpose of this project is to design a methodology using Verilog to control the traffic with specified time delays for a T-Shaped road.

## Methodology

### Directions Considered

![directions](https://github.com/user-attachments/assets/22ede362-9d52-4f0e-9cfe-127520759d8c)

### Problem Statement

![ps](https://github.com/user-attachments/assets/f9c0a73c-4430-472e-b7db-12ba3f6821bc)

- Green light indicates that there is no traffic and there is easy flow of vehicles in that route/direction. 
- Red light indicates that there is a traffic jam and that route is blocked for the vehicles to move and, 
- Yellow light indicates that the route has medium flow of vehicles.      

The directions, M1, MT, M2, S and six states, S1, S2, S3, S4, S5, S6 are taken into consideration and state diagram.      
Time delays for changing from one state to another is considered as, TMG(from S1 to S2), TY(from S2 to S3), TTG(from S3 to S4), TY(from S4 to S5), TSG(from S5 to S6) 
and TY(from S6 to S1) and the cycle continues.

### State Diagram

![sd](https://github.com/user-attachments/assets/5b259815-66b9-4c39-b53e-198e2debade9)

### State Table


<table><tr><th colspan="1">Present State(ABC)</th><th colspan="1">Input</th><th colspan="1">Next State(A*B*C*)</th><th colspan="1">ST</th><th>M1(RYG)</th><th>M2(RYG)</th><th>MT(RYG)</th><th>S(RYG)</th></tr>
<tr><td colspan="1" valign="bottom">001</td><td colspan="1">!TMG</td><td colspan="1">001</td><td colspan="1">0</td><td colspan="1">001</td><td colspan="1">001</td><td colspan="1">100</td><td colspan="1">100</td></tr>
<tr><td colspan="1"></td><td colspan="1">TMG</td><td colspan="1">010</td><td colspan="1">1</td><td colspan="1">001</td><td colspan="1">001</td><td colspan="1">100</td><td colspan="1">100</td></tr></td></tr>
<tr><td colspan="1" valign="bottom">010</td><td colspan="1">!TY</td><td colspan="1">010</td><td colspan="1">0</td><td colspan="1">001</td><td colspan="1">010</td><td colspan="1">100</td><td colspan="1">100</td></tr>
<tr><td colspan="1"></td><td colspan="1">TY</td><td colspan="1">011</td><td colspan="1">1</td><td colspan="1">001</td><td colspan="1">010</td><td colspan="1">100</td><td colspan="1">100</td></tr></td></tr>
<tr><td colspan="1" valign="bottom">011</td><td colspan="1">!TTG</td><td colspan="1">011</td><td colspan="1">0</td><td colspan="1">001</td><td colspan="1">100</td><td colspan="1">001</td><td colspan="1">100</td></tr>
<tr><td colspan="1"></td><td colspan="1">TTG</td><td colspan="1">100</td><td colspan="1">1</td><td colspan="1">001</td><td colspan="1">100</td><td colspan="1">001</td><td colspan="1">100</td></tr></td></tr>
<tr><td colspan="1" valign="bottom">100</td><td colspan="1">!TY</td><td colspan="1">100</td><td colspan="1">0</td><td colspan="1">010</td><td colspan="1">100</td><td colspan="1">010</td><td colspan="1">100</td></tr>
<tr><td colspan="1"></td><td colspan="1">TY</td><td colspan="1">101</td><td colspan="1">1</td><td colspan="1">010</td><td colspan="1">100</td><td colspan="1">010</td><td colspan="1">100</td></tr>
<tr><td colspan="1" valign="bottom">101</td><td colspan="1">!TSG</td><td colspan="1">101</td><td colspan="1">0</td><td colspan="1">100</td><td colspan="1">100</td><td colspan="1">100</td><td colspan="1">001</td></tr>
<tr><td colspan="1"></td><td colspan="1">TSG</td><td colspan="1">110</td><td colspan="1">1</td><td colspan="1">100</td><td colspan="1">100</td><td colspan="1">100</td><td colspan="1">001</td></tr>
<tr><td colspan="1" valign="bottom">110</td><td colspan="1">!TY</td><td colspan="1">110</td><td colspan="1">0</td><td colspan="1">100</td><td colspan="1">100</td><td colspan="1">100</td><td colspan="1">010</td></tr>
<tr><td colspan="1"></td><td colspan="1">TY</td><td colspan="1">001</td><td colspan="1">1</td><td colspan="1">100</td><td colspan="1">100</td><td colspan="1">100</td><td colspan="1">010</td></tr>
<tr><td colspan="1" valign="bottom">111</td><td colspan="1">-</td><td colspan="1">000</td><td colspan="1">0</td><td colspan="1">000</td><td colspan="1">000</td><td colspan="1">000</td><td colspan="1">000</td></tr>
