# API Builder Stock Quote Watchlist API

A stock quote and watch list API based on [Finnhub](https://finnhub.io/) created in Axway's [API Builder](https://docs.axway.com/bundle/api-builder/page/docs/index.html).

The project exposes two end points

GET /quote?symbol=AAPL
GET /watchlist?symbols=AAPL,INTC,TXN,NVDA,AMZN,MSFT

This is all described [here](https://github.com/lbrenman/ai-stockquote-fh) and uses the same OAS Doc.

You can download a Docker Image of this project [**here**](https://hub.docker.com/repository/docker/lbrenman/apib_stockquotefh/general).

You can run it as follows:

`docker run --name apib_stockquotefh -e PORT=8081 -e API_KEY={{API KEY OF YOUR CHOOSING}} -e FINNHUBTOKEN={{YOUR FINNHUB API KEY}} -p 80:8080 --rm lbrenman/apib_stockquotefh:latest`

Then you can call it as follows:

`curl --location 'http://localhost:80/api/quote?symbol=T' -H 'accept: application/json' -H 'APIKey: {{API KEY OF YOUR CHOOSING THAT YOU ENTERED ABOVE}}'`