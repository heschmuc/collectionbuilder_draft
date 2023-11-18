---
title: Documentation
layout: page
permalink: /documentation.html
---
{% include feature/jumbotron.html %}

{% include feature/nav-menu.html sections="About the Documentation;Technical and Metadata Standards;How to Add Items;Field Formats" %}

## About the Documentation  
This page is a description of what processes went into creating this website and the technical and metadata standards. You can use this page to get an overview of the site as well as to add objects of your own to the collection which are of the same standard. 

## Technical and Metadata Standards
This site was generated using [CollectionBuilder-GH](https://collectionbuilding.github.io/gh/), a project to create a free and simple digital collection using [GitHub Pages](https://pages.github.com/). It is based on a template website, with objects and related metadata added and the basic code and website content edited for the purposes of the collection and creator.  
Most of the technical and metadata standards came from CollectionBuilder and [Dublin Core](https://www.dublincore.org/specifications/dublin-core/usageguide/elements/), but there were some additional standards which were created specifically for the purposes of this project. You can find more information about these additional standards under the Field Formats section.  
For full details of the technical standards of CollectionBuilder, read the [CollectionBuilder Documentation](https://collectionbuilder.github.io/cb-docs/) documentation pages!

## How to Add Items
This section is about how to add items to this online collection. 
1. Digitization - You can take a picture, scan, or other way of digitizing the recipe. All the original files were pdfs, but the files can whatever kind you'd like (jpeg, png, etc.). If the front and back were used in writing down the recipe, include both sides. If only one side was used, the other side can be left off. Save the file according to how it will be named in the metadata file. This makes sure that the website will correctly access each of the files and match it to the correct metadata. You can look at either the objects folder or the metadata file in the repository to find the correct number for the filename.
2. Editing - Using photo or pdf editing software, such as Adobe Photoshop or Acrobat, or coding language such as ImageMagick. Make sure the file is centered, clear and not blurry, and not have any words cut off anywhere.
3. Transcription - Using OCR software or manual labor, transcribe the recipe. Separate the ingredients from the instructions for the recipe.
4. Adding Object to Website - Upload the file to the objects folder in the collectionbuilder-final repository. Commit the addition.
5. Metadata - Look at the following section for all the necessary and optional metadata fields. Create the metadata and add it (with the correct filename) to the _data/collectionbuilder-final.csv file in the collectionbuilder-final repository on GitHub. Commit the change.

## Field Formats

### Title
 | Property | Element | 
 | --- | --- | 
 | Element Name | title | 
 | Dublin Core Element | Title | 
 | Cardinality | Non-repeatable | 
 | Obligation | Required | 
 | Vocabulary? | N/A | 
 | How to Use | The title of the recipe.  <br><br>Take from the top of the recipe card. look for centered text, bigger text, or Recipe For… line beginning.  <br><br>The title of each recipe will have the first letter of each word (except for filler words such as a, the, of, etc., unless these words are the beginning of the recipe) capitalized. | 
 | Examples | Chocolate Cake, Divinity Puffs, Lasagna | 

### ObjectID
 | Property | Element | 
 | --- | --- | 
 | Element Name | objectid | 
 | Dublin Core Element | Identifier | 
 | Cardinality | Non-repeatable | 
 | Obligation | Required | 
 | Vocabulary? | N/A | 
 | How to Use | The id will be made of two parts, the recipe number and the recipe number. The number at the beginning of the id will start at 000 and continue, incrementing by 1 with each recipe.  <br><br>The name will be taken from the title field, with underscores in place of the spaces or filler words, and all lowercase. Special characters from the title, such as dashes, apostrophes, etc. should not be included in the objectid. | 
 | Examples | 000_chocolate_cake, 002_lasagna, …, 031_divinity_puffs, etc. | 

### Filename
 | Property | Element | 
 | --- | --- | 
 | Element Name | filename | 
 | Dublin Core Element | Identifier | 
 | Cardinality | Non-repeatable | 
 | Obligation | Required | 
 | Vocabulary? | N/A | 
 | How to Use | This will be the objectid value with the file extension at the end of it. This should exactly match the filename of the object it is associated with.  <br><br>Refer to objectid field for How to Use. | 
 | Examples | 000_chocolate_cake.jpeg, 001_lasagna.tiff, …, 031_divinity_puffs.png, etc. | 

### Format
 | Property | Element | 
 | --- | --- | 
 | Element Name | format | 
 | Dublin Core Element | Format | 
 | Cardinality | Non-repeatable | 
 | Obligation | Required | 
 | Vocabulary? | [MME Type Vocabulary](https://www.iana.org/assignments/media-types/media-types.xhtml) | 
 | How to Use | The object’s type of file. These will be formatted as format/filetype. | 
 | Examples | image/jpeg, image/png, image/gif, etc. | 

### Date
 | Property | Element | 
 | --- | --- | 
 | Element Name | date | 
 | Dublin Core Element | Date | 
 | Cardinality | 0 to 1 | 
 | Obligation | Not Required | 
 | Vocabulary? | N/A | 
 | How to Use | The year the recipe was made, if available. Format as YYYY. | 
 | Examples | 1987, 2001, etc. | 

### Subject
 | Property | Element | 
 | --- | --- | 
 | Element Name | subject | 
 | Dublin Core Element | Subject | 
 | Cardinality | 0 to 3 | 
 | Obligation | Not Required | 
 | Vocabulary? | Local Authority File | 
 | How to Use | Deciding what the recipe describes (a meal such as lunch, dinner, breakfast; a side, a sauce, dessert, etc.) and using the authority file for the collection to find the related vocabulary.  <br><br>If there are multiple entries, use a semicolon to separate the values. | 
 | Examples | Dinner; Lunch; Dessert | 
 
### Author
 | Property | Element | 
 | --- | --- | 
 | Element Name | author | 
 | Dublin Core Element | Creator | 
 | Cardinality | 0 to 1 | 
 | Obligation | Not Required | 
 | Vocabulary? | N/A | 
 | How to Use | Use the name attached to the title or within parenthesis to the side if available. Otherwise, if possible, determine based on handwriting which grandparent wrote out the recipe.  <br><br>The author will be entered as ‘Lastname, Firstname’ (where each name is capitalized), unless there is only a first or last name, where it will just be entered as ‘Name’. | 
 | Examples | Novy, Mary Lou; Yhae, Anna; Crocker, Betty | 

### Servings 
 | Property | Element | 
 | --- | --- | 
 | Element Name | servings | 
 | Dublin Core Element | N/A | 
 | Cardinality | 0 to 1 | 
 | Obligation | Not Required | 
 | Vocabulary? | N/A | 
 | How to Use | Find using text such as Serves: …, Number of Servings: … etc. and then put in the corresponding numbers. If it is one number, use the numerical form (2, 5, etc.). If it is a range, use a dash between the two numerical forms of the numbers, without a space (3-5, 10-15, etc.) | 
 | Examples | 24, 12-15 | 

### Dietary
 | Property | Element | 
 | --- | --- | 
 | Element Name | dietary | 
 | Dublin Core Element | Subject | 
 | Cardinality | 0 to 3 | 
 | Obligation | Not Required | 
 | Vocabulary? | Local Authority File | 
 | How to Use | Look at the ingredients list and list the appropriate vocabulary from the authority file.  <br><br>For example, if there are no meat products, but there are animal products (cheese, eggs, milk, etc.), use the Vegetarian authority file word. If there are fish products, but no other meat products, use the Pescatarian authority file word. If there are no meat or animal products, use the Vegan authority file word.  <br><br>The same goes for food allergies. For a couple examples, if there are no nuts, put ‘No Nuts’ and if there are no gluten products, put ‘No Gluten’.  <br><br>If there is more than one item which applies to the recipe, use a semicolon to separate them. However, if an item is Vegan, you do not have to put Vegetarian as well, as this is implied. | 
 | Examples | Vegan; Gluten Friendly; No Nuts | 

### Ingredients
 | Property | Element | 
 | --- | --- | 
 | Element Name | ingredients | 
 | Dublin Core Element | Description | 
 | Cardinality | Non-repeatable | 
 | Obligation | Required | 
 | Vocabulary? | N/A | 
 | How to Use | The transcription of the ingredient part of the recipe. If there are any words which you are unsure of, put wd? in parentheses immediately after the word. If there are any shorthand words to stand in for phrases (ex. soda for baking soda), put the unincluded word(s) in parentheses where they would go by the original word. If there is an abbreviation, put the normal word. If you are not sure what the abbreviation means, look at the Transcription File for the correct word.  <br><br>Enter fractions as number/number (ex. 1/2, 3/4). If there is a number before, put a space between the two numbers for ease of differentiation (ex. 1 1/2 2 1/4).  <br><br>If there is a range for any ingredients, use the - character to show it can be between those two numbers (ex. 1-3, 4-5).  <br><br>Separate the number versus the measurement type versus ingredient with spaces. Separate the ingredients with commas.
| Examples | 1 egg, 1 cup sugar, 1 tbsp (tablespoon) butter, 2-3 tbsp (tablespoon) cocoa, 1 cup sour milk, 1 tsp (teaspoon) (baking) soda, 1 1/2 cup flour, vanilla | 

### Directions
 | Property | Element |
 | --- | --- |
 | Element Name | directions | 
 | Dublin Core Element | Description | 
 | Cardinality | Non-repeatable | 
 | Obligation | Required | 
 | Vocabulary? | N/A | 
 | How to Use | The recipe directions. Include all text which comes after the ingredient list.   <br><br> <br><br>If there are any words which you are unsure of, put wd? in parentheses immediately after the word. If there are any shorthand words to stand in for phrases (ex. soda for baking soda), put the unincluded word(s) in parentheses where they would go by the original word. | 
 | Examples | Cream egg and sugar. Melt butter and cocoa together. Add to first mixture. Add (baking) soda to milk and stir in. Then add the flour and vanilla.| 


