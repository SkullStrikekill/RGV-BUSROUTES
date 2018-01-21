# RGV-BUSROUTES

This is a project to convert PDF bus routes in the Rio Grande Valley to the General Transit Feed Specification for ingestion by route mapping tools. 

RGV Metro Connect PDF: http://rgvmetroconnect.com/wp-content/uploads/2017/05/Route-NEW.pdf
Google GTFS Example Page: https://developers.google.com/transit/gtfs/examples/gtfs-feed
Google GTFS Specification Page: https://developers.google.com/transit/gtfs/reference/
Google GTFS Testing Page: https://developers.google.com/transit/gtfs/guides/tools
Google GTFS Publishing Page: https://support.google.com/transitpartners/answer/1111577

Checked the following:
agency.txt
calendar.txt
routes.txt
trips.txt
stops.txt
stop_times.txt
shape.txt

Improvment suggestions:
Consider updating "stop_desc" in "stops.txt" to make them more useful.

In order to run validation tests with the Google Python validator, you will use these scripts: 
python feedvalidator.py <File Path>
python schedule_viewer.py --key <Google API Key> --feed_filename <File Path>

_Perform the following steps:_
`cd transitfeed-master` to navigate to the appropriate folder
`python feedvalidator.py FinalGTFS` to use the Google Python validator
`python schedule_viewer.py --key <Google API Key> --feed_filename FinalGTFS` to plot the GTFS file on Google Maps using the schedule viewer