# Entry 5
##### 4/19/26

#### Context
My partner and I have been using and practising with our tool [Godot](https://godotengine.org/). We decided to change our idea for our Freedom Project and instead of making a game where the character is in a museum, instead it's going to be a farming game. We both found some tutorials that will be useful in implementing ideas into our game. The [tutorial](https://www.youtube.com/watch?v=LOhfqjmasi0) that I used previously was very useful because I learned a lot of basic things that I can add into our game. I learned how to use Godot and I also learned a lot of the functions in the game engine. Right now, we have a very basic things set up, including me making a map and my partner creating multiple test maps, and the character in the game has the ability to move. 

Our mvp took a while to solidify because we couldn't decide on what to make for our project. We thought out a few ideas, such as making a nature simulation, but needing to do everything in 3d made us change our minds. We decided to change our idea to making a game that includes farming since we did a nature themed game last year with crops and animals. A decent chunk of what we did in Godot was building the background/map, which doesn't need any coding. All we need to do was to download some assets and put it on a sheet and place all the tiles down. It was a bit annoying because deleting the tiles is very slow and I have to click 1 by 1 (unless there is a shortcut I'm unaware of), and so if I make mistakes when building the map or if I dislike what I made, it is annoying to revert it. Some of the code we added are:
```
const SPEED = 150.0
const JUMP_VELOCITY = -300.0

	# Handle jump.
	if Input.is_action_just_pressed("ui_accept") and is_on_floor():
		velocity.y = JUMP_VELOCITY

	# Get the input direction and handle the movement/deceleration.
	var direction := Input.get_axis("ui_left", "ui_right")
	if direction:
		velocity.x = direction * SPEED
	else:
		velocity.x = move_toward(velocity.x, 0, SPEED)
```
Here is part of my code for my character's movement. What it does is when the player presses the arrow keys left, right, up, and down; their speed will go to 150 and the character gets to move in any direction at that speed and also if the player is standing on a floor, they can jump up. And there's a jump velocity setting to make sure the character falls back down.
```
extends Area2D
func _on_body_entered(body):
    if body.name == "Player":
        print("Pickup collected!")
        queue_free()
```
My partner added some code for the future for when we add collectables to the game. This code will allow the player to collect items. 

#### Engineering Design Process
We are at steps 5 & 6 for the EDP(Engineering design process), which is creating and testing. We did add code to our game and we also made some maps and use the tile blocks to edit and make things. We also made the camera follow the player sprite in Godot. For our beyond mvp, we want to add more features to this game. My partner did have some issues with putting the camera on the player and making it follow the sprite, but with a tutorial, we were able to do it. We do need more time and do a bit more collaboration and working together to help process this project. 

#### Skill
##### Communication
During this project, we practiced the skill communication a lot, we wanted to do this together so we wanted to make some time and work together. When we called each other, we discussed on what we should do to make our project work, and we talked a lot and decided together on what we should do for the project, what background should we use, what sprites should we use and not use in the game, etc. Though it was a bit difficult to maintain us communicating throughout our break, because we both had days where we are busy and we didn't have time at the beginning or middle of the break to call and talk to each other.

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
