# React Intro

* Start from the up-to-date main branch (`git checkout main; git pull origin main`)
* Create a feature branch named 'react-intro' (`git checkout -b react-intro`)
* Create a react application in this directory using Vite
* Create and modify the files in `src/` of the created project folder to fulfill the requirements below
* Add, commit, and push the branch to github
* Create a PR to merge to main
* Be sure to include the TA(s) and I as reviewers on the PR.  
* **Due by Sun Mar 31, 11:59pm PT**


## Goals

- Create a React application that is made up of multiple components
- Demonstrate an understanding of the `useState` hook
- Demonstrate an understanding of passing props, including handlers/setters to components
- Demonstrate an understanding of gathering input into state as it is entered
- Demonstrate an understanding of how to conditionally render content
- Be able to import non-React JS and use it inside a component
- Demonstrate an understanding of applying CSS to React components

## Assignment Goals and Requirements
- This application will test front-end code only
  - Nothing is sent to a service
  - No backend calculation is done
  - Refreshing the page will wipe all front end state and start over
- The application will ask a user to login, showing an input field for the username and a button
  - A username is allowlisted in the frontend code
    - Remember what "allowlisted" means
  - An invalid username will be shown a message that the username is not made up of valid characters
  - username "dog" will be shown a message saying they are not a valid user
- The application will ask the logged in user to input a 5 letter word and show an input field and a button
- A logged in user can log out
- When the button is clicked, the page will clear the input field AND display one of three messages:
  - If the input did not contain a 5 character word, the page will add the message "XXX was not a valid word", where XXX is what was in the input field
  - If the input did contain a 5 character word, but it was not the secret word, the page will say "XXX had N letters in common", where XXX is what was in the input field, and N is the number of letters in common with the secret word, using the same concepts from the compare code from section 1
  - If the input did contain a 5 character word, and it was identical (regardless of case) to the secret word, the page will say "XXX is the secret word!"
- Your code to compare letters between two words will be in a .js file and the function will be imported into a component
  - Hint: This code will have to use import/export syntax instead of require, so you will have to change your compare function from earlier
  - Hint: make sure you are importing the compare function from a .js file into a .jsx file
- The secret word is "RECAT" - just hardcode this to a variable
  - The secret word does not change in this assignment - there is no list of allowed words
  - Yes, "RECAT" - it's a cat/react joke
- Your application can be tested by entering the created directory and running `npm install` and `npm run dev`
### Structure
- The App component should load and conditionally render a Login component and a Game component
  - The App component should pass any necessary handler functions and/or setters to the Login and Game components
- The Login component handles the login form
- The Game component handles the form to make guesses
- These components may import and use other components as you wish
### Visuals
- Apply CSS to your components
  - Remember to use "className" instead of "class"
  - Remember to use lowercase classnames, not MixedCase, nor MixedCase-with-hyphens
- Make your application reasonably attractive
- Include enough space around items
- Have elements reasonably aligned
- This app does not have a lot of visuals, so make sure you do enough to show you understand
  - Hint: This means if you have not applied any meaningful styling beyond the default provided, you have NOT shown an understanding.  It does not have to be complex, but it does have to prove you can do it. 

## Restrictions
- Use only the libraries/packages installed by Vite and shown in class
- No server-side code
- All components must be .jsx files named in MixedCase
- Components should have good separation of concerns
  - not too large
  - not doing too much
  - same logic as splitting up functions
- Components should have good, accurate, meaningful names
- state values should have good, accurate, meaningful names
- Component filenames should match the component name
- Components must each be in a single file with no other exported values
- Logic that is not about JSX should be imported from .js files
- .js files and functions should have good, accurate, meaningful names

## Additional Requirements
- You may not use `document.querySelector()` or otherwise query or set the DOM directly outside of reading elements from event targets
- You may not use `useRef`, or `ref` props from React (If you do not know what I mean, that is fine)
- Follow the best practices described in class, in the code-review doc, and in the best-practices in the readings
- Use Semantic HTML as much as you can
- Follow any suggestions previously given to you in code reviews
- Do NOT include files in your PR that are outside the assignment (no IDE configs, `node_modules/`, etc)
  - Vite creates a .gitignore file that should handle the `node_modules/` file
  - Vite installs sample files in addition to required files.  Make sure you don't include sample files that you aren't using
    - `index.html` and `src/main.jsx` are required
    - `src/App.jsx` and other `.jsx`/`.css` files should be modified/replaced/deleted as appropriate
    - The images used in the example code should be removed
- Do not use external CSS libraries
- You may not use floats to do more than manage flowing text with images
- You may not use HTML tables or CSS table layouts
- You may not use Set() or Map() 
- You may not use CSS preprocessors, minifiers, or other tools to modify your CSS
  - I and the TA(s) must be able to read it easily
