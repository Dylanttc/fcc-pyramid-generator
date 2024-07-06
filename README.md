# Pyramid Generator

This is the first lesson of freeCodeCamp's javascript course. I learnt fundamental programming concepts in JavaScript by building a Pyramid Generator.

## What I Learned

### JavaScript Basics

- **Variables:**
  - `const character = "#";` - This sets the character for building the pyramid.
  - `const count = 8;` - This sets the number of rows in the pyramid.
  - `let inverted = true;` - This decides if the pyramid is upside down.

- **Arrays:**
  - `const rows = [];` - An empty array to store each row of the pyramid.

- **Functions:**
  - The `padRow` function makes a single row of the pyramid with spaces and the character.
    ```javascript
    function padRow(rowNumber, rowCount) {
      return " ".repeat(rowCount - rowNumber) + character.repeat(2 * rowNumber - 1) + " ".repeat(rowCount - rowNumber);
    }
    ```

- **Loops:**
  - A `for` loop to build each row of the pyramid.
    ```javascript
    for (let i = 1; i <= count; i++) {
      if (inverted) {
        rows.unshift(padRow(i, count));
      } else {
        rows.push(padRow(i, count));
      }
    }
    ```

- **String Methods:**
  - `" ".repeat(n)` - Makes a string with `n` spaces.
  - `character.repeat(n)` - Makes a string with `n` characters.

- **Array Methods:**
  - `rows.unshift(element)` - Adds a new row at the beginning.
  - `rows.push(element)` - Adds a new row at the end.

- **Template Literals:**
  - Putting together the final output string with newlines.
    ```javascript
    let result = "";
    for (const row of rows) {
      result = result + "\n" + row;
    }
    ```

- **Console Output:**
  - `console.log(result);` - Prints the pyramid to the console.
