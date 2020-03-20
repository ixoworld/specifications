Bond Events are recorded by ixo protocol blockchains as core state records.
These events are triggered by state changes in the `Bonds` module.
Functionally, state changes are what drives the bond state machine. The diagram maps these states and transition events.

https://www.lucidchart.com/invitations/accept/ecaccdec-bdb5-495e-87c3-2aa5fd3dd701

|Type        | Attribute Key | Attribute Value             |
|------------| --------------| ----------------------------|
|Alert       | `BondAction`. | {"bondaction":"issue"}.     |
|Alert | `BondAction`| {"bondaction":"completionclaim"}|
|Alert | `BondAction`| {"bondaction":"settle"}|
|Alert | `BondAction`| {"bondaction":"suspend"}|
|Alert |`Alphaupdate`|{"bondalpha":"alpha"}|
|Status | `BondState`|{"bondstate":"Setup"}|
|Status | `BondState`|{"bondstate":"Launch"}|
|Status | `BondState`|{"bondstate":"Active"}|
|Status | `BondState`|{"bondstate":"Paused"}|
|Status | `BondState`|{"bondstate":"Suspended"}|
|Status | `BondState`|{"bondstate":"Closing"}|
|Status | `BondState`|{"bondstate":"Settled"}|
|Status | `BondState`|{"bondstate":"Archived"}|
|Announcement |`Announce`|{"announce":"AnnouncementURI"}|
|Dispute | `DisputeClaim`|{"disputeclaimID":"ClaimID"}|
|Dispute | `DisputeStatus`|{"disputestatus":"ClaimID.Open"}|
|Dispute | `DisputeStatus`|{"disputestatus":"ClaimID.Resolving"}|
|Dispute | `DisputeStatus`|{"disputestatus":"ClaimID.Audit"}|
|Dispute | `DisputeStatus`|{"disputestatus":"ClaimID.Resolved"}|
|Dispute | `DisputeStatus`|{"disputestatus":"ClaimID.Closed"}|

`AnnouncementURI` is typically the IPFS content address of an announcement message file serialised in JSON.
