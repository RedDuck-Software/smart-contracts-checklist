# smart-contracts-checklist

All options should be either checked or crossed out (if option does'nt meet project requirements)

### For small 1-2 contracts project with owner permissions
- [ ] Should be upgradeable (if there is no requirement for decentralization or if the contract is not supposed to hold any funds)
- [ ] Should have withdraw ERC20/ETH functions for onlyOwner

If contract dont have to held eth/erc20 on it's balance
- [ ] Transfer out all the balances remainders
- [ ] Require that balances before and after the transaction are equal
- [ ] Property based tests for all options above

### For all projects

Contracts usage
- [ ] Aware of 3rd party audits for all contract that we used

Tests
- [ ] Property based tests for all contract's state and functions
- [ ] 95%+ total test coverage

Static analyzers
- [ ] Slither's analysis does'nt contain any critical issues

Deployment
- [ ] No deployment configuration hardcode
- [ ] `wighawag/hardhat-deploy` for non upgradeable smart contracts
- [ ] Hardhat's scripts or tasks and `@openzeppelin/hardhat-upgrades` for upgradeable smart contracts
