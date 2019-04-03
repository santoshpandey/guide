---
title: Never Mutate State
---
## Never Mutate State

const immutableReducer = (state = todos, action) => {
  switch(action.type) {
    case ADD_TO_DO:
      // don't mutate state here or the tests will fail
      // Can be used anyone from below
      const tasks = state.concat(action.todo);    // using concat concat doesnt mutate the original array and always return new array
      const tasks = [...state, action.todo]       // Using Spread operator 
      return tasks
    default:
      return state;
  }
};
