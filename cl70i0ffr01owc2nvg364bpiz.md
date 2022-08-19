## IFCONFIG / IP:  Linux Commands


# Introduction 👋🏽

These linux command are used to manage, control and configure all the networking things like IP, Interfaces Configurations , Netmask, Broadcast Addresses, MTU (Maximum Transmission Units) etc.

- **ifconfig (old way)**
- **ip (new way)**

> I am also telling about ifconfig here (In case wanna learn only about “ip”, you can skip this part, most people are now switching to “ip”)

# ifconfig (Interface Configuration)

![2794209.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1660907973446/WKQhNK-Vd.jpg align="left")

This helps to get all the basic details of the **active** interfaces we have in the network, like Ethernet, Localhost, WLAN etc. 

> ifconfig

- **MAC (Media access control) address**

A Media Access Control address (MAC address) is a hardware identifier that uniquely identifies each device on a network. Primarily, the manufacturer assigns it.

- **IP (internet protocol) address**

An IP address, or Internet Protocol address, is a series of numbers that identifies any device on a network. Computers use IP addresses to communicate with each other both over the internet as well as on other networks

- **MTU (Maximum Transmission Unit)**

It is the maximum size of a packet in bytes that can be transferred on the network, if data is bigger in size than the MTU, then it get fragmented and then travel onto the network/internet.


![Screenshot 2022-08-19 at 4.22.35 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660906813839/8J0Jyr1Me.png align="left")

![Screenshot 2022-08-19 at 2.34.55 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660906311516/2lHz4gIBP.png align="left")

- Incase want to see all the interfaces irrespective of they are **active or not**
> ifconfig -a

- **Want to see only a specific interface.**
> ifconfig "interface_name"

![Screenshot 2022-08-19 at 2.41.26 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660906983832/8OVCT30IK.png align="left")

## Features in ifconfig
- **Deactivate an interface**
> ifconfig "interface_name" down


![Screenshot 2022-08-19 at 2.48.35 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660907133446/q2e8m2VQM.png align="left")

- **Activate an interface**
> ifconfig "interface_name" up


![Screenshot 2022-08-19 at 2.50.16 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660907148799/yBhb7zpYf.png align="left")

- **Change the IP address of the interface**
> ifconfig "interface_name" "ip_address"


![Screenshot 2022-08-19 at 2.54.57 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660907206318/0RapcfBJC.png align="left")

- **Change the Netmask of the interface**
> ifconfig "interface_name" netmask "netmask"

> Netmask - Every network has its own id so that the routers can select a network in which they want to route a data packet, that Netword ID is called as Netmask.


![Screenshot 2022-08-19 at 3.02.42 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660907288382/_G_cizltI.png align="left")

- **Change the Broadcast address of the interface**
> ifconfig "interface_name" broadcast "broadcast"

> Broadcast - Incase we want to send the message/data to every one in the network, then we make the destination address as the broadcast address.


![Screenshot 2022-08-19 at 3.32.15 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660907327510/Amdtpp9_b.png align="left")

- **Same for MTU**
> ifconfig "interface_name" mtu "mtu"

> MTU (maximum transmission unit) - It means maximum size of a packet in bytes that can be transferred on the network, if data is bigger in size than the MTU, then it get fragmented and then travel onto the network/internet.


![Screenshot 2022-08-19 at 3.41.16 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660907430027/99Z3mTGLu.png align="left")

# ip (internet protocol)


![4782264.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1660907856686/ylwUr8A08.jpg align="left")

This command is used to show / manipulate routing, network devices, interfaces and tunnels.

## Features in ip

- **To show all the interfaces.**

> ip address show

> ip address

> ip addr show

> ip addr

> ip a show

> ip a


![Screenshot 2022-08-19 at 3.58.24 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660907736401/3ziB0caSa.png align="left")

- **To show only version 4  or version 6 addresses**

> ip -4 addr

> ip -6 addr


![Screenshot 2022-08-19 at 4.01.58 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660907761356/dKjgI_p5I.png align="left")

- **Want to see only a specific interface.**
> ip addr show dev "interface_name"

> show : Used to show the interfaces.

> dev : Used to select a device from all the interfaces.


![Screenshot 2022-08-19 at 4.53.47 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660908293134/gQ255QfoZ.png align="left")

- **Add multiple IP addresses to an Interface**
> sudo ip addr add "ip_address" dev "interface_name"

> add : To add an IP to an Interface

> dev : To select a device among all the interfaces in the HOST.

> Addition of these IPs are temporary as the system boots up, all this will come back to the default once.

![Screenshot 2022-08-19 at 5.05.04 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660909007533/VXyLM-EP8.png align="left")

- **Delete IP addresse from an Interface**
> sudo ip addr del "ip_address" dev "interface_name"


![Screenshot 2022-08-19 at 5.08.25 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660909194329/Hs4wFiV_5.png align="left")

- **Link command**

It is used to display link layer information, it will fetch characteristics of the link layer devices currently available.

> ip link

>ip -s link

> ip link list


![Screenshot 2022-08-19 at 5.18.50 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660909780010/dwiJEOJJ5.png align="left")

> ip link set dev "interface_name" down
- To activate

> ip link set dev "interface_name" up
- To deactivate

# Conclusion 🙇🏽‍♂️

In this post, I discussed about Some networking command of linux which basically helps us to manage, control and configure the networking variables in the network like (ip, netmask, broadcasting address, mtu, etc).

> **NOTE** : Try these commands on your terminal side by side and experiment with these commands.

> type **man "command name"** for more details in your own terminal.


![Screenshot 2022-08-19 at 6.40.04 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660914625201/A1SlODkbC.png align="left")



# What's NEXT

**IP ROUTE** : Used to manage the static routing in the network.

> NOTE : Not covered in this one, because it deserves a dedicated blog. If you will come here after 4 days, when this blog is published, you will get the link for IP ROUTE and many other commands related to **NETWORKING**

# Socials 🤝

> [ ***Twitter*** ](https://twitter.com/_s_k_yyy_)

> [ ***LinkedIn*** ](https://www.linkedin.com/in/akash-tiwari-03b3621b7/)

> [ ***Github*** ](https://github.com/akku750156)




