import random
import time

def print_board(player1_score, player2_score):
    print(f"Player 1: {player1_score} | Player 2: {player2_score}")
    print("-" * 20)

def play_ping_pong():
    player1_score = 0
    player2_score = 0
    max_score = 5  # গেমটি ৫ পয়েন্টে শেষ হবে

    while player1_score < max_score and player2_score < max_score:
        time.sleep(1)
        ball = random.choice([1, 2])  # ১ = প্লেয়ার ১, ২ = প্লেয়ার ২
        if ball == 1:
            player1_score += 1
            print("Player 1 scores!")
        else:
            player2_score += 1
            print("Player 2 scores!")

        print_board(player1_score, player2_score)

    if player1_score > player2_score:
        print("Player 1 wins!")
    else:
        print("Player 2 wins!")

if __name__ == "__main__":
    play_ping_pong()
