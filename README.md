import random

def magic_8_ball():
    # List of possible answers
    responses = [
        "It is certain", "It is decidedly so", "Without a doubt", 
        "Yes, definitely", "You may rely on it", "As I see it, yes", 
        "Most likely", "Outlook good", "Yes", "Signs point to yes", 
        "Reply hazy, try again", "Ask again later", "Better not tell you now", 
        "Cannot predict now", "Concentrate and ask again", "Don't count on it", 
        "My reply is no", "My sources say no", "Outlook not so good", "Very doubtful"
    ]

    # Greet the user
    print("Welcome to the Magic 8-Ball Game!")
    
    while True:
        question = input("\nAsk a yes/no question (or type 'quit' to exit): ").strip()
        
        if question.lower() == 'quit':
            print("Goodbye!")
            break
        elif question.endswith('?'):
            print("Thinking...")
            answer = random.choice(responses)
            print("Magic 8-Ball says: ", answer)
        else:
            print("Please ask a valid yes/no question ending with a '?'")

# Run the game
magic_8_ball()
