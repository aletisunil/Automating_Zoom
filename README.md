# Zoom Automation
A python script that automatically joins a zoom meeting based on your timetable.

<ol>
<li>Checks the "timings.xlsx" file to look for meetings that are going to start.</li>
<li>As soon as the current time matches any meeting time it opens the Zoom Desktop application.</li>
<li>Navigates the cursor automatically to various steps to join the meeting.</li>
<li>The meeting ID and passcode are extracted from "timings.xlsx" and entered into the Zoom app automatically.</li>
</ol>

## Prerequisites

<ol>
<li>Zoom app must be installed in your system.</li>
<li>Meeting time for the day along with Meeting ID and passcode must be entered manually into the "timings.xlsx"</li>
  <li>pyautogui, python, pandas</li>
</ol>

## Behind the scenes

<ol>
<li>An infinite loop keeps checking the current time of the system using "datetime.now" funtion.</li>
<li>The zoom app is opened using "os.startfile()" funtion as soon as current time matches the time mentioned in "timings.xlsx".</li>
<li>"pyautogui.locateOnScreen()" function locates the image of join button on the screen and returns the position.</li>
<li>"pyautogui.moveTo()" moves the cursor to that location.</li>
<li>"pyautogui.click()" performs a click operation.</li>
<li>The meeting Id and Passcode are entered using the "pyautogui.write()" command.</li>
</ol>

## License & Copyright

© 2020 <b>Sunil Aleti</b><br>
Licensed under <a href="https://github.com/aletisunil/Automating_Zoom/blob/master/LICENSE">MIT License</a>
