##Source Rank

Accern analyzes 300 million+ sources in favor of how promptly they cover stories and if their information will go viral (similar articles published by others). With Accern Source Rank, users can have the analytics for `timeliness` and `republish_rate`.

**Quick Definition:**

* **Timeliness** - determines how timely the source is at releasing articles.

<img src="images/source_timeliness.jpg" alt="source_timeliness" width="100%" />

The source timeliness score is calculated for each source across all the stories which have articles from it, and are weighted by the story size, giving more credibility to trending stories and decreasing the importance of small stories.

* **Republish Rate** - determines how much the source is at releasing stories.


**How is it created?** A graphical model takes into account historical data (past articles), how certain news appeared in the past and how the distribution of articles within a story looked like.
It checks in the past, which sources posted faster in comparison to other sources which then posted contextually similar articles.

**Examples**

- **Overall Source Rank (High)** - StreetInsider releases stories first, and their stories get republished by many other sources.

- **Overall Author Rank (Low-Mid)** - *John Paul* releases stories on StreetInsider first, but his stories don’t get republished by any other authors.

## Author Rank(author_rank)
**What is it?** Ranks are based on the same Accern Rank model which tries to predict promptness and ability to post republished stories.
**Rank 1** is lowest and **Rank 10** is highest.
**event_source_rank/event_author_rank** is more precise.
For ex. Tumblr posts rumors faster than others. Bloomberg posts financial docs faster than others.
It would be prudent to the client to notice that sources will have varied ranks for different events.

<aside class="notice">
Difference between source and author? Source is the website. Ex NYT or Bloomberg. Author is the writer within the organization.
In the below examples we use fictional name John Paul.
</aside>

**Quick Definition:**

* **event_source_rank** - determines if the SOURCE is *reliable* at releasing articles associated with a financial event.

* **event_author_rank** - determines if the AUTHOR is *reliable* at releasing articles associated with a financial event..

**How is it created?** The ranking model is the same. Ranks are calculated by filtering based on financial events.

**Examples**

- **Event Source Rank (High)** - StreetInsider releases lawsuit stories first, and their lawsuit stories get republished by many other sources.

<img src="images/cuttykitty.jpg" alt="IMAGE ALT TEXT HERE" width="100%" />
