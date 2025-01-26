# Understanding ERC Tokens

ERC tokens are standards for creating and managing tokens on the Ethereum blockchain. These tokens are governed by specific rules (or standards) to ensure compatibility with Ethereum-based applications. The most commonly used ERC token standards include **ERC-20**, **ERC-721**, and **ERC-1155**.

## ERC-20 Tokens: Fungible Tokens

ERC-20 is the most widely used Ethereum token standard. It defines a set of functions for creating **fungible tokens**—tokens that are identical and interchangeable (like cryptocurrencies or utility tokens).

### Key Functions of ERC-20:
- `totalSupply()`: Returns the total supply of tokens.
- `balanceOf(address)`: Returns the token balance of a given address.
- `transfer(address, uint256)`: Transfers tokens to a specified address.
- `approve(address, uint256)`: Approves another address to spend tokens on behalf of the sender.

### Sample ERC-20 Token Code:
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract MyERC20Token is ERC20 {
    constructor(uint256 initialSupply) ERC20("MyToken", "MTK") {
        _mint(msg.sender, initialSupply);
    }
}
```
### Sample ERC-721 Token Code
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC721/ERC721.sol";
import "@openzeppelin/contracts/utils/Counters.sol";

contract MyNFT is ERC721 {
    using Counters for Counters.Counter;
    Counters.Counter private _tokenIds;

    constructor() ERC721("MyNFT", "MNFT") {}

    function mintNFT(address recipient) public returns (uint256) {
        _tokenIds.increment();
        uint256 newItemId = _tokenIds.current();
        _safeMint(recipient, newItemId);
        return newItemId;
    }
}
```
### ERC-1155 Tokens: Multi-Asset Tokens
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC1155/ERC1155.sol";

contract MyERC1155 is ERC1155 {
    constructor() ERC1155("https://myapi.com/api/token/{id}.json") {}

    function mint(address account, uint256 id, uint256 amount) public {
        _mint(account, id, amount, "");
    }
}
```
# Summary 
- `ERC-20`: Creates fungible tokens (identical, interchangeable). Used for cryptocurrencies, stablecoins, and DeFi.
- `ERC-721`: Creates non-fungible tokens (unique, non-interchangeable). Used for digital art, collectibles, and NFTs
- `ERC-1155`: Supports both fungible and non-fungible tokens within a single contract. Ideal for gaming and multi-asset ecosystems.
