# CeneoScraper
https://www.ceneo.pl/84514582#tab=reviews_scroll
## Ceneo Scrapiing Agorithm
1. Analysis of the structure of the website
2. Send http request to acces first page with opinions
3. Check the code of http response
4. Parse the html code of page with opinion
5. Extract required data
6. If there are more pages, move to the next page and repeat steps  2-6 for it
7. Save extracted data 

## Analysis of ten structure of the webpage
|Component|Selector|Variable|
|----------|-------|-------|
|opinion|div.js_product-review:not(.user-post---highlight)|opinion|
|opinion ID |data-entry-id|opinion_id|
|author |span.user-post__author-name|author|
|recommendation |span.user-post__author-recomendation > em|recommendation|
|number of stars |span.user-post__score-count|stars|
|content of opinion |div.user-post__text|content|
|list od adventages |div.review-feature__item--positive|pros|
|list od disadventages |div.review-feature__item--negative|cons|
|fow how many helpful |button.vote-yes[data-total-vote]|vote_yes|
|fow how many unhelpful|button.vote-no[data-total-vote]| |
|publishing date |span.user-post__published > time:nth-child(1)[datatime]| |
|purchase date |span.user-post__published > time:nth-child(2)[datatime]| |

