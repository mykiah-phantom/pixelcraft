# 🎮 PixelCraft - Game Launcher

A Pokémon-style game launcher hub where you can manage and play multiple games!

## Features

✨ **Arrow Key Navigation** - Use ← → arrow keys or A/D to switch between games  
🎯 **Play in New Window** - Click PLAY to open each game in its own window  
🎨 **Pokémon-Style UI** - Beautiful card-based interface inspired by Pokémon games  
📝 **Easy to Extend** - Simple comments show exactly how to add new games  

## Quick Start

1. Open `index.html` in your web browser
2. Use arrow keys (← →) or A/D keys to navigate games
3. Click **PLAY** to open the selected game in a new window
4. Click **Reset** to go back to the first game

## Adding New Games

### Step 1: Create Your Game File

Create a new HTML file in the `games/` folder:
```
games/your-game.html
```

### Step 2: Add to Game List

Open `index.html` and find the `games` array in the JavaScript section (it's clearly marked). Add a new game object:

```javascript
const games = [
    {
        name: "My Awesome Game",
        icon: "🎮",
        description: "This is my cool game!",
        url: "games/my-awesome-game.html"
    },
    // ... other games ...
];
```

### Parameters:
- **name**: Display name of your game
- **icon**: Emoji icon to show
- **description**: Brief description (1 line)
- **url**: Path to game file (local or URL)

## File Structure

```
pixelcraft/
├── index.html              (Main launcher - start here!)
├── README.md               (This file)
└── games/
    ├── pokemon-picker.html (Example game)
    ├── color-clicker.html  (Add your games here)
    └── snake.html          (Just create, add to index.html)
```

## Game Window Options

Games open in a new window with customizable size. Edit the `playGame()` function to adjust:

```javascript
window.open(game.url, '_blank', 'width=800,height=600');
```

Change `800x600` to your desired dimensions.

## Controls

| Key | Action |
|-----|--------|
| ← Arrow Left | Previous Game |
| → Arrow Right | Next Game |
| A | Previous Game |
| D | Next Game |
| Enter | Play Game |
| Click Game Card | (Future: select) |
| Click PLAY Button | Open Game |

## Tips

💡 Games should be self-contained HTML files  
💡 Use relative paths for local games, absolute URLs for online games  
💡 Each game opens in a new window independently  
💡 The launcher stays open when you play a game

## Example Game Structure

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Game</title>
</head>
<body>
    <h1>My Game</h1>
    <button onclick="window.close()">Close Game</button>
</body>
</html>
```

---

**Have fun creating games! 🚀**
