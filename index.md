---
layout: default
---
# York Pirates!
## About This Website
This is the website for the York Pirates! game.
This game was originally made by Bass<sub>2</sub> (Team 14) for the Engineering 1 module group project at the University of York. For the second half of the assessment, Eleven Musketeers (Team 11) have picked it up to continue developing it.

Original game: [download](https://github.com/engteam14/yorkpirates/releases) 

Modified game's [GitHub repository](https://github.com/UOY-ENG1-Team-11/yorkpirates)

- [**Home**]() - This page will go over what York Pirates! is, how to play it, and provide information about how the code works.
- [**Team 14's GitHub**](https://github.com/engteam14/yorkpirates) - The old team's GitHub repository contains all the code for the project as of the end of assessment 1, as well as downloads.
- [**(Old) Deliverables**](/deliverables) - All the old project deliverables will be listed here.
- [**(NEW) Deliverables**](/deliverables2) - All the new project deliverables will be listed here.
- [**(Old) Plan**](/plan) - Information about how the project was planned throughout development is shown here.
- [**(Old) Use Case**](/usecase) - Shows our planned use case for the game.
- [**Files**](/files) - Any additional files are listed here.

![Game Logo](/media/Logo.gif)

## The Game
<hr/>
### Animated Title Screen
![Title Screen](/media/Title_Screen.gif)
<br/>
Application comes with a main screen, where you can enter a name of your choice, start the game, and view our wonderful title graphic!
<hr/>
### Dynamic Tutorial
![Tutorial](/media/Tutorial.gif)
<br/>
Our game begins with a tutorial to show even the least inventive player just how to get 100% out of York Pirates!
<hr/>
### Fluid Goal Indicators
![Indicators](/media/Indicators.gif)
<br/>
In addition to our seamless movement, the game contains indicators so that you're never lost in our wonderfully crafted map environment!
<hr/>
### Fast Paced Combat!
![Combat](/media/Combat.gif)
![Combat](/media/Combat2.gif)
<br/>
Engage in fierce and engaging combat against colleges that feature individually processed projectiles to keep you on your toes!
<hr/>
### Game Over...
![Game Over](/media/Game_Over.gif)
<br/>
No punches (or in this case cannonballs) were pulled during the making of this game, and player death is implemented and possible!
<hr/>
### Player Tasklist
![Tasks](/media/Tasks.gif)
<br/>
In addition to allowing inferior foes to join your ranks (complete with full image and palette swaps!), defeating colleges and other commendable tasks award you with well-earned loot!
<hr/>
### Game Win!
![Game Win](/media/Game_Win.gif)
<br/>
Once all the colleges are captured, return to your home college to win the game!

<hr/>

## The Code

### Scene2D.UI

We use LibGDX Sprite2D's UI system to allow User Interface and Heads Up Display (HUD) to be easily rendered and customised.

```java
// Make a table
Table table = new Table();
table.setBackground(skin.getDrawable("Background"));

// Create widgets
Image title = new Image(titleTexture);
ImageButton button = new ImageButton(skin, styleName: "Restart");

// Add widgets to table
table.add(title).expand();
table.row();
table.add(button).expand();
```
But that's not all...

![Debug Mode](/media/Debug.gif)
Featuring a UI debug mode! All at the flip of a boolean.

<hr/>

### ScreenAdapter

To make managing the project easy, we use LibGDX's ScreenAdapter. 
This package allows many screens for both gameplay and menus to be easily put together and organised as their own classes.
The easiest way to get the best project structure!

```java
public class ScreenName extends ScreenAdapter {
    
    public ScreenName() {
        // Initialise the screen
    }
    
    @Override
    public void render(float delta) {
        // Called every frame
        // Perform calculations
        // Render graphics
    }
    
    @Override
    public void dispose() {
        // Dispose of assets when done to improve performance
    }
}
```

<hr/>

### TiledMap
Using LibGDX's package for Tiled maps is the easiest way to rapidly produce gameplay levels.
The software [Tiled](https://www.mapeditor.org) can be used to produce levels, with easy to use wide-ranging functionality, it's the industry's best for a reason!
<br/><br/>![Tiled](/media/tiled.gif)
<br/><br/>Maps from Tiled can be easily imported into LibGDX, and we've even implemented our own collision system around it - ready out of the box!