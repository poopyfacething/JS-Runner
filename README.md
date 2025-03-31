# JS Runner

JS Runner is a simple web application that allows you to run JavaScript code in a browser. You can input your JavaScript code, click the "Run" button, and see the result in a new tab.

## Features
- **Run JavaScript**: Enter JavaScript code in the text area and execute it.
- **Fallback System**: If the primary script fails to load, a fallback URL is used to fetch the content.
- **Simple UI**: Clean, minimal interface with a focus on functionality.

## Usage

1. Open the `JS Runner.html` file in your browser.
2. Enter your JavaScript code in the provided text area.
3. Click the "Run" button to execute the code.
4. A new tab will open showing the result of the executed code.

## Demo

You can directly view the demo by clicking the following link:

[Open JS Runner Demo](data:text/html;charset=utf-8,%3C!DOCTYPE%20html%3E%0A%3Chtml%20lang%3D%22en%22%3E%0A%3Chead%3E%0A%20%20%20%20%3Cmeta%20charset%3D%22UTF-8%22%3E%0A%20%20%20%20%3Cmeta%20name%3D%22viewport%22%20content%3D%22width%3Ddevice-width%2C%20initial-scale%3D1.0%22%3E%0A%20%20%20%20%3Ctitle%3EJS%20Runner%3C%2Ftitle%3E%0A%3C%2Fhead%3E%0A%3Cbody%3E%0A%20%20%20%20%3Cscript%3E%0A%20%20%20%20%20%20%20%20document.addEventListener(%22DOMContentLoaded%22%2C%20()%20%3D%3E%20%7B%0A%20%20%20%20%20%20%20%20%20%20%20%20const%20main%20%3D%20%22https%3A%2F%2Fraw.githubusercontent.com%2Fpoopyfacething%2FJS-Runner%2Frefs%2Fheads%2Fmain%2FJS%2520Runner.html%22%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20const%20fallback%20%3D%20%22https%3A%2F%2Fraw.githubusercontent.com%2Fpoopyfacething%2FJS-Runner%2Frefs%2Fheads%2Fmain%2FJS%2520Runner_fallback.html%22%3B%20%2F%2F%20Define%20fallback%20URL%0A%0A%20%20%20%20%20%20%20%20%20%20%20%20fetch(main)%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20.then(response%20%3D%3E%20%7B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20if%20(!response.ok)%20throw%20new%20Error(%22Primary%20URL%20failed%22)%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20return%20response.text()%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%7D)%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20.catch(()%20%3D%3E%20%7B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20return%20fetch(fallback).then(response%20%3D%3E%20%7B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20if%20(!response.ok)%20throw%20new%20Error(%22Fallback%20URL%20failed%22)%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20return%20response.text()%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%7D)%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%7D)%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20.then(html%20%3D%3E%20%7B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20document.open()%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20document.write(html)%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20document.close()%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%7D)%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20.catch(error%20%3D%3E%20%7B%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20console.error(%22Error%20fetching%20HTML%3A%22%2C%20error)%3B%20%2F%2F%20Handle%20errors%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%7D)%3B%0A%20%20%20%20%20%20%20%20%7D)%3B%0A%20%20%20%20%3C%2Fscript%3E%0A%3C%2Fbody%3E%0A%3C%2Fhtml%3E%0A)