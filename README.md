# BestPM-student-project
Web application (economic simulator), which will allow the user (player) to feel like a project manager.
# Project link http://bestpm.pp.ua/

# Objective of the project:
Write a web application (economic simulator), which will allow the user (player) to feel like a project manager and to visit in conditions close to the realities of the IT market.
# Functional purpose of the project:
The project is a multi-user web game that contains a set of modules, entities and connections between them, which allows the user to manage the game version of the project manager of the company's IT.
Description of project modules:
# User Profiles
Each user has the opportunity to become a participant in the project after completing the registration procedure. When registering, the user must enter a unique username containing from 6 to 32 characters, a unique mail address in the format **@**.** and a password containing from 6 to 32 characters, after the successful registration of the user is automatically logged into the game. Users have access to their profile page, which contains the login, email, photo of the user. The game has the ability to recover the password using a letter that will be sent to the user's email address (the password recovery link is valid for 24 hours). If the renewal link has expired, the user will be redirected to the email password recovery page.
# Offices
In the game there are three types of offices (office level 1 for 5 programmers, office level 2 for 20 programmers, office level 3 for 50 programmers), on which the maximum number of programmers hired by the user and other game modules. When the game starts, all users get an "office level 1". All users can buy higher-level offices for game currency.
# Project Market
In the game there is a market of projects on which the user can take projects for the game. Projects are generated automatically or created by the administrator, and stored in the database.
# Market of programmers
The game has a market of programmers on which the user can hire programmers to play. Programmers are generated automatically or created by the administrator, and stored in the database. In the market of programmers, the game users see 10 programmers selected from the database randomly (there are at least one senior or teamlead programmer in the list of programmers, at least two middle-level programmers, and at least three junior programmers). Programmers after hiring are attached to the user, all programmers have motivators tied to this user.
# Credits
In the game, players can take credits in game currency. Loans are generated automatically or created by the administrator. On the credits page, the game users see 10 credits generated randomly.
# Market motivators
In the game there is a market of motivators, where the player can buy them for the game currency. Motivators are of two types: permanent and temporary. Motivators are attached to the user, affect all of the user's programmers, except those that are affected by the random event. All motivators positively influence the level of motivation of programmers. When buying a motivator, the player gets an increase in the motivation of programmers which decreases throughout the game, but always has a value of at least zero. Motivators are generated automatically or created by the administrator, and stored in the database.
# Game mechanics
The game has playing time (playing days and playing months, consisting of 30 game days). One game day is equal to one minute of real time. The game uses two game currency: currency "Bucks" - used to charge money to the player and deduct money from the player; currency "Coins" - is bought by the player for real money, used to buy motivators and offices.
# A) Random events
Random events are generated automatically for each user at random intervals throughout the game. The probability of occurrence of random events affecting the motivation of programmers is negatively greater than the probability of occurrence of positive random events. All events that happened to the player are stored in the player's event history displayed as pop-up messages throughout the game. Random events are divided into three groups according to the nature of the impact on the gameplay:
# A.1) The players acting on all programmers
Change the level of motivation of all programmers alike.
# A.2) The players acting on the same programmer
Change the level of motivation of one programmer, chosen randomly.
# A.3) Players acting on the balance
Change the player's balance at random, but not more than 5% of the total balance. Both positively (investors) and negative (tax, etc.).
# B) Charge of money
The player is credited for the execution of projects:
For projects with the type of payment "TIMEMATERIAL" on the first day of each game month;
For projects with the type of payment "FIXPRICE" when the value of "project complexity" is reduced to zero;
If there is an accidental event that positively affects the player's balance.
# C) Subtraction of money
The player deducts money:
To pay salaries to programmers on the first day of each game month;
For payments on current loans on the first day of each game month;
If a random event occurs that adversely affects the player's balance;
To pay salaries to programmers who were fired during the game at the time of their dismissal for all unpaid days that the programmer worked;
# Management of game sessions (stop game)
At the entrance to the game for the player begins the game session (the countdown of game days begins, the game mechanics begins to work). The player can finish the game session if he quits the game. If the player did not perform any actions in the game for 30 game days - the game session will be interrupted by the game server automatically.
# End of the game
If during the game the player's balance in the currency "Banks" falls below "-10.000" the game ends, namely: the player wipes out all the offices acquired / acquired during the game, projects, programmers, credits, motivators. The player receives an "office level 1" and 5000 "bucks" on the game account. The balance of the "Coin" remains unchanged.
