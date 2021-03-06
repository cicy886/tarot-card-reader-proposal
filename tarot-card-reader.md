Name of Student: Sisi Vieira

Name of Project: Tarot Card Reader

Project's Purpose or Goal: (What will it do for users?)
A tarot card reader for everyone. Users will be able to read the meaning of all the cards that were being selected.

List the absolute minimum features the project requires to meet this purpose or goal:

* The back of 78 tarot cards is listed on the webpage.
* Users will be able to flip the cards with a single click.
* Users will be redirected to the details page when they double-click the cards and read the full meaning of the cards.
* A button on the page “Select me and see how things are with you generally!”. When users click it, it will redirect them to a page with six random cards. Six cards indicate:
1. How you feel about yourself now
2. What you most want at this moment
3. Your fears
4. What is going for you
5. What is going against you
6. The outcome according to your current situation or the question you asked
* On the random page, users should be able to input their name, and what they’re wishing for.
* The random page should be able to shuffle the cards with their spread position or reversal position.
* On the random page, there should be a “Random” button to randomize another six cards.

What tools, frameworks, libraries, APIs, modules and/or other resources (whatever is specific to your track, and your language) will you use to create this MVP? List them all here. Be specific.
* React -- Create a single page app.
* Redux -- Manage state.
* APIs -- For the card readings https://github.com/ekelen/tarot-api
* Tarot Decks -- For the list of all the tarot cards 
1. https://xsj.699pic.com/lauthor/taluoka-3325457-1new/1.html or
2. https://www.bennionkearny.com/wp-content/uploads/2019/11/Tarot-Card-Deck.pdf
* CSS Obects -- Styling the app

If you finish developing the minimum viable product (MVP) with time to spare, what will you work on next? Describe these features here: Be specific.

* Users can log in and log off
* Users can sort the cards by their’ categories
* Users can pick the 6 random cards by themselves instead of generates by the app

What additional tools, frameworks, libraries, APIs, or other resources will these additional features require?

* Authentication -- Firebase

Is there anything else you'd like your instructor to know?

* It seems like I can use Firebase can use for authentications, but I'v heard it is not good to use with Redux? So if I really want to add authetications for the app, what do you recommend me to use?
* Is it possible to make the button as a tab? For example, instead of having a botton says “Select me and see how things are with you generally!”, can I make it a "Random" tap to redirect the users to the random page? Will it still be a single page app with React?

Additional sources for coding:

* React + Firebase/Firestore tutorial https://www.youtube.com/watch?v=jCY6DH8F4oc&ab_channel=PedroTech
* Make image to pixel art https://theimagekit.com/image-to-pixel
* Import mutipule images with one import https://www.youtube.com/watch?v=gEMAZSO85KY&ab_channel=WebStylePress
* Using useEffect to fetch data from the api https://www.youtube.com/watch?v=RVFAyFWO4go&t=3362s&ab_channel=DaveGray from 4:04:00 to 4:44:00
* Tutorial video for popup: https://www.youtube.com/watch?v=i8fAO_zyFAM&list=PLdoNE8-w7k0w3I0bCGKnUAdb1ilDsYmf0&index=2&t=765s&ab_channel=TylerPotts
* Card flip animation with css: https://www.youtube.com/watch?v=OV8MVmtgmoY&ab_channel=ArjunKhara
* Card flip animation project example: https://codesandbox.io/s/xovuw?file=/src/components/Card.jsx

Problem found:

* Only create script version 5.0.0 can show images correctly with custom import function.
* Pixeled tarot card are too blury to see, consider just use pixel arts as decorations for the app
* Need to think about how to connect api contents with corresponding images. With the import function, images don't have extra information, ie, names, id, etc. Thoughts about solving the problem: Discard the image import function, use the JSON file fetched from api and use it in the image link. For example: 
const image= require(`./../img/${card.name_short}.jpg`)
<img src = {image}>

* The selected card functionality was suppose to loop through an object within and object, so use cards[id] won't work. It needs to be cards.cards[id]
* react boostrap doesn't see working well with react router dom. Going to just use react router dom for the navbar
* Category page is basically the same as the home page. Maybe combine those two pages together.