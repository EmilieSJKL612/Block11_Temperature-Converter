# Yards to Meters

Let's build an interactive web application that will help users convert a number of yards into meters!

## Instructions

1. Clone this repository down to your local machine. This will not be submitted.
2. Open the cloned folder with VS Code.
3. Live serve `index.html`.
4. Choose one person in the group to share their screen.
5. Everyone else should follow along and type the answers on their own computers.
6. As a team, read each question out loud and reach a consensus on the answer before moving to the next question.

## Complete the documented functions

1. Connect the `index.js` file to the HTML. The rest of this guided practice will refer to `index.js`.
2. The multiline comment above the `convertToMeters` function is called JSDoc, which is a format for documenting JavaScript. What type of input does `convertToMeters` expect? => number (@param {number} yards, so the parameter is iexpecting type number abd the content should be yards) 
3. What is the type of the value that `convertToMeters` returns? => number
4. Complete `convertToMeters` so that it correctly converts the given yards into meters. => `function convertToMeters(yards) {return yards * 0.9144;}`
5. What is the name and type of `describeDistance`'s parameter? => name (content): yards ; type: number
6. What is `describeDistance`'s return type? => string
7. According to the JSDoc, what should `describeDistance(100)` return? => `Returns "100 yards is 91.44 meters, which is longer than a decameter!"`
8. What would `describeDistance(200)` return? => `Returns "200 yards is 182.88 meters, which is longer than a hectometer."`
9. Complete `describeDistance` so that it behaves as described in the JSDoc. First, convert the given yards to meters. Then, use a conditional statement to return the appropriate description. 
=> `function describeDistance(yards) {
    let meters = yards * 0.9144;
    if (meters > 1000) {console.log(`${yards} yards is ${meters} meters, which is longer than a kilometer.`)} 
    else if (meters > 100) {console.log(`${yards} yards is ${meters} meters, which is longer than a hectometer.`)}
    else if (meters > 10) {console.log(`${yards} yards is ${meters} meters, which is longer than a decameter.`)}
    else {console.log(`The distance is longer than a sandwich.`)}
}`


> [!TIP]
>
> One of the great things about functions is that they can be used in other functions! For example, `convertToMeters` can be called within the declaration of `describeDistance`.

## Interact with the user

This next snippet of code can live either above or below the function declarations. Your preference!

10. Prompt the user for a number of yards and store their answer in a variable named `yards`.
11. Pass `yards` into `describeDistance` and store the resulting value in a variable named `description`.
12. Display the description to the user with `alert`.
