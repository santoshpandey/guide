---
title: Send Action Data to the Store
---
## Send Action Data to the Store

This is a stub. <a href='https://github.com/freecodecamp/guides/tree/master/src/pages/certifications/front-end-libraries/redux/send-action-data-to-the-store/index.md' target='_blank' rel='nofollow'>Help our community expand it</a>.

<a href='https://github.com/freecodecamp/guides/blob/master/README.md' target='_blank' rel='nofollow'>This quick style guide will help ensure your pull request gets accepted</a>.
const notesReducer = (state = 'Initial State', action) => {
  switch(action.type) {
    // change code below this line
    case ADD_NOTE:
      return state = action.text
    // change code above this line
    default:
      return state;
  }
};

<!-- The article goes here, in GitHub-flavored Markdown. Feel free to add YouTube videos, images, and CodePen/JSBin embeds  -->
const addNoteText = (note) => {
  // change code below this line
    return {
      'type': ADD_NOTE,
      'text': note
    }
  // change code above this line
};
