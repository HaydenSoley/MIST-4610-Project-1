
# MIST 4610 Project 1

# Team Name
Group 10

# Team Memebers:
1. Liam Kilner https://github.com/liamkilner/Project-1-SQL
2. Ashley Potts https://github.com/ashley-potts/MIST-4610-Project1 
3. Emma Surbrook https://github.com/emmasurbrook/MIST-Project 
4. Hayden Soley https://github.com/HaydenSoley/MIST-4610-Project-1
5. Victoria Wiest https://github.com/victoriawiest/MIST4610Project1

# Problem Description:
Pretend you are the owner/operator of a tennis (or football, soccer - your choice) club needing to build a relational database. You hired some students from the MIST 4610 class at the University of Georgia to create the database for you. They need to know more about your organization to identify which entities, attributes, and relationships are important for you. Start by describing your business as a real client. At least 12-15 entities are needed including their respective attributes and relationships. 

# Data Model:
Our model is based on a Soccer Club, called UGA United Soccer Club. Our “Teams” table serves as our central entity, branching to many other tables throughout the model. “Teams” includes many important attributes, such as team name, age group, and practice schedules. Our “Teams” table has a one-to-many relationship, as well as a one-to-one relationship with our “Coaches” table. There are many coaches per team, with one being the head coach, shown by the one-to-one relationship. Our “Coaches” table gives important information about each coach, such as name, contact information, and coaching experience. Additionally, “Teams” links, as a one-to-many relationship, to “Registration”. There are many registrations per team. There is also one player per registration. Our “Registrations” entity as a one-to-one relationship with “Players”. This table includes information such as name, age, contact information, and emergency contacts. “Teams” continues its relationships by having a one-to-many relationship with “Sponsors”. Each team can have multiple sponsors, each of different levels and payments. There is also a one-to-many relationship between “Teams” and “Tournaments”. Each tournament is linked to multiple teams. This table includes important information such as the name, location, and date of the tournaments, as well as the winning team. Our “Tournaments” entity branches to “Facilities”, with multiple facilities as a part of each tournament. Our facilities offer different field conditions, such as turf or grass, and multiple fields within the facility. The “Facilities” entity also links to our “Staff” entity through a one-to-many relationship. Each facility has multiple staff members, where we can find information about their contact information and position. The “Tournaments” entity also links to another entity, “Matches”, through a one-to-many relationship. There are multiple games in each tournament, and also multiple referees in each match. This is shown by the “Matches” and “Referees” entities being connected with a one-to-many relationship. Our “Teams” entity connects to one more entity, “Practice Sessions”, through a one-to-many relationship since there are multiple practice sessions for each team. Since many facilities can have many practice sessions, there is an associative entity between “Practice Sessions” and “Facilities” called “Practice_Sessions_has_Facilities”. This shows which practice sessions are occurring at each facility. Our conversation with our client included three more entities, “Parents/Guardians”, “Payments”, and “Merchandise”, but we felt that it made more sense to include these as attributes in the other existing entities.


# Project Description : 
The current project is to create a relational database that models the general operations of a soccer club. The primary entity of the model is the Teams entity with the Teams representing each individual team that belongs to the UGA United Soccer Club. The Team entity has various relationships with other entities in the model such as Players, Coaches, Tournaments, etc. We are interested in accurately depicting these relationships and generating sample data to ensure that the goals of the database are achieved. Additionally, we plan to execute queries on the sample data to provide information that is relevant to the club from a managerial perspective.

![unnamed](https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148247978/e4ee7ccf-d5b8-4f6d-b998-9454dd7b7361)
# Data Dictionary
![image](https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148247978/ddede0f3-a4a7-49c9-b7df-fda7d907d56e)
![image](https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148247978/54859646-2f9f-4121-9cac-f9b29b0159ae)
![image](https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148247978/2eaa4fe7-6db6-455e-a183-fb1f9b2ee301)
![image](https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148247978/034e6cf6-f14c-48be-b91a-c8ea6a6ec2a6)
![image](https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148247978/7b27b941-a953-4ab9-8697-c1b984305b37)
![image](https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148247978/44bbdea7-3cc1-4a41-8110-a91c9e83bc65)
![image](https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148247978/762a3e7c-4d6b-473e-895a-a43a198e9a0d)
![image](https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148247978/d1fbc0dd-d360-42bd-8d24-e703bb389275)
![image](https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148247978/ef245b5d-5161-4bac-9fd1-3c7449f43019)
![image](https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148247978/611c714d-91fd-4f41-b4e1-a94a9bf0032a)
![image](https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148247978/be515fb6-92a3-4ba8-9d89-75c74e0e8e51)
![image](https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148247978/4353d0f0-3cad-4287-bc9f-ce81eccfe033)


# Queries

![image](https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148247978/989006a0-bab3-4fe6-83b1-87bcd3d4ca79)

1. Retrieve all players who have not suffered any injuries:
This query lists the first name, last name, and team name of all the players who have not suffered any injuries.

<img width="1002" alt="q1" src="https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148873180/c5d9ad91-2f4e-4266-8847-6fb9d04d6925">

From a managerial perspective, this query would be important because knowing what players have not been injured in the past and whether or not they are currently injured or not would be significant in understanding the state of the team and help predict how they would fare in a tournament. For a team that has many injured players it would not be wise to send them to participate in a tournament because they wouldn’t be able to perform on a competitive level with many injured players. 

2. Retrieve the names of the teams and their respective head coaches that won a tournament:
This query lists out the head coaches for teams that won each tournament.

<img width="935" alt="q2" src="https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148873180/51127b15-3bdd-40ee-85ca-7108eb836c76">

The manager would want to know who the head coach is for every team that won the different tournament. This would be important that the manager was aware of which coaches were in charge of the overall winners of the four tournaments. 

3.Write a query that lists the first name of the players on the Lions team.
This query lists the first name of every player on the Lions team.

<img width="1111" alt="q3" src="https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148873180/58199daa-6b66-4946-92fe-6bc2f67ab00e">

This information would be important for a manager who is interested in the Lions team and wants to know who each player is in order to do research on the stats of each player.


4. Write a query to list the names of the teams that played in the S.M.A.S.H tournament and order them in alphabetical order. 
This query lists those teams that played in the S.M.A.S.H tournaments and then orders those teams alphabetically.

<img width="1082" alt="q4" src="https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148873180/55e0d448-379e-4631-8b6f-4d42a165e644">

This query is important from a managerial perspective because the S.M.A.S.H. tournament was the last one of the season. It is important to see which teams practiced the longest before playing in any tournaments to compare performance evaluations.

5. Write a query that shows sponsors who have paid more than the average payment:
This query lists out the name and the payment of those sponsors whose payment amount is greater than the average payment amount made by all the sponsors.

<img width="1079" alt="q5" src="https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148873180/58cacf11-71de-4c2c-8a3e-94333f35ed51">

A manager would want to know this information because it would show which sponsors are the most generous in comparison to the rest. The sponsors that donate the most money would be put on the jerseys of the players. 


6. List of referees for each match:
This query lists the first name and last name of the referees of each match played by the bulldogs. 

<img width="1083" alt="q6" src="https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148873180/35c3d0f6-606a-4c8e-8c5d-d0450b3eb529">

A manager would want to know this information to determine if the bulldogs are cheating so they want to know the referees in order to contact them.

7. List the maintenance staff name from each facility whose field condition is turf:
This query lists all the staff that are maintenance workers at facilities with field conditions that are turf.

<img width="1084" alt="q7" src="https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148873180/e544b8d8-1e44-420e-b56c-0b05b7fca414">

This query would be significant to a manager who would want to understand how many maintenance workers are at a particular facility that has turf.


8. List the team names and the average number of coaching years between those team’s coaches whose average is over 15 years of experience
This query shows the average number of years of experience coaches have for each team where the number of years of experience is greater than 15

<img width="1078" alt="q9" src="https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148873180/3b4250b2-9589-486f-8f6b-6722d3314300">

The manager would want to know this information to understand the individual experience of each coach and which teams have coaches with the most experience. This would allow the manager to assign head coaches to competition levels that are appropriate for their experience level. Coaches with more coaching experience should be assigned to higher competition levels, and the opposite could be said for coaches with less experience. 

9. List the first and last name of each coach that does not have a coaching certificate & their respective team. 
This query shows the first and last name of each individual coach that has no coaching  certification along with the team that they coach for.

<img width="1078" alt="q9" src="https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148873180/15cd54bb-5125-4459-88e1-8000da45efec">

The owner of the Bulldog United soccer club would want to know this information to track each coach’s progress towards obtaining their coaching certification. This would be relevant when coaches are up for evaluation and would help in determining what coaches would be qualified to become a head coach of a team for the upcoming season. 

10. List the tournament name that had a payment average from its teams that was greater than the overall average sponsor payment.
This query shows the name of the tournament that had an average amount of payments that was higher than the average total amount of payments from all sponsors.

<img width="1084" alt="q10" src="https://github.com/HaydenSoley/MIST-4610-Project-1/assets/148873180/5441fd03-b71e-4ab1-83a6-268916def547">

A manager would be interested in this information to determine which tournament had the highest amount of money from its sponsors. It would help them see which tournament was the biggest, most profitable event to these sponsors. This particular tournament had a group of teams that brought money in from some of the highest paying sponsors. 

# Database Information
The name of the database is : cs_g10p1

Additional information: Each query created is marked in the database using stored procedures. The stored procedures can be called using the following format : CALL Q1();
