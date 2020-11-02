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
* Logs
    * LogListView
    * LogCreateView
    * LogDetailView
    * LogUpdateView
    * DailyLogDeleteView
    * MealLogDeleteView
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
### 10/26 - 11/2
* LogUpdateView
    - [x] Change log date: successful
    - [x] Change log time: successful
    - [x] Change food and portions: successful
    - [x] Add foods: successful
    - [x] Change to future date: unsuccessful

### 10/19 - 10/26
* LogCreateView
    - [x] Create log with one food: successful
    - [x] Create log with multiple foods: successful
    - [x] Same-day meal uses existing DailyLog: successful
    - [x] Future date: unsuccessful
* DailyLog, MealLog, MealFood
    - [x] get_total(): correct
