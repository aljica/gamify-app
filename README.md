# Description of Project

## Short Description of Project

This project aims at creating a hub of two different games which is meant to bring people together online. Players login with their Spotify accounts, and are redirected to a welcome page. There, they can either create their own room or join an existing room. In a room, they can invite their friends to play one of two different music-related quiz games, some of which use Spotify to play audio tracks or retrieve personal information from Spotify about the user (with their consent, of course).
The games are: 
- Song guess: Here the user listen to a song and have to choose the correct title of it
- Music quiz game: Here the user will respond to questions to test their  general knowledge in music


## Project File Structure

- src/index.js: project entry point.
- src/reportWebVitals.js: setup code.
- gamify/public/\_: setup code.
- gamify/\_: setup code, gitignore, eslint & prettier for correct code styling. Config files.

* src/api/opentriviadb/opentriviadb.js: contains api calls to opentriviadb (which returns a question and 4 possible answers, one of which is correct. Used in the Music Quiz Game. also contains api
* api/spotify/spotify.js: contains api calls to spotify, currently only to authenticate the user. Will expand to also include retrieving information about user music tastes (most played songs, playlists etc) or whatever is necessary for the other games.

* src/app/app.jsx: the app itself, where routing is done etc.
* app/showPresenter.jsx: Used in app.jsx to show hashes correctly etc.

* app/gameInterface/Player.jsx: an individual player object.
* app/gameInterface/game.css: css for the game.
* app/gameInterface/resultsPresenter.jsx: presenter for the resultsView
* app/gameInterface/resultsView: View showing the results of a game

* app/homepage/welcomeView: view of the welcome page (the one user is redirected to after logging in.
* app/homepage/welcomePresenter: presenter of the welcomeView.
* app/homepage/createPresenter.jsx: depending on the state, shows either a game or a join view (the lobby of a room).
* app/homepage/gamePresenter.jsx: shows either the lobby of a room or the game view, depending on current state.
* app/homepage/game.css: css styling.

* app/lobby/lobbyview.jsx: The lobby view of a room.
* app/lobby/lobbyPresenter.jsx: presenter of lobby view.
* app/lobby/lobby.css: css styling for the lobby.

* app/login/loginView.jsx: login view.
* app/login/loginPresenter.jsx: presenter of login view.
* app/login/login.css: css styling for login page.

* app/reusable_components/choiceButton/choiceButtonView.jsx: the view for a choice button, consider it a button component.
* app/reusable_components/choiceButton/choiceButton.css: css styling of button component.
* app/reusable_components/game/gamePresenter.jsx: the presenter of a game, which shows a question and choice buttons.
* app/reusable_components/game/questionView.jsx: shows a game question.

* src/assets/css/global.css: global css styling used by different views.
* assets/fonts/\_: fonts.
* assets/images/\_: images.
* assets/audio/nyc.mp3: the audio sound played in the question game 

* src/data/firebase/firebase.js: communicating with firebase and modifying the database.
* data/firebase/firebaseUtils.js: communicating with firebase and modifying the database.
* data/model/model.js: a class which each connected user instantiates, with their unique information (such as which roomID they're in, their login tokens etc).
* data/model/message.js: to send data from the model to the observers.


# How to setup the app
- Download the app folder in the main branch
- On your conputer open the terminal in the ```Gamify``` folder
- Install, the dependencies of the application by running ```npm install``` in the terminal
- Once the dependencies installed, run the application locally by running the command ```npm start```
- You can now access the application on your browser at the addresss indicated by create-react-app on your terminal

