#### TCP THREE-WAY HANDSHAKE

1. Open the network capture file `/root/THA/network-protocols/assets/3wayhandshake.pcap` on your THA Kali VM using the Wireshark application.

2. Examine the first 3 packets in this capture which depicts the following TCP three-way handshake:

  ```
  10.0.2.15               -SYN->            74.125.47.105
  ```

  ```
  74.125.47.105           -SYN+ACK->        10.0.2.15
  ```

  ```
  10.0.2.15               -ACK->            74.125.47.105
  ```

3. Wireshark is a robust protocol analyzer and can display the actual TCP Flow Graph for this connection.  Select “Flow Graph” located under the “Statistics” Menu bar.  From within the pop up change the “flow type” (middle selection box) to select “TCP Flow” and press the “OK” button.  Note the Flow Graph rendered clearly shows the three-way handshake.

4. Feel free to explore this flow graph further on your own and close it when you’re finished.

5. You have completed this lab. You can continue to lab 2 by following the instructions found at 
    ```
    /root/THA/network-protocols/lab2.md
    ```
