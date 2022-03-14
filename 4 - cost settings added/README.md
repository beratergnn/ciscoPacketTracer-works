# explanation
* In this example, we continue over the example which was at the second study. Firstly, we need to add 1 port for each of the 
B and the C routers. In order to do this, we close the router after the " copy running-config startup-config" command, 
which is done for taking the routers' running-config file to the startup-config, and add our port. 
Then, we introduce this directly connected port to the B and the C routers. We add "int e0/0/0 " and "ip add 192.168.100.10 255.255.255.252" 
for the B router while it is in "B(config)#" mode. Similarly, we add the related ip adress for the C router. After that, 
because we have a shorter way for the B router to connect to the 192.168.3.0 network, we delete this road with 
"no ip route 192.168.3.0 255.255.255.0 192.168.100.1" code while it is in "B(config)#" mode and we add the same way again 
with 2 cost because of the 2 at the end of the code with "ip route 192.168.3.0 255.255.255.0 192.168.100.1 2". Then, 
we add the short way again with "ip route 192.168.3.0 255.255.255.0 192.168.100.10". Lastly, we add our alternative long way, 
which opens to the 192.168.1.0 network, with "ip route 192.168.1.0 255.255.255.0 192.168.100.10 2" code with 2 cost.  
After we do the similar configurations for the A and the C routers, our network is ready. With this study, 
we presented alternative ways for our network to use in case of a cable dissociation.

## screenshot
* 
