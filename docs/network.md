# Network Architecture Overview

## Global Metastore

A metastore has been deployed in the **South** region and configured for use across all environments.

---

## Network Design: Hub and Spoke Architecture

### Hub

The **Hub virtual network** is the central point of connectivity for cross-premises networking. It:

- Contains the primary point of egress.
- Enables communication between spokes when required.
- Hosts shared services like DNS, NTP, or AD DS.

### Spoke

The **Spoke virtual networks** are used to isolate and manage workloads for each environment. Currently:

- Two spokes are deployed in **Development**.
- One spoke is deployed in **Production**.

---

### Why We’ve Used This Architecture

- We have multiple environments (development, testing, production) needing shared services.
- Shared services are placed in the **hub**.
- Spokes maintain **environmental isolation**.
- Spokes do **not require connectivity with each other**, but **do require access to shared services**.
- Central control is needed for:
  - **Security**, e.g., DMZ firewall, VPN Gateway in the hub.
  - **Connectivity**, e.g., selective isolation between spokes.

---

## Ownership

- The **hub network infrastructure** is owned by the **Team**.
- The **spoke network infrastructure** has been provisioned by the **Team**.

---

## Assumption

- Hub address space: `10.0.0.0/16`
- Address range: `10.0.0.0 – 10.0.255.255`
- Already in use by the team.

---

## VNet Details

A **Virtual Network** with an **address count of 4,096** has been provisioned in each environment.
