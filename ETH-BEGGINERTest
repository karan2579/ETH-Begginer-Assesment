// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract TaralaviToken {
    // Public variables to store the details about the coin
    string public name = "TaralaviToken";
    string public symbol = "TTK";
    uint256 public totalUserSupply;

    // Mapping to store user balances
    mapping(address => uint256) public userBalances;

    // Mint function to increase total user supply and balance of a specified address
    function mint(address userAccount, uint256 amount) public {
        // Ensure a reasonable amount is minted
        if (amount > 0 && amount <= 10000) {
            totalUserSupply += amount;
            userBalances[userAccount] += amount;
        }
    }

    // Burn function to decrease total user supply and balance of a specified address
    function burn(address userAccount, uint256 amount) public {
        // Conditional to check if the balance is sufficient to burn
        if (amount > 0 && userBalances[userAccount] >= amount) {
            totalUserSupply -= amount;
            userBalances[userAccount] -= amount;
        }
    }
}
