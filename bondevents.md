Bond Events are recorded by ixo protocol blockchains as core state records.
These events are triggered by state changes in the `Bonds` module.
Functionally, state changes are what drive the bond state machine. The diagram maps these states and transition events.

https://www.lucidchart.com/invitations/accept/ecaccdec-bdb5-495e-87c3-2aa5fd3dd701

|Type          | Attribute Key     | Attribute Value             |
|--------------| ------------------| ----------------------------|
|bond_action   | bond_did          | {bondDid}                   |
|bond_action   | action            | {action} [**0**]                |
|alpha_update  | bond_did          | {bondDid}                   |
|alpha_update  | alpha             | {alpha}                     |
|status_update | bond_did          | {bondDid}                   |
|status_update | status            | {status} [**1**]                |
|announcement  | bond_did          | {bondDid}                   |
|announcement  | announcement_uri  | {announcementUri} [**2**]       |
|dispute       | bond_did          | {bondDid}                   |
|dispute       | claim_id          | {claimId}                   |
|dispute       | status            | {status} [**3**]                |

Possible values:
- [**0**]: issue, complete, settle, suspend
- [**1**]: setup, launch, active, paused, suspended, closing, settled, archived
- [**3**]: open, resolving, audit, resolved, closed

Notes:
- [**2**]: the announcement URI is typically the IPFS content address of an announcement message file serialised in JSON
