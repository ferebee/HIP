# HIP 148: Reallocate Mobile Mapping Rewards

- Author: [@madninja](https://github.com/madninja)
- Start Date: 2025-09-23
- Category: Economic, Technical
- Original HIP PR: [#1186](https://github.com/helium/HIP/pull/1186)
- Tracking Issue: [#1187](https://github.com/helium/HIP/issues/1187)
- Voting Requirement: veHNT Holders

---

## Summary

Currently, 20% of HNT emissions allocated to the Mobile network are reserved for Mobile Mapping rewards. Despite a growing number of mappers since Helium Mobile launched, mapping has not delivered the impact originally intended. This proposal aims to simplify the reward structure and refocus incentives by making the following changes:

1. Move the 10% back into the Service Provider Rewards Pool as originally intended prior to [HIP-79][hip-79].
2. Move the remaining 10% of Mobile Mapping rewards to the Data Transfer pool for coverage deployers.
3. Repeal the [HIP-79][hip-79], [HIP-114][hip-114], and [HIP-118][hip-118] to reflect these changes.

In addition, this HIP proposes the following changes to the Service Provider rewards to further simplify the Mobile tokenomics:

1. Remove the Oracle Operator rewards allocation (4%) and allocate it to the Service Provider pool.
2. Remove the proportional Service Provider rewards system based on DC burn introduced in [HIP-87][hip-87] and emit rewards to the Nova Service Provider.
3. Remove the Referral program introduced in [HIP-114][hip-114] that allocated a portion of unused Service Provider rewards to incentive programs.
4. Repeal [HIP-87][hip-87], and [HIP-114][hip-114] to reflect these changes.

## Motivation

The issues with Mobile Mapping include:

1. The complexity of maintaining software that shares location regularly on highly variable handsets. Battery, memory, and CPU impact with slow feedback to end users have plagued the system from the start.
2. The ongoing sophistication of the mapping gaming techniques to maximize mapping rewards by gaming location data. This has polluted the mapping data set substantially, which has caused more work to clean up the data.
3. Verification mapping, where an active Helium Mobile mapper connects to a Helium Mobile Hotspot, has only been observed in under 5% of all mapping data. This number is even lower if the forced hotspot CDR verification methods required for PoC rewards are excluded.
4. The number of Helium Mobile subscribers turning off mapping is quite high given the impact on battery and the lack of clear benefit to the end user once the focus shifted to normal, non-crypto subscribers.
5. While the mapping data set has been used in an "observed demand" layer on Helium World, it has not been very useful in guiding deployers to locations to deploy at. This is partially due to polluted data sets, but mostly because carrier offload locations are a much higher quality signal of where to deploy than mapping data.

The Service Provider Rewards Pool was designed to reward multiple Service Providers on the network based on their contribution to the network. Since that has not materialized, has existing complexity around both tracking the DC burned, and raises questions what to do with any overage if the SP does not transfer enough to use up the pool fully. The Referral program was designed to try to utilize these overages but the same effect can be achieved in other ways.

Finally, since the Oracle Operator rewards are not being used, we propose to move them to the Service Provider Rewards pool. This simplifies the rewards structure to a simpler set of deployers, stakers, and service providers.

## Stakeholders

This proposal affects:

- Legacy Crypto Mappers, which would lose their mapping rewards. The upside is they retain a competitive cell phone plan.
- Helium Mobile would see the rewards shift from per-subscriber mapping rewards to a simpler Service Provider rewards model.
- Subscriber Referral Programs, which will be terminated as part of this HIP.
- Nova, as the Oracle Operator will no longer have access to a future Oracle Operator pool since the rewards will be moved to the Service Provider Rewards Pool, which may be re-allocated for other uses in the future.

## Detailed Explanation

Under this proposal, the 10% reservation of HNT emissions for Mobile Mapping would move back to the Service Provider Rewards Pool. The other 10% would be moved to the Data Rewards Pool.

The Incentive Escrow Fund would be terminated, but this would not affect existing Service Provider Rewards and simplifies on-chain accounting and behavior.

Finally, the 4% Oracle Operator rewards would be emitted to the Service Provider Rewards Pool.

A table of the percentage changes over time is given below. The last column shows the new allocation proposed under this HIP.

|                                      |  HIP 53  |  HIP 79  | HIP 146  | HIP 148  |
| ------------------------------------ | :------: | :------: | :------: | :------: |
| **Data Transfer**<br>(unused to POC) |   40%    |   40%    |   60%    |   70%    |
| **POC**                              |   20%    |   20%    |    0%    |    0%    |
| **Service Providers**                |   20%    |   10%    |   10%    |   24%    |
| **Mappers**                          |   10%    |   20%    |   20%    |    0%    |
| **Oracle Operators**                 |    4%    |    4%    |    4%    |    0%    |
| **Stakers**                          |    6%    |    6%    |    6%    |    6%    |
| **Total**                            | **100%** | **100%** | **100%** | **100%** |

### Repeal of HIP-79, HIP-87, HIP-118, and HIP-114

[HIP-79][hip-79] defined the increase of the Mobile Mapping Rewards by allocating an additional 10% of emissions from Service Provider Rewards to Mobile Mapping Rewards. [HIP-118][hip-118] defined a more granular breakdown of the Mobile Mapping rewards to include Verification Mapping behavior.

This HIP will remove the need for these two mapping related HIPs. Future systems for Verification Mapping like behavior, will be defined as needed and could be achieved without a rewards system.

[HIP-87][hip-87] defined a proportional rewards system for Service Providers based on the amount of Data Credits (DC) burned. This was originally designed to reward multiple Service Providers on the network based on their contribution to the network. Since that has not materialized, has existing complexity around both tracking the DC burned, and raises questions what to do with any overage if the SP does not transfer enough to use up the pool fully, this HIP will repeal [HIP-87][hip-87]. Service Provider Rewards will be emitted directly to the current single active Service Provider (Nova). At the time a new Service Provider is onboarded as an on-chain entity instead of an offload partner, the Service Provider pool can be re-evaluated through a new HIP.

[HIP-114][hip-114] defined a mechanism for Service Providers to allocate portions of Service Provider Rewards to Referral like programs before any Service Provider Reward overage is burned. Given the repeal of [HIP-87][hip-87] this HIP will end the involved complexity.

### Adjustments to HIP-53

[HIP-53][hip-53] defined the original 10% reservation of HNT emissions to Mobile Mapping rewards. This HIP will adjust the reservation to move the 10% to the Data Rewards Pool.

In addition, [HIP-53][hip-53] also defined the 4% of emissions to Oracle Operators. This HIP will move the 4% to the Service Provider Rewards Pool.

## Drawbacks

- Without discovery mapping data, geographic user demand data for Helium Mobile will not be available in the same form. This is mitigated by getting a much larger volume of high-quality tower-based data to infer both valid subscriber activity and approximate demand areas.

## Unresolved Questions

## Deployment Impact

Core developers will complete the implementation of this HIP on approval.

[hip-53]: https://github.com/helium/HIP/blob/main/0053-mobile-dao.md
[hip-87]: https://github.com/helium/HIP/blob/main/0087-proportional-service-provider-rewards.md
[hip-79]: https://github.com/helium/HIP/blob/main/0079-increase-mobile-mapping-rewards.md
[hip-118]: https://github.com/helium/HIP/blob/main/0118-mobile-verification-mapping.md
[hip-114]: https://github.com/helium/HIP/blob/main/0114-mobile-referral-programs.md
