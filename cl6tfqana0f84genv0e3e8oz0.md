## SYSTEMCTL : Linux Command

# Introduction 👋🏽

These linux command are used to manage, control and configure all the systemd system services which we are using either in our own system or the other remote systems.

# Syntax of the Command

 > systemctl    options   command   service_name

**EX:** Helps to start a service named jenkins

![Screenshot 2022-08-14 at 4.36.55 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660475246622/hjgNYFjWj.png align="left")

# Commands 🖥

> - list-unit-files
> - enable
> - disable
> - status
> - start
> - stop
> - restart
> - reload
> - kill
> - mask / unmask

## list-unit-files

Command used to list all the files in the systemd and gives all the state and configurations it is following.


![Screenshot 2022-08-14 at 4.42.19 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660475544829/xk0_PSfVe.png align="left")

**UNIT-FILES** - Gives the names of all the files in the systemd

**STATE** - Current state of the files in systemd (enable, disable, static).

- **ENABLE** : If a unit is in the enabled state, the systemd starts it at boot time.

- **DISABLE** : If a unit is in the disabled state, the systemd does not start it at startup.

- **STATIC** :  If a unit is in the static state, neither the systemd starts it at startup nor allows us to change its state.

> In easy language, if a unit is in the disabled or enabled state, you can change its state from the "systemctl enable/disable" command. But if a unit is in the static state, you can’t change its state. Technically, if a unit is in the static sate, then it means that the unit does not have the "install" section in its configuration file which is required to start a unit at boot time.

**VENDOR PRESET** - This fields tell us what will be the state of the file after installation.

## enable

***Remember*** we have a **VENDOR PRESET**, so in case if it is defined as **DISABLED** for any file/service in the systemd, then we have to **enable** it before starting it.

Here in our example, the jenkins current state is **disabled**. So before starting the service we have to enable it.

![Screenshot 2022-08-14 at 4.55.57 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660476504798/iaaYSOf0-.png align="left") 
![Screenshot 2022-08-14 at 5.00.04 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660476649834/bku2sKSbz.png align="left")

## disable

To again disable it, we can use **disable** command.


![Screenshot 2022-08-14 at 5.04.25 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660476967608/Be1rEOahx.png align="left")

## status

To check the status of the services in systemd, we can use **status** command


![Screenshot 2022-08-14 at 7.03.04 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660484058925/ppstJTV7k.png align="left")


## start

To start a service in systemd, we can use **start** command.


![Screenshot 2022-08-14 at 7.05.24 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660484200744/mDiEqZA46.png align="left")

## stop 

To stop a service in systemd, we can use **stop** command.


![Screenshot 2022-08-14 at 7.07.42 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660484296100/gADmY8oH2.png align="left")

## restart

In case you change the configurations of the service file and you want to restart the service, then you can use **restart** command.



> This command will apply the new configuration but for this moment, the service will get down and start again.

## reload

In case you change the configurations of the service file and you don't want the service to go down, then you can use **reload** command.

> This command will apply the new configuration and service will still be running and applying the configurations. - (**NO DOWN-TIME**)

## kill

To stop the running service and for the later  clean up, we use **kill** command.


![Screenshot 2022-08-14 at 7.39.39 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660486342084/C9zHCf_9Y.png align="left")

> However, note that it's best to use the stop subcommand whenever possible. By default, systemctl kill sends signal 15, or SIGTERM 15, which sends a request to kill the system and enables the system to clean up as it does so.


## mask

If a service is not running, but it is called by another service, then the service will get enabled and start, to prevent this we can mask the service, so that other services can't able to start the service, in case of the service is not running.

Use **mask** command to apply the masking on any service.

![Screenshot 2022-08-14 at 7.53.28 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660487077546/tuvb7F3ql.png align="left")

> This links the service configuration to the /dev/null file, to unmask it we can use **unmask** command.

# Conclusion 🙇🏽‍♂️

In this post, I discussed about SYSTEMCTL command of linux which basically helps us to manage, control and configure the systemd services and files.

> **NOTE** : Try these commands on your terminal side by side and experiment with these commands, you will get a lot of ideas for some automation, If not you will get to know in the later posts, so stay tuned...❤️


> Will add multiple other commands of **SYSTEMCTL** , these are some main commands so I add them first.

# Socials 🤝

> [ ***Twitter*** ](https://twitter.com/_s_k_yyy_)

> [ ***LinkedIn*** ](https://www.linkedin.com/in/akash-tiwari-03b3621b7/)

> [ ***Github*** ](https://github.com/akku750156)