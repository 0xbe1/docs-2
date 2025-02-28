# Maintaining your bot

## Verifying bot health

When your bot is published **and picked up by a scan node**, you can view the findings it generates using [Forta Explorer](https://explorer.forta.network/). You can filter findings using your bot ID (which looks like a SHA-256 hash e.g. `0x855b1556a45637abf05c63407437f6f305b4627c4361fb965a78e5731999c0c7`) using the search bar near the top of the page.

Also, you can verify that your bot is healthy by visiting the bot status page on Forta Explorer. The URL for this page looks like `https://explorer.forta.network/agent/YOUR_AGENT_ID`. You can see various information about the bot including how many transactions it processed, the different severities of alerts it produced and how long it took to respond to requests.

## Viewing bot logs

If [logging is enabled](deploying.md#enable-logging-optional), bot logs are updated by scan nodes every minute. You can fetch the latest logs from `https://api.forta.network/logs/agents/YOUR_AGENT_ID`. Only logs from the past 30 days are stored. To enable JSON format responses, you can specify the `Accept: application/json` header in your request. If you would like to integrate an existing error monitoring tool, check out the [error monitoring pattern](error-monitoring.md).

By default, the logs API will return the most recent logs but you can query previous logs using the `minute` query param. By specifying a minute in RFC3339 format (e.g. `https://api.forta.network/logs/agents/YOUR_AGENT_ID?minute=2019-10-12T07:20:50.52Z`), you can view previous logs. Note that not every minute may have logs.

## Disabling/enabling your bot

If you will not be using the alerts your bot generates (i.e. you were just testing out Forta, which we encourage), we ask that you please disable the bot. You can use [Forta App](https://app.forta.network/) or the CLI to enable or disable your bot. In Forta App, go to the My Agents page (from the menu at the top right) and click on the options menu to the right of your bot. From the options menu, you can choose to disable or enable your bot.

You can also use the CLI command `npm run disable`. Just make sure to set the `agentId` property in your **project folder's** forta.config.json before running the command (you should create the forta.config.json if it doesn't exist). You will also need to ensure you have Polygon MATIC tokens in your keyfile address to execute the disable transaction (you can get the keyfile address using `npm run keyfile`). See [this guide](matic.md) on how to acquire Polygon MATIC tokens. Similarly, you can re-enable a disabled bot using `npm run enable`.


## Updating your bot

You may want to update the code for your bot from time to time (e.g. if you found a bug, or there is a new scenario you want to detect). You can use [Forta App](https://app.forta.network/) or the CLI to update your bot. In Forta App, go to the My Agents page (from the menu at the top right) and click on the options menu to the right of your bot. From the options menu, you can choose to edit your bot.

You can also use the CLI command `npm run publish` to update your bot. If you have already deployed a bot, the CLI will know to update the existing bot. Ensure that the keyfile used for updating is the same one you used for creating the bot. Make sure to set the `agentId` property in your **project folder's** forta.config.json before running the command (you should create the forta.config.json if it doesn't exist). You will also need to ensure you have Polygon MATIC tokens in your keyfile address to execute the update transaction (you can get the keyfile address using `npm run keyfile`). See [this guide](matic.md) on how to acquire Polygon MATIC tokens.

