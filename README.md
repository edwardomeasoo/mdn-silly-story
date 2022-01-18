# Project Brief
Using the provided HTML, CSS and text strings, write the necessary Javascript to finish the program which does:
* Generate a silly story when the button is pressed
* Replace the default name 'Bob' with a custom name, if a custom name is entered
* Convert the default US weight and temperature measurements into UK equivalents, if radio button is selected
* Generate another random silly story if the button is pressed again

# Steps
## Architecturing
1. Create `main.j`
2. Link to `main.js` in `index.html`
## Variables and Functions
1. Copy all code under "1. COMPLETE VARIABLE AND FUNCTION DEFINITIONS" from raw text file, paste into `main.js`
2. From "2. RAW TEXT STRINGS" in raw text file, copy the text strings into:\
	* `storyText` = first big long string
	* `insertX` = the set of 3 strings, in an array
	* `insertY` = the second set of 3 strings
	* `insertZ` = the third set of 3 strings

## Event Handler and Complete `result()` Function
1. Copy the code under "3. EVENT LISTENER AND PARTIAL FUNCTION DEFINITION", past into `main.js`
2. Create a variable `newStory`, declare it equal to `storyText`
3. Create variables `xItem`, `yItem`, and `zItem`, make them equal to the result of calling `randomValueFromArray()` on the three arrays.
4. Replace the three placeholders---`:insertx:`, `:inserty:`, `:insertz:`---in the `newStory` string with the strings `xItem`, `yItem`, `zItem`\
	You may repeat the replace() method multiple times, or you can use regular expressions
	
	`let text = 'I am the biggest lover, I love my love'; text.replace(/love/g,'like');`

5. Inside the first `if` block, add another string replacement method call to replace the name `Bob` in the `newStory` string, if a `name` was submitted\
	`if` a value has been entered into the `customName` text input, replace `Bob` with `customName.value`

6. Inside the second `if` block, check to see if `uk` radio button has been selected.
	
	If yes, \
		- convert the weight and temperature values and units
		- replace '94 fahrenheit' with contents of `temperature` variable
		- replace '300 pounds' with contents of `weight` variable

7. Make `textContent` of `story` variable (which references the paragraph element) equal to `newStory`