# Plaid quickstart

This repository accompanies Plaid's [**quickstart guide**][quickstart].

Here you'll find full example integration apps using our [**client libraries**][libraries]:

- [Go][go-example]
- [Node][node-example]
- [Ruby][ruby-example]
- [Python][python-example]
- [Java][java-example]

If [docker][] is available to you, you can quickly spin up an example using: `% make QUICKSTART=go up`.
Be sure to have `PLAID_CLIENT_ID` and `PLAID_SECRET` defined in your environment or
replace the respective `${VARIABLES}` in the `x-environment` section in
[`docker-compose.yml`](/docker-compose.yml) directly.

To further adjust the quickstart to your use-case, you can define `PLAID_PRODUCTS`, `PLAID_COUNTRY_CODES`,
`PLAID_REDIRECT_URI` in your environment or set the respective `${VARIABLES}` in in the `x-environment`
section in [`docker-compose.yml`](/docker-compose.yml) directly. `PLAID_DIRECT_URI` is used for the
OAuth redirect flow and the redirect URI needs to be added to the [allowed redirect URI list in Dashboard](https://dashboard.plaid.com/team/api).

To see the log output of the quickstart run: `% make QUICKSTART=go logs` (when done, quit using `CTRL-C`).

To stop the quickstart use: `% make QUICKSTART=go stop`

Replace `go` in the command examples above with the name of the quickstart you want to start, e.g. `python`.

![Plaid quickstart app](/assets/quickstart-screenshot.png)

[quickstart]: https://plaid.com/docs/quickstart
[libraries]: https://plaid.com/docs/libraries
[node-example]: /node
[ruby-example]: /ruby
[python-example]: /python
[java-example]: /java
[go-example]: /go
[docker]: https://www.docker.com
