# CIS30EFinalProject

Project is of a script intented to be used by a Raspberry Pi to allow for speech activation of a solenoid lock or other output device. 
The script mainly utilizes Google's Speech API module as well as other libaries such GPIOzero and RPi.GPIO for basic functionality.
Other libraries such as timeit, asyncio, and multiprocessing are used to optimize the dictation process. 

The original test program of the set is: speech2texttest.py 
This script does not implement any benchmarking or optimization

The script implementing only benchmarking is: speech2textTiming.py
This script implements timeit to benchmark the amount of time it takes for the program to send the audio snippet to the Google API and return the dictated speech. 

The script implementing an asychronous process is: speech2textAsync.py
This uses asyncio to run the dictation processes as well as its resulting GPIO output as a coroutine. Timeit is still utilized in this script to monitor the amount of time it takes for the process to trigger GPIO action. 

The script implementing multiprocessing is: speech2textMulti.py
This uses multiprocessing with the dictation and GPIO output as a target function. Timeit is still utilized in this script to monitor the amount of time it takes for the process to trigger GPIO action. 
