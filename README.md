# project2
fun math game
import random

score = 0
rounds = 5

print("🎮 Welcome to the Math Game!")
print("You will get", rounds, "questions.\n")

for i in range(rounds):
    num1 = random.randint(1, 20)
    num2 = random.randint(1, 20)
    operation = random.choice(["+", "-", "*"])

    if operation == "+":
        correct = num1 + num2
    elif operation == "-":
        correct = num1 - num2
    else:
        correct = num1 * num2

    print(f"Question {i+1}: {num1} {operation} {num2} = ?")
    
    try:
        answer = int(input("Your answer: "))
        
        if answer == correct:
            print("✅ Correct!\n")
            score += 1
        else:
            print(f"❌ Wrong! The correct answer was {correct}\n")
    
    except:
        print("⚠️ Please enter a number!\n")

print("Game Over!")
print(f"Your score: {score}/{rounds}")

if score == rounds:
    print("🏆 Amazing! Perfect score!")
elif score >= 3:
    print("👍 Good job!")
else:
    print("📚 Keep practicing!")
