Starts two nginx instances.
nginx1 (port 8000) is started with default settings.
nginx2 (port 8001) is started with CORS settings (Access-Control-Allow-Origin: *)


***with CORS error***

1. docker-compose up
2. Browse to localhost:8000, press the button and it will make a request to localhost:8001/file.json
3. You will get a CORS error


***without CORS error***

1. edit docker-compose.yml and remove the comment on the last line
2. docker-compose up # nginx2 is now started with CORS nginx configuration
3. Browse to localhost:8000, press the button and it will make a request to localhost:8001/file.json
4. You will now get the content from file.json displayed on the page
