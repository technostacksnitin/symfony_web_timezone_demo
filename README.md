# symfony_web_timezone_demo
Please read everything below before you start to work.

PREPARATION

Before you start:

1. Install Apache2 or nginx server installed with PHP 7.3+ support.
2. Install Composer and make it ready to use.

THE TASK

Create a new Symfony regular web project.
In this project, create a page with an HTML form. The form should have 2 fields:
- date - text input; always in the format Y-m-d, no validation required, the input date is always valid,
- timezone - text input; e.g. Europe/London, Asia/Tokyo, America/Lower_Princes - no validation required, the input timezone is always valid with: https://en.wikipedia.org/wiki/List_of_tz_database_time_zones
After submitting the form, the following page should show the information about given date and timezone in the format:
The timezone [input-timezone] has [A] minutes offset to UTC.<br />
February in this year has [B] days.<br />
Specified month [C] has [D] days.
Where:
[input-timezone] is the timezone received from the input.
[A] is the time offset to UTC - in minutes. Values: may be 0, negative integer with minus (e.g. -60), positive integer with plus (e.g. +60)
[B] is the number of days in February in the year of given date. An integer.
[C] is the name of given month. A string.
[D] is the number of days in the month of given date. An integer.

The result may be on a separate page or it may be on the page with form, above the form.

EXAMPLES

1)
Form input:
date=2019-07-10
timezone=Europe/London

Output:
The timezone Europe/London has +60 minutes offset to UTC.<br />
February in this year has 28 days.<br />
Specified month (July) has 31 days.

2)
Form input:
date=2016-11-28
timezone=Asia/Tokyo

Output:
The timezone Asia/Tokyo has +540 minutes offset to UTC.<br />
February in this year has 29 days.<br />
Specified month (July) has 30 days.

3)
Form input:
date=1853-01-30
timezone=America/Lower_Princes

Output:
The timezone Asia/Tokyo has -270 minutes offset to UTC.<br />
February in this year has 28 days.<br />
Specified month (July) has 31 days.

PROJECT DELIVERY

Create a public GIT repository (e.g. GitHub), push the project there (without composer dependencies) and send the URL to the repository to us.
