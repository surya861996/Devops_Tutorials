# Docker Network Step by step

1. To display the network list
    ~~~
    # docker network ls
    ~~~

2. To Display detailed information on one or more networks
    ~~~
    # docker  inspect <cid>
    ~~~

3. To Create a network
    ~~~
    # docker  network  create --subnet 10.1.0.0/24 --gateway 10.1.0.1 mynet1
    ~~~
    ~~~
    # docker  network  create --subnet 10.1.0.0/24 --gateway 10.1.0.1 --ip-range 10.1.5.0/24 --driver=bridge --label=ownnetwork mynet2
    ~~~

4. To Remove one or more networks
    ~~~
    # docker  network  rm  <network_name>
    ~~~

5. Remove all unused networks
    ~~~
    # docker  network    prune 
    ~~~

6. Connect a container to a network
    ~~~
    # docker  network   connect
    ~~~

7. Disconnect a container from a network
    ~~~
    # docker  network   disconnect
    ~~~

8. To run the image with ip to particular net.
    ~~~
    # docker  run   -it  --name  <cname>  --net < network_name > <img_name>
    ~~~
     ~~~
    # docker  run   -it  --name  <cname>  --net < network_name > --ip <ip_address> <img_name>
    ~~~

9. To run the image with ip,port and web address
    ~~~
    # docker  run –it  --name  <cname>  --net < network_name >  --ip <ipaddress>  -p  82:80  -h <host_name>   ubuntu   
    ~~~

