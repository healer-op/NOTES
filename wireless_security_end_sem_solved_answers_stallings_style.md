# Wireless Security – End Semester Examination (Solved)
### Based on concepts from William Stallings (Cryptography & Network Security / Wireless Security Topics)
**Course Code:** CPISE03  
**Max Marks:** 40  
**Semester:** II/IV  

---

# Q1. Attempt any 2 parts

---

# Q1(a) Explain the role of access points in securing infrastructure-based wireless networks.

## Introduction
An Access Point (AP) is the central communication device in an infrastructure-based wireless LAN. It connects wireless clients to the wired network and enforces security policies.

According to William Stallings, APs act as the “security gateway” between wireless users and organizational resources.

---

# Roles of Access Points in Security

| Role | Explanation |
|---|---|
| Authentication | Verifies identity of users/devices before access |
| Encryption Enforcement | Applies WPA2/WPA3 encryption |
| Access Control | Restricts unauthorized users |
| Traffic Monitoring | Detects suspicious traffic patterns |
| Network Segmentation | Separates guest and internal traffic using VLANs |
| Intrusion Prevention | Detects rogue APs and attacks |
| Centralized Policy Management | Applies organization-wide security rules |

---

# Working of Secure AP

1. Wireless client sends connection request.
2. AP authenticates client using password/certificate.
3. Encryption keys are exchanged.
4. AP forwards packets securely.
5. Suspicious traffic is monitored continuously.

---

# Security Features Provided by APs

## 1. Authentication
- Uses:
  - WPA2-PSK
  - WPA3-SAE
  - 802.1X authentication
  - RADIUS server

### Example
In a university Wi‑Fi network, students must enter credentials before Internet access.

---

## 2. Encryption
AP encrypts wireless frames.

| Standard | Encryption |
|---|---|
| WEP | RC4 |
| WPA2 | AES-CCMP |
| WPA3 | SAE + AES |

---

## 3. MAC Filtering
Only approved device MAC addresses can connect.

### Limitation
MAC addresses can be spoofed.

---

## 4. Rogue AP Detection
AP monitors nearby unauthorized access points.

### Example
A hacker installs fake Wi‑Fi inside an office.
Enterprise AP detects and blocks it.

---

## 5. VLAN Segmentation
Separates:
- Guest network
- Employee network
- IoT devices

This minimizes lateral attacks.

---

# Advantages of Access Points

| Advantage | Description |
|---|---|
| Centralized security | Easy policy management |
| Scalability | Supports many users |
| Better monitoring | Easier intrusion detection |
| Secure roaming | Seamless secure mobility |
| Supports enterprise authentication | Uses RADIUS/802.1X |

---

# Disadvantages / Limitations

| Limitation | Explanation |
|---|---|
| Single point of failure | If AP fails, communication stops |
| Rogue AP risk | Fake APs may impersonate legitimate APs |
| Signal leakage | Attackers outside building may intercept signals |
| Congestion | Many users reduce performance |

---

# Mnemonic
## “AETRM”
**A**uthentication  
**E**ncryption  
**T**raffic monitoring  
**R**ogue detection  
**M**anagement

---

# Conclusion
Access points play a major role in wireless security by enforcing authentication, encryption, monitoring, and access control. Modern APs using WPA3 and enterprise security mechanisms provide strong protection against wireless threats.

---
---

# Q1(b) Explain how wireless encryption standards (WEP, WPA2, WPA3) differ in terms of security features.

# Introduction
Wireless encryption standards protect confidentiality and integrity of wireless communication.

WEP was the first standard, followed by WPA/WPA2, and finally WPA3.

---

# Comparison Table

| Feature | WEP | WPA2 | WPA3 |
|---|---|---|---|
| Full Form | Wired Equivalent Privacy | Wi‑Fi Protected Access 2 | Wi‑Fi Protected Access 3 |
| Encryption | RC4 | AES-CCMP | AES + SAE |
| Security Level | Weak | Strong | Very Strong |
| Authentication | Shared Key | PSK / 802.1X | SAE |
| Key Size | 40/104-bit | 128-bit | 192-bit enterprise |
| Protection from Brute Force | No | Limited | Yes |
| Forward Secrecy | No | No | Yes |
| Vulnerable to Packet Replay | Yes | Less | Highly resistant |

---

# 1. WEP (Wired Equivalent Privacy)

## Features
- Uses RC4 stream cipher
- Static shared key
- 24-bit Initialization Vector (IV)

## Problems
- Weak IV reuse
- Easy key cracking
- Vulnerable to replay attacks

### Example
Attackers can crack WEP using Aircrack-ng within minutes.

## Advantages
- Simple
- Low hardware requirement

## Disadvantages
- Extremely insecure
- Deprecated

---

# 2. WPA2

## Features
- Uses AES-CCMP encryption
- Stronger integrity checking
- Supports Enterprise authentication

## Modes
| Mode | Use |
|---|---|
| Personal (PSK) | Home networks |
| Enterprise (802.1X) | Organizations |

## Advantages
- Strong encryption
- Widely supported
- Better authentication

## Limitations
- Vulnerable to weak passwords
- KRACK attack vulnerability

---

# 3. WPA3

## Features
- Uses SAE (Simultaneous Authentication of Equals)
- Forward secrecy
- Strong protection against offline attacks
- Mandatory Protected Management Frames (PMF)

## Advantages
- Highest security
- Resists dictionary attacks
- Better IoT security

## Limitations
- Requires newer hardware
- Compatibility issues with old devices

---

# Real World Example

| Environment | Standard Used |
|---|---|
| Old café router | WEP |
| Home Wi‑Fi | WPA2 |
| Modern enterprise | WPA3 |

---

# Mnemonic
## “RAW”
**R**C4 → WEP  
**A**ES → WPA2  
**W**PA3 with SAE

---

# Conclusion
WEP is obsolete due to weak security. WPA2 introduced strong AES encryption, while WPA3 provides advanced authentication and protection against modern attacks.

---
---

# Q1(c) Describe the concept of jamming attacks and possible defense mechanisms in wireless networks.

# Introduction
A jamming attack is a Denial-of-Service (DoS) attack where attackers intentionally transmit radio signals to disrupt wireless communication.

---

# Types of Jamming Attacks

| Type | Description |
|---|---|
| Constant Jamming | Continuous noise transmission |
| Deceptive Jamming | Sends fake packets |
| Random Jamming | Alternates between sleep and attack |
| Reactive Jamming | Jams only when communication detected |

---

# Working of Jamming

1. Attacker transmits high-power signals.
2. Legitimate signals become corrupted.
3. Receiver cannot decode packets.
4. Communication fails.

---

# Effects of Jamming

| Effect | Description |
|---|---|
| Packet Loss | Data corruption |
| High Delay | Retransmissions increase |
| Energy Waste | Devices consume more battery |
| Service Unavailability | Communication stops |

---

# Defense Mechanisms

## 1. Frequency Hopping Spread Spectrum (FHSS)
Sender changes frequencies rapidly.

### Advantage
Hard for attacker to jam all channels.

---

## 2. Direct Sequence Spread Spectrum (DSSS)
Signal spread over wider frequency band.

---

## 3. Channel Switching
Devices move to cleaner channel.

---

## 4. Signal Detection Algorithms
Monitor unusual interference patterns.

---

## 5. Directional Antennas
Focus signals in specific directions.

---

## 6. Power Control
Increase transmission power temporarily.

---

# Real World Example
Military wireless networks use FHSS to prevent enemy jamming.

---

# Advantages of Defense Mechanisms

| Method | Advantage |
|---|---|
| FHSS | Strong anti-jamming |
| DSSS | Better noise resistance |
| Channel switching | Fast recovery |
| Directional antennas | Reduced interference |

---

# Limitations

| Limitation | Description |
|---|---|
| High cost | Advanced hardware required |
| Complexity | Difficult implementation |
| Partial protection | Strong jammers still effective |

---

# Mnemonic
## “FCDSP”
**F**HSS  
**C**hannel switching  
**D**SSS  
**S**ignal detection  
**P**ower control

---

# Conclusion
Jamming attacks severely affect wireless availability. Techniques like FHSS, DSSS, and channel switching improve resilience and maintain reliable communication.

---
---

# Q2(a) Explain the impact of mobility on the effectiveness of security protocols in MANETs. Provide a practical example.

# Introduction
MANET (Mobile Ad Hoc Network) consists of mobile nodes communicating without fixed infrastructure.

Mobility creates dynamic topology changes, affecting security protocols.

---

# Impact of Mobility

| Impact | Explanation |
|---|---|
| Frequent Route Changes | Routes become unstable |
| Authentication Difficulty | Nodes continuously join/leave |
| Key Management Issues | Keys need frequent updates |
| Increased Packet Loss | Mobility breaks routes |
| Trust Instability | Hard to maintain trust values |

---

# Security Challenges Due to Mobility

## 1. Dynamic Topology
Links break frequently.

### Result
Security associations expire quickly.

---

## 2. Handoff Delays
Node movement causes reconnection delay.

---

## 3. Increased Attack Surface
Mobile attackers can change locations rapidly.

---

## 4. Resource Constraints
Battery and bandwidth limitations affect cryptography.

---

# Practical Example
## Disaster Recovery MANET
Rescue teams use MANET after earthquake.

### Problem
As rescuers move:
- routes change continuously
- authentication delays occur
- packet drops increase

### Security Impact
Intrusion detection becomes difficult.

---

# Advantages of Mobility

| Advantage | Description |
|---|---|
| Flexible deployment | No infrastructure needed |
| Fast communication setup | Useful in emergencies |
| Self-organizing | Nodes configure automatically |

---

# Disadvantages

| Disadvantage | Description |
|---|---|
| Unstable routes | Frequent disconnections |
| Security overhead | Frequent re-authentication |
| Hard trust management | Dynamic nodes |

---

# Mnemonic
## “RATS”
**R**oute changes  
**A**uthentication difficulty  
**T**rust instability  
**S**ecurity overhead

---

# Conclusion
Mobility significantly affects MANET security by causing unstable routes, authentication challenges, and increased vulnerability to attacks.

---
---

# Q2(b) Describe how route maintenance in ad hoc networks can be exploited by attackers and suggest mitigation techniques.

# Introduction
Route maintenance ensures valid paths remain available in ad hoc networks.

Attackers exploit routing updates to disrupt communication.

---

# Attacks During Route Maintenance

| Attack | Description |
|---|---|
| Black Hole Attack | Malicious node drops packets |
| Wormhole Attack | Two attackers tunnel packets |
| Route Error Manipulation | Fake route failures generated |
| Replay Attack | Old routing messages resent |
| Byzantine Attack | Creates routing loops |

---

# Example
Attacker sends fake Route Error (RERR) packets.

Result:
- nodes delete valid routes
- communication disrupted

---

# Mitigation Techniques

## 1. Authentication of Routing Messages
Use digital signatures/MACs.

---

## 2. Secure Routing Protocols
Examples:
- SAODV
- ARAN

---

## 3. Intrusion Detection Systems (IDS)
Detect abnormal routing behavior.

---

## 4. Multipath Routing
Use alternate routes.

---

## 5. Trust-Based Routing
Avoid low-trust nodes.

---

# Advantages of Mitigation

| Technique | Benefit |
|---|---|
| Secure routing | Prevents spoofing |
| IDS | Detects attacks quickly |
| Multipath routing | Improves reliability |

---

# Limitations

| Limitation | Explanation |
|---|---|
| Computational overhead | Cryptography consumes resources |
| Energy consumption | IDS increases battery usage |
| Scalability issues | Difficult in large MANETs |

---

# Mnemonic
## “SMART”
**S**ecure routing  
**M**ultipath routing  
**A**uthentication  
**R**eputation/trust  
**T**raffic monitoring

---

# Conclusion
Attackers exploit route maintenance using fake routing information. Secure routing protocols, IDS, and trust-based mechanisms help protect ad hoc networks.

---
---

# Q2(c) Discuss how cluster-based security approaches work in PANs with a real-world use case.

# Introduction
PAN (Personal Area Network) connects nearby personal devices such as smartwatches, phones, and sensors.

Cluster-based security organizes devices into groups with a cluster head.

---

# Working of Cluster-Based Security

1. Devices form clusters.
2. One node becomes Cluster Head (CH).
3. CH manages authentication and key distribution.
4. CH monitors member behavior.

---

# Architecture

| Component | Role |
|---|---|
| Cluster Head | Security management |
| Member Nodes | Normal communication |
| Gateway Node | Connects other networks |

---

# Security Functions

| Function | Description |
|---|---|
| Key Distribution | Shared keys distributed |
| Access Control | Unauthorized devices blocked |
| Monitoring | Detect malicious nodes |
| Data Aggregation | Efficient communication |

---

# Real World Use Case
## Healthcare PAN
Wearable sensors connect to smartphone.

### Cluster Head
Smartphone acts as CH.

### Benefits
- centralized security
- efficient battery use
- secure health monitoring

---

# Advantages

| Advantage | Description |
|---|---|
| Reduced overhead | CH handles security |
| Better scalability | Organized communication |
| Energy efficient | Less redundant transmission |

---

# Limitations

| Limitation | Description |
|---|---|
| Single point failure | CH compromise affects cluster |
| CH overload | High processing burden |
| Frequent re-clustering | Mobility causes instability |

---

# Mnemonic
## “KAMD”
**K**ey distribution  
**A**ccess control  
**M**onitoring  
**D**ata aggregation

---

# Conclusion
Cluster-based approaches improve PAN security through centralized management, efficient monitoring, and scalable communication.

---
---

# Q3(a) Describe a real-world scenario where preserving privacy in a MANET is critical.

# Scenario: Military Battlefield Communication

In military operations, soldiers use MANETs for communication without fixed infrastructure.

Privacy is critical because:
- enemy may intercept messages
- troop locations are sensitive
- attack plans must remain confidential

---

# Privacy Requirements

| Requirement | Importance |
|---|---|
| Confidentiality | Protect message contents |
| Anonymity | Hide sender identity |
| Location Privacy | Prevent troop tracking |
| Integrity | Prevent message tampering |

---

# Threats

| Threat | Description |
|---|---|
| Eavesdropping | Intercept communication |
| Traffic Analysis | Study communication patterns |
| Location Tracking | Identify troop movement |
| Impersonation | Fake military nodes |

---

# Privacy Protection Mechanisms

1. Encryption (AES)
2. Anonymous routing
3. Pseudonyms
4. Secure key management
5. Frequency hopping

---

# Example
A commander sends troop movement orders.
Encryption and anonymous routing prevent enemy interception.

---

# Advantages

| Advantage | Description |
|---|---|
| Secure communication | Prevents information leakage |
| Operational secrecy | Protects missions |
| Resistance to surveillance | Hides identities |

---

# Limitations

| Limitation | Description |
|---|---|
| Computational overhead | Encryption consumes power |
| Delay | Secure routing increases latency |
| Key management complexity | Difficult in dynamic MANET |

---

# Mnemonic
## “CALI”
**C**onfidentiality  
**A**nonymity  
**L**ocation privacy  
**I**ntegrity

---

# Conclusion
Privacy preservation is essential in military MANETs to protect sensitive data, locations, and communication from adversaries.

---
---

# Q3(b) Differentiate between signature-based and anomaly-based intrusion detection in wireless environments.

# Introduction
Intrusion Detection Systems (IDS) monitor wireless networks for malicious activity.

Two main approaches are:
1. Signature-based IDS
2. Anomaly-based IDS

---

# Comparison Table

| Feature | Signature-Based IDS | Anomaly-Based IDS |
|---|---|---|
| Detection Method | Known attack patterns | Deviation from normal behavior |
| Detects New Attacks | No | Yes |
| False Positives | Low | High |
| Training Required | No | Yes |
| Speed | Faster | Slower |
| Complexity | Low | High |

---

# 1. Signature-Based IDS

## Working
Compares traffic with attack database.

### Example
Detects known malware signatures.

## Advantages
- Accurate for known attacks
- Low false alarms

## Disadvantages
- Cannot detect zero-day attacks
- Needs regular updates

---

# 2. Anomaly-Based IDS

## Working
Learns normal behavior and detects deviations.

### Example
Sudden huge traffic from node detected as abnormal.

## Advantages
- Detects unknown attacks
- Adaptive security

## Disadvantages
- High false positives
- Computationally expensive

---

# Real World Example
Wi‑Fi IDS detects unusual traffic spikes indicating DDoS attack.

---

# Mnemonic
## “KUN”
**K**nown attacks → Signature IDS  
**U**nknown attacks → Anomaly IDS  
**N**ormal behavior analysis

---

# Conclusion
Signature-based IDS is efficient for known threats, while anomaly-based IDS is useful for detecting unknown attacks in wireless environments.

---
---

# Q3(c) How can mobile edge computing enhance security in hybrid wireless-wired network deployments?

# Introduction
Mobile Edge Computing (MEC) processes data near users instead of centralized cloud servers.

This improves security and reduces latency.

---

# Security Enhancements Using MEC

| Mechanism | Description |
|---|---|
| Local Threat Detection | Detect attacks near source |
| Reduced Data Exposure | Less data sent to cloud |
| Fast Incident Response | Low-latency mitigation |
| AI-based Monitoring | Real-time anomaly detection |
| Secure Authentication | Edge-based access control |

---

# Example
Smart city cameras process surveillance data locally.
Suspicious activity detected instantly.

---

# Advantages

| Advantage | Description |
|---|---|
| Low latency | Faster detection |
| Better privacy | Local data processing |
| Reduced bandwidth usage | Less cloud dependency |
| Scalability | Distributed architecture |

---

# Limitations

| Limitation | Description |
|---|---|
| Edge node compromise | Local attacks possible |
| Resource limitations | Less power than cloud |
| Management complexity | Many distributed nodes |

---

# Mnemonic
## “LFAS”
**L**ow latency  
**F**ast detection  
**A**I monitoring  
**S**ecure authentication

---

# Conclusion
MEC enhances hybrid network security through local processing, rapid detection, and reduced data exposure.

---
---

# Q4(a) Discuss the use of distributed trust models in drone-based delivery networks.

# Introduction
Drone delivery networks use UAVs for package transport.
Distributed trust models evaluate reliability of drones without central authority.

---

# Working of Distributed Trust Models

1. Drones monitor each other.
2. Trust scores assigned based on behavior.
3. Malicious drones receive low trust.
4. Routing/access decisions depend on trust.

---

# Trust Parameters

| Parameter | Meaning |
|---|---|
| Packet forwarding | Reliable communication |
| Energy level | Operational capability |
| Behavior consistency | Honest behavior |
| Delivery success | Correct package delivery |

---

# Example
If a drone repeatedly drops packets, other drones reduce its trust score.

---

# Advantages

| Advantage | Description |
|---|---|
| No central dependency | Decentralized security |
| Attack resilience | Malicious drones isolated |
| Scalability | Supports large fleets |

---

# Limitations

| Limitation | Description |
|---|---|
| False trust evaluation | Incorrect scoring |
| Communication overhead | Frequent trust updates |
| Collusion attacks | Malicious drones cooperate |

---

# Mnemonic
## “PEBD”
**P**acket forwarding  
**E**nergy level  
**B**ehavior consistency  
**D**elivery success

---

# Conclusion
Distributed trust models improve security and reliability in drone delivery systems by identifying malicious or unreliable drones.

---
---

# Q4(b) How can Zero Trust Security principles be integrated with Blockchain-based access control?

# Introduction
Zero Trust follows the principle:
“Never trust, always verify.”

Blockchain provides decentralized and immutable access control.

---

# Integration Process

| Zero Trust Principle | Blockchain Support |
|---|---|
| Continuous verification | Immutable authentication logs |
| Least privilege access | Smart contracts |
| Identity verification | Decentralized identity |
| Auditability | Transparent ledger |

---

# Working

1. User requests access.
2. Identity verified continuously.
3. Smart contract checks permissions.
4. Access decision stored on blockchain.

---

# Example
IoT smart factory uses blockchain smart contracts for machine access.

---

# Advantages

| Advantage | Description |
|---|---|
| Tamper resistance | Immutable records |
| Decentralized control | No single failure |
| Transparency | Easy auditing |
| Better trust | Continuous verification |

---

# Limitations

| Limitation | Description |
|---|---|
| High computational cost | Blockchain processing overhead |
| Scalability issues | Slow transaction rates |
| Energy consumption | Consensus algorithms costly |

---

# Mnemonic
## “CLIA”
**C**ontinuous verification  
**L**east privilege  
**I**mmutability  
**A**uditability

---

# Conclusion
Combining Zero Trust with blockchain improves decentralized authentication, transparency, and tamper-resistant access control.

---
---

# Q4(c)(a) Calculate aggregated trust value in VANET.

Given:
- Message integrity = 0.95, weight = 0.4
- Location accuracy = 0.85, weight = 0.3
- Behavior consistency = 0.9, weight = 0.3

---

# Formula
Weighted Trust Calculation:

genui{"math_block_widget_always_prefetch_v2":{"content":"T=(w_1x_1)+(w_2x_2)+(w_3x_3)"}}

Substitute values:

genui{"math_block_widget_always_prefetch_v2":{"content":"T=(0.4\times0.95)+(0.3\times0.85)+(0.3\times0.9)"}}

Calculation:
- 0.4 × 0.95 = 0.38
- 0.3 × 0.85 = 0.255
- 0.3 × 0.9 = 0.27

Final:

genui{"math_block_widget_always_prefetch_v2":{"content":"T=0.38+0.255+0.27=0.905"}}

# Final Answer
## Aggregated Trust Value = 0.905

---

# Interpretation
A trust value of 0.905 indicates a highly trustworthy vehicle node.

---
---

# Q4(c)(b) Explain how blockchain can provide immutability and auditability in wireless access control systems.

# Introduction
Blockchain stores records in linked blocks using cryptographic hashes.

This ensures immutability and auditability.

---

# Immutability

## Meaning
Data cannot be modified after recording.

## How Achieved
- Each block contains previous block hash.
- Tampering changes hash values.
- Network rejects altered chain.

---

# Auditability

## Meaning
All actions are traceable.

## Features
- Permanent logs
- Timestamped records
- Transparent verification

---

# Example
Every Wi‑Fi access request stored on blockchain.
Administrators can trace:
- who accessed
- when accessed
- permission granted

---

# Advantages

| Advantage | Description |
|---|---|
| Tamper-proof records | High integrity |
| Transparent auditing | Easy monitoring |
| Decentralization | No single authority |

---

# Limitations

| Limitation | Description |
|---|---|
| Storage overhead | Large blockchain size |
| Slow transactions | Consensus delay |
| Energy cost | Mining overhead |

---

# Mnemonic
## “HAT”
**H**ashes  
**A**udit logs  
**T**imestamps

---

# Conclusion
Blockchain enhances wireless access control through immutable records and transparent auditing.

---
---

# Q5(a) Define the general architecture of an IoT system and explain its key components.

# Introduction
IoT architecture connects physical devices, communication networks, processing systems, and applications.

---

# General IoT Architecture

| Layer | Function |
|---|---|
| Perception Layer | Sensors and data collection |
| Network Layer | Communication and routing |
| Processing Layer | Data processing/storage |
| Application Layer | User services |

---

# 1. Perception Layer

## Components
- Sensors
- RFID
- Actuators

## Function
Collect environmental data.

### Example
Temperature sensor in smart home.

---

# 2. Network Layer

## Technologies
- Wi‑Fi
- Bluetooth
- ZigBee
- 5G

## Function
Transfers data.

---

# 3. Processing Layer

## Functions
- Cloud computing
- Data analytics
- Security management

---

# 4. Application Layer

Provides services to users.

### Examples
- Smart healthcare
- Smart cities
- Smart agriculture

---

# Advantages

| Advantage | Description |
|---|---|
| Automation | Reduced manual work |
| Real-time monitoring | Continuous observation |
| Remote access | Control from anywhere |

---

# Limitations

| Limitation | Description |
|---|---|
| Security risks | Vulnerable devices |
| Privacy concerns | Data leakage |
| Interoperability issues | Different standards |

---

# Mnemonic
## “PNPA”
**P**erception  
**N**etwork  
**P**rocessing  
**A**pplication

---

# Conclusion
IoT architecture integrates sensors, networks, processing, and applications to enable smart connected systems.

---
---

# Q5(b) List the main security requirements of IoT in healthcare systems.

# Introduction
Healthcare IoT handles sensitive patient information and medical devices.
Strong security is essential.

---

# Main Security Requirements

| Requirement | Purpose |
|---|---|
| Confidentiality | Protect patient data |
| Integrity | Prevent data modification |
| Availability | Ensure continuous service |
| Authentication | Verify users/devices |
| Authorization | Restrict access |
| Privacy | Protect personal information |
| Non-repudiation | Prevent denial of actions |

---

# 1. Confidentiality
Encryption protects medical records.

### Example
AES encryption in hospital systems.

---

# 2. Integrity
Hash functions ensure data accuracy.

---

# 3. Availability
Medical systems must remain operational.

### Example
ICU monitoring systems.

---

# 4. Authentication
Only authorized doctors access records.

---

# 5. Privacy
Compliance with HIPAA/GDPR.

---

# Threats in Healthcare IoT

| Threat | Impact |
|---|---|
| Ransomware | Hospital shutdown |
| Data breach | Privacy loss |
| Device hijacking | Patient safety risk |

---

# Advantages of Security Measures

| Advantage | Description |
|---|---|
| Better patient trust | Secure systems |
| Safe treatment | Accurate data |
| Regulatory compliance | Legal protection |

---

# Limitations

| Limitation | Description |
|---|---|
| High implementation cost | Advanced security tools |
| Resource constraints | Small devices |
| Complex management | Large device networks |

---

# Mnemonic
## “CIA-APN”
**C**onfidentiality  
**I**ntegrity  
**A**vailability  
**A**uthentication  
**P**rivacy  
**N**on-repudiation

---

# Conclusion
Healthcare IoT security focuses on protecting patient safety, privacy, and system reliability.

---
---

# Q5(c) List and explain types of IoT attacks with real-world examples.

# Introduction
IoT devices are vulnerable because of weak security, limited resources, and Internet connectivity.

---

# Types of IoT Attacks

| Attack | Description | Example |
|---|---|---|
| DDoS Attack | Floods network traffic | Mirai botnet |
| Malware Attack | Infects IoT devices | Smart camera malware |
| Eavesdropping | Intercepts communication | Wi‑Fi sniffing |
| Replay Attack | Reuses captured packets | RFID attacks |
| Man-in-the-Middle | Intercepts communication | Fake Wi‑Fi AP |
| Physical Attack | Direct hardware tampering | Sensor manipulation |

---

# 1. DDoS Attack
Large number of compromised IoT devices flood servers.

## Example
Mirai botnet attacked Dyn DNS in 2016.

---

# 2. Malware Attack
Malicious software infects IoT systems.

### Example
Smart cameras used in botnets.

---

# 3. Eavesdropping
Attackers listen to unencrypted communication.

---

# 4. Replay Attack
Captured packets resent to gain access.

---

# 5. MITM Attack
Attacker positions between devices.

---

# Advantages for Attackers

| Advantage | Explanation |
|---|---|
| Weak device security | Easy compromise |
| Large attack surface | Millions of devices |

---

# Security Countermeasures

| Countermeasure | Protection |
|---|---|
| Encryption | Confidentiality |
| Authentication | Prevent unauthorized access |
| IDS | Attack detection |
| Firmware updates | Patch vulnerabilities |

---

# Mnemonic
## “DMERM”
**D**DoS  
**M**alware  
**E**avesdropping  
**R**eplay attack  
**M**ITM

---

# Conclusion
IoT attacks target device vulnerabilities and network weaknesses. Proper encryption, authentication, and updates are essential for protection.

---
---

# Q5(d) Propose a cyber-physical protection strategy that includes both data and device-level safeguards.

# Introduction
Cyber-physical systems integrate physical devices with digital communication.
Protection must secure both data and hardware.

---

# Protection Strategy

# 1. Data-Level Safeguards

| Safeguard | Purpose |
|---|---|
| Encryption | Protect confidentiality |
| Hashing | Ensure integrity |
| Access Control | Restrict users |
| Backup Systems | Recovery after attacks |

---

# 2. Device-Level Safeguards

| Safeguard | Purpose |
|---|---|
| Secure Boot | Prevent unauthorized firmware |
| TPM/Hardware Security Module | Secure key storage |
| Physical Locks | Prevent tampering |
| Firmware Updates | Patch vulnerabilities |

---

# 3. Network-Level Protection

- Firewalls
- IDS/IPS
- Segmentation
- VPN tunnels

---

# Example
Smart power grid:
- encrypted communication
- secure substations
- authenticated controllers
- continuous monitoring

---

# Advantages

| Advantage | Description |
|---|---|
| Multi-layer security | Better protection |
| Reduced attack impact | Faster recovery |
| Improved reliability | Stable operations |

---

# Limitations

| Limitation | Description |
|---|---|
| High cost | Advanced hardware/security |
| Complex deployment | Multiple technologies |
| Maintenance overhead | Continuous updates |

---

# Mnemonic
## “EHAF”
**E**ncryption  
**H**ardware security  
**A**ccess control  
**F**irmware updates

---

# Conclusion
An effective cyber-physical protection strategy combines encryption, authentication, secure hardware, and continuous monitoring to protect both data and physical infrastructure.

---

# Important Exam Writing Tips (William Stallings Style)

1. Start with definition/introduction.
2. Draw architecture or flow if possible.
3. Use tables for comparison.
4. Mention advantages and limitations.
5. Add real-world examples.
6. End with concise conclusion.
7. Write keywords in bold/underline during exam.

---

# Quick Master Mnemonic List

| Topic | Mnemonic |
|---|---|
| Access Point Security | AETRM |
| Wireless Standards | RAW |
| Jamming Defense | FCDSP |
| MANET Mobility | RATS |
| Secure Routing | SMART |
| PAN Security | KAMD |
| MANET Privacy | CALI |
| IDS Types | KUN |
| MEC Security | LFAS |
| Drone Trust | PEBD |
| Zero Trust + Blockchain | CLIA |
| Blockchain Security | HAT |
| IoT Architecture | PNPA |
| Healthcare IoT | CIA-APN |
| IoT Attacks | DMERM |
| Cyber-Physical Security | EHAF |

---

# End of Solved Paper

