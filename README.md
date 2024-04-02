# World Cup Database Project

This project involves creating a PostgreSQL database named "worldcup" and populating it with data from the provided games.csv file. Additionally, you will complete a set of queries to extract specific information from the database.

## Part 1: Create the Database

1. Log into the psql interactive terminal with the command `psql --username=freecodecamp --dbname=postgres`.
2. Create the database structure according to the user stories below.
3. Connect to the "worldcup" database after creating it.

## Part 2: Insert the Data

1. Complete the `insert_data.sh` script to correctly insert all the data from `games.csv` into the database.
2. Use the provided `$PSQL` variable to make database queries efficiently.
3. Ensure that the script inserts each unique team into the "teams" table and adds rows for each game from the `games.csv` file into the "games" table.
4. Verify that there are 24 rows in the "teams" table and 32 rows in the "games" table after running the script.
5. Avoid hard-coding values and use appropriate IDs from the "teams" table when inserting data into the "games" table.

## Part 3: Query the Database

1. Complete the empty `echo` commands in the `queries.sh` file to produce output matching the `expected_output.txt` file.
2. Test your queries in the psql prompt first to ensure correctness.
3. Use the provided `$PSQL` variable to execute queries efficiently.
4. Pay attention to the number of decimal places in some query results to match the expected output exactly.
5. Ensure that the output of your queries exactly matches the content in the `expected_output.txt` file.

## Notes

- Ensure that both `.sh` script files have executable permissions.
- Save a dump of your database using `pg_dump` command to preserve your progress.
- Save the final version of your `.sh` files and the `worldcup.sql` dump in a public repository for submission.

## User Stories

1. Create a database named "worldcup".
2. Connect to the "worldcup" database and create tables for "teams" and "games".
3. The "teams" table should have a primary key column "team_id" of type SERIAL and a unique column "name".
4. The "games" table should have a primary key column "game_id" of type SERIAL, and columns for "year", "round", "winner_id", "opponent_id", "winner_goals", and "opponent_goals".
5. The "games" table should have foreign key columns "winner_id" and "opponent_id" referencing the "team_id" column of the "teams" table.
6. All columns in both tables should have the NOT NULL constraint.
7. The insert_data.sh script should add each unique team to the "teams" table (24 rows) and insert rows for each game from the games.csv file into the "games" table (32 rows).
8. Complete the queries.sh file to produce output matching the expected_output.txt file exactly.
