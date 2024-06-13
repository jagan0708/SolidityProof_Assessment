# SolidityProof_Assessment
Here's a simple `README.md` file to explain the functionality of your Solidity contract:

---

# MyToken Contract

This Solidity contract defines a basic ERC20-like token with minting and burning capabilities. Below are the details and functionalities provided by the contract:

## Contract Details

- **Token Name:** Dollar
- **Token Abbreviation:** Dlr
- **Total Supply:** 0 (initially)

## Public Variables

- `string public tokenName`: Stores the name of the token.
- `string public abbr`: Stores the abbreviation of the token.
- `uint public totalSupply`: Stores the total supply of the token.

## Mapping

- `mapping(address => uint) public balances`: This mapping keeps track of the balances of different addresses.

## Functions

### `mint(address _address, uint _value)`

This function increases the total supply of the token and the balance of the specified address.

- **Parameters:**
  - `_address`: The address to which the tokens will be minted.
  - `_value`: The number of tokens to mint.

### `burn(address _address, uint _value)`

This function decreases the total supply of the token and the balance of the specified address. It ensures that the address has enough tokens to burn.

- **Parameters:**
  - `_address`: The address from which the tokens will be burned.
  - `_value`: The number of tokens to burn.
    
- **Condition:**
  - The function requires that the balance of the `_address` is greater than or equal to `_value`.

## Usage

1. **Minting Tokens:**
   - Call the `mint` function with the desired address and token amount.
   - This increases the total supply and the balance of the specified address.

2. **Burning Tokens:**
   - Call the `burn` function with the desired address and token amount.
   - This decreases the total supply and the balance of the specified address, ensuring sufficient balance before burning.
 
  ## License

This contract is licensed under the MIT License. 
