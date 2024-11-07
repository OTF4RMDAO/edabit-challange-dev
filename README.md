# edabit-challange-dev

This repository contains solutions to various Edabit development challenges, listed from the easiest to the most challenging. Each solution is implemented in JavaScript with brief explanations and examples.

1. CONVERT A NUMBER TO BASE-2 (BINARY)
DESCRIPTION:
Write a function that converts a base-10 number to a base-2 (binary) string.

SOLUTION:

function binary(num) {
    if (num === 0) return "0";
    return num.toString(2);
}

// Example usage:
console.log(binary(1));  // "1"
console.log(binary(5));  // "101"
console.log(binary(10)); // "1010"


EXPLANATION:
We use the toString(2) method to convert the number to a binary string.

2. ADD NAME TO OBJECT
DESCRIPTION:
Create a function that adds a key-value pair to an object. Given an object, a key (name), and a value, return the updated object.

SOLUTION:

function addName(obj, name, value) {
    obj[name] = value;
    return obj;
}

// Example usage:
console.log(addName({}, "Brutus", 300));                 // { Brutus: 300 }
console.log(addName({ piano: 500 }, "Brutus", 400));     // { piano: 500, Brutus: 400 }
console.log(addName({ piano: 500, stereo: 300 }, "Caligula", 440)); // { piano: 500, stereo: 300, Caligula: 440 }


EXPLANATION:
We use bracket notation obj[name] = value to add the new key-value pair and return the updated object.


3. FIND ANCESTORS AND OFFSPRING.
DESCRIPTION:
Create a function that, given a number x (generation) and a character y ("m" for male, "f" for female), returns the name of the ancestor or descendant.

SOLUTION:

function generation(x, y) {
    const generations = {
        "-3": { "m": "great grandfather", "f": "great grandmother" },
        "-2": { "m": "grandfather", "f": "grandmother" },
        "-1": { "m": "father", "f": "mother" },
        "0": { "m": "me!", "f": "me!" },
        "1": { "m": "son", "f": "daughter" },
        "2": { "m": "grandson", "f": "granddaughter" },
        "3": { "m": "great grandson", "f": "great granddaughter" }
    };
    
    return generations[x][y];
}

// Example usage:
console.log(generation(2, "f"));   // "granddaughter"
console.log(generation(-3, "m"));   // "great grandfather"
console.log(generation(1, "f"));    // "daughter"


EXPLANATION:
Using an object generations, we map each generation number and gender to its appropriate term, accessing the correct value with generations[x][y].


4. AGE CALCULATION IN DAY'S.
DESCRIPTION:
Given an age in years, return the age in days. This function assumes a non-leap year (365 days per year).

SOLUTION:

function calcAge(age) {
    return age * 365;
}

// Example usage:
console.log(calcAge(65)); // 23725
console.log(calcAge(0));  // 0
console.log(calcAge(20)); // 7300


EXPLANATION:
We multiply the age by 365 to get the age in days.
