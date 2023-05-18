# Metacrafters
DEPLOYED ON POLYGON MUMBAI
# MyToken Contract

This contract is a simple implementation of a token contract in Solidity. It includes functionalities for minting and burning tokens, as well as storing token details.

## Contract Details

### Public Variables

- `tokenName`: A string variable representing the name of the token (e.g., "MUDASSIR").
- `tokenAbbr`: A string variable representing the abbreviation of the token (e.g., "MUDS").
- `totalSupply`: An unsigned integer variable representing the total supply of tokens.

### Mapping Variable

- `balances`: A mapping that associates addresses with their token balances. It maps addresses to unsigned integer values.

### Mint Function

The `mint` function is used to create new tokens. It takes two parameters: `_address` (the address to which the tokens will be assigned) and `_value` (the amount of tokens to be created). The function increases the total supply by the specified `_value` and increments the balance of the `_address` by the same amount.

### Burn Function

The `burn` function is used to destroy existing tokens. It takes two parameters: `_address` (the address from which the tokens will be burned) and `_value` (the amount of tokens to be burned). The function checks if the balance of the `_address` is greater than or equal to the specified `_value`. If the condition is met, it deducts the `_value` from the total supply and reduces the balance of the `_address` by the same amount.

It's worth noting that the `burn` function does not revert if the condition is not met (i.e., the balance is insufficient). This means that calling the `burn` function with an amount that exceeds the balance will simply have no effect.

## License

This contract is released under the MIT License.
