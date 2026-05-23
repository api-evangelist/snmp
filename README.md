# SNMP (snmp)

Simple Network Management Protocol (SNMP) is the foundational IETF standard for monitoring and managing network devices. SNMP defines a request/response protocol over UDP (ports 161 and 162) for retrieving and altering management variables exposed by agents on routers, switches, servers, UPSs, and other equipment, plus an asynchronous trap/notification channel for event delivery. The protocol family spans three major generations — SNMPv1 (RFC 1157), SNMPv2c (RFC 1901-1908), and the modular SNMPv3 architecture (RFC 3411-3418, extended by RFC 7860 for HMAC-SHA-2 authentication) — and is paired with the Structure of Management Information (SMI) and a vast catalog of MIB modules, most notably the IF-MIB (RFC 2863) for network interfaces. SNMP remains the lingua franca of network monitoring, consumed primarily by NMS platforms such as Nagios, Zabbix, PRTG, SolarWinds, LibreNMS, and Observium, and implemented in open source primarily by the Net-SNMP suite.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/snmp/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

SNMP, Network Management, Network Monitoring, IETF, Protocol, MIB, SMI, OID, Agents, Traps, UDP, Operations

## Timestamps

- **Created:** 2025-01-01
- **Modified:** 2026-05-23

## APIs

### SNMPv1 (RFC 1157)
The original Simple Network Management Protocol defined in RFC 1157 (May 1990). Establishes the five core PDUs (GetRequest, GetNextRequest, GetResponse, SetRequest, Trap), community-string authentication, ASN.1 message encoding, and UDP transport on ports 161 and 162. Now classified as Historic by the IETF but still widely deployed on legacy equipment.

**Human URL:** [https://datatracker.ietf.org/doc/html/rfc1157](https://datatracker.ietf.org/doc/html/rfc1157)

#### Tags

SNMPv1, Community Strings, PDU, Historic

#### Properties

- [Specification](https://datatracker.ietf.org/doc/html/rfc1157)
- [Documentation](https://datatracker.ietf.org/doc/rfc1157/)

### SNMPv2c (RFC 1901-1908)
Community-based SNMPv2, the most widely deployed version of SNMP in production today. Adds the GetBulkRequest PDU for efficient table retrieval and the InformRequest PDU for acknowledged notifications, while retaining the community-string security model of SNMPv1. RFC 3416 later republished the v2 protocol operations as part of the SNMPv3 framework.

**Human URL:** [https://datatracker.ietf.org/doc/html/rfc1901](https://datatracker.ietf.org/doc/html/rfc1901)

#### Tags

SNMPv2c, GetBulk, InformRequest, Community Strings

#### Properties

- [Specification (RFC 1901)](https://datatracker.ietf.org/doc/html/rfc1901)
- [Specification (RFC 3416)](https://datatracker.ietf.org/doc/html/rfc3416)
- [Documentation](https://datatracker.ietf.org/doc/rfc1901/)

### SNMPv3 Architecture (RFC 3411-3418)
The modular SNMPv3 management framework. RFC 3411 defines the SNMP engine, Message Processing Subsystem, Security Subsystem, and Access Control Subsystem; RFC 3414 specifies the User-based Security Model (USM) with authentication and privacy; RFC 3415 specifies the View-based Access Control Model (VACM); RFC 3416 redefines protocol operations; RFC 3417 covers transport mappings; RFC 3418 contains the MIB for SNMPv3 itself. RFC 7860 extends USM with HMAC-SHA-2 authentication protocols.

**Human URL:** [https://datatracker.ietf.org/doc/html/rfc3411](https://datatracker.ietf.org/doc/html/rfc3411)

#### Tags

SNMPv3, USM, VACM, Security, Authentication, Privacy

#### Properties

- [Specification — RFC 3411 (Architecture)](https://datatracker.ietf.org/doc/html/rfc3411)
- [Specification — RFC 3412 (Message Processing)](https://datatracker.ietf.org/doc/html/rfc3412)
- [Specification — RFC 3414 (USM)](https://datatracker.ietf.org/doc/html/rfc3414)
- [Specification — RFC 3415 (VACM)](https://datatracker.ietf.org/doc/html/rfc3415)
- [Specification — RFC 3416 (Protocol Operations v2)](https://datatracker.ietf.org/doc/html/rfc3416)
- [Specification — RFC 3417 (Transport Mappings)](https://datatracker.ietf.org/doc/html/rfc3417)
- [Specification — RFC 3418 (SNMPv3 MIB)](https://datatracker.ietf.org/doc/html/rfc3418)
- [Specification — RFC 7860 (HMAC-SHA-2 Auth)](https://datatracker.ietf.org/doc/html/rfc7860)

### IF-MIB (RFC 2863) — The Interfaces Group MIB
The canonical SNMP MIB module for network interface management, published June 2000. Defines ifTable, ifXTable, ifStackTable, and ifRcvAddressTable, plus the ifType enumeration registered by IANA. Universally implemented by routers, switches, NICs, and operating systems; the most-polled MIB in production network monitoring.

**Human URL:** [https://datatracker.ietf.org/doc/html/rfc2863](https://datatracker.ietf.org/doc/html/rfc2863)

#### Tags

IF-MIB, MIB, Interfaces, ifTable, ifXTable

#### Properties

- [Specification](https://datatracker.ietf.org/doc/html/rfc2863)
- [ifType Registry](https://www.iana.org/assignments/ianaiftype-mib/ianaiftype-mib)

### SMI and the OID Tree
Structure of Management Information — the data definition language and naming scheme that every MIB module is written against. The IANA SMI Numbers registry administers the OID hierarchy rooted at 1.3.6.1, including standard MIBs under 1.3.6.1.2.1 and Private Enterprise Numbers under 1.3.6.1.4.1 (the namespace organizations use to publish their own MIBs).

**Human URL:** [https://www.iana.org/assignments/smi-numbers/smi-numbers.xhtml](https://www.iana.org/assignments/smi-numbers/smi-numbers.xhtml)

#### Tags

SMI, OID, IANA, Enterprise Numbers, PEN

#### Properties

- [SMI Numbers Registry](https://www.iana.org/assignments/smi-numbers/smi-numbers.xhtml)
- [Private Enterprise Numbers](https://www.iana.org/assignments/enterprise-numbers/)

## Common Properties

- [IETF OPSAWG Working Group](https://datatracker.ietf.org/wg/opsawg/about/)
- [RFC 3411 — SNMPv3 Architecture](https://datatracker.ietf.org/doc/html/rfc3411)
- [Net-SNMP Project](https://www.net-snmp.org/)
- [Net-SNMP Source Code](https://github.com/net-snmp/net-snmp)
- [IANA SMI Numbers Registry](https://www.iana.org/assignments/smi-numbers/smi-numbers.xhtml)

## Artifacts

- **Vocabulary:** [vocabulary/snmp-vocabulary.yml](vocabulary/snmp-vocabulary.yml) — normative SNMP terminology drawn from RFCs 1157, 1901-1908, 3411-3418, 7860, and 2863
- **JSON-LD Context:** [json-ld/snmp-context.jsonld](json-ld/snmp-context.jsonld) — linked-data context mapping SNMP concepts (Engine, MIBModule, ManagedObject, OID, PDU, etc.) onto schema.org and the SNMP vocabulary

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
