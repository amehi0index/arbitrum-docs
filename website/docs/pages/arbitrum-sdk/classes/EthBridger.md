---
id: "EthBridger"
title: "Class EthBridger"
sidebar_label: "EthBridger"
sidebar_position: 0
custom_edit_url: null
---

Bridger for moving ETH back and forth between L1 to L2

## Hierarchy

- `AssetBridger`\<`EthDepositParams` \| `EthDepositToParams` \| `L1ToL2TxReqAndSigner`, `EthWithdrawParams` \| `L2ToL1TxReqAndSigner`\>

  ↳ **`EthBridger`**

## Constructors

### constructor

• **new EthBridger**(`l2Network`): [`EthBridger`](EthBridger.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `l2Network` | [`L2Network`](../interfaces/L2Network.md) |

#### Returns

[`EthBridger`](EthBridger.md)

#### Inherited from

AssetBridger\<
  EthDepositParams \| EthDepositToParams \| L1ToL2TxReqAndSigner,
  EthWithdrawParams \| L2ToL1TxReqAndSigner
\>.constructor

#### Defined in

[src/lib/assetBridger/assetBridger.ts:37](https://github.com/OffchainLabs/arbitrum-sdk/blob/4d1c5a4e2/src/lib/assetBridger/assetBridger.ts#L37)

## Properties

### l1Network

• `Readonly` **l1Network**: [`L1Network`](../interfaces/L1Network.md)

#### Inherited from

AssetBridger.l1Network

#### Defined in

[src/lib/assetBridger/assetBridger.ts:35](https://github.com/OffchainLabs/arbitrum-sdk/blob/4d1c5a4e2/src/lib/assetBridger/assetBridger.ts#L35)

___

### l2Network

• `Readonly` **l2Network**: [`L2Network`](../interfaces/L2Network.md)

#### Inherited from

AssetBridger.l2Network

#### Defined in

[src/lib/assetBridger/assetBridger.ts:37](https://github.com/OffchainLabs/arbitrum-sdk/blob/4d1c5a4e2/src/lib/assetBridger/assetBridger.ts#L37)

## Methods

### checkL1Network

▸ **checkL1Network**(`sop`): `Promise`\<`void`\>

Check the signer/provider matches the l1Network, throws if not

#### Parameters

| Name | Type |
| :------ | :------ |
| `sop` | `SignerOrProvider` |

#### Returns

`Promise`\<`void`\>

#### Inherited from

AssetBridger.checkL1Network

#### Defined in

[src/lib/assetBridger/assetBridger.ts:50](https://github.com/OffchainLabs/arbitrum-sdk/blob/4d1c5a4e2/src/lib/assetBridger/assetBridger.ts#L50)

___

### checkL2Network

▸ **checkL2Network**(`sop`): `Promise`\<`void`\>

Check the signer/provider matches the l2Network, throws if not

#### Parameters

| Name | Type |
| :------ | :------ |
| `sop` | `SignerOrProvider` |

#### Returns

`Promise`\<`void`\>

#### Inherited from

AssetBridger.checkL2Network

#### Defined in

[src/lib/assetBridger/assetBridger.ts:58](https://github.com/OffchainLabs/arbitrum-sdk/blob/4d1c5a4e2/src/lib/assetBridger/assetBridger.ts#L58)

___

### deposit

▸ **deposit**(`params`): `Promise`\<`L1EthDepositTransaction`\>

Deposit ETH from L1 onto L2

#### Parameters

| Name | Type |
| :------ | :------ |
| `params` | `EthDepositParams` \| `L1ToL2TxReqAndSigner` |

#### Returns

`Promise`\<`L1EthDepositTransaction`\>

#### Overrides

AssetBridger.deposit

#### Defined in

[src/lib/assetBridger/ethBridger.ts:179](https://github.com/OffchainLabs/arbitrum-sdk/blob/4d1c5a4e2/src/lib/assetBridger/ethBridger.ts#L179)

___

### depositTo

▸ **depositTo**(`params`): `Promise`\<`L1ContractCallTransaction`\>

Deposit ETH from L1 onto a different L2 address

#### Parameters

| Name | Type |
| :------ | :------ |
| `params` | `EthDepositToParams` \| `L1ToL2TransactionRequest` & \{ `l1Signer`: `Signer` ; `overrides?`: `Overrides`  } & \{ `l2Provider`: `Provider`  } |

#### Returns

`Promise`\<`L1ContractCallTransaction`\>

#### Defined in

[src/lib/assetBridger/ethBridger.ts:231](https://github.com/OffchainLabs/arbitrum-sdk/blob/4d1c5a4e2/src/lib/assetBridger/ethBridger.ts#L231)

___

### getDepositRequest

▸ **getDepositRequest**(`params`): `Promise`\<`OmitTyped`\<`L1ToL2TransactionRequest`, ``"retryableData"``\>\>

Get a transaction request for an eth deposit

#### Parameters

| Name | Type |
| :------ | :------ |
| `params` | `EthDepositRequestParams` |

#### Returns

`Promise`\<`OmitTyped`\<`L1ToL2TransactionRequest`, ``"retryableData"``\>\>

#### Defined in

[src/lib/assetBridger/ethBridger.ts:149](https://github.com/OffchainLabs/arbitrum-sdk/blob/4d1c5a4e2/src/lib/assetBridger/ethBridger.ts#L149)

___

### getDepositToRequest

▸ **getDepositToRequest**(`params`): `Promise`\<`L1ToL2TransactionRequest`\>

Get a transaction request for an ETH deposit to a different L2 address using Retryables

#### Parameters

| Name | Type |
| :------ | :------ |
| `params` | `EthDepositToRequestParams` |

#### Returns

`Promise`\<`L1ToL2TransactionRequest`\>

#### Defined in

[src/lib/assetBridger/ethBridger.ts:204](https://github.com/OffchainLabs/arbitrum-sdk/blob/4d1c5a4e2/src/lib/assetBridger/ethBridger.ts#L204)

___

### getWithdrawalRequest

▸ **getWithdrawalRequest**(`params`): `Promise`\<`L2ToL1TransactionRequest`\>

Get a transaction request for an eth withdrawal

#### Parameters

| Name | Type |
| :------ | :------ |
| `params` | `EthWithdrawParams` |

#### Returns

`Promise`\<`L2ToL1TransactionRequest`\>

#### Defined in

[src/lib/assetBridger/ethBridger.ts:260](https://github.com/OffchainLabs/arbitrum-sdk/blob/4d1c5a4e2/src/lib/assetBridger/ethBridger.ts#L260)

___

### withdraw

▸ **withdraw**(`params`): `Promise`\<[`L2ContractTransaction`](../interfaces/L2ContractTransaction.md)\>

Withdraw ETH from L2 onto L1

#### Parameters

| Name | Type |
| :------ | :------ |
| `params` | `L2ToL1TxReqAndSigner` \| `EthWithdrawParams` & \{ `l2Signer`: `Signer`  } |

#### Returns

`Promise`\<[`L2ContractTransaction`](../interfaces/L2ContractTransaction.md)\>

#### Overrides

AssetBridger.withdraw

#### Defined in

[src/lib/assetBridger/ethBridger.ts:290](https://github.com/OffchainLabs/arbitrum-sdk/blob/4d1c5a4e2/src/lib/assetBridger/ethBridger.ts#L290)

___

### fromProvider

▸ **fromProvider**(`l2Provider`): `Promise`\<[`EthBridger`](EthBridger.md)\>

Instantiates a new EthBridger from an L2 Provider

#### Parameters

| Name | Type |
| :------ | :------ |
| `l2Provider` | `Provider` |

#### Returns

`Promise`\<[`EthBridger`](EthBridger.md)\>

#### Defined in

[src/lib/assetBridger/ethBridger.ts:140](https://github.com/OffchainLabs/arbitrum-sdk/blob/4d1c5a4e2/src/lib/assetBridger/ethBridger.ts#L140)