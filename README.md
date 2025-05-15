# Integration Portfolio Projects

This repository contains a collection of enterprise integration projects showcasing various Oracle Integration Cloud (OIC) and SOA implementation patterns. Each project demonstrates different integration approaches, technologies, and solutions to common enterprise challenges.

## [ChatWithERP: AI-Powered Email to HCM Cloud Integration](https://github.com/amitguptaforwork/integration_portfolio_projects/blob/main/OIC_ChatWithERP_Email_OIC_HCMCloud_GenAI/README.md)
**OIC | Javascript | OCI Generative AI using Cohere LLM**

Vendors regularly reach out to our organization's customer care regarding status of their invoice. In order to automate resolution of such queries, a innovative AI based system was proposed to be developed.  The project has been initially developed as a Agentic AI system that can answer vendor queries via emails.  Vendors can send in their invoice related queries on email, and the system replies back to them.  The USP of the solution is, vendors can send their query in normal english (also called as 'Natural Language').  The solution leverages Oracle Integration Cloud (OIC) with an Email Adapter to monitor a dedicated inbox, integrates with LLM (OCI Generative AI using Cohere LLM) to extract intent and parameters from email's natural language query, and then executes the appropriate Oracle Cloud operations through REST APIs. It then responds to the user via email with a natural language sounding response.

## [Data Digitalization: SFTP to REST API Integration](https://github.com/amitguptaforwork/integration_portfolio_projects/blob/main/OIC_DataDigitalization_SFTP_OIC_RESTApi/README.md)
**OIC | REST**

This project demonstrates a robust data digitalization solution that transforms traditional file-based processes into API-based operations. Using Oracle Integration Cloud (OIC), the implementation establishes an automated pipeline that monitors SFTP locations for incoming CSV files, processes them through a efficient framework, and ultimately submits the data to a RESTful API endpoint. This solution elegantly addresses the challenge of having large number of files delivered efficiently to the Target by clubbing multiple files' data into a single message, thereby avoiding the Chatty conversation anti-pattern

## [HCM Data Processing Flow: Automated File Handling for Oracle Fusion HCM](https://github.com/amitguptaforwork/integration_portfolio_projects/blob/main/OIC_HCMDataProcessingFlow_SFTP_OIC_FBDI_SFTP/README.md)
**OIC | HCM Cloud | GoAnywhere MFT**

This enterprise-grade integration streamlines the complex process of getting employee data into Oracle Fusion HCM Cloud using Fusion's File-Based Data Import (FBDI) framework. Built on Oracle Integration Cloud (OIC), the solution monitors SFTP locations for incoming data files, and orchestrates the entire lifecycle of data ingestion into HCM Cloud. 

## [Three-Layer File Transfer System with Monitoring, Resubmission, and Guaranteed Delivery](https://github.com/amitguptaforwork/integration_portfolio_projects/blob/main/SOA_3LayerFileTransferSystemWithMonitoringResubmissionGuaranteedDelivery/README.md)
**SOA | ADF | Oracle DB | Java | Jenkins**

This advanced SOA-based implementation offers a highly reliable file transfer system designed for mission-critical enterprise environments. The architecture features three distinct layers—transport, processing, and business—that work together to provide comprehensive capabilities including guaranteed message delivery, robust error handling, and automated resubmission mechanisms. Built using Oracle SOA Suite, the system leverages Oracle Database for reliability, implements custom Java for PGP encryption and decryption, and provides a sophisticated monitoring dashboard built on Oracle ADF for operational visibility.  This project demonstrates how to overcome the challenges of building a fault-tolerant file transfer system that offers exceptional visibility for smooth support operations