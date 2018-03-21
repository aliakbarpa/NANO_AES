# NANO_AES
AES 128 with serial mode encryptio.
Suitable for IoT applicatio.
It requires only 1,705 gate counts where the normal AES is 9,450 gatecounts, parallel mode encryption
The interface for this verilog design is as follows :

(Kin, Din, Dout, Krdy, Drdy, Kvld, Dvld, EN, BSY, CLK, RSTn, sel);

   //------------------------------------------------
   input  [127:0] Kin;  // Key input
   input [127:0]  Din;  // Data input
   output [127:0] Dout; // Data output
   input          Krdy; // Key input ready
   input          Drdy; // Data input ready
   output         Kvld; // Data output valid
   output         Dvld; // Data output valid

   input          EN;   // AES circuit enable
   output         BSY, sel;  // Busy signal
   input          CLK;  // System clock
   input          RSTn; // Reset (Low active)
   //-=====================================================
   
  The operating frequncy is from 2MHz to 1.2GHz.
  More than 1.2GHz frequncy yields to error data encryption.
Please acknowledge  Nanynag Technological University Singapore, EEE. if you use the design
Team member: Ali Akbar Pammu & Kwen-Siong Chong
Email: ali1@e.ntu.edu.sg
