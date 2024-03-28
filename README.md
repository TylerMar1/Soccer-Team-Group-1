# MIST 4610 Group Project 1 
### Group Name:

Sp24_47114_Group 1

### Group Members:

Isabelle Kiser 
[@isabellekiser](https://github.com/isabellekiser)

Will Cobb 
[@wjc56122](https://github.com/wjc56122)

Bhavik Maniklal 
[@BhavikManiklal](https://github.com/BhavikManiklal ) 

Ty Marcinczyk 
[@TylerMar1](https://github.com/TylerMar1)

Ryan Schoessling 
[@rschoess3](https://github.com/rschoess3)

Jaiden Timmons 
[@jaidentimmons](https://github.com/jaidentimmons)

### Client Scenario Overview:

Community FC, under the dynamic leadership of the owner, has established itself as a cornerstone of local soccer culture, offering extensive programs that cater to various age groups, skill levels, and interests. The club aims to nurture talent, promote physical well-being, and foster a sense of community through soccer. Its offerings include many levels of teams, training camps, weekend matches, and special events.

The club's facilities are top-notch, featuring multiple soccer fields, a clubhouse with locker rooms, a gym, and a merchandise shop. Community FC prides itself on its inclusive environment, welcoming members from various backgrounds to participate in its programs.

### Project Problem:

At Community FC, our primary challenge revolves around the complex coordination needed to manage our soccer club efficiently. From member management and team organization to league administration, facility scheduling, financial transactions, and merchandise sales, many interconnected elements require seamless integration.

Coordinating member profiles, team assignments, league participation, facility bookings, financial transactions, and merchandise inventory demands meticulous attention to detail and effective communication among staff, coaches, players, and parents.

To tackle this challenge, we require a relational database system that can streamline these processes, providing real-time visibility into club operations and facilitating smooth coordination across all facets of our organization. This solution will enable us to enhance member experiences, optimize resource utilization, and uphold Community FC's commitment to excellence in our local soccer community.

### Data Model:
![d](https://github.com/isabellekiser/Soccer-Team-MIST4610/assets/149964200/b661c931-e2fb-49a2-a013-38d1e4faba8c)

Our data model is based on the structure of a hypothetical professional soccer club. The Member entity represents individual members of the club. A member can be a player, coach, athletic trainer, etc. This is represented by the “role” attribute within member. A member is further detailed by the entity Membership which is related to Member with a many-to-one relationship. A member may have multiple membership types if they have multiple duties with the club. 

Member is also related to Transactions with a one-to-many relationship which shows that a member can make multiple transactions with the club. Our soccer club also sells merchandise. The transaction is related to the Merchandise entity through a many-to-one relationship. This represents that a piece of merchandise can be sold in multiple transactions.

Our soccer club has many different teams ranging from the highest level professional teams to many developmental teams where we have players that we believe will one day be good enough to play on our top team. The Team entity is related to Member with a many-to-many relationship through the associative entity MemberTeam. MemberTeam represents the different team members on each team.

Since we have multiple teams with different skill levels, naturally they play in different leagues. The League entity is related to team through a one-to-many relationship. This is because a league hold host to many different teams, but a team can only play in one league.

Each team has a number of different matches they play throughout the season. This is why Team is related to the Matches entity through a many-to-many relationship with the associated entity TeamMatches. TeamMatches represents the individual matches and which team played in the match.

Our players will only get better if they practice their craft. This is why we host multiple training sessions per week. Team is connected to the TrainingSession entity by a one-to-many relationship. This represents how one team has many different training sessions. These training sessions take place in one of our state-of-the-art facilities. The Facility entity is connected to TrainingSession by a one-to-many relationship because a facility can host many different training sessions.

Since our facilities are so nice, we also host matches in these facilities. This is why Facility has a one-to-many relationship with the Matches entity. One facility will host many matches.

Being such a popular soccer club, we have many spectators at every game. The spectators have to buy tickets to gain admission to the matches. This is why there is a one-to-many relationship between Matches and the Ticket entity. One match will have many tickets.

### Data Dictionary:
# <img width="664" alt="Screenshot 2024-03-27 at 7 18 15 PM" src="https://github.com/TylerMar1/Soccer-Team-Group-1/assets/150088753/fa573d2b-8523-4ac4-9abc-d61e64b83a9f">
# <img width="655" alt="Screenshot 2024-03-27 at 7 17 48 PM" src="https://github.com/TylerMar1/Soccer-Team-Group-1/assets/150088753/9801610b-9b8f-4015-a864-111e297df126">
# <img width="661" alt="Screenshot 2024-03-27 at 7 19 42 PM" src="https://github.com/TylerMar1/Soccer-Team-Group-1/assets/150088753/56a24bc3-5a8e-43db-8f69-3bf2d102536c">
# <img width="663" alt="Screenshot 2024-03-27 at 7 20 32 PM" src="https://github.com/TylerMar1/Soccer-Team-Group-1/assets/150088753/2ac438ec-907c-4c0e-8249-04e122cd660f">
# <img width="640" alt="Screenshot 2024-03-27 at 7 20 59 PM" src="https://github.com/TylerMar1/Soccer-Team-Group-1/assets/150088753/691eb359-34ed-4ddf-975f-71f06002a6e7">
# <img width="652" alt="Screenshot 2024-03-27 at 7 21 16 PM" src="https://github.com/TylerMar1/Soccer-Team-Group-1/assets/150088753/a227f9e9-d186-4692-beac-f490b27475f1">
# <img width="651" alt="Screenshot 2024-03-27 at 7 21 35 PM" src="https://github.com/TylerMar1/Soccer-Team-Group-1/assets/150088753/44b26c7f-f210-4b16-bc68-613d2e1362b6">
# <img width="707" alt="Screenshot 2024-03-27 at 7 22 59 PM" src="https://github.com/TylerMar1/Soccer-Team-Group-1/assets/150088753/c58668b5-de5c-4007-83de-d5ff766bcca0">
# <img width="635" alt="Screenshot 2024-03-27 at 7 24 09 PM" src="https://github.com/TylerMar1/Soccer-Team-Group-1/assets/150088753/bdc1c0c1-a837-462d-80a6-38386924b965">
# <img width="636" alt="Screenshot 2024-03-27 at 7 24 29 PM" src="https://github.com/TylerMar1/Soccer-Team-Group-1/assets/150088753/e83fc649-5a19-4acf-9de6-8d2a04433bd2">
# <img width="635" alt="Screenshot 2024-03-27 at 7 24 53 PM" src="https://github.com/TylerMar1/Soccer-Team-Group-1/assets/150088753/c9b31699-476e-49ed-8b2c-42285084bcad">
# <img width="678" alt="Screenshot 2024-03-27 at 7 25 49 PM" src="https://github.com/TylerMar1/Soccer-Team-Group-1/assets/150088753/42fd42ca-14d0-4a16-b297-138373b8f046">

### Queries:
<img width="760" alt="Screenshot 2024-03-27 at 4 57 14 PM" src="https://github.com/isabellekiser/Soccer-Team/assets/150088753/96ebecb4-8f05-4fc1-8f98-fdbe39497afa">

Query 1:
# ![query 1](https://github.com/isabellekiser/Soccer-Team/assets/149964200/8ef2d313-7802-407e-bb86-dea37f59fc90)
Query 1 selects product names and their corresponding stock levels from the "Merchandise" table, filtering for items with stock levels below 40 and prices exceeding 50. This provides managers with a concise list of high-value products that are running low on stock, aiding in strategic inventory management. By prioritizing restocking efforts for these items, managers can ensure the availability of profitable products to meet customer demand, optimize inventory levels, and minimize the risk of stockouts, thereby enhancing sales and customer satisfaction.

Query 2:
# ![query 2](https://github.com/isabellekiser/Soccer-Team/assets/149964200/bce6e505-feab-4b6d-9c38-925385fbd406)
Query 2 aggregates data from a training session database, counting the occurrences of each focus area within the sessions. This information is invaluable for managers as it provides a clear snapshot of where training efforts are being directed. By identifying which skills or topics receive more attention, managers can allocate resources more effectively, tailor training programs to address specific needs and ensure a balanced approach to skill development within the organization. Additionally, it enables managers to pinpoint areas of strength and areas needing improvement, facilitating informed decision-making to optimize workforce performance and achieve organizational goals efficiently.

Query 3:
# ![query 3](https://github.com/isabellekiser/Soccer-Team/assets/149964200/f2eb3074-85a9-47a3-9c65-27fddb524384)
Query  3 combines data from two tables, "Team" and "TrainingSession", to provide managerial insights into team training activities. By joining the tables based on matching team IDs, the query counts the number of training sessions associated with each team and presents this information alongside the team ID and name. This allows managers to assess the level of training engagement within each team, identify high-performing teams that are actively participating in training sessions, and pinpoint teams that may require additional support or encouragement to engage in training activities. 

Query 4:
# ![query 4](https://github.com/isabellekiser/Soccer-Team/assets/149964200/9de8f5a8-f84d-4f2f-b736-bb9c49171dfb)
Query 4 retrieves the genders of members whose memberships are set to end in 2024 by joining the "Membership" table with the "Member" table on their respective IDs and filtering for memberships ending in that year. This information is crucial for soccer team management as it allows them to understand the demographic composition of expiring memberships, which in turn informs targeted retention strategies, marketing efforts, and resource allocation. By knowing the genders of members whose memberships are ending, the management can tailor communication, programming, and facilities to better cater to the diverse preferences of their membership base, ultimately fostering greater engagement and ensuring the club's long-term success.

Query 5:
# ![query 5](https://github.com/isabellekiser/Soccer-Team/assets/149964200/8b6ba846-7031-419c-94c1-34856b74d720)
This SQL query retrieves data about matches, including their names and attendance figures, while also calculating the percentage of the facility filled for each match. Joining the Matches table with the Facility table based on matching facility IDs ensures accurate attendance data aligned with the corresponding facility capacity. The WHERE clause filters only matches with a status of "TRUE", ensuring the inclusion of active matches. Results are then ordered by the calculated percentage of facilities filled, with higher percentages appearing first. The query's concise yet comprehensive structure enables efficient analysis of match attendance and facility utilization.

Query 6:
# ![query 6](https://github.com/isabellekiser/Soccer-Team/assets/149964200/cdca4ca4-8794-4772-9a60-a7a1cc5642f0)
The SQL query provides a list of coaches who earn above the average salary of other coaches, highlighting the club's financial commitments to its coaching staff. It's a useful tool for budgeting, ensuring competitive compensation, and assessing the correlation between salary and coach performance. The data aids in financial planning and helps establish benchmarks for future salary negotiations. For a pro soccer team, this information is crucial for maintaining a balanced budget while ensuring the coaching staff is well-compensated and effective.

Query 7:
# ![query 7](https://github.com/isabellekiser/Soccer-Team/assets/149964200/72d5c9e0-999e-4d5e-b2c6-f522c0d96e3e)
The SQL query in question identifies the top three most profitable jerseys by multiplying the sales price by the number sold, specifically filtering for items categorized as "jerseys." It's crucial for a soccer team's merchandise management because it highlights which jerseys are the biggest revenue generators, aiding in inventory decisions and marketing focus. The results, ordered from highest to lowest profit, allow management to pinpoint successful products and strategize on how to leverage this information for future sales and promotions.

Query 8:
# ![query 8](https://github.com/isabellekiser/Soccer-Team/assets/149964200/ce3c7421-68c6-48f3-9448-09d874c78a9c)
The SQL query calculates the combined salaries of members in each team, specifically for those teams at level 3 or higher, and sorts the teams by their total salary expenditure in descending order. This information is crucial for a league manager to understand the financial commitments of different teams, assisting in budget comparisons and financial health assessments across the league. High-salary teams can be a focus for investment analysis and revenue generation strategies.

Query 9:
# ![query 9](https://github.com/isabellekiser/Soccer-Team/assets/149964200/ce6d7ba0-b8cf-482f-8670-64e769fafd63)
The SQL query identifies club members who have spent more than $400 in total transactions, highlighting the highest spending individuals. This insight is valuable for recognizing and potentially rewarding top patrons, or for targeted marketing efforts. It's also useful for financial analysis, as tracking spending patterns can inform budgetary decisions and revenue forecasts for a soccer club.

Query 10:
# ![query 10](https://github.com/isabellekiser/Soccer-Team/assets/149964200/4e37e059-22b8-4e50-964c-632b93956060)
The SQL query retrieves the count of matches played at each facility type for every league, indicating which types of pitches are most frequently used. This information is valuable for league managers to optimize the use of facilities and potentially direct maintenance and investment efforts where needed. Understanding facility usage patterns also aids in scheduling and could influence future facility developments or enhancements.


### Database information:
Name of the database: Sp24_47114_Group 1

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();
