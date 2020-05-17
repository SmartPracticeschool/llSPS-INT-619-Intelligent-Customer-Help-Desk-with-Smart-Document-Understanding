# Intelligent Customer Help Desk with Smart Document Understanding
 
This repository is created to show you a working example of web app that utilizes various IBM Watson services to create a better quality customer experience. It includes Watson Discovery, Watson Assistant, Node-Red app and Cloud Function.

Project description:

This project is focused on creating a Customer care chatbot with a feature which will enhance customer experience. This feature is called Smart Document Understanding (SDU). When the query is of technical domain, SDU  will link to appropriate help context from the user manual upploaded in Watson Discovery. Unlike the typical chatbot with predefined dialogs wherein if a technical query is been asked it will direct it to some customer representative, this enhanced chatbot will display the appropriate solution. There will be no human interaction and the scope will be widened.

With the help of Smart Document Understanding feature, Watson Discovery model will be customized so that the queries will be focused on the search for most relevant information from the users manual uploaded in Discovery.

Watson Assistant will acts as the Chatbot will predefined standard dialogs loaded to handle typical conversation between customer. When the query comes under technical domain, it will communicate with Discovery service with the help of 'Webhook'.
Webhook will be created by defining a web action using Cloud Functions.

Node-Red will wire all the services utilized in this project and create a UI for the customers.

FLOW

![Image description](https://github.com/IBM/watson-discovery-sdu-with-assistant/blob/master/doc/source/images/architecture.png)

This flow basically summarizes the project. It begins with :
1. The annotation of document using Watson Dicovery SDU.
2. The user interacts with Node-Red app UI.The chatbot engages the user in conversation.
3. Dialog in this interaction is coordinated by Watson Assistant.
4. If the customer asks a technical question, it will be passed to Cloud Functions action.
5. This action will further pass onto to Watson Discovery and return with appropriate solution.
