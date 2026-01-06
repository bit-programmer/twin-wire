# FTP (File Transfer Protocol)

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

## SWOT

## My Assumptions

* Will host a ftp server on one computer where we can configure the file permissions
