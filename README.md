# Isjianne Dumlao - Age Checker

A simple JavaScript program that tells you how your favorite artist's age compares to Google.

---

## How It Works

1. Enter the **age** of your favorite artist in the input field.
2. Click **Check Age**.
3. See the message telling you whether they are younger, as old, or older than Google (25 years).

---

## JavaScript Code

```javascript
// Get references to input and result elements
const ageInput = document.getElementById('ageInput'); // Grabs the input box
const result = document.getElementById('result');    // Grabs the div where the result will show

// Function to check the age
function checkAge() {
  const age = parseInt(ageInput.value); // Converts the input value to a number

  // Check if input is valid
  if (!age) {
    result.textContent = "Please enter a valid age!"; // Shows error message
    return;
  }

  // Conditional statements to compare age
  if (age < 25) {
    result.textContent = `They are ${age}, and they're younger than Google.`; // Age less than 25
  } else if (age === 25) {
    result.textContent = `They are ${age}, and they're as old as Google.`; // Age equals 25
  } else {
    result.textContent = `They are ${age}, and they're older than Google.`; // Age greater than 25
  }
}
