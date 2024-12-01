def start_game():
    print("Welcome to 'The Adventure of the Lost Treasure'!")
    print("Your journey begins now...")
    scene_1()

def scene_1():
    print("\nYou stand at the entrance of a dark cave.")
    print("1. Enter the cave cautiously.")
    print("2. Look around the entrance for clues.")
    print("3. Turn back and leave.")
    
    choice = input("What do you do? (1/2/3): ")
    
    if choice == "1":
        scene_2_cave()
    elif choice == "2":
        scene_2_clues()
    elif choice == "3":
        print("\nYou decide adventuring isn’t for you and head home. Game over!")
    else:
        print("\nInvalid choice! Try again.")
        scene_1()

def scene_2_cave():
    print("\nYou enter the cave cautiously and find a fork in the path.")
    print("1. Take the left tunnel (it smells damp).")
    print("2. Take the right tunnel (you hear faint noises).")
    
    choice = input("Which path do you choose? (1/2): ")
    
    if choice == "1":
        print("\nYou find a hidden underground river but no treasure. You safely return. You survived!")
    elif choice == "2":
        print("\nYou encounter a sleeping dragon guarding the treasure!")
        scene_3_dragon()
    else:
        print("\nInvalid choice! Try again.")
        scene_2_cave()

def scene_2_clues():
    print("\nYou find strange symbols carved into a rock near the entrance.")
    print("They seem to warn of danger ahead.")
    print("1. Ignore the warning and enter the cave.")
    print("2. Head back and leave.")
    
    choice = input("What do you do? (1/2): ")
    
    if choice == "1":
        scene_2_cave()
    elif choice == "2":
        print("\nYou heed the warning and decide to leave. Maybe some treasures aren’t worth the risk. Game over!")
    else:
        print("\nInvalid choice! Try again.")
        scene_2_clues()

def scene_3_dragon():
    print("\nThe dragon wakes up and roars!")
    print("1. Fight the dragon.")
    print("2. Try to sneak around and grab the treasure.")
    print("3. Run back the way you came.")
    
    choice = input("What do you do? (1/2/3): ")
    
    if choice == "1":
        print("\nYou bravely fight the dragon, but it’s too strong. You perish. Game over!")
    elif choice == "2":
        print("\nYou manage to sneak past the dragon and grab the treasure. You are victorious!")
    elif choice == "3":
        print("\nYou escape the cave safely, but the treasure remains lost. You survived!")
    else:
        print("\nInvalid choice! Try again.")
        scene_3_dragon()

# Start the game
start_game()
