# Train Scheduler

![Running the app](/assets/images/preview.jpg)

## What Is This Thing?
This web app allows users to track and add train schedules. Simple JQuery scripting generates a table that shows all currently stored train lines, how often they arrive at station, and when they'll next arrive in realtime. Train information is stored on Firebase so it's acessible from anywhere, and users can add or remove lines from the display.

## What's Special About It?
Rather than displaying trains in an arbitrary order, the app runs a sort function using Moment.JS to determine in what order the trains will arrive, placing them in descending order so the next train to arrive is always at the top of the table.

## How Do I Use It?
Simply navigating to the webpage by [clicking this link](https://quething.github.io/train-scheduler/) will automatically load any existing trains and begin keeping accurate time. To add trains, fill out and submit the form at the bottom of the page; a validation check will ensure that intervals and arrival times are entered correctly, and the page should immediately refresh. A train line can be removed by clicking its corresponding "remove line" button on the table.

## Who Made It?
All local code was written solely by myself, Mars Getsoian. JQuery, Moment.js, and Bootstrap are the product of their respective communities, and the Firebase server service is provided by Google.

## Are There Bugs?
* An issue exists with the sorting function around noon and midnight, when trains scheduled to arrive after 1:00 sort higher than trains arriving earlier at times with higher numbers (generally 11-12).
* Some users have reported issues loading the page in non-Chrome browsers.
