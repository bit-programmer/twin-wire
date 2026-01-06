# Twin Wire

* Twin-Wire is a secure, peer-assisted file transfer system designed to enable fast and controlled file sharing between users by combining modern HTTPS-based coordination with dedicated file transfer protocols such as FTPS.
* Instead of routing large files through a central server, Twin-Wire uses a hybrid architecture where a trusted server handles authentication, authorization, and security policies, while the actual file transfer happens directly between clients. This approach reduces server load, improves transfer speeds, and maintains strong access control.
* The system supports multiple client types (web and desktop), where one client can temporarily act as a file host while another downloads the file securely. All permissions, session validation, and security rules are managed centrally, ensuring safe and auditable transfers without exposing sensitive infrastructure.
* Twin-Wire is built as a proof-of-concept for scalable, secure, and efficient peer-to-peer file distribution using a mix of HTTP-based control channels and protocol-optimized data channels.

## FTP (File Transfer Protocol)

* Use to transfer a file across the network
* It uses a client-server model
* **Server** : will host the file
* **client** : will download the file
* In order to connect to ftp server we wanted the host, port, username and password
* Default port of ftp server is 21
* A dynamic port is selected on the client side
* Transport protocol used : TCP
* FTP uses two different connections
  * **Control Connection** : handles all of the ftp commands and instructions such as GET and PUT commands
  * **Data Connection** :
    * When we want to start transferring files, a new connection is established (known as data connection)
    * There are two types of data connection
      * **Active Data Connection** : Server initilized a session (which is often terminated / blocked by the firewall)
        * Random port on client side
      * **Passive Data Connection** : Client initilises a session rather than a server
        * Random port on client side as well as server side
        * Because the client initiated the connection internally, the firewall will happily let the traffic pass without blocking it

## Problems in FTP connection

* It lacks some of the most basic security features (specially encryption)
* The communication between the client and server is in clear text
* This includes login credentials and files being transfered

## Alternatives of FTP

* SFTP (SSH File Transfer Protocol)
* FTPS (File Transfer Protocol SSL)
* TFTP (Trivial File Transfer Protocol)

## FTPS

* FTPS (FTP Secure or FTP SSL)
* is an extension of FTP that supports the use of TLS and SSL encryption

## SFTP

* SSH file transfer protocol
* is an extension of SSH. Not to be confused with FTPS
* Not a part of FTP protocol, but a part of SSH protocol
* uses SSH to securely transfer file

## TFTP

* is a stripped back version of FTP. It provides a very simple way to transfer files quickly and efficiently.
* Used the UDP port 69
* It also does not have any of the bells and whistles of standard FTP
* Authentication and encryption does not exist in TFTP.
* TFTP should not be used when

## SWOT

## My Assumptions

* Will host a ftp server on one computer where we can configure the file permissions
