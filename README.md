# MazeFinder
# This is a python script to find the way through a maze.Use this link to view:  https://reeborg.ca/reeborg.html?lang=en&amp;mode=python&amp;menu=worlds%2Fmenus%2Freeborg_intro_en.json&amp;name=Maze&amp;url=worlds%2Ftutorial_en%2Fmaze1.json
def turn_right():
    turn_left()
    turn_left()
    turn_left()
    
while not at_goal():
    if wall_in_front():
       if right_is_clear():
          turn_right()
          move()
       else:
          turn_left() 
          if right_is_clear():
              turn_right()
              move()
          else:
              if front_is_clear():
                    move()
              else:
                    turn_left()
                    move()
    elif right_is_clear():
        turn_right()
        move()
    elif front_is_clear():
        move()
    else:
        turn_left()
        
