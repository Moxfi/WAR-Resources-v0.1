## How do macros work

Game attempts to execute the macro one line per each in-game frame. \
60 fps, 60 lines a second.

Filling up all the slots with repeating lines sort of simulates queuing. \
The real reasoning is that macros read one line per each in-game frame. \
If the macro tries to execute an action while in animation lock (from another action, for example), it has no effect.

Frame 1: /merror off \
Frame 2: /ac "Nascent Flash" <2> \
Frame 3: /ac "Nascent Flash" <2> \
Frame N: ...

So when you repeat the action inside the macro, you stretch the action activation window. \
Instead of a macro that has a single frame where it attempts to use an action, you have a macro with 13 frames of attempts.

This gets around the issue of "Animation Lock vs Macros" where you might not be able to use a skill because of the Animation Lock.
