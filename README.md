# MIST-4610-Group-Project-1
## Team Name
29704 Group 7
## Team Members
1) Alex Kang @ALEXKANG1
2) Andy Kim @Andykim2003
3) Braden Johnson @baj30400
4) Jake Page @jtp38938
5) Justin Hozman @justinhozman
## Problem Description
The problem scenario we are modeling is for an NBA organization. Player is a central piece that connects to many different entities in the data model. As players are paid to play games they create injury reports, contracts, and have statistics for every game they play in. The organization has many staff members who receive contracts just as players do to run the behind the scenes of the organization. The organization is also centralized around fans who are supporting the organization financially. Fans purchase merchandise as well as tickets in order to attend games. Our group wants to model the relationships between the different entities and input data for the attributes. We are creating queries on the data to receive beneficial information about the organization and discover optimal performance. 
## Data Model
Our data model is based on an NBA organization. The player entity represents the players on the team and includes information such as their position, height, and weight. Players get injured from time to time and can have multiple injuries over the course of their career. The injury report entity details the type of injury and the date of the injury as well as when the player is expected to recover. Players can play in many games and games are played by multiple players. Therefore an associative table is created which is PlayerGameStatistics. The associative table includes a player's statistics for a game which are statistics such as points, assists, rebounds, blocks and more. The game entity includes the opponent, venue, and score. 

Contracts are how players and staff are paid. The contract entity includes the salary, start, and end of the contract. A contract is paid out in multiple instances and so there are multiple financial transactions. Financial transactions include the amount, date, and type. Contracts are connected to two entities both through a one to one relationship. The two tables are PlayerContracts and StaffContracts. PlayersContracts will have playerID and contractID as its primary keys and StaffContracts will have staffID and contractID as its primary keys. Players can have many contracts over the course of their career but a contract can only be associated with one player. Staff can also have many different contracts but StaffContracts can only be associated with one staff member. The staff entity includes staffName, staffRole, department, and other information. 

Fans are the main customer for the organization and fans purchase merchandise. Fans can buy as much merchandise as they want and merchandise can be purchased by multiple fans. The fans table includes the name of the fan as well as their email, phone number, and date of birth. The merchandise table includes the item name and the category it belongs to as well as size, color, quantity, and price. The fan and merchandise table share a many to many relationship and create the associative table merchandise purchase. The associative table includes the fan and merchandise primary keys as its own primary keys and includes attributes such as buy price, quantity sold, payment method, and shipping address.

Fans also support the organization by attending games. Games are attended by many fans and fans can attend many games so an associative table is created called tickets. Tickets have the game and fan primary keys as its own primary keys. Attributes include price, purchase date, seat number, and more. The game is also played at an arena. An arena can have many different games played at the venue but a game can only be played at one arena. Arena includes attributes such as arena name, location, seating capacity, amenities, and more. 

<img width="639" alt="Screenshot 2023-11-03 at 2 07 57 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/149821533/4b603184-f859-4ff1-b9a9-9b9ae72c3771">


## Data Dictionary

<img width="755" alt="Screenshot 2023-11-03 at 2 10 23 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/149821533/c062e977-dbaf-4f9c-9df7-0a522478e6a9">

<img width="745" alt="Screenshot 2023-11-03 at 2 11 23 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/149821533/3c1c8c5a-12f1-4173-a27a-72489aa8e4e3">

<img width="775" alt="Screenshot 2023-11-03 at 2 11 50 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/149821533/51bf02cf-a55c-4c95-88a4-9b3555d5fa93">

<img width="754" alt="Screenshot 2023-11-03 at 2 12 53 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/149821533/535bbc56-e953-405b-8ca2-b6908dc2b62a">

<img width="759" alt="Screenshot 2023-11-03 at 2 13 13 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/149821533/1a77ae7b-198d-4050-a2d2-e518e97d31d1">




## Queries

<img width="737" alt="Screenshot 2023-11-03 at 5 23 37 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/131297312/6bc73784-f108-486d-a25f-4a5f4f06669e">


- Query 1 lists the full name of each fan and the total amount of money that each fan has spent on merchandise.
  - <img width="809" alt="Screenshot 2023-11-03 at 2 12 57 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/149818793/fc3889f5-c8c7-4ebb-a374-404fa339c39e">
  - Query 1 allows for the team to see how much money fans are contributing to their merchandise sales. This gives the executives a grasp as to who they could market more toward, if they're hitting target revenue goals, and they could also use the results to get the average amount spent per fan. Moreover, the team could use this to identify who their top spenders are and possibly reward them.

- Query 2 states the average price of a ticket for each ticket selling company as well as their own website's tickets, ordered from most expensive to least expensive.
  - <img width="661" alt="Screenshot 2023-11-03 at 2 17 55 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/149818793/c983a7ad-9940-4dfc-a21f-ab7619f9fb76">
  - Query 2 allows the team to compare each ticket purchasing method to see who provides a bargain and who overprices the tickets. They can also use this data to see if the average fan is better off purchasing tickets from the team website or from the offshoot ticket companies.

- Query 3 lists each player's name and the most points that they have ever scored, ordered from most to least amount of points.
  - <img width="540" alt="Screenshot 2023-11-03 at 2 20 08 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/149818793/263a8e35-a0ac-4022-b529-fdb26cb3ab35">
  - Query 3 allows the team to get a guage of who has ever had a high scoring game and who has not. This means that the team can see who has the potential to have a great game on any given night. It is important to see career highs because it means that the player has the capabilites to produce similar results and can work toward scoring high amounts of points consistently.

- Query 4 lists each player on the roster that has never been on the injured report.
  - <img width="827" alt="Screenshot 2023-11-03 at 2 23 05 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/149818793/ad4b2502-5991-49f0-bc06-b991004d3c0d">
  - It is important that basketball players remain healthy throughout their career. Having players on the team that have never been injured before provides a huge advantage to team because these players can be considered extremely reliable. Players need to be healthy to contribute to their team's success in the regualr season and especially the playoffs.

- Query 5 lists the total amount of money that each player has generated through merchandise products that represent them from greatest to least.
  - <img width="1440" alt="Screenshot 2023-11-03 at 2 35 52 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/149818793/39b06be2-82b3-4980-ae0a-cbfb50d34019">
  - It is very advantageous for teams to know who draws the most and least attention through merchandise sales because it helps the team make more money. This can allow the team to try to boost merchandise sales of the players that have less sales by marketing and showcasing those players on things like commercials and billboards. 

- Query 6 lists the point guards (PGs) that make more money than the average point guard.
  - <img width="1205" alt="Screenshot 2023-11-03 at 2 31 24 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/149818793/bd0d7001-7d5e-4357-b850-412b9f36dd0c">
  - Teams need to see which of their point guards are getting paid more than average for a few reasons. Point guards are very important because they are typically leaders and so called "floor generals" meaning they typically have the ball and inform other teammates where to go. If a certain point guard is making an above average salary, they should be creating a lot of value on the court through personal statistics and team wins.

- Query 7 shows the names and salaries of players who have had career ending injuries from highest to lowest salary.
  -  <img width="625" alt="Screenshot 2023-11-03 at 2 43 58 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/149818793/28196e60-d631-445b-937f-2465ab2ccd2e">
  - Career ending injuries are detrimental to both a team and a player because they can never create value as a player ever again. Teams need to know exactly how much these players are still being paid after a career ending injury because they are going to have to develop a plan to either get rid of the player and their salary, or find a way for the player to create value off the court.

- Query 8 shows the players, their position, and shooting percentages only for players that are point guards (PGs) or shooting guards (SGs) that have also taken more than 8 shots.
  - <img width="622" alt="Screenshot 2023-11-03 at 2 32 01 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/149818793/52ca513c-e487-4109-a584-2cf0f3bfcea6">
  - It is important for teams to know both the standard field goal and three point percentages for players as it is indicative of the value that they bring to the team. This is especially true for guards because they typically rely on shooting the ball from farther from the basket compared to the bigger players near the basket. These shots are much more difficult so if a guard has high percentages, it would be very advantageous for the team to keep that player. It is also important that the player has taken a lot of shots because this typically means that they are a starter and have a large enough sample size.

- Query 9 lists the emails of fans who had their ticket purchase fail along with the price of the ticket and the date the game is supposed to be played on.
  - <img width="622" alt="Screenshot 2023-11-03 at 2 32 55 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/149818793/89ff9db7-828f-4af4-983b-d4468e931ce8">
  - Having this data is very important from a customer service perspective because a fan deserves their money back if they are being restricted from going to the game. This can happen for a multitude of reasons but it is essential for teams to get the money that the fan spent on a ticket back to them as soon as possible to keep them happy.

- Query 10 lists every player and the conference of the college that they attended grouped by two large conferences and then the remaining conferences as one group.
  - <img width="621" alt="Screenshot 2023-11-03 at 2 39 11 PM" src="https://github.com/baj30400/MIST-4610-Group-Project-1/assets/149818793/b25ca164-d4b0-4e9d-8a13-bed4667846e9">
  - The SEC and ACC are two powerful basketball conferences that have historically produced a lot of high level basketball talent. It can be beneficial for a team to know where their players came from because they can use the conference that they come from as a factor. If the team has a lot of good players from the SEC, it could be a good sign that the competition level in the SEC translates to good professional talent so the team can acquire more players from there.

## Database Information
- Name of the Database: ns_F2329704Group7
- Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();
