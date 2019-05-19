---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to Food Portfolio API! You can use our API to access Food Portfolio API endpoints, which can get information on unique recipes in our database.

You can view code examples in the dark area to the right, and you can switch the programming language of the examples (if implemented in more than one language) with the tabs in the top right.

# Recipes

## Get All Recipes

```shell
curl "https://foodie-portfolio.herokuapp.com/recipe"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "title": "Shrimp Cakes",
    "mealType": "dinner",
    "ingredients": "1/4 cup cumin seeds, 3 tablespoons whole black peppercorns, 1 tablespoons coriander seeds, 2 tablespoons sugar, 1 1/2 teaspoons sea salt",
    "instructions": "1 Make the spice mix: Add cumin seeds, peppercorns, and coriander to a heavy medium skillet. Cook over medium heat, stirring, until fragrant and lightly toasted, about 8 minutes. Let cool a few minutes. Grind spices in a blender or spice grinder (can use a coffee grinder that has been cleaned by grinding raw rice) until finely ground. Transfer to a small bowl, stir in sugar and salt. This makes about half a cup. You'll only need 1 1/2 teaspoons of the spice mix for one shrimp cakes recipe, so store the remainder for future use. 2 Preheat the oven to 375°F. 3 Microwave the sweet potatoes and the garlic: Pierce sweet potatoes all over with a fork. Bake in microwave for about 15 minutes until done. Rub one tablespoon of oil over the unpeeled garlic cloves. Cook in microwave a few minutes, until soft. Let the garlic and sweet potatoes cool enough to handle. Peel the garlic. Cut the sweet potato in half and use a spoon to scoop out the flesh. Combine the cooked sweet potato and garlic in a bowl and mash until smooth. 4 Make the shrimp mixture: Add the shrimp, cilantro, breadcrumbs, jalapeño, onion, and 1 1/2 teaspoons of the spice mix to the bowl with the sweet potatoes. Mix until well blended. Season with salt.",
    "image": "https://www.simplyrecipes.com/wp-content/uploads/2006/03/shrimp-cakes-horiz-a-1600.jpg",
    "user_id": 9
  },
  {
    "id": 2,
    "title": "Salmon Avocado Poke Bowl",
    "mealType": "dinner",
    "ingredients": "Sliced cucumber, Sliced radish, Sliced or cubed avocado, Furikake, Thinly sliced scallion, Red pepper flakes",
    "instructions": "Once you have your fish, the rest of the poke bowl comes together really quickly. Just cook some rice, toss the fish with the dressing, and serve! I like to place all the extra toppings on the table so that everyone can help themselves",
    "image": "https://www.simplyrecipes.com/wp-content/uploads/2017/03/2017-04-26-PokeBowls-2-768x1075.jpg",
    "user_id": 8
  },
]
```

This endpoint retrieves all recipes.

### HTTP Request

`GET https://foodie-portfolio.herokuapp.com/recipe`

## Get a Specific Recipe

```shell
curl "https://foodie-portfolio.herokuapp.com/recipe/1"
```

> The above command returns JSON structured like this:

```json
{
  "id": 3,
  "title": "Corn Salsa Recipe",
  "mealType": "lunch",
  "ingredients": "2 ears fresh corn on the cob, 1/2 cup minced red onion, 1 jalapeño chili pepper, seeded and minced, 1/4 teaspoon ground cumin, 1/3 cup chopped cilantro, including tender stems, 2 teaspoons fresh oregano, chopped (or 1 teaspoon dry), 1 teaspoon kosher salt, 2 Tbsp lime juice",
  "instructions": "2 Cut away the kernels: When the corn has cooled to the touch, cut the kernels away from the cobs. The easiest way to do this is to invert a medium sized bowl and place it in a larger bowl. Hold the stem end of the corn cob and place the tip on top of the domed middle bowl. Use a sharp chef's knife to cut down along the sides of the corncob to cut away the kernels.",
  "image": "https://www.simplyrecipes.com/wp-content/uploads/2015/08/corn-salsa-vertical-b-640.jpg",
  "user_id": 1
}
```

This endpoint retrieves a specific recipe.

### HTTP Request

`GET https://foodie-portfolio.herokuapp.com/recipe/:id`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the user (chef) to retrieve

## Create a Specific Recipe

```shell
curl "https://foodie-portfolio.herokuapp.com/recipe"
  -X POST
  -H "Authorization: token"
```

> The above command returns JSON structured like this:

```json
{
  "id": 4,
  "title": "New Recipe",
  "mealType": "desert",
  "ingredients": "1 Oreo cookie, 1 tablespoon vanilla ice cream",
  "instructions": "Eat them however you want",
  "image": null,
  "user_id": 7
}
```

This endpoint creates a new recipe.

### HTTP Request

`POST https://foodie-portfolio.herokuapp.com/recipe`

## Update a Specific Recipe

```shell
curl "https://foodie-portfolio.herokuapp.com/recipe/1"
  -X PUT
  -H "Authorization: token"
```

> The above command returns count of the recipes that have been deleted:

```json
  {
    "id": 1,
    "title": "Shrimp Cakes2",
    "mealType": "dinner",
    "ingredients": "1/4 cup cumin seeds, 3 tablespoons whole black peppercorns, 1 tablespoons coriander seeds, 2 tablespoons sugar, 1 1/2 teaspoons sea salt",
    "instructions": "1 Make the spice mix: Add cumin seeds, peppercorns, and coriander to a heavy medium skillet. Cook over medium heat, stirring, until fragrant and lightly toasted, about 8 minutes. Let cool a few minutes. Grind spices in a blender or spice grinder (can use a coffee grinder that has been cleaned by grinding raw rice) until finely ground. Transfer to a small bowl, stir in sugar and salt. This makes about half a cup. You'll only need 1 1/2 teaspoons of the spice mix for one shrimp cakes recipe, so store the remainder for future use. 2 Preheat the oven to 375°F. 3 Microwave the sweet potatoes and the garlic: Pierce sweet potatoes all over with a fork. Bake in microwave for about 15 minutes until done. Rub one tablespoon of oil over the unpeeled garlic cloves. Cook in microwave a few minutes, until soft. Let the garlic and sweet potatoes cool enough to handle. Peel the garlic. Cut the sweet potato in half and use a spoon to scoop out the flesh. Combine the cooked sweet potato and garlic in a bowl and mash until smooth. 4 Make the shrimp mixture: Add the shrimp, cilantro, breadcrumbs, jalapeño, onion, and 1 1/2 teaspoons of the spice mix to the bowl with the sweet potatoes. Mix until well blended. Season with salt.",
    "image": "https://www.simplyrecipes.com/wp-content/uploads/2006/03/shrimp-cakes-horiz-a-1600.jpg",
    "user_id": 9
}
  }
```

This endpoint updates a specific recipe.

### HTTP Request

`PUT https://foodie-portfolio.herokuapp.com/recipe/:id`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the recipe to update

## Delete a Specific Recipe

```shell
curl "https://foodie-portfolio.herokuapp.com/recipe/:id"
  -X DELETE
  -H "Authorization: token"
```

> The above command returns count of the recipes that have been deleted:

```json
  1
```

This endpoint deletes a specific recipe.

### HTTP Request

`DELETE https://foodie-portfolio.herokuapp.com/recipe/:id`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the recipe to delete

# Chefs

## Get All Chefs

```shell
curl "https://foodie-portfolio.herokuapp.com/users"
-H "Authorization: token"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "username": "jasonh"
  },
  {
    "id": 2,
    "username": "jabrilb"
  },
  {
    "id": 3,
    "username": "scottg"
  },
  {
    "id": 4,
    "username": "terriek"
  }
]
```

This endpoint retrieves all chefs.

### HTTP Request

`GET https://foodie-portfolio.herokuapp.com/users`

## Register a new Chef

```shell
curl "https://foodie-portfolio.herokuapp.com/users/register"
-X POST
-H "Content-Type: application/json"
```

> The above command returns JSON structured like this:

```json
{
  "id": 6,
  "username": "terr1e4",
  "password": "$2a$10$Woiiy9FBAtyQAmDAI.hf5erT/KW98UNXFYnGnI1QcwYMF9O/ne8Gi",
  "location": "Los Angeles",
  "email": "terr1e@ls.com",
  "firstName": "Terrie",
  "lastName": "Kim"
}
```

This endpoint registers a new Chef (user).

### HTTP Request

`POST https://foodie-portfolio.herokuapp.com/users/register`

## Log in a Specific Chef

```shell
curl "https://foodie-portfolio.herokuapp.com/users/login"
  -X POST
  -H "Content-Type: application/json"
```

> The above command returns JSON structured like this:

```json
{
  "message": "terr1e3 has successfully logged in",
  "token": "ehSFehfEfh34dfHfdf34DF3F3SFD6yff45D.SdfjkGfg34"
}
```

This endpoint logs in a specific Chef.

### HTTP Request

`POST https://foodie-portfolio.herokuapp.com/users/login`
