# Training-Days
codecademy//beginners//js//practice
// The scope of `random` is too loose 
const name = 'Nayla';
const name2 = 'Warren';


const getRandEvent = () => {
  const random = Math.floor(Math.random() * 3);
  if (random === 0) {
    return 'Marathon';
  } else if (random === 1) {
    return 'Triathlon';
  } else if (random === 2) {
    return 'Pentathlon';
  }
};



// The scope of `days` is too tight 
const getTrainingDays = (event) => {
let days;
  if (event === 'Marathon') {
   days = 50;
  } else if (event === 'Triathlon') {
    days = 100;
  } else if (event === 'Pentathlon') {
    days = 200;
  }

  return days;
};

const event = getRandEvent();
const days = getTrainingDays(event);

// The scope of `name` is too tight 
const logEvent = (name, event) => {
  
  console.log(`${name}'s event is: ${event}`);
};

const logTime = (name, days) => {
 
  console.log(`${name}'s time to train is: ${days} days`);
};


// Define a `name` variable. Use it as an argument after updating logEvent and logTime 

const event2 = getRandEvent();
const days2 = getTrainingDays(event2);


logEvent(name, event);
logTime(name, days);
logEvent(name2, event2);
logTime(name2, days2);

const samerace = () => {
if (event === event2) { 
  console.log('They are running the same race. \nPlease select different races for the atheletes, as they can\'t be in the same race');
}
};

samerace();
