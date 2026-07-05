# Men Stack Notes
| CRUD Action | RESTful Action | HTTP Method | Definition |
| ----------- | -------------- | ----------- | ------------------------ |
| Create | `new` | `GET` | Show a form to create a new item |
| Create | `create` | `POST` | Add a new item to the database |
| Read | `index` | `GET` | Show all items |
| Read | `show` | `GET` | Show one specific item |
| Update | `edit` | `GET` | Show a form to edit an existing item |
| Update | `update` | `PUT` | Save changes to an existing item |
| Delete | `delete` | `DELETE` | Remove an item from the database |

# Setup 
- create a directory 
- create server file and i like to format my code `touch server.js`
- initialize aq node project with `npm init -y`
- install express `npm i express`

### Write Server Boilerplate 
```js
// bring express into our server
const express = require('express') //u should use the express code i give 

// actually use express
const app = express()

//listen takes 2,
app.listen(3000,function(){
    console.log('Listening on port 3000')
})

```

Run the server with `nodemon server.js`

Navigate to `http://localhost:3000` to view our server

Use `ctrl + c` to stop the server in the terminal

### Creating a Test Route

```js
app.get('/test', function(req, res) {
    res.send('this is a test ✨')
})
```
<img width="330" height="145" alt="Screenshot 2026-07-05 at 12 30 29 PM" src="https://github.com/user-attachments/assets/5afaaa31-7117-4e82-99cf-79316aed6b9a" />

Navigate to `http://localhost:3000/test`

### Using request parameters 
```js
app.get('/:userId', function(req, res){
    res.send(`Hello user number:${req.params.userId}`)
    console.log(req.params.userId)
})
```
Navigate to `http://localhost:3000/2490`

<img width="532" height="179" alt="Screenshot 2026-07-05 at 2 12 17 PM" src="https://github.com/user-attachments/assets/4a428ac3-5fdd-4917-ab90-38e9cd39fad3" />
