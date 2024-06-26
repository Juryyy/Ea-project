# Csgo-matches API:
This is a simple API, working with dataset of esea matches. It provides some basic statistics, aswell option for adding more data.
Main goal is just to practice with Spring and PostgreSQL, but can help with collecting information about game itself.

## Project tasks:

- [x] Uses Spring, IDEA, PostgreSQL
- [x] Includes at least 10 endpoints
- [x] Includes at least 5 calculations (mathematical operations on arrays of data)
- [x] Code follows DRY principle
- [x] One method is always doing one thing
- [x] Method should not exceed 20 lines and 2 indentations
- [x] Handles error states (no uncaught exceptions)
- [x] Uses migrations to prepare database tables
- [x] Provides web-based documentation of endpoints and models
- [x] Includes unit tests for all calculations
- [x] Includes integration tests for all endpoints
- [x] Includes performance tests for all endpoints - done in Python


## Endpoints:
### Matches

    - GET /matches - get all matches
    - GET /matches/{id} - get match by id, with all other data about match  
    - GET /matches/maps - get matches count for each map    
    - GET /matches/map/{map_name} - get matches by map name
    - GET /matches/top-map-matches - get list of maps with matches with the highest rounds

    - POST /matches - create a new match
    - DELETE /matches/{id} - delete a match by id
    - PUT /matches/{id} - update a match by id

### Rounds

    - GET /rounds - get all rounds
    - GET /counts - get rounds count + map for each match
    - GET /maps - get rounds count for each map

    - POST /rounds - create a new round
    - PUT /rounds/{id} - update a round by id
    - DELETE /rounds/{id} - delete a round by id

### Damage 
#### Not implemented, just a inspiration for future development
    !- GET /damage - get total damage for each match
    !- GET /damage/{id} - get total damage for specific match
    !- GET /damage/highest/{id} - get highest damage for specific match
    !- GET /damage/lowest/{id} - get lowest damage for specific match


## Mathematical Operations - Endpoints
### Rounds

    - GET /rounds/avg - get average rounds count for all matches
    - GET /rounds/avg/{map_name} - get average rounds count for matches on specific map
    - GET /rounds/winrate/{map_name} - get winrate for each team on specific map

### Kills
    - GET /kills/avg - get average kills count for each map
    - GET /kills/avg{map_name} - get average kills count for matches on specific map
    - GET /kills/avg/sides - get average kills count for matches on specific side
    - GET /kills/weapons - get average kills count for matches with each weapon

