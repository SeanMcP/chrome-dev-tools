# Debugging

## Set up

### Set breakpoint
Set a breakpoint by clicking in the line number on the left of the editor. The blue marker indicates that a breakpoint has been set on that line.

Click the marker again to **remove a breakpoint**.

## Buttons

### Pause/Resume
`F8` or `Command + \`

Pauses or resumes the execution of the code

### Step over ⭐️
`F10` or `Command + '`

Moves to the next functional line

### Step into
`F11` or `Command + ;`

Move into a function. Use it to jump into a fuction that is being called.

### Step out
`Shift + F11` or `Command + Shift + ;`

Moves out of the current scope. Use it to escape a child function to return to the parent.

### Step
`F9`

## Watch
Add a variable and watch its value change as the code run. ⭐️

## Call stack
List of breadcrumbs leading to current point.

### Restart
`Call Stack > Right Click > Restart Frame`

Restarts the code from the beginning of that frame. Provides more navigability when tracing an issue.

## Console
While within the scope of a function, you can use the Console to access variables. ⭐️

Global variables are always accessible in the Console.
