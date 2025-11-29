# This is a rework of https://github.com/memejames/elerium-v2-ui-library made by me (Henne)

Loadstring
```lua
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/imhenne187/SilenceElerium/refs/heads/main/src/SilenceEleriumLibrary.luau", true))()
```

Create Window Here:
```lua
local window = library:AddWindow("NameGui", {
	title_bar = {Color3.fromRGB(180, 0, 0), Color3.fromRGB(115, 0, 0), Color3.fromRGB(50, 0, 0)}, -- Title Bar Gradient (1-3 Colors)
	title_bar_transparency = 0.2, -- Title Bar transparency (0-1 with 1 being fully transparent)
	background = {Color3.fromRGB(0, 0, 0), Color3.fromRGB(34, 0, 0), Color3.fromRGB(68, 0, 0)}, -- (Background Gradient 1-3 Colors)
	background_transparency = 0.1, -- Background transparency (0-1 with 1 being fully transparent)
	main_color = Color3.fromRGB(255, 0, 0), -- Main Color for some Elements like Particles
	min_size = Vector2.new(400, 300), -- Size of the Window (vertically, horizontally)
	can_resize = true -- resizable (PC exclusive)
})
```
AddLabel:
```lua
features:AddLabel("Hello World!")
```

AddTab:
```lua
local tab1 = window:AddTab("Name") -- Name of the Tab
tab1:Show() -- Shows the tab first when executing
```
AddButton:
```lua
tab1:AddButton("Name",function()
	-- Code here
end)
```
AddToggle:
```lua
local switch1 = tab1:AddSwitch("name", function(bool)
	 -- toggle_god_mode(bool)
end)
switch1:Set(true) -- not needed (its set to false on default)
```
AddTextBox:
```lua
local textbox1 = tab1:AddTextBox("Name", function(text)
    print(text)
end) -- Text stays as placeholder
-- or
local textbox2 = tab1:AddTextBox("Name", function(text)
    print(text)
end, {clear = true}) -- Text will be cleared in the Textbox
```

AddDropdown:
```lua
local dropdown1 = tab1:AddDropdown("select", function(text)
	if text == "Mars" then  -- Code
		print("o")
	elseif text == "Earth" then
	print("k")
	elseif text == "Iridocyclitis" then
	print("Weeeee")
	end
end)
local mars = dropdown:Add("Mars")  -- Options 
local earth = dropdown:Add("Earth")
local not_a_planet = dropdown:Add("Iridocyclitis")
```



```

Credit to Chinawasspyingonusa
