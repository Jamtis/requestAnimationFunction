# requestAnimationFunction

A wrapper for `requestAnimationFrame`, supports "permanent arguments" and "overridable arguments" mode.

Here the first event is used for the invocation.
```
import requestAnimationFunction from "...";

const update_once_per_frame = requestAnimationFunction(async (event) => {
  \\ do stuff
});
// update_once_per_frame is a async function

addEventListener("update_stuff", update_once_per_frame);
```

Here the most current argument is used.
```
import requestAnimationFunction from "...";

const log_newest_once_per_frame = requestAnimationFunction(argument => {
  console.log("current state", argument);
}, true);

addEventListener("update-state", state => log_newest_once_per_frame(state));
```
