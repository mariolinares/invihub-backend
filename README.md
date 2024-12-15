# invihub-backend



                                      +--------------------+
                                      |  Frontend (Angular)|
                                      +--------------------+
                                               |
                                               |
                                               v
                                    +------------------------+
                                    |  API Gateway (NestJS)  |
                                    +------------------------+
                                                |
     +------------------------------------------+---------------------------------------------+
     |                                          |                                             |
     v                                          v                                             v
+-------------------+            +------------------------+                      +-------------------------+
|  Auth Service     |            |  Invitation Service    |                      |   Notification Service  |
|-------------------|            |------------------------|                      |-------------------------|
| - JWT/OAuth2      |            | - CRUD for invitations |                      | - Email notifications   |
| - User Roles      |            | - Template management  |                      | - SMS/WhatsApp (Twilio) |
| - Secure Sessions |            | - Personalization      |                      | - Push Notifications    |
+-------------------+            +------------------------+                      +-------------------------+
     |                                          |                                             |
     |                                          |                                             |
     v                                          v                                             v
+-------------------+            +------------------------+                      +-------------------------+
|  User DB          |            |  Invitation DB         |                      |   Queue (RabbitMQ/Redis)|
| - PostgreSQL      |            | - MongoDB for templates|                      | - Asynchronous tasks    |
| - Encrypted PWs   |            | - Guest personalization|                      | - Event-driven actions  |
+-------------------+            +------------------------+                      +-------------------------+

     +------------------------------------------+---------------------------------------------+
     |                                                                                         |
     v                                                                                         v
+------------------------+                                                           +--------------------------+
|   Event Management     |                                                           |  External Integrations   |
|------------------------|                                                           |--------------------------|
| - Event Roadmaps       |                                                           | - Google Maps API        |
| - Scheduling API       |                                                           | - Spotify API (Playlist) |
| - Dynamic updates      |                                                           | - Amazon API (Gifts)     |
+------------------------+                                                           | - Payment Gateway        |
     |                                                                                 (Stripe/PayPal)          |
     v                                                                                 +--------------------------+
+------------------------+                                                                                         
| Event DB               |
| - Relational data      |
| - PostgresQL           |
+------------------------+



     +------------------------------------------+---------------------------------------------+
     |                                                                                         |
     v                                                                                         v
+------------------------+                                                           +--------------------------+
|   Multimedia Service   |                                                           |   Analytics Service       |
|------------------------|                                                           |-------------------------- |
| - Image processing     |                                                           | - Usage statistics        |
| - Video streaming links|                                                           | - Engagement metrics      |
| - Playlist management  |                                                           | - Behavioral patterns     |
+------------------------+                                                           +--------------------------+

     |
     v
+------------------------+
|  Cloud Storage (S3)   |
|------------------------|
| - Images, Videos       |
| - Static templates     |
+------------------------+
