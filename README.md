# Integration Portfolio Projects

This repository contains a collection of enterprise integration projects showcasing various Oracle Integration Cloud (OIC) and SOA implementation patterns. Each project demonstrates different integration approaches, technologies, and solutions to common enterprise challenges.

## [ChatWithERP: AI-Powered Email to HCM Cloud Integration](https://github.com/amitguptaforwork/integration_portfolio_projects/blob/main/OIC_ChatWithERP_Email_OIC_HCMCloud_GenAI/README.md)

This innovative project implements a seamless workflow that allows users to access HCM Cloud data through natural language email requests. The solution leverages Oracle Integration Cloud (OIC) with an Email Adapter to monitor a dedicated inbox, integrates with Open AI to extract intent and parameters from unstructured emails, and then executes the appropriate HCM Cloud operations through REST APIs. By transforming complex HCM Cloud operations into conversational email exchanges, this project overcomes the challenge of bridging natural language with structured system operations, creating a more intuitive user experience without requiring expertise in the HCM Cloud interface.

## [Data Digitalization: SFTP to REST API Integration](https://github.com/amitguptaforwork/integration_portfolio_projects/blob/main/OIC_DataDigitalization_SFTP_OIC_RESTApi/README.md)

This project demonstrates a robust data digitalization solution that transforms traditional file-based processes into API-based operations. Using Oracle Integration Cloud (OIC), the implementation establishes an automated pipeline that monitors SFTP locations for incoming CSV files, processes them through a efficient framework, and ultimately submits the data to a RESTful API endpoint. This solution elegantly addresses the challenge of having large number of files delivered efficiently to the Target by clubbing multiple files' data into a single message, thereby avoiding the Chatty conversation anti-pattern

## [HCM Data Processing Flow: Automated File Handling for Oracle Fusion HCM](https://github.com/amitguptaforwork/integration_portfolio_projects/blob/main/OIC_HCMDataProcessingFlow_SFTP_OIC_FBDI_SFTP/README.md)

This enterprise-grade integration streamlines the complex process of getting employee data into Oracle Fusion HCM Cloud using Fusion's File-Based Data Import (FBDI) framework. Built on Oracle Integration Cloud (OIC), the solution monitors SFTP locations for incoming data files, and orchestrates the entire lifecycle of data ingestion into HCM Cloud. 

## [Three-Layer File Transfer System with Monitoring, Resubmission, and Guaranteed Delivery](https://github.com/amitguptaforwork/integration_portfolio_projects/blob/main/SOA_3LayerFileTransferSystemWithMonitoringResubmissionGuaranteedDelivery/README.md)

This advanced SOA-based implementation offers a highly reliable file transfer system designed for mission-critical enterprise environments. The architecture features three distinct layers—transport, processing, and business—that work together to provide comprehensive capabilities including guaranteed message delivery, robust error handling, and automated resubmission mechanisms. Built using Oracle SOA Suite, the system leverages Oracle Database for reliability, implements custom Java for PGP encryption and decryption, and provides a sophisticated monitoring dashboard built on Oracle ADF for operational visibility.  This project demonstrates how to overcome the challenges of building a fault-tolerant file transfer system that offers exceptional visibility for smooth support operations