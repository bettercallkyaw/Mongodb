```bash

mongoimport tv-shows.json -d movieData -c movies --jsonArray --drop

db.movies.find({runtime:{$ne:60}}).pretty()

db.movies.find({runtime:{$lt:40}}).pretty()

db.movies.find({'rating.average':{$gt:7}}).pretty()

db.movies.find({genres: ["Drama"]}).pretty()

db.movies.find({runtime: {$inc: [30,42]}}).pretty()

db.movies.find({runtime: {$nin: [30,42]}}).pretty()

db.movies.find({$or: [{"rating.average": {$lt: 5}},{"rating.average": {$gt: 9.3}}]}).pretty()

db.movies.find({$and: [{"rating.average": {$gt: 9}},{genres: "Drama"}]}).pretty()

db.movies.find({$and: [{"rating.average": {$gt: 9}},{genres: "Drama"}]}).count()

db.movies.find({"rating.average": {$gt: 9},genres: "Drama"}).count()

db.movies.find({genres:"Drama",genres:"Horror"}).count()

db.movies.find({$and: [{genres: "Drama"},{genres: "Horror"}]}).count()

db.movies.find({runtime: {$not: {$eq: 60}}}).count()

db.movies.find({summary: "musical"}).pretty()

db.movies.find({summary: {$regex: /musical/}}).pretty()

db.moviestarts.find({genre: ["action","thriller"]}).pretty()

db.moviestarts.find({genre:{$all: ["action","thriller"]}}).pretty()

db.movies.find({genres:"Drama"},{"genres.$": 1}).pretty()

db.movies.find({genres: {$all: ["Drama","Horror"]}},{"genres.$": 1}).pretty()

db.movies.find({genres: "Drama"}, {genres: {$elemMatch: {$eq: "Horror"}}}).pretty()

db.movies.find({"rating.average":{$gt: 9}},{genres: {$slice: 2},name: 1}).pretty()

db.movies.find({},{name: 1, genres: 1,runtime: 1,rating: 1}).pretty()

```