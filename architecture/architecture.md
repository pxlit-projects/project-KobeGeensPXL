# Architecture
![Java drawio_6](https://github.com/user-attachments/assets/33efb969-18d4-4581-9f5a-06488f33eeb3)
# Sync communciation
The comment, post and review microservice communicate between each other using OpenFeign to retreive the linked Reviews and Comments of a post.
# Async communication
When a new comment or review is added to an existing post, a message is sent to the queue wich the PostService is listening to. Upon receiving the message the id of the comment or review is added to thee correct post in the database.
