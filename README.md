###So it's not exactly smooth starting....
###Steps to run:
####1. use docker compose 
```javascript
docker-compose up --build
```
####2. Restart nginx container singley (If homepage does not render)
####3. Possibly need to restart api container also (if no "Indexes I have seen" values show)

If you get some weird shitty errors from nginx, restart docker desktop and do another compose down & up 
(you might then still have to restart nginx container)