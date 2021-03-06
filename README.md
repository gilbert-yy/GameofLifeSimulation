# ACSE 6 Individual Assignment
### Yang YE, CID 01776005
![topic](https://github.com/acse-2019/acse-6-individual-assignment-acse-yy1719/blob/master/gol.png)
## Code structure:
![code sturcture](https://github.com/acse-2019/acse-6-individual-assignment-acse-yy1719/blob/master/Flowchat.png)

(from https://play.google.com/store/apps/details?id=com.baiels.gameoflife&hl=en_US)

Some characteristic of the main algorithm includes:

•	Do partial iteration when waiting for the non-blocking communication to finish;

•	Take in 1/0 at execution time to instruct Periodic or Non-periodic;

•	Read all data except number of iterations from the files generated by pre_processing.cpp;

•	Capable to handle situations where small number of processors are involved.

## User instruction:

All code files are inside file "Game_of_life"

#### Pre_processing.cpp
Mannual input inside the code: int p; int rows; int columns.

Get initial data by reading from "./testdata/testdata.txt", or generate by random. The data will be divided and assigned into subsets in different files for further processing.

#### main_iteration.cpp
Input when execution: int iteration; bool periodic.

Do the iterations with MPI Paralleled and write result files during each iteration.

#### post_processing.cpp
Mannual input inside the code: int p; int rows; int columns; int iteration.

Combine the files created by main_iteration.cpp to a single file for further analysis.

#### animation.ipynb
Input the directory of files created by post_processing.cpp

Generates videos for visualisation

#### MPI_type_random.cpp
Input when execution: int rows; int columns; int iterations; bool periodic.

The algorithm is same with main_iteration.cpp. But instead of reading and writing file, MPI_type_random.cpp generates random initial condition and write no file.

MPI_type_random.cpp is used in HPC to test the efficiency and characteristic of the implemented algorithm.

