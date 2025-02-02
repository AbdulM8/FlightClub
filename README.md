A Python-based tool that checks flight deals for user-specified destinations and notifies subscribers by email whenever a matching flight deal is found below their desired price. 
This project expands on the standard flight deals finder by including a Google Form that collects user email addresses and preferred price thresholds, automatically storing them in a Google Sheet.
Overview
This tool allows end-users to subscribe to flight price alerts using a Google Form. The form collects:

Email Address
Desired Destination
Maximum Price (the price at or below which they’d like to be notified)
When a new flight deal is found using the Amadeus API (or another flight data provider) that matches or is below the maximum price, an email notification is sent to the subscriber.

Features
User Sign-Up via Google Form

Users provide their email, desired destination, and maximum price threshold.
The data is saved to a Google Sheet via Sheety or direct Google Forms integration.
Flight Search & Price Monitoring

Checks flight offers from the origin city to user-specified destination(s).
Leverages the Amadeus Flight Offers Search API (or a similar service) to get current flight prices.
Automated Email Alerts

Uses an SMTP server (e.g., Gmail SMTP) or a 3rd-party service (e.g., Twilio SendGrid) to send alert emails.
Sends emails only if a flight price is equal to or lower than the user’s threshold.
IATA Code Updating

If a city’s IATA code is missing from the Google Sheet, it fetches it using Amadeus and updates the sheet.
Multiple Destinations & Subscribers

Handles multiple user entries, each with a unique destination and price threshold.
