"# UnityNotes" 
<11/11/2021> 
	- Scriptable object should be used When: 
		+ Multiple objects using a common configuration.
		+ The Object is unique and not a GameObject: if an object that is not a gameobject still need tobe configured within unity, it should not be a normal C# class.
		+ One Object changes its data at runtime. Then that multiple data should be configured somewhere ready for using.

	- Otherwise configuration should belong to the Gameobject.
		+ Configuration variables: are the variables tweaked in the inspector to define your object through its properties. For example, maxHealth.
		+ State variables: are the variables that completely determines your object's current state, and are the variables you need to save if your game supports saving. For example, currentHealth.
		+ Bookkeeping variables: are used for speed, convenience, or transitional states. They can always completely be determined from the state variables. For example, previousHealth.

==> Damn!!!! Scriptable object is yet another object, that can be instantiated just like the Prefab

	- Do it normally, no ScriptableObject Yet, until we need it. only for shared config data, which should not resist within a single gameobject