# Hybrid Windows Enterprise IT Lab

## Overview

This project documents a virtualized Windows enterprise environment built to simulate common IT support and systems administration tasks in an Active Directory and hybrid Microsoft Entra ID environment.

The lab includes a Windows Server domain controller and Windows 11 domain-joined workstation configured for centralized identity management, Group Policy, DNS, file sharing, access control, and hybrid identity synchronization.

On-premises Active Directory identities are synchronized to Microsoft Entra ID using Microsoft Entra Cloud Sync with password hash synchronization and OU-based provisioning.

## Environment

- Windows Server
- Windows 11 domain-joined workstation
- Active Directory Domain Services (AD DS)
- DNS
- Group Policy
- SMB file sharing
- NTFS and share permissions
- Microsoft Entra ID
- Microsoft Entra Cloud Sync
- Password Hash Synchronization

## Architecture

The environment uses a Windows Server domain controller to provide Active Directory and DNS services to a Windows 11 domain-joined workstation. Active Directory identities are synchronized to Microsoft Entra ID through the Microsoft Entra provisioning agent.

## Implementation

### Active Directory and DNS

- Created and configured the `mendoza.local` Active Directory domain.
- Joined a Windows 11 workstation to the domain.
- Created and administered organizational units, users, and security groups.
- Configured DNS to support domain authentication and resource discovery.

### Group Policy and Account Management

- Created and applied Group Policy Objects to domain users and computers.
- Configured domain account and lockout policies.
- Tested policy application and domain authentication from the Windows 11 client.
- Used Event Viewer and Windows administrative tools to investigate authentication and policy behavior.

### File Services and Permissions

- Created SMB network shares hosted within the domain environment.
- Configured NTFS and share permissions.
- Assigned access through Active Directory security groups.
- Tested authorized and unauthorized access from the domain-joined workstation to validate least-privilege permissions.

### Microsoft Entra Hybrid Identity

- Integrated on-premises Active Directory with Microsoft Entra ID.
- Installed and configured the Microsoft Entra provisioning agent.
- Configured Microsoft Entra Cloud Sync for the `mendoza.local` domain.
- Scoped synchronization using organizational units.
- Enabled password hash synchronization.
- Verified automatic provisioning of Active Directory users into Microsoft Entra ID.
- Validated synchronization by modifying on-premises identity attributes and confirming the changes propagated to Microsoft Entra ID.

## Troubleshooting

During implementation, I diagnosed issues involving domain authentication, Group Policy application, file permissions, and Microsoft Entra Cloud Sync.

Cloud Sync troubleshooting included reviewing provisioning logs, verifying provisioning-agent service status, investigating provisioning quarantine, validating synchronization scope, and confirming successful communication between the on-premises environment and Microsoft Entra ID.

## Skills Demonstrated

Active Directory Administration • Windows Server • Group Policy • DNS • Identity and Access Management • User and Group Administration • SMB • NTFS Permissions • Least-Privilege Access • Windows Troubleshooting • Event Viewer • Microsoft Entra ID • Microsoft Entra Cloud Sync • Hybrid Identity • Password Hash Synchronization
