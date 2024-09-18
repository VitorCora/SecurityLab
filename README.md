# SecurityLab
This repo is intended to help you deploy your own Security testing lab

This lab is composed of 2 vulnerable instances (DVWA and PyGoat) and 2 Trend Micro security systems (Trend Vision One Network Sensor and Trend Network Security)

The lab topology is as follows:

![image](https://github.com/user-attachments/assets/2e5155e1-c5dd-4e96-a85f-276ccc8668ae)


DVWA Data Flow:

![image](https://github.com/user-attachments/assets/06e96e8c-1d6b-4d56-8c1b-66d9eef43c0e)

All incoming traffic will be send from the Igw to the VPC Endpoint (Trend Network Security), this traffic will be inspected and cleaned by Trend Network Security, this traffic will then be routed to the DVWA instance carring a public IP

A copy of All traffic recieved and sent by the DVWA Instance will be send to the Trend Vision One Network Sensor for deep inspection and visibility over lateral moviment.

Pygoat Data Flow:

![image](https://github.com/user-attachments/assets/cd89b41b-b9b9-4a51-afee-a732ed321562)

All incoming traffic will be send from the Igw to the VPC Endpoint (Trend Network Security), this traffic will be inspected and cleaned by Trend Network Security, this traffic will then be routed to the PyGoat instance carring a public IP


