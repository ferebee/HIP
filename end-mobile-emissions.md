# HIP: End MOBILE Emissions

- Author(s): [@DanielChrobak](https://github.com/DanielChrobak)

- Start Date: 2024-11-23

- Category: Economic, Technical

- Original HIP PR: [To be filled after submission]

- Tracking Issue: [To be filled after submission]

- Vote Requirements: veMOBILE Holders
  
## Summary

With the implementation of [HIP-138][hip-138], projected to occur around January 2025, HNT emissions to the MOBILE treasury will cease. [HIP-138][hip-138], whose veHNT vote succeeded, specifies certain provisions which would support the treasury exchange rate of MOBILE. These provisions are contingent on the cessation of MOBILE emissions, which would have been specified with a succesful veMOBILE vote on [HIP-138][hip-138], but the veMOBILE vote failed. This proposal would separately approve the cessation of MOBILE emissions by veMOBILE vote, thereby fulfilling the conditions stated in [HIP-138][hip-138] and allowing the subsidies to proceed.

## Motivation

Although broad consensus was reached on the provisions of [HIP-138][hip-138] prior to the vote, the veHNT and veIOT votes passed, but the veMOBILE vote failed due to large NO votes shortly before voting ended.

It has been suggested that these votes may have been motivated by an incomplete understanding of [HIP-138][hip-138], and that further discussion prior to the vote could have contributed to a fuller understanding by all parties.

Separately, the contingency provisions in [HIP-138][hip-138] relating to a NO vote by veMOBILE, as explained in the Voting section of that proposal, were intended to avoid a situation in which continuing MOBILE emissions post implementation would have been supported by subsidies to the MOBILE treasuries which were not intended for that purpose.

Therefore, if the MOBILE subnetwork, with a full understanding of all issues involved, now decides to stop MOBILE emissions with the implementation of [HIP-138][hip-138], the original intents of [HIP-138][hip-138] may be implemented in harmony, with the support of a supermajority of all stakeholders, as represented by their final and independent votes.

## Stakeholders

- MOBILE network participants (Hotspot owners, operators)
- MOBILE token holders

Indirectly, all other stakeholders in the Helium network are affected, but their positions are already represented by their votes on [HIP-138][hip-138], which could be implemented fully if this proposal is approved.

## Detailed Explanation

The passing of this HIP will result in the following key actions:

1. **Cessation of MOBILE Token Emissions**: All new emissions of MOBILE tokens will be halted with the implementation of [HIP-138][hip-138].

2. **HNT Allocation to MOBILE Treasury**: As specified in [HIP-138][hip-138], 2.9M HNT will be minted and allocated over time to the MOBILE treasury.

3. **Exchange of Operations Fund MOBILE Tokens**: As specified in [HIP-138][hip-138], Helium Foundation will burn MOBILE tokens from the MOBILE Operations Fund, and the burned tokens will be replaced through a one-time mint of 1.3M HNT.

This aligns with the intent of the contingency provisions in [HIP-138][hip-138], which that proposal explains as follows in the `Voting` section:

```The additional mint of 2.9M HNT to the MOBILE treasury is intended to support the value of existing MOBILE tokens, rather than to back additional MOBILE emissions. Therefore, it is contingent on a veMOBILE decision to stop MOBILE emissions. The same applies to the Foundation burn of the 18.2B MOBILE tokens in the Operations Fund.```

## Implementation Timeline:
This HIP will be implemented simultaneously with the implementation of [HIP-138][hip-138].

## Drawbacks

Some participants may prefer the tokenomics resulting from the provisions of [HIP-138][hip-138] as voted, with YES votes from veHNT and veIOT, and a NO vote from veMOBILE. However, a YES vote on this proposal would deliver the same result as [HIP-138][hip-138] would have delivered if it had received YES votes from all three groups, implemented as originally proposed.

## Rationale and Alternatives

This proposal is the best path forward because:
- It aligns with the broader Helium ecosystem’s direction as set by [HIP-138][hip-138].
- It secures additional value for the MOBILE network through HNT allocation.
- It simplifies the reward structure.

An alternative would be to continue MOBILE emissions beyond the implementation of [HIP-138][hip-138], but this would result in the dilution of existing MOBILE tokens.

## Deployment Impact

This proposal will be implemented by Helium core developers. An initial investigation of the work required suggests that this HIP can be implemented within the specified timeline.

## Success Metrics

This HIP is successful if MOBILE emissions cease with the implementation of [HIP-138][hip-138].

[hip-138]: https://github.com/helium/HIP/blob/main/0138-return-to-hnt.md
