![image](https://github.com/user-attachments/assets/f8541d3c-a72e-4996-94a2-89011f953d3b)



![image](https://github.com/user-attachments/assets/60829de6-533f-4c36-967a-73f7ff9c6bc7)

![image](https://github.com/user-attachments/assets/69604d12-89b9-4385-b4ec-e1658cd8a43f)


![image](https://github.com/user-attachments/assets/a33c2ef4-2467-41a6-915b-8fbbe5cf581d)


![image](https://github.com/user-attachments/assets/115a146d-2fe2-4e38-94e3-40d34272223a)

![image](https://github.com/user-attachments/assets/f68a6708-eb8a-4f47-8960-1c78fefaf069)


![image](https://github.com/user-attachments/assets/a93da6a9-2b36-49af-a252-a199231c80e0)


![image](https://github.com/user-attachments/assets/e806d796-96d2-4e10-8c69-268dc9113e8a)


![image](https://github.com/user-attachments/assets/eb293841-81f5-45bd-aa04-65d7ddef75d5)


![image](https://github.com/user-attachments/assets/f5376744-0aa6-46c7-9cd5-114bbe0aa36d)


<img width="1250" alt="Screenshot 2025-06-11 200640" src="https://github.com/user-attachments/assets/335151e5-97d0-4f8b-98e7-aa33f5a92ce4" />


![image](https://github.com/user-attachments/assets/dcc8af07-2960-4d5a-939a-8533461b4f08)


![image](https://github.com/user-attachments/assets/8cb74516-252b-4a8c-aaae-303b37367968)

![image](https://github.com/user-attachments/assets/774cd2fd-e65d-44b6-a707-1dfad8124639)


Incident Summary

One virtual machine, `win-vm-mde`, was targeted by repeated brute force login attempts originating from four different IP addresses. Notably, as the alert was generated, the most recent threat actor was actively attempting to log in via brute force, triggering the alert concurrently with the incident creation. This timing likely explains why the accompanying graphic displays only one malicious IP address instead of all four.

Details of failed login attempts:
![image](https://github.com/user-attachments/assets/a24b208d-a19e-4cdb-aa4b-5dd551b5fcd0)



A subsequent query was executed to verify if any of these malicious IP addresses successfully logged in. No successful logons were detected from any of the identified IPs.

![image](https://github.com/user-attachments/assets/02b84c34-c5a8-4f09-97c9-cd8b4f74f16c)


Containment Actions
- The affected VM was isolated using Microsoft Defender for Endpoint (MDE).
- A full antimalware scan was performed on the VM through MDE.
- Network Security Group (NSG) rules were tightened to block Remote Desktop Protocol (RDP) access from the public internet, allowing connections only from approved IP addresses.
- A corporate policy has been proposed to enforce this NSG lockdown for all virtual machines moving forward.

<img width="1547" alt="Screenshot 2025-06-11 210357" src="https://github.com/user-attachments/assets/973f0fd2-e37c-416a-bffd-bc3981ccf6fa" />


Closure
It is classified as a True Positive - Suspicious Activity. Brute force attempt occurred but was unsuccessful. 






