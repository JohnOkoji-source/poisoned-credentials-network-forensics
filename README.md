# Poisoned Credentials: Network Forensics Investigation

## Overview

This project documents a network forensics investigation into suspicious network activity involving credential poisoning.

Using Wireshark and captured network traffic, the investigation focused on identifying evidence associated with LLMNR/NBT-NS poisoning, examining affected systems, tracing credential exposure, and analyzing related SMB network activity.

The project demonstrates how packet-level evidence can be used to reconstruct suspicious activity and develop findings during a network security investigation.

> **Note:** This investigation was performed in a controlled academic environment using provided network capture evidence.

## Tools and Technologies

- Wireshark
- PCAP Analysis
- LLMNR
- NBT-NS
- SMB
- TCP/IP
- Network Forensics
- Packet Analysis

## Investigation Objectives

- Analyze captured network traffic using Wireshark
- Identify suspicious LLMNR and NBT-NS activity
- Determine systems involved in the suspicious traffic
- Investigate evidence of credential exposure
- Examine SMB-related network activity
- Correlate packet evidence to reconstruct the incident
- Document findings from the investigation

## Investigation Process

### 1. Evidence Review

The investigation began by examining the provided packet capture in Wireshark.

Network traffic was reviewed and filtered to identify protocols and communication patterns relevant to the suspected credential-poisoning activity.

### 2. LLMNR/NBT-NS Analysis

Traffic associated with LLMNR and NBT-NS was examined for evidence of name-resolution poisoning.

These protocols can become relevant during an investigation when a system attempts to resolve a hostname and another device responds to the request.

The captured traffic was analyzed to determine which systems participated in the suspicious name-resolution activity.

### 3. Identification of Involved Systems

Packet evidence was correlated using network identifiers such as IP addresses and communication patterns.

This helped distinguish the system generating the name-resolution request from the system responding to it and supported identification of the hosts involved in the incident.

### 4. Credential Exposure Investigation

The investigation continued by examining authentication-related network evidence associated with the suspicious activity.

Relevant packets were analyzed to determine whether credential information had been exposed as part of the poisoning activity and to identify the account associated with the observed authentication attempt.

### 5. SMB Traffic Analysis

SMB-related traffic was examined to understand activity occurring after the suspicious name-resolution exchange.

Analyzing this traffic provided additional context about communications between the involved systems and helped reconstruct the sequence of events.

### 6. Evidence Correlation

Findings from the LLMNR/NBT-NS, authentication, and SMB traffic were correlated to develop a clearer picture of the incident.

Rather than relying on a single packet, multiple pieces of network evidence were used to understand how the suspicious activity progressed.

## Skills Demonstrated

- Network Forensics
- Wireshark Packet Analysis
- PCAP Investigation
- LLMNR/NBT-NS Analysis
- Credential Exposure Investigation
- SMB Traffic Analysis
- Network Protocol Analysis
- Evidence Correlation
- Incident Investigation
- Technical Documentation

## Defensive Recommendations

Based on the attack pattern investigated in this project, defensive considerations include:

- Reducing reliance on unnecessary legacy name-resolution protocols
- Monitoring for abnormal LLMNR and NBT-NS responses
- Monitoring authentication activity for suspicious credential usage
- Restricting unnecessary SMB communication
- Applying network segmentation where appropriate
- Investigating unusual internal name-resolution and authentication traffic

## Key Takeaway

This project strengthened my understanding of how network packet evidence can be used during a cybersecurity investigation.

By examining name-resolution traffic, authentication activity, affected systems, and SMB communications, I was able to correlate multiple pieces of evidence and reconstruct suspicious activity from a network-forensics perspective.

The exercise reinforced the importance of understanding normal network protocols because legitimate functionality can sometimes be abused during credential-based attacks.
