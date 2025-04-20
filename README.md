# ProBait_Dataset

**ProBait_Dataset** repository welcomes you! 🚀 We have endeavoured to opensource the dataset that was designed for **ProBait** This dataset can be an asset for researchers working on **Cellular Networks, Machine Learning and Cybersecurity**

📌 The dataset consists of behaviour of **10 unique Apple and Samsung User Equipment hooked to 5 different 4G and 5G networks.**

# Collection Methodology
Our dataset was collected from students in our lab. We captured data as a PCAP file and then converted them to CSV file to strip off all Personally Identifiable Information. We have further anonymized the CSV files to anonymize the source and destination IP addresses. The data was collected taken into account handover scenarios, i.e., when UEs were mobile (bus, car, subway).

A collection of CSV files (2 per UE) containing relative time at which packets were sent (starting from 0, no real timestamp), anonymized source and destination IP address, Protocol, Length of the packet sent and Information (related to protocol if it’s a control packet otherwise “protected packet”)

**Tools used**
🔹 rvictl, a command-line utility officially supported by apple and accessible to all Apple Developers ([rvictl](https://developer.apple.com/documentation/network/recording-a-packet-trace)) to capture network traffic from Apple UEs <br>
🔹 PCAPdroid, an official app with 100k+ downloads with 3.9 rating ([PCAPDroid](https://play.google.com/store/apps/details?id=com.emanuelef.remote_capture&hl=en_CA)) to capture network traffic from Android UEs <br>
🔹 WireShark to analyse the packet capture <br>

---

## 🔔 Unique features of our Dataset?
To the best of our knowledge, no dataset exists that provides real world UE data. The existing datasets either do not include mobility scenarios, are generated using automated tools (therefore they cannot mirror real-world temporal patterns, packet sizes, network failures etc), collected from a single network operator or are based on fewer UEs.

Our dataset is diverse as it includes
🔹 Multiple real devices (no simulators) <br>
🔹 Includes mobility scenarios <br>
🔹 Is generated manually by people (not bots or tools)  <br>
🔹 Gathered from 5 operators <br>
🔹 Gathered from 4G and 5G <br>
🔹 Learn real-world de-registration timers <br>
 

**Potential use case of this dataset:** 
🔹 Get access to real world patterns of cellular traffic (temporal pattern, packet sizes, protocols) <br>
🔹 Use this data to generate artificial network traffic for attacks/defence <br>
🔹 Can use data plane traffic to predict control plane events. Control Plane traffic is very difficult to get. Therefore, people who need control plane traffic can use our dataset to correlate certain events in the user plane traffic to control plane and use it. <br>

## 📂 Repository Structure

```plaintext
/ProBait_Dataset
  ├── Idle/                     # Contains the CSV file with idle usage
  └── Mixed_Uage/               # Contains the CSV file with mixed usage
README.md
```

--- 

## 🛡️ Ethics Statement  
All the participants were fully informed of the purpose behind collecting the data, the nature of the data collected and procedure by which the data would be collected. They willingly consented to share their usage data with us. As per the [Criminal Code of Canada – Section 184](https://laws-lois.justice.gc.ca/eng/acts/c-46/section-184.html) it is legal to collect user plane data from one's own smartphone. we do not send any unauthorized signals to commercial networks. We send only user plane data. Also, we do not mess with the stability or abuse the network in any way (we do not perform dynamic testing). Our usage is that of a normal everyday user (activities, data consumed, duration). We do not tax the network.

