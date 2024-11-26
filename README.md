# Azure-recovery-overview

Backup and immutability are shared responsibilities between the cloud provider and the cloud service consumer. The cloud provider offers backup and recovery capabilities, while the consumer is responsible for configuring, validating, and testing these capabilities to ensure they meet their needs. 

Backup & Recovery orchestration tools like [Azure Backup](https://learn.microsoft.com/en-us/azure/backup/backup-overview) hide a lot of complexity offers a lot of capabilities covering multiple scenarios: **cross-region restores**, including non-paired regions, **cross-subscription**, or **same-subscription recovery**, especially when running on IaaS services and to a certain extent on PaaS services. When it comes to modern distributed workloads, they require nuanced backup strategies. Consider this workload: A containerized app running on Azure Container Apps with persistent storage in CosmosDB. To successfully restore this app, We need the backup of 

 - **Persistentengt Data**: in Cosmos DB. Backing up this data ensures the recovery of critical customer information or stateful application behaviour.
 - **Configuration Metadata**: Recovery also depends on preserving deployment pipelines (e.g., container image hashes) and application configurations. Without this metadata, recovery risks partial or failed restores.

In addition to that, Due to technological implications, the capabilities can vary per Azure service. For instance, the recovery process for CosmosDB differs from that of Azure SQL DB.

## How does this repo help?

This initiative addresses the lack of a centralized Azure documentation resource for backup and recovery capabilities across services. Recognizing the value of such an overview, we collaborated with multiple customers seeking to validate compliance with regulatory standards like [DORA](https://www.eiopa.europa.eu/digital-operational-resilience-act-dora_en) and [NIST 2](https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.pdf).

This repository presents an Azure Service vs. Backup Capability matrix, offering clear insights on backing up Azure services, ensuring immutability, and implementing effective recovery orchestration. It empowers Azure service consumers to make informed decisions by highlighting the backup and immutability features across various Azure services, enabling optimal service configuration to meet specific requirements. By sharing this resource, we aim to empower stakeholders to navigate these requirements. As Azure evolves, we’ve ensured this effort reflects a best-effort interpretation of the most current Azure documentation.


## Azure Backup
The Excel file details the backup capabilities of different Azure services, including whether they store consumer data, have backup features, and can achieve immutability. It also covers various recovery scenarios such as same subscription recovery, cross-subscription recovery, paired region recovery, and non-paired region recovery.

## Azure immutability
Immutability is a critical feature for protecting against malicious deletion or configuration changes. The file provides information on whether immutability can be achieved for each Azure service and the maximum data retention period.

## Legenda

The sheet collates data from multiple sources; the legend explains the different columns. 

![image](https://github.com/user-attachments/assets/8adb3a90-4792-457f-a470-d6e4a76604c0)


## Best effort - disclaimer
This information is provided on a best-effort basis and may not be complete or accurate. No rights, statements, or commitments can be derived from the information provided. Please contribute to keep this information up to date.

## Feedback
We welcome your feedback and suggestions! Please submit any issues or feature requests through Issues or discussions.

## Changelog
1.2 splitted azure files recovery in multiple components (account, share, file)
1.1 added non paired cross region recovery
1.0 initial document

## Contributors
[Jochen van Wylick](https://www.linkedin.com/in/jochen-van-wylick-26209325/?originalSubdomain=nl).
[Naveen Kumar Selvaraj](https://www.linkedin.com/in/selvarajnaveenkumar/).
[Nikita Dandwani](https://www.linkedin.com/in/nikita-dandwani-3680b856/).
[Dylan de Jong](https://www.linkedin.com/in/dylandejong/).

