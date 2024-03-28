# AI-assisted-Language-Learning
Créez une application d'apprentissage des langues alimentée par l'IA qui utilise des modèles de langage importants pour fournir un enseignement personnalisé et une pratique de la conversation.
import random

class AILanguageLearningApp:
    def __init__(self):
        self.languages = ["French", "Spanish", "German"]
        self.learning_preferences = ["grammar", "vocabulary", "conversation"]
        self.conversations = {
            "French": [
                {"q": "Comment vas-tu?", "a": "Je vais bien, merci."},
                {"q": "Quel est ton nom?", "a": "Mon nom est AI."},
            ],
            "Spanish": [
                {"q": "¿Cómo estás?", "a": "Estoy bien, gracias."},
                {"q": "¿Cuál es tu nombre?", "a": "Mi nombre es AI."},
            ],
            "German": [
                {"q": "Wie geht es dir?", "a": "Mir geht es gut, danke."},
                {"q": "Wie heißt du?", "a": "Mein Name ist AI."},
            ]
        }

    def start(self):
        print("Welcome to the AI-assisted Language Learning App!\n")
        self.user_language = input(f"Choose a language to learn ({', '.join(self.languages)}): ")
        self.user_preference = input(f"What would you like to focus on? ({', '.join(self.learning_preferences)}): ")
        print("\nStarting your personalized learning session...\n")
        self.run_session()

    def run_session(self):
        if self.user_preference == "conversation":
            print("Let's practice some conversation. I'll ask you something, and you try to respond!\n")
            for conv in self.conversations[self.user_language]:
                print(f"AI: {conv['q']}")
                user_response = input("You: ")
                print(f"AI: Normally, I'd say: '{conv['a']}'\n")
        else:
            print(f"Currently, the demo focuses on conversation practice. More features coming soon!")

app = AILanguageLearningApp()
app.start()
