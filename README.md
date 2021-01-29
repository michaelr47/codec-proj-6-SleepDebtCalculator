# codec-proj-6-SleepDebtCalculator
/*The program will determine the actual and ideal hours of sleep for each night of the last week.
It will calculate, in hours, how far you are from your weekly sleep goal. */


const getSleepHours = day => {
  switch (day) {
    case 'monday': 
     return 8
     break;
     case 'tuesday':
     return 4
     break;
     case 'wednesday':
     return 5
     break;
     case 'thursday': 
     return 7
     break;
     case 'friday':
     return 10
     break;
     case 'saturday':
     return 12
     break;
     case 'sunday': 
     return 8
     break; 
     default: 
     return 'Error!'
  }
};

const getActualSleepHours = () => getSleepHours('monday') + getSleepHours('tuesday') + getSleepHours('wednesday') + getSleepHours('thursday') + getSleepHours('friday') + getSleepHours('saturday') + getSleepHours('sunday');

const getIdealSleepHours = () => {
  let idealHours = 8;
   return idealHours * 7;
};

const calculateSleepDebt = () => {
 const actualSleepHours = getActualSleepHours();
 const idealSleepHours = getIdealSleepHours();

if (actualSleepHours === idealSleepHours) { 
 console.log('You got the perfect amount of sleep!');
} else if (actualSleepHours > idealSleepHours) {
  console.log('Wow, you got ' + idealSleepHours - actualSleepHours + ' more sleep then you needed!');
} else if (actualSleepHours < idealSleepHours) {
  console.log('You need to get some rest because you slept ' + (idealSleepHours - actualSleepHours) + ' hours less than you should have this week');
} else {
  console.log('Check your code!');
 }
};

calculateSleepDebt();
