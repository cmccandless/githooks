# githooks

Project-agnostic git hooks

## Install

1. Clone this repository
2. Add the following to any corresponding git hook to run the globals (making the appropriate substitution for $LOCATION_OF_CLONE):

```Bash
HOOK=$(basename $0)
GLOBAL_HOOKS_LOCATION=$LOCATION_OF_CLONE
if [ -f $GLOBAL_HOOKS_LOCATION/$HOOK ]; then
    $GLOBAL_HOOKS_LOCATION/$HOOK $@
fi
```
