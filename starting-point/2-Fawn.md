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

## Questions

### ___What does the 3-letter acronym FTP stand for?___
File Transfer Protocol

### ___What communication model does FTP use, architecturally speaking?___ 
server-client model

### ___What is the name of one popular GUI FTP program?___
FileZilla

### ___Which port is the FTP service active on usually?___ 
21 tcp

### ___What acronym is used for the secure version of FTP?___ 
sftp

### ___What is the command we can use to test our connection to the target?___ 
ping

### ___From your scans, what version is FTP running on the target?___ 
vsftpd 3.0.3 

___A partir du scan des ports ouverts grâce à la commande:___
```
nmap -sC -sV 10.129.141.136
```

On a alors :
![image](https://user-images.githubusercontent.com/81636746/171954297-c9faefa2-0ffd-42ac-a18a-2b4f2738ca4d.png)

### ___From your scans, what OS type is running on the target?___ 
Unix

## Récupérer le flag final
___Se connecter au serveur ftp:___
```
ftp
ftp> open 10.129.141.136
ftp> Login : anonymous
ftp> Password : anonymous
```

___Transférer le flag sur la VM : ___
```
ftp> ls
ftp> get flag.txt
```

___L'ouvrir sur la VM : ___
```
cat flag.txt
```
