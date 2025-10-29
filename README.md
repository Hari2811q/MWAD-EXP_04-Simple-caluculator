# MWAD-EXP_04-Simple-caluculator
## Date:29?10/25

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
```
App.js
import React, { useState } from "react";
import "./App.css";

function App() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const handleClear = () => {
    setInput("");
  };

  const handleCalculate = () => {
    try {
      // eslint-disable-next-line no-eval
      const result = eval(input);
      setInput(result.toString());
    } catch (error) {
      setInput("Error");
    }
  };

  return (
    <div className="calculator-container">
      <div className="calculator">
        <input type="text" value={input} readOnly className="display" />

        <div className="buttons">
          <button onClick={handleClear} className="clear">
            C
          </button>
          <button onClick={() => handleClick("/")}>÷</button>
          <button onClick={() => handleClick("*")}>×</button>
          <button onClick={() => handleClick("-")}>−</button>

          <button onClick={() => handleClick("7")}>7</button>
          <button onClick={() => handleClick("8")}>8</button>
          <button onClick={() => handleClick("9")}>9</button>
          <button onClick={() => handleClick("+")}>+</button>

          <button onClick={() => handleClick("4")}>4</button>
          <button onClick={() => handleClick("5")}>5</button>
          <button onClick={() => handleClick("6")}>6</button>
          <button onClick={handleCalculate} className="equal">
            =
          </button>

          <button onClick={() => handleClick("1")}>1</button>
          <button onClick={() => handleClick("2")}>2</button>
          <button onClick={() => handleClick("3")}>3</button>
          <button onClick={() => handleClick("0")}>0</button>
          <button onClick={() => handleClick(".")}>.</button>
        </div>
      </div>
    </div>
  );
}

export default App;
```
```App.css

.calculator-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: linear-gradient(135deg, #c6ffdd, #fbd786, #f7797d);
  font-family: "Poppins", sans-serif;
}

.calculator {
  background-color: #222;
  padding: 20px;
  border-radius: 20px;
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.3);
  width: 320px;
  max-width: 90%;
}

.display {
  width: 100%;
  height: 60px;
  border: none;
  border-radius: 10px;
  background-color: #333;
  color: white;
  text-align: right;
  font-size: 2rem;
  padding: 10px;
  margin-bottom: 15px;
  outline: none;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 10px;
}

button {
  background-color: #444;
  color: white;
  font-size: 1.5rem;
  border: none;
  border-radius: 10px;
  padding: 15px;
  cursor: pointer;
  transition: all 0.2s ease-in-out;
}

button:hover {
  background-color: #666;
  transform: scale(1.05);
}

.clear {
  background-color: #ff5c5c;
}

.equal {
  background-color: #00b894;
  grid-column: span 1;
}

@media (max-width: 480px) {
  .calculator {
    width: 260px;
  }

  button {
    font-size: 1.2rem;
    padding: 12px;
  }

  .display {
    font-size: 1.5rem;
  }
}
```

## OUTPUT

<img width="1721" height="1038" alt="image" src="https://github.com/user-attachments/assets/6d1bbdd0-e6a8-4201-b0e9-431c0ceab1a9" />
<img width="1591" height="1078" alt="image" src="https://github.com/user-attachments/assets/2be3e4d6-3de0-4074-b8dc-70c3c62f655f" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.
