# OIC Project: HCM Data Loader Integration

This Oracle Integration Cloud (OIC) project automates a multi-step data handling process involving ZIP file ingestion, UCM upload, HCM Data Loader invocation, and final report distribution via MFT (GoAnywhere). Below is an overview of the process and Mermaid diagrams to visualize the architecture and flow.

---

## 📦 High-Level Flow

```mermaid
flowchart TD
    A[User uploads ZIP to OIC File Server] --> B[OIC Integration triggered]
    B --> C[Copy ZIP and Upload to UCM]
    C --> D[Trigger HCM Data Loader Process]
    D --> E[Wait for HCM processing to complete]
    E --> F[Download CSV report from Oracle HCM]
    F --> G[Write report to SFTP server]
    G --> H[GoAnywhere MFT picks up file]
    H --> I[Send secure email with a link to the file to distribution lists]
```

---

## 🧭 Sequence Diagram

```mermaid
sequenceDiagram
    participant User
    participant OIC
    participant UCM
    participant HCM
    participant SFTP
    participant GoAnywhere

    User->>OIC: Upload ZIP to File Server
    OIC->>OIC: Trigger Integration on File Arrival
    OIC->>UCM: Upload file
    OIC->>HCM: Trigger HCM Data Loader Job
    OIC-->>OIC: Wait for processing (sleep/polling)
    OIC->>HCM: Check job status
    HCM-->>OIC: Job Status
    OIC->>HCM: Download Report
    HCM-->>OIC: Return CSV report
    OIC->>SFTP: Write report file
    GoAnywhere->>SFTP: Pick up report
    GoAnywhere->>Distribution List: Send secure email which has link to file
```

---

## 📂 Components

- **OIC File Server**: Receives incoming ZIP files via SFTP.
- **OIC Integration Flow**:
  - Unzips file and uploads to **UCM**.
  - Triggers **HCM Data Loader** process.
  - Waits/polls for the process to complete.
  - Downloads a **CSV report**.
  - Uploads the report to an **external SFTP server**.
- **GoAnywhere MFT**:
  - Monitors SFTP server.
  - Picks up report and distributes **secure download links** to a list of recipients.

---

## ⚙️ Technologies Used

- Oracle Integration Cloud (OIC)
- Oracle File Server (SFTP)
- Oracle UCM (Universal Content Management)
- Oracle HCM Cloud (HCM Data Loader)
- External SFTP Server
- GoAnywhere MFT

---

## 🛡️ Security Considerations

- All file transfers use **SFTP** for encrypted transit.
- Distribution is done via **secure Email functionality** by GoAnywhere.  This is the main reason to use GoAnywhere MFT, as OIC lacks this feature.
- Credentials and connections are stored in OIC using encrypted keys.

---

## 📌 Notes

- Ensure proper retry logic in the OIC integration for UCM upload and HCM job polling.
- In case of errors due to data import, responsibility of the Integration team is to notify the business team via email.  They are responsible for resubmitting the files with corrected data.
- Monitor GoAnywhere job completion for auditability.  GoAnywhere provides comprehensive dashboard for monitoring file delivery

---
