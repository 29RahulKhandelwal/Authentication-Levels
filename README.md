# Authentication-Levels

## Level's
```
Level 1 - Username and Password Only
Level 2 - Encryption 
Add Environment Vars 
Level 3 - Hashing with md5 
Level 4 - Hashing and Salting with bcrypt 
Level 5 - Cookies and Sessions 
Level 6 - Google OAuth 2.0 Authentication 
```

## Server Starting Code

```
const express=require("express");
const app=express();
const mongoose=require("mongoose");

app.set("view engine","ejs");
app.use(express.urlencoded({extended:true}));
app.use(express.static("public"));

mongoose.connect("mongodb://localhost:27017/userDB",{useNewUrlParser:true,useUnifiedTopology:true});

app.listen(3000, function() {
  console.log("Server started on port 3000");
});

```
