# flags #

Bourne shell flags are similar to booleans, in that they only have two possible states: set and not set.

I've tried to compile a comprehensive list of all you can do with flags; if you feel like something is missing feel free to make a pull request or open an issue.

### Bourne shell flags ###

This table of commandline flags has been loosely adapted from the Dash man-pages on Debian 8. I could not find license information on the man-page, so if you think I should add a footnote with further attribution please open an issue or send a PR.

flag |    name     | effect
-----|-------------|-------
a    | allexport   | Export all variables assigned to.
b    | notify      | Enable asynchronous notification of [background job completion](jobcontrol.md).
c    | noclobber   | Read commands from the command_string operand instead of from the standard input. Special parameter 0 will be set from the command_name operand and the [positional parameters](parameters.md) ($1, $2, etc.) set from the remaining argument operands.
e    | errexit     | If not interactive, exit if any command fails, unless it's explicitly tested with `if`, `elif`, `while`, or `until`; or if command is the left hand operand of an `&&` or `||` operator. To disregard whether a command succeeds with this flag set, append `|| true` to the command.
E    | emacs       | Enable the built-in emacs command line editor (disables -V if it has been set).
f    | noglob      | Disable pathname expansion.
i    | interactive | Force the shell to behave interactively.
I    | ignoreeof   | Ignore EOF's from input when interactive.
l    |             | Run as login shell.
m    | monitor     | Turn on [job control](jobcontrol.md) (set automatically when interactive).
s    | stdin       | Read commands from standard input (set automatically if no file arguments are present). This option has no effect when set after the shell has already started running (i.e. with set).
n    | noexec      | dIf not interactive, read commands but do not execute them. This is useful for checking the syntax of shell scripts.
u    | nounset     | Write a message to standard error when attempting to expand a variable that is not set, and if the shell is not interactive, exit immediately with a nonzero exit status.
v    | verbose     | The shell writes its input to standard error as it is read. Useful for debugging.
V    | vi          | Enable the built-in vi command line editor (disables -E if it has been set).
x    | xtrace      | Write each command to standard error (preceded by a +) before it is executed. Useful for debugging.


### Setting flags ###

Flags cannot be set to a value like normal [variables](variables.md); they have to be set with the `set` command.

You can set a flag by using `set -FLAG`, where FLAG is the letter of the relevant flag. Flags are unset in a very similar way, with `set +FLAG`.
