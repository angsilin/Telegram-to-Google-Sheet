As the name states, this code allows users to send messages via their Telegram Bot and it will automatically be filled into their designated Google Sheet.

In this scenario, I have created a Telegram bot to automatically update my travel spending on my Google Sheet so that I am able to track 1) Total cost of spending 2) Spending based on Payment Method 3) Category spent on while on the move.

**Workflow with example:**
1. User sends '/start'
2. User prompted to 'Please select an option:'. (E.g. Menu with 5 categories: Transport, Food & Drinks, Entertainment, Shopping, Others)
3. Once an option is chosen, Bot prompts user to provide an Item description. (E.g. Top-up Train Card)
4. Then, Bot prompts user to provide amount. (E.g. 1000)
5. Lastly, Bot prompts user to select which of the Payment Methods was used. (E.g. Debit Card)

From point 2 of the workflow, the first option selection will help dictate which column the data should be filled.
Item description will be filled in the first empty row of the designated column, while Amount will be filled in the right column/cell.
Last option selection will then be automatically filled in the next column/cell as well.

P.S I have made my Option 1 skip 2 columns before filling in Payment Method.

---

Before that, you need to allow your script to access Google Sheets and Google Drive on behalf of your service account: 
1. Go to the Google Cloud Console: Google Cloud Console
2. Create a new project.
3. Enable Google Sheets API and Google Drive API.
4. Go to APIs & Services > Credentials.
5. Click Create Credentials > Service Account.
6. Download the JSON key file and store it in your project folder.
7. Share your Google Sheet with your service account email which is found in the JSON file.

On Terminal,
pip install python-telegram-bot gspread oauth2client

Have the following ready:
1. Telegram Token (via BotFather)
2. Google Sheet ID (Between /d/ and /edit of your Google Sheet)
