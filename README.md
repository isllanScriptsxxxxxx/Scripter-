# Scripter-
esse aqui e meu script e so testa ainda nao tem muitas funções eu ainda vou add ok

```lua
local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()

local Window = OrionLib:MakeWindow({Name = "Bot Hub", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})

 local Tab = Window:MakeTab({
	Name = "Tab User",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "UserYour"
})

 Tab:AddLabel("Libary User OrionLibary")
local localPlayer = game.Players.LocalPlayer
local playerName = localPlayer.Name
Tab:AddLabel("Player Name: " .. playerName)

Tab:AddLabel("This script was made by isllanjuanxxxx")

local Tab = Window:MakeTab({
	Name = "Tab Powers",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
 

  local function setSpeed(speed)
    if not tonumber(speed) then
        return
    end
    
    local localPlayer = game.Players.LocalPlayer
    local humanoid = localPlayer.Character and localPlayer.Character:FindFirstChildOfClass("Humanoid")
    if humanoid then
        humanoid.WalkSpeed = tonumber(speed)
    end
end

Tab:AddTextbox({
    Name = "Speed",
    Default = "16",
    TextDisappear = true,
    Callback = function(Value)
        setSpeed(Value)
    end	  
})

local function setJumpPower(jumpPower)
    if not tonumber(jumpPower) then
        return
    end
    
    local localPlayer = game.Players.LocalPlayer
    local humanoid = localPlayer.Character and localPlayer.Character:FindFirstChildOfClass("Humanoid")
    if humanoid then
        humanoid.JumpPower = tonumber(jumpPower)
    end
end

Tab:AddTextbox({
    Name = "Jump Power",
    Default = "50",
    TextDisappear = true,
    Callback = function(Value)
        setJumpPower(Value)
    end	  
})

local function setGravity(gravity)
    if not tonumber(gravity) then
        return
    end
    
    game.Workspace.Gravity = tonumber(gravity)
end

Tab:AddTextbox({
    Name = "Gravity",
    Default = "196.2",
    TextDisappear = true,
    Callback = function(Value)
        setGravity(Value)
    end	  
})
```
# Att-
toda vez que eu atualizar ele eu vou atualizar aqui também!
