# Chatbot-

def get_reply(msg: str) -> str:
    """Return a canned reply based on the user message."""
    msg = msg.strip().lower()

   if msg in ("hello", "hi", "hey"):
        return "Hi!"
    elif msg in ("how are you", "how's it going", "what's up"):
        return "I'm fine, thanks!"
    elif msg in ("bye", "goodbye", "see you"):
        return "Goodbye!"
    else:
        return "Sorry, I didn't understand that."

def chat():
    print("Chatbot: Hi! Type 'bye' to exit.")
    while True:
        user_input = input("You: ")
        if user_input.lower().strip() in ("bye", "goodbye", "see you"):
            print("Chatbot: Goodbye!")
            break
        print("Chatbot:", get_reply(user_input))

if __name__ == "__main__":
    chat()
