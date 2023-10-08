# Configuring VLAN "OfficeExpansion" (VLAN ID: 20) on Cisco Switch

## Introduction
In this guide, we'll outline the steps taken to create a Virtual Local Area Network (VLAN) named "OfficeExpansion" with VLAN ID 20 on a Cisco switch using Cisco Packet Tracer.

## Step-by-Step Instructions

### 1. Accessing the Switch
   - Access the switch's command-line interface by typing the following commands:
     ```
     Switch> en
     Switch# show vlan brief
     ```

### 2. Creating VLAN "OfficeExpansion" (VLAN ID: 20)
   - Enter the global configuration mode by typing:
     ```
     Switch# configure terminal
     ```
   - Create VLAN 20 and name it "OfficeExpansion":
     ```
     Switch(config)# vlan 20
     Switch(config-vlan)# name OfficeExpansion
     Switch(config-vlan)# exit
     ```

### 3. Assigning Ports to VLAN
   - Configure a port (e.g., Fa0/10) to be part of VLAN 20:
     ```
     Switch(config)# interface FastEthernet0/10
     Switch(config-if)# switchport mode access
     Switch(config-if)# switchport access vlan 20
     Switch(config-if)# exit
     ```

### 4. Verifying VLAN Configuration
   - Verify the VLAN configuration using the following command:
     ```
     Switch# show vlan brief
     ```


## Video Tutorial
You can watch a video tutorial demonstrating these steps on Google Drive: [VLAN Configuration Video](https://drive.google.com/file/d/1NBB5NyrzDjEP8BchdA1EqDia1gm0NhZn/view?usp=sharing)

## Rationale
Creating VLAN "OfficeExpansion" isolates the network traffic for the expanded office area, enhancing security and traffic management. This segmentation reduces the risk of unauthorized access and improves network performance.

