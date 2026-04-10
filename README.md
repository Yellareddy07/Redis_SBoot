This is the example project of using REDIS in SpringBoot.
It includes adding user, deleting and retrieving the user.

Project Flow :

Client (Postman / Browser)

        ↓
Controller
        ↓
Service  (Caching logic here)
        ↓
Repository (JPA)
        ↓
MySQL Database
        ↕
     Redis Cache

     
READ (GET):
    Check Redis
        ↓
    HIT → Return
    MISS → DB → Cache → Return

WRITE (POST/DELETE):
    Update DB
        ↓
    Update/Evict Cache
     
