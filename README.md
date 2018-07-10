# 3dJS (this project is outdated, check [Brew.js](https://github.com/XorTroll/Brew.js) for its new project)
- JS interpreter for 3DS, using duktape engine.
- You can load plain JS here, and you can use the elements below to access 3DS system's functions.

# Special variables and functions
- Modules / element collections:  
  - System (manages common system operarions):  
  `system.exitApp()` -> Closes 3dJS app, not just the code. This will return to Home menu or HBW launcher.  
  `system.isNew3DS()` -> Returns true if current console is a New 3DS model, otherwise false.  
  `system.getTime()` -> Returns a collection with time elements: `getTime().Hour`, `getTime().Minutes`, `getTime().Seconds`, `getTime().DayName`, `getTime().DayNumber`, `getTime().MonthName`, `getTime().MonthNumber` and `getTime().Year`.  
  `system.reboot()` -> Reboots the console.  
  `system.powerOff()` -> Turns the console off.  
  `system.getBattery()` -> Returns the aproximate battery level (0, 20, 40, 60, 80 or 100)  
  `system.isCharging()` -> Returns true if the console is being charged, otherwise false.  
  `system.launchApplet(Applet)` -> Opens an applet and waits till it is closed.
  - Console (manages printing to console in both screens):  
  `console.log(...)` -> Prints every argument to the console and then ends it with a line.  
  `console.read()` -> Opens the console keyboard and returns its text.  
  `console.setScreen(Screen)` -> Sets the screen where `console.log()` will print data.  
  `console.clear()` -> Clears the text at the selected screen.  
  - Screen (contains two variables refering to top and bottom screen):  
  `screen.Top` -> Represents the top screen.  
  `screen.Bottom` -> Represents the bottom screen.  
  - Input (manages reading and handling common input, like buttons or touch):  
  `input.None` -> No input is pressed.  
  `input.A` -> A button.  
  `input.B` -> B button.  
  `input.Select` -> Select button.  
  `input.Start` -> Start button.  
  `input.DRight` -> D-pad, right part.  
  `input.DLeft` -> D-pad, left part.  
  `input.DUp` -> D-pad, up part.  
  `input.DDown` -> D-pad, down part.  
  `input.R` -> R button.  
  `input.L` -> L button.  
  `input.X` -> X button.  
  `input.Y` -> Y button.  
  `input.ZL` -> ZL button.  
  `input.ZR` -> ZR button.  
  `input.Touch` -> Screen touched.  
  `input.CSRight` -> C-stick right part.  
  `input.CSLeft` -> C-stick left part.  
  `input.CSUp` -> C-stick up part.  
  `input.CSDown` -> C-stick down part.  
  `input.CPRight` -> Circle pad right part.  
  `input.CPLeft` -> Circle pad left part.  
  `input.CPUp` -> Circle pad up part.  
  `input.CPDown` -> Circle pad down part.  
  `input.checkUp()` -> Returns the input when it's pressed.  
  `input.checkDown()` -> Returns the input when it's released.  
  `input.checkHeld()` -> Returns which input is constantly pressed.  
  `input.isPressed()` -> Returns true if there's any input pressed.  
  `input.getTouch()` -> Returns the touch coords of the screen is touched: `getTouch().X`, `getTouch().Y`.  
  - Applet (contains some IDs of system applets as variables):  
  `applet.HomeMenu` -> Home menu applet.  
	`applet.AlternateMenu` -> Alternate home menu?  
	`applet.Camera` -> Camera applet.  
	`applet.FriendsList` -> Friends list applet.  
	`applet.GameNotes` -> Game notes applet.  
	`applet.WebBrowser` -> Internet Browser applet.  
	`applet.InstructionManual` -> Current app's manual?  
	`applet.Notifications` -> Notifications' applet.  
	`applet.Miiverse` -> Miiverse applet.  
	`applet.MiiversePosting` -> Miiverse applet, posting part.  
	`applet.AmiiboSettings` -> Ammibo settings' applet.  
	`applet.Application` -> Application?  
	`applet.eShop` -> eShop common applet.  
	`applet.SoftwareKeyboard` -> Internal keyboard applet.  
	`applet.MiiSelector` -> Mii selector applet.  
	`applet.PhotoSelector` -> Photo selector applet.  
	`applet.SoundSelector` -> Sound selector applet.  
	`applet.ErrorDisplay` -> Error display's applet.  
	`applet.eShopMint` -> eShop (MINT, downloader?) applet.  
	`applet.CirclePadCalibrator` -> CirclePad pro calibrator applet.  
	`applet.Notepad` -> Notepad applet.   
- You can use all of these constants and functions in JS code processd by 3dJS.
- IMPORTANT! Any issues you find, please tell me about them. Enjoy your scripting!
