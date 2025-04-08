# Chat Service

## What is this?
This is a very simple chat service using websockets and the Spring Boot framework.

## How does it work?
- Fire up the service, then navigate to http://localhost:8080. 
- Enter a username and click on the 'Start Chatting' button.

This will open up a chat window. If you do the same thing on another tab, you can have 2 users in a websocket driven chat
room. If the service is deployed somewhere other than locally, users should be able to access the server and chat through
the only available public topic.

## Considerations
This could be extended by allowing for other channels to be made available, or for authentication to happen using Oauth2 and
OICD as an example, but currently the usernames can be anything (even duplicates).

If we wanted to show the last 10 messages of the conversation (to let new joiners catch up with the conversation) we could
deploy a write through cache with a capacity of 10 messages. This way, we can just load all messages from the cache into the
chat window on entry.