# Creating local site manually

1. Create directory to store your content:
    ```bash
    mkdir $HOME/localwebsite
    ```
2. Create a sample web-page in this directory:
    ```bash
    mousepad $HOME/localwebsite/index.html
    ```
3. Write the following HTML code into this file:
    ```
    <html>
        <body>
            <center>
                <h1>Hello, PLACE_YOUR_NAME_HERE!</h1>
                <img src="logo.svg" alt="GD logo">
            </center>
        </body>
    <html>
    ```
4. Replace `PLACE_YOUR_NAME_HERE` with your name.
5. Place image (GD logo) into site's directory:
    ```bash
    cp $HOME/logo.svg $HOME/localwebsite
    ```
6. Run your site with the following command:
    ```bash
    sudo docker run --rm -p 8080:80 -v $HOME/localwebsite:/usr/share/nginx/html:ro nginx
    ```
7. Run web-browser and go to http://localhost:8080/
8. Interminal window press `Ctrl+C` to stop local web server.
