# Prework review

Hi Ignacio 🙋🏻‍♀️!! I am writing to give you some feedback on your prework! 🚀

### 1. Snail-and-Well

Go go go with the snail!!! 

Overall you did a very good job, I will comment here a few things in case they add value for you:

- In the second bonus's exercise *What is its maximum displacement in one day? And its minimum? Calculate the displacement using only the travel distance of the days used to get out of the well* we had to calculate the maximum and minimun distance of snail travel.

    Ok, you have obtained the max and min of snail displacment, but this values should be calculated considering the nightly distance as you did in the exercise 3. 

### 2. Duel-of-Sorcerers

Let's go with this exercise! 
- In the first question the exercise ask us about a number of spells that the sorcerers cast. As you code this exercise it is perfect! You can also use the `len` method, which give us the longitude of a list
    ```python
    spells = len(gandalf) 
    ```
- In the exercise 3 *Using the lists of spells of both sorcerers, update variables gandalf_wins and saruman_wins to count the number of times each sorcerer wins a clash.* 
As you resolve the problem it is perfect. Another way to reach the correct result is using the `zip` method. I give you some documentation [docu](https://realpython.com/python-zip-function/#:~:text=Python's%20zip()%20function%20is,%2C%20sets%2C%20and%20so%20on.) to explore it!
    ```python
    for g, s in zip(gandalf, saruman):
        if g > s:
            gandalf_wins += 1
        elif g < s:
            saruman_wins += 1
        else: 
            ties += 1
    # with this method it is not necessary to create a new variable to iterate. 
    ```


Note that, in the same way you use the `statistic` library to calculate the standard deviation, you could use this library to calculate the `mean`

Really good job in this part of the prework Ignacio!!!🚀

### 3. Bus

Nothing to say Ignacio!!! Really nice work 😃

### 4. Robin-Hood

In this part of the prework you were really eficient in your code, congratulations Ignacio! 
- As a detail, in the exercise 2 *Calculate how many arrows have fallen in each quadrant.*, you did: 
    ```python
    for p in points:
        if p[0] > 0:
            if p[1] > 0:
                q1.append(p)
            if p[1] < 0:
                q2.append(p)
        if p[0] < 0:
            if p[1] > 0:
                q4.append(p)
            if p[1] < 0:
                q3.append(p)
    ```
The if statement alone tells us that if a condition is true it will execute a block of statements and if the condition is false it won’t. But what if we want to do something else if the condition is false. Here comes the else statement. We can use the else statement with if statement to execute a block of code when the condition is false.

- In the last part of this jupyter, we had to create a function that give a distance to the center which we could use in the last exercise. One possible option could be: 
    ```python
    def find_distance(point):
        x, y = point
        return (x ** 2 + y ** 2) ** 0.5
    ```
    Then, we could use this function to select those arrows that don't hit the target: 

    ```python

    points_outside_target = []

    for coordinates in points:
        if (find_distance(coordinates) > 9):
            points_outside_target.append(coordinates)
    arrows_missed = len(points_outside_target)

    print (arrows_missed)
    print (points_outside_target)
    ```


### 5. Temperature-Processor

This exercise it is perfect! The objetive was learn about `list` and how iterate through them and you do it💪!

### 6. Rock–Paper–Scissors
Let's go with this exercise, overall it is perfect, however, there are part of the code that you could atomize. For example: 
- In the exercise 8 *Define a function that checks who won a round.* 
  The `game` function it is perfect, but we could optimize our code using the `or` and `and` operators and reduce the number of lines. It is good practice to try to avoid repeating lines of code that are too similar. One possible solution in this case could be: 

  ```python
  def game(player, pc):
    # return true is the player beats the pc
    # winning conditions: r > s, s > p, p > r
    if (player == pc): 
        return 0
    elif (player == 'r' and pc == 's') or (player == 's' and pc == 'p') or (player == 'p' and pc == 'r'):
        return 1
    else: 
        return 0
  ```
- The bonus exercise was similar to rock, paper, scissors, the only thing we should do is add two more possible options. 
  
Still, great job Ignacio!!!! You are on the data analysis rocket! 🚀
