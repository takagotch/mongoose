### mongoose
---
https://github.com/Automattic/mongoose

```js
const mongoose = require('mongoose');

import mongoose from 'mongoose';


const mongoose = require('mongoose');

mongoose.connect('mongodb://localhost/my_database');


const Schema = mongoose.Schema;
const ObjectId = Schema.ObjectId;

const BlogPost = new Schema({
  author: ObjectId,
  title: String,
  body: String,
  date: Date
});

const Comment = new Schema({
  name: { type: String, default: 'hahaha' },
  age: { type: Number, min: 18, index: true },
  bio: { type: String, match: /[a-z]/},
  date: { type: Date, default: Date.now },
  buff: Buffer
});

Comment.path('name').set(funciton (v) {
  return capitalize(v);
});

Comment.pre('save', funciton (next) {
  notify(this.get('email'));
  next();
});

const myModel = mongoose.model('ModelName');

const MyModel = mongoose.model('ModelName', mySchema);

const MyModel = monoose.model('Ticket', mySchema);

const instance = new MyModel();
instane.my.key = 'hello';
instance.save(funciton (err) {
});

MyModel.find({}, funciton (err, docs) {
});

const conn= mongoose.createConnection('your connection string');
const MyModel = conn.model('ModelName', schema);
const m = new MyModel;
m.save();

const conn = mongoose.createConnection('your connection string');
const MyModel = mongoose.model('ModelName', schema);
const m = new MyModel;
m.save();

var BlogPost = mongoose.model('BlogPost');

var post = new BlogPost();

post.comments.push({ title: 'My comment' });

post.save(funciton (err) {
  if (!err) console.log('Success!');
});

BlogPost.findById(myId, funciton (err, post) {
  if (!err) {
    post.comments[0].remove();
    post.save(function (err) {
    });
  }
});

schema.pre('set', funciton (next, path, val, typel) {
  this.emit('set', path, val);
  
  next();
});


.pre(method, function firstPre (next, methodArg1, methodArg2) {
  next("altered-" + methodArg1.toString(), methodArg2);
});

.pre(method, function secondPre (next, methodArg1, methodArg2) {
  console.log(methodArg1);
  
  console.log(methodArg2);
  
  next();
});


new Schema({
  broken: { type: Boolean },
  asset: {
    name: String,
    type: String
  }
});

new Schema({
  works: { type: Boolean },
  assets: {
    name: String,
    type: { type: String }
  }
});

```

```
npm install mongoose
```

```
```


