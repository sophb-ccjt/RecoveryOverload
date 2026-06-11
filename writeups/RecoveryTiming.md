# RecoveryTiming - Write-up

## Description
RecoveryTiming is an exploit that allows selecting an arbitary Developer mode option.

It takes advantage of a race condition found in 
the modern recovery UI on enrolled Chromebooks with blocked Developer Mode.


When cancelling the (forced) transition to secure mode in the "`Return to secure mode`" dialog,
the Developer Mode menu appears for a singular frame.

And if you've lived with slow computers,
you might've noticed that multiple keyboard/mouse/whatever inputs are registered in the next frame without issue.

RecoveryTiming works exactly like that--
registering the keyboard inputs necessary to select the option normally, but all in a single frame,
that frame being the one where the Dev Mode options are visible.


## Method

1. Boot into recovery (`Esc+⟳+⏻`)
2. Enter Developer Mode (`Ctrl+D` → `Enter`)
3. Cancel secure mode transition (Select the `[Cancel]` option OR press `Escape`)
4. Spam the keyboard inputs to the Developer Mode option you want to select

And if all goes well, the behavior for the option you selected will happen.
If that doesn't happen, just restart from *step 3*.
