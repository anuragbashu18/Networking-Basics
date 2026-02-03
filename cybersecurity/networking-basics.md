
## Networking Basics

## These are my personal notes while learning networking fundamentals

# Computer Network----
A computer network is a group of computers and devices connected to each other to share data and resources.

In simple words, when computers are connected with each other — for example, my computer connected to my friend’s computer, or my computer connected to my home Wi-Fi

## Examples:

Home Wi-Fi network

College computer lab network

Office LAN network

## INTERNET

The Internet is the connection of multiple computer networks across regions, countries, or worldwide.

In simple terms:

The Internet is a network of networks.

It is used to access information and communicate online.

## Uses of the Internet:----

Browsing websites,

Sending emails,

Online communication (chat, video calls),

Online learning, payments, and entertainment.

## important 
  you take a example of google what do you think how networks work here 

 ## Very Important line

 Google uses TCP for reliable services like Search, Gmail, and Drive, while UDP is used for real-time services like YouTube streaming and Google Meet.

 ### When you search on Google 

Protocols used:  HTTPS over TCP

What happens:---

You type google.com

Browser sends HTTPS request

HTTPS runs on TCP

TCP ensures:---

All data reaches safely

No packet missing

Google server replies back

## Gmail / Google Drive 

Protocols used:  HTTPS over TCP

Why?

Emails & files are critical

Data loss  unacceptable

Security  required

### HTTPS gives:

Encryption

Authentication

Integrity

# In short:

Emails & files = Secure TCP

## Why TCP here?

Search results must be accurate

Missing data is not allowed

## In short:

Google Search = HTTPS → TCP

# one concern that why HTTPS use over TCP(in example like google )----

    because https provide security - encryption,authentication,integrity 

    imagine you connect with public wifi , without https only tcp what happens your username or password will be visible and also may be possible data is stolen , man in the middle attcak will be happen , also cookies can be stolen 

    if i used https over tcp then our data is safe 

   # example--- 

    if i connected to public wifi then we use browser for something like searching google.com

    so here https works

    https starts and check TLS verification

    it checks server have certification valid or trusted

    if valid then it allow to use and it is safe to use

    https does not check wifi network but it secure the data between user and server (end to end)

    if any unwanted or any kind of situation will happen then browser show warning and say “your connection is not private”

    when we use https and i open any browser then MITM attack is not possible if the certificate is valid and no browser warning is ignored

    because it cant see our data like username, password

    they only see encrypted packets 



## TCP (RANSMISSION CONTROL PROTOCOL)

    the idea is it will insure that data will reach its destination not be corrupted on the way 

    so if you want to share data completely to someone in an applocation that applicaation is used TCP 

   # Characteristics:

    Connection-oriented

    Data order maintain

    Packet loss hua → resend

   # Used for:

    HTTP / HTTPS   

    Website login

    File download

    Email sending (SMTP, IMAP)

    File transfer

    Database communication

    
    # “Jahan data important hai → TCP”

## UDP (USER DATAGRAM PROTOCOL)
you will not care about data is reaching in its destination or not  whomever you want to send the data 

example like video conferencing not all data ,totally fine bythis 

# Use hota hai jab speed > accuracy

# Characteristics:

Connectionless

No resend

Faster than TCP

# Used for:

Video calls (Zoom, Meet)

Live streaming

DNS queries

Online gaming

# important (connection vs connectionless oriented)
 
  connection--
   
   first connection establish then sends the data 
      if data is not received  then resend the data ,because data order is maintened  
      example--email sending ,login any systems etc

   # How it works:

    Client says: Hello, can I connect?

    Server says: Yes

    Client says: Okay, let’s start

  connectionless--
   
   direct sends the data 
    it dont care about data is reached at its destination or not 
    example-- live streaming , video call or online communcation 

 

 ## HTTP (hypertext transfer protocol)

  * it uses a port number- 80( default port)
  * it is not encrypted
  * data send as plain text
  * attack is mostly possible (like MITM ATTACK)
  * it is rarely used in modern tachnology 

   http is a protocol using this data is transfer between client(browser) and web server 

   if i open a website eg- google.com , in which http/*https* send a request to web server and then server response back with the data 
   
   * Most modern websites use HTTPS rather than HTTP due to security reasons. 

## HTTPS (hypertext transfer protocol secure)

 https is secure protocol for data transfer bw client and server 

 * it uses a port number- 443 (default port)
 * it is encypted 
 * data send as encypted form 
 * attack is rarely possible 
 * it is mostly used in modern technology



## PACKETS--
  
  A packet is small or chunks of data (or, small pieces of data )
  
  * when i have a big data it converted into packets (chunks of data ) and at destination , all packets reassemble and form original data 

  # Why data is sent as packets

  Faster transmission of data 

  Efficient use of network

  Easy error handling (lost packet → resend)

  Multiple routes possible (packet switching)

# who exactly convert big data into packets 

* so it is OS KERNEL in which it have TCP/IP protocol which convert data into chunks 

  # worksflows----

  Application (Browser)
          ↓
  OS Kernel (TCP/UDP breaks data)
          ↓
  OS Kernel (IP makes packets)
          ↓
  Network Interface Card (NIC)
          ↓
      Network



# if i have to message to someone example ------

  - How a message like “hello” is sent 

  - User types a message like “hello” in an app (WhatsApp / browser).

  - The application only creates data, it does not create packets.

  - The Operating System (OS) kernel receives this data.

  - The TCP/IP network stack in the OS breaks the data into small pieces.

  - These pieces are converted into packets by adding headers.

  - Packets are sent to the network card (NIC).

  - Packets travel through the network / internet.

  - The receiver’s OS kernel collects the packets.

  - Packets are reassembled into the original message.

  - The application shows the message “hello” to the user.


# exactly how working inside os kernal-----

- Jab app data bhejta hai (example: “hello”)

- App (WhatsApp / Browser) sirf data banata hai.

- App data OS kernel ko deta hai.

- TCP:----

- Data ko chhote parts me todta hai

- Order number lagata hai

- Check karta hai data sahi pahunch raha ya nahi

- IP:-----

- Data ke upar source IP aur destination IP lagata hai

- Ab data packet ban jaata hai.

- Packet network card (Wi-Fi / mobile data) ko diya jaata hai.

- Packet internet par send ho jaata hai.

* Receiver side par------>

* Receiver ka OS kernel packets receive karta hai.

* IP check karta hai address.

* TCP packets ko sahi order me jodta hai.

* Poora data app ko de deta hai.

* App message screen par dikha deta hai.

# how exactly have a work of TCP/IP---

  - TCP aur IP – different but together

  - TCP aur IP dono alag protocols hain.

  - TCP ka kaam:--->>

  - Data ko todna (segments)
  
  - Order maintain karna

  - Data sahi pahunch raha hai ya nahi check karna

  - IP ka kaam:--->>

  - Source aur destination IP address dena

  - Packet ko sahi device tak route karna

  - TCP data handle karta hai,

  - IP address handle karta hai.

  - Dono milkar data ko internet par bhejte hain.


# important note--

 IF i have a big data convert to packets and i have many packet so each packet have differnet source ip and destination ip

  so answer is NO , beacause if i put different ip for source and destination then packets are mismatch not exactly know  which packet belongs to which order  so , i have to write same ip in each packets so in destination all packets are combine and give user origial data.

* EXAMPLE----
  
  Tumhara IP: 10.1.1.5 (like your computer ip )
  Friend ka IP: 20.2.2.8 ( frieind computer ip)

  Tum “HELLO WORLD” bhejte ho → 3 packets bante hain:

  Packet 1 → Source IP: 10.1.1.5 | Destination IP: 20.2.2.8

  Packet 2 → Source IP: 10.1.1.5 | Destination IP: 20.2.2.8

  Packet 3 → Source IP: 10.1.1.5 | Destination IP: 20.2.2.8

  ✔ IP same, ✔ packet number different




# conclusion---

- OS kernel (TCP/IP stack) converts data into packets.

## example like -- what happens  when I open google.com?
    
step 1-- we enter url(https://www.google.com)
     - browser know or read only 
         protocol- https
         domain - google.com

step 2-- DNS resolution ( it is the process of converting domain name into corresponing ip address )

       step1-- browser catch check ( browser apni memory or history check krta h kya maine recently google.com ka ip resolve kiya h if YES, then easily IP mil jata h  ,if, NO , then next step-- )

       step2-- OS catch check ( browser will ask to OS , OS will contain DNS catch , and hosts file if IP found then good else next     step--)

       step3-- OS sends a DNS query to ISP DNS (DNS server provided by your internet service provider || means ISP DNS server checks its DNS catch if ip found then good else next step-- )

       step4-- DNS resolver will ask the authoritative DNS server fir the ip address of google .com

step3-- TCP Connection (3-Way Handshake)

      * Client aur server ke beech reliable connection banta hai:

           - SYN

           - SYN-ACK

           - ACK

step4-- HTTPS / TLS Security

      Browser aur server TLS handshake karte hain

      Encryption keys exchange hoti hain

      Secure encrypted tunnel ban jaata hai ( after that data is encypted)

step5-- HTTPS request ( browser will send https get request to server )     

step6-- data into packets 

step7-- server processing ( google server process-- server receive packets , tcp packets reassemble)

step8-- server response (  like html , css , js images || response bhi data packets me aata hh and also add ip address on those packets)

step9-- browser rendering ( we see the google homepage, html css images all that )      






## IP ADDRESS 

* ip address identify the device , like which device sending the data and which device receiving the data .

## PORT NUMBER----

* port number identify the  which application is sending or recieving the data  in that device.

* port number have 16 bits (total no of ports= 2^16 =~ 65000)

* reserved port (0 - 1023) --( used or reserved by standards network services) -- if i want to create a aplication and i want to run in 80 port number we cant do it because its already reserved by http.
   
   - ex-- 22- SSH,
         80- HTTP,
        443- HTTPS,
        25- SMTP.

* reserved ports(1024- 49151)-  regestered / used ports by application)
 
    - ex-- 3306- mysql,
           3389- rdp,
           8080- http-alt.( http alternative port)

* reserved ports (49152-65535)-- you can use , temporary ports , used by clients ( your browser source port)

* speed of network---

  - 1 mbps (mega bits per seconds)= 1000000 bits/s
  - 1 gbps (gega bits per seconds)= 10^9 bits/s
  - 1 kbps (kilo bits per seconds)= 1000 bits/s


  ## how network connected and how do they communicated  with each other across continent?

  * so answer is under the ocean across contry whaich is fibre optic cable ( you can visit submarine cable in google) 

  * you have a question like why need of cable underwater if satelite is there beacause underwatercable is faster than satelite and more reliable and carry 95%+ of the world's internet traffic.

  # Lan (local area network)------
  


  
 



