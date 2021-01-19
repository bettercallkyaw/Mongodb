```bash

use hospital

db.patients.insertOne({
    name:"htin kyaw",
    age:21,
    diseaseSummary:"summary-kyaw-1"
})

db.patients.drop()

db.patients.findOne().diseaseSummary

db.diseaseSummaries.insertOne({
    _id:"summary-kyaw-1",
    diseases:["cold","broken leg"]
})

var dsid=db.patients.findOne().diseaseSummary
dsid

db.diseaseSummaries.findOne({_id: dsid})

db.patients.deleteMany({})

db.patients.insertOne({
    name:'htin kyaw',
    age:21,
    diseaseSummary:{
        diseases:["head","broken leg"]
    }
})

---------------------------------------
_______________________________________

use carData

db.persons.insertOne({
    name:'htin kyaw',
    car:{
        model:'BMW',
        price:333333
    }
})

db.persons.insertOne({name:'htin kyaw',salary:3333333,age:21})

db.persons.insertOne({model:'BMW',price:444444,owner:ObjectId("5f46377385fcb1e50cd06b6e")})

---------------------------------------
_______________________________________

use support

db.questionThread.insertOne({
    creator:'htin kyaw',
    question:'how dare you?',
    answers:["q1q1","q2w3"]
})

db.questionThread.insertOne({
    creator:'udemy teacher',
    question:'can you done?',
    answers:[
        {text:'no problem'},
        {text:'thanks'}
    ]
})

db.answers.insertMany([
    {_id:"q1w2",text:"It is work"},
    {_id:"e22",text:"thanks"}
])

---------------------------------------
_______________________________________

use cityData

db.cities.insertOne({name:'New York',coordinates:{lan:21,lng:44}})

db.citizens.insertMany([
    {
        name:'htin kyaw',
        ctiyId:'raeiadai434ake'
    },
    {
        name:'william kyaw',
        cityId:'adekaea343eee'
    }
])

---------------------------------------
_______________________________________

use shop

db.products.insert({car:'BWM',price:444444})

db.customers.insertOne({name:'htin kyaw',age:33})

db.orders.insertOne({
productId:ObjectId('5f463f5f85fcb1e50cd06b75'),
customerId:ObjectId('5f463f6085fcb1e50cd06b76')})

db.customers.updateOne({},
{$set: {orders:[{title:'A book',price:333.33,quantity:33}]}})

---------------------------------------
_______________________________________

use bookRegistry

db.books.insertOne({
    name1:'My favorite books is kyaw',
    name2:'My favorite books is min',
    authors:[
        {
            name:'htin kyaw',
            age:21
        },
        {
            name:'min oo',
            age:20
        }
    ]
})

db.authors.insertMany([
    {
        name:'htin kyaw',
        age:21,
        addrees:{
            street:'Main'
        }
    },
    {
        name:'min oo',
        age:20,
        address:{
            street:'Bahan'
        }
    }
])

---------------------------------------
_______________________________________

use blog

db.users.insertMany([
    {
        name:'htin kyaw',
        age:21,
        email:'htinkyaw@gamil.com'
    },
    {
        name:'min oo',
        age:20,
        email:'min@yahoo.com'
    }
])

```