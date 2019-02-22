# Elevens-Lab-Activity7

1. What items would be necessary if you were playing a game of Elevens at your desk (not on the
computer)? List the private instance variables needed for the ElevensBoard class.

Flat Surface
Cards(Layout of Cards and Cards in Deck)
Cursor for selection(Hand)
	Select Cards in Deck
	Set Cards Aside
Place to set cards aside

2. Write an algorithm that describes the actions necessary to play the Elevens game.

1. Lay cards down in a 3x3 square
*Check to see if there are two cards that contain numbers that equal 11. If not, the game is lost, if so continue to 2
2. match 2 cards that contain numbers equal to 11 (select)
3. Replace them with the two top cards on the deck
4. Repeat until all of deck is gone.

3. Now examine the partially implemented ElevensBoard.java file found in the Activity7
Starter Code directory. Does the ElevensBoard class contain all the state and behavior
necessary to play the game?

No, Not all of them. Most though

4. ElevensBoard.java contains three helper methods. These helper methods are private
because they are only called from the ElevensBoard class.

a. Where is the dealMyCards method called in ElevensBoard?

Line 206


b. Which public methods should call the containsPairSum11 and containsJQK
methods?


anotherPlayIsPossible()
isLegal()



c. It’s important to understand how the cardIndexes method works, and how the list that it
returns is used. Suppose that cards contains the elements shown below. Trace the execution
of the cardIndexes method to determine what list will be returned. Complete the diagram
below by filling in the elements of the returned list, and by showing how those values index
cards. Note that the returned list may have less than 9 elements.

![My image](https://bsimps3.github.io/Elevens-Lab-Activity7/cards.png)

{0, 1, 3, 6,7}

d. Complete the following printCards method to print all of the elements of cards that are
indexed by cIndexes.

    public static printCards(ElevensBoard board) {

    	List<Integer> cIndexes = board.cardIndexes();
	for(int h = 0; h < cIndexes.size(); h++){
		println(cIndexes.get(h));
	}	

  
    }
  
  
  e. Which one of the methods that you identified in question 4b above needs to call the
      cardIndexes method before calling the containsPairSum11 and containsJQK
      methods? Why?
	
	anotherPlayIsPossible(): the cards on the board need to be checked for possible 	sums in order for the user to continue to play. If no sums are available, the game 	ends. Cards removed from board also need to be removed in order for the sum 		methods to efficiently check every variable	

		
