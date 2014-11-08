#### EXPLORING ICMP TYPES AND CODES
1. Open the network capture file `/root/THA/network-protocols/assets/3wayhandshake.pcap` on your THA Kali VM using the Wireshark application.
2. Using the Wireshark Help menu and Wireshark Cheat sheets use wireshark to answer the following questions regarding this network capture:What is the ICMP Type for packet number 8? Was IP address 209.42.40.20 able to successfully ping 129.171.32.10?
3. IP address 129.171.199.1 appears to be experiencing some network connection issues.  Answer the following questions regarding these issues: What ICMP Type and Code was associated with these issues? What is the IP reporting the error message back to 129.171.199.1? What layer 4 protocol was 129.171.199.1 utilizing while experiencing these issues?  Hint: ICMP is layer 3, so that isn’t the answer! What IP was 129.171.199.1 trying to connect to? What Port number was 129.171.199.1 trying to connect to and what common network service is this port associated with?With all this information describe what you believe was occurring with 129.171.199.1 and whether this was an attack or a configuration issue?
4. You have completed this lab. You can continue to lab 5 by following the instructions found at 
    ```
    /root/THA/network-protocols/lab5.md
    ```
