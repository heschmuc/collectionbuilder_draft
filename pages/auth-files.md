---
title: Local Authority Files
layout: about
permalink: /auth-files.html
---
## Local Authority Files
This is the page with the lists of words to be used for the metadata fields of Subjects and Dietary. You should always check this
page before creating your metadata. If the recipe requires a new word for either the subject or dietary field, you should add it to 
the correct section of this page. However, avoid any overlaps and synonyms. Only add new wordsto the metadata when absolutely necessary.

### Subjects
The subjects field describes the type of recipe which is written on the card. This includes two sections: the type of dish a recipe
is and a more descriptive portion detailing either when the dish is usually eaten, or the general type of food it is.  
**Dish Type List**
 - Appetizer
 - Dessert
 - Dressing
 - Main
 - Sauce
 - Side
 - Snack

**Meal/Food Type**
 - Bread
 - Breakfast
 - Cake
 - Cookie
 - Dinner
 - Filling
 - Jam
 - Meringue
 - Pie
 - Pudding
 - Sherbet
 - Soup
 - Vegetable

Here is a word cloud visualization of the Subjects field. Here you can see how many 
times each word was used in the metadata.  
{% include feature/cloud.html fields="subject" min=2 %}

### Dietary
This section details the dietary restriction field of the metadata. The following words are used
to describe the recipe as allergen or diet friendly. 
**Allergies**
 - No Gluten
 - No Nuts
**Diets**
 - Pescatarian
 - Vegan
 - Vegetarian

Here is a word cloud visualization of the Dietary field. You can see how many times 
each word was used in the metadata.  
{% include feature/cloud.html fields="dietary" min=2 %}
