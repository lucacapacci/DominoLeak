# Lotus Domino Path Discovery
A python script to identify unauthenticated Lotus Domino exposed paths.

## Howto
#### 1st step
Edit the domino_discovery.py file:
- variable "starting_points" (line 8): you need to replace the current content with your target(s)
- variable "fail_page_contents" (line 12): most of the time login pages are custom made, so in this field you can put one or more strings to identify login pages - in order to NOT flag the page as an exposed path. If you don't want to use this feature just set the variable to an empty list: `fail_page_contents = []`
- fail_status_codes (line 15): sometimes the target doesn't show any login form but just responds with a particular HTTP code. When the script crawls pages with an HTTP belonging to this list it doesn't flag the page as an exposed path. If you don't want to use this feature just set the variable to an empty list: `fail_status_codes = []`
- variable "sleep_time_seconds" (line 17): delay between requests to the target. Default value is 1 second
- variable "paths" (line 19): list of paths to check - most of the time you don't want to modify it
#### 2nd step
run `python domino_discovery.py`
