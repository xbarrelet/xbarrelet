Welcome to my humble Github account! You'll find in the public space:

An ongoing project about a system that automatically optimizes algorithmic financial strategies and test them using a paper trading API composed by:
- quotes-importer : Imports quotes and historical data from providers on which to backtest the strategies
- ta4j : Enriched open-source Java library for technical analysis (mainly used for its technical indicators)
- backtester : Backtests the algorithmic financial strategies on the quotes by basically bruteforcing different parameters (using dedicated Java annotations)
- tradingbot: A tradingbot using Akka that tests the resulting strategies in real conditions through a Paper trading api (Alpaca)

  
The components of the website letsfindamovie.com that uses a CQRS architecture and everything is reactive. Made of:
  - movies-manager : Source of truth of the system that loads from csv files the movies, tags and ratings and serves them to all the caches
  - converter-gateway: Converts rest calls to events propagated within the system to add tags and ratings to movies in all components, written in async Python with Aiohttp
  - cache-tags-manager : reactive cache of tags using ElasticSearch as a datastore
  - cache-movies-manager: reactive cache of movies using Redis as datastore and Micronaut as a Framework.
  - cache-movies-manager-haskell: same cache but coded in Haskell, still needs to implement the update of movies in Redis
  - cache-ratings-manager: reactive cache of ratings coded in Scala using Akka and Play as framework, with Eventstore as a datastore (event sourcing)
  - movies-explorer-webapp: React/Redux/RxJs webapp to consult and edit movies/tags/ratings + to consult Grafana dashboards about the state of every components (technical + business) + a diagram of the architecture with the link to this repo
  - k8: Scripts and configuration to start the system in Kubernete clusters locally and on Google Cloud
  - docker: Scripts to load the components in Docker as a dev/test environment

- Redis-tester : Performance tests with Gatling of different Java frameworks and Redis clients for a project of GVentures LLC Service.
  
My website https://letsfindamovie.com is not currently up due to costs but can be instantiated on GKE on-demand.
  
I'm a freelancer always interested in new projects, my Upwork profile: https://www.upwork.com/freelancers/~01a7e4d1f5ebce66f4 and my linkedIn :  https://www.linkedin.com/in/xavier-barrelet/
