## Files
### Defi Llama TVL Analysis
The file `defi_llama_tvl_analysis.ipynb` contains the analysis. The analysis is split into two segments. The first a Snapshot analysis focused on TVL at one point in time alongside the most recent percentage changes in TVL all by category and chain. The second is a TVL over time analysis looking at the trend in TVL.

### Archive 
The `data_clean.ipynb` was used to obtain a list of Chainlink user protocols and the rest of the market protocols (non Chainlink users) both which are separated from the protocols not to include in the analysis. Some minor assumptions were made due to ambiguity:
- Tron governance staking did not have a similar match and this all tron protocol and related was removed (poor Justin Sun). This was 5 protocols only (justlend, justcryptos, sunswap, juststables, sun.io).
- bunny was in both the to include chainlink users and list of users to exlude, the decision was to exlude it.
- No match for armour as a protocol so this was ignored

## Clarifications
The Market refers to other protocols that are not excluded and not a protocol that uses Chainlink.

## What is TVL?
By the definition from Defi Llama: 
* Assets on pool2, that is, money that is providing liquidity to an AMM pool where one of the tokens is from the protocol (except on some cases where those assets are performing an active function such as being used as collateral).
* Non-crypto assets which are external to the blockchain, such as bonds or fiat currency. We don't consider the dollars stored on Tether's bank account as TVL, for example.

## Further ideas for implementation
* Hide the code in a back end and export the graphs. 
* Make the graphs in `streamlit` or `dash` so we have a web application that can be hosted.
* Work on tooltip hover over feature (would make comparisons much easier than just using eye).
* Create some more aesthetic visualisations (more time consuming in python, I would probably do the back end in `python` and export the tables to a better visualisation tool if I was to do this again).
* Clean up code (there is code reuse, some code could be replace with a function, some code could be more efficient).
* Add a count/total dollar value into the piecharts as currently it is just a percentage. 
* Potentially better names for the titles and the x and y axis. 
* More dynamic graphs to be able to zoom in and select the protocols in smaller groups
* Do a token breakdown TVL per protocol as well not just the totalTVL of the protocol
* Incorporate external data sources to verify the TVL, or compare TVL across different data sources as well. 