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

```js
const mongoose = require('mongoose');
mongoose.connect('mongodb://localhost:27017/test', {useNewUrlParser: true});

const Cat = mongoose.model('Cat', { name: String });

const kitty = new Cat({ name: 'Zildjian' });
kitty.save().then(() => console.log('meow'));

var mongoose = require('mongoose');
mongoose.connect('mongodb://localhost/test');

var db = mongoose.connection;
db.on('error', console.error.bind(console, 'connection error:'));
db.once('open', funciton() {
});

var kittySchema = new mongoose.Schema({
  name: String
});

var Kitten = mongoose.model('Kitten', kittySchema);

var slience = new Kittne({ name: 'Silence' });
console.log(silence.name);

kittySchema.methods.speak = function () {
  var greeting = this.name
    ? "Meow name is" + this.name
    : "I don't have a name";
  console.log(greeting);
}

var Kitten = mongoose.model('Kitten', kittySchema);


var fluffy = new Kitten({ name: 'fuffy' });
fluffy.speak();

fluffy.save(function (err, fluffy) {
  if (err) return console.error(err);
  fluffy.speak();
});

Kitten.find(function (err, kittens) {
  if (err) return console.error(err);
  console.log(kittens);
});

Kitten.find({ name: /^fluff/ }, callback);

// api https://mongoosejs.com/docs/api.html#mongoose_Mongoose
Thing.findOne().select('name').exec(function (err, doc) {
  doc.isSelected('name')
  doc.isSelected('age')
})

```


