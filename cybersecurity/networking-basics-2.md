
# protocols in application layer ---
 
       - web protocols
         --  Tcp/Ip:  
                 - HTTP-- [Get,Post,Put,Delete]
                 - DHCP
                 -FTP
                 - SMTP
                 - POP3 & IMAC
                 - SSH
                 - VNC
        -- Telnet--- port 23
        --UDP--

        -- sockets--

        --ports: --   Emphmeral ports

        -- status code--   1xx - infirmation code
                           2xx - sucess code
                           3xx - redirecting purpose 
                           4xx - this is client error
                           5xx - server error
                  
       -- cookiees- unique string 
                   - it store in client browser
                  ex  - when you visit the any website very first time , it will set a cookie
                     and after that whenever you revisit that website and make a new request in that request header a cookie will be send then the server will know ohh the request is coming from anurag ,and anurag is send me a cookie , let me check my database then the server will check the database and it will find the state for that.
                -- in http request you will send a cookie and vice versa for http 
                
            -- types- session
                     - persistant

            -- sometimes cookie will use hack possibility.

       -- third party cookie --- cookies that are set for the url that you donot visit 
                             -- third party cookies are cookies created and stored by a domain other than the website a user is currently visiting, mainly used to track user activity across multiple websites for advertising and analytics purposes
                            - or simple defination-- 
                                    - cookies from another websites that track you 

        * how email works?-- elctronic mail is used to exchange message over the internet.
                   - SMTP (Simple mail transffer protocol) - it is used to sending email from client to mail server.
                         -- port:25
                   - POP3 (post office protocol version 3) - it is used to receive emails by downloading them from mail server to local 
                                                             devices
                         -- port: 110
                   - IMAP (internet message acess protocol) - it is a protocol used to access and manage emails directly on the mail 
                                                              server without downloading them 
                         -- port:143
                