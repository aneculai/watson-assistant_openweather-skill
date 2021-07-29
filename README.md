# watson-assistant_openweather-skill
Skill for IBM Watson Assistant to connect with OpenWeather API
***************
This repository offers details on how to build weather capabilities in your Watson Assistant chatbot.
You need to create an action in IBM Functions to call the OpenWeather API. We will use Node.js to make the API call and to process the JSON response. The code will save the weather elements in a variable that is passed on to Watson Assistant when the Dialog node uses a webhook to call the action defined in the IBM Functions. Here is a simplified diagram:
WA dialog node<---- webhook call----> IBM Functions Action <----API call to OpenWeather----> OpenWeather
Remember, first you have to create an account on OpenWeather so you get an API_ID that you have to use when calling the OpenWeather API from the IBM Functions. Also, IBM Functions will generate for you a weblink to use as webhook in Watson Assistant.
There is one more “trick” you need to be aware of: you will use the city you want the weather conditions for as a parameter. This way the city is not hard-coded in the chatbot and you can define multiple values for a weather entity, each value for a different city. This way the chatbot can tell the weather for different locations instead of just one.
***********
Read the pdf file that offers all the details and steps, with screen captures, on how to create the Watson Assistant Skill to connect to OpenWeather API.
************
