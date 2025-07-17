# Wireshark-Network-Traffic-Capture-and-Analysis---Kali-Linux


---

**1. Introduction**

This report provides a step-by-step guide on capturing and analyzing network traffic using Wireshark on Kali Linux. Wireshark is a widely-used network protocol analyzer that allows you to monitor and inspect packets in real time. This document covers installation, capture, filtering, and basic analysis techniques.

---

**2. Installation of Wireshark on Kali Linux**

Open a terminal and run the following commands:

```bash
sudo apt update
sudo apt install wireshark -y
```

During installation, select **Yes** if prompted to allow non-superusers to capture packets. Then, add your user to the `wireshark` group:

```bash
sudo usermod -aG wireshark $USER
```

Log out and log back in (or reboot) to apply the changes.

---

**3. Launching Wireshark**

Start Wireshark via terminal:

```bash
wireshark
```

Or search for "Wireshark" in the Applications menu. If needed, it can be run as root:

```bash
sudo wireshark
```

---

**4. Capturing Network Traffic**

* Choose the appropriate interface (e.g., `eth0` for Ethernet, `wlan0` for Wi-Fi).
* Click the interface to start capturing packets.

**Optional Capture Filters:**

* Capture HTTP traffic: `port 80`
* Capture traffic from a specific IP: `host 192.168.1.10`

---

**5. Stopping the Capture**

Click the red square **Stop** button in the toolbar to end the capture.

---

**6. Analyzing Captured Packets**

Common protocols to analyze:

* **HTTP** – Inspect requests and responses
* **DNS** – View name resolution
* **TCP/UDP** – Observe ports and data flow
* **ICMP** – Analyze ping packets

**Display Filters Examples:**

* `http` – Display only HTTP packets
* `dns` – Display only DNS packets
* `ip.addr == 192.168.1.10` – Filter by IP
* `tcp.stream eq 0` – Follow a specific TCP conversation

**Follow a TCP Stream:**

* Right-click on a TCP packet → **Follow** → **TCP Stream** to view complete communication

---

**7. Saving Captures**

Go to **File > Save As** to store the capture in `.pcap` format for later analysis.

---



---

**8. Conclusion**

Wireshark is a powerful tool for network traffic capture and analysis. Mastering its filters, stream tracking, and protocol analysis enables in-depth understanding of network behavior and threat detection.

---

**Appendix**

**Useful Display Filters:**

* `tcp` – TCP packets
* `udp` – UDP packets
* `icmp` – ICMP packets
* `tcp.port == 443` – HTTPS traffic
* `frame contains "login"` – Frames containing the string "login"

---


