# Restaurant Assignment

Uses data in index.js

# GraphQL

## here are the query and mutation structures

#### restaurant: This gets a single restaurant based on a provided ID. 
query getrestaurant($iid: Int = 1){
    restaurant(id:$iid){
name
description
}
}

#### restaurants: This gets a list of all restaurants. 
query getrestaurants {
restaurants {
name
}
}

#### setrestaurant: This creates a new restaurant. 
mutation setrestaurants {
setrestaurant(input: {
name: "Granite",
description: "American"}) {
name
description
}
}

#### Deleterestaurant: This deletes a restaurant based on the provided id.
mutation deleterestaurants($idd: Int = 1){
  deleterestaurant(id: $idd){
ok
}
}

#### editrestaurant: This updates a restaurant based on the provided id.
mutation editrestaurants($idd: Int = 1, $name: String = "OLDO"){
editrestaurant(id: $idd, name: $name){
name
description
}
}



