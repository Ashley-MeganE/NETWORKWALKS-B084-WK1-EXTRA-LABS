<h1 align="center"> Wireshark Extra Labs </h1>

### Objectives
To complete all 10 questions of the given labs and practice my Wireshark skills. The objective for each lab are as follows:
|Lab Name | Goal |  
| :--- | :--- |
| 1. [Identify the Attacker’s IP](https://networkwalks.com/wireshark-lab3/) | Find the IP address of an attacker and identify the attack method being used. |
|2. [Follow TCP Stream](https://networkwalks.com/wireshark-lab4/) |Follow the TCP stream and rebuild a conversation taking place on the network. |
|3. [Follow TCP Stream, Part II](https://networkwalks.com/wireshark-lab5/) | Look through the TCP stream and discover the 'hidden' file. |
|4. [HTTP Plain Text Credentials](https://networkwalks.com/wireshark-lab6/) | Find usernames and passwords sent in clear text over HTTP. |
| 5. [Catch the Brute Force Attacker](https://networkwalks.com/wireshark-lab7/) | Investigate the repeated login attempts and find the attacker. |
|6. [Catch the Call Scammer](https://networkwalks.com/wireshark-lab8/) | Investigate the packets and listen to the captured call to find the scammer. |

### Tools Used
* Wireshark

### Lessons Learned
* A server answers with [SYN,ACK] only when a port is open. An attacker uses this to scan for open ports. Closing unnecessary ports and securing open ones limits attackers.

* Unencrypted secrets in a webpage can easily be accessed by attackers in a man-in-the-middle attack, even if the browser hides it. Messages should always be encrypted to prevent eavesdropping

* RTP, Real Time Transport Protocol, is used to carry real time voice data over the network. Through Telephony, one can listen to an unencrypted call. Calls must be encrypted to prevent this. 

### Skills Used
* Network Forensics & Packet Analysis: Reconstructing fragmented packet data to uncover the exact timeline of a breach.

* Deep Packet Inspection (DPI): Looking past basic packet headers into the payload to inspect cleartext strings and raw data.

* Cryptographic & Protocol Assessment: Identifying insecure data in transit (unencrypted HTTP) and recognizing where encryption (HTTPS/TLS) should have been enforced.

* Telephony & VoIP Analysis: Navigating voice-specific protocols (SIP and RTP) to track down scam activities.

* Wireshark Display Filtering: Using and crafting advanced filters (e.g. http.request.method == "POST", tcp.flags.syn == 1, or VoIP-specific streams) to quickly isolate indicators of compromise.

* Anomalous Pattern Recognition: Spotting brute-force signatures by recognizing high-frequency, repetitive traffic patterns targeted at authentication endpoints.
 
* Session Reconstruction: Assembling isolated packets into complete TCP/UDP streams to read the raw text of attacker-to-host communications.
  
* Threat Actor Identification: Correlating network behavior to isolate malicious IP addresses, source ports, and specific attack tools

## Author Information
Ashley-Megan Ikhialose Ehiede
