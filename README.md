# Active Directory and SIEM Lab

## Objective

The Active Directory and SIEM Lab was designed to simulate a domain environment to monitor real-world attack scenarios and generate telemetry for security analysis. The project involved configuring Active Directory to manage user accounts, using Kali Linux for conducting brute-force attacks, integrating Splunk for centralized log ingestion and threat detection, and employing Atomic Red Team to emulate threats. 

### Skills Learned

- Configured Active Directory for user account provisioning
- Conducted brute-force attacks using Kali Linux to simulate an attack
- Configured Splunk to ingest and analyze security logs
- Utilized Atomic Red Team tests to emulate MITRE ATT&CK techniques
- Deep understanding of log sources and event types for threat detection

## Steps

To begin this lab, I created a logical diagram of the network that will host the Virtual Machines to better visualize the environment. I then set up Virtual Machines for the Active Directory Server, Splunk Server (Ubuntu), Windows 10 machine, and Kali Linux machine.
<img src="NetworkDiagram.PNG" alt="Network Diagram" width="350">

To ensure that the Splunk server can send logs, I created my own configuration named "inputs.conf" in the file: SplunkUniversalForwarder > etc > local > system. This will allow Splunk to send logs to an index I will created named "endpoint". I am also using sysmon-modular for easier maintenance and specific configs.


The Splunk Universal Forwarder on my Windows 10 machine is sending data to the Splunk server through port 9997 which I enabled.
<img src="SplunkIndex.PNG" alt="Splunk Index" width="350">



