# Stablecoin Threat Detection Kit


<p align="left">
    <img width=1200 alt="Stablecoin Threat Detection Kit Overview" src="../stablecoin-threat-detection-kit.png">
</p>

!!! important "Frequent Doc Updates"
    Forta will continue to add more curated security bots in the coming months, so stay tuned and come check this page frequently for new updates!

| Bot Name | Bot Details/Template Link | Bot Description  |
|----------|------------------|------------------|
| Alert Combiner | [Bot Details](starter-kit-bot-details.md#alert-combiner) | Combines past alerts under common adddress to emit a high precision alert. |
| Balance Decreases | Coming Soon | Identifies when the balance of an account decreases significantly. |
| Chainalysis Sanctioned Addresses | [Bot Details](starter-kit-bot-details.md#chainalysis-sanctioned-addresses) | Alerts when a Chainalysis sanctioned account interacts with the address monitored. |
| Events Monitor | [Template Link](https://github.com/arbitraryexecution/forta-bot-templates/tree/main/src/monitor-events) | Monitors blockchain transactions for specified events emitted from specified contract addresses. This template can be used to alert events emitted from functions that should only be callable by privileged roles. [USDT USDC Blocklist Events Monitor](https://github.com/forta-network/starter-kits/tree/main/stablecoin-blocklist-events-js#usdt-and-usdc-blacklist-related-events) used this template to monitor stablecoin providers' blocklists. To subscribe to this bot, please visit [this bot page](https://explorer.forta.network/agent/0x39c87864afec7637089be141e13cef943ef572961974b456f2be73bb4757e134) and click on "Subscribe to this bot". |
| Exploiter Addresses | [Bot Details](starter-kit-bot-details.md#exploiter-addresses) | Alerts when known exploiter address interacts with the address monitored. |
| Flash Loan Detector | [Bot Details](starter-kit-bot-details.md#evidence-of-phishing-bot) | Alerts when a flash loan results in large profits indicative of an attack |
| Function call with access control monitor | [Template Link](https://github.com/arbitraryexecution/forta-bot-templates/tree/main/src/monitor-function-calls) | Alerts on function calls that should only be callable by privileged roles.|
| Ice Phishing Detection Bot | [Bot Details](starter-kit-bot-details.md#evidence-of-phishing-bot) | Alerts when ice phishing (social engineer users into token approvals) for a token contract monitored. |
| Mint/Borrow Value Anomalies | [Bot Details](starter-kit-bot-details.md#mint-borrow-anomalies) | Alerts when mint/borrow volume is changing in a statistically significant way. |
| OpenZeppelin-Gnosis Safe Contract Events | [Bot Details](starter-kit-bot-details.md#openzeppelin-gnosis-safe-contract-events) | Alerts on security relevant events of the OZ contract library/ Gnosis Safe contact instances. |
| Price Change Anomalies | [Bot Details](starter-kit-bot-details.md#price-change-anomaly) | | Identifies when a price of an asset changes significantly. |
| Stablecoin interaction with DeFi protocols | Coming Soon | Identifies when stablecoin is used in DeFi protocols. |
| Successful transactions with internal failures | [Bot Details](starter-kit-bot-details.md#anomalous-transaction-volume) | Alerts on transactions involving the address monitored that succeed, but had internal failures.|
| Suspicious Contract Creation | [Bot Details](starter-kit-bot-details.md#suspicious-contract-creation) | Alerts on contract creation that contained the address monitored. |
| Tornado Cash Funded Account Interaction | [Bot Details](starter-kit-bot-details.md#tornado-cash-funded-account-interaction) | Alerts when a Tornado Cash funded account interacts with the address monitored. |
| Transaction Volume Anomalies | Coming Soon | Identifies whether transaction volume is changing in a statistically significant way. |
| Unverified Contract Creation | [Bot Details](starter-kit-bot-details.md#unverified-contract-creation) | Alerts on contract creation that isnt verified on Etherscan. |



