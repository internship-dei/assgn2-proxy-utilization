# proxy-utilization

As you might have understood , web URLs block IP's that programmatically (web scrapers, bots etc) try to scrape their web content. This is because it add overload on their web sites and thus brings their site response time down and strains underlying infrastructure.

So then if you hit a web URL a threshold number of times it is likely to block your scraper.Whst is the solution ? 

Rotating  IP's via proxy is a standard solution used along with timer interval introduced while scraping :

Go through this link: https://www.scrapehero.com/how-to-rotate-proxies-and-ip-addresses-using-python-3/

In this assignment , you are going to hit the URL : https://fossbytes.com/10-best-free-music-websites-to-download-songs-legally/ ( or any particular URL of your choice), multiple times from your scraper and note the requests response ! While you 're getting 200 OK as response it's fine , but when it blocks you (as it did to me in session) then you 're going to re-route your IP via a proxy

To obtain various proxies , scrape https://free-proxy-list.net/  : free proxies listed over there via the html content which get refreshed every 10 mins (as per the site). If you do view-source of the page you'll find all the proxies neatly present , like shown below -

"Updated at 2021-07-05 05:12:03 UTC.

117.58.245.66:40137
180.183.132.131:8213
34.146.77.219:3128
195.74.72.129:37213
77.238.79.111:8080
119.82.252.25:42914
95.84.145.67:8080
88.82.95.146:3128
47.243.12.14:8888
217.219.67.110:8080
119.28.68.91:8080 "

Use each of the proxy to access the web page that has blocked your IP and record the response of the webpage i.e 200 OK or some other response.We're trying to evaluate what percentage of these proxies work ( not all will) and the success hit ratio

Do this for over 100 different proxies ( at time interval of 15 mins or more) and summarize what %age were successful and what were not , along with your observations.Upload the notebook with the details around stats and observations
