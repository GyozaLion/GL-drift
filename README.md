# GL-drift
A simple drift-mode script for fiveM. Toggle the drifting mode with `shift`. The script works by changing handling variables of the active vehicle.

modified Version off MoravianLion Drift Scrift
original repo : https://github.com/MoravianLion/Drift-Script
now its support qb-notify and okokNotify
and fixing some issues

## Configuration

Configuration is stored in the `handleMods` array:
```lua
local handleMods = {
	{"fInitialDragCoeff", 90.22},
	{"fDriveInertia", .31},
	{"fSteeringLock", 22},
	{"fTractionCurveMax", -1.1},
	{"fTractionCurveMin", -.4},
	{"fTractionCurveLateral", 2.5},
	{"fLowSpeedTractionLossMult", -.57}
}
```

## _Old readme below_
First proper and public drift script for FiveM! Use and share as you like.

Script works on simple principle - increasing and decreasing values in handling model in real time upon pressing left Shift.

Applies appropriately for AWD vehicles too.

Drift script works the best with semi-realistic handlings. If you have a shitty handling by default, drifting will be shitty as well, unless you will make changes in values yourself.

By default, the drift script is only allowed for road and personal vehicles. I really wasn't interested to see drifting busses, but if you will change the code, anything's possible, right?

Bugs:

Some vehicles can upon hitting drift settings got stuck on the spot and wheels will disappear. One of the value isn't converted as a solely number anymore. Look at the print in your client's console, to see something like 

0.512335abE

Solution:

Simply change car's default value in it's handling file by few units - 

instead of 

0.511112 

to 

0.511110

This will solve the problem with vehicle getting incorrect values.

