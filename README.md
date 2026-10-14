# Twitter advanced search operators for X

Twitter advanced search operators narrow a search to the exact posts you need.
They work in X advanced search, in the search box & through an API. This page
lists each operator we confirmed on X, with 1 tested example.

Last verified on 2026-10-13. We ran each example on X in the Latest & Top tabs.

[Xquik](https://xquik.com) maintains this list. Xquik is the world's fastest and
cheapest X Twitter scraper service with the most complete X data.

## How to use Twitter advanced search

1. Open [x.com/search-advanced](https://x.com/search-advanced), or use the
   search box on X.
2. Type your words, then add operators from the tables below.
3. Separate operators with spaces. X returns posts that match all of them.
4. Put a hyphen before an operator to leave its matches out.
5. Pick Latest for the newest posts, or Top for the most popular.

Copy 1 of these searches to start.

| You want                          | Search                                        |
| --------------------------------- | --------------------------------------------- |
| An account's posts from 1 month   | `from:NASA since:2026-09-01 until:2026-10-01` |
| Popular posts without replies     | `nasa min_faves:1000 -filter:replies`         |
| Posts from either of 2 accounts   | `from:NASA OR from:SpaceX`                    |
| Images in 1 language              | `ramen lang:ja filter:images`                 |
| An account's media posts          | `from:NASA filter:media`                      |
| Every reply in 1 conversation     | `conversation_id:2109320622882873464`         |

```text
from:NASA since:2026-09-01 until:2026-10-01
```

## Twitter search operators

Each row has 1 example that we ran on X. Latest & Top say whether the example
returned matching posts in that tab. Verified is the day we last ran it.

### Words and phrases

| Operator | What it does | Example | Latest | Top | Verified |
| --- | --- | --- | --- | --- | --- |
| `word1 word2` | Posts that contain both words, in any order. | `climate energy` | Yes | Yes | 2026-10-13 |
| `"exact phrase"` | Posts that contain the exact phrase. | `"climate change"` | Yes | Yes | 2026-10-13 |
| `OR` | Posts that contain either term. Write OR in capitals. | `tesla OR rivian` | Yes | Yes | 2026-10-13 |
| `-` | Leaves out posts that match the term after the hyphen. | `jaguar -car` | Yes | Yes | 2026-10-13 |
| `( )` | Groups terms, so OR applies only inside the brackets. | `(nasa OR spacex) launch` | Yes | Yes | 2026-10-13 |
| `#` | Posts with the hashtag. | `#photography` | Yes | Yes | 2026-10-13 |
| `$` | Posts with the cashtag of a stock or coin. | `$TSLA` | Yes | Yes | 2026-10-13 |

### Accounts

| Operator | What it does | Example | Latest | Top | Verified |
| --- | --- | --- | --- | --- | --- |
| `from:` | Posts sent by the account. | `from:NASA` | Yes | Yes | 2026-10-13 |
| `to:` | Posts addressed to the account, such as replies to it. | `to:NASA` | Yes | Yes | 2026-10-13 |
| `@` | Posts that mention the account. | `@NASA` | Yes | Yes | 2026-10-13 |
| `list:` | Posts by members of a public List. Use the List ID. | `list:1261769117331345415` | Yes | Yes | 2026-10-13 |
| `filter:verified` | Posts by verified accounts. | `nasa filter:verified` | Yes | Yes | 2026-10-13 |
| `filter:blue_verified` | Posts by accounts with a blue checkmark. | `nasa filter:blue_verified` | Yes | Yes | 2026-10-13 |

### Dates and times

| Operator | What it does | Example | Latest | Top | Verified |
| --- | --- | --- | --- | --- | --- |
| `since:` | Posts sent on or after the UTC day. | `from:NASA since:2026-10-01` | Yes | Yes | 2026-10-13 |
| `until:` | Posts sent before the UTC day. | `from:NASA until:2026-01-01` | Yes | Yes | 2026-10-13 |
| `until:YYYY-MM-DD_HH:MM:SS_UTC` | Posts sent before the exact UTC time. Works with since too. | `from:NASA until:2026-01-01_00:00:00_UTC` | Yes | Yes | 2026-10-13 |
| `since_time:` | Posts sent at or after the Unix time in seconds. | `from:NASA since_time:1767225600` | Yes | Yes | 2026-10-13 |
| `until_time:` | Posts sent before the Unix time in seconds. | `from:NASA until_time:1767225600` | Yes | Yes | 2026-10-13 |
| `since_id:` | Posts newer than the post with this ID. | `from:NASA since_id:2000000000000000000` | Yes | Yes | 2026-10-13 |
| `max_id:` | Posts no newer than the post with this ID. | `from:NASA max_id:2000000000000000000` | Yes | Yes | 2026-10-13 |
| `within_time:` | Posts from the last period. 2d means the last 2 days. | `nasa within_time:2d` | Yes | Yes | 2026-10-13 |

### Post types

| Operator | What it does | Example | Latest | Top | Verified |
| --- | --- | --- | --- | --- | --- |
| `filter:replies` | Only replies. | `nasa filter:replies` | Yes | Yes | 2026-10-13 |
| `-filter:replies` | Leaves out replies. | `nasa -filter:replies` | Yes | Yes | 2026-10-13 |
| `filter:quote` | Only quote posts. | `nasa filter:quote` | Yes | Yes | 2026-10-13 |
| `filter:nativeretweets` | Only reposts. | `nasa filter:nativeretweets` | Yes | Yes | 2026-10-13 |
| `filter:retweets` | Only reposts. It matched `filter:nativeretweets` in our tests. | `nasa filter:retweets` | Yes | Yes | 2026-10-13 |
| `include:nativeretweets` | Adds reposts to the results. Search hides them by default. | `from:NASA include:nativeretweets` | Yes | Yes | 2026-10-13 |
| `filter:self_threads` | Only replies an author sent to their own post, as in a thread. | `nasa filter:self_threads` | Yes | Yes | 2026-10-13 |
| `conversation_id:` | Posts in the conversation that the post with this ID started. | `conversation_id:2109320622882873464` | Yes | Yes | 2026-10-13 |
| `in_reply_to_tweet_id:` | Replies to the post with this ID. | `in_reply_to_tweet_id:2109320622882873464` | Yes | Yes | 2026-10-13 |
| `quoted_tweet_id:` | Quote posts of the post with this ID. | `quoted_tweet_id:2109320622882873464` | Yes | Yes | 2026-10-13 |
| `quoted_user_id:` | Quote posts of any post by the account with this ID. | `quoted_user_id:11348282` | Yes | Yes | 2026-10-13 |
| `filter:spaces` | Posts that link to a Space. | `nasa filter:spaces` | Yes | Yes | 2026-10-13 |

### Media and links

| Operator | What it does | Example | Latest | Top | Verified |
| --- | --- | --- | --- | --- | --- |
| `filter:media` | Posts with an image, video or GIF. | `nasa filter:media` | Yes | Yes | 2026-10-13 |
| `filter:images` | Posts with an image. | `nasa filter:images` | Yes | Yes | 2026-10-13 |
| `filter:twimg` | Posts with an image uploaded to X. | `nasa filter:twimg` | Yes | Yes | 2026-10-13 |
| `filter:videos` | Posts with a video. | `nasa filter:videos` | Yes | Yes | 2026-10-13 |
| `filter:native_video` | Posts with a video uploaded to X. | `nasa filter:native_video` | Yes | Yes | 2026-10-13 |
| `filter:links` | Posts with a link. | `nasa filter:links` | Yes | Yes | 2026-10-13 |
| `url:` | Posts with a link that contains the text, such as a domain. | `url:github.com` | Yes | Yes | 2026-10-13 |
| `filter:hashtags` | Posts with at least 1 hashtag. | `nasa filter:hashtags` | Yes | Yes | 2026-10-13 |
| `filter:mentions` | Posts that mention at least 1 account. | `nasa filter:mentions` | Yes | Yes | 2026-10-13 |
| `filter:safe` | Posts that X does not mark as sensitive. | `nasa filter:safe` | Yes | Yes | 2026-10-13 |

### Engagement

| Operator | What it does | Example | Latest | Top | Verified |
| --- | --- | --- | --- | --- | --- |
| `min_faves:` | Posts with at least this many likes. | `nasa min_faves:1000` | Yes | Yes | 2026-10-13 |
| `min_retweets:` | Posts with at least this many reposts. | `nasa min_retweets:500` | Yes | Yes | 2026-10-13 |
| `min_replies:` | Posts with at least this many replies. | `nasa min_replies:100` | Yes | Yes | 2026-10-13 |
| `-min_faves:` | Posts with fewer likes than the number. | `nasa -min_faves:5` | Yes | Yes | 2026-10-13 |
| `-min_retweets:` | Posts with fewer reposts than the number. | `nasa -min_retweets:2` | Yes | Yes | 2026-10-13 |
| `-min_replies:` | Posts with fewer replies than the number. | `nasa -min_replies:2` | Yes | Yes | 2026-10-13 |
| `filter:has_engagement` | Posts with at least 1 like, reply or repost. | `nasa filter:has_engagement` | Yes | Yes | 2026-10-13 |

### Language and place

| Operator | What it does | Example | Latest | Top | Verified |
| --- | --- | --- | --- | --- | --- |
| `lang:` | Posts in the language. Use its 2-letter code, such as ja or es. | `ramen lang:ja` | Yes | Yes | 2026-10-13 |
| `place:` | Posts tagged with the X place that has this ID. | `coffee place:96683cc9126741d1` | Yes | Yes | 2026-10-13 |

## Twitter search filters

A filter keeps 1 kind of post. Write `filter:` & a name, such as
`filter:images`.

- Put a hyphen first to remove that kind, as in `-filter:replies`.
- Join filters with OR inside brackets, as in
  `nasa (filter:images OR filter:videos)`.
- A filter needs no keyword. `from:NASA filter:media` lists that account's media
  posts.
- Search shows replies & hides reposts by default. Add `include:nativeretweets`
  to show reposts.
- In Top, X can show the post a matching reply answers above that reply.

## Search tweets by date

- `since:` includes its day. `until:` leaves its day out.
- X reads both days in UTC.
- For 1 full day, set `until:` to the next day, as in
  `since:2026-10-01 until:2026-10-02`.
- For an exact time, write `until:2026-01-01_00:00:00_UTC`.
- `since_time:` & `until_time:` take Unix seconds.
- `within_time:2d` covers the last 2 days.

## Twitter advanced search on mobile

Operators belong to X search itself, not to the advanced search form. Type or
paste them into the search box on your phone. Then pick Top or Latest. The form
at x.com/search-advanced also opens in a phone browser.

## Operators X no longer honors

X returned no posts for these examples in the Latest & Top tabs. Remove them
from your saved searches. We leave out `near:` because its results were
inconsistent in our tests.

| Operator | What it did | Example | Verified |
| --- | --- | --- | --- |
| `filter:vine` | Posts with a Vine video. | `nasa filter:vine` | 2026-10-13 |
| `filter:consumer_video` | Posts with a video from a personal account. | `nasa filter:consumer_video` | 2026-10-13 |
| `filter:pro_video` | Posts with a video from a professional publisher. | `nasa filter:pro_video` | 2026-10-13 |
| `filter:news` | Posts that link to a news site. | `nasa filter:news` | 2026-10-13 |
| `retweets_of:` | Reposts of the account's posts. | `retweets_of:NASA` | 2026-10-13 |
| `include:replies` | Added replies to the results. Search now shows them by default. | `nasa include:replies` | 2026-10-13 |
| `source:` | Posts sent from the named app. | `nasa source:Twitter_for_iPhone` | 2026-10-13 |
| `geocode:` | Posts near a latitude & longitude. | `coffee geocode:35.6762,139.6503,10km` | 2026-10-13 |
| `within:` | The radius of a search near a place. | `coffee near:tokyo within:10km` | 2026-10-13 |
| `card_name:` | Posts with a card of the named type, such as a poll. | `vote card_name:poll2choice_text_only` | 2026-10-13 |

## Run these searches through an API

Xquik runs the same operators through a REST API, an MCP server & Apify Actors.
You pay only for delivered, unique posts that match your filters.

- Read the [tweet search docs](https://docs.xquik.com/api-reference/x/search-tweets).
- Browse all [Xquik docs](https://docs.xquik.com).
- Create an API key at [xquik.com](https://xquik.com).

## How this list stays current

- We run every example again each week.
- Each run updates the Verified day of every operator.
- We review an operator that changed before its row changes.
- [operators.json](operators.json) holds the same data for scripts.

## Report a change

Did an operator stop working, or did we miss 1? Open an
[issue](https://github.com/Xquik-dev/x-twitter-advanced-search/issues/new) with
the search you ran & what X returned.

## More Xquik tools

- [X (Twitter) scraper API & Twitter MCP server](https://github.com/Xquik-dev/x-twitter-scraper) with REST, MCP & Skill setup.
- Twitter API SDKs for [TypeScript](https://github.com/Xquik-dev/x-twitter-scraper-typescript), [Python](https://github.com/Xquik-dev/x-twitter-scraper-python), [Go](https://github.com/Xquik-dev/x-twitter-scraper-go), [Ruby](https://github.com/Xquik-dev/x-twitter-scraper-ruby), [Java](https://github.com/Xquik-dev/x-twitter-scraper-java), [Kotlin](https://github.com/Xquik-dev/x-twitter-scraper-kotlin), [C#](https://github.com/Xquik-dev/x-twitter-scraper-csharp) & [PHP](https://github.com/Xquik-dev/x-twitter-scraper-php).
- [Twitter CLI & X CLI](https://github.com/Xquik-dev/x-twitter-scraper-cli) for terminal workflows.
- [Xquik X API & Twitter scraper](https://xquik.com) and the [Twitter API documentation](https://docs.xquik.com/api-reference/overview).

## License

[MIT](LICENSE)

> Xquik is an independent third-party service. Not affiliated with X Corp.
> "Twitter" and "X" are trademarks of X Corp.
