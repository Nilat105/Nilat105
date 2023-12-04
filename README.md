- 👋 Hi, I’m @Nilat105
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Nilat105/Nilat105 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
from kivy.app import App
from kivy.uix.gridlayout import GridLayout
from kivy.uix.button import Button

class TicTacToeGame(GridLayout):
    def __init__(self, **kwargs):
        super(TicTacToeGame, self).__init__(**kwargs)
        self.cols = 3  # 3x3 grid
        self.buttons = [[Button() for _ in range(3)] for _ in range(3)]

        for row in self.buttons:
            for button in row:
                button.bind(on_press=self.on_button_press)
                self.add_widget(button)

    def on_button_press(self, instance):
        # Handle button press event
        pass  # Add your game logic here

class TicTacToeApp(App):
    def build(self):
        return TicTacToeGame()

if __name__ == '__main__':
    TicTacToeApp().run()
