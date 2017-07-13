Exercise 1
////////////////////////////////////////////////////////////////////////////////
var lastWord = 'welcome';
console.log(lastWord);
lastWord = 'goodbye';

Log returns 'welcome'
////////////////////////////////////////////////////////////////////////////////
var message = "Up here!";

function shout() {
  console.log(message);
}

shout();

Log returns 'Up here!'
////////////////////////////////////////////////////////////////////////////////
var message = "Up here!";

function shout(message) {
  console.log(message);
}

shout("Down below!")

Log returns 'Down below!'
////////////////////////////////////////////////////////////////////////////////
var muffins = 'two dozen';
var purchasedMuffins;

function getMuffins() {
  return muffins;
}
purchasedMuffins = getMuffins();
console.log(purchasedMuffins);

Log returns 'two dozen'
////////////////////////////////////////////////////////////////////////////////
var chore = 'laundry';

function doChores() {
  var chore = 'sneak out';

  function reportActivity() {
    console.log(chore);
  }

  reportActivity();
}

doChores(); // calling doChores(), which then calls reportActivity()

Log returns 'sneak out'
////////////////////////////////////////////////////////////////////////////////
var letter;
var contents = 'Looking for gold';

function getMail() {

  function changeContents() {
    var contents = 'Struck it rich!';
  }

  changeContents();
  return contents;
}

letter = getMail();
console.log(letter);

Log returns 'Looking for gold'
////////////////////////////////////////////////////////////////////////////////
var decision;

function firstIdea() {
  var decision = 'Buy a new car';
  return decision;
}

function secondIdea() {
  console.log(decision);
}

firstIdea();
secondIdea();

Log returns 'undefined'
////////////////////////////////////////////////////////////////////////////////
Exercise 2
////////////////////////////////////////////////////////////////////////////////
Problem 1
////////////////////////////////////////////////////////////////////////////////
function buildHouse(address) {
  // ... house gets built
  return 'Building house at ' + address;
}
buildHouse('123 Happy St.');
console.log(address);

Log returns 'ReferenceError: address is not defined'
////////////////////////////////////////////////////////////////////////////////
Problem 1 Rewrite
////////////////////////////////////////////////////////////////////////////////
function buildHouse(address) {
  // ... house gets built
  return 'Building house at ' + address;
}
address = buildHouse('123 Happy St.');
console.log(address);
////////////////////////////////////////////////////////////////////////////////
