# Basic-Extercises
rock paper scissors

const getUserChoice = userInput => {
userInput = userInput.toLowerCase();
if (userInput === 'rock' || userInput === 'paper' || userInput === 'scissors') {
  return userInput;
} else {
  console.log('Error! not a valid choice');
}
};

console.log(getUserChoice('Rock'));
console.log (getUserChoice('pickle'));

const getComputerChoice = () => {
  const randomNumber = Math.floor(Math.random() * 3);
  switch (randomNumber) {
  case 0:
    return 'rock';
  case 1:
    return 'paper';
  case 2:
   return 'scissors';
   }
};

const determineWinner = (userChoice, computerChoice) =>{
if (userChoice === computerChoice){
  return 'This game is a tie';
  }
  if(userChoice ==='rock'){
    if(computerChoice === 'paper'){
      return "Computer Victory";
    } else {
      return 'Flawless Victory';
      }
    }

if (userChoice === 'paper'){
  if( computerChoice === 'scissors'){
    return 'You Will Never Win';
  } else {
    return 'Flawless victory!';
  }
}

  

if (userChoice === 'scissors'){
  if( computerChoice === 'rock'){
    return 'You Will Never Win';
  } else {
    return 'Flawless victory!';
    }
}

};

const playGame = () => {
  const userChoice = getUserChoice ('paper');
  const computerChoice = getComputerChoice ();
  console.log ('You Struck:' + userChoice)
  console.log ('Your enemy stuck:' + computerChoice);

  console.log(determineWinner(userChoice, computerChoice));

};
playGame();
