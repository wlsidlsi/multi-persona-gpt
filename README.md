# MultiPersonaGPT

As a team solve problems, talk it out, write stories , add engaging personas (e.g., "Add Albert Einstein"), and manage participants. Enjoy dynamic conversations, variety of insights. Skip the ordinary—explore ideas effortlessly! Ask "how to use this gpt" for help.

# Instructions

The instructions aim to guide the conversation and detail formatting. The conversation tends to follow a cyclic order, as if everyone is sitting at a table and always has something to say while circling around the table.

The user is the host. The instructions aim to prevent a separate conversation between the GPT and the host, keeping the conversation contained to the participants. If there are four participants, including the host, in a conversation, then ideally the four participants converse with one another. Sometimes, a participant might have more to remark on another participant's comments. It should be allowed for at least two people to have a back and forth before the host jumps in.

Breaks in the conversation for the host should be a natural points and not in the middle of a back and forth to let the idea flow naturally.

# GitHub Action

The GitHub Action works as expected. All participants can commit files, and create and update issues, such as stories, epics, and defects. Since participants other than the host cannot perform work directly, they can create GitHub issues as action items. The host can then take action on these items or assign them to an agent.

# Google Drive Action

I went round and round trying to figure out a method that didn't involve an external middleware API due to OpenAI's strict security adherence to the token. The token is only passable to the domain in the URL under servers. 

That means in order to upload files, an external service needs to be created to act as a bridge to allow the action to pass information as JSON, and then the middleware service would make the request to Google Drive. If OpenAI allowed for a token to be passed to the middleware service, then Zapier or Make.com might be viable options (still might depending on the amount of effort one wants to take). 

However, I did not want to manage tokens or run services that have associated financial costs. I left the Google Drive action in place in case someone needs to create folders, move documents around, or read content from Google Drive. That being said, I removed it from the ChatGPT description so I don't have to continuously have the Drive API enabled unless it seems people are actually using it.
