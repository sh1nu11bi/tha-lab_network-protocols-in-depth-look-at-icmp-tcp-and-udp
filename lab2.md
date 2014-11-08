#### TCP SEQUENCE AND ACKNOWLEDGMENT NUMBERS
1. Open the network capture file `/root/THA/network-protocols/assets/3wayhandshake.pcap` on your THA Kali VM using the Wireshark application.
2. Select the first packet within the capture and expand out the “Transmission Control Protocol” decode section to expose the “Sequence Number” field.  Select this field in Wireshark and notice that Wireshark displays sequence and acknowledgment numbers in a “relative sequence” by default.  When the sequence number is highlighted the corresponding section within the raw packet data window is highlighted.  This can be seen in the following figure:
![screenshot](https://github.com/madsec/tha-lab_network-protocols-in-depth-look-at-icmp-tcp-and-udp/raw/master/images/wireshark.png)
3. To calculate the real sequence number we need to convert the HEX number 4985A4AF to decimal and we can do this by feeding this value into your favorite calculator or HEX to Decimal conversion application found on the Internet.  Perform this conversion which should result in the decimal value of 1233495215.  Remember that the security of a TCP connection depends upon these initial sequence numbers being random.
4. Now perform this same process for packets 2 and 3 within the capture and record the following values:

  ```
  Packet 1 Sequence numbers:
  ```

  ```
  Relative: 0                 HEX: 4985A4AF              Decimal: 1233495215
  ```

  ```
  Packet 2 Sequence numbers:
  ```

  ```
  Relative:                   HEX:                       Decimal:
  ```

  ```
  Packet 2 Acknowledgment numbers:
  ```

  ```
  Relative:                   HEX:                       Decimal:
  ```

  ```
  Packet 3 Sequence numbers:
  ```

  ```
  Relative:                   HEX:                       Decimal:
  ```

  ```
  Packet 3 Acknowledgment numbers:
  ```

  ```
  Relative:                   HEX:                       Decimal:
  ```

Notice that the sequence number increment as suspected and we can clearly see the relationship now between the client and server sequence and acknowledgment numbers.
5. Wireshark is extremely configurable and can be set to show the actual sequence and acknowledgement numbers so that you don’t have to perform this calculation manually.  To configure Wireshark to show these values select “Preferences” from the “Edit” menu bar.  Expand out “Protocols” located on the left hand side of the pop up dialog box and highlight the “TCP” menu item.  Uncheck the option “Relative sequence numbers and window scaling” and click “OK” to apply this setting.  Now go back and verify that your manual calculations were accurate.
6. Once you have finished exploring the sequence numbers don’t forget to reset the display “Relative sequence numbers” option, as it tends to be easier to read and analyze in general.
7. You have completed this lab. You can continue to lab 3 by following the instructions found at 
    ```
    /root/THA/network-protocols/lab3.md
    ```