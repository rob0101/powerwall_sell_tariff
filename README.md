# pw_forced_sell
script to set a tariff in the Tesla Powerwall setting that has a time period when you want to export power

Customer's of Amber Electricity in Australia may find this useful to automate times the battery can be forced to sell.

You'll need to install TeslaPY first to use this script.
 See: https://github.com/tdorssers/TeslaPy

Call the script with 6 paramaters.

hhmm1 hhmm2 p1 p2 p3 p4

hhmm1 is the start time for the peak period when you want to sell to the grid.  This is 24 hour time e.g. 17:45 (for 15 minutes to 6pm)
hhmm2 is the end time for the peak sell period.

p1 = the price you pay to import (buy) from the grid, outside of the peak period

p2 = the price you pay to export (sell) to the grid, outside the peak

p3 = the price you pay to import (buy) from the grid during the peak period.

p4 = the price you pay to export (sell) to the grid during the peak period.

example:

pw_forced_sell 1710 1835 10 -5 60 50

The peak period is 1710 to 1835  (5:10pm to 6:35pm)
The offpeak buying price is 10 cents
the offpeak selling price is minus 5 cents
the peak buying price is 60 cents
the peak selling price is 50 cents.

The Powerwall needs to be in TBC (Time Based Control) mode for this to have any effect.

