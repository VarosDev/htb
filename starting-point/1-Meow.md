# Premier Starting Point - Meow

⚠️⚠️ -- Attention ce topic solutionne le Starting Point, si vous ne voulez pas voir les réponses, merci de ne pas lire ce topic. -- ⚠️⚠️

## Connexion à la VM

Entrez les paramètres suivant, puis télécharger le fichier : 
![image](https://user-images.githubusercontent.com/81636746/171740588-d8eb4e60-0d0b-488f-8efa-bc3ae59d5324.png)

*L'exécuter sur la VM avec la commande :*

```
sudo openvpn [filename].ovpn
```

## Vérifier la connectivité à la VM

*Ping la machine :*

![image](https://user-images.githubusercontent.com/81636746/171741280-3ab6b61e-42d7-41d1-8809-84e0cd036670.png)

```
ping 10.129.141.136
```

### What does the acronym VM stand for?
Virtual Machine

### ___What tool do we use to interact with the operating system in order to issue commands via the command line, such as the one to start our VPN connection? It's also known as a console or shell.___
terminal

### ___What service do we use to form our VPN connection into HTB labs?___
Openvpn

### ___What is the abbreviated name for a 'tunnel interface' in the output of your VPN boot-up sequence output?___
tun

### ___What tool do we use to test our connection to the target with an ICMP echo request?___
ping

### ___What is the name of the most common tool for finding open ports on a target?___
nmap

### ___What service do we identify on port 23/tcp during our scans?___
telnet

### ___What username is able to log into the target over telnet with a blank password?___
root

## Récupérer le flag final
*Se connecter en telnet à la machine*

```
telnet 10.129.141.136
Login : root
Password :
```

Aucun password n'est requis (réponse à la question précédente).

*Récupérer le flag sur le bureau :*

```
cat flag.txt
```



