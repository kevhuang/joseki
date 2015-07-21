#### Frontend

- Architected the app following the Flux architecture—created the working folders and most of the files under client/public/js
- Set up Bootstrap framework for menu navbar, main content body, and footer for the main App component (client/public/js/components/App.js)
- Added feature to allow users to toggle mode in App component (lines 118 and 273–275)
- Wrote most of the code for retrieving and displaying events (EventList component calls EventActions, which then calls the EventAPI utility to retrieve the event data and pass to the AppDispatcher to distribute, and the EventStore would listen for the data and store it, and then emit an event to the registered EventList component to inform it of new data)
- Similarly, wrote the functionality to create events with EventCreate.js as the React component and followed the similar process as above for Flux (actions, stores, API utils)
- Implemented modal functionality using Bootstrap in client/public/js/components/ObservationList/ObservationListItem.js (lines 15–26 and 33–36)
- Did a good portion of the CSS styles (client/public/assets/css/app.css)

#### Backend
- Set up the "react" and "build" Gulp tasks in Gulpfile.js to automatically bundle and rebuild the React and Flux JavaScript files for the frontend
- Wrote all of server/db/index.js to set up the PostgreSQL data models and relations
- Implemented most of the API endpoints in server/api/event/index.js
- Iterated on and added error handling for observation API endpoints in server/api/observation/index.js
- Added all the integration tests for the event and observation API endpoints in server/test/