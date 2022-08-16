# Spark-Dataframe-Clustering-Find-the-hackers
Using clustering, find the number of hackers involved

* The entire project is undertaken on an AWS ubuntu virtual machine.

A large technology firm needs your help, they’ve been hacked! Luckily their forensic engineers have grabbed valuable data about the hacks, including information like session time,locations, wpm typing speed, etc. The forensic engineer relates to you what she has been able to figure out so far, she has been able to grab meta data of each session that the hackers used to connect to their servers.

* Created a model that can find the number of hackers by clustering similar activities.
* Find out there were only two hackers instead of 3  or more as I originally supposed.
* Used "Silhouette with squared euclidean distance" to find a good k value.


## Code and Resources Used 
**Languages and Packages:** python, sql, pyspark, KMeans clustering, AWS

## These are the features of the data:

* ‘Session_Connection_Time’: How long the session lasted in minutes
* ‘Bytes Transferred’: Number of MB transferred during session
* ‘Kali_Trace_Used’: Indicates if the hacker was using Kali Linux
* ‘Servers_Corrupted’: Number of server corrupted during the attack
* ‘Pages_Corrupted’: Number of pages illegally accessed
* ‘Location’: Location attack came from (Probably useless because the hackers used VPNs)
* ‘WPM_Typing_Speed’: Their estimated typing speed based on session logs.

<br>
<br>
The conclusion at the end of the notebook<br>

### Bingo! It was 2 hackers, in fact, our clustering algorithm created two equally sized clusters with K=2, no way that is a coincidence! Furthermore, k=2 respects our condition "< 6" which we discovered earlier. 
