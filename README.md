# IBC-relayer

## What is IBC? ##

IBC is a reliable, ordered, and authenticated protocol for relaying arbitrary messages between independent distributed ledgers

StakeWithUs is currently relaying (Using Hermes) for the following projects:

1) Cosmos (ATOM)
2) Osmois (OSMOS)
3) EVMOS (EVMOS)
4) JUNO (JUNO)
4) Injective (INJ)
5) Bandchain (BAND) - Oracle
6) Persistence (XPRT)

## Recommended Hardware and OS Configuration ##

OS: Ubuntu 20.04 LTS minimal
* Disable root login
* Change SSH default port
* Use SSH Keys
* Enable UFW and only allow SSH custom port and port 3001 (telemetry) to specific IP (bastion host and monitoring host) ingress.

Hardware: Hetzner Bare Metal AX101
* AMD Ryzen 9 5950X
* 128GB DDR4 ECC RAM
* 4 x 3.84TB NVMe SSD RAID 10

We require a more powerful bare metal node due to the fact that we are running relayer full nodes as well to improve the latency in relaying the packets.

## Channels

Chain | Chain-ID | Token | Dst-Chain | Channel | Port
----- | -------- | ----- | --------- | ------- | ----
CosmosHub | cosmoshub-4 | uatom | Osmosis | Channel-141 | Transfer
CosmosHub | cosmoshub-4 | uatom | Juno | Channel-207 | Transfer
CosmosHub | cosmoshub-4 | uatom | Evmos | Channel-292 | Transfer
Osmosis | osmosis-1 | uosmos | CosmosHub | Channel-0 | Transfer
Osmosis | osmosis-1 | uosmos | Juno | Channel-42 | Transfer
Osmosis | osmosis-1 | uosmos | Evmos | Channel-204 | Transfer
Osmosis | osmosis-1 | uosmos | Injective | Channel-122 | Transfer
Osmosis | osmosis-1 | uosmos | Persistence | Channel-6 | Transfer
Osmosis | osmosis-1 | uosmos | Persistence | Channel-6 | ICA
Juno | juno-1 | ujuno | CosmosHub | Channel-1 | Transfer
Juno | juno-1 | ujuno | Osmosis | Channel-0 | Transfer
Juno | juno-1 | ujuno | Injective | Channel-59 | Transfer
Evmos | evmos_9001-2 | uevmos | CosmosHub | Channel-3 | Transfer
Evmos | evmos_9001-2 | uevmos | Osmosis | Channel-0 | Transfer
Injective | injective-1 | uxprt | Osmosis | Channel-8 | Transfer
Injective | injective-1 | uxprt | Juno | Channel-78 | Transfer
Injective | injective-1 | uxprt | Bandchain | Channel-3 | Oracle
Bandchain | laozi-mainnet | uband | Injective | Channel-7 | Oracle
Persistence | core-1 | uxprt | Osmosis | Channel-4 | Transfer
Persistence | core-1 | uxprt | Osmosis | Channel-4 | ICA


## Relayer Addresses

Network | StakeWithUs Relayer Address
------- | ---------------------------
CosmosHub | [cosmos1av54qcmavhjkqsd67cf6f4cedqjrdeh7ed86fc](https://www.mintscan.io/cosmos/account/cosmos1av54qcmavhjkqsd67cf6f4cedqjrdeh7ed86fc "Cosmos Relayer Address")
EVMOS | [evmos15gxjl4m4e4p4yc986k350ml8f5ywjr76nu6vtc](https://www.mintscan.io/evmos/account/evmos15gxjl4m4e4p4yc986k350ml8f5ywjr76nu6vtc "EVMOS Relayer Address")
Osmosis | [osmo1av54qcmavhjkqsd67cf6f4cedqjrdeh73k52l2](https://www.mintscan.io/osmosis/account/osmo1av54qcmavhjkqsd67cf6f4cedqjrdeh73k52l2 "Osmosis Relayer Address")
Juno | [juno1av54qcmavhjkqsd67cf6f4cedqjrdeh70lypwy](https://www.mintscan.io/juno/account/juno1av54qcmavhjkqsd67cf6f4cedqjrdeh70lypwy "Juno Relayer Address")
Bandchain | [band1q5py62z4fq0kcfjj9u6rhgegaxqjd57w5cn87m](https://www.mintscan.io/band/account/band1q5py62z4fq0kcfjj9u6rhgegaxqjd57w5cn87m "Band Relayer Address")
Injective | [inj15gxjl4m4e4p4yc986k350ml8f5ywjr76m5uxrg](https://www.mintscan.io/injective/account/inj15gxjl4m4e4p4yc986k350ml8f5ywjr76m5uxrg "Injective Relayer Address")
Persistence | [persistence1rd2gwjk6cmvgxedl5gwcvhw8lt62wttyla65my](https://www.mintscan.io/persistence/account/persistence1rd2gwjk6cmvgxedl5gwcvhw8lt62wttyla65my "Persistence Relayer Address")
