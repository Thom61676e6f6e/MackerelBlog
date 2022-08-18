---
title: "ICS and OT Security Overview"
categories:
  - ICS
tags:
  - OT
  - ICS
toc: true
toc_label: "ICS and OT Security Overview"
toc_icon: "cogs"
---
<h2 id="header-two">Abstract</h2>
The world of OT and ICS devices is a complex system rooted in our daily lives. While most people are unaware of the existence of these devices, they are responsible for running most of our critical infrastructures, such as Water, Electric, Shipping, Transportation, and many others. These systems are built to automate and monitor processes in these facilities. But what happens when a malicious party takes over these systems. The security of these devices can be paramount to National Security. Widespread damage and outages can affect an entire nation, Attacks focused on these systems have begun to increase throughout the past years, and the trend indicates that this will continue. The security of these devices is sometimes lacking, but innovation focused on this space has led to better security in the long term. Implementing these security controls on critical infrastructure allows the analyst to identify and respond to these events before irreparable damage occurs. These controls also help support a common goal of securing these networks because we will give a blueprint of these attacks, enabling us to secure these networks further and help respond to potential attacks faster. 
<h3 id="header-three">WHAT IS OT</h3>
Operational Technology commonly refers to any piece of technology, whether hardware or software, used to Operate, Control, or Monitor Industrial equipment assets and processes. These devices are generally simple devices that send requests or commands and either respond to the request or execute these commands to the specified devices. While these devices share common networking and protocols with Information Technology devices, these devices exist in the same realm but have very different purposes, These OT devices are designed to perform specific task and are not generally found in a data center, they exist on the floors or in tunnels near the machines that they are designed to interact with.  
<h3 id="header-three">WHO USES OT DEVICES?</h3>
While most OT devices are generally unnoticed, these endpoints are Critical for running operations in many different facilities; these devices are commonly found in industries that deal with Energy production and distribution, Manufacturing, Transportation, and Utilities. These devices help monitor and control the work needed to produce the goods and services we need for daily life. The ability to automate and monitor accounts in these industries makes it possible for these companies to provide these resources at scale.
<h3 id="header-three">OT VENDORS </h3>
While there are millions of OT devices out in the world, they are primarily produced by a few companies; the primary producers of these devices are Siemens, Schneider Electric, Emerson, Yokogawa, Honeywell, and Allen-Bradley. Each company produces a wide range of standard OT and ICS devices. However, some are more focused on specific sectors than others. Siemens and Schneider Electric focus on the Energy Sector, Emerson and Yokogawa focus on the Oil and Water sector. Honeywell and Allen-Bradley tend to be focused on the manufacturing sector. While these are a general overview of the industries these devices support, they are not tied directly to these and may produce controls for other industries. Another area is the Industrial Internet of Things producers. While most of these companies produce IIoT devices, this has also opened the market to other vendors to produce their own IIoT devices on to the market.
<h3 id="header-three">OT Devices</h3>
A Short overview of typical OT and ICS devices found in modern networks
<h4 id="header-four">SCADA</h4>
A Supervisory Control and Data Acquisition system is a system that controls a wide range of Remote Terminal Units known as RTUs. The primary responsibility of the SCADA system is the ability to interact with RTUs and PLCs. All SCADA systems have the same components regardless of their intended use: Input Devices (Keyboard, Mouse, etc.) Graphical Display, Networking, Alarms and Alerts, Monitoring, and an Interface for connecting to Programmable Logic Controllers (PLCs) and Remote Terminal Units (RTU). These systems are generally built to be redundant and Scalable and use specialized software to manage their operations. 
<figure style="width: 300px" class="align-center">
  <img src="https://thom61676e6f6e.github.io/MackerelBlog/assets/images/ICSOTimages/scada.jpg" alt="" />
  <figcaption> (Bailey & Wright, 2003) </figcaption>
</figure>
<h4 id="header-four">DCS</h4>
A Distributed Control System is a device that allows operator workstations to interact with OT devices to send commands and monitor the devices in the network. DCS can also trigger devices to automate processes in the OT Network such as starting or stopping actions depending on the states it receives and taking corrective actions if the given state is not within its operational guidelines. For the Operator end, these devices also can poll the connected devices for data that an operator can review.
<figure style="width: 300px" class="align-center">
  <img src="https://thom61676e6f6e.github.io/MackerelBlog/assets/images/ICSOTimages/dcs.jpg" alt="" />
  <figcaption> (Bailey & Wright, 2003) </figcaption>
</figure>
<h4 id="header-four">PLCs</h4>
A Programmable Logical Controller is what SCADA and DCS rely on to send messages to the endpoint devices, which can be any machines found on the factory floor or plant, such as robots, valves, machines, or various industrial control. Programmable logical controllers are devices that perform input and output operations and take simple process information to complete their tasks. One benefit to PLCs is their ability to operate in various environments. 
<h4 id="header-four">RTU</h4>
Remote Terminal Devices are the same as a Programable logic controller. However, one crucial feature, these devices can do any task that a PLC will do but also have the benefit of being able to run as its entity which gives it the ability to monitor and operate the machine it is connected to. Because of this feature, these devices allow remote users to enable management from a central location.
<h3 id="header-three">Communicating with OT Devices</h3>

<h4 id="header-four">DNP3</h4>
Distributed Network Protocol was developed in YEAR and later adopted by IEEE in 2010. The DNP3 protocol uses serial and Internet Protocol connections to send data to the SCADA system; this protocol has been developed as a more reliable communication method from SCADA systems to RTUs. DNP3 uses a master and outstation model to orchestrate commands and uses CRC Checks for error detection. According to "The data payload in the link frame contains a pair of CRC octets for every 16 data octets. This provides a high degree of assurance that communication errors can be detected." (Curtis, 2005). DNP3 also supports TLS to improve the security of the protocol.
<h4 id="header-four">Modbus</h4>
Schneider Electric developed Modbus in 1979, and it is an open-source standard that is used across a wide range of devices. It supports Serial and Ethernet connections between SCADA and PLCs in its modern format; it has also been adapted to be used to communicate with RTUs. Modbus is continuously updated to this day and now supports CRC and TLS security.
<h4 id="header-four">IEC 61850</h4>
IEC 61850 is the protocol that is primarily used to communicate with Intelligent Electrical Devices. IEC61850 can be transmitted over TCP/IP as well as substation networks
<h4 id="header-four">OPC</h4>
Open Platform communications were developed to create a common language for Windows and PLCs to reduce the need for duplicating efforts to send logs between the two platforms.
<h4 id="header-four">PROFINET</h4>
Process Field Net is a communication standard used for communicating over industrial ethernet, which is not to be confused with standard ethernet. These protocols tend to transmit on layer two as opposed to layer three. These connections offer lower latency than traditional ethernet.
<h3 id="header-three">OT Programming</h3>

<h4 id="header-four">Ladder diagram</h4>
Ladder Logic is one of the first uses of programing PLCs; In contrast, Ladder logic is a programing language for PLCs. It was initially developed to show the relation of relays in a rack as the process worked through the function. It has now been adopted for PLC instruction sets.
<figure style="width: 300px" class="align-right">
  <img src="https://thom61676e6f6e.github.io/MackerelBlog/assets/images/ICSOTimages/ladderdiagram.gif" alt="" />
  <figcaption>(Romanov, 2020) </figcaption>
</figure>
<h4 id="header-four">Function block diagram</h4>
FBD is a graphical-based form of PLC programming generally used for chemical processes. Function blocks tend to work in a loop where one input will go back to the output and loop till the exit condition is met. The function block is useful for smaller applications but can be troublesome when scaled
<figure style="width: 300px" class="align-right">
  <img src="https://thom61676e6f6e.github.io/MackerelBlog/assets/images/ICSOTimages/functionblock.png" alt="" />
  <figcaption>(Romanov, 2020) </figcaption>
</figure>
<h4 id="header-four">Structured text</h4>
Structured text programming is the closest to modern programming languages. While this makes it easier to develop the same rules apply to ST as any other programing language where error handling must be written into the program or the PLC will run into an error condition. Looking at the output below, you can see the resemblance to C.
<figure style="width: 300px" class="align-right">
  <img src="https://thom61676e6f6e.github.io/MackerelBlog/assets/images/ICSOTimages/structredtext.jpg" alt="" />
  <figcaption>(Romanov, 2020) </figcaption>
</figure>
<h4 id="header-four">Instruction list</h4>
Instruction List is a text-based form of programming that relies on sending an ordered list to a PLC that it can step through. Instruction lists are very similar to the assembly language. Generally a command is loaded with an LD value and this is set to an accumulator to be processed.
<figure style="width: 300px" class="align-right">
  <img src="https://thom61676e6f6e.github.io/MackerelBlog/assets/images/ICSOTimages/instructionlist.jpg" alt="" />
  <figcaption>(Mitsubishi Electric, 2009)</figcaption>
</figure>
<h4 id="header-four">Sequential function chart</h4>
Sequential functions are similar to the instruction list but will verify the state of the device and environment; once the state has been confirmed, the sequential function will move to the following condition and will continue until the process has been completed. Structured text can be included within SF for more complex operations.
<figure style="width: 300px" class="align-right">
  <img src="https://thom61676e6f6e.github.io/MackerelBlog/assets/images/ICSOTimages/sequential.jpg" alt="" />
  <figcaption>(Romanov, 2020) </figcaption>
</figure>
<h3 id="header-three">Why are ICS and OT Security Important?</h3>
The disruption of OT devices can have various effects on an organization in the manufacturing industry and potentially have to stop production entirely. At the same time, systems are restored, which can be a massive loss of profits. Other issues that can arise are the tampering of OT devices that substitute values so that the machines being controlled are not mixing materials correctly or possibly forcing the machines to operate in a manner that can cause damage to the machinery.
	The effects on the Energy industry can have potentially damaging effects on the countries or areas that are affected. OT controls in the energy sector allow plants to operate safely and provide the consistency needed to produce and transmit energy. If these controls are compromised, it can have an overall effect. Very few things in the modern age function without electricity; this can affect almost all aspects of life and potentially shut down entire cities if they are compromised.
	Transportation is another industry that can have potentially devastating effects in case of a compromise of an OT network. According to the New York MTA, Over 5 million people ride the subway on an average weekday (pre-Covid). The New York MTA operates 64000 Subway cars on 665 Miles of the track. If an attack were successfully launched against the New York MTA, this would turn into a massive shutdown of the transportation system for a major American city. 
	The Port of Los Angeles is responsible for importing over 10,677,610 TEUs (Twenty-foot Equivalent Units) in 2021 Per (The Port Of Los Angeles, 2022). The OT systems that exist to keep the port operating efficiently; disruption of these critical systems could result in the port not having the ability to dock ships and unload them so they can get the next ship in to start the process over again.
If these complex OT networks are compromised, there can be a lot of adverse effects, from ruining production to power outages or supply chain interruptions. When IT systems are compromised, it can reveal personal information, or there can be a financial impact; with OT compromises, there is the potential loss of life. This can have a massive effect on a population when basic needs can no longer be met.

<h3 id="header-three">Notable OT Attacks</h3>
<h4 id="header-four">Australia – Maroochy shire Water Services</h4>
In 1999, The Maroochy Shire council had a SCADA system installed for their waste waters services; in 2000, the system began to experience unexplained shutdowns such as

•	Pumps were not running when they should have been 
•	Alarms were not reporting to the central computer 
•	A loss of communication between the central computer and various pumping stations. 
(Abrams & Weiss, 2008)
The controls were rebooted, and the system was running as intended. These shutdowns and malfunctions continued to happen. The city decided to bring in an investigator from the company that installed the equipment to investigate the incident and rule out the faulty equipment that caused the issues. The Investigator concluded that there was no faulty equipment in the SCADA system. But the outages continued; on 4/23/00, Vitek Boden was arrested near one of the pumping houses with a computer and radio equipment in his car.
Vitek had been an employee of Hunter Watertech during the installation of the SCADA system; he had quit his job at Hunter Watertech and was seeking employment from the city council. After his application was rejected, Vitek Boden decided to take revenge on the city. Using his knowledge of the SCADA system and a Radio transmitter, he could remotely send commands to the pumps. He shut them down, causing over 265000 gallons of sewage to flood the township and irreparably affecting the wildlife ecosystem in the area.
<h4 id="header-four">Stuxnet</h4>
In 2010, Stuxnet is regarded as the most sophisticated attack on an OT and IT environment, and On the IT side, the attack was the emergence of the EternalBlue exploit. As part of its OT component, this Malware was a worm that could interact with the Iranian-made IR-1 Centrifuge" These centrifuges are also fragile, and an abrupt change of speed can cause damage or even breakage" (Baezner & Robin, 2017). Iran operates 15000 of these centrifuges at the Natanz Nuclear Refinement facility. 
Stuxnet was able to compromise the networked workstations in the facility. From there, the worm was able to attach itself to USBs that were plugged into a workstation. Once a USB was infected and plugged into another device, the worm would begin propagating until it reached the air-gapped OT network. At this point, it could send commands to the centrifuges and commence its intended attack. While there is no clear attribution to the creation and deployment of this worm, it is believed that NATO, The United States, or Israel may be responsible for orchestrating this attack.
<h4 id="header-four">NotPetya</h4>
In 2017, Maersk Experienced a ransomware attack requesting 300 dollars to decrypt this device; soon, a large portion of the organization was presented with the same screen. While Petya was a ransomware attack from the previous year, this Ransomware was a ruse; while the device was encrypted, this was not the attack's goal, and neither was Maersk; They were the fallout of the attack.
 	Before this attack, a Ukrainian-based tax software company called M.E.Doc had been hacked. The attackers had compromised the server M.E.Doc used to send updates to their customers. By packaging the Malware disguised as Ransomware with an update, they pushed this virus to every user of M.E.Doc, including Maersk. Once the Malware was on a system, the system was already gone.
When looking at the effects of NotPetya on Ukraine, Andy Green gives the best summary," It would hit at least four hospitals in Kyiv alone, six power companies, two airports, more than 22 Ukrainian banks, ATMs, and card payment systems in retailers and transport, and practically every federal agency." (Greenberg, 2018), Because of these attacks, it took Ukraine Months and possibly years to return to full operational capacity in their energy sectors.
The effects ranged much further than its original target of Ukraine "It ¬crippled multinational companies including Maersk, pharmaceutical giant Merck, FedEx's European subsidiary TNT Express, French construction company Saint-Gobain, food producer Mondelēz, and manufacturer Reckitt Benckiser." (Greenberg, 2018)
While attacks take many resources to identify the source confidently, This Attack has been Directly linked to the Russian GRU group known as Sandworm, which has been launching attacks against Ukraine for years. On October 15, 2020, the United States defense department filed an indictment naming 6 GRU hackers as the perpetrators of this attack

<h4 id="header-four">Triton</h4>
In 2017 a chemical processing plant based in Saudi Arabia was alerted to an unsafe condition developing in their chemical processing zone; this prompted the facility to shut down and examine the controllers in the network; the onsite technician had decided this was a glitch in the system and decided to bring the system back online. Later that week, the same condition was reported, prompting the company to reach out to a third party for an investigation into the network.
The company deployed Triconex systems produced by Schneider electric to run their emergency shutdown protocols. These controllers are responsible for "critical use cases including emergency shutdown systems, burner management, fire and gas detection, high-pressure protection, and turbomachinery control. Failure of any of these systems can have catastrophic impacts." (Virsec, 2019) Failure of these controls can result in the death of everyone at the facility and potentially nearby communities.
During the investigation, it was discovered that the attackers were in the system starting in 2014 and had managed to pivot into the engineering workstations on the IT network. These machines were dual-homed and interacted with the SCADA system. From these engineering machines, the attackers could send commands to the Triconex system to ignore unsafe conditions and allow the plant to continue operating. As a failsafe, The Triconex system has a physical key that needs to be turned to PROG for the controller to accept commands. However, the system will still run while in the PROG mode to not disrupt operations. Roughly half of these controllers were left in this mode, and these were compromised.
Attribution for these attacks is not always easy to identify, while this could be any group that views Saudi Arabia as an enemy. It is believed that a Russian-backed group carried out this attack, but this remains to be confirmed.

<h4 id="header-four">Conclusion</h4>
Attacks against OT systems are not an everyday event. These attacks tend to come from one primary source: Nation State Actors. Most organizations have a strong security posture regarding securing Operational Technology. But not all of them failing to take proper precautions can lead to hackers compromising systems. However, when you look at the complexity of these attacks, they are being run by well-funded groups that can develop the tools they need to execute them. While, Nation State actors are the biggest threat to operational security. The risk of insider threats can be just as damaging, if not more because these attackers have a leg up on the company; they can easily carry out these attacks because they know where to look.
<h3 id="header-three">OT threat actors</h3>
<h4 id="header-four">Russia</h4>
Regarding volume and severity of attacks, Russia has become one of the largest threats to operational technologies. The Russian Government has multiple bureaus that are engaged in hacking efforts across the world. MITRE ATT&CK has identified 13 groups responsible for ICS attacks. Five of these groups are Russia State-Backed. Dragonfly[G0035], Sandworm [G0034], TEMP.Veles [G0088], Wizard Spider [G0102], and ALLANITE [G1000].
<h4 id="header-four">Iran</h4>
While Russia tends to be behind a wide range of ICS attacks, Iran has been ramping up attacks against critical infrastructure. Three groups have been linked to state actors. Primarily their targets have been located in the middle east, but in recent reports, they have been expanding their efforts outside the middle east. MITRE has observed these three groups, in particular, OilRig [G0049], APT33 [G0064], and  HEXANE [G1001].
<h4 id="header-four">North Korea</h4>
While North Korea has compromised ICS systems, their primary goal seems to be financially motivated, and these compromises seem to be residual fallout from their attacks. MITRE ATT&CK has identified these two groups APT38 [G0082] and Lazarus Group [G0032]
<h4 id="header-four">Various groups</h4>
The last three groups have been traced to ICS attacks, but these are typically due to misconfiguration or gaps in security that allow these attacks to affect critical systems. MITRE ATT&CK has identified these groups as FIN6 [G0037],  FIN7 [G0046], and GOLD SOUTHFIELD [G0115].
•	FIN6 – "This group has aggressively targeted and compromised point of sale (PoS) systems in the hospitality and retail sectors." (ATT&CK, FIN6, 2017)
o	Also known for spreading Magecart
•	FIN7 – "financially-motivated threat group that has been active since 2013 primarily targeting the U.S. retail, restaurant, and hospitality sectors, often using point-of-sale malware." (ATT&CK, FIN7 , 2017)
•	Gold Southfield – "operates the REvil Ransomware-as-a Service (RaaS). GOLD SOUTHFIELD provides backend infrastructure" (ATT&CK, GOLD SOUTHFIELD, 2020)

<h4 id="header-four">Insider Threats</h4>
One prevalent trend in OT compromises is Insider threats, and These attacks tend to be significant because of the attackers' knowledge of the network. At the same time, these attacks can be mitigated for former employees. Those still employed can pose a threat to security.
<h3 id="header-three">OT Security and Risk Frameworks</h3>
<h4 id="header-four">NIST SP 800-82 Rev. 2</h4>
NIST, or National Institute of Standards and Technology, is a federal agency that promotes standards and practices for Technology and science. NIST has produced the NIST SP 800-82 Rev 2 as a guide for the Secure Deployment of ICS devices, Including SCADA, DCS, and PLCs that comprise an OT network. All NIST publications are free to view and use.
 800-82 outlines
•	Risk management and assessments
•	Security Program Development
•	Architecture
•	Security controls
•	Supervisory control
<h4 id="header-four">IEC 62443</h4>
IEC, the International Electrotechnical Commission, is the Standard for securing ICS controls. The group is an international standards organization that is based in Switzerland. It is similar to the NIST 800-82. IEC 62443 is written and controlled by an independent board, and the documentation for the Standard is a paid service offered by IEC.

<h4 id="header-four">ISO 27000 series</h4>
ISO is the International Organization for Standardization; ISO 27000 series refers to the family of documentation that outlines the secure deployment and operation of ICS devices. The 27000 series is widely adopted Standard for ICS controls. This series is co-written with the IEC. 
<h3 id="header-three">OT Security Models</h3>
The most common models for deploying ICS devices in a secure network are the Perdue model and the ISA-95 Model. While both models have advantages, both models are sufficient for deploying secure networks for ICS devices.
<h4 id="header-four">Purdue Model</h4>
The Purdue Model was designed in the 1990s at Perdue University, where it gets its name; the Perdue model functions on a simple principle of layered networks that shield the critical components of the ICS network from the IT network. While still enabling the ICS devices and IT devices to share a standard network that restricts access using Network segregation. The Model relies on the use of a Top-down Level system
<h5 id="header-five">Level 5</h5>
This level is the enterprise network. This zone is responsible for network services. This level is sometimes combined with Level 4
<h5 id="header-five">Level 4</h5>
This level is the enterprise network. This zone is responsible for the Domain network and workstations.
<h5 id="header-five">DMZ</h5>
The DMZ or Demilitarized Zone refers to the gap between the ICS systems and the Enterprise network 
<h5 id="header-five">Level 3</h5>
The ICS management level is where the Alarms, Monitoring, and other Human Interaction is possible.
<h5 id="header-five">Level 2</h5>
Is level is responsible for the ICS supervisory controls such as DCS; devices are broken into groups by their work process at this boundary. 
<h5 id="header-five">Level 1</h5>
Level 1 is responsible for containing the PLCs and RTUs
<h5 id="header-five">Level 0</h5>
Is the physical process Devices such as Pumps, Mills, IIoT Devices etc.
<h5 id="header-five">Graphical representation Of Purdue Model</h5>
<figure style="width: 1200px" class="align-center">
  <img src="https://thom61676e6f6e.github.io/MackerelBlog/assets/images/ICSOTimages/purduegraphic.png" alt="" />
  <figcaption>(Greenfield, 2020)</figcaption>
</figure>
<h3 id="header-three">OT Security & Monitoring</h3>
OT security is a relatively overlooked area when it comes to options. The use of IT security controls can be implemented in most OT environments. While some of these devices need to be specialized to pull data or read data coming off the wire it is easy to implement security controls given the correct solution. Having proper controls and security is essential, but it is vital to understand risk management in this area. 
For simplicity's sake, I am referring to the Purdue model when referring to Levels 0, 1, and so on as an example of deployment options. One thing of note is the level of insight an organization needs to develop within the OT boundaries. 

<h4 id="header-four">OT SIEM Solutions</h4>
SIEMS can offer a wealth of information. Because of the separation of OT networks given in the Purdue model, the use of a OT specific SIEM is a valuable resources for organizations. Deploying a SIEM specifically for OT use allows the ICS environment to manage track and respond to threats that may develop in the network. By proxies, it is possible to route SIEM information to the DMZ.
Routing SIEM logs to a proxy will enable the SOC to integrate the OT messages and alerts into the IT network's SIEM solution; this level of control helps retain a central point where all alerts can be viewed. This way, the organization has a unified view of all its operations. If OT SIEM information is not being carried to the IT area, this can cause potential lapses in the SIEMS's ability to organize and track events. 

<h4 id="header-four">IDS/IPS</h4>
Intrusion Detection and Prevention Devices are a standard for most security programs. The use of these devices is not limited to the IT realm. IDS and IPS systems tend to come in two variations, either Host Based or Network based. Because of the existing network segregation in the Purdue model, it is possible to place NIDS between the levels, giving a granular look at the traffic flowing through each zone. 
The use of network monitoring is an effective tool for Level 0 up to Level 3. By monitoring the connections being established, it will be possible to break down traffic flowing up to the DMZ; anything flowing to the DMZ will be previously defined protocols. For example, if an attacker was attempting to fingerprint a network and ICMP was explicitly denied, a NIDS would be able to quickly pick up this traffic which could point to a potential IOC. 
 When looking at NIDS from an Enterprise(level 5/4) Perspective, we can see what traffic is flowing to the DMZ and what traffic is flowing from the DMZ to the OT(Level 3-0) boundary. Rule-based IDS systems are valuable in this area because the protocols allowed through the boundary are limited.

<h4 id="header-four">Air-Gap</h4>
Air-gapped networks tend to be one of the solutions that many organizations tend to lean on; following the Stuxnet attack, it was proven that to jump this air-gapped network takes a lot of technical ability, but the possibility of air-gapped networks being compromised by the tools and resources that are brought into this areas remains a threat to the environment.
<h4 id="header-four">Vulnerability Scanning</h4>
IT networks have a host of tools readily available such as Nessus or Rapid7; OT environments are not always readily able to be scanned. Tenable, the makers of Nessus, have begun to cross this boundary to start scanning OT networks (Tenable, 2022), Tenable OT product can integrate with The IT tenable deployment which can give an organization the ability to centrally manage vulnerabilities across the network. One of the important aspects of vulnerability management is the implementing a accurate asset management system. This is another system that can be integrated into the network.
<h4 id="header-four">Configuration management</h4>
Configuration management is another tool that is dependent on an asset management system. By leveraging configuration management system it gives the organization the insight into how the systems are supposed to be configured and According to Langner the core methods of Configuration management is Baselines, Change management, Lifecycle management. With these methods is possible to develop a system for understanding the network as well as help security find anomalies in the OT Devices. Configuration management is not only a security tool but also a production tool.
<h3 id="header-three">OT Incident Response</h3>
When you look at the incident response in the view of IT, we have set a lot of standards and best practices for effective response; one advantage of IT Incident response is the type of devices that are in the environment; generally speaking, environments are Windows or Linux and primarily Linux. When looking at OT devices, a handful of vendors are running their own propriety software on their devices. Sometimes, the firmware on these systems or devices will differ depending on the device's application. This widens the scope of an incident responder.
	Incident response can only be as effective as the resources in the environment. If the proper controls are not put in place when building or securing the environment, it will be difficult even to know if an incident has occurred until a disruption has occurred. PICERL (Preparation Identification Containment Eradication remediation Lesson learned) is still possible for OT environments, but it has to start with Preparation. 
Utilizing systems such as SIEM, NIDS, and configuration management can help bring this wide array of devices into a manageable containment system to identify and adequately respond to when these incidents occur. There are many different resources out there that are free and readily available CISA has developed an Incident Response process specifically for OT environments. 

<h3 id="header-three">OT Forensics</h3>
Memory Forensics is a popular form of gathering forensic data; PLCs and RTU are essential devices that rely on RAM to execute a task. Forensics becomes more complex in OT environments because of how PLCs handle data, and developing sound practices can be more difficult. Forensics in the OT area is dependent on the same resources as incident response. 	
The issue we are presented with in OT environments is the availability of forensic data. Suppose the SCADA or DCS system misses or fails to log operations on PLCs properly. In that case, we become reliant on the memory, and RAM is volatile memory. If these devices are switched off during an incident, we may lose important information on what is occurring. Monitoring SIEM or NIDS is critical in these areas, and proper logging enables investigators to use Log correlation and configuration management to track changes in the environment.

<h3 id="header-three">OT Adversarial Emulation</h3>
Adversarial Emulation is essential for securing IT networks, this practice can be applied to OT networks, but one issue with OT is the lack of Adversarial Emulation; this creates a gap for ICS responders and Security professionals while we have seen the effects of ICS Attacks there are not many resources to help train and test the professionals that work in these areas. One of the most significant issues is that OT networks can be highly complex, and it can be hard to build accurate representations of OT networks. While it is possible to run through events, it is not easy to simulate ICS Events to the level you can with IT systems. Unless organizations are willing to pay a decent sum of money to build these tests it is not accessible to find modern and relevant training in this area.
I have found two sources: SANS top 5 ICS response Tabletops and CISA's Tabletop exercises. 

<h3 id="header-three">Conclusion</h3>
Attacks on Critical infrastructure have been growing at a steady rate. Without proper implementation of security systems for ICS, it will be challenging to stop these attacks before it has caused a significant effect on the industries they are supporting. ICS attacks have had profound effects on multiple industries, but one example that stands out the most is NotPetya. The ability of one nation to effectively stop another by attacking OT is a grim reminder of the effects these large-scale attacks can have. Implementing security controls around critical power and water infrastructure is necessary. Attacks in this area will only increase, and the only way to stay ahead is to increase the security and controls at the same rate.
<h3 id="header-three">References</h3>
Abrams, M., & Weiss, J. (2008). Malicious Control System Cyber Security Attack Case Study–Maroochy Water Services, Australia. MITRE Corporation.
ATT&CK, M. (2017, May 31). FIN7 . Retrieved from MITRE ATT&CK: https://attack.mitre.org/groups/G0046/
ATT&CK, M. (2017, May 31). Lazarus Group . Retrieved from MITRE ATT&CK: https://attack.mitre.org/groups/G0032/
ATT&CK, M. (2017, May 31). ALLANITE. Retrieved from MITRE ATT&CK: https://attack.mitre.org/groups/G1000/
ATT&CK, M. (2017, May 24). Dragonfly. Retrieved from MITRE ATT&CK: https://attack.mitre.org/groups/G0035/
ATT&CK, M. (2017, May 31). FIN6. Retrieved from MITRE ATT&CK: https://attack.mitre.org/groups/G0037/
ATT&CK, M. (2017, December 14). OilRig. Retrieved from MITRE ATT&CK: https://attack.mitre.org/groups/G0049/
ATT&CK, M. (2017, May 31). Sandworm Team. Retrieved from MITRE ATT&CK: https://attack.mitre.org/groups/G0034/
ATT&CK, M. (2018, October 18). HEXANE. Retrieved from MITRE ATT&CK: https://attack.mitre.org/groups/G1001/
ATT&CK, M. (2019, January 2019). APT38 . Retrieved from MITRE ATT&CK: https://attack.mitre.org/groups/G0082/
ATT&CK, M. (2019, April 16). TEMP.Veles. Retrieved from MITRE ATT&CK: https://attack.mitre.org/groups/G0088/
ATT&CK, M. (2020, September 22). GOLD SOUTHFIELD. Retrieved from MITRE ATT&CK: https://attack.mitre.org/groups/G0115/
ATT&CK, M. (2020, May 12). Wizard Spider. Retrieved from MITRE ATT&CK: https://attack.mitre.org/groups/G0102/
Baezner, M., & Robin, P. (2017). Hotspot Analysis: Stuxnet. Center for Security Studies (CSS). Zürich: Center for Security Studies (CSS), ETH Zürich.
Bailey, D., & Wright, E. (2003). Practical SCADA for Industry. n/a: Newnes.
CISA. (2019, October). Abstract: ICS Cyber Incident Response Plan RP. Retrieved from CISA.gov: https://www.cisa.gov/uscert/ics/Abstract-ICS-Cyber-Incident-Response-Plan-RP
Curtis, K. (2005). DNP3 Primer Rev A. DNP. Retrieved 7 2022, from https://www.dnp.org/Portals/0/AboutUs/DNP3%20Primer%20Rev%20A.pdf
Greenberg, A. (2018, July 25). The Untold Story of NotPetya, the Most Devastating Cyberattack in History. Retrieved from Wired: https://www.wired.com/story/notpetya-cyberattack-ukraine-russia-code-crashed-the-world/
Greenfield, D. (2020, May 12). Is the Purdue Model Still Relevant? Retrieved from Automation World: https://www.automationworld.com/factory/iiot/article/21132891/is-the-purdue-model-still-relevant
Langner. (2021, April 23). What is OT/ICS configuration management, and how does it benefit engineers, admins, and auditors? Retrieved from OT-BASE by Langner: https://www.langner.com/2018/10/what-is-ot-ics-configuration-management/
MITRE ATT&CK. (2018, April 18). APT33. Retrieved from MITRE ATT&CK: https://attack.mitre.org/groups/G0064/
Mitsubishi Electric. (2009). FX1S FX1N FX2N(C) FX3U Beginner's Manual. Mitsubishi Electric.
Nagorny, K., Colombo, A., & Schmidtmann, U. (2012, November). A service- and multi-agent-oriented manufacturing automation architecture: An IEC 62264 level 2 compliant implementation. Computers in Industry, 63(8), 813-823. doi:10.1016/j.compind.2012.08.003
New York MTA. (2020). Subway and bus ridership for 2020. Retrieved from MTA: https://new.mta.info/agency/new-york-city-transit/subway-bus-ridership-2020
NIST. (2015, May). Guide to Industrial Control Systems (ICS) Security - NIST. Retrieved from csrc.nist.gov: https://csrc.nist.gov/publications/detail/sp/800-82/rev-2/final
Romanov, V. (2020). Blog. Retrieved 2021, from solisplc.com: https://www.solisplc.com/blog/plc-programming-languages
SANS. (2022, June 20). SANS ICS. Retrieved from SANS Institute: https://www.sans.org/blog/top-5-ics-incident-response-tabletops-and-how-to-run-them/
Tenable. (2022, March 3). Solution Overview: Industrial Cybersecurity for OT Environments. Retrieved from Tenable: https://www.tenable.com/solution-briefs/industrial-cybersecurity-for-ot-environments
The Port Of Los Angeles. (2022). Container Statistics. Retrieved from portoflosangeles: https://www.portoflosangeles.org/business/statistics/container-statistics
Virsec. (2019). Getting Ahead of the Triton ICS Attack. Retrieved from https://cdn2.hubspot.net/hubfs/1850012/Virsec_triton_ics.pdf


