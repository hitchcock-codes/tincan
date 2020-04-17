# TinCan Chat Server

## Functional Requirements

| Scope         | Action   | Description                                                                                     |
| :------------ | :------- | :---------------------------------------------------------------------------------------------- |
| Auth          | Login    | Users can login and receive a token used for authentication/authorization                       |
|               | Logout   | Users can logout, effectively closing their connection and revoking their token                 |
|               | Register | Users can register for an account with the chat server                                          |
| Groups        | Create   | Users can create groups of other users where they can host their conversations                  |
|               | Edit     | Users can edit information about a group they own, such as the name, visibility, and members    |
|               | List     | Users can view a list of available groups to join                                               |
|               | Join     | Users can join/request to join a group to participate in conversations with other group members |
|               | Leave    | Users can leave a group they had joined previously                                              |
|               | Remove   | Users can remove a group that they own                                                          |
| Conversations | Create   | Users can create a conversation within a group                                                  |
|               | Edit     | Users can edit information about a conversation they own, such as name, participants, etc.      |
|               | List     | Users can view the available conversation within a group they are a member of                   |
|               | Remove   | Users can remove a conversation they own within a group                                         |
|               | Typing   | The system can detect when a client is starting/stopping typing                                 |
| Messages      | Create   | Users can create new messages to add to a conversation                                          |
|               | Edit     | Users can edit a message they've posted in the past                                             |
|               | Remove   | Users can remove a message they've posted in the past                                           |

## Architecture

## Messages

### Client Messages

| Message                   | Description                                                            |
| :------------------------ | :--------------------------------------------------------------------- |
| `auth/logout`             | Request from the client to terminate their connection and log out      |
| `group/create`            | Create group request from the client                                   |
| `group/edit`              | Edit group request from the client                                     |
| `group/list`              | Request from the client to view available groups                       |
| `group/view`              | Request from the client to view public details about a single group    |
| `group/join`              | Request from the client to join a group                                |
| `group/leave`             | Request from the client to leave a group                               |
| `group/remove`            | Request from the client to remove a group                              |
| `conversation/create`     | Create conversation request from the client                            |
| `conversation/edit`       | Edit conversation information request from the client                  |
| `conversation/list`       | Request from the client to list available conversations within a group |
| `conversation/remove`     | Request from the client to remove a conversation                       |
| `conversation/type-start` | Notification that the client has detected typing                       |
| `conversation/type-end`   | Notification that the client has detected a stop to typing             |
| `message/create`          | Create message request from the client (new message post)              |
| `message/edit`            | Edit message request from the client                                   |
| `message/remove`          | Remove message request from the client                                 |

### Server Messages

| Message                      | Description                                                                              |
| :--------------------------- | :--------------------------------------------------------------------------------------- |
| `group/created`              | Server notification that a group was successfully created                                |
| `group/create-failed`        | Server notification that a group was not created successfully                            |
| `group/edited`               | Server notification that a group's information was edited successfully                   |
| `group/edit-failed`          | Server notification that a group's information failed to be edited                       |
| `group/list-response`        | Server notification to a client's `group/list` request containing available groups       |
| `group/view-response`        | Server notificatikon to a client's `group/view` request containing details about a group |
| `group/joined`               | Server notification that a client successfully joined a group                            |
| `group/join-failed`          | Server notification that a client request to join a group failed                         |
| `group/left`                 | Server notification that a client request to leave a group succeeded                     |
| `group/leave-failed`         | Server notification that a client request to leave a group failed                        |
| `group/removed`              | Server notification that a client request to remove a group succeeded                    |
| `group/remove-failed`        | Server notification that a client request to remove a group failed                       |
| `conversation/created`       | Server notificatikon to a conversation was created successfully                          |
| `conversation/create-failed` | Server notification that a conversation failed to be created                             |
| `conversation/edited`        | Server notification that a conversation edit suceeded                                    |
| `conversation/edit-failed`   | Server notiication that a conversation edit failed                                       |
| `conversation/list-response` | Server notification for a `conversation/list` request                                    |
| `conversation/removed`       | Server notiication that a conversation was removed successfully                          |
| `conversation/remove-failed` | Server notification that a conversation failed to be removed                             |
| `conversation/type-start`    | Server notification that another user in the conversation is typing on that conversation |
| `conversation/type-end`      | Server notification that another user has stopped typing in a conversation               |
| `message/created`            | Server notification that a message was created successfully                              |
| `message/create-failed`      | Server notification that a message failed to be created                                  |
| `message/edited`             | Server notification that a message was edited successfully                               |
| `message/edit-failed`        | Server notification that a message failed to be edited                                   |
| `message/removed`            | Server notiication that a message was removed successfully                               |
| `message/remove-failed`      | Server notification that a message failed to be removed                                  |
