# Oboe
This is a set of bandwidth traces of real video streaming sessions. These traces have been used for evaluations in:

Oboe: Auto-tuning video ABR algorithms to network conditions, Zahaib Akhtar*, Yun Seong Nam*, Ramesh Govindan, Sanjay Rao, Jessica Chen, Ethan Katz-Bassett, Bruno Ribeiro, Jibin Zhan, Hui Zhang, ACM SIGCOMM, 2018. (*: Both authors contributed equally)

The data corresponds to 500 video sessions. For each session, the bandwidth observed for each downloaded video chunk is provided. For privacy reasons, we do not provide information regarding the clients such as the video publisher or location of the clients.

The data is being made available to the research community as part of a collaboration between Conviva (lead contact: Jibin Zhan), Purdue (lead contacts: Yun Seong Nam and Prof. Sanjay Rao), and USC (lead contacts: Zahaib Akthar, and Prof. Ramesh Govindan). Please feel free to contact the Purdue or USC team for information about the traces (nam21@purdue.edu, sanjay@ecn.purdue.edu, zakhtar@usc.edu and ramesh@usc.edu)


The format of the trace is as follows:

For each pair of lines starting at the beginning of the file

t1 b1

t2 b1

t1 and t2 represent the start time and end time of a chunk (in milliseconds), and b1 represents the average bandwidth (in Kbps) during the time (t1, t2), and is repeated on both lines.

For two consecutive chunks,

t1 b1

t2 b1

t3 b2

t4 b2

It indicates that the first chunk download starts at t1 and ends at t2, and average bandwidth during the time (t1, t2) is b1.
Similary, the second chunk download starts at t3 and ends at t4, and average bandwidth during the time (t3, t4) is b2.
The bandwidth during the time (t2, t3) could be estimated using linear interpolation.

