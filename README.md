# Detection Engineering Lab

Detection Engineering lab built using the ELK Stack and Sigma rules to detect credential access activity on Linux systems.

## Project Overview

This project demonstrates how to build a basic Detection-as-Code pipeline using the ELK Stack. Logs are collected from a Linux system, shipped to Elasticsearch using Filebeat, and analyzed in Kibana where a detection rule identifies a simulated credential access attack.

The goal of this lab is to demonstrate how security detections can be engineered, tested, and validated in a controlled environment.

## Technologies Used

ELK Stack (Elasticsearch, Logstash, Kibana)
Filebeat
Docker
Sigma Rules
Lucene Queries

## Attack Simulation

The lab simulates a credential access attack on a Linux system. Logs generated from the attack are collected and analyzed by the detection pipeline.

Technique mapped to the MITRE ATT&CK framework:

Credential Dumping (T1003)

## Detection Logic

A Sigma rule was used to describe the detection logic.  
The rule was converted into a Lucene query and deployed as a detection rule inside Kibana.

When the simulated attack was executed, the rule successfully detected the activity.

Result:

Detection Rule Status: Enabled  
Execution Result: Success  
Success Rate: 100%

## Architecture

Linux System → Filebeat → Elasticsearch → Kibana Detection Rule

## Screenshots

Screenshots showing the working detection rule and alert results are located in the `screenshots` folder.

Examples include:

Kibana detection rule configuration  
Alert triggered in Kibana  
ELK stack running in Docker  
Log evidence of the simulated attack

## Learning Objectives

Build a functional Detection Engineering lab  
Understand how Sigma rules can be used for detection logic  
Learn how logs are ingested and analyzed in ELK  
Simulate attacks and validate detection rules

## Future Improvements

Automate Sigma-to-ELK rule conversion  
Add more attack simulations from the MITRE ATT&CK framework  
Integrate alerting and automated response

## Author

Omar Fattouh  
Cybersecurity Engineer
