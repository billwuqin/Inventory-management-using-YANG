Comparative analysis including drafts and standards reference looking at inventory or consuming inventory data.

|                                       | Network-Service/Network-Element &  Device Level Coverage | HW/SW Coverage                                   | comments                                                                                                                                                                                                                                                                                                                                                                           | Use cases                                                                                                                                                                                                      | IETF-WG | Easy to extend |
|---------------------------------------|----------------------------------------------------------|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|----------------|
| openconfig-platform                   |                                                          | HW                                           | Module that covers inventory as specific Use Case  Inlcude the concept of subcomponent but doesn’t add flexibility                                                                                                                                                                                                                                                                 | 1.       network inventory                                                                                                                                                                                     | N/A     | ++             |
| DMLMO                                 | Network Service Network-Element Device                   | SW, HW, virtual or physical,  including Service  | The YANG modules in the draft needs to consume inventory information,  but it is not exclusive use case:  Asset: needs to be identified as part of the inventory to correlate license,  feature, usage, etc. Augment allows to include vendor specification as part of the inventory module                                                                                        | 1.       License Inventory&Activation   2.       Features in Use  3.       Assets in Use  4.       Risk Mitigation Check (RMC) 5.       Errata   6.       Security Advisory  7.       Optimal Software Version | OPSAWG  | +++            |
| SBOM                                  | Device                                                   | Identifies SW running on a system                | It is not looking at HW inventory.   The YANG module in the draft needs to consume inventory information, in particular,  to augment MUD (Manufacturer Usage Description Specification)  https://datatracker.ietf.org/doc/html/rfc8520                                                                                                                                             | 1.       visibility to what software is running on a system 2.       determine vulnerabilities that software may have                                                                                          | OPSAWG  | N/A            |
| network-inventory                     | Device                                                   | network HW inventory data                        | It can be augmented by specific technology / vendor It doesn’t refer to any SW running on the HW network device.                                                                                                                                                                                                                                                                   | Physical location where the equipment is placed,  including how to locate the specific module to the slot in the chassis                                                                                       | CCAMP   | ++             |
| Data manifest for Streaming Telemetry | Device                                                   |                                                  | The YANG modules in the draft needs to consume inventory information:  The platform manifest contains a comprehensive set of information  characterize a data source.    The so called “platform manifest” can be compared with the asset concept  from DMLMO, even draft´s use cases are different.   Draft doesn’t address the relationship with other elements in the inventory | Store the contextual information(details about the platform that generate those data)  along with the collected data, in order to keep the collected data exploitable in the future.                           | OPSAWG  | N/A            |
| RFC8348                               | Device                                                   | HW inventory data                                | Aligned YANG module to ENTITY-MIB                                                                                                                                                                                                                                                                                                                                                  |                                                                                                                                                                                                                |         |                |
| RFC8199                               | Network-Service  Network-Element(equal to feature)       | N/A                                              | RFC covers the concept and term to form a useful  taxonomy for consistent classification of YANG modules  in two dimensions:    o  The layering of modules based on their abstraction levels    o  The module origin type based on the nature and intent of the       content                                                                                                      | no YANG modules included in the RFC.   note: DMLMO could consume the such concepts, but needs YANG  specification for the representation                                                                       |         |                |
| RFC8520*                              | Device                                                   | HW, SW                                           | focus is on Access control use cases, also to consume from inventory                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                |         |                |