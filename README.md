# PHP Reverse Shell using NC.exe

This is a rewrite of the [original script](https://github.com/Dhayalanb/windows-php-reverse-shell/blob/master/Reverse%20Shell.php). Unlike the original, which is utilizing an unknown binary ([Virus Total](https://www.virustotal.com/gui/file/c2c295e38ec2529a47c3e54c0ec87576b96b8bb2bfdee2964f58efe8ba873b86/relations)), this one is using the well known NC.exe which can be verified by using
[this Cybercheff](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true)Raw_Inflate(0,0,'Adaptive',false,false)MD5()&input=JHBheWxvYWQgZ29lcyBoZXJl) recipe to decode the payload and obtain a hash.

## Usage:
* Edit the php script and change the $ip & $port values according to your setup
* Start a reverse listener using `nc -nvlp <port_number>`
* Upload the shell to a php webserver and execute.
