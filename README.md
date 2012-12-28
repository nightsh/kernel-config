kernel-config
=============

Kernel configuration used for my Lenovo ThinkPad Edge 530

For the impatient, links to my built packages for amd64 (just ask if you 
want a specific architecture):

* linux-image http://ge.tt/16PTmLU/v/0
* linux-source http://ge.tt/16PTmLU/v/1
* linux-headers http://ge.tt/16PTmLU/v/2

Stock Debian Wheezy kernel (3.2.0) was doing fine, but was experiencing 
random freezes (issue not checked against the BTS yet). Tried installing 
Liquorix kernels, which did not freeze, but instead were sucking my battery dry. 


After checking a (big) diff between the stock kernel and the liquorix, I pulled 
together a config which I used with the latest available sources from kernel.org. 
The big difference between this and the Liquorix Linux is in the PREEMPT configuration, 
where i preferred the middle value and not the low-latency, power-hungry model 
they preferred. And yay!, the system work fine and battery life is now 5 hrs +

