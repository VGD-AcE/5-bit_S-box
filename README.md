5-bit S-box DFA Repository

This repository provides C++ source code and experiment output files for conducting Differential Fault Analysis (DFA) on lightweight authenticated encryption schemes with 5-bit S-boxes. The focus of this work is on fault injection and the statistical recovery of S-box inputs under bit-stuck fault models. The experiments target well-known algorithms such as SHAMASH, Ascon, ISAP, and Sycon.

Repository Contents

shamashcpp.cpp: This file contains the implementation of fault injection specifically targeting the SHAMASH cipher.

main.cpp: This file conducts DFA experiments for Ascon, ISAP, and Sycon using nibble-based fault models.

.xlsx output: The output from each experiment is generated in Excel format using libxl for reading and writing .xlsx files.

Requirements

To run the experiments, the following requirements are needed:

C++17 compiler: Ensure that your compiler supports C++17.

libxl: This library is used for reading and writing .xlsx files. You will need to link the library to your project and set up your license key if using the trial version.

Usage Instructions

Configure libxl:

Set the license key (if you're using the trial version) and ensure that the paths to the library are correctly set in the code.

Build and Run:

Compile and run main.cpp and/or shamashcpp.cpp to conduct the DFA experiments. These experiments will simulate fault injections and perform statistical recovery of S-box inputs.

Output:

The results of the experiments will be saved in an Excel (.xlsx) file. The output will include:

S-box values: Both the original 5-bit S-box input values and faulted 4-bit values.

Fault values: The fault injections performed during the experiments.

Round count and nibble statistics: Detailed information on the rounds and nibble-level statistics from the fault injections.

Per-trial intersection logs: These logs indicate how many fault injections were needed to uniquely determine the S-box inputs.

Example Output

The generated .xlsx file contains detailed results for each experiment. It includes:

Raw S-box input values: Both the original 5-bit S-box values and the faulted 4-bit values.

Fault injection patterns: This section outlines how faults were injected in each round of the cipher.

Differential output: Displays the differences observed in the output due to fault injections.

Input recovery statistics: Provides per-nibble recovery statistics, as well as averages over the 64 S-boxes.

License Information

This repository is provided for academic and research purposes only. It is not intended for commercial use. If you use this code or the results in any publications, please ensure you cite this repository appropriately.
