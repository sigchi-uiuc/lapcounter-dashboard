* A method to return an array of all users
* A method to return all information of a specific user
  * Name
  * Year
  * When they registered
  * Average Lap Completion Time
  * Average Speed
  * Fastest Lap Time
  * Total Laps Completed
  * Total Distance Ran
  * Total time spent running

* A method to return all information of a specific running session
  * Average Lap Speed
  * Fastest Lap Speed
  * Duration of Session
  * Start and End time of Session

Poopsicles. If you see this, it means all is well.

* Current paths for displaying data
    * /info/users
        * returns a list of users (names) with their ids
        * { "results": [ { "id": 1, "name": "username" } ] }
    * /info/<input_users>/data
        * returns the user's name and a list of laps
        * {
            "info": {
                "average": 5.5,
                "max_lap_time": 10,
                "min_lap_time": 1,
                "num_laps": 2,
                "total_time": 11
            }
            "laps": [
                {
                  "duration": 10,
                  "end": 10,
                  "start": 0,
                  "user_id": 2
                },
                {
                  "duration": 1,
                  "end": 124,
                  "start": 123,
                  "user_id": 2
                }
              ],
              "user": {
                "id": 2,
                "name": "username"
              }
            }
    * /info/data
        * returns a list of all laps
           * { "results": [ { /* duration, end, start, user_id */ } ] }