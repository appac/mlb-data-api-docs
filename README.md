# MLB Data API

**All of the data you get back from these endpoints is property of MLB/MLB Advanced Media, and you should refer to their [terms of use](http://gdx.mlb.com/components/copyright.txt) before using any of it in projects.**

## Getting Started

### 1. Request Structure

- Host: `http://lookup-service-prod.mlb.com`
- Path: `/json/named.[endpoint].bam`

### 2. Example Request

```no-highlight
http://lookup-service-prod.mlb.com/json/named.search_player_all.bam
```

### 3. Using col_in & col_ex

For many responses from the API, you can determine what data is included and excluded, using the `col_in` and `col_ex` parameters respectively. This is useful and almost required for some endpoints that return large amounts of additional data that you likely won't need.

The format for these params is `[endpoint].col_in` or `[endpoint].col_ex`, for example a search request with `col_in` would look like this:

```no-highlight
http://lookup-service-prod.mlb.com/json/named.search_player_all.bam?sport_code='mlb'&active_sw='Y'&name_part='young%'&search_player_all.col_in=player_id
```

This would perform a search for 'young' but any results found would only have the `player_id` field. Conversely, we could *exclude* the `player_id` field by using `col_ex`

```no-highlight
http://lookup-service-prod.mlb.com/json/named.search_player_all.bam?sport_code='mlb'&active_sw='Y'&name_part='young%'&search_player_all.col_ex=player_id
```

This way we get search results that feature every field except the player's ID.
