# Basic-Chatbot
def get_bot_response(user_input):
    user_input = user_input.lower().strip()

    if user_input in ["hello", "hi", "hey"]:
        return "Hello! How can I help you today?"
    elif user_input in ["how are you", "how are you?"]:
        return "I'm doing well, thank you for asking! How about you?"
    elif user_input in ["what is your name", "who are you"]:
        return "I am a simple rule-based Chatbot created for CodeAlpha assignment."
    elif user_input in ["bye", "goodbye", "exit"]:
        return "Goodbye! Have a great day ahead!"
    else:
        return "I'm sorry, I don't understand that. You can say 'hello', 'how are you', or 'bye'."

def run_chatbot():
    print("=== Rule-Based Chatbot ===")
    print("Type 'bye' or 'exit' to end the conversation.\n")

    while True:
        user_msg = input("You: ")
        if not user_msg:
            continue
        
        response = get_bot_response(user_msg)
        print(f"Bot: {response}")

        if user_msg.lower().strip() in ["bye", "goodbye", "exit"]:
            break

if __name__ == "__main__":
    run_chatbot()
