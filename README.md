# OL-CustomAttributeUpdater
Can be used to update a custom attribute on user's within your OneLogin account

###
# Created by: Patric Fox ( patric[dot]fox[at]onelogin[dot]com )
# Date: 02/24/2015
###

Requires the following python modules to be available:

Requests: http://docs.python-requests.org/
LXML: http://lxml.de/
CSV: (should be available in default installation)
Collections: (should be available in default installation)

Usage:
You MUST edit the script and change, at the minimum, two variables:

apikey - In your OneLogin account under Settings -> API, copy the API key that is available and paste it in between the quotes.

custom_attribute - format should be custom_attribute_YOURATTRIBUTENAME

The script also looks for the file "user_details.csv".  You can change the name of your file to match this filename or change the filename in the script to match your file.

Note that the script attempts to parse email addresses from the CSV file and expects them to be in the first column of the CSV.  If the email address is in a different column you must update the value for:
email = columns[0]

Change the 0 to whichever column your email address is stored in.  Columns are counted from the left, starting at 0 => 1 => 2, etc
