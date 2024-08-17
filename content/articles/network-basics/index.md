---
title: "Networking Basics for the Common Folk"
description: "This description will be used for the article listing and search results on Google."
date: "2021-05-28"
# banner:
#   src: "../../images/kelly-sikkema-Hl3LUdyKRic-unsplash.jpg"
#   alt: "First Markdown Post"
#   caption: 'Photo by <u><a href="https://unsplash.com/photos/Nc5Q_CEcY44">Florian Olivo</a></u>'
categories:
    - "Tech"
    - "Networking"
keywords:
    - "Tech"
    - "Networking"
    - "Markdown"
    - "Blog"
---
Networking doesn't have to be as confusing as some people might think! Here's a quick guide on the core concepts you need to know. Whether you want to configure a good home network or you're curious about how the whole internet works, follow along and you'll learn a ton!


## So... What is a network?
Let's start from the basics. 

If you just go to [Wikipedia](https://en.wikipedia.org/wiki/Computer_network) you'll find the following nonsense:

>A **computer network** is a set of [computers](https://en.wikipedia.org/wiki/Computer "Computer") sharing resources located on or provided by [network nodes](https://en.wikipedia.org/wiki/Node_(networking) "Node (networking)"). Computers use common [communication protocols](https://en.wikipedia.org/wiki/Communication_protocol "Communication protocol") over [digital](https://en.wikipedia.org/wiki/Digital_signal "Digital signal") [interconnections](https://en.wikipedia.org/wiki/Interconnection "Interconnection") to communicate with each other. These interconnections are made up of [telecommunication network](https://en.wikipedia.org/wiki/Telecommunication_network "Telecommunication network") technologies based on physically wired, [optical](https://en.wikipedia.org/wiki/Optical_fiber "Optical fiber"), and wireless [radio-frequency](https://en.wikipedia.org/wiki/Radio_frequency "Radio frequency") methods that may be arranged in a variety of [network topologies](https://en.wikipedia.org/wiki/Network_topology "Network topology").

If you're anything like me when I started learning about networks, that wall of text means a whole bunch of nothing, so let's use a better way to explain what a network is.

Devices are social creatures, they like to talk to each other. At its most basic level, the whole internet is just a bunch of computers talking! The device you're reading this with is currently talking to the computer I set up to serve you this website. That being said, the International Telecommunications Union estimates that [5.4 billion people are using the internet](https://www.itu.int/en/ITU-D/Statistics/Pages/stat/default.aspx), and well, *that's a boatload of devices!* How do you even begin to make all of those devices communicate efficiently and securely? Let alone, websites? What even are those? 

To make managing those billions of devices more simple, they are grouped up in networks. Let's start out with the most common type of home network:

![[basic_home_network.png]]

This is the most common type of setup for home networks. In this network, the PC 1, PC 2, Laptop and Smart Phone can all talk to each other through the switch, and then, all of them can talk to the internet through the router. 

In short, **a network is a group of computers that can all talk to each other.**

There are two main types of networks that you need to understand:
### Local Area Network (LAN)
A Local Area Network refers to a network where all of the devices are part of the same network. Connecting devices in your home router makes them all part of the same LAN, so your laptop and your phone can talk back and forth over the network. Remember LAN Parties? they work by connecting all of the devices people played with in the same network, and then configuring the games so that they could play together, in other words, their devices could talk to each other because they were part of the same LAN (hence, LAN party).
### Wide Area Network (WAN)
A wide Area Network refers to a large group of smaller networks connected to each other in different ways that allow for devices in any given network to talk to devices in other networks. WAN can span large geographical zones, and connect together hundreds or thousands of networks in many different ways


*"... But Gabe! I don't have a switch or a Wireless Access Point! I only have a weird box where everything is connected!"*, you might say, but the answer for that is really simple. Most Internet Service Providers give you an All in One box with a modem, a router, a switch and a Wireless Access Point all combined together into a grotesque amalgamation of technology. *"But wait... what are all of those?"*, I'm glad you asked! Let's now look at the different network devices and what they do! 

## Network devices
There's a vast array of devices created to create, manage and secure networks. These devices are called network devices — very creative, i know —. The way to configure them might differ between manufacturers, but their functionality remains consistent across the board. Here's a list of the most important network devices you might find on a network:
### 1. Routers
Routers can be considered the separation between networks, as they communicate two networks with each other. When messages need to move between networks, they go from router to router until they find their destination. 

Let's say you want to visit www.google.com from your laptop. The moment you hit `enter` to go to the page, your device sends a message to your router that for now can be boiled to:
```
from:  the_super_laptop
to: www.google.com
message: can i has website?
```

Your router sees this message coming from a device the LAN and sends it out to the WAN, until it reaches Google's servers (as they are the recipient). Google looks at that message and decides to reply with what you requested, something like this:
```
from: www.google.com
to: the_super_laptop
message: Sure! Here you go!
		 (then a bunch of HTML to render Google's website)
```

Google sends that message back to the WAN until it reaches your router. Finally, your router forwards it to your laptop so that it can render Google's website.

### 2. Switches
Switches allow you to connect many devices inside of a network. They usually have many ports for an Ethernet connection, and allow devices to talk to each other through those ports. Switches keep track of each device's address, and know how to transfer messages from one device to another, and vice versa. 

### 3. Modem
This is an easy one, as its only job is to receive the connection from your Internet Service Provider (ISP), the company you pay for your internet connection. This might be through a fiber-optic, Ethernet, or a coaxial cable. ISPs generally give out those modem/router/switch devices, that receive the initial connection from the ISP (the modem part), then connects the network from the ISP (WAN) to your home network (LAN) (the router part), and offers several Ethernet ports to connect devices into (the switch part). They are also able to create a wireless network to connect your devices through WiFi (just like a Wireless Access Point)

### 4. Wireless Access Point
A device that sends out WiFi signal to connect your devices with. That's it! 

## IP Addresses

### Private IP Addresses

Private IP addresses are the unique identifiers assigned to devices within a local network. Think of them as house numbers in a neighborhood. Each device in your home has its own private IP address, allowing them to communicate with each other and the internet. These addresses are not visible to the outside world and are assigned by your router. Common private IP address ranges include:

- 192.168.0.0 to 192.168.255.255
- 172.16.0.0 to 172.31.255.255
- 10.0.0.0 to 10.255.255.255

So, when your phone talks to your laptop, it uses these private IP addresses.

### Public IP Addresses

Public IP addresses, on the other hand, are like the street addresses of buildings. They are unique across the entire internet and are assigned by your Internet Service Provider (ISP). These addresses allow your home network to communicate with other networks. When you access a website, your router uses its public IP address to request data from the internet. The website sees this public IP and sends the data back to it.

In summary, private IP addresses let devices within your home network talk to each other, while public IP addresses let your entire network communicate with the rest of the world.

## Data Packets

Imagine you want to send a long letter to a friend, but instead of sending it as one huge piece of paper, you break it down into smaller, manageable postcards. Each postcard contains a piece of the letter and instructions on how to put the entire letter back together. This is essentially how data packets work on the internet.

When you send data over the internet, it is broken down into smaller chunks called packets. Each packet contains:

- A header with information like the source and destination IP addresses, sequence number, and other control information.
- The actual data being sent.

These packets travel independently across the network, possibly taking different paths to reach their destination. Once they arrive, they are reassembled in the correct order to form the original data.

## How the Internet Works

### Servers

Servers are like the super libraries of the internet. They store and manage data and provide services to other computers, called clients. When you request a website, your device acts as a client, asking the server to send the website's data. Servers handle everything from hosting websites to managing emails and databases.

### DNS

The Domain Name System (DNS) is the internet's phonebook. It translates human-readable domain names (like [www.google.com](http://www.google.com)) into IP addresses that computers use to identify each other. When you type a website address into your browser, a DNS server translates it into an IP address so your device can find and communicate with the appropriate server.

### Packet Flow Around the Internet

When you hit enter on a website URL, here's a simplified journey of how the data flows:

1. Your device sends a DNS request to find the IP address of the website.
2. The DNS server responds with the IP address.
3. Your device sends an HTTP request to the server's IP address asking for the website's data.
4. The server responds by breaking the website data into packets and sending them back to your device.
5. The packets travel across the internet, passing through various routers and switches.
6. Your device receives the packets, reassembles them, and displays the website.
