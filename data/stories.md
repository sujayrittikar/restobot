## happy path
* greet
  - utter_greet
* mood_great
  - utter_happy

## sad path 1
* greet
  - utter_greet
* mood_unhappy
  - utter_cheer_up
  - utter_did_that_help
* affirm
  - utter_happy

## sad path 2
* greet
  - utter_greet
* mood_unhappy
  - utter_cheer_up
  - utter_did_that_help
* deny
  - utter_goodbye

## say goodbye
* goodbye
  - utter_goodbye

## bot challenge
* bot_challenge
  - utter_iamabot

## greet
* greet
  - utter_greet

## affirm
* affirm
  - utter_affirm

## restaurant story
* greet
  - utter_greet
* restaurant_search
  - utter_ask_location
* location
  - action_set_location
  - slot{"location": "Sangli"}
  - utter_ask_cuisine
* cuisine 
  - slot{"cuisine": "Pizza"}
  - utter_affirm
  - action_show_restaurants
* goodbye
  - utter_goodbye

## deny cuisine
* greet
  - utter_greet
* restaurant_search
  - utter_ask_location
* location
  - action_set_location
  - slot{"location": "Mumbai"}
  - utter_ask_cuisine
* deny
  - utter_affirm
  - action_default_restaurants

## location cuisine
* greet
  - utter_greet
* location_cuisine
  - slot{"location": "Sangli"}
  - slot{"cuisine": "maharashtrian"}
  - utter_affirm
  - action_show_restaurants
* goodbye
  - utter_goodbye

## get menu
* greet
  - utter_greet
* location_cuisine
  - slot{"location": "Sangli"}
  - slot{"cuisine": "maharashtrian"}
  - utter_affirm
  - action_show_restaurants
* get_menu
  - action_menu
* goodbye
  - utter_goodbye 

## get order
* greet
  - utter_greet
* location_cuisine
  - slot{"location": "Kolhapur"}
  - slot{"cuisine": "Pizza"}
  - utter_affirm
  - action_show_restaurants
* get_menu
  - action_menu
* order
  - utter_ask_order
* get_order
  - action_set_order
  - slot{"order": "3 Roti, 1 Paneer Tikka Masala"}
  - utter_ask_address
* get_address
  - action_set_address
  - slot{"address": "405 Red Enclave, Time Society, Kolhapur"}
  - utter_ask_contact
* get_contact
  - action_set_contact
  - slot{"contact": "9051328610"}
  - action_ask_confirm
* affirm
  - utter_ordered

## some_story
* greet
  - utter_greet
* restaurant_search
  - utter_ask_location
* location
  - action_set_location
  - slot{"location": "Mumbai"}
  - utter_ask_cuisine
* cuisine
  - utter_affirm
  - action_show_restaurants
* goodbye
  - utter_goodbye

## order story 3
* greet
  - utter_greet
* restaurant_search
  - utter_ask_location
* location
  - action_set_location
  - slot{"location": "Mumbai"}
  - utter_ask_cuisine
* cuisine
  - slot{"cuisine": "maharashtrian"}
  - utter_affirm
  - action_show_restaurants
* get_menu
  - action_menu
* order
  - utter_ask_order
* get_order
  - action_set_order
  - slot{"order": "3 Chapati, 1 Pithla"}
  - utter_ask_address
* get_address
  - action_set_address
  - slot{"address": "17 Savlon street, Bhandup"}
  - utter_ask_contact
* get_contact
  - action_set_contact
  - slot{"contact": "8011256493"}
  - action_ask_confirm
* affirm
  - utter_ordered
* affirm
  - utter_affirm

## order story 2
* order
  - utter_ask_location
* location
  - action_set_location
  - slot{"location": "Sangli"}
  - utter_ask_cuisine
* cuisine
  - slot{"cuisine": "Pizza"}
  - utter_affirm
  - action_show_restaurants
* get_menu
  - action_menu
* get_order
  - action_set_order
  - slot{"order": "1 Italian Pizza"}
  - utter_ask_address
* get_address
  - action_set_address
  - slot{"address": "405 Red Enclave, Time Society, Sangli"}
  - utter_ask_contact
* get_contact
  - action_set_contact
  - slot{"contact": "9051328610"}
  - action_ask_confirm
* affirm
  - utter_ordered


## get order_1
* greet
  - utter_greet
* location_cuisine
  - slot{"location": "Kolhapur"}
  - slot{"cuisine": "Pizza"}
  - utter_affirm
  - action_show_restaurants
* get_menu
  - action_menu
* order
  - utter_ask_order
* get_order
  - action_set_order
  - slot{"order": "3 Roti, 1 Paneer Tikka Masala"}
  - utter_ask_address
* get_address
  - action_set_address
  - slot{"address": "405 Red Enclave, Time Society, Sangli"}
  - utter_ask_contact
* get_contact
  - action_set_contact
  - slot{"contact": "9051328610"}
  - action_ask_confirm
* affirm
  - utter_ordered
* affirm
  - utter_affirm

## default resto_order
* greet
  - utter_greet
* restaurant_search
  - utter_ask_location
* location
  - action_set_location
  - slot{"location": "Mumbai"}
  - utter_ask_cuisine
* deny
  - utter_affirm
  - action_default_restaurants
