# Charles Proxy is an HTTP proxy / HTTP monitor / Reverse Proxy to view all of the HTTP and SSL / HTTPS traffic

https://www.charlesproxy.com/

## About Charles

https://www.charlesproxy.com/overview/

Charles is a web proxy (HTTP Proxy / HTTP Monitor) that runs on your own computer. Your web browser (or any other Internet application) is then configured to access the Internet through Charles, and Charles is then able to record and display for you all of the data that is sent and received.

In Web and Internet development you are unable to see what is being sent and received between your web browser / client and the server. Without this visibility it is difficult and time-consuming to determine exactly where the fault is. Charles makes it easy to see what is happening, so you can quickly diagnose and fix problems.

Charles makes debugging quick, reliable and advanced; saving you time and frustration!

## Key Features
- `SSL Proxying` – view SSL requests and responses in plain text
- `Bandwidth Throttling` to simulate slower Internet connections including latency
- `AJAX debugging` – view XML and JSON requests and responses as a tree or as text
- `AMF` – view the contents of Flash Remoting / Flex Remoting messages as a tree
- `Repeat requests` to test back-end changes
- `Edit requests` to test different inputs
- `Breakpoints` to intercept and edit requests or responses
- `Validate recorded HTML`, CSS and RSS/atom responses using the W3C validator

https://www.charlesproxy.com/documentation/installation/apt-repository/

## APT repository
Charles has an APT repository for Debian-based Linux distributions.

NB: The keys for the repo changed on 26 July 2016, to utilise a larger key size and stronger digests. Existing users of the APT repository will need to import the new public key. The new public key is at the same URL as the old public key, therefore repeat the apt-key add step below to add it. Finally, run apt-get update to use the new key.

## GPG public key
First install the GPG public key for the repository so you can verify that the packages are correctly signed. The current public key id is 1AD28806 and its fingerprint is 4BA7 DB85 7B57 0089 7420  96E1 5F16 B97C 1AD2 8806:

```java
wget -q -O - https://www.charlesproxy.com/packages/apt/PublicKey | sudo apt-key add -
```

or alternatively:

```java
sudo apt-key adv --keyserver pgp.mit.edu --recv-keys 1AD28806
```

Then add the repository to your sources:

```java
sudo sh -c 'echo deb https://www.charlesproxy.com/packages/apt/ charles-proxy main > /etc/apt/sources.list.d/charles.list'
```

Then update your sources and install Charles:

```java
sudo apt-get update
sudo apt-get install charles-proxy
```

The package creates a "charles" command in `/usr/bin`, and adds Charles in your application menus in your window manager.

You may also install the beta track of Charles which is called charles-proxy-beta.

Output
```java
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following NEW packages will be installed:
  charles-proxy
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 49.1 MB of archives.
After this operation, 75.7 MB of additional disk space will be used.
Get:1 https://www.charlesproxy.com/packages/apt charles-proxy/main amd64 charles-proxy amd64 4.6.2 [49.1 MB]
Fetched 49.1 MB in 2s (29.1 MB/s)        
Selecting previously unselected package charles-proxy.
(Reading database ... 218834 files and directories currently installed.)
Preparing to unpack .../charles-proxy_4.6.2_amd64.deb ...
Unpacking charles-proxy (4.6.2) ...
Setting up charles-proxy (4.6.2) ...
update-alternatives: using /usr/bin/charles4 to provide /usr/bin/charles (charles) in auto mode
gtk-update-icon-cache: Cache file created successfully.
Processing triggers for mime-support (3.64ubuntu1) ...
Processing triggers for hicolor-icon-theme (0.17-2) ...
Processing triggers for gnome-menus (3.36.0-1ubuntu1) ...
Processing triggers for shared-mime-info (1.15-1) ...
Processing triggers for desktop-file-utils (0.24-1ubuntu3) ...
```

Run Charles

```java
charles
```

Output
```java
INFO     com.xk72.charles.CharlesContext                       Loading Configuration
INFO     com.xk72.charles.CharlesContext                       Version 4.6.2
INFO     com.xk72.charles.CharlesContext                       Loading Preferences
Charles is shareware. If you continue using Charles you must pay the shareware fee.
Charles will wait for 10 seconds before starting...
INFO     com.xk72.charles.CharlesContext                       Configuring Access Control List
INFO     com.xk72.charles.CharlesContext                       Starting Proxy Server
INFO     com.xk72.charles.CharlesContext                       Loading Tools
INFO     com.xk72.charles.CharlesContext                       Starting Tools
INFO     com.xk72.charles.CharlesContext                       Configuring Proxies
INFO     com.xk72.charles.CharlesContext                       Ready
```
