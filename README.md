Tom's Translator 🌎

Tom's Translator is a simple web app that allows you to translate text between different languages using Google Translate API. 🚀

## How it works

The code consists of three main parts: the HTML template, the CSS style sheet and the Python script.

- The HTML template (`index.html`) defines the structure and layout of the web page. It uses Jinja syntax to render the variables and loops passed from the Python script. It also includes a form with two select elements and two text areas for the input and output of the translation. The form sends a POST request to the same URL when the user clicks on the "Translate" button.
- The CSS style sheet (`style.css`) defines the appearance and formatting of the web page. It sets the background color, font family, font size, text alignment, margin, padding, border, box shadow and other properties for the elements in the HTML template.
- The Python script (`app.py`) defines the logic and functionality of the web app. It uses Flask framework to create and run a web server that handles the requests from the browser. It also uses Googletrans library to access and use the Google Translate API. The script does the following steps:
  - Import Flask, render_template, request, LANGUAGES and Translator modules.
  - Create an instance of Flask class and assign it to a variable named `app`.
  - Create an instance of Translator class and assign it to a variable named `translator`.
  - Define a route decorator for the root URL (`/`) and specify that it accepts both GET and POST methods.
  - Define a function named `index` that handles the requests for the root URL.
  - Initialize an empty string variable named `translated_text`.
  - Check if the request method is POST.
  - If yes, get the values of `text`, `src_lang` and `dest_lang` from the form data using `request.form` dictionary.
  - If `text` is not empty, call the `translate` method of `translator` object with `text`, `src_lang` and `dest_lang` as arguments and assign the returned object to a variable named `translation`.
  - Get the value of `text` attribute from `translation` object and assign it to `translated_text` variable.
  - Return the result of calling `render_template` function with `index.html`, `translated_text` and `languages` as arguments. This will render the HTML template with the values of these variables.
  - If no, return the same result as above but with an empty string for `translated_text`.
  - Define a special variable named `__name__` that holds the name of the current module.
  - Check if the value of `__name__` is equal to `"__main__"`. This means that the script is executed directly and not imported by another module.
  - If yes, call the `run` method of `app` object to start the web server.

## Installation and Usage

To use Tom's Translator, you need to have Python 3 and pip installed on your system. You also need to get a Google Translate API.

Clone this repository or download the zip file. 📥
Navigate to the project directory and create a virtual environment: python3 -m venv venv 🗂️
Activate the virtual environment: source venv/bin/activate 🔌
Install the required packages: pip install -r requirements.txt 📦
Open your browser and go to http://localhost:5000 🌐
Enter the text you want to translate in the first text area and select the source and target languages from the drop-down menus. ✍️
Click on the “Translate” button and see the translation in the second text area. 👀


Authors and Contributors
This project was coded by me as part of my AI specialization project. You can contact me on LinkedIn or Github. 👋

If you want to contribute to this project, feel free to fork this repository and make a pull request. 💻

Resources
For more information about this project, you can check out these resources:

Google Translate API documentation 📚
Flask documentation 📚
Jinja documentation 📚
