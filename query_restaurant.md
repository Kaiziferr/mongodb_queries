1. Todos los restaurantes de la base de datos
	
	db.restaurant.find()

	db.restaurant.find().forEach(printjson)

2. Todos los restaurantes: únicamente los campos  restaurant_id ,  name ,  cuisine .


 	db.restaurant.find({}, {restaurant_id:1, name:1, cuisine:1})

3. Todos los restaurantes: únicamente los
campos  restaurant_id ,  name ,  zipcode  y SIN  _id .

	db.restaurant.find({}, {restaurant_id:1, name:1, cuisine:1, _id:0})

4. Restaurante en el  borough  “Manhattan”.
	
	db.restaurant.find({borough:'Manhattan'})

5. Restaurantes con  score  mayor que 90.

	db.restaurant.find({"grades.score": {$gt:90}})

6. Restaurante con  score  mayor que 80 y menor que 90.

	db.restaurant.find({$and: [{"grades.score": {$gt:90}},{ "grades.score" : {$lt:90}}]})

7. Restaurantes ubicados en  latitude  menor a -95.754168.
