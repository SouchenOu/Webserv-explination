# Webserv-explination






How internet works
-------------------

The Internet is the backbone of the Web, the technical infrastructure that makes the Web possible. At its most basic, the Internet is a large network of computers which communicate all together.


Deeper dive:

A simple network

When two computers need to communicate, you have to link them, either physically (usually with an Ethernet cable) or wirelessly (for example with Wi-Fi or Bluetooth systems). All modern computers can sustain any of those connections.

<img width="639" alt="Screen Shot 2023-03-14 at 6 17 16 PM" src="https://user-images.githubusercontent.com/87101785/225086696-5bb1907e-d76f-4b43-a92a-32c87ec40baa.png">

Such a network is not limited to two computers. You can connect as many computers as you wish. But it gets complicated quickly. If you're trying to connect, say, ten computers, you need 45 cables, with nine plugs per computer!

<img width="639" alt="Screen Shot 2023-03-14 at 6 20 11 PM" src="https://user-images.githubusercontent.com/87101785/225086710-fbb0ce41-849a-4ed3-85e4-aa6691b2a3b8.png">


To solve this problem, each computer on a network is connected to a special tiny computer called a router. This router has only one job: like a signaler at a railway station, it makes sure that a message sent from a given computer arrives at the right destination computer. To send a message to computer B, computer A must send the message to the router, which in turn forwards the message to computer B and makes sure the message is not delivered to computer C.

Once we add a router to the system, our network of 10 computers only requires 10 cables: a single plug for each computer and a router with 10 plugs.

<img width="639" alt="Screen Shot 2023-03-14 at 6 22 37 PM" src="https://user-images.githubusercontent.com/87101785/225087284-f47815f2-2574-438c-a57b-a9068e3e4f0d.png">

<img width="639" alt="Screen Shot 2023-03-14 at 6 34 34 PM" src="https://user-images.githubusercontent.com/87101785/225090304-98770158-9cb2-4e2a-a033-231729fcbd41.png">




1: Web server
-------------

1.1-What is web server?
-----------------------

The term web server can refer to hardware or software, or both of them working together.

1:On the hardware side, a web server is a computer that stores web server software and a website's component files (for example, HTML documents, images, CSS stylesheets, and JavaScript files). A web server connects to the Internet and supports physical data interchange with other devices connected to the web.

2:On the software side, a web server includes several parts that control how web users access hosted files. At a minimum, this is an HTTP server. An HTTP server is software that understands URLs (web addresses) and HTTP (the protocol your browser uses to view webpages). An HTTP server can be accessed through the domain names of the websites it stores, and it delivers the content of these hosted websites to the end user's device.



At the most basic level, whenever a browser needs a file that is hosted on a web server, the browser requests the file via HTTP. When the request reaches the correct (hardware) web server, the (software) HTTP server accepts the request, finds the requested document, and sends it back to the browser, also through HTTP. (If the server doesn't find the requested document, it returns a 404 response instead.)


<img width="663" alt="Screen Shot 2023-03-13 at 4 19 39 PM" src="https://user-images.githubusercontent.com/87101785/224746231-34b20423-0930-4f2f-82d8-663201bbcb06.png">


A static web server, or stack, consists of a computer (hardware) with an HTTP server (software). We call it "static" because the server sends its hosted files as-is to your browser.

A dynamic web server consists of a static web server plus extra software, most commonly an application server and a database. We call it "dynamic" because the application server updates the hosted files before sending content to your browser via the HTTP server.


---->Deeper dive

To review: to fetch a webpage, your browser sends a request to the web server, which searches for the requested file in its own storage space. Upon finding the file, the server reads it, processes it as needed, and sends it to the browser. Let's look at those steps in more detail.

1...Hosting files

First, a web server has to store the website's files, namely all HTML documents and their related assets, including images, CSS stylesheets, JavaScript files, fonts, and video.

Technically, you could host all those files on your own computer, but it's far more convenient to store files all on a dedicated web server because:

A dedicated web server is typically more available (up and running).
Excluding downtime and system troubles, a dedicated web server is always connected to the Internet.
A dedicated web server can have the same IP address all the time. This is known as a dedicated IP address. (Not all ISPs provide a fixed IP address for home lines.)
A dedicated web server is typically maintained by a third party.

1.2-Examples of web server software
---------------------------------------



Below are examples of web server software.

Apache Web Server: official Apache website.

Nginx: official Nginx website.

Boa Webserver: official Boa website.

FoxServ Web Server: official FoxServ website.

Lighttpd: official lighttpd website.

Microsoft's Web Server, IIS: official IIS website.

Savant: official Savant website.

Tomcat: official Tomcat website.



What is TCP/IP ?
--------------

Une suite de protocoles (organisée en couche) utilisés pour le transfert des données sur internet.

C'ést a dire lorsque deux ordinateur veulent communiquer entre eux via internet, les données echangées vont être mises en forme selon des règles qui sont toujours les mêmes afin que chaque machine puissent se comprendre et que le transfert des données soient fiables. Et pour bien comprendre le fonctionnement, on va voir que le TCP/IP et trés facilement comparables a l'envoi de courrier par la poste. Alors par ailleurs, sacher qu'il ya plusieur facons de voir le TCP/IP et pour ma part, j'ai choisi de présenter un modèle en 4 couche.Et le nom de TCP/IP, acronyme de Transfer Control Protocol et internet Protocol  est en réalité le nom des protocoles qui sont le plus souvent utilisés dans la deuxième et la troisième couche.


<img width="530" alt="Screen Shot 2023-03-14 at 10 27 36 AM" src="https://user-images.githubusercontent.com/87101785/224956594-612ce051-2a22-47c7-88cb-b12ed44497c0.png">





Lorsqu'un message arrive dans un ordinateur, de savoir a quelle application s'addresse le message. Par example, le port 80 identifie une application de serveurs web. La machine elle même doit être identifiée, on utilise pour cela la fameuse adresse IP, elle permet, alors de l'acheminement de  données sur le réseau, de déterminer á chaque embranchement, en fonction de cette adresse IP, de savoir quel chemin emprunter.


<img width="2539" alt="Screen Shot 2023-03-14 at 11 11 17 AM" src="https://user-images.githubusercontent.com/87101785/224969414-f420265b-fdf4-4b61-a6c8-f842e16e575f.png">


Enfin, chaque carte réseau qui permet de brancher l'ordinateur au réseau possède elle aussi une identificateur ->l'adresse MAC(Media access control) qui est l'adresse physique d'une machine, Elle permet dans un reseau d'identifier de manière unique.



Supposont que depuis notre navigateur web, nous voulons afficher la page web de facebook.

Plus detaillé:


Sur votre ordinateur on tape www.facebook.com puis Enter, la couche application va traduire cette requête par "GET" qui signifier (obtenir) suivi de l'adresse du site web sous forme d'adresse IP.

<img width="629" alt="Screen Shot 2023-03-14 at 11 36 48 AM" src="https://user-images.githubusercontent.com/87101785/224974651-40711a39-a90c-4a97-91e1-b449963f3732.png">


Dans notre ordinateur les données sont traitées par la couche "transport" qui va ajouter une en tête avec la port source, vous souvenez c'est le numéro qui identifier les applications, ici le port 1337 identifier notre navigateur web, Il est ajouté le port de destination (80 c'est celui qui identifier une application de serveur web) le message est numéroté et il est prévu un FLAG ou (drapeau) en francais qui servira pour l'accusé de reception,( Ici cette case est pour le moment inutilisée). A ce niveau là, on dit que les données ont été encapsulées, c'est a dire que l'on a ajouter une entête "transport" au message "GET http". 


<img width="629" alt="Screen Shot 2023-03-14 at 11 42 48 AM" src="https://user-images.githubusercontent.com/87101785/224976220-9435ddaa-6d07-4e47-b987-abdd5edc254a.png">

Ce nouvel ensemble de données est alors appelé un "Segment"

<img width="629" alt="Screen Shot 2023-03-14 at 12 10 29 PM" src="https://user-images.githubusercontent.com/87101785/224983522-f8098860-01eb-4380-a777-821dfc1bb797.png">

Dans l'ordinateur, le segment est encapsulé par la couche 2 "internet" qui ajoute l'adresse IP de destination(Dont cette cas c'est l'adresse IP du serveur qui héberge la page web du site facebook) et l'adresse IP source (C'est a dire l'adresse IP de notre ordinateur). A ce niveau, l'ensemble de cette données et appelée "paquet". 

<img width="629" alt="Screen Shot 2023-03-14 at 12 15 43 PM" src="https://user-images.githubusercontent.com/87101785/224984687-76f1a525-771f-4b5b-8e79-3cbb3d92b3a7.png">


La couche réseau encapsule le paquet en lui ajoutant une entête avec l'adresse MAC de la carte réseau de destinations du prochain routeur et l'adresse MAC de la carte réseau de notre ordinateur, et ici on a ce que l'on appelle une "Trame". Alors, voyons la suite ou les messages


<img width="1772" alt="Screen Shot 2023-03-14 at 12 20 24 PM" src="https://user-images.githubusercontent.com/87101785/224985821-3968746f-1e6e-4433-8c6e-d2ffb5e9243a.png">




En bas notre trame quitte notre ordinateur et arrivent au premier routeur, la carte reseau du routeur a son adresse MAC ici


<img width="1826" alt="Screen Shot 2023-03-14 at 2 36 22 PM" src="https://user-images.githubusercontent.com/87101785/225018286-76afee95-2b9a-4eb2-b202-d99055964fd4.png">





et quand l'adresse MAC de destination est bonne , la trame est désencapsulée et l'adresse IP de destination est lue 


<img width="1826" alt="Screen Shot 2023-03-14 at 2 36 06 PM" src="https://user-images.githubusercontent.com/87101785/225018394-48f5f077-dc54-43c7-8b72-3ae6cfd4287b.png">

Alors le paquet est a nouveau  encapsulé et l'adresse MAC src est ajoutée ainsi que l'adresse MAC du prochain routeur.


<img width="1826" alt="Screen Shot 2023-03-14 at 2 41 31 PM" src="https://user-images.githubusercontent.com/87101785/225019721-c296a409-3eed-4519-b1d7-83f7b5d55de1.png">

Alors pour information, les prochaine adresse MAC sont connus par le routeur (grace a ca table de routage) .

En suit la TRAME voyage et arrive au routeur suivant. L'adresse MAC est identifier 

<img width="1826" alt="Screen Shot 2023-03-14 at 2 52 19 PM" src="https://user-images.githubusercontent.com/87101785/225023026-eb8c2301-d93a-4497-a8a3-9aff815d91ef.png">

la trame est donc désencapsulée, 


<img width="1826" alt="Screen Shot 2023-03-14 at 2 55 08 PM" src="https://user-images.githubusercontent.com/87101785/225023736-e7022eed-6be6-4a89-8330-968ffe89ea78.png">





la lecture de l'adresse IP de destination entrain une nouvelle encapsulation ou est ajoutée l'adresse MAC de la carte reseau source et celle de destination 


<img width="1826" alt="Screen Shot 2023-03-14 at 2 54 53 PM" src="https://user-images.githubusercontent.com/87101785/225023770-38971ce8-e2ad-4004-b5c6-3d2093cde62b.png">

<img width="1826" alt="Screen Shot 2023-03-14 at 2 57 44 PM" src="https://user-images.githubusercontent.com/87101785/225024382-b8ad5301-dbdc-4f65-8dac-0a2db6954d93.png">


aprés notre trame arrive dans le serveur de facebook, dans le serveur, comme l'adresse MAC correspond á celle de la carte réseau , la trame est désencapsulée et remontre vers la couche internet 

<img width="2174" alt="Screen Shot 2023-03-14 at 3 01 46 PM" src="https://user-images.githubusercontent.com/87101785/225025419-9ffd538e-7cf9-4bad-97a1-8e5f578fbc88.png">

dans notre serveur l'adresse IP etant bien celle de destination

<img width="502" alt="Screen Shot 2023-03-14 at 3 04 38 PM" src="https://user-images.githubusercontent.com/87101785/225026137-47d62a57-c044-4ac4-8d03-366c1ed9a9b8.png">

le paquet est cette fois, lui aussi désencapsulé et remonte vers la couche transport  

<img width="502" alt="Screen Shot 2023-03-14 at 3 06 22 PM" src="https://user-images.githubusercontent.com/87101785/225026655-733f3561-d914-41ad-a7de-67caf64cbea9.png">

La couche transport voire que les données sont adressées au port 80, c'ést a dire je vous rappele l'application du serveur web, le segment est alors desencapsulé et remonte a la couche application  

<img width="502" alt="Screen Shot 2023-03-14 at 3 09 16 PM" src="https://user-images.githubusercontent.com/87101785/225027493-74dddca0-c892-49ec-8c04-b76faa3fc531.png">


et a la fin la couche application transmet la requete a l'application du serveur web.


Alors ! Les message sont arrivés au destinataire







mais comment l'expéditeur va t-il le savoir?


les port source et destination sont inversés, le numero du message est augmenté de 1, donc il passe a 2, c'est la manière de savoir que l'accusé de réception fait suite aux messages précédents, et le FLAG va être maintenant utilisé en y inscrivant ACK qui signifie en anglais (Acknowledgment)

<img width="502" alt="Screen Shot 2023-03-14 at 3 33 04 PM" src="https://user-images.githubusercontent.com/87101785/225034360-dc7f859e-d5c7-4060-955f-3fd49779c456.png">

<img width="502" alt="Screen Shot 2023-03-14 at 3 33 36 PM" src="https://user-images.githubusercontent.com/87101785/225034559-a6c99cd1-7fa9-4a07-83ec-1dbbc5e29b47.png">

<img width="502" alt="Screen Shot 2023-03-14 at 3 33 50 PM" src="https://user-images.githubusercontent.com/87101785/225034571-d2ad2542-4af5-4459-b451-c41903db77b2.png">


c'ést a dire "accusé de réception", sous entendu -->"jai bien recu le message".

Alors ce message est vide, vous aurez remarqué ici que la partie "application" est vide c'est seulement l'enveloppent qui va voyager donc ce message vide va être a son tour encapsulé par la couche internet 

<img width="502" alt="Screen Shot 2023-03-14 at 3 36 26 PM" src="https://user-images.githubusercontent.com/87101785/225035307-dfd3c2b4-1edf-48b6-830a-d0b3ce82f830.png">


et aprés l'adresse IP de destination est inversée avec l'adresse IP source 



<img width="502" alt="Screen Shot 2023-03-14 at 3 39 02 PM" src="https://user-images.githubusercontent.com/87101785/225036071-a61a70ee-c764-49b2-ac59-70db9307db4f.png">





et puis le  paquet est encapsulé par la couche "réseau"


<img width="1606" alt="Screen Shot 2023-03-14 at 3 40 11 PM" src="https://user-images.githubusercontent.com/87101785/225036537-e3608c02-a288-45c9-b5ad-8b8778a4b527.png">


aprés l'adresse MAC sont mis a jour puis la trame repart sur réseau internet jusqu'a notre ordinateur


<img width="1606" alt="Screen Shot 2023-03-14 at 3 42 08 PM" src="https://user-images.githubusercontent.com/87101785/225056398-26f3017f-fca4-4504-94bf-5cb13f34c8cc.png">





<img width="2523" alt="Screen Shot 2023-03-14 at 3 43 31 PM" src="https://user-images.githubusercontent.com/87101785/225037539-23728bbe-cbce-4199-9e30-4fdfbbbef906.png">




------------------------------------------------------------------------------------------------------------------------

TCP/IP stands for Transmission Control Protocol/Internet Protocol and is a suite of communication protocols used to interconnect network devices on the internet. TCP/IP is also used as a communications protocol in a private computer network (an intranet or extranet).

TCP defines how applications can create channels of communication across a network. It also manages how a message is assembled into smaller packets before they are then transmitted over the internet and reassembled in the right order at the destination address.






levels:

<img width="594" alt="Screen Shot 2023-03-13 at 11 40 29 AM" src="https://user-images.githubusercontent.com/87101785/224678598-0ee5e092-87ee-4f82-9a25-de47e4ae8cf9.png">



TCP/IP carefully defines how information moves from sender to receiver. First, application programs send messages or streams of data to one of the Internet Transport Layer Protocols, either the User Datagram Protocol (UDP) or the Transmission Control Protocol (TCP). These protocols receive the data from the application, divide it into smaller pieces called packets, add a destination address, and then pass the packets along to the next protocol layer, the Internet Network layer.

The Internet Network layer encloses the packet in an Internet Protocol (IP) datagram, puts in the datagram header and trailer, decides where to send the datagram (either directly to a destination or else to a gateway), and passes the datagram on to the Network Interface layer.

The Network Interface layer accepts IP datagrams and transmits them as frames over a specific network hardware, such as Ethernet or Token-Ring networks.

<img width="1279" alt="Screen Shot 2023-03-13 at 5 24 16 PM" src="https://user-images.githubusercontent.com/87101785/224764069-84c5588b-7c43-47d0-9acc-d839623a98a4.png">




What is OSI?
-----------

The OSI reference model defines how applications can communicate over a network.

 🌱 What is HTTP?
------------

The Hypertext Transfer Protocol (HTTP) is the foundation of the World Wide Web, and is used to load webpages using hypertext links. HTTP is an application layer protocol designed to transfer information between networked devices and runs on top of other layers of the network protocol stack. A typical flow over HTTP involves a client machine making a request to a server, which then sends a response message.


C'est un protocole la plus utiliser sur internet, il pêrmet un navigateur d'obtenir des page web.

le navigateur web est une application client qui accède aux ressources stockees sur un serveur web.

Lorsque une URL est saisie au niveau des navigateur web client, le client http envoyer un requête http au serveur, le protocole http au niveau de serveur http s'éxecute en arriere plan, donc il s'agie d'un service, donc ce service il va traiter la requête http et il envois ce que n'appele une reponse http.


 🌱 La structure d'une requite HTTP:
-----------------------------------





<img width="446" alt="Screen Shot 2023-03-10 at 11 55 16 AM" src="https://user-images.githubusercontent.com/87101785/224298314-ffc5c25c-f99f-45c6-a59b-156489bba8b5.png">




💬💬💬💬💬💬💬💬💬💬💬-------------------------------->Une requête http comprend 3 parties :💬💬💬💬💬💬💬💬💬💬💬💬
*******************************



📫 1 ******: une ligne de commades: 📫

-> La ligne du commande il est composer de trois partie:

🔭 Partie 1: 

La methode-> qui peux être sois de type :

👨‍💻 GET ---> demander des page HTML (La requête http il est envoyer pour demander une page html)

👨‍💻 HEAD ---> le client il est entrain de demander a travers la requête http des informations sur une ressource sans demander la ressource elle-même.

👨‍💻 POST---->  envoyer des donnéer saisies dans un formulaire integré a une page web au serveur web (Quand le client saisie ses informations dans un formulaire et ses informations il vont être envoiyer dans une requête http)

🔭 Partie 2:


URL-> Pour identifier la ressource

🔭 Partie 3:


Il dois être séparer du reste de la requête par une ligne vide. Il contient les donner a fournir au serveur(cet partie il est utiliser lorsque le client il veux envoyer des donner au serveur).



📫 2 ********: Une liste d'entêtes avec leur valeur 📫 

📫 3 ********: Le corps de la requêtes(facultatif). 📫





💬💬💬💬💬💬💬💬💬💬💬💬💬--------------------------------> Réponse HTTP:💬💬💬💬💬💬💬💬💬💬💬💬💬💬💬💬
*********************************************************************




Une reponse HTTP contient des donner envoyer depuis le serveur (Les donner recue peuvent être  de différent types(Données en text clair ou html, blug-in donnees nécessitant un autre service au programme ou .....))

Pour aider le navigateur a determiner le type de fichier qu'il recois, le serveur indique le type de donner que contient le fichier



 🌱  example:
------------


<img width="810" alt="Screen Shot 2023-03-10 at 12 22 38 PM" src="https://user-images.githubusercontent.com/87101785/224303727-09e580df-3f57-45f8-bd55-3676f36524a7.png">

l'utilisateur saisie URL suivant : http://www.example.com

les etapes:

1: Le navigateur interprète les trois partie de L'URL(Uniform ressorce locator):

il saura que :

*Le protocol--> HTTP

*Le nom du domaine --> www.example.com

*resource demainder --> c'est la page index.html

2: a partir du prefix http du URL, le navigateur determine que le protocole a utiliser est http, ainsi il definie 80 comme numéro de port destination et un numéro aléatoire comme numéro de port source. 

3: cash DNS qui est consulter pour extraire l'address IP qui correspont le nom du domaine



<img width="1901" alt="Screen Shot 2023-03-10 at 12 36 05 PM" src="https://user-images.githubusercontent.com/87101785/224306249-8604456e-7ecd-485d-b018-cb54e7422207.png">


donc ici une requête http est envoyer au serveur consérner, aprés le serveur il va traiter la requéte et apres il va envoyer la ressouce demander (la page www.example.com/index.html)



------------------------------------------------------------------------------------------


HTTP : Hyper-text-Transfer-Protocol basically responsible for communication between web servers and clients, it is the protocol of the web, so every time you open your browser and you visit a web-page or you submit a form, or you click a button than sends some kind of ajax request or fetch request, something like that you are using HTTP and you are going through what is called the request and response cycle. You make a requeste and you get a response back that has something called headers and something called the body, and we are going to look more into that cycle in a bit.

http is stateless, meaning that every request is completely independent, when you make one request visiting a web page or go to another page after that,
or reload the page it dosent remember anyting about the previous, you can kind of look at each request as a single transaction.

HTTPS: Hyper-text-Transfer-Protocol-secure(Data sent is encrypted) it basically where all the data that is sent back is encrypted by something called SSL which stands for secure sockets layer or by TLS which is transport security layer, so anytime you have users that are sending sensitive information 

it should always be over https especially if it is like credit card data, social security numbers, you want to have a hight level of security for that stuff.

A lot of websites and applications now are just forcing https on every page which is a bad idea, you can do this by installing an ssl certificate on your web host, there is different level of security.


Al right when a request is made to a server it has some kind of method attached to it, and there is more than this .


GET: a get request is used to get or fetch data from the server, it could be just loading a standard HTML page, loading assets like CSS or images JSON data XML data, so everytime you visit a webpage you are making a get request to the server via HTTP.

POST: post request is usually used when you are posting data or when you are adding something to the server(adding a ressource) or when you submit a form like let's say a contact form you will be making a post request, if you are submitting maybe a blog post or creating a blog post that is gonna be a POST request, you are sending data to the server and typically that data will be stored in a database somewhere. we can also have forms that make GET request but it is less secure.

PUT : put request which is used to update data that is already on the server so if you have a blog post you want to edit it, maybe change the image or change some text, typically you do that with a put request.


Delete: delete request just delete data from the server.





With each request and response using HTTP  we have something called the header and something called the body

<img width="937" alt="Screen Shot 2023-03-13 at 2 50 42 PM" src="https://user-images.githubusercontent.com/87101785/224721630-8d929d10-09e8-4aac-ae19-8ecd68716fab.png">


The body typically with a response is going to be the html page that you are trying to load  the json data whatever is being sent from the server and then when you make a request you can also send a request body for instance when you submit a form, the form fields you are submitting are part of the request body.

When you comes to the header you also have a request headers and response headers in something called a general header, it is basically divided into three parts and there is different fields on each parts 

<img width="2390" alt="Screen Shot 2023-03-13 at 3 06 39 PM" src="https://user-images.githubusercontent.com/87101785/224725654-6b07a55c-48b8-41d2-9dce-065024d1aef9.png">

A header will look something like this, you will make a (Method like a GET request)(Path or URL)(with aprotocol in this case http) and have all this different header fields and a lot of this you are not really  going to care about but it is good to know what some of the more common ones 
do and what they are especially with the general part of it.

so in general we have --->

request URL: It is just the URL you are requesting 

Request Method : so if it is a get request, post request .....

Statues code: it is probably the most important 

Remote address: which is the ip of the remote computer.

Referrer Policy: if you go to a page from another page it might have some information and that and whatever the poll referrer policy  is.



In Response we have --->

server : so if it is apache or nginx or something like that, and a lot of times this will be hidden just to prevent hackers from knowing what type of server the website uses.

Set-Cookies : is used for servers to send small pieces of data called cookies from the server to the client.

content type : so every response has a content type for instance if it is an html page it will have a content type of text/html, css files would be test/css, images will have image/png or image/jpeg.

Content-Length: Content length which is just that it is the length, it is in octets.

In request we have --->

Cookies: if you have a cookie that was previously sent by the server and you need to send it back to the server you would do it in this field 

Accept-xxx: Like accepting coding, accepting character set , accepting language.

Content-Type: if you are sending data like lets say you are sending json, you had want to set this to application/json

Content-Length: 

Authorization: remember that http is stateless so you might need to send some type of token withing the header , the authorization and the header so that you can for instance validate a user to access a protected route or a protected page, unless you are using something like session on the server .

User-Agent: is typically a long string that has to do with the software that the user is using the operating system, the browser think like that .

Referrer: referrer has info regarding the referring site, if you are to click on a link or whatever

------------------------------------------------------------------------



2: Protocole:
************************


2.1: What is protocole:
----------------------

a protocol can be defined as a set of rules convensions and data structures that dictate how devices extchange data across a networks. In other words network protocols can be equated to languages that two devices most understand for seamless communication of information, regardless of their infrastructure and design desparities.

A network protocol is an established set of rules that determine how data is transmitted between different devices in the same network. Essentially, it allows connected devices to communicate with each other, regardless of any differences in their internal processes, structure or design. Network protocols are the reason you can easily communicate with people all over the world, and thus play a critical role in modern digital communications.

Similar to the way that speaking the same language simplifies communication between two people, network protocols make it possible for devices to interact with each other because of predetermined rules built into devices’ software and hardware. Neither local area networks (LAN) nor wide area networks (WAN) could function the way they do today without the use of network protocols.


Protocols are sets of rules for message formats and procedures that allow machines and application programs to exchange information. These rules must be followed by each machine involved in the communication in order for the receiving host to be able to understand the message.

2.2: List of Network Protocols:
-------------------------------

There are thousands of different network protocols, but they all perform one of three primary actions:

1-> Communication

2->Network management

3->Security


----------DNS:

Domain name system. DNS is a database that includes a website's domain name, which people use to access the website, and its corresponding IP addresses, which devices use to locate the website. DNS translates the domain name into IP addresses, and these translations are included within the DNS. Servers can cache DNS data, which is required to access the websites. DNS also includes the DNS protocol, which is within the IP suite and details the specifications DNS uses to translate and communicate.

--------DHCP:

Dynamic Host Configuration Protocol. DHCP assigns IP addresses to network endpoints so they can communicate with other network endpoints over IP. Whenever a device joins a network with a DHCP server for the first time, DHCP automatically assigns it a new IP address and continues to do so each time a device moves locations on the network.

When a device connects to a network, a DHCP handshake takes place, where the device and DHCP server communicate. The device establishes a connection; the server receives it and provides available IP addresses; the device requests an IP address; and the server confirms it to complete the process.

Every device on a TCP/IP-based network must have a unique unicast IP address to access the network and its resources. Without DHCP, IP addresses for new computers or computers that are moved from one subnet to another must be configured manually; IP addresses for computers that are removed from the network must be manually reclaimed.



---------FTP:

FTP stands for File transfer protocol.

FTP is a standard internet protocol provided by TCP/IP used for transmitting the files from one host to another.

It is mainly used for transferring the web page files from their creator to the computer that acts as a server for other computers on the internet.

It is also used for downloading the files to computer from other servers.




Objectives of FTP:

It provides the sharing of files.

It is used to encourage the use of remote computers.

It transfers the data more reliably and efficiently.



--------IP:

The Internet Protocol (IP) is a protocol, or set of rules, for routing and addressing packets of data so that they can travel across networks and arrive at the correct destination. Data traversing the Internet is divided into smaller pieces, called packets. IP information is attached to each packet, and this information helps routers to send packets to the right place. Every device or domain that connects to the Internet is assigned an IP address, and as packets are directed to the IP address attached to them, data arrives where it is needed.

Once the packets arrive at their destination, they are handled differently depending on which transport protocol is used in combination with IP. The most common transport protocols are TCP and UDP.

--------Telnet:

TELNET stands for Teletype Network. It is a type of protocol that enables one computer to connect to local computer. It used as a standard TCP/IP protocol for virtual terminal service which is provided by ISO. The computer which starts the connection is known as the local computer. The computer which is being connected to i.e. which accepts the connection known as the remote computer. During telnet operation, whatever is being performed on the remote computer will be displayed by the local computer. Telnet operates on client/server principle. The local computer uses telnet client program and the remote computers uses telnet server program. 


------TCP/UDP:

TCP et UDP se trouvent dans la quatrième couche du modèle OSI qui est la couche de transport juste au-dessus de la couche IP. TCP et UDP les deux supportent la transmission de données de deux manières différentes, TCP est en mode orienté connexion et UDP est en mode non-connecté.

TCP est un protocole fiable de bout en bout orienté connexion pour garantir la transmission de données. Certaines des principales caractéristiques de TCP sont (SYN, SYN-ACK, ACK), la détection d’erreur, le démarrage lent, le contrôle de flux et le contrôle de congestion.

UDP est un protocole de transmission simple qui fournit un service non fiable. Cela ne signifie pas que UDP ne fournira pas les données mais il n’y a pas de mécanismes pour surveiller le contrôle de congestion ou la perte de paquets, etc. Comme c’est simple, cela évite le traitement du congestion. Les applications en temps réel utilisent principalement UDP car la suppression des paquets est préférable. Un exemple typique est celui des flux de média (Streaming)

🌱 Ressources:
------------

https://www.youtube.com/watch?v=auhEJDGHI8Q

https://www.youtube.com/watch?v=2JYT5f2isg4

https://www.youtube.com/watch?v=YqEqjODUkWY&list=PLPUbh_UILtZW1spXkwszDBN9YhtB0tFKC&index=2

https://developer.mozilla.org/en-US/docs/Web/HTTP


https://www.youtube.com/watch?v=iYM2zFP3Zn0

https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_web_server

https://www.youtube.com/watch?v=_0thnFumSdA&t=41s
