# TinCan Chat Server

## Functional Requirements

| Scope         | Action | Description                                                                                     |
| :------------ | :----- | :---------------------------------------------------------------------------------------------- |
| Auth          | Login  | Users can login and receive a token used for authentication/authorization                       |
|               | Logout | Users can logout, effectively closing their connection and revoking their token                 |
| Groups        | Create | Users can create groups of other users where they can host their conversations                  |
|               | Edit   | Users can edit information about a group they own, such as the name, visibility, and members    |
|               | List   | Users can view a list of available groups to join                                               |
|               | Join   | Users can join/request to join a group to participate in conversations with other group members |
|               | Leave  | Users can leave a group they had joined previously                                              |
|               | Remove | Users can remove a group that they own                                                          |
| Conversations | Create | Users can create a conversation within a group                                                  |
|               | Edit   | Users can edit information about a conversation they own, such as name, participants, etc.      |
|               | List   | Users can view the available conversation within a group they are a member of                   |
|               | Remove | Users can remove a conversation they own within a group                                         |
| Messages      | Create | Users can create new messages to add to a conversation                                          |
|               | Edit   | Users can edit a message they've posted in the past                                             |
|               | Remove | Users can remove a message they've posted in the past                                           |
| System        | Typing | The system can detect when a client is starting/stopping typing                                 |
|               | Status | The system provides status about a user's availability                                          |


## Architecture

## Messages

### Client Messages

### Server Messages
