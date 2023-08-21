# Fibonacci Grid
Grid that clears detected sequence

# Running
Simple: Just run the html. I am great believer in saving time. We all have enough to do ;)

In a larger architecture code would be separated/minified etc. This is obvious with comments in the code block without complication.

# Architecture
All CSS is within a single style - no inline.

Code is split (via comments for clarity) into two roles. UI and COORDINATES (which I have decided the grid represents).

The two are coupled via one method for each direction and by Row and Col only, this would make it simple to modify one without affecting the other. (eg. zoomed views)

# Assumptions
Sequences are assumed to be valid both horizontal and vertical.
Request did not state preferences for handling sequences greater than 5, so the code will clear the longest valid sequence above this minimum.

# Additional
The UI and requested operation in this case, make very high numerical values improbable. However as a code exercise I have shown how the overhead of testing high values would be reduced.

# Issues
Fast clicks over various overlapping lines can create a minor premature clear of the highlight. Should this be seen as problematic, then a dictionary of callbacks could be kept and cleared were needed.

High numerical values would require an alternative view (I would use zoomed sections of the whole grid map)
