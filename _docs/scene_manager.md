****SceneManager****
____________
**Usage**:
	
	- You must update the scene manager every time you add a scene which you
	would like it to have access to
	
	- You will add the scene's alias and preload it in the first dictionary and
	add its alias and its path in the second dictionary
	
	- To switch scenes simply call switch_scenes("alias") or, alternatively,
	if the scene is large and you would like a loading screen you can call 
	load_scene("alias")
	
	- If you wish to additively load a scene, i.e. not remove the current scene,
	you may call the add_scene() method
	
	*Note:* You will likely want to remove this scene using queue_free() or a
	similar process as using switch_scene() or load_scene() will clear the
	entire tree

**Removal:**

	- This system can be safely removed, simply delete the autoload and make 
	sure all calls to its methods are removed
	
	*Note:* This makes the "loading_screen" scene obsolete, so it can be removed
	as well
	
	- These calls can be found in the "main_menu" scene and the "settings_menu"
	scene