# Bonus Wagering Requirement Calculator

This repository contains the source code for a simple **Bonus Wagering Requirement Calculator** designed to help users calculate how much they need to wager based on a bonus amount and the wagering requirement percentage.

You can view and use the live version of the calculator at [Rehelliset Kasinot](https://rehellisetkasinot.com/).

## How It Works

The calculator takes two inputs:
1. **Bonuksen määrä (€)** (Bonus Amount): The amount of the bonus in Euros.
2. **Kierrätysvaatimus** (Wagering Requirement): The wagering requirement as a multiplier (e.g., 35x).

Once the user clicks the "Laske" (Calculate) button, it calculates the total amount that must be wagered to meet the requirement.

### Example:
If the bonus amount is €100 and the wagering requirement is 35, the calculator will return:


## HTML Code

The following is the main structure of the calculator:

### HTML Structure

```html
<div class="calculator-container">
    <h2>Laske bonuksen kierrätysvaatimukset</h2>
    <label for="bonusAmount">Bonuksen määrä (€):</label><br>
    <input type="number" id="bonusAmount" placeholder="Esim. 100€"><br><br>

    <label for="wageringRequirement">Kierrätysvaatimus:</label><br>
    <input type="number" id="wageringRequirement" placeholder="Esim. 35"><br><br>

    <button onclick="calculateWager()">Laske</button>

    <p id="result"><strong>Sinun täytyy panostaa yhteensä:</strong> - €</p>
</div>

JavaScript Functionality

function calculateWager() {
    var bonusAmount = parseFloat(document.getElementById("bonusAmount").value);
    var wageringRequirement = parseFloat(document.getElementById("wageringRequirement").value);
    var resultElement = document.getElementById("result");

    if (bonusAmount > 0 && wageringRequirement > 0) {
        var totalWager = bonusAmount * wageringRequirement;
        resultElement.innerHTML = "<strong>Sinun täytyy panostaa yhteensä:</strong> " + totalWager + " €";
    } else {
        resultElement.innerHTML = "Syötä kelvolliset arvot.";
    }
}

.calculator-container {
    max-width: 400px;
    margin: 20px auto;
    padding: 20px;
    background-color: #e3af64;
    border-radius: 10px;
    text-align: center;
    font-family: 'Akagi Pro', sans-serif;
    color: #000000;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

/* Additional styling for responsiveness, buttons, inputs, etc. */

Usage
To use this calculator:

Clone the repository or copy the HTML, CSS, and JavaScript code.
Embed the code directly into your webpage.
The calculator will display and calculate the required wager amount based on user inputs.
Live Example
You can see a live version of this calculator on the official website Rehelliset Kasinot.

License
This project is licensed under the MIT License. You are free to use, modify, and distribute the code.


### Key points of this README:
- **Description of the calculator**: I’ve summarized the purpose and use of the calculator.
- **Code structure**: The main HTML, JavaScript, and CSS sections are listed in the README for reference.
- **Usage**: Instructions on how to use the calculator code.
- **Live link**: The link to your live website is provided for users to test it.
- **License**: Added a placeholder for the license (feel free to modify or remove it if necessary).

You can customize the README further as needed. Let me know if you need any changes or additions!


