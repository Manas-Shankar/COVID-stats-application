# COVID-stats-application
A repository to collate the multiple repositories used to build the COVID-statistics application. Links in the readme correspond to each component of the application.

[COVID-stats-server](https://github.com/Manas-Shankar/covid-stats-server) <br>
A server built using nodeJS and ExpressJS that acts as the backend for the covid-stats-website.
Performs daily inserts (at 4 AM) into the database by retrieving data scraped by india-covid-scraper and world-covid-scraper.
Also retrieves user data (name,phone number and region) submitted via a form on the website and sends a sms message containing daily statistics for their entered region. This is done everyday at 9 AM.
Uses node-cron for scheduling tasks and the FAST2SMS service to send messages.<br>


[COVID-stats-website](https://github.com/Manas-Shankar/covid-stats-website) <br>
A COVID-19 statistics website built using Next.js. Uses the covid-stats-server as a server backend, which itself connects to MongoDB to store daily statistics and user data.
Users can view daily statistics in India and the world, as well as view statistics for individual states.
They can also sign up to receive daily sms notifications at 8 AM by entering their name, phone number, and region of stay.<br>

[COVID-world-scraper](https://github.com/Manas-Shankar/world-covid-scraper) <br>
An actor (scraper) hosted on apify to scrape Covid statistics for the world. This repo has been integrated with the apify platform via a webhook, which automatically builds the actor on apify upon every push to this repo.<br>

[COVID-India-scraper](https://github.com/Manas-Shankar/india-covid-scraper) <br>
An actor (scraper) hosted on apify that scrapes covid statistics for India. This repo has been integrated with the apify platform via a webhook, which automatically builds the actor on apify upon every push to this repo.<br>


