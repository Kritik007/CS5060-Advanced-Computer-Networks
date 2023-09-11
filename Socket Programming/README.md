<p align="center">
  <a href="https://github.com/Kritik007//CS5060-Advanced-Computer-Networks/tree/main/Socket%20Programming"></a>
  <h3 align="center">Socket Programming</h3>
  <p align="center">Programming Assignment (Socket Programming) Completed for the course CS5060-ACN.
    <br/>
    <br/>
    <a href="https://github.com/Kritik007//CS5060-Advanced-Computer-Networks/tree/main/Socket%20Programming"><strong>Explore the codes »</strong></a>
    <br/>
    <br/>
  </p>
</p>



## Table Of Contents

* [About the Project](#about-the-project)
* [Built using](#built-using)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [License](#license)
* [Authors](#authors)
* [Acknowledgements](#acknowledgements)

## About The Project
<div align="justify">
  The assignment is based on Socket Programming. In order to complete it, we first had to analyse a straightforward Python Ping server and create a corresponding client. These programs offer functionality similar to that of the conventional ping programs found in contemporary operating systems. However, these programs communicate with one another using the less complex UDP/TCP protocol rather than the default Internet Control Message Protocol (ICMP). The ping protocol enables a client system to send a packet of data to a remote machine, and the remote machine to return the data to the client in uppercase (a process known as echoing loud!). The ping protocol, among other things, enables hosts to ascertain the travel time between two machines, i.e., round-trip-time.
</div>

## Built using
<div align="justify">
  I chose C++ over Python for Socket Programming. The main reason is that C++ has better performance, better resource management, and better support for low-level networking, which is critical for building fast and responsive networking apps.
</div>

## Prerequisites
Before running the Project, ensure you have the following prerequisites:

- A C++ development environment (e.g., g++ compiler)
- Basic understanding of socket programming
- Access/Knowledge of a UNIX System/Commands preferably Ubuntu 22.04

## Installation and running the code.
<br/>

1. Clone the repository to your local machine:
```shell
git clone https://github.com/CS5060-Advanced-Computer-Networks.git
```
<br/>

2. On Ubuntu systems the iproute2 package (including netem) can be installed using following command:
   The purpose of this command is to emulate packet loss at the network interface card (NIC) level which we will see further.

```sh
sudo apt install iproute2
```
<br/>

3. Choose the directory of Socket Programming

```shell
cd Socket\ Programming/
```
<br/>

4. Start the UDP Server using your C++ compiler:

```shell
cd UDP
```
<br/>

  * UDP Server
```shell
g++ UDPPingerServer.cpp -o UDPPingerServer
./UDPPingerServer
```
<br/>

  * UDP Modified Server - for this, we need emulate packet loss at
the network interface card (NIC) level for which we have installed iproute2 in Step 2
```shell
g++ UDPPingerModifiedServer.cpp -o UDPPingerModifiedServer
./UDPPingerModifiedServer
```
<br/>

  * UDP Client - Ensure your server is running before starting the client.
```shell
g++ UDPPingerCleint.cpp -o UDPPingerClient
./UDPPingerClient
```
<br/>

5. Start the TCP Server using your C++ compiler:

```shell
cd TCP
```
<br/>

  * TCP Server
```shell
g++ TCPPingerServer.cpp -o TCPPingerServer
./TCPPingerServer
```
<br/>

*  TCP Modified Server - for this, we need emulate packet loss at
the network interface card (NIC) level for which we have installed iproute2 in Step 2
```shell
g++ TCPPingerModifiedServer.cpp -o TCPPingerModifiedServer
./TCPPingerModifiedServer
```
<br/>

*  TCP Concurrent Server - a server that waits on the welcoming socket and then creates a new thread or process to handle the incoming ping messages from different clients.
```shell
g++ TCPPingerConcurrentServer.cpp -o TCPPingerConcurrentServer -pthread
./TCPPingerConcurrentServer
```
<br/>

*  TCP Client - Ensure your server is running before starting the client.
```shell
g++ TCPPingerCleint.cpp -o TCPPingerClient
./TCPPingerClient
```

## License

Created under the MIT License. See [LICENSE](https://github.com/Kritik007//CS5060-Advanced-Computer-Networks/blob/main/LICENSE) for more information.

## Authors

* **[Kritik Agarwal](https://github.com/Kritik007/)** - *M.Tech CSE Student @ IIT Hyderabad*

## Acknowledgements

* [Dr. Bheemarjuna Reddy Tamma](https://people.iith.ac.in/tbr/)
* [Dept. of CSE, IIT Hyderabad](https://cse.iith.ac.in)
