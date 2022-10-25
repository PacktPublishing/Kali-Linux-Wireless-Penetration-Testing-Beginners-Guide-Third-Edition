# Kali Linux Wireless Penetration Testing Beginner’s Guide - Third Edition
This is the code repository for [Kali Linux Wireless Penetration Testing Beginner’s Guide - Third Edition](https://www.packtpub.com/networking-and-servers/kali-linux-wireless-penetration-testing-beginner’s-guide-third-edition?utm_source=github&utm_medium=repository&utm_campaign=9781788831925), published by [Packt](https://www.packtpub.com/?utm_source=github). It contains all the supporting project files necessary to work through the book from start to finish.
## About the Book
As wireless networks become ubiquitous in our lives, wireless penetration testing has become a key skill in the repertoire of the professional penetration tester. This has been highlighted again recently with the discovery of the KRACK attack enabling attackers to break into wi-fi networks encrypted with WPA2. The Kali Linux security distribution comes with a myriad of tools used for networking attacks and detecting security loopholes.

Kali Linux Wireless Penetration Testing Beginner's Guide, Third Edition has been updated with the latest methodologies, including full coverage of the KRACK attack and how to defend against it. The book presents wireless pentesting from the ground up, introducing all elements of penetration testing with each new technology. You'll learn various wireless testing methodologies by example, from the basics of wireless routing and encryption through to detailed coverage of hacking methods and attacks such as the Hirte and Caffe Latte.
## Instructions and Navigation
All of the code is organized into folders. Each folder starts with a number followed by the application name. For example, Chapter02.



The code will look like the following:
```
import subprocess
import datetime
results = open("results.txt", "a")
while 1:
    cmd = subprocess.check_output(["tshark –n –i wlan0mon –T fields -e wlan.sa –e wlan.ssid –c 100"], shell=True)
    split = cmd.split("\n")
    for value in split[:-1]:
           if value.strip():
                   splitvalue = value.split("\t")
                   MAC = str(splitvalue[0])
                   SSID = str(splitvalue[1])
                   time = str(datetime.datetime.now())
                   results.write(MAC+" "+SSID+" "+time+"\r\n")

```

To follow and recreate the practical exercises in this book, you will need two laptops with built in Wi-Fi cards, a USB wireless Wi-Fi adapter, Kali Linux, and some other hardware and software. We have detailed this in Chapter 1, Wireless Lab Setup.
As an alternative to the two laptop setup, you can also create a virtual machine housing Kali Linux and connect the card to it using the USB interface. This will help you get started with using this book much faster, but we would recommend that you use a dedicated machine running Kali Linux for actual assessments in the field.
From a prerequisite perspective, you should be aware of the basics of wireless networks. This includes having prior knowledge about the basics of the 802.11 protocol and client-access point communication. Though we will briefly touch upon some of this when we set up the lab, it is expected that you are already aware of these concepts.


## Related Products
* [Kali Linux Wireless Penetration Testing Cookbook](https://www.packtpub.com/networking-and-servers/kali-linux-wireless-penetration-testing-cookbook?utm_source=github&utm_medium=repository&utm_campaign=9781783554089)

* [Mastering Kali Linux Network Scanning](https://www.packtpub.com/networking-and-servers/mastering-kali-linux-network-scanning?utm_source=github&utm_medium=repository&utm_campaign=9781788473323)

* [Kali Linux 2017 Wireless Penetration Testing for Beginners [Video]](https://www.packtpub.com/networking-and-servers/kali-linux-2017-wireless-penetration-testing-beginners-video?utm_source=github&utm_medium=repository&utm_campaign=9781788394055)

### Download a free PDF

 <i>If you have already purchased a print or Kindle version of this book, you can get a DRM-free PDF version at no cost.<br>Simply click on the link to claim your free PDF.</i>
<p align="center"> <a href="https://packt.link/free-ebook/9781783280414">https://packt.link/free-ebook/9781783280414 </a> </p>