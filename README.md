# Azure-recovery-overview
Get insights in recovery and immutability options per Azure service. This repository contains an Excel file that provides insights into how you can backup an Azure service, achieve immutability, and perform cross-region restores, including non-paired regions, cross-subscription, or same subscription recovery. This information is intended to help consumers to configure their Azure services to comply with their requirments by understanding the backup capabilities of various Azure services.

Backup and immutability are a shared responsibility between the cloud provider and the cloud service consumer. The cloud provider offers the backup and recovery capabilities, while the consumer is responsible for configuring, validating, and testing these capabilities to ensure they meet their requirements.

## Azure Backup
The Excel file details the backup capabilities of different Azure services, including whether they store consumer data, have backup features, and can achieve immutability. It also covers various recovery scenarios such as same subscription recovery, cross-subscription recovery, paired region recovery, and non-paired region recovery.

## Azure immutability
Immutability is a critical feature for protecting against malicious deletion or configuration changes. The file provides information on whether immutability can be achieved for each Azure service and the maximum data retention period.

## Legenda

There is a lot of data collected in the sheet, the legenda gives an explenation of the different colums. 

![image](https://github.com/user-attachments/assets/8adb3a90-4792-457f-a470-d6e4a76604c0)


## Best effort - disclaimer
This information is provided on a best-effort basis and may not be complete or accurate over time. No rights, statements, or commitments can be derived from the information provided. Please contribute to keep this information up to date.

## Feedback
We welcome your feedback and suggestions! Please submit any issues or feature requests through Issues or discussions.

## Questions and remarks:

Please submit an issue if you find things for improvement or things are not correct.

## changes
1.2 splitted azure files recovery in multiple components (account, share, file)
1.1 added non paired cross region recovery
1.0 initial document
