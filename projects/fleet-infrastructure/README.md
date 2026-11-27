# Fleet IT Infrastructure Modernization

**Role:** Technical Lead / Head of IT  
**Period:** 2023–2026  
**Environment:** Distributed shore and expedition-vessel infrastructure  
**Status:** Implemented with ongoing lifecycle management  
**Focus:** Windows Server | Hyper-V | Microsoft 365 | Intune | Networking | Security

[← Return to main portfolio](../../README.md)

---

## Executive Summary

This case study describes the modernization, standardization, and lifecycle management of distributed IT infrastructure supporting maritime and shore-side operations.

A vessel operates like a remote office, datacenter, communications hub, and operational site combined into one mobile environment.

The technology estate may include:

- Physical servers
- Virtual servers
- Windows endpoints
- Active Directory
- Microsoft cloud services
- Local applications
- Network infrastructure
- Wireless services
- Firewalls
- Satellite WAN services
- Vendor-managed equipment
- Operational technology

The objective is to establish infrastructure that is secure, resilient, supportable, documented, and appropriate for remote operations.

---

## The Challenge

Maritime infrastructure presents several challenges that differ from conventional office IT.

### Geographic distribution

Each vessel may operate thousands of kilometres from shore-based support.

### Variable connectivity

Cloud access, remote management, software distribution, and support may be affected by satellite availability and bandwidth.

### Limited physical access

Hardware replacement and specialist intervention may depend on vessel schedules, ports, customs, and technician availability.

### Mixed technology lifecycles

Enterprise endpoints may be refreshed regularly, while specialist vessel systems can remain in service for much longer.

### Operational impact

Infrastructure changes can affect vessel administration, communications, user services, and operational systems.

### Documentation dependency

Accurate inventories and diagrams are essential because support may be provided remotely by people who cannot physically inspect the environment.

---

## My Role

My responsibilities included:

- Infrastructure architecture
- Server and virtualization management
- Network architecture
- Microsoft cloud administration
- Endpoint-management strategy
- Security coordination
- Hardware lifecycle planning
- Vendor coordination
- Technical documentation
- Asset inventory
- Remote support
- Technology transitions and handovers
- Operational standards
- Infrastructure troubleshooting
- Management and stakeholder communication

The role required both strategic planning and hands-on technical involvement.

---

## Infrastructure Objectives

The modernization approach focused on:

1. Improving infrastructure reliability.
2. Standardizing technology where practical.
3. Simplifying remote management.
4. Improving documentation.
5. Strengthening endpoint and network security.
6. Supporting vessel-to-shore integration.
7. Reducing unsupported or unmanaged technology.
8. Improving visibility of assets and dependencies.
9. Supporting controlled lifecycle replacement.
10. Making handovers and transitions more manageable.

---

## Reference Architecture

```text
                     CLOUD SERVICES
                          |
              +-----------+-----------+
              |                       |
        Microsoft 365             Business
        Cloud Services             Systems
              |                       |
              +-----------+-----------+
                          |
                     INTERNET
                          |
                  Multi-WAN Layer
                          |
                  Security Gateway
                          |
                     Core Network
                          |
          +---------------+---------------+
          |               |               |
      Server Layer    Corporate IT      Operational
          |               |               Systems
      Hyper-V          Endpoints             |
      Windows          Printers             OT
      Server            Wi-Fi             Systems
```

This is a conceptual reference architecture. It does not represent any specific vessel or organization.

---

## Compute Infrastructure

The compute environment includes combinations of:

- Physical server hardware
- Windows Server
- Hyper-V
- Virtual machines
- Active Directory
- File and print services
- Application services
- Backup infrastructure
- System-management tools

### Virtualization

Virtualization provides several potential benefits:

- Better hardware utilization
- Easier workload separation
- Simplified backup
- Faster recovery
- More consistent deployment
- Easier replacement of physical hosts
- Reduced hardware footprint

However, virtualization also creates dependencies.

The design must consider:

- Host failure
- Storage failure
- Backup integrity
- Recovery procedures
- Licensing
- Hardware compatibility
- Firmware lifecycle
- Monitoring
- Capacity
- Spare equipment

---

## Server Lifecycle Management

Server infrastructure requires a controlled lifecycle.

```text
Requirement
    |
    v
Design
    |
    v
Procurement
    |
    v
Configuration
    |
    v
Deployment
    |
    v
Operations
    |
    v
Maintenance
    |
    v
Replacement
    |
    v
Secure Decommissioning
```

Lifecycle planning includes:

- Hardware age
- Warranty status
- Operating-system support
- Firmware support
- Capacity
- Backup compatibility
- Spare availability
- Deployment windows
- Vessel schedule
- Data migration
- Decommissioning

---

## Microsoft Cloud Environment

Microsoft cloud services form an important part of the wider infrastructure.

Technology areas include:

- Microsoft 365
- Exchange Online
- Microsoft Teams
- SharePoint Online
- OneDrive
- Microsoft Intune
- Identity and access management
- Endpoint policy
- Application deployment
- Collaboration governance

### Conceptual model

```text
                     Microsoft 365
                          |
        +-----------------+-----------------+
        |                 |                 |
   Collaboration       Identity         Management
        |                 |                 |
      Teams            Identity          Intune
   SharePoint                            Endpoints
    OneDrive                              Policies
        |
 Exchange Online
```

The cloud platform must be integrated with vessel operations while considering:

- Variable connectivity
- Cloud authentication
- Offline access
- Data synchronization
- Device compliance
- Application deployment
- Bandwidth consumption
- User support
- Security
- Governance

---

## Endpoint Management

Endpoint management should provide consistency across distributed devices.

Areas include:

- Device enrolment
- Configuration policy
- Security policy
- Application deployment
- Patch management
- Antivirus or endpoint-security deployment
- Local administrator governance
- Inventory
- Compliance status
- Device retirement
- Secure data removal

### Desired lifecycle

```text
Procure
   |
   v
Register
   |
   v
Configure
   |
   v
Secure
   |
   v
Deploy
   |
   v
Monitor
   |
   v
Maintain
   |
   v
Retire
```

A maritime endpoint-management approach must account for devices that may have intermittent access to cloud services.

---

## Network Infrastructure

The network environment may include:

- Core switching
- Access switching
- Wireless networking
- Firewalls
- VLANs
- WAN services
- Satellite communications
- Local servers
- User networks
- Operational systems
- Vendor equipment
- Guest or crew services

### Conceptual segmentation

```text
                   WAN Services
                        |
                 Security Gateway
                        |
                    Core LAN
       +----------------+----------------+
       |                |                |
 Enterprise Services   OT          User Services
       |                |                |
 Servers            Operational      Endpoints
 Corporate           Systems         Wireless
 Endpoints
```

Network segmentation should support:

- Security boundaries
- Operational separation
- Traffic management
- Fault isolation
- Controlled vendor access
- Appropriate monitoring
- Easier troubleshooting
- Clear ownership

---

## Wireless Infrastructure

Wireless connectivity aboard vessels can be affected by:

- Steel construction
- Fire doors
- Deck layout
- Equipment rooms
- Passenger areas
- Crew areas
- Interference
- Access-point placement
- Cabling limitations
- Capacity requirements
- Roaming behavior

Wireless design should consider:

- Coverage
- Capacity
- Segmentation
- Authentication
- Management
- Guest access
- Crew access
- Corporate access
- Device density
- Operational areas

A strong signal alone does not guarantee a high-quality wireless experience. Capacity, interference, routing, WAN availability, and application behavior also matter.

---

## Security Controls

Infrastructure security includes several control layers.

### Identity

- Named accounts
- Role-based access
- Privileged-account management
- Account lifecycle
- Authentication
- Access review

### Endpoint

- Security agents
- Patch management
- Configuration policy
- Disk encryption where appropriate
- Application control
- Local administrator restrictions

### Network

- Segmentation
- Firewall policy
- Secure administration
- Controlled remote access
- Vendor-access restrictions
- Configuration management

### Cloud

- Identity protection
- Access governance
- Device management
- Collaboration governance
- Data protection
- Audit and monitoring

### Operations

- Change management
- Incident management
- Backup
- Recovery
- Documentation
- Vendor management

---

## Backup and Recovery

Backup is only useful when recovery is possible.

A recovery strategy should consider:

- Critical workloads
- Backup frequency
- Retention
- Local copies
- Offsite copies
- Cloud copies
- Connectivity limitations
- Encryption
- Access control
- Restoration testing
- Recovery time
- Recovery order
- Documentation

### Recovery model

```text
Incident
   |
   v
Impact Assessment
   |
   v
Containment
   |
   v
Recovery Decision
   |
   v
Restore Infrastructure
   |
   v
Restore Applications
   |
   v
Validate Data
   |
   v
Return to Service
```

Restoration testing is necessary because a successful backup job does not automatically prove that systems can be recovered.

---

## Monitoring and Support

Remote infrastructure requires visibility.

Monitoring areas may include:

- Server health
- Storage capacity
- Backup status
- Endpoint-security status
- WAN availability
- Network-device availability
- Critical services
- Certificate expiry
- Licensing
- Hardware alarms
- Environmental conditions where available

The support model should define:

- First-line responsibility
- Shore-side escalation
- Vendor escalation
- Incident severity
- Communication methods
- Out-of-hours escalation
- Documentation requirements
- Replacement procedures

---

## Documentation

Infrastructure documentation should include:

- Asset inventory
- Server inventory
- Virtual-machine inventory
- Network diagrams
- Switch documentation
- Service dependencies
- Vendor contacts
- Licensing
- Warranty information
- Backup information
- Recovery procedures
- Administrative ownership
- Change history
- Decommissioning records

Documentation should be maintained as part of the operational process rather than created only during handovers or incidents.

---

## Implementation Approach

### Phase 1: Discovery

- Document existing assets
- Identify dependencies
- Review support status
- Review operating systems
- Review network architecture
- Identify risks
- Identify documentation gaps

### Phase 2: Standardization

- Define preferred platforms
- Standardize naming
- Standardize documentation
- Define security baselines
- Establish management processes
- Improve inventory quality

### Phase 3: Modernization

- Upgrade supported systems
- Consolidate workloads where appropriate
- Improve virtualization
- Introduce cloud management
- Improve endpoint-management coverage
- Review network segmentation

### Phase 4: Operationalization

- Establish monitoring
- Improve incident handling
- Introduce change control
- Document recovery
- Train responsible personnel
- Clarify vendor escalation

### Phase 5: Lifecycle Management

- Track age and support
- Plan replacements
- Review security
- Review capacity
- Update documentation
- Improve standards

---

## Outcomes

The work contributed to a more structured infrastructure environment.

Key outcomes include:

- Improved infrastructure documentation
- Better visibility of physical and virtual assets
- Increased standardization
- Stronger lifecycle planning
- Improved cloud integration
- More consistent endpoint-management practices
- Better alignment between vessel and shore-side systems
- Stronger security governance
- Improved handover readiness
- A clearer reference architecture for distributed maritime sites

---

## Lessons Learned

### Standardization reduces support complexity

A smaller number of supported patterns makes remote troubleshooting and replacement easier.

### Documentation is part of the infrastructure

Undocumented systems create operational and security risk.

### Cloud services do not remove local dependencies

Vessels still require local networking, identity considerations, resilient connectivity, and recovery procedures.

### Connectivity affects management strategy

Policies and application deployments must account for periods of limited bandwidth.

### Hardware lifecycle needs early planning

Vessel schedules, logistics, customs, and installation windows can significantly extend replacement timelines.

### Infrastructure and security must be designed together

Security controls are more effective when incorporated into architecture and operations from the beginning.

---

## Skills Demonstrated

- Infrastructure architecture
- Windows Server
- Hyper-V
- Active Directory
- Microsoft 365
- Microsoft Intune
- Exchange Online
- Microsoft Teams
- SharePoint
- OneDrive
- Endpoint management
- Networking
- VLAN architecture
- Firewalls
- Wireless networking
- Asset management
- Backup and recovery
- Technical documentation
- Vendor management
- Infrastructure lifecycle management

---

## Confidentiality Notice

This case study is intentionally generalized.

It does not include:

- Production hostnames
- IP addresses
- VLAN identifiers
- Firewall rules
- Credentials
- Tenant identifiers
- Device identifiers
- Actual network diagrams
- Backup configurations
- Security incidents
- Licensing details
- Vendor contracts
- Vessel-specific system inventories

All diagrams are conceptual and are provided only to demonstrate infrastructure and architecture experience.

---

[← Return to main portfolio](../../README.md)
