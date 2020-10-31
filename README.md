# Habit Tracker

For this project, you will build a Django application that you can use to help track and reinforce daily habits.

* Your application should have registration and login.
* Users should be able to create a new habit tracker. Each habit should have a name and a target or goal. What is this "target"? Each habit should have a daily number of some action you want to do. Some examples:
  * I want to walk 1000 steps daily
  * I want to write 100 lines of code daily
  * I want to talk to 2 new people each day
  * I want to read 200 pages daily
  * I want to sleep 8 hours daily
* Once you have habits, you should be able to make a daily record of your activity on each habit. That record should contain a date and a number for that date.
* A user can only have one record per day per habit. You will need to use [the `unique_together` option](https://docs.djangoproject.com/en/2.2/ref/models/options/#unique-together) to enforce this.
* Optimally, users can edit/update records and add records for previous days.
* Make your interface for this feature as easy to use as possible. For example, if you can choose the date for your record, have it default to the current date.
* On the detail page for a habit, you should be able to see all the records for that habit in an HTML table. Show the user whether they met their goal for that day visually somehow -- maybe via colors. Think about accessibility here -- how would a user that can't see know whether they met their goal each day?

### Some stretch goals for this project

* Add a line chart to the detail page for a habit showing your records for the last 30 days.
* On the detail page for a habit, show the best day for that habit, and the average day for that habit.
* When you list the records for a habit, show any days that don't have a record that are between the first and last record. For example, if there's a record for June 28 and a record for June 30, show June 29 as well and highlight that it has missing data. Provide a way to fill in that data easily.
* Add the ability to have "negative habits." These habits should have a goal you want to get under. For example:
  * I want to watch less than 60 minutes of TV daily
  * I want to eat less than 15 jellybeans a day
  * I want to say less than 3 curse words a day
* If a user is missing a record for a habit for the previous day, show them a message on their dashboard that lets them know and asks them to put in the record. Make it easy to jump from that message to the form to enter the data.
* Use the [`constraints` option for models](https://docs.djangoproject.com/en/3.1/ref/models/constraints/) with `UniqueConstraint` to make the habit records unique by user, habit, and day.

### How much of this is JavaScript?

You can make your forms a lot more usable by adding JavaScript -- to begin with, you can have a button for making a record that then shows a form without reloading the page.

If you want to add charts to your habits, you'll definitely need JavaScript. Check out [Chart.js](https://www.chartjs.org/).
