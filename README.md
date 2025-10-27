# airbnb-automation-demo
Here's an example of an automated booking management system I built for Airbnb. This is a modified version of a system I built for a client. The system collects data about upcoming Airbnb bookings and automatically:
1. Creates a cleaning schedule for the cleaner based on checkin and checkout dates
2. Generates invoices
3. Sends automated reminders using the line messaging service

This system could be built upon to generate additional documents or reminders. 

# How it works
For more details please refer to following blog post. (Blog post coming soon)!

Airbnb only makes its API available to select partners, so instead I use gmail's API to pull information about booking and billing from automated reminder emails that airbnb sends hosts. I then wrote code to automatically parse the emails for data, create a dataframe of all bookings, and then generate documents such as schedules, invoices, and reminder messages. I then used additional google APIs to upload the dataset and documents to a google drive account. As a final step I created a Line official account (https://www.linebiz.com/jp-en/other/) and used the Line messaging API to send reminder messages, schedules and links to the google drive to the Airbnb hosts and the cleaner. The entire project runs automatically on a schedule using github actions. 

# Files in the repository
1. 
