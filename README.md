# Introduction
### 1. This project designed a circuit (SW.v) with 16 PEs to perform Smith-Waterman Algorithm on 64-bits reference and 48-bits query.
### 2. The circuit (SW.v) was synthesized with Synopsys Design Compiler (to SW_syn.v) and the APR process was done with Cadence Innovus (to SW_APR.v). 
### 3. The details of synthesis are in SW_area/power/timing.txt and the details of APR are in summaryReport.rpt.
# How it works
### To run the testbench file, users should first run the command 'source license.cshrc'.
### 1. SW.v: ncverilog tb.v SW.v +define+tb1
### 2. SW_syn.v: ncverilog tb.v SW_syn.v tsmc13.v +define+tb1+SDFSYN
### 3. SW_APR.v: ncverilog tb.v SW_APR.v -v ./syn/tsmc13_neg.v +define+tb1+SDFAPR +ncmaxdelays
#### P.S. The testbench file provides three test cases. (tb1, tb2, tb3)
