# Expedition Fleet Connectivity Strategy

**Role:** Technical Lead / Head of IT  
**Period:** 2023–2026  
**Environment:** Expedition-vessel operations  
**Status:** Operational strategy with continuous evaluation  
**Focus:** Starlink | Eutelsat OneWeb | VSAT | Iridium | Inmarsat | Multi-WAN | Business Continuity

../../README.md

---

## Executive Summary

This case study describes the development and evaluation of resilient connectivity strategies for expedition vessels operating across geographically challenging regions.

Vessel connectivity must support a wide range of operational and business requirements, including:

- Vessel administration
- Corporate applications
- Email and collaboration
- Technical support
- Vendor access
- Crew services
- Passenger services
- Operational communications
- Safety-related communications
- Business continuity

No single communications technology provides optimal coverage, performance, resilience, and cost in every region.

The strategy therefore considers a layered, multi-orbit approach using combinations of:

- Low Earth Orbit connectivity
- Geostationary VSAT
- L-band services
- Terrestrial connectivity where available
- Secure vessel networking
- Traffic management
- Failover and recovery procedures

---

## The Challenge

Expedition vessels can operate far from conventional terrestrial communications infrastructure.

Operational areas may include:

- High-latitude regions
- Arctic itineraries
- Antarctic itineraries
- Open-ocean crossings
- Remote islands
- Areas with limited gateway visibility
- Regions with regulatory restrictions
- Ports with congested terrestrial networks

Connectivity performance can be influenced by:

- Satellite visibility
- Coverage boundaries
- Weather
- Obstructions
- Vessel heading
- Antenna placement
- Regulatory authorization
- Provider availability
- Network congestion
- Service-plan limitations
- Bandwidth demand
- Local port infrastructure

A connectivity architecture must therefore account for technical coverage, operational requirements, commercial sustainability, and contingency options.

---

## My Role

My responsibilities included:

- Evaluating satellite-connectivity technologies
- Comparing provider capabilities
- Assessing coverage for vessel itineraries
- Reviewing polar availability
- Considering connectivity redundancy
- Supporting service migration
- Coordinating communication-service transitions
- Evaluating technical and commercial risks
- Supporting provider discussions
- Reviewing bandwidth requirements
- Developing contingency options
- Connecting WAN decisions with vessel network requirements
- Supporting business-continuity planning

The role combined infrastructure architecture, provider management, operational planning, technical analysis, and commercial awareness.

---

## Strategy Objectives

The principal objectives were:

1. Improve vessel connectivity availability.
2. Avoid dependence on a single communications technology.
3. Accommodate polar and remote operations.
4. Support critical vessel and business services.
5. Create practical failover arrangements.
6. Improve visibility of provider and geographic limitations.
7. Support secure connectivity.
8. Balance capacity, resilience, and cost.
9. Enable future provider diversification.
10. Establish a repeatable architecture across the fleet.

---

## Connectivity Technologies

### Low Earth Orbit

LEO services offer lower latency and high-capacity connectivity where coverage and service authorization are available.

Technologies considered include:

- Starlink
- Eutelsat OneWeb

Potential advantages include:

- Lower latency than traditional GEO services
- High throughput
- Increasing global reach
- Relatively compact terminals
- Rapid deployment

Considerations include:

- Provider dependence
- Coverage changes
- Regulatory restrictions
- Commercial-plan changes
- Antenna placement
- Obstruction
- Weather and environmental exposure
- High-latitude performance
- Service-policy limitations

### Geostationary VSAT

Traditional GEO VSAT can provide established maritime connectivity across wide operating regions.

Potential advantages include:

- Mature maritime ecosystem
- Established service providers
- Known operational models
- Broad regional coverage
- Integration with maritime support services

Considerations include:

- Higher latency
- Coverage-beam limitations
- Antenna size and installation
- Blockage zones
- Contract structure
- Capacity constraints
- Polar limitations

### L-Band

L-band services can provide lower-bandwidth but highly resilient connectivity.

Relevant services include:

- Iridium
- Inmarsat

Typical uses may include:

- Backup connectivity
- Operational communication
- Low-bandwidth critical services
- Voice
- Emergency or contingency access

L-band should not generally be treated as a direct replacement for high-capacity broadband, but it can provide an important continuity layer.

### Terrestrial Connectivity

When alongside or near shore, vessels may also use:

- Port Wi-Fi
- Cellular connectivity
- Local fiber or Ethernet services
- Temporary service-provider connections

Terrestrial connectivity can reduce satellite demand but requires careful security and reliability assessment.

---

## Multi-Orbit Architecture

A conceptual multi-orbit design is shown below.

```text
                    EXPEDITION VESSEL
                            |
                  WAN ORCHESTRATION
                            |
          +-----------------+-----------------+
          |                 |                 |
         LEO               GEO             L-Band
          |                 |                 |
     Starlink /            VSAT          Iridium /
       OneWeb                              Inmarsat
          |                 |                 |
          +-----------------+-----------------+
                            |
                    Security Gateway
                            |
                       Core Network
                            |
          +-----------------+-----------------+
          |                 |                 |
      Corporate IT     Operational       User Services
                          Systems
```

This diagram is conceptual. It does not represent the WAN configuration of any specific vessel.

---

## Service Prioritization

Not all vessel traffic has the same priority.

A general traffic model may include:

```text
Priority 1   Safety and critical operational communications
Priority 2   Vessel operations and essential business systems
Priority 3   Corporate services and technical support
Priority 4   Crew services
Priority 5   Passenger or high-volume recreational traffic
```

During degraded connectivity, traffic policies should protect higher-priority services.

Potential controls include:

- Quality of Service
- Application prioritization
- Bandwidth limits
- Session limits
- Scheduled transfers
- Content filtering
- Traffic shaping
- Backup-link restrictions
- User communication

---

## Business Continuity

Connectivity continuity requires more than installing a second terminal.

The continuity plan should consider:

- Provider independence
- Orbit diversity
- Terminal diversity
- Power dependencies
- Network dependencies
- Firewall dependencies
- DNS
- Authentication
- Cloud-service behavior
- Manual failover
- Automatic failover
- Support contacts
- Spare equipment
- Crew procedures
- Escalation paths

### Resilience model

```text
Primary Service
      |
      v
Service Monitoring
      |
      +---- Healthy ----> Normal Operation
      |
      +---- Degraded ---> Traffic Prioritization
      |
      +---- Failed -----> Secondary Service
                              |
                              v
                       Restricted Operation
                              |
                              v
                     L-Band Contingency Layer
```

A backup service is useful only when routing, authentication, user expectations, and operating procedures support the failover.

---

## Polar Operations

Polar connectivity requires specific analysis.

Coverage maps alone may not establish actual operational suitability.

Evaluation should also consider:

- Commercial maritime availability
- Terminal support
- Service authorization
- Elevation angles
- Satellite density
- Gateway dependencies
- Vessel heading and blockage
- Environmental conditions
- Provider support
- Service-plan conditions
- Evidence from actual operations

The strategy distinguishes between:

- Theoretical satellite visibility
- Published coverage
- Commercial service availability
- Operational evidence
- Contractual support

This prevents planned connectivity from being based solely on optimistic coverage graphics.

---

## Vessel Network Integration

WAN services must integrate with the vessel network in a controlled manner.

A conceptual design is:

```text
                 Satellite and WAN Services
                            |
                     WAN Management
                            |
                     Security Gateway
                            |
                        Core LAN
          +-----------------+-----------------+
          |                 |                 |
      Corporate IT         OT          Crew / Guest
          |                 |                 |
       Servers         Operational         User
       Endpoints         Systems          Services
```

Key considerations include:

- Segmentation
- Firewall policy
- DNS
- Authentication
- Bandwidth allocation
- Monitoring
- User groups
- Service prioritization
- Vendor access
- Logging
- Configuration management

---

## Provider Evaluation

Provider evaluation should cover more than headline bandwidth.

### Technical criteria

- Coverage
- Latency
- Throughput
- Terminal requirements
- Antenna performance
- Blockage sensitivity
- Installation implications
- Power requirements
- Support model
- Integration capability
- Failover compatibility
- Cybersecurity

### Operational criteria

- Supported itineraries
- Polar suitability
- Port restrictions
- Activation process
- Service restoration
- Equipment replacement
- Vessel support
- Documentation
- Escalation paths

### Commercial criteria

- Monthly service cost
- Data allowance
- Overage
- Installation cost
- Hardware ownership
- Commitment period
- Suspension conditions
- Upgrade options
- Early termination
- Currency exposure
- Price-change risk

Unconfirmed pricing should not be treated as an established cost in a formal comparison.

---

## Implementation Approach

### Phase 1: Requirements

- Identify vessel operating regions
- Document critical services
- Estimate bandwidth demand
- Identify user groups
- Understand existing contracts
- Review current equipment

### Phase 2: Coverage Analysis

- Compare provider coverage
- Review polar areas
- Document known limitations
- Distinguish theoretical and commercial availability
- Gather operational feedback

### Phase 3: Architecture

- Define primary and secondary services
- Determine failover approach
- Establish traffic priorities
- Review firewall and routing requirements
- Identify monitoring requirements

### Phase 4: Commercial Review

- Obtain provider proposals
- Compare confirmed pricing
- Separate assumptions from confirmed costs
- Review contract terms
- Consider fleet-level purchasing

### Phase 5: Implementation

- Coordinate equipment
- Plan installation
- Configure integration
- Test services
- Test failover
- Document support procedures
- Train responsible personnel

### Phase 6: Review

- Monitor performance
- Compare actual and planned coverage
- Review incidents
- Track costs
- Update the contingency plan
- Reassess providers periodically

---

## Outcomes

The work established a stronger basis for resilient fleet connectivity.

Key outcomes include:

- Improved understanding of multi-orbit options
- Clearer distinction between capacity and resilience
- Increased attention to polar service availability
- Structured provider-comparison criteria
- Better alignment between WAN design and vessel operations
- Improved business-continuity planning
- Recognition of single-provider dependency as a strategic risk
- A framework for future fleet cost modelling
- A repeatable method for evaluating new communications services

---

## Lessons Learned

### Coverage maps need operational validation

Published coverage does not automatically mean commercially supported or operationally proven maritime service.

### Redundancy must include provider diversity

Two terminals using the same provider may not protect against a provider-level outage or commercial disruption.

### Backup links need testing

A backup service that has not been tested may fail because of routing, authentication, configuration, or procedural issues.

### Bandwidth is not the only metric

Latency, availability, support, installation, service terms, and geographic coverage are equally important.

### Commercial risk is also technical risk

Pricing changes, data policies, equipment availability, and contract terms can affect operational resilience.

### User expectations require management

High-capacity LEO services can rapidly increase bandwidth demand. Traffic governance remains necessary.

---

## Skills Demonstrated

- Maritime connectivity architecture
- Satellite communications
- LEO, GEO, and L-band evaluation
- Starlink
- Eutelsat OneWeb
- VSAT
- Iridium
- Inmarsat
- Multi-WAN strategy
- Polar coverage analysis
- Business continuity
- Provider evaluation
- Commercial analysis
- Network integration
- Infrastructure planning
- Vendor management

---

## Confidentiality Notice

This case study is intentionally generalized.

It does not include:

- Vessel names
- Terminal identifiers
- IP addresses
- Provider account details
- Actual routing
- Firewall configurations
- Contracts
- Commercial pricing
- Bandwidth allocations
- Usage statistics
- Provider quotations
- Vessel-specific coverage records

All diagrams are conceptual and are intended only to demonstrate the architecture and decision-making approach.

---

../../README.md
