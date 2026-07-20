# Incident INC-001: Network Connectivity Failure

## User Report

The server cannot access the network.

The user reports that the machine cannot reach external resources.

## Environment

- Operating System: Linux
- Number of machines: 1
- Network interface: enp0s3
- Network manager: [NetworkManager/systemd-networkd/etc.]

## Symptoms

- Network connectivity unavailable
- External hosts cannot be reached

## Objective

Determine the root cause of the connectivity failure and restore network connectivity.

## Restrictions

Use only the following tools:

- ip
- ping
- ip neigh
- nmcli
- tcpdump

## Investigation
ip -br link
ip -br addr
ip route
ip neigh 

<img width="582" height="141" alt="net 01" src="https://github.com/user-attachments/assets/56e2113c-e5f4-4b62-b362-35dccada0ac9" />


## Root Cause

-The network interface was administratively down.

## Resolution

-The interface was brought back up.

ip link set enp0s3 up 

## Verification

<img width="788" height="445" alt="net 02" src="https://github.com/user-attachments/assets/8a48f838-fd9d-4749-82e2-8c0ce47ae93c" />
