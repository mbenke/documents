# SIMPLE POLL

The objective of this task is to implement a simple poll using blockchain technology.

Flow should look like that:

- Contract admin defines topic of a poll
- Contract admin opens adding options to a poll
- Users can add up to 5 options
- Contract admin closes adding options to a poll
- Contract admin starts voting
- Users can vote
- Contract admin finishes voting
- Users can get votes stats

Please implement smart contract with following features:

1. **DefineQuestion**

   Can be called only by whitelisted addresses.

   Sets the topic of a poll.

   Can be called only when there is no running poll.

1. **AllowAddingOptions**

   Can be called only by whitelisted addresses.

   Users are now allowed to add options.

1. **DisallowAddingOptions**

   Can be called only by whitelisted addresses.

   Users are now disallowed to add options.

1. **AddOption**

   Everyone can call this function.

   User need to lock 50 GLM in contract to add poll option (expressed as string)

   Maximum number of options is 5. If it is reached before _DisallowAddingOptions_ has been called method take no effect.

1. **StartVoting**

   Can be called only by whitelisted addresses.

   Disallows adding options.

   Voting can be done now.

1. **Vote**

   Everyone can call this function.

   It should cost 1 GLMs to vote. Those funds are not returned after voting.

   Every address can vote only once.

1. **FinishVoting**

   Can be called only by whitelisted addresses.

   Transfers funds gathered from voting to caller’s address.

1. **Claim**

   Can be called only by users who added options and locked their funds in a contract.

   Can be called only after voting has been finished.

   If caller has some funds locked in a contract this method should transfer them back to his address.

1. **Reset**

   stops voting, disallows adding options, clears all options and votes, clears question

Smart contract should be implemented using solidity. Using additional libraries like OpenZeppelin is absolutely ok.

# Deployment

Deploy smart contract on Polygon’s Mumbai. Provide simple application (js, python, c#, java, rust …) demonstrating interactions with smart contract.

Please upload source code of smart contract and aforementioned application to a github repository.

# Demo

Please provide readme file with instructions how your code can be run and tested.

Attach additional file with description of several test scenarios.

\
_Optional_

If that's possible please record a short demonstration video showcasing your code and it's usage.

# Miscellaneous

_GLM token on Mumbai testnet_
https://mumbai.polygonscan.com/token/0x2036807B0B3aaf5b1858EE822D0e111fDdac7018
