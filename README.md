# curve-dao-contracts

Vyper contracts used in the [Curve](https://www.curve.finance/) Governance DAO.

## Overview

Curve DAO consists of multiple smart contracts connected by [Aragon](https://github.com/aragon/aragonOS). Interaction with Aragon occurs through a [modified implementation](https://github.com/curvefi/curve-aragon-voting) of the [Aragon Voting App](https://github.com/aragon/aragon-apps/tree/master/apps/voting). Aragon's standard one token, one vote method is replaced with a weighting system based on locking tokens. Curve DAO has a token (CRV) which is used for both governance and value accrual.

View the [documentation](https://resources.curve.finance/governance/overview/) for a more in-depth explanation of how Curve DAO works.

## Testing and Development

### Dependencies

- [python3](https://www.python.org/downloads/release/python-368/) version 3.6 or greater, python3-dev
- [vyper](https://github.com/vyperlang/vyper) version [0.2.4](https://github.com/vyperlang/vyper/releases/tag/v0.2.4)
- [brownie](https://github.com/iamdefinitelyahuman/brownie) - tested with version [1.14.6](https://github.com/eth-brownie/brownie/releases/tag/v1.14.6)
- [brownie-token-tester](https://github.com/iamdefinitelyahuman/brownie-token-tester) - tested with version [0.2.2](https://github.com/iamdefinitelyahuman/brownie-token-tester/releases/tag/v0.2.2)
- [ganache-cli](https://github.com/trufflesuite/ganache-cli) - tested with version [6.12.1](https://github.com/trufflesuite/ganache-cli/releases/tag/v6.12.1)

### Setup

To get started, first create and initialize a Python [virtual environment](https://docs.python.org/3/library/venv.html). Next, clone the repo and install the developer dependencies:

```bash
git clone https://github.com/curvefi/curve-dao-contracts.git
cd curve-dao-contracts
pip install -r requirements.txt
```

### Running the Tests

The test suite is split between [unit](tests/unitary) and [integration](tests/integration) tests. To run the entire suite:

```bash
brownie test
```

To run only the unit tests or integration tests:

```bash
brownie test tests/unitary
brownie test tests/integration
```

## Deployment

See the [deployment documentation](scripts/deployment/README.md) for detailed information on how to deploy Curve DAO.

## Audits and Security

Curve DAO contracts have been audited by Trail of Bits and Quantstamp. These audit reports are made available on the [Curve website](https://docs.curve.finance/security/security/#security-audits).

There is also an active [bug bounty](https://docs.curve.finance/security/security/#bug-bounty) for issues which can lead to substantial loss of money, critical bugs such as a broken live-ness condition, or irreversible loss of funds.

## Resources

You may find the following guides useful:

1. [Curve and Curve DAO Resources](https://resources.curve.finance/)
2. [How to earn and claim CRV](https://resources.curve.finance/vecrv/claiming-trading-fees/)
3. [Voting and vote locking on Curve DAO](https://resources.curve.finance/vecrv/overview/)

## Community

If you have any questions about this project, or wish to engage with us:

- [Telegram](https://t.me/curvefi)
- [Twitter](https://twitter.com/curvefinance)
- [Discord](https://discord.gg/rgrfS7W)

## License

This project is licensed under the [MIT](LICENSE) license.
