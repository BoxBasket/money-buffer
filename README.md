# money-buffer
Money managing sheet. Created to help me more finencially aware each day. 

---
## Initial setup
It is good idea to enter values that most likely will not change throghout the year. This is because a new monthly sheet is copied from sheet named `Base`. Below are suggested fields to fill out in the `Base` sheet.

* Year
* Model buffer
* Monthly Expense 
* Income

## How to start a new month
1. **Copy sheet named `Base`.** Everytime you start a new month, copy this sheet. Unfortunately there is no shiny button you can click to spawn a new clean template. 
2. **Fill out month (and year, if you have not done so) on the top.** This populates correct dates into the sheet as well as highlight today's date in the daily chart.
3. **In `Subtract from Pool` section,** enter amount you want to subtract from your pool in field `Actually Reserved`. This is the amount of money you promise yourself you will put into your savings account. Reference the amount in `Reservable` as model. That's the model amount you can save that will allow you to have amount shown in `model buffer` each day. The moment you enter your custom amount in `Actually Reserved`, the money buffer value in `Buffer` column will automatically update.
4. **In `Add to Pool` section,** enter amount you want to add to your pool. This can be amount of unused buffer from last month or any extra money you decide to add to the pool (in case your pool is too small this month)

## Recording Daily Expense
Record your daily expense into the daily chart, and watch `Total Buffered` go up! (If you are spending less than your daily money buffer).

Because it's just a single cell for you to record your daily expense, I recommend using formula such as:
```
=12.40+(9.00+4.13)
``` 
If you need to add a comment about the expense on that day, simply `right click > Insert comment` on the cell. I am aware this is not very efficient. I hope to make this easier in the future. 

## Other widgets
There are some small (possibly useless) widgets that you can use to make your chart more friendly for you.

* **Automatic/Manual Bill**: Set value between `Au`(Automatic) or `Ma`(Manual) for each monthly bill to mark which one must be manually handled. If a bill is set to manual, the date which the bill is due will be marked with red star in the daily chart.
* **Bill-Paid Marker**: You can choose between check mark, gray circle, or yellow triagle to mark the status of your bill payment. 
* **Daily Expense Marker**: On the tiny cell on the right of the daily expense cell, select from choice of many icons to make a mark about that day. This is not required and does not effect the buffer. This is just for your own view. 
  * Note: if you wish to make any customization on this cell, see section *Fine Tuning* below.
* **Reminders List**: Use this list to set special custom markers on your daily chart. The date you set will be marked with whatever value in the `Mark` column of this table.
 
## Fine Tuning
* **How to change the list of the icons:** the list of icons are stored in the `Data` sheet. Editing this list will change what icon appears in the dropdown.
* **How to change the number of icons in the list:** to alter the amount of icons in the list, select the dropdown cell, go to `Data > Data Validation`. The reference to the array/vector of icons is set in `Source` field.

