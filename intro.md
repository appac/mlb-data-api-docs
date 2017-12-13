Documentation for MLB's public `lookup/json/named` endpoints. These endpoints cover a range of data, including that of players, teams, rosters, league standings and game types.

## How The Endpoints Work

All endpoints use a base url of `http://mlb.mlb.com/lookup/json`, with a `/named.[endpoint].bam` appended to denote the specific endpoint you want to access.

For example the `search_player_all` endpoint looks like this:

`http://mlb.mlb.com/lookup/json/named.search_player_all.bam`

This is then further modified with parameters to determine which team or player we want data for, as well as giving us some control over what data is returned to us.

## Using MLB Data

Please remember that all of the data you get back from these endpoints is property of MLB/MLB Advanced Media, and you should refer to their [terms of use](http://gdx.mlb.com/components/copyright.txt) before using any of it in projects.
