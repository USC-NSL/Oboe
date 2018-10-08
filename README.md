# Oboe
### coming soon!
------

The format of the trace is as follows:

For each pair of lines starting at the beginning of the file

t1 b1
t2 b1

t1 and t2 represent the start time and end time of a chunk (in milliseconds)

b1 represents the average bandwidth (in Kbps) during the time (t1, t2), and is 
repeated on both lines.

For two consecutive chunks,

t1 b1
t2 b1
t3 b2
t4 b2

The bandwidth during the time (t2, t3) is estimated using linear interpolation.

