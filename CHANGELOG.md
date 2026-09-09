# Changlog

## v1.2.5

* Fix grade calculation and presentation
* Change `Classes` to `Courses` to hide conflict with native Class keyword
* Change variables and function names to camelCase
* Add log() function for logging
* Use for..of loops
* Utilize CSS for supplying assignment icons rather than `img` tag
* Used Prettier formatter to format
* Changed `osu` to `canvas`
    * Script works on all university canvas sites
* Add icon for discussion topics

## v1.3.0

* Improve removal of iframes to decrease the amount of memory used
* Filters are preserved and restored

## v1.3.1

* The page loads a bit faster
* All assignments are retrieved

## v1.4.0

* Filters now work on Firefox
* Grades now show properly if grade letters are not supported

## v1.4.1

* Fix `now.addDays is not a function` error that prevented assignments from loading
* Stagger course requests to avoid Canvas rate limiting (HTTP 429), which silently dropped entire courses' assignments
* Retry requests up to 5 times with exponential backoff (honoring `Retry-After`) when rate limited or on server errors
* Fail loudly (console) instead of silently when a course's assignments cannot be fetched
* Fix crash when the grades page fails to load (`Cannot destructure property 'grading_scheme'`)

## v1.5.0

* Add "Hide No Due Date" filter option
* Announcements are now sorted with the newest first
* Announcements section can be collapsed by clicking its heading (state is remembered)
* When collapsed, courses and assignments expand to fill the freed space

## v1.5.2

* Missing assignments are now indicated by a colored badge around the type icon instead of a red icon
* Assignments due today are highlighted with a yellow badge around the type icon

## v1.5.3

* Icons are now centered inside the colored badge

## v1.5.4

* Due-today highlight is now only the badge around the icon, matching the missing-assignment style

## v1.5.5

* Status badges are slightly bigger

## v1.5.6

* Fix zebra striping breaking when rows are hidden by filters (stripes are now computed over visible rows only)
