# Email Authentication Lab – Postfix, OpenDKIM and DNS Configuration

## Overview

This project demonstrates the deployment and configuration of a Linux-based email authentication environment using Postfix and OpenDKIM on Ubuntu 24.04 LTS hosted on a Kamatera VPS.

The goal of the project was to gain hands-on experience with email infrastructure, SMTP services, DNS-based authentication, and Linux server administration by configuring DKIM signing for outbound email.

## Objectives

- Deploy a cloud-hosted Linux server
- Configure a working SMTP service using Postfix
- Implement DKIM email signing with OpenDKIM
- Configure DNS records required for email authentication
- Validate authenticated outbound email delivery
- Document the configuration and deployment process

## Architecture

     +----------------+
     | Email Sender   |
     +--------+-------+ 
              |          
              v
     +----------------+
     | Postfix SMTP   |
     | Ubuntu 24.04   |
     +--------+-------+
              |          
              v 
     +----------------+
     | OpenDKIM       |
     | Message Signing|
     +--------+-------+         
              |          
              v
     +----------------+
     | DNS Records    |
     | DKIM Public Key|
     +--------+-------+         
              |         
              v
     +----------------+
     | Recipient Mail |
     | Server         |
     +----------------+ 

## Technologies Used

- Ubuntu 24.04 LTS
- Postfix
- OpenDKIM
- DNS
- SMTP
- SSH
- Git
- GitHub
- Kamatera VPS

## Configuration Highlights

### Postfix

Configured Postfix as the SMTP service responsible for handling outbound email delivery.

Key areas configured:

- SMTP service configuration
- Network settings
- Hostname configuration
- Mail routing
- OpenDKIM integration

### OpenDKIM

Configured OpenDKIM to digitally sign outbound email messages.

Implemented:

- DKIM key generation
- KeyTable configuration
- SigningTable configuration
- TrustedHosts configuration
- Postfix milter integration

### DNS Authentication

Published DKIM DNS records to allow recipient mail servers to verify message authenticity.

Implemented:

- DKIM public key record
- Domain authentication configuration

## Repository Structure

     postfix-opendkim-mail-server/
     │
     ├── README.md
     ├── .gitignore
     │
     ├── postfix/
     │   ├── main.cf
     │   └── master.cf
     │
     ├── opendkim/
     │   ├── key.table
     │   ├── signing.table
     │   ├── trusted.hosts
     │   └── tiko.txt
     │
     └── screenshots/
          ├── gmail-authentication-results.png
          └── easydmarc-email-investigation.png

## Skills Demonstrated

- Linux Administration
- Email Infrastructure
- SMTP Configuration
- DNS Management
- DKIM Authentication
- SSH Server Management
- Git Version Control
- Technical Documentation
- Troubleshooting and Validation

## Outcome

Successfully deployed and configured a mail server environment capable of DKIM-signing outbound email messages.

The project provided practical experience with email authentication technologies, DNS configuration, Linux system administration, and secure mail infrastructure deployment.
