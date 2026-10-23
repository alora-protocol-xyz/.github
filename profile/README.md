<p align="center">
  <img src="https://raw.githubusercontent.com/alora-protocol-xyz/.github/main/profile/alora-lockup-white.png#gh-dark-mode-only" alt="Alora" width="320">
  <img src="https://raw.githubusercontent.com/alora-protocol-xyz/.github/main/profile/alora-lockup-black.png#gh-light-mode-only" alt="Alora" width="320">
</p>

# Alora Protocol

**A protocol for running tokenized funds onchain.**

A fund on Alora holds a basket of tokenized assets, issues a share token, and settles every creation and redemption onchain. A sponsor defines the fund's rules, a fund manager steers the portfolio inside them, approved trading firms create and redeem shares at net asset value (NAV), and investors hold and trade the shares.

## What Alora does

- **One record.** The fund keeps its share register and its holdings together, so the two always match and anyone can read both.
- **NAV at the moment of the trade.** Every creation and redemption is priced from current market prices and settles in kind, at that NAV.
- **Bounded trading.** The sponsor publishes a trade list. The fund manager trades only from that list, within size limits and above a price floor.
- **One fee.** A management fee accrues every second and is paid through NAV; a holder's share count stays the same.
- **Built for compliance.** Shares move only between addresses that passed KYC, and each fund applies the transfer restrictions its legal requirements call for.

## How a fund works

1. The **sponsor** configures a fund: price feeds, the fee rate and the trade list.
2. The **access manager** runs KYC on investors and authorized participants (APs) and lists their addresses.
3. The **fund manager** sets the creation and redemption baskets.
4. **APs** create shares by delivering the creation basket, and sell them on trading venues.
5. **Investors** buy shares on venues or from APs, hold them, and sell on venues to exit.
6. The **fund manager** rebalances from the trade list as the portfolio drifts.
7. The **fee** accrues every second and settles each period in shares.

## Security

- Roles are separated: the key that defines what a fund may trade, the key that trades, and the key that grants roles sit on different addresses.
- Every creation, redemption and trade passes its checks before it settles, or is cancelled in full.
- Alora's monitoring can pause a fund on any high-severity event; share transfers keep working.
- Every contract is upgradeable only through governance.
- Each fund's chain, addresses, audit and governance address are published in its deployment record.

## Links

- 🌐 Website: [aloraprotocol.xyz](https://aloraprotocol.xyz)
