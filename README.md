# Exp-6-Synchornous-counters - up counter and down counter 
## Name: Tharun V K
## Register Number: 23003686
### AIM: To implement 4 bit up and down counters and validate  functionality.
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 

## UP COUNTER 
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.

Note that each bit in this four-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.



 
 

Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.

The Q outputs of each flip-flop will serve as the respective binary bits of the final, four-bit count:

 
 

![image](https://user-images.githubusercontent.com/36288975/169644758-b2f4339d-9532-40c5-af40-8f4f8c942e2c.png)

Four-bit “Up” Counter


## DOWN COUNTER 

As well as counting “up” from zero and increasing or incrementing to some preset value, it is sometimes necessary to count “down” from a predetermined value to zero allowing us to produce an output that activates when the zero count or some other pre-set value is reached.

This type of counter is normally referred to as a Down Counter, (CTD). In a binary or BCD down counter, the count decreases by one for each external clock pulse from some preset value. Special dual purpose IC’s such as the TTL 74LS193 or CMOS CD4510 are 4-bit binary Up or Down counters which have an additional input pin to select either the up or down count mode.
![image](https://user-images.githubusercontent.com/36288975/169644844-1a14e123-7228-4ed8-81a9-eb937dff4ac8.png)


4-bit Count Down Counter
### PROCEDURE
1.Create a new project in Quartus2 software . 

2.Name the project as uc for upcounter and dc for down counter. 

3.Create a new verilog hdl file in the project file. 

4.Name the module declare as dc and uc for down counter and upcounter. 

5.Within the module declare input and output variables. 

6.Create a loop using if-else with condition parameter as reset. 

7.End the loop. 

8.End the module



### PROGRAM FOR UPCOUNTER
![Screenshot 2024-01-02 105102](https://github.com/tharunkumaran2006/Exp-7-Synchornous-counters-/assets/151625188/30270c77-6a11-4ddd-a71b-81f84c6aa083)

### PROGRAM FOR DOWNCOUNTER
![image](https://github.com/tharunkumaran2006/Exp-7-Synchornous-counters-/assets/151625188/e368f2bd-98a2-4d7d-b554-baf8218ca6fd)

### RTL LOGIC UP COUNTER
![Screenshot 2024-01-02 105145](https://github.com/tharunkumaran2006/Exp-7-Synchornous-counters-/assets/151625188/07750252-0b25-4bf3-a3a2-7b925ba270f5)


### RTL LOGIC DOWN COUNTER
![Screenshot 2024-01-02 104954](https://github.com/tharunkumaran2006/Exp-7-Synchornous-counters-/assets/151625188/04ae0a16-16f6-4306-8af6-7841b953359a)

### TIMING DIGRAMS FOR UP COUNTER 
![Screenshot 2024-01-02 105302](https://github.com/tharunkumaran2006/Exp-7-Synchornous-counters-/assets/151625188/a61d9087-71e2-452a-b43b-7c5eb26bdab2)


### TIMING DIAGRAMS FOR DOWNCOUNTER
![Screenshot 2024-01-02 104909](https://github.com/tharunkumaran2006/Exp-7-Synchornous-counters-/assets/151625188/121b531b-4216-4892-9bc9-b69b51e5a226)

### TRUTH TABLE FOR UPCOUNTER 

![Screenshot 2024-01-02 105313](https://github.com/tharunkumaran2006/Exp-7-Synchornous-counters-/assets/151625188/604d7ebd-6dc6-435d-bd8b-01b044a8642e)

### TRUTH TABLE FOR DOWNCOUNTER
![Screenshot 2024-01-02 104839](https://github.com/tharunkumaran2006/Exp-7-Synchornous-counters-/assets/151625188/21a56c9f-af7f-4130-939d-424845fe0302)







### RESULTS 

To design a Synchornous counters up counter
