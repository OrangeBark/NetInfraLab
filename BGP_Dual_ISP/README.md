
Following is a BGP / DUAL ISP LAB on GNS3

![BGP DUAL ISP Diagram](images/BGP_DUAL_ISP.png)

We are using FRROUTING on GNS3 afters configuring HQ and REMOTE-HQ routers

The main success criteria are:  

* Both BGP sessions established  
* Each neighbor receives 1 prefix  
* Both BFD sessions Up  
* Two equal-weight next hops installed  
* PC-HQ can reach PC-REMOTE-HQ  
* Either ISP can fail while the other continues forwarding

Expected ECMP route on Remote HQ:  
10.10.10.0/24  
  * 172.16.1.1, via eth8, weight 1  
  * 172.16.2.1, via eth9, weight 1

Expected ECMP route on HQ:  
10.20.20.0/24  
  * 172.16.1.2, via eth8, weight 1  
  * 172.16.2.2, via eth9, weight 1  
