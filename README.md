# CLINK-on-FPGA
Compact LSTM inference kernel implementation based on Vivado HLS on FPGA.

## Brief Description

The compact LSTM kernel is a one-hidden-layer 5-node LSTM network.

It is designed to perform IIR filter approximation without acausal delay for the EEG signal processing.

However, the idea and implementation can be extended for a variety of embedded real-time applications.

The C simulation is based on the test bench of EEG sampling sequence, and the CLINK kernels implemented by RTL/Verilog and Vivado HLS for FPGA implementation have been verified to perform the same function.

Both the C and the FPGA implementations of the LSTM kernel are in 16-bit fixed point.

The Vivado HLS implementation of the kernel is time multiplexed by 16 slices, so that it can be shared among 16 input channels.

## Reference
**Please cite this paper when you use CLINK on FPGA in your research. Thanks!**

Zhe Chen, Hugh T. Blair, Andrew Howe, Jason Cong. [CLINK: Compact LSTM Inference Kernel for Energy Efficient Neurofeedback Devices](https://vast.cs.ucla.edu/sites/default/files/publications/CLINK_ISLPED%202018%20publication.pdf). 2018 International Symposium on Low Power Electronics and Design, Seattle, WA, July 23-25, 2018.
