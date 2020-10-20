# Object Following Mouse

## 20/10/2020

Hello! By the end of this tutorial, you should have an object that will follow your mouse in game.

---

1. Once your project is open, drag in the sprite you wish to use into the assets folder.

When this is in, edit it however you wish.

---

2. After this, click on the object then add conponent. Add a script to the object and name it FollowMouse.

The script will also hide the cursor in game.

---

3. Once the script is open, delete void update and replace it with the following:

public void Update()

    {
        
    }
    
---

4. Now look back up to void Start. Here is where the dissapearing cursor script will go. Write up the following in void Start:

        Cursor.visible = false;

This simple line grabs the cursor, checks its visibility and sets it to false. Turning it off.

---

5. Now onto the object following part. This is two simple lines in the newly made public void Update section. Write up the following:

        Vector2 cursorPos = Camera.main.ScreenToWorldPoint(Input.mousePosition);
        transform.position = new Vector2(cursorPos.x, cursorPos.y);







