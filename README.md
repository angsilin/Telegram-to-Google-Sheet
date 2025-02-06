As the name states, this code allows users to send messages via their Telegram Bot and it will automatically be filled into their designated Google Sheet.

In this scenario, I have created this bot to automatically update my travel spending so that I am able to track 1) Total cost of spending 2) Spending based on Payment Method 3) Category spent on.

**Workflow with example:**
1. User sends '/start'
2. User prompted to 'Please select an option:'. (E.g. Menu with 5 categories: Transport, Food & Drinks, Entertainment, Shopping, Others)
3. Once an option is chosen, Bot prompts user to provide an Item description. (E.g. Top-up Train Card)
4. Then, Bot prompts user to provide amount. (E.g. 1000)
5. Lastly, Bot prompts user to select which of the Payment Methods was used. (E.g. Debit Card)

From point 2 of the workflow, the first option selection will help dictate which column the data should be filled.
Item description will be filled in the first empty row of the designated column, while Amount will be filled in the right column/cell.
Last option selection will then be automatically filled in the next column/cell as well.

