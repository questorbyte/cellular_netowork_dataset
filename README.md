# ProBait Dataset

**ProBait Dataset** repository welcomes you! 🚀 This repository contains a part of our dataset. We include data for 3 UEs out of 10. We will open-source the full version of our dataset upon acceptance of the paper. This dataset might be useful for researchers working on **Cellular Networks, Machine Learning and Cybersecurity**.

📌 The dataset consists of behavior of **10 unique user equipment**.

--- 

## Collection Methodology
Our dataset is collected from 10 unique user equipment (UEs). We captured data as PCAP files and then converted them to CSV files to strip off all Personally Identifiable Information. We have further processed the CSV files to anonymize the source and destination IP addresses. The data collected considers handover scenarios, i.e., when UEs were mobile (bus, car, subway).

A collection of CSV files (2 per UE) containing relative time at which packets were sent (starting from 0, no real timestamp), anonymized source and destination IP address, Protocol, size of the packet sent and Information (related to protocol if it is a control packet otherwise “protected packet”)

**Tools used** <br>
🔹 rvictl, a command-line utility officially supported by apple and accessible to all Apple Developers ([rvictl](https://developer.apple.com/documentation/network/recording-a-packet-trace)) to capture network traffic from Apple UEs <br>
🔹 PCAPdroid, an official app with 100k+ downloads with 3.9 rating ([PCAPDroid](https://play.google.com/store/apps/details?id=com.emanuelef.remote_capture&hl=en_CA)) to capture network traffic from Android UEs <br>
🔹 Wireshark to analyze the packet capture <br>

---

## 🔔 Features of our Dataset
To the best of our knowledge, no dataset exists that provides real world UE data. The existing datasets either do not include mobility scenarios, are generated using automated tools (therefore they cannot mirror real-world temporal patterns, packet sizes, network failures etc.), collected from a single network operator or are based on fewer UEs.

**Our dataset is diverse as it includes:** <br>
🔹 Multiple real devices (no simulators) <br>
🔹 Includes mobility scenarios (Car, Bus and Subway) <br>
🔹 Devices are connected to 4G and 5G networks provided by 5 different Telecom operators <br>
🔹 Is generated manually by people (not bots or tools) and is gathered from devices where users perform several activities (e.g., browsing, streaming, scrolling through social media) <br>
 
**Potential use case of this dataset:**  <br>
🔹 Get access to real world patterns of cellular traffic (temporal pattern, packet sizes, protocols) <br>
🔹 Use this data to generate artificial network traffic for attacks/defense <br>
🔹 Can use data plane traffic to predict control plane events. Control Plane traffic is very difficult to get. Therefore, people who need control plane traffic can use our dataset to correlate certain events in the user plane traffic to control plane and use it. <br>

## 📂 Repository Structure
<pre>
<code>
📊 ProBait_Dataset
├── 📁 Mobility                     # Contains Idle and Mixed Activity usage when the UE was mobile
│   ├── 📁 Bus
│   │   ├── 📁 Idle
│   │   │   └── 📄 UE_a_bg.csv
│   │   └── 📁 Mixed Usage
│   │       └── 📄 UE_a.csv
│   ├── 📁 Car
│   │   ├── 📁 Idle
│   │   │   └── 📄 UE_b_bg.csv
│   │   └── 📁 Mixed Usage
│   │       └── 📄 UE_b.csv
│   └── 📁 Subway
│       ├── 📁 Idle
│       │   └── 📄 UE_c_bg.csv
│       └── 📁 Mixed Usage
│           └── 📄 UE_c.csv
├── 📁 Stationary                   # Contains Idle and Mixed Activity usage in when the UE was not mobile
│   ├── 📁 Idle
│   │   └── 📄 UE_d_bg.csv
│   └── 📁 Mixed Usage
│       └── 📄 UE_d.csv
├── 📄 LICENSE.txt
└── 📄 README.md
</code>
</pre>

--- 

## 🛡️ Ethics  
All the participants were fully informed of the purpose behind collecting the data, the nature of the data collected and procedure by which the data would be collected. They willingly consented to share their usage data with us. As per the [Criminal Code of Canada – Section 184](https://laws-lois.justice.gc.ca/eng/acts/c-46/section-184.html) it is legal to collect user plane data from one's own smartphone. we do not send any unauthorized signals to commercial networks. We send only user plane data. Also, we do not mess with the stability or abuse the network in any way (we do not perform dynamic testing). Our usage is that of a normal everyday user (activities, data consumed, duration). We do not tax the network.

--- 

## License
This project is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).
