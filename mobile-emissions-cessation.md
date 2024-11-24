# HIP: MOBILE Network Emission Cessation

- Author(s): [@DanielChrobak](https://github.com/DanielChrobak)

- Start Date: 2024-11-23

- Category: Economic, Technical

- Original HIP PR: [To be filled after submission]

- Tracking Issue: [To be filled after submission]

- Vote Requirements: veMOBILE Holders

## Summary

This proposal aims to halt MOBILE token emissions and replace them with HNT emissions in accordance with HIP 138. It seeks to secure the allocation of 2.9M HNT to the MOBILE treasury and establish a new 1.3M HNT MOBILE Growth Fund in exchange for burning 18.2B MOBILE tokens from the Operations Fund. This HIP addresses the specific needs of the MOBILE network following the partial approval of HIP 138.

HIP 138 states the contingencies for the MOBILE network as follows:

> The additional mint of 2.9M HNT to the MOBILE treasury is intended to support the value of existing MOBILE tokens, rather than to back additional MOBILE emissions. Therefore, it is contingent on a veMOBILE decision to stop MOBILE emissions. The same applies to the Foundation burn of the 18.2B MOBILE tokens in the Operations Fund.

Under [Voting](https://github.com/helium/HIP/blob/main/0138-return-to-hnt.md#voting)

> Following HIP 20, Helium experienced L1 outages, leaving 4.2 million unminted HNT. This proposal intends to use this HNT in two ways. First, a new gradual emission of HNT into the MOBILE treasury from the implementation date until the next halvening (August 1, 2025) is established, contingent on a veMOBILE decision to stop MOBILE emissions. This would be a total of 2.9M HNT supplementing the MOBILE treasury.

> Second, a new MOBILE Growth Fund is established using the remaining 1.3M HNT, which corresponds roughly to the value of the current MOBILE tokens in the Operations Fund at the treasury rate. This fund, directed by the Helium Foundation, is to be used for deployer incentives, such as boosted rewards, subsidized hardware swaps, or incentives for new service providers. To balance this, the Foundation will burn the entirety of its current 18.2B MOBILE holdings, also contingent on a veMOBILE decision to stop MOBILE emissions, thereby decreasing the circulating supply of the MOBILE token and strenghtening the treasury exchange rate.

Under [Unissued HNT Adjustment and Reestablishment of the MOBILE Operations Fund](https://github.com/helium/HIP/blob/main/0138-return-to-hnt.md#unissued-hnt-adjustment-and-reestablishment-of-the-mobile-operations-fund)

The use of "a veMOBILE decision" rather than "the veMOBILE decision" in these contexts is significant. It indicates that the contingency is not tied specifically to the approval of HIP 138, but rather to any decision made by veMOBILE to stop MOBILE emissions. This interpretation, supported by at least two-thirds of the HIP 138 authors, allows for greater flexibility in implementing these changes.

Consequently, this HIP proposes to fulfill the contingency required by HIP 138 by providing a veMOBILE decision to discontinue MOBILE emissions. Upon approval, this would trigger the allocation of 2.9M HNT to the MOBILE treasury, the establishment of the 1.3M HNT MOBILE Growth Fund, and the burning of 18.2B MOBILE tokens from the Operations Fund, as outlined in HIP 138.

## Motivation

- To align the MOBILE network with the broader Helium ecosystem's move towards simplification and unified tokenomics.
- To secure the additional HNT allocation for the MOBILE treasury.
- To reduce the circulating supply of MOBILE tokens.
- To streamline rewards distribution directly in HNT, making the system more attractive to network builders and participants.

## Stakeholders

- MOBILE network participants (Hotspot owners, operators)
- MOBILE token holders
- Helium Foundation
- Future MOBILE network builders and investors

Feedback will be solicited through:
- Helium Community Discord channels
- Helium Forum discussions
- Direct outreach to major MOBILE network stakeholders

## Detailed Explanation

The passing of this HIP will result in the following key actions:

1. **Cessation of MOBILE Token Emissions**: All new emissions of MOBILE tokens will be halted before or simultaneously with the implementation of HIP 138.

2. **HNT Allocation to MOBILE Treasury**: As outlined in HIP 138, 2.9M HNT will be minted and allocated to the MOBILE treasury. This will occur gradually from the implementation date until the next halvening (August 1, 2025).

3. **Exchange of Operations Fund MOBILE Tokens**: The Helium Foundation will burn the 18.2B MOBILE tokens currently held in the Operations Fund in exchange for a new 1.3M HNT MOBILE Growth Fund. This exchange process involves two key steps:
   1. The creation of a new 1.3M HNT MOBILE Growth Fund, which is part of the 4.2 million unissued HNT from the Helium L1 mentioned in HIP 138.
   2. The burning of 18.2B MOBILE tokens by the Helium Foundation from the Operations Fund.

## Implementation Timeline:
This HIP must be implemented before or simultaneously with the implementation of HIP 138 to ensure a smooth transition and to secure the proposed benefits in HIP 138 for the MOBILE network.

## Drawbacks

Potential confusion for MOBILE network participants during the transition period.

## Rationale and Alternatives

This proposal is the best path forward because:
- It aligns with the broader Helium ecosystem's direction as set by HIP 138.
- It secures additional value for the MOBILE network through HNT allocation.
- It simplifies the reward structure, making it more attractive for network growth.

## Deployment Impact

This proposal will be implemented by Helium core developers. An initial investigation of the work required suggests that this HIP can be implemented within the specified timeline.

## Success Metrics

This HIP is successful if MOBILE emissions cease by the implementation of HIP 138.
