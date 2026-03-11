# UiLibrary

UiLibrary is a simple Roblox UI library that allows developers to easily create windows, tabs, and UI components with a clean API.

---

# Installation

Load the library using `loadstring`.

```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/NeziaReal/UiLibrary/main/library.lua"))()
```

---

# Basic Example

```lua
local Library = loadstring(game:HttpGet("URL"))()

local Window = Library:CreateWindow({
    Name = "Example UI"
})

local Tab = Window:CreateTab("Main")

Tab:CreateButton({
    Name = "Print Hello",
    Callback = function()
        print("Hello")
    end
})
```

---

# API Documentation

## CreateWindow

Creates the main UI window.

```lua
local Window = Library:CreateWindow({
    Name = "Window Name"
})
```

### Options

| Property | Type | Description |
|--------|--------|--------|
| Name | string | Title of the UI window |

---

# Tabs

## CreateTab

Creates a new tab inside the window.

```lua
local Tab = Window:CreateTab("Main")
```

### Parameters

| Parameter | Type | Description |
|--------|--------|--------|
| Name | string | Name of the tab |

---

# Components

## Button

Creates a clickable button.

```lua
Tab:CreateButton({
    Name = "Button Name",
    Callback = function()
        print("Clicked")
    end
})
```

### Options

| Property | Type | Description |
|--------|--------|--------|
| Name | string | Button text |
| Callback | function | Function executed when clicked |

---

## Toggle

Creates a toggle switch.

```lua
Tab:CreateToggle({
    Name = "Enable Feature",
    Default = false,
    Callback = function(state)
        print(state)
    end
})
```

### Options

| Property | Type | Description |
|--------|--------|--------|
| Name | string | Toggle label |
| Default | boolean | Default state |
| Callback | function | Called when toggled |

---

## Slider

Creates a value slider.

```lua
Tab:CreateSlider({
    Name = "Speed",
    Min = 0,
    Max = 100,
    Default = 50,
    Callback = function(value)
        print(value)
    end
})
```

### Options

| Property | Type | Description |
|--------|--------|--------|
| Min | number | Minimum value |
| Max | number | Maximum value |
| Default | number | Starting value |
| Callback | function | Triggered when value changes |

---

## Dropdown

Creates a dropdown selector.

```lua
Tab:CreateDropdown({
    Name = "Select Option",
    Options = {"A","B","C"},
    Callback = function(option)
        print(option)
    end
})
```

### Options

| Property | Type | Description |
|--------|--------|--------|
| Options | table | List of selectable options |
| Callback | function | Runs when an option is selected |

---

## Label

Creates a text label.

```lua
Tab:CreateLabel("This is a label")
```

---

# Full Example

```lua
local Library = loadstring(game:HttpGet("URL"))()

local Window = Library:CreateWindow({
    Name = "Demo UI"
})

local Main = Window:CreateTab("Main")

Main:CreateButton({
    Name = "Test Button",
    Callback = function()
        print("Button clicked")
    end
})

Main:CreateToggle({
    Name = "Test Toggle",
    Default = false,
    Callback = function(state)
        print(state)
    end
})
```

---

# License

MIT License
