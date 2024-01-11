# Authors
    BONFIM FRANÇA Louise
    DO PRADO GONÇALVES Laura
    ROSA FREIRE SOUSA Camilla
    VILLANOVA VECCHIO Gustavo

# Requirements
    Python3
    SASS (for scss)

# How to install SASS
    npm install -g sass

# How to run
    ./integration/compile_css.sh or sass --watch integration/style.scss:integration/assets/stylesheets/output.css
    python ./run_server.py

Now you just need to open https://localhost:8000

# How to run the backend server
The back end consists of a database with information on the clients, the employees, the products for sale and the orders made via the app.

To run it, simply acess the local terminal on the automacorp folder using IntelliJ and run the command

    .\gradlew bootRun

While it's executing, it's connected to the frontend. You can open the webpages and they should be getting the data from the API.

# Guide for user
For the home page, that's accesible to the clients, nothing is connected to the API. To find a usecase that encounters it, you must acess the private area for the owner and employees. 

Head to the footer of the home page to find a login. You need to have an employee email and password that is stored on the database, for example: .

From there, you're on the private section of the website. There you'll find:
- Insights for the app;
- A list of all orders and their status (for which you can filter the orders);
- A list of products and employees (that you can edit by adding a new one and removing or altering an existing one);
- A list of the clients that have an account on the app.

# Guide for developers

All of the information listed is coming from the API using Vue JS, as well as all the changes made to them.
- axios.get: To display the list of data (be it insights, orders, employees, products or clients) and to filter the orders;
- axios.put: To update the information;
- axios.delete: To remove the data.

- v-if: Used to display only a portion of the itens, as to not go over the borders of the page even if there are too many of them.
