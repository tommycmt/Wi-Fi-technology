# Wi-Fi Technology
--------------------------------
## Table of Content  
  1. [Learning Progress](#learning-progress)
  2. [WLAN Channel](#wlan-channel)
  3. [IEEE standard](#ieee-standard)
  4. [Signal Strength](#signal-strength)
  5. [Wi-Fi authentication](#wi-fi-authentication)
  6. [Major Wi-FI solution vendor](#major-wi-fi-solution-vendor)
  7. [Thin AP VS Fat AP](#thin-ap-vs-fat-ap)
  8. [DNS, DHCP, Gateway and Speed Test](#dns-dhcp-gateway-speed-test)
  
-------------------------------
## Learning Progress

### Day 0
  - [x] General study on all topic
  
### Day 1
  - [x] WLAN Channel
  - [x] IEEE standard
  - [x] Signal Strength
  
### Day 2
  - [x] Wi-Fi authentication
  - [x] Major Wi-FI solution vendor
  - [x] Thin AP VS Fat AP
  
### Day 3
  - [x] DNS / DHCP / Gateway / Speed Test
  - [x] PoE – Power Over Ethernet
  - [ ] WiFi interference

### Day 4
  - [ ] Basic Linux command (SSH / cd / pwd / chmod / vi / ifconfig … )
  
### Day 5
  - [ ] Basic Linux command (Continue)
  - [ ] Cron job
  - [ ] Shell Script

### Day 6
  - [ ] Shell Script (Continue)
  
--------------------------------
# Content

## WLAN Channel

### 2.4 GHz
  - 802.11b, 802.11g, 802.11n, 802.11ax
  - To prevent the overlapping between channels, in most of the countries, 3 channels will be used
  - channel 1, 6, 11
  ![2.4GHz channels](https://upload.wikimedia.org/wikipedia/commons/thumb/8/84/NonOverlappingChannels2.4GHzWLAN-en.svg/425px-NonOverlappingChannels2.4GHzWLAN-en.svg.png "2.4GHz channels")
  - Relative lower speed
  - Better penetration on different materials, longer distance and more stable
  - Many other technologies are using 2.4GHz also, e.g. bluebooth, Microwave oven, wireless microphones
  - Interference would be a problem

### 5 GHz
  - 802.11a, 802.11n, 802.11ac, 802.11ax
  - Much more channels and provide more choice on the bandwidth, 20, 40, 80, 160Mhz
  - The wider bandwidth, the faster data transmission rate
  ![5GHz channels](https://metis.fi/wordpress/wp-content/uploads/2018/01/5GHz.png "5GHz channels")
  - Providing a faster transmission rate
  - But relative shorter distance and weaker penetration on obstacle
  
------------------------------------
## IEEE standard

### 802.11a
  - 5 GHz, 20 MHz
  - 54 Mbit/s
  
### 802.11b
  - 2.4 GHz, 20 MHz
  - 1, 2, 5.5, 11 Mb/s
  
### 802.11g
  - 2.4 GHz, 20 MHz
  - 6, 9, 12, 18, 24, 36, 48, 54 Mbit/s
  - Compatible to 802.11b
  
### 802.11n
  - aka Wi-Fi 4
  - 2.4/5 GHz, 20/40 MHz
  - Support 4x4 MIMO
  - 20 MHz: up to 288.8 Mb/s
  - 40 MHz: up to 600 Mb/s
  - Compatible to 802.11a/b/g
  
### 802.11ac
  - aka Wi-Fi 5
  - Wave 1, Wave 2, IEEE
  - 5 GHz, 20/40/80 MHz, 3x3 MIMO
  - Wave 2: MU-MIMO, 80+80/160 MHz, 3-4 MIMO
  - 20 MHz: up to 346.8 Mb/s
  - 40 MHz: up to 800 Mb/s
  - 80 MHz: up to 1733.2 Mb/s
  - 160 MHz: up to 3466.8 Mb/s
  - IEEE: 8x8 MIMO
  - 160 Mhz: 6.9 Gb/s

### 802.11ax
  - aka Wi-FI 6
  - 2.4 and 5 GHz, incorporate 1 - 7 GHz
  - Next generation
  - 160 MHz: 1201 Mb/s (Single spatial stream)
  - Demo product up to 11 Gbit/s
  
------------------------------------
## Signal Strength
  - in terms of mW
  - RSSI (dBm)
  - Noise floor (dBm)
  - RSSI - Noise floor -> SNR (Signal to Noise Ratio)
  
### RSSI (Received Signal Strength Indicator)
  - Non-linear indication
  ![equation of mW to dBm](https://shopdelta.eu/obrazki_art/dbm_img2_d.jpg "mW_to_dBm")
  - The higher the RSSI, the stronger the signal received

### SNR (Signal to Noise Ratio)
  - The higher the SNR, the more signal than noise
  
------------------------------------
## Wi-Fi authentication

### WEP (Wired Equivalent Privacy)
  - PSK (Pre Shared key) for all clients
  - 40 bit -> 104-bit key (US gov restrictions)
  - Combined with a 24-bit initialization vector
  - Easy to crack
  
### WAP (Wi-Fi Protected Access)
  - Interim standard
  - Same alogrithm to WEP but using TKIP (Temporal Key Integrity Protocol)
  - 256 bits keys, per-packet key mixing, unique key for each packet
  - automatic broadcast of updated keys
  - message integrity check
  - Larger IV size (48 bits)
  - Personal mode, PSK
  - Enterprise mode, EAP (Extensible Authentication Protocol) with 802.1x
  - Enterprise mode required an authenticatioin server

### WAP2 (Wi-Fi Protected Access II)
  - AES (Advanced Encryption Standard) and Counter Mode with (Cipher Block Chaining Message Authentication Code Protocol)
  - Support TKIP as a fallback
  - Seamless roaming, allowing client to move between AP on same network without having reauthtication
  - Use of Pairwise Master Key caching or preauthentication
  - Personal mode, PSK
  - Enterprise mode, EAP with 802.1x

![Wi-Fi_auth_method](https://cdn.ttgtmedia.com/rms/onlineImages/wirelesssec_chart.PNG "Wi-Fi_auth_method")

### 802.1x
  - Authenticator and Authentication Server
  - Only allow client to connect the network after authenticate by Authenticator
------------------------------------
## Major Wi-FI solution vendor

### Aruba
  - AirWave for management
  - Better on managing multiple different security profiles across different location, Clearpass
  - Has decent switches which can use to control different AP
  - More focus on the security issue
  - Mor enterprise support capailities
  
### Ruckus 
  - Unleashed & Unleashed Multi-Site Manager (UMM)
  - Easy to configure and monitor
  - Cheaper than Aruba
  - Only focus on wireless 
  - Focus on the user interface, the ease to control their product
  - ZoneDirectors do not have integrated RADIUS servers
  
### Cisco
  - Complicated to configure than Ruckus
  - More to cover an area
  - Better migrate with the wired components

-----------------------------
## Thin AP vs Fat AP

### Thin AP
  - Transmission only
  - Controlled by switch, centralized control
  - Bottleneck on controller
  - Do not even perform WLAN encryption
  - Keeps APS simple and avoiding the necessity to upgrade their hard or software

### Fat AP
  - Each AP is an addressable node in the network with its own IP address on its interfaces
  - Can operate without any controller device
  - SNMP (Simple Network Management Protocol) or HTTP to manage APs
  - Complex and costly

------------------------------
## DNS, DHCP, Gateway, Speed Test

### DNS (Domain Name System)
  - Hierarchical decentralized nameing system
  - Translate between ip address and domain name
  - FQDN (Fully Qualified Domain Name)
  ![DNS resolver](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Example_of_an_iterative_DNS_resolver.svg/563px-Example_of_an_iterative_DNS_resolver.svg.png "DNS resolver")

### DHCP (Dynamic Host Configuration Protocol)
  - UDP/IP
  - 1. Client send a broadcast DHCPDISCOVER message
  - 2. DHCP Server send a broadcast DHCPOFFER message
  - 3. Client send a unicast DHCPREQUEST message to DHCP
  - 4. DHCP Server send a unicast DHCPACK message to Client

### Gateway
  - Connecting two deivce
  - Similar to proxy
  - May communicate with different protocol
  - IP Gateway in router -> transmitting data in different network
  
### Speed Test
  - Throught sending some packets and measure the response time and loss
  - Check the current network performance


  
