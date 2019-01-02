# JSON Data Tree

The following table contains names of variables, data types and their description in `tabular structure` for easy use of **JSON Data** present in _data.json_ file.

| Variable Name                         |      Data Type     |                Description               |
| ------------------------------------- | :----------------: | :--------------------------------------: |
| `competition`                         |      _String_      |                League Name               |
| `location`                            |      _String_      |      Location where League is played     |
| `season`                              |      _String_      |              Current season              |
| `starting_date`                       |      _String_      |               Starting date              |
| `ending_date`                         |      _String_      |                Ending date               |
| `total_matchdays`                     |      _Integer_     |  Total number of matchdays in the season |
| `total_matches`                       |      _Integer_     |   Total number of matches in the season  |
| `number_of_participating_clubs`       |      _Integer_     |   Total clubs taking part in the season  |
| `participating_clubs`                 | _Array of Strings_ |       Names of participating clubs       |
| `stadiums`                            | _Array of Strings_ |       Names of respective stadiums       |
| `team_codes`                          | _Array of Strings_ |  Three character code of respective club |
| [`clubs`](#clubs)                     | _Array of Objects_ |        Detailed data of each Club        |
| [`season_fixtures`](#season_fixtures) | _Array of Objects_ |     Complete details of each fixture     |
| [`players`](#players)                 | _Array of Objects_ |       Detailed data of each Player       |
| [`goals`](#goals)                     | _Array of Objects_ | Details of all Goals Goals in the season |
| [`assists`](#assists)                 | _Array of Objects_ |   Details of all Assists in the season   |
| [`clean_sheets`](#clean_sheets)       | _Array of Objects_ |  Detail of all Goalkeepers clean sheets  |
| [`own_goals`](#own_goals)             | _Array of Objects_ |  Details of all own goals in the season  |

#### clubs

| Property Name         |      Data Type     |                        Description                       |
| --------------------- | :----------------: | :------------------------------------------------------: |
| `id`                  |      _Integer_     |                  Unique ID for each club                 |
| `name`                |      _String_      |                     Name of the club                     |
| `short_name`          |      _String_      |                  Short name for the club                 |
| `club_code`           |      _String_      |                     Three letter code                    |
| `stadium`             |      _String_      |                      Name of Stadium                     |
| `capacity`            |      _Integer_     |                     Stadium capacity                     |
| `manager`             |      _String_      |                       Manager Name                       |
| `manager_nationality` |      _String_      |                    Manager Nationality                   |
| `position`            |      _Integer_     |               Current Position in the Table              |
| `last_week_position`  |      _Integer_     |              Last Week Position in the Table             |
| `games_played`        |      _Integer_     |                    Total games played                    |
| `home_games_played`   |      _Integer_     |                  Total Home games played                 |
| `away_games_played`   |      _Integer_     |                  Total Away games played                 |
| `wins`                |      _Integer_     |                        Total Wins                        |
| `home_wins`           |      _Integer_     |                      Total Home Wins                     |
| `away_wins`           |      _Integer_     |                      Total Away Wins                     |
| `draws`               |      _Integer_     |                        Total Draws                       |
| `home_draws`          |      _Integer_     |                     Total Home Draws                     |
| `away_draws`          |      _Integer_     |                     Total Away Draws                     |
| `losses`              |      _Integer_     |                       Total Losses                       |
| `home_losses`         |      _Integer_     |                     Total Home Losses                    |
| `away_losses`         |      _Integer_     |                     Total Away Losses                    |
| `goals_scored`        |      _Integer_     |                    Total Goals Scored                    |
| `home_goals_scored`   |      _Integer_     |                  Total Home Goals Scored                 |
| `away_goals_scored`   |      _Integer_     |                  Total Away Goals Scored                 |
| `goals_conceded`      |      _Integer_     |                   Total Goals Conceded                   |
| `home_goals_conceded` |      _Integer_     |                 Total Home Goals Conceded                |
| `away_goals_conceded` |      _Integer_     |                 Total Away Goals Conceded                |
| `goals_difference`    |      _Integer_     | Goals Difference (**goals_scored** - **goals_conceded**) |
| `points`              |      _Integer_     |                       Total Points                       |
| `home_points`         |      _Integer_     |                     Total Home Points                    |
| `away_points`         |      _Integer_     |                     Total Away Points                    |
| `next_fixture`        |      _String_      |          Next opponent in the following matchday         |
| `previous_fixtures`   | _Array of Strings_ |           List of all previous fixtures played           |
| `results`             | _Array of Strings_ |                 List of all match results                |
| `form`                | _Array of Strings_ |                       List of form                       |

#### season_fixtures

| Property Name             |      Data Type     |                        Description                       |
| ------------------------- | :----------------: | :------------------------------------------------------: |
| `matchday`                |      _Integer_     |                  Match Day / Match Week                  |
| `upcoming`                |      _Boolean_     |    TRUE for upcoming round of matches, FALSE otherwise   |
| `total_goals_scored`      |      _Integer_     |         Total goals scored in the given matchweek        |
| `total_home_goals_scored` |      _Integer_     |      Total home goals scored in the given matchweek      |
| `total_away_goals_scored` |      _Integer_     |      Total away goals scored in the given matchweek      |
| `number_of_own_goals`     |      _Integer_     | Total numbers of own goals scored in the given matchweek |
| [`fixtures`](#fixtures)   | _Array of Objects_ |                  Detail of every Fixture                 |

#### players

| Property Name            | Data Type |                     Description                    |
| ------------------------ | :-------: | :------------------------------------------------: |
| `id`                     | _Integer_ |                      Unique ID                     |
| `club_code`              |  _String_ |                Associated club code                |
| `current_club`           |  _String_ |                Associated club name                |
| `previous_club`          |  _String_ |             Last Associated club if any            |
| `first_name`             |  _String_ |                     First Name                     |
| `middle_name`            |  _String_ |                 Middle Name if any                 |
| `last_name`              |  _String_ |                      Last Name                     |
| `jersey_name`            |  _String_ |                   Name on Jersey                   |
| `jersey_number`          |  _String_ |                  Number on Jersey                  |
| `nationality`            |  _String_ |                     Nationality                    |
| `position`               |  _String_ |                  Playing Position                  |
| `appearances`            | _Integer_ | Total appearances including substitute appearances |
| `substitute_appearances` | _Integer_ |            Total Substitute appearances            |
| `goals_scored`           | _Integer_ |                 Total Goals scored                 |
| `own_goals`              | _Integer_ |                   Total Own goals                  |
| `assists_made`           | _Integer_ |                 Total Assists made                 |

#### goals

| Property Name                       | Data Type |                        Description                        |
| ----------------------------------- | :-------: | :-------------------------------------------------------: |
| `id`                                | _Integer_ |                 Incremental count of goals                |
| `home_team`                         |  _String_ |                   Home team of the match                  |
| `away_team`                         |  _String_ |                   Away team of the match                  |
| `goal_scorer_id`                    | _Integer_ |          Goal scorer ID from the _players_ array          |
| `goal_scored_for`                   |  _String_ |                     Goal scorer's team                    |
| `goal_scorer_name`                  |  _String_ |                     Goal scorer's name                    |
| `goal_scorer_jersey_number`         | _Integer_ |                Goal scorer's Jersey number                |
| `scoring_minute`                    |  _String_ | Goal scoring minute (_String for stoppage time addition_) |
| `assist_given`                      | _Boolean_ |              Assist for the goal, if provided             |
| [`assist_details`](#assist_details) |  _Object_ |        Assist details if provided otherwise _null_        |
| `is_penalty`                        | _Boolean_ |              True if scored from penalty spot             |

#### assists

| Property Name                      | Data Type |                     Description                     |
| ---------------------------------- | :-------: | :-------------------------------------------------: |
| `id`                               | _Integer_ |             Incremental count of assists            |
| `home_team`                        |  _String_ |                Home team of the match               |
| `away_team`                        |  _String_ |                Away team of the match               |
| `assist_provided_for`              |  _String_ |                Assist provider's team               |
| `assist_provider_id`               | _Integer_ |       Assist provider ID from _players_ array       |
| `assist_provider_name`             |  _String_ |                Assist provider's name               |
| `assist_provider_jersey_number`    |  _String_ |           Assist provider's jersey number           |
| `assist_minute`                    |  _String_ | Assist minute (_String for stoppage time addition_) |
| `assist_provided_to_id`            | _Integer_ |         Goal scorer ID from _players_ array         |
| `assist_provided_to_name`          |  _String_ |                  Goal scorer's name                 |
| `assist_provided_to_jersey_number` | _Integer_ |             Goal scorer's jersey number             |

#### clean_sheets

| Property Name            |      Data Type     |             Description             |
| ------------------------ | :----------------: | :---------------------------------: |
| `id`                     |      _Integer_     |  Goalkeeper ID from _players_ array |
| `club_code`              |      _String_      |    Club association of Goalkeeper   |
| `first_name`             |      _String_      |       Goalkeeper's first name       |
| `middle_name`            |      _String_      |       Goalkeeper's middle name      |
| `last_name`              |      _String_      |        Goalkeeper's last name       |
| `jersey_name`            |      _String_      |       Goalkeeper's jersey name      |
| `jersey_number`          |      _Integer_     |      Goalkeeper's jersey number     |
| `number_of_clean_sheets` |      _Integer_     |   Goalkeeper's clean sheets count   |
| `oppositions`            | _Array of Strings_ | Clean sheets against opposing teams |

#### own_goals

| Property Name          | Data Type |                      Description                      |
| ---------------------- | :-------: | :---------------------------------------------------: |
| `id`                   | _Integer_ |             Incremental count of own goals            |
| `home_team`            |  _String_ |                 Home team of the match                |
| `away_team`            |  _String_ |                 Away team of the match                |
| `against`              |  _String_ |                     Opponent Team                     |
| `scorer_id`            | _Integer_ |             Player ID from _players_ array            |
| `scorer_name`          |  _String_ |                      Player name                      |
| `scorer_jersey_number` | _Integer_ |                  Player jersey number                 |
| `scoring_minute`       |  _String_ | own goal minute (_String for stoppage time addition_) |

##### fixtures

| Property Name       |      Data Type     |                    Description                   |
| ------------------- | :----------------: | :----------------------------------------------: |
| `id`                |      _Integer_     |                     Unique ID                    |
| `home_team`         |      _String_      |         Name of Home Team of the Fixture         |
| `home_team_code`    |      _String_      |        Three letter code of the Home Team        |
| `away_team`         |      _String_      |         Name of Away Team of the Fixture         |
| `away_team_code`    |      _String_      |        Three letter code of the Away Team        |
| `fixture_code`      |      _String_      |          Six letter code of the Fixture          |
| `venue`             |      _String_      |               Venue of the Fixture               |
| `date`              |      _String_      |                Date (_DD-MM-YYYY_)               |
| `local_time`        |      _String_      |         Fixture Kick-off time in UK times        |
| `attendance`        |      _Integer_     |                 Total Attendance                 |
| `half_time_score`   |      _String_      |                Score at Half Time                |
| `full_time_score`   |      _String_      |                Score at Full Time                |
| `home_team_goals`   |      _Integer_     |           Number of Goals by Home Team           |
| `away_team_goals`   |      _Integer_     |           Number of Goals by Away Team           |
| `home_team_scorers` | _Array of Strings_ | List of goals scorers for home team with minutes |
| `away_team_scorers` | _Array of Strings_ | List of goals scorers for away team with minutes |
| `postponed`         |      _Boolean_     |   True if Fixture is postponed, false otherwise  |
| `status`            |      _String_      |              Fixture Current Status              |

##### assist_details

| Property Name                   | Data Type |               Description               |
| ------------------------------- | :-------: | :-------------------------------------: |
| `assist_provider_id`            | _Integer_ | Assist provider ID from _players_ array |
| `assist_provider_name`          |  _String_ |          Assist provider's name         |
| `assist_provider_jersey_number` | _Integer_ |     Assist provider's jersey number     |
