# Game 0

When we talking about game zero, it is not a game but it is give instruction how to play game and it introduces all the things of solidity what's thing used in game and when use.And also given instructions about metamask because it is very important for game.

# Fallback

The donate function in the given code snippet was used to add 1 wei to the contract. Based on the contribution amounts, the owner was then checked and updated. A 1 wei transaction was sent using the sendTransaction function, and since your donation was greater than the previous owner's, ownership was changed. The full contract balance was then withdrawn by using the withdraw function, which was only available to the owner because of the onlyOwner modifier. By limiting withdrawal ability to the specified owner, this approach ensures secure fund management by preventing unauthorised access to contract money.


# Fal1out

I started by running the Fal1out function to engage with the Fallout smart contract.The contract should have a sendAllocation function modifier, similar to the onlyOwner modifier, to ensure that only the allocator may withdraw their funds. putting require(msg.sender == allocator, "caller is not the allocator"); before the allocator.And in this contract openzeppelin also given wrong. This error could be fixed by using the transfer(allocations[allocator]); statement.