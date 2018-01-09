# Flashcard-Generator

### Running the app

Run the following in node and follow the instructions:

```
node app.js
```

The first prompt asks you what the user would like to do. If the user chooses the add-flashcard option, user will be prompted to pick which type of flashcard they would like to create. The options will be basic-flashcard or cloze-flashcard. More information about these types below. Once the user has created the flashcard it will be appended to the log.txt file. The user will then be given the options create-new-flashcard, show-all-cards, nothing.  Create-new-flashcard will restart the flashcard creation process described above. Choosing the nothing option will end the app.

If the user chooses to show-all-cards, each of the flashcards will be displayed as a question (front) of the card. The user's response will be compared to the correct response (back) of the card. The user will be shown each card until there are no more cards. When they are exhausted the app will quit.

#### Basic Flashcard

A basic flashcard has a front and a back. A basic flashcard is created through a constructor BasicCard which takes two arguments: front and back, respectively. BasicCard has a create function which uses fs to append the flashcard to the log.txt file.

##### To create a new basic flashcard:

```
var newBasic = new BasicCard('What is your favorite color?`, 'Blue');
newBasic.create();
```

#### Cloze Flashcard

A cloze flashcard has a piece of text removed. A cloze flashcard is created through a constructor ClozeCard which takes two arguments: text and cloze, respectively. The ClozeCard has the property clozeDeleted, which takes the text and replaces the cloze portion with _____. ClozeCard also has a create function which uses fs to append the flashcard to the log.txt file.

##### To create a new cloze flashcard:

```
var newCloze = new ClozeCard('My favorite color is blue.`, 'blue');
newCloze.create();
```
