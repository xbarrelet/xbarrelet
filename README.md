Welcome to my humble Github account! You'll find here :

- An ongoing project about automatically optimizing algorithmic financial strategies using Reactor composed by:
  - quotes-importer : Import quotes from Finnhub on which to backtest the strategies
  - ta4j : Enriched open-source Java library for technical analysis (mainly used for technical indicators)
  - backtester : Backtest the algorithmic financial strategies on the quotes by basically bruteforcing different parameters (using limits in annotations)
  - results-analyzer: not implemented yet, will analyze the results of the backtester to determine which combinations of parameters are the best
  
- The components of the website letsfindamovie.com that uses a CQRS architecture and everything is reactive. Made of:
  - movies-manager : Source of truth of the system that loads from csv the movies, tags and ratings and serves them to the caches
  - converter-gateway: Converts rest calls to events propagated within the system to add tags and ratings to movies, written in Python with Aiohttp
  - cache-tags-manager : cache of tags using ElasticSearch as a datastore
  - cache-movies-manager: Cache of movies using Redis as datastore
  - cache-movies-manager-haskell: same cache but coded in Haskell, still needs to implement the update of movies in Redis
  - cache-ratings-manager: Cache of ratings coded in Scala using Akka and Play as framework, with Eventstore as a datastore (event sourcing)
  - movies-explorer-webapp: React/Redux/RxJs webapp with minimalist design to consult and edit movies/tags/ratings + to consult Grafana dashboards about the state of every components (technical + business) + a diagram of the architecture with the link to this repo
  - k8: Scripts and configuration to start clusters locally and on Google Kubernetes Engine with every components
  - docker: Scripts to load the components in Docker, mostly for test
  
You can visit the website here : https://letsfindamovie.com
  
  
I'm currently looking for some remote work, my linkedIn :  https://www.linkedin.com/in/xavier-barrelet/
