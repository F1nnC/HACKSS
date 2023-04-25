<html>
    <head>
    <link rel="stylesheet" href="extra.css">
    </head>
    <body>
<div class="index-header">
    <h1>Extra Seed: Random Joke getter with bootstrap table</h1>
<table class="table">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">Joke</th>
    </tr>
  </thead>
  <tbody>

  </tbody>
</table>
</div>
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/lodash.js/4.17.21/lodash.min.js"></script>

<script>
  // Define an array of jokes
  const jokes = [
    "Why don't scientists trust atoms? Because they make up everything!",
    "What do you call a fake noodle? An impasta!",
    "Why couldn't the bicycle stand up by itself? Because it was two-tired!",
    "Why do seagulls fly over the sea? Because if they flew over the bay, they'd be bagels!",
    "Why did the golfer wear two pairs of pants? In case he got a hole in one!",
    "Why do elephants never use computers? Because they're afraid of mice!",
    "What did the janitor say when he jumped out of the closet? 'Supplies!'",
    "Why did the picture go to jail? Because it was framed!",
    "Why did the hipster burn his tongue? He drank his coffee before it was cool.",
    "What do you get when you cross a snowman and a shark? Frostbite!",
    "Why don't oysters give to charity? Because they're shellfish!",
    "Why don't skeletons fight each other? They don't have the guts!",
    "Why did the tomato turn green? Because it was green with envy!",
    "Why did the vampire go to art school? He wanted to learn how to draw blood!",
    "Why did the bicycle fall over? Because it was two-tired!",
    "Why did the cookie go to the doctor? Because it was feeling crummy!",
    "Why did the banana go to the doctor? Because it wasn't peeling well!",
    "Why did the duck go to the doctor? Because it was feeling a little down!",
    "Why did the chicken cross the road? To get to the other side!",
    "Why don't ghosts use elevators? They lift their spirits!",
    "Why did the scarecrow win an award? Because he was outstanding in his field!",
    "Why do we tell actors to 'break a leg'? Because every play has a cast!",
    "What did the grape say when it got stepped on? Nothing, it just let out a little wine.",
    "What do you call an alligator in a vest? An investigator!",
    "Why did the computer go to the doctor? Because it had a virus!"
];


  // Get the table body element
  const tbody = document.querySelector('tbody');

  // Shuffle the jokes array using Lodash
  const shuffledJokes = _.shuffle(jokes);

  // Loop through the table rows and add a joke to each row
  for (let i = 1; i <= 3; i++) {
    // Get the i-th joke from the shuffled array
    const joke = shuffledJokes[i - 1];
    
    // Create a new table row and cell elements
    const tr = document.createElement('tr');
    const tdNumber = document.createElement('td');
    const tdJoke = document.createElement('td');

    // Set the text content of the row and cell elements
    tdNumber.textContent = i;
    tdJoke.textContent = joke;

    // Append the cell elements to the row element
    tr.appendChild(tdNumber);
    tr.appendChild(tdJoke);

    // Append the row element to the table body element
    tbody.appendChild(tr);
  }
</script>
