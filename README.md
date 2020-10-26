# Unit Tests for Nutrition Helper Project

## Functionalities
* Nutrifacts nutrient calculator
* Search food and recipe
* Profile
* User Accounts
* Allergies/Diet Preferences
* Create daily log
* Display daily log
* Create recipe


## Functionalities that need to be tested
Models:
* Profile
    * get_metric_profile()
    * create_profile()
* DailyLog, MealLog, MealFood
    * create()
    * get_total()
* Recipe, RecipeFood
    * create()
    * get_total()

Views:
* SearchResultsView
* RegisterAccountView
* UpdateProfile
* Diet and Allergies
    * AddAllergyView
    * AddDietPreferenceView
    * DeleteAllergyView
    * DeleteDietPreferenceView
* LogView
* DisplayLogView
* DetailRecipe
    * ListRecipe
    * CreateRecipe
    * UpdateRecipe
    * DeleteRecipe
    * RecipeView

## Functionalities that don't need to be tested
Models:
* RecipePreset
* User Accounts (default Django model)
* Allergy
* Diet Preference
* BrandedIds

Views:
* Index
* Description
* Nutrifacts
* LoginView (default Django view)
* LogoutView (default Django view)
* PasswordChangeView (default Django view)

## My tests
* Create daily log & LogView
    * One food: successful
    * Multiple foods: successful
    * Same-day meal uses existing DailyLog: successful
    * Future date: unsuccessful
* DailyLog, MealLog, MealFood
    * get_total(): correct
