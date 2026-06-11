# Recovery² - Write-up

**Notice:** Recovery² doesn't seem to be useful yet, and this notice will be removed when a use is found.

## Description
Recovery² is a really dumb exploit, and not really an exploit per se.
It also only works on keyrolled devices *(needs confirmation!)*.

All you need to do is boot into a shim, but without a USB *`M a s s   S t o r a g e   D e v i c e`* connected.

## Method
1. Boot into recovery (`Esc+⟳+⏻`)
2. Enter Developer Mode (`Ctrl+D` → `Enter`)
3. Enter recovery again (`Esc+⟳+⏻` if you have somehow forgotten it in the span of like, 5 seconds)

You should be in recovery while on Developer Mode now.
You can verify that by attempting to enter Developer Mode again,
and a popup dialog reading "`Developer mode is already enabled.`" (or similar) should appear.
