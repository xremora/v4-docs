[@pooltogether/v4-client-js](../) / [Exports](../modules) / PrizePoolNetwork

# Class: PrizePoolNetwork

A Prize Pool Network.
The network consists of one or more Prize Pools and Prize Distributors. PrizePoolNetwork provides read only functions for reading data from the contracts that make up the network. Initializes several PrizePools and PrizeDistributors on creation.

## Table of contents

### Constructors

- [constructor](PrizePoolNetwork#constructor)

### Properties

- [beaconAddress](PrizePoolNetwork#beaconaddress)
- [beaconChainId](PrizePoolNetwork#beaconchainid)
- [contractList](PrizePoolNetwork#contractlist)
- [drawBeaconContract](PrizePoolNetwork#drawbeaconcontract)
- [drawBeaconMetadata](PrizePoolNetwork#drawbeaconmetadata)
- [drawBufferContract](PrizePoolNetwork#drawbuffercontract)
- [drawBufferMetadata](PrizePoolNetwork#drawbuffermetadata)
- [prizeDistributors](PrizePoolNetwork#prizedistributors)
- [prizePools](PrizePoolNetwork#prizepools)
- [prizeTierHistoryContract](PrizePoolNetwork#prizetierhistorycontract)
- [prizeTierHistoryMetadata](PrizePoolNetwork#prizetierhistorymetadata)
- [providers](PrizePoolNetwork#providers)

### Methods

- [getBeaconChainDrawIds](PrizePoolNetwork#getbeaconchaindrawids)
- [getBeaconChainDraws](PrizePoolNetwork#getbeaconchaindraws)
- [getDrawBeaconPeriod](PrizePoolNetwork#getdrawbeaconperiod)
- [getPrizeDistributor](PrizePoolNetwork#getprizedistributor)
- [getPrizePool](PrizePoolNetwork#getprizepool)
- [getUpcomingPrizeTier](PrizePoolNetwork#getupcomingprizetier)
- [getUsersPrizePoolBalances](PrizePoolNetwork#getusersprizepoolbalances)
- [id](PrizePoolNetwork#id)

## Constructors

### constructor

• **new PrizePoolNetwork**(`providers`, `prizePoolNetworkContractList`)

Create an instance of a PrizePoolNetwork by providing ethers Providers for each relevant network and a Contract List.

#### Parameters

| Name                           | Type                                         | Description                                                                           |
| :----------------------------- | :------------------------------------------- | :------------------------------------------------------------------------------------ |
| `providers`                    | [`Providers`](../interfaces/Providers)       | ethers Providers for each network in the Prize Pool Network, keyed by their chain id. |
| `prizePoolNetworkContractList` | [`ContractList`](../interfaces/ContractList) | a Contract List containing all of the relevant metadata for the Prize Pool Network.   |

#### Defined in

[src/PrizePoolNetwork.ts:41](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L41)

## Properties

### beaconAddress

• `Readonly` **beaconAddress**: `string`

#### Defined in

[src/PrizePoolNetwork.ts:23](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L23)

---

### beaconChainId

• `Readonly` **beaconChainId**: `number`

#### Defined in

[src/PrizePoolNetwork.ts:22](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L22)

---

### contractList

• `Readonly` **contractList**: [`ContractList`](../interfaces/ContractList)

#### Defined in

[src/PrizePoolNetwork.ts:19](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L19)

---

### drawBeaconContract

• `Readonly` **drawBeaconContract**: `Contract`

#### Defined in

[src/PrizePoolNetwork.ts:31](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L31)

---

### drawBeaconMetadata

• `Readonly` **drawBeaconMetadata**: [`Contract`](../interfaces/Contract)

#### Defined in

[src/PrizePoolNetwork.ts:26](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L26)

---

### drawBufferContract

• `Readonly` **drawBufferContract**: `Contract`

#### Defined in

[src/PrizePoolNetwork.ts:32](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L32)

---

### drawBufferMetadata

• `Readonly` **drawBufferMetadata**: [`Contract`](../interfaces/Contract)

#### Defined in

[src/PrizePoolNetwork.ts:27](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L27)

---

### prizeDistributors

• `Readonly` **prizeDistributors**: [`PrizeDistributor`](PrizeDistributor)[]

#### Defined in

[src/PrizePoolNetwork.ts:18](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L18)

---

### prizePools

• `Readonly` **prizePools**: [`PrizePool`](PrizePool)[]

#### Defined in

[src/PrizePoolNetwork.ts:17](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L17)

---

### prizeTierHistoryContract

• `Readonly` **prizeTierHistoryContract**: `Contract`

#### Defined in

[src/PrizePoolNetwork.ts:33](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L33)

---

### prizeTierHistoryMetadata

• `Readonly` **prizeTierHistoryMetadata**: [`Contract`](../interfaces/Contract)

#### Defined in

[src/PrizePoolNetwork.ts:28](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L28)

---

### providers

• `Readonly` **providers**: [`Providers`](../interfaces/Providers)

#### Defined in

[src/PrizePoolNetwork.ts:16](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L16)

## Methods

### getBeaconChainDrawIds

▸ **getBeaconChainDrawIds**(): `Promise`<`number`[]\>

Fetch the range of available draw ids in the Draw Buffer for the beacon Prize Pool.

#### Returns

`Promise`<`number`[]\>

an array of draw ids

#### Defined in

[src/PrizePoolNetwork.ts:143](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L143)

---

### getBeaconChainDraws

▸ **getBeaconChainDraws**(): `Promise`<{ [drawId: number]: [`Draw`](../interfaces/Draw); }\>

Fetch all of the available Draws in the Draw Buffer for the beacon Prize Pool.

#### Returns

`Promise`<{ [drawId: number]: [`Draw`](../interfaces/Draw); }\>

an object of draws keyed by their draw id

#### Defined in

[src/PrizePoolNetwork.ts:168](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L168)

---

### getDrawBeaconPeriod

▸ **getDrawBeaconPeriod**(): `Promise`<{ `drawId`: `number` ; `endsAtSeconds`: `BigNumber` ; `periodSeconds`: `number` ; `startedAtSeconds`: `BigNumber` }\>

Fetch the current Draw Beacon period data from the beacon Prize Pool.

#### Returns

`Promise`<{ `drawId`: `number` ; `endsAtSeconds`: `BigNumber` ; `periodSeconds`: `number` ; `startedAtSeconds`: `BigNumber` }\>

the current draw beacon period.

#### Defined in

[src/PrizePoolNetwork.ts:121](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L121)

---

### getPrizeDistributor

▸ **getPrizeDistributor**(`chainId`, `address`): `undefined` \| [`PrizeDistributor`](PrizeDistributor)

Returns a PrizeDistributor from the list of Prize Distributors that was created on initialization by their primary key. The primary key of a Prize Disctributor is the chain id it is on and the address of the PrizeDistributor contract.

#### Parameters

| Name      | Type     | Description                                        |
| :-------- | :------- | :------------------------------------------------- |
| `chainId` | `number` | the chain id the requested prize distributor is on |
| `address` | `string` | the address of the PrizeDistributor contract       |

#### Returns

`undefined` \| [`PrizeDistributor`](PrizeDistributor)

#### Defined in

[src/PrizePoolNetwork.ts:218](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L218)

---

### getPrizePool

▸ **getPrizePool**(`chainId`, `address`): `undefined` \| [`PrizePool`](PrizePool)

Returns a PrizePool from the list of Prize Pools that was created on initialization by their primary key. The primary key of a Prize Pool is the chain id it is on and the address of the YieldSourcePrizePool contract.

#### Parameters

| Name      | Type     | Description                                      |
| :-------- | :------- | :----------------------------------------------- |
| `chainId` | `number` | the chain id the requested prize pool is on      |
| `address` | `string` | the address of the YieldSourcePrizePool contract |

#### Returns

`undefined` \| [`PrizePool`](PrizePool)

#### Defined in

[src/PrizePoolNetwork.ts:206](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L206)

---

### getUpcomingPrizeTier

▸ **getUpcomingPrizeTier**(): `Promise`<[`PrizeTier`](../modules#prizetier)\>

Fetches the upcoming prize tier data from the prize tier history contract. This data is used for the next prize distribution that will be added to the Prize Distribution Buffer for the beacon Prize Pool.

#### Returns

`Promise`<[`PrizeTier`](../modules#prizetier)\>

the upcoming prize tier

#### Defined in

[src/PrizePoolNetwork.ts:188](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L188)

---

### getUsersPrizePoolBalances

▸ **getUsersPrizePoolBalances**(`usersAddress`): `Promise`<{ `address`: `string` = prizePool.address; `balances`: [`PrizePoolTokenBalances`](../interfaces/PrizePoolTokenBalances) ; `chainId`: `number` = prizePool.chainId }[]\>

Fetch the users balances for all relevant tokens for all Prize Pools in the Prize Pool Network.

#### Parameters

| Name           | Type     | Description                  |
| :------------- | :------- | :--------------------------- |
| `usersAddress` | `string` | address to get balances for. |

#### Returns

`Promise`<{ `address`: `string` = prizePool.address; `balances`: [`PrizePoolTokenBalances`](../interfaces/PrizePoolTokenBalances) ; `chainId`: `number` = prizePool.chainId }[]\>

an array of objects containing the chain id & Prize Pool address and a balances object with the users balances for relevant tokens to the prize pool

#### Defined in

[src/PrizePoolNetwork.ts:105](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L105)

---

### id

▸ **id**(): `string`

Returns a unique id string for this PrizePoolNetwork.

#### Returns

`string`

a unique id for the PrizePoolNetwork

#### Defined in

[src/PrizePoolNetwork.ts:94](https://github.com/pooltogether/v4-client-js/blob/d352428/src/PrizePoolNetwork.ts#L94)
