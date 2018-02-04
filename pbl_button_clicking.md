# Clicking pbl buttons 
Hey, I made some small scripts to quickly click all the buttons when you get students for the first time.
This should save time by allowing you to quickly set all quality/frequency to good/bad status.
The intended usage for this is with Chrome, where you open the console (ctrl+shift+i and click the console tab)
and simply copy pasting the script for the action you want

## Grab input fields
var inputs = document.getElementsByTagName('input')

## Set all boxes to good
*This will also automatically set student status to failure, so remember to change that*
for (var i=0; i<inputs.length; i++)
    if (inputs[i].type == 'checkbox' && inputs[i].id.slice(0,2)=='nu')
        if(inputs[i].id.indexOf('A') != -1)
            inputs[i].checked = true;
            
## Set all boxes to bad
*This will also automatically set student status to poor, so remember to change that*
for (var i=0; i<inputs.length; i++)
    if (inputs[i].type == 'checkbox' && inputs[i].id.slice(0,2)=='nu')
        if(inputs[i].id.indexOf('B') != -1)
            inputs[i].checked = true;
            
## Clear all check boxes
*This is incase you mess up and want to reset every checkbox to being empty*
for (var i=0; i<inputs.length; i++)
    if (inputs[i].type == 'checkbox' && inputs[i].id.slice(0,2)=='nu')
        inputs[i].checked = false;
