
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

 Google uses TCP for reliable services like Search, Gmail, and Drive, UDP is usewhile d for real-time services like YouTube streaming and Google Meet.

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

example like video conferencing not all data ,totally fine by this

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

  * LAN is a network that connects computers and devices within a small geographical area.

  * it is high sped more secure.

    ex--   your home wifi connected with home Laptop , mobile, smart tv etc

 # man(metropolitan area network)

    * MAN is a network that connects across city like patna
    * intrnet network across patna city 
    * in MAN = multiple LAN network

    ex--- tv cable network across city 

 # wan(wide area network)
  
    * wan is network in which access across state / country
    * speed is comparetively low because of long  distance, many routers , many satelite , heavy traffic 

    ex--INTERNET uses across country ,
        bank network across country   

  # modem and router
  -- MOdulator + DEModulator

  * it is a device which takes internet signal from isp (internet service provider) and convert into digital signal then gives to router

   Ex--- * Airtel/Jio fiber at home(it is a combo of modem and router )

   **   IN past days we are using modem and router seperately like 2 physical devices boxex  but IN  PRESENT DAYS we are using in one single devices like airtel /jio fibre it have inbuilt both modem and routers 
          

  **  Modem and Router working:

   A modem receives the internet signal from the ISP and converts it into digital data.
    This digital data is then sent to the router.
    The router distributes this data to different devices and provides internet access to devices like smartphones, laptops, and computers through Wi-Fi or LAN cables.

   **  Router--
        A router is a networking device that takes internet from the modem and distributes it to multiple devices like phones, laptops, and computers.
           

  ## TOPOLOGIES

  * bus--
     
  - bus topology means computers are connected with one main single cable
 - if it broke all computer will dosconnect and not working 
   - and only one persons can sends data at a time 

    Advantage---
      easy to install 
      cheap
      less cable required

    limitations 
    - hard to troubl shoots 



  * ring--Each computer is coonected in a circle (ring)
          - data travels in one direction 

          Advantage--
          - no data collison
        - equal acess to all devices 

        limitations
        - one device fails whole network fails 
        - difficult to add new devices 
        - hard to troubeshoot

  * star--All devices connected to one central device (router/switch).
  
    - example- home wifi network or office network

      - Advantages

          - Easy to manage

          - If one cable fails → only one device affected

          - Fast

   -  Limitations

       -  Central device fails  whole network down

       -  More cable needed

        - Cost higher

  * tree--bus and star combination / hierarchial structure like tree

  - Example

   -  Big office network

    - School network

 -  Advantages

  -   Easy to expand

   -  Good for large networks

   -  Organized structure

  -  Limitations

      - If backbone fails → big problem

     -  Expensive

      - Complex


  * mesh--Every device connected to every other device.

    -  Example

          Internet backbone

          Military network

  -  Advantages

      Very reliable

      If one link fails → network still works

      High security

 - Limitations

      Very costly

      Too many cables

      Complex setup


  ## structure of network

  * OSI model -- OSI model is a 7- layer framework that explains how data travel from one device to another over the network 

  Layer No      	Name

    7         	Application
    6          	Presentation
    5         	Session
    4         	Transport
    3          	Network
    2          	Data Link
    1         	Physical
  
  * Application layer--
      
      - this is the top layer of OSI model 
      - it is closest to user 
      - provides network serveice to application
      - user interact here

      - PROTOCOLS -
          - HTTP/HTTPS
          - FTP
          - SMTP(email)
          - DNS
      - Example-
          - you open chrome -> search google -> then this layer works 

   * Presentation layer-  what it does - -data formatting,encryption &  decryption,compression  (Makes data secure & readable)

      - data formatting - convert data into a standard format so sender and receiver can understand 
               -  Why needed?

                      - Different systems use different formats → need common format.

                      -  Example

                        Text → ASCII / Unicode

                        Image → JPEG, PNG

                        Audio → MP3

                       - If one system sends “text”, other system must understand same format.
  
      - Encryption&decryption- secure data 

      - compression- it reduces the size of file to send faster 

      - PROTOCOLS / EXAMPLE--
           - SSL/TLS
           - JPEG,MP3 formats
      - example-- https website -- data encrypted hota h 

    * SESSION layer --  it manages communication between two devices that means -three main functions ---
                        - start connection
                       -  keep connection alive 
                        - end connection properly

              - start connection-- Before data transfer, session layer creates a connection.
                              - ex-- you open whatsapp, you login to instagram ,  you connect to website 

              - keep connection alive (session maintenance)-- Keeps session active
                                                              Syncs communication
                                                              Handles interruptions

                              - ex- you watching youtube if internet is slow down -> video pause -> then resume 

              - end connection-- closes connection properly 
                           ex- logout from website , closes app 


    * TRANSPORT LAYER--- it ensures that data is deleivered correcty from sender to receiver.

                    Main Functions ---
                      1.Segmentation-- it divide(break ) large no of data into small segments or packets .
                                      - due to this data transfered is fast 
                      2. Reassemble--- it joins all small segments or packets in Receiver side   

                      3. Error Detection and Recovery--- it will check data receive is correct or not if not then resend like one   
                                                          packets is missing then it will recover again from resend the data.
                      4.Flow control--- control data speed betwen sender and receiver
                                    ex- sender fast and receiver slow == adjust speed data 
                      5.port adressing -- each application has a port number 
                                    ex-- http-80
                                         https-443
                                         ftp-21
                       port=  TCP AND UDP --- tcp is ensures data is reched safely on reciver side 
                                          tcp is conection oriented 
                                          it have slower speed 
                                          ex-gmail , google drive 

                                          UDP doesnot care about data is reached at destination or not 
                                          it is connectionless oriented
                                          it have hiher speed 
                                          ex- google meetings , watching youtube video 

      * Network layer --- The Network Layer is responsible for the transmission of data packets from one computer to another across 
                          different networks using logical addressing and routing.   

                          Main work:
                            It is responsible for routing (path selection) and logical addressing (IP address)  

                            main functions--
                               1.logical adressing---Every device gets a unique IP address
                                                 ex--Example---
                                                              Your phone → 192.168.x.x (local IP)
                                                              Websites → public IP

                               2.  Routing(path selection)   ---Finds best path from sender to receiver
                                                              - it Uses routers      
                                                    Example---
                                                         --   You send request to Google → data travels through multiple routers
                                                         --   Chooses shortest/fastest path   
                              3. packet forwarding--Moves packet from one router to another
                                                    Step-by-step delivery   

                              4. fragmentation--Breaks large packets into smaller ones
                                                Needed when network size limit hota hai  

            -----  Devices used in network layer is 
                    - Router (MOST IMPORTANT)                                 


                        @ important --You break big item into parts → Segments
                                      Then you put address & route → becomes Packet

                                   -   What is Segment?
                                               A segment is a piece of data created by the Transport Layer
                                     - what is packets?         
                                                A packet is a segment + IP address info, used by Network Layer

                                  | Feature  | Segment             | Packet               |
                                  | -------- | ------------------- | -------------------- |
                                  | Layer    | Transport           | Network              |
                                  | Contains | Port numbers        | IP addresses         |
                                  | Work     | End-to-end delivery | Routing              |
                                  | Purpose  | Divide data         | Send across networks |

                          
      * data link layer--it will add mac address to the packets and called is as a frame and then send it.
                         Main work:
                                  -  Provides node-to-node (local) communication within the same network.
                                   - It ensures data goes from one device to another device in the same LAN

                         main functions--
                         1️ Framing
                               What happens?
                              Takes data from Network Layer (packet)
                              Converts it into frames

                               Frame = packet + MAC address + error info

                         2️ Physical Addressing (MAC Address)
                               What is MAC?
                              Unique hardware address of device
                              Example: 00:1A:2B:3C:4D:5E     (alphanumeric 12 digit mac)

                               Used for local delivery

                         3️ Error Detection
                               What happens?
                              Checks if data is correct
                              Uses methods like CRC

                               If error -> data rejected

                         4️ Flow Control
                               What happens?

                             - Controls speed between sender & receiver
                              - Prevents data overload

                         5️ Access Control
                               What happens?

                             - Decides who can use network at a time
                              - Prevents collision

                              -- Devices used
                                    Switch (MOST IMPORTANT)
                                   Bridge


      * physical layer --
                         Main work:
                           - It is responsible for actual transmission of raw bits (0s and 1s) through physical medium.

                           - This is the hardware level of networking    

                main functions---
                             1️ Bit Transmission
                                   What happens?
                                  Converts data into binary bits (0 and 1)
                                  Sends it as signals

                                   signals can be:

                                  Electrical (copper cable)
                                  Light (fiber optic)
                                  Radio (Wi-Fi)
                                  
                                 -- Data ko 0 aur 1 me convert karke signal ke form me bhejta hai

                             2️ Physical Media
                                   What it includes?
                                  Cables
                                  Connectors
                                  Wireless signals

                              --  Examples
                                    Ethernet cable
                                    Fiber optic cable
                                    Wi-Fi signals

                                 -- Actual wire aur medium jisse data travel karta hai

                             3️ Signal Encoding
                                   What happens?
                                  Converts bits into signals
                                  Defines voltage/light levels

                                   Example:
                                      1 = high voltage
                                      0 = low voltage

                             4️ Data Rate (Speed)
                                   What happens?
                                  Defines how fast bits are transmitted

                                   Example:
                                      100 Mbps
                                      1 Gbps

                             5️ Synchronization
                                   What happens?
                                  Keeps sender & receiver in sync

                                   So bits are correctly received

                                    Devices used
                                    Cables
                                    Hubs
                                    Repeaters

                               ---    Real-life Example

                                   Sending file via LAN cable:

                                        Data comes from upper layers
                                        Converted into bits
                                        Sent through cable as electrical signals
                                        Receiver gets signals → converts back                  


                ()important---
                             Transport → Segment
                             Network → Packet
                             Data Link → Frame
                             Physical → Bits

                             