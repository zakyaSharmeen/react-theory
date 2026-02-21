//props destructure
✅ When is Event Binding used?

It is used when you attach a function to an event in JSX.

Example:
<button onClick={handleClick}>Click</button>

Here:

You are binding handleClick to the click event.

This happens when the component renders.

👉 Used whenever you want something to happen on:

Click

Change

Submit

Hover

etc.

✅ When is Synthetic Event used?

It is used automatically by React when the event actually happens.

When you click the button:

Browser creates a native event.

React wraps it inside a SyntheticEvent.

Your function receives that wrapped event.

Example:
function handleClick(e) {
console.log(e.target);
}

Here e is a SyntheticEvent.

👉 Used when:

You access e.target

You use e.preventDefault()

You use e.stopPropagation()

🔥 Super Short Difference

Event Binding → Connecting the function.

Synthetic Event → The event object React gives you when it runs.

Think like this:

Binding = setup time

Synthetic Event = runtime when user clicks
//////////////////////////////////////////////////////////////////////////////////////////////////

Code What Happens
onClick={handleClick} Runs when clicked ✅
onClick={handleClick()} Runs immediately ❌

/////////////////////////////rtk
//"Redux is a state container for managing global state.it requires a lot of boilerplate,
// Manual action + switch-case
// data flow--------
// Component
// → dispatch(action)
// → Reducer (switch-case)
// → Store updates state
// → UI re-renders
// ex
// Action
// const increment = () => ({ type: "INCREMENT" });
// // Reducer
// function counterReducer(state = { value: 0 }, action) {
// switch (action.type) {
// case "INCREMENT":
// return { value: state.value + 1 };
// default:
// return state;
// }
// }
