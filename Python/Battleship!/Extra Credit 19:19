from random import randint

def game():
    board = []

    for x in range(5):
        board.append(["O"] * 5)

    def print_board(board):
        for row in board:
            print " ".join(row)

    print "Let's play Battleship!"
    print_board(board)

    def random_row(board):
        return randint(0, len(board) - 1)

    def random_col(board):
        return randint(0, len(board[0]) - 1)

    ship_row = random_row(board)
    ship_col = random_col(board)

    count = 0

    while count <= 4:
        print "You tried: %s of 5 times" % count
        guess_row = int(raw_input("Guess Row:"))
        guess_col = int(raw_input("Guess Col:"))
        guess_row -= 1
        guess_col -= 1
        count += 1
        if guess_row == ship_row and guess_col == ship_col:
            print "Congratulations! You sunk my battleship!"
            print_board(board)
            break
        elif guess_row >= 5 or guess_col >= 5:
            print "Hey, that's not even on battle area!"
        elif (board[guess_row][guess_col] == "X"):
            print "You was shooting here already!"
        else:
            print "You missed my battleship!"
            board[guess_row][guess_col] = "X"
            print_board(board)
    else:
        print "Game over! Ship was on row %s" %ship_row, "and col %s" % ship_col
        board[ship_row -1][ship_col -1] = "="
        print_board(board)
        new_game = raw_input("Do you want to play again? y/n\n")
        if new_game == "yes" or new_game == "y":
            game()
        else:
            print "Bye!"

game()
