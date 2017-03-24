# Message Board

This application allows user to post questions and answers on the subject of Peruvian cuisine. Any user can submit a question and other users can respond with answers.

## Prerequisites

You will need the following things properly installed on your computer.

* [Git](https://git-scm.com/)
* [Node.js](https://nodejs.org/) (with NPM)
* [Bower](https://bower.io/)
* [Ember CLI](https://ember-cli.com/)
* [PhantomJS](http://phantomjs.org/)

## Installation

* `git clone <repository-url>` this repository
* `cd bustle`
* `npm install`
* `bower install`
*  `npm install -g ember-cli`
* `ember install emberfire`
* `ember install ember-bootstrap`

## Planning and structure to build my project

* Create folder project: ember new board
* do correspondent installation mentioned above inside of my board folder.
* generate my two models: question, answer.
* add attributes to models.
  ** question.js: author, content, notes, answers(hasMany).
  ** answer.js: author, content, question(belongsTo)
* create project in Firebase and get API key.
* modify environment.js based on firebase configuration.
* create questions.json, hard code data for questions and answers.
* import data json in Firebase and change 'rules' to 'true'.
* generate my two ember routes: index and question.

  - Index template will include the component question-tile.hbs a button to add a new question(that will come from new-question.hbs), which will to display the questions and its authors.

  - index.js will findAll from model() and have save action(that will come from new-question component).

  * new-question.hbs: form to add a new question in the form with save button.

  * new-question.js: actions to show form and to save new question.

  - Question template will display a particular question with additional information, update/delete the question and display the answers that belong to that question.

  - question.js will findRecord through question_id and will handle the actions for updating, saving and deleting question.

* generated components: question-tile, new-question, question-detail, update-question, answer-tile, new-answer.

* build a consistent header, navbar and footer for all pages through application.hbs

## Running / Development

* `ember s`
* Visit your app at [http://localhost:4200](http://localhost:4200).

### Code Generators

Make use of the many generators for code, try `ember help generate` for more details

### Running Tests

* `ember test`
* `ember test --server`

### Building

* `ember build` (development)
* `ember build --environment production` (production)

## Known Bugs

* If you find errors in this program or files, please let me know. Your suggestions will be appreciated and taken in consideration.

## Technologies Used
  * HTML
  * CSS
  * Bootstrap
  * Javascript
  * jQuery
  * Node.js
  * npm
  * bower
  * Sass
  * Ember.js

## Further Reading / Useful Links

* [ember.js](http://emberjs.com/)
* [ember-cli](https://ember-cli.com/)
* Development Browser Extensions
  * [ember inspector for chrome](https://chrome.google.com/webstore/detail/ember-inspector/bmdblncegkenkacieihfhpjfppoconhi)
  * [ember inspector for firefox](https://addons.mozilla.org/en-US/firefox/addon/ember-inspector/)
