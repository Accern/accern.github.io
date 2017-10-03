##Source Rank

**What is it?** Accern analyzes 300 million sources in favor of how promptly they cover stories and if their information will go viral (similar articles published by others). With Accern Source Rank, users can have the analytics for `source_timeliness` and `source_republish`.

**Quick Definition:**

* **source_timeliness.overall** - value from 0 to 100, determines how timely the source is at releasing articles.

<img src="images/source_timeliness.jpg" alt="source_timeliness" width="600px" />

The source timeliness score is calculated for each source across all the stories which have articles from it, and are weighted by the story size, giving more credibility to trending stories and decreasing the importance of small stories.

* **source_timeliness.on_entities** determines the timeliness of the source to cover mentioned companies.

* **source_timeliness.on_events** determines the timeliness of the source to cover mentioned events.

* **source_republish.overall** - value from 0 to 100, determines how likely that more similar articles will come in a short period of time after an article is published from a specific source.

* **source_republish.on_entities** determines regarding to the mentioned companies, how likely more article will cover the similar story after the selected source.

* **source_republish.on_events** determines regarding to the mentioned events, how likely more article will cover the similar story after the selected source.

**Examples**


- **Overall Source Timeliness Score** - If Source A has overall timeliness score higher than Source B, Source A publishes article earlier than Source B in general .

- **Overall Source Republish Score** - If Source A has overall republish score higher than Source B, a new article from Source A will in general have more follow up articles than Source B in general.

- **Source Timeliness Score on Company Earnings** - If Source A has timeliness score on Company Earnings higher than Source B, Source A reports faster about Company Earings than Source B.

```json
{
    "source": "***",
    "source_timeliness": {
        "overall": 41,
        "on_entities": [
            {
                "key": "AAPL",
                "value": 43
            },
            {
                "key": "AMZN",
                "value": 32
            }
        ],
        "on_events": [
            {
                "key": "Acquisition",
                "value": 96
            },
            {
                "key": "Financial Ratings",
                "value": 16
            }
        ]
    },
    "source_republish": {
        "overall": 23,
        "on_entities": [
            {
                "key": "AAPL",
                "value": 10
            },
            {
                "key": "AMZN",
                "value": 1
            }
        ],
        "on_events": [
            {
                "key": "Acquisition",
                "value": 14
            },
            {
                "key": "Financial Ratings",
                "value": 20
            }
        ]
    },
}
```

- **Metric Combination** Consider the right-side object, and a new article from a specific source reporting a recent acquisition from Apple, we see that for this particular source, it generally report story about `AAPL` and `Acquisition` very timely comparing to the all the events and companies overall.


## Author Rank
**What is it?** Ranks are based on the same Source Rank model which tries to predict promptness and ability to post republishable stories.

<aside class="notice">
Difference between source and author? Source is the website like New York Times or Bloomberg. Author is the writer within the websites like Twitter or Tumblir.
</aside>

**Quick Definition:**

* **author_timeliness.overall** - value from 0 to 100, determines the promptness the author covers articles.

* **author_timeliness.on_entities** determines the timeliness of the author to cover mentioned companies.

* **author_timeliness.on_events** determines the timeliness of the author to cover mentioned events.

* **author_republish.overall** - value from 0 to 100, determines how likely that more similar articles will come in a short period of time after an article is published from a specific author.

* **author_republish.on_entities** determines regarding to the mentioned companies, how likely more article will cover the similar story after the selected author.

* **author_republish.on_events** determines regarding to the mentioned events, how likely more article will cover the similar story after the selected author.
