# GovernorCompatibilityBravo







*Compatibility layer that implements GovernorBravo compatibility on to of {Governor}. This compatibility layer includes a voting system and requires a {IGovernorTimelock} compatible module to be added through inheritance. It does not include token bindings, not does it include any variable upgrade patterns. NOTE: When using this module, you may need to enable the Solidity optimizer to avoid hitting the contract size limit. _Available since v4.3._*

## Methods

### BALLOT_TYPEHASH

```solidity
function BALLOT_TYPEHASH() external view returns (bytes32)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes32 | undefined |

### COUNTING_MODE

```solidity
function COUNTING_MODE() external pure returns (string)
```

module:voting

*A description of the possible `support` values for {castVote} and the way these votes are counted, meant to be consumed by UIs to show correct vote options and interpret the results. The string is a URL-encoded sequence of key-value pairs that each describe one aspect, for example `support=bravo&amp;quorum=for,abstain`. There are 2 standard keys: `support` and `quorum`. - `support=bravo` refers to the vote options 0 = Against, 1 = For, 2 = Abstain, as in `GovernorBravo`. - `quorum=bravo` means that only For votes are counted towards quorum. - `quorum=for,abstain` means that both For and Abstain votes are counted towards quorum. If a counting module makes use of encoded `params`, it should  include this under a `params` key with a unique name that describes the behavior. For example: - `params=fractional` might refer to a scheme where votes are divided fractionally between for/against/abstain. - `params=erc721` might refer to a scheme where specific NFTs are delegated to vote. NOTE: The string can be decoded by the standard https://developer.mozilla.org/en-US/docs/Web/API/URLSearchParams[`URLSearchParams`] JavaScript class.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | string | undefined |

### EXTENDED_BALLOT_TYPEHASH

```solidity
function EXTENDED_BALLOT_TYPEHASH() external view returns (bytes32)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes32 | undefined |

### cancel

```solidity
function cancel(uint256 proposalId) external nonpayable
```



*Cancels a proposal only if sender is the proposer, or proposer delegates dropped below proposal threshold.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |

### castVote

```solidity
function castVote(uint256 proposalId, uint8 support) external nonpayable returns (uint256)
```



*See {IGovernor-castVote}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |
| support | uint8 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### castVoteBySig

```solidity
function castVoteBySig(uint256 proposalId, uint8 support, uint8 v, bytes32 r, bytes32 s) external nonpayable returns (uint256)
```



*See {IGovernor-castVoteBySig}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |
| support | uint8 | undefined |
| v | uint8 | undefined |
| r | bytes32 | undefined |
| s | bytes32 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### castVoteWithReason

```solidity
function castVoteWithReason(uint256 proposalId, uint8 support, string reason) external nonpayable returns (uint256)
```



*See {IGovernor-castVoteWithReason}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |
| support | uint8 | undefined |
| reason | string | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### castVoteWithReasonAndParams

```solidity
function castVoteWithReasonAndParams(uint256 proposalId, uint8 support, string reason, bytes params) external nonpayable returns (uint256)
```



*See {IGovernor-castVoteWithReasonAndParams}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |
| support | uint8 | undefined |
| reason | string | undefined |
| params | bytes | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### castVoteWithReasonAndParamsBySig

```solidity
function castVoteWithReasonAndParamsBySig(uint256 proposalId, uint8 support, string reason, bytes params, uint8 v, bytes32 r, bytes32 s) external nonpayable returns (uint256)
```



*See {IGovernor-castVoteWithReasonAndParamsBySig}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |
| support | uint8 | undefined |
| reason | string | undefined |
| params | bytes | undefined |
| v | uint8 | undefined |
| r | bytes32 | undefined |
| s | bytes32 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### execute

```solidity
function execute(address[] targets, uint256[] values, bytes[] calldatas, bytes32 descriptionHash) external payable returns (uint256)
```



*See {IGovernor-execute}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| targets | address[] | undefined |
| values | uint256[] | undefined |
| calldatas | bytes[] | undefined |
| descriptionHash | bytes32 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### execute

```solidity
function execute(uint256 proposalId) external payable
```



*See {IGovernorCompatibilityBravo-execute}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |

### getActions

```solidity
function getActions(uint256 proposalId) external view returns (address[] targets, uint256[] values, string[] signatures, bytes[] calldatas)
```



*See {IGovernorCompatibilityBravo-getActions}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| targets | address[] | undefined |
| values | uint256[] | undefined |
| signatures | string[] | undefined |
| calldatas | bytes[] | undefined |

### getReceipt

```solidity
function getReceipt(uint256 proposalId, address voter) external view returns (struct IGovernorCompatibilityBravo.Receipt)
```



*See {IGovernorCompatibilityBravo-getReceipt}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |
| voter | address | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | IGovernorCompatibilityBravo.Receipt | undefined |

### getVotes

```solidity
function getVotes(address account, uint256 blockNumber) external view returns (uint256)
```



*See {IGovernor-getVotes}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| account | address | undefined |
| blockNumber | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### getVotesWithParams

```solidity
function getVotesWithParams(address account, uint256 blockNumber, bytes params) external view returns (uint256)
```



*See {IGovernor-getVotesWithParams}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| account | address | undefined |
| blockNumber | uint256 | undefined |
| params | bytes | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### hasVoted

```solidity
function hasVoted(uint256 proposalId, address account) external view returns (bool)
```



*See {IGovernor-hasVoted}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |
| account | address | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### hashProposal

```solidity
function hashProposal(address[] targets, uint256[] values, bytes[] calldatas, bytes32 descriptionHash) external pure returns (uint256)
```



*See {IGovernor-hashProposal}. The proposal id is produced by hashing the ABI encoded `targets` array, the `values` array, the `calldatas` array and the descriptionHash (bytes32 which itself is the keccak256 hash of the description string). This proposal id can be produced from the proposal data which is part of the {ProposalCreated} event. It can even be computed in advance, before the proposal is submitted. Note that the chainId and the governor address are not part of the proposal id computation. Consequently, the same proposal (with same operation and same description) will have the same id if submitted on multiple governors across multiple networks. This also means that in order to execute the same operation twice (on the same governor) the proposer will have to change the description in order to avoid proposal id conflicts.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| targets | address[] | undefined |
| values | uint256[] | undefined |
| calldatas | bytes[] | undefined |
| descriptionHash | bytes32 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### name

```solidity
function name() external view returns (string)
```



*See {IGovernor-name}.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | string | undefined |

### onERC1155BatchReceived

```solidity
function onERC1155BatchReceived(address, address, uint256[], uint256[], bytes) external nonpayable returns (bytes4)
```



*See {IERC1155Receiver-onERC1155BatchReceived}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |
| _1 | address | undefined |
| _2 | uint256[] | undefined |
| _3 | uint256[] | undefined |
| _4 | bytes | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes4 | undefined |

### onERC1155Received

```solidity
function onERC1155Received(address, address, uint256, uint256, bytes) external nonpayable returns (bytes4)
```



*See {IERC1155Receiver-onERC1155Received}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |
| _1 | address | undefined |
| _2 | uint256 | undefined |
| _3 | uint256 | undefined |
| _4 | bytes | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes4 | undefined |

### onERC721Received

```solidity
function onERC721Received(address, address, uint256, bytes) external nonpayable returns (bytes4)
```



*See {IERC721Receiver-onERC721Received}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |
| _1 | address | undefined |
| _2 | uint256 | undefined |
| _3 | bytes | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bytes4 | undefined |

### proposalDeadline

```solidity
function proposalDeadline(uint256 proposalId) external view returns (uint256)
```



*See {IGovernor-proposalDeadline}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### proposalEta

```solidity
function proposalEta(uint256 proposalId) external view returns (uint256)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### proposalSnapshot

```solidity
function proposalSnapshot(uint256 proposalId) external view returns (uint256)
```



*See {IGovernor-proposalSnapshot}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### proposalThreshold

```solidity
function proposalThreshold() external view returns (uint256)
```



*Part of the Governor Bravo&#39;s interface: _&quot;The number of votes required in order for a voter to become a proposer&quot;_.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### proposals

```solidity
function proposals(uint256 proposalId) external view returns (uint256 id, address proposer, uint256 eta, uint256 startBlock, uint256 endBlock, uint256 forVotes, uint256 againstVotes, uint256 abstainVotes, bool canceled, bool executed)
```



*See {IGovernorCompatibilityBravo-proposals}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| id | uint256 | undefined |
| proposer | address | undefined |
| eta | uint256 | undefined |
| startBlock | uint256 | undefined |
| endBlock | uint256 | undefined |
| forVotes | uint256 | undefined |
| againstVotes | uint256 | undefined |
| abstainVotes | uint256 | undefined |
| canceled | bool | undefined |
| executed | bool | undefined |

### propose

```solidity
function propose(address[] targets, uint256[] values, bytes[] calldatas, string description) external nonpayable returns (uint256)
```



*See {IGovernor-propose}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| targets | address[] | undefined |
| values | uint256[] | undefined |
| calldatas | bytes[] | undefined |
| description | string | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### propose

```solidity
function propose(address[] targets, uint256[] values, string[] signatures, bytes[] calldatas, string description) external nonpayable returns (uint256)
```



*See {IGovernorCompatibilityBravo-propose}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| targets | address[] | undefined |
| values | uint256[] | undefined |
| signatures | string[] | undefined |
| calldatas | bytes[] | undefined |
| description | string | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### queue

```solidity
function queue(address[] targets, uint256[] values, bytes[] calldatas, bytes32 descriptionHash) external nonpayable returns (uint256 proposalId)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| targets | address[] | undefined |
| values | uint256[] | undefined |
| calldatas | bytes[] | undefined |
| descriptionHash | bytes32 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |

### queue

```solidity
function queue(uint256 proposalId) external nonpayable
```



*See {IGovernorCompatibilityBravo-queue}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |

### quorum

```solidity
function quorum(uint256 blockNumber) external view returns (uint256)
```

module:user-config

*Minimum number of cast voted required for a proposal to be successful. Note: The `blockNumber` parameter corresponds to the snapshot used for counting vote. This allows to scale the quorum depending on values such as the totalSupply of a token at this block (see {ERC20Votes}).*

#### Parameters

| Name | Type | Description |
|---|---|---|
| blockNumber | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### quorumVotes

```solidity
function quorumVotes() external view returns (uint256)
```



*See {IGovernorCompatibilityBravo-quorumVotes}.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### relay

```solidity
function relay(address target, uint256 value, bytes data) external payable
```



*Relays a transaction or function call to an arbitrary target. In cases where the governance executor is some contract other than the governor itself, like when using a timelock, this function can be invoked in a governance proposal to recover tokens or Ether that was sent to the governor contract by mistake. Note that if the executor is simply the governor itself, use of `relay` is redundant.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| target | address | undefined |
| value | uint256 | undefined |
| data | bytes | undefined |

### state

```solidity
function state(uint256 proposalId) external view returns (enum IGovernor.ProposalState)
```



*See {IGovernor-state}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId | uint256 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | enum IGovernor.ProposalState | undefined |

### supportsInterface

```solidity
function supportsInterface(bytes4 interfaceId) external view returns (bool)
```



*See {IERC165-supportsInterface}.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| interfaceId | bytes4 | undefined |

#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | bool | undefined |

### timelock

```solidity
function timelock() external view returns (address)
```






#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | address | undefined |

### version

```solidity
function version() external view returns (string)
```



*See {IGovernor-version}.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | string | undefined |

### votingDelay

```solidity
function votingDelay() external view returns (uint256)
```

module:user-config

*Delay, in number of block, between the proposal is created and the vote starts. This can be increassed to leave time for users to buy voting power, or delegate it, before the voting of a proposal starts.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |

### votingPeriod

```solidity
function votingPeriod() external view returns (uint256)
```

module:user-config

*Delay, in number of blocks, between the vote start and vote ends. NOTE: The {votingDelay} can delay the start of the vote. This must be considered when setting the voting duration compared to the voting delay.*


#### Returns

| Name | Type | Description |
|---|---|---|
| _0 | uint256 | undefined |



## Events

### ProposalCanceled

```solidity
event ProposalCanceled(uint256 proposalId)
```



*Emitted when a proposal is canceled.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId  | uint256 | undefined |

### ProposalCreated

```solidity
event ProposalCreated(uint256 proposalId, address proposer, address[] targets, uint256[] values, string[] signatures, bytes[] calldatas, uint256 startBlock, uint256 endBlock, string description)
```



*Emitted when a proposal is created.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId  | uint256 | undefined |
| proposer  | address | undefined |
| targets  | address[] | undefined |
| values  | uint256[] | undefined |
| signatures  | string[] | undefined |
| calldatas  | bytes[] | undefined |
| startBlock  | uint256 | undefined |
| endBlock  | uint256 | undefined |
| description  | string | undefined |

### ProposalExecuted

```solidity
event ProposalExecuted(uint256 proposalId)
```



*Emitted when a proposal is executed.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId  | uint256 | undefined |

### ProposalQueued

```solidity
event ProposalQueued(uint256 proposalId, uint256 eta)
```





#### Parameters

| Name | Type | Description |
|---|---|---|
| proposalId  | uint256 | undefined |
| eta  | uint256 | undefined |

### VoteCast

```solidity
event VoteCast(address indexed voter, uint256 proposalId, uint8 support, uint256 weight, string reason)
```



*Emitted when a vote is cast without params. Note: `support` values should be seen as buckets. Their interpretation depends on the voting module used.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| voter `indexed` | address | undefined |
| proposalId  | uint256 | undefined |
| support  | uint8 | undefined |
| weight  | uint256 | undefined |
| reason  | string | undefined |

### VoteCastWithParams

```solidity
event VoteCastWithParams(address indexed voter, uint256 proposalId, uint8 support, uint256 weight, string reason, bytes params)
```



*Emitted when a vote is cast with params. Note: `support` values should be seen as buckets. Their interpretation depends on the voting module used. `params` are additional encoded parameters. Their intepepretation also depends on the voting module used.*

#### Parameters

| Name | Type | Description |
|---|---|---|
| voter `indexed` | address | undefined |
| proposalId  | uint256 | undefined |
| support  | uint8 | undefined |
| weight  | uint256 | undefined |
| reason  | string | undefined |
| params  | bytes | undefined |



## Errors

### Empty

```solidity
error Empty()
```



*An operation (e.g. {front}) couldn&#39;t be completed due to the queue being empty.*



