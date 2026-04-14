# WAR
WAR — Python OOP Card Game
A fully playable simulation of the card game War built with Python, demonstrating object-oriented programming and game loop design.
What It Does
Simulates a complete game of War between two players. Each player flips a card each round — the higher card wins both cards. When there is a tie, War is declared and each player puts down five additional cards, with the last card determining the winner of the round. The game ends when one player runs out of cards.
How to Run
bash# Clone the repo
git clone https://github.com/trcpoet/WAR.git
cd WAR

# Open in Jupyter
jupyter notebook WAR.ipynb

# Or run directly with Python
jupyter nbconvert --to script WAR.ipynb
python WAR.py
OOP Design
The project uses three classes with clear, single responsibilities:
Card — Represents a single playing card with suit, rank, and numeric value. Values are stored in a dictionary mapping rank names to integers, making card comparisons straightforward.
Deck — Builds all 52 Card objects across four suits and thirteen ranks. The shuffle() method randomizes the deck in place. deal_one() uses pop() to deal cards from the top.
Player — Represents a player in the game. add_cards() accepts either a single Card or a list of Cards (used when a player wins a round and collects multiple cards). remove_one() takes a card from the player's hand to play each round.
Game Rules Implemented

Standard 52-card deck split evenly between two players at game start
Higher card value wins both played cards each round
On a tie: War is declared, each player plays five additional cards face-down, and the last card determines the winner of all cards on the table
If a player has fewer than five cards when War is declared, they lose immediately
Game ends when one player holds all 52 cards

Python Concepts Demonstrated

Object-oriented programming: classes, __init__, __str__, instance methods
Dictionary lookups for card value mapping
List operations: pop(), append(), extend() for card management
Nested while loops for game flow and war resolution
Type checking with type() to handle single cards vs lists of cards
Break/continue for game state control

Related Projects

BLACKJACK — Blackjack with betting, chips, and dealer AI
blackjack-api — Blackjack converted into a production FastAPI REST API
