local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("TITLE", "Midnight")
local Tab = Window:NewTab("Batman")
    local Section = Tab:NewSection("Skill")
        Section:NewKeybind("Taser Punch", "KeybindInfo", Enum.KeyCode.Z, function()
	local args = {
        [1] = game:GetService("Players").LocalPlayer
        }
        game:GetService("ReplicatedStorage").Characters.TheBatman.Remotes.ElectricuteRemote:FireServer(unpack(args))
    end)
    Section:NewKeybind("Slam Counter", "KeybindInfo", Enum.KeyCode.X, function()
	local args = {
        [1] = game:GetService("Players").LocalPlayer
        }
        game:GetService("Players").LocalPlayer.Character.TheBatman.CounterActivate:FireServer(unpack(args))
    end)
    Section:NewKeybind("Mini-Explosive", "KeybindInfo", Enum.KeyCode.C, function()
	local args = {
        [1] = game:GetService("Players").LocalPlayer
        }
        game:GetService("ReplicatedStorage").Characters.TheBatman.Remotes.MiniExplosive:FireServer(unpack(args))
    end)
    Section:NewKeybind("Vengeance Finisher", "KeybindInfo", Enum.KeyCode.V, function()
	game:GetService("ReplicatedStorage").Characters.TheBatman.Remotes.VengeanceCombo:FireServer()
    end)
    Section:NewKeybind("Adrenaline", "KeybindInfo", Enum.KeyCode.E, function()
	local args = {
        [1] = game:GetService("Players").LocalPlayer
        }
        game:GetService("ReplicatedStorage").Characters.TheBatman.Remotes.AdShotRemote:FireServer(unpack(args))
    end)
local Tab = Window:NewTab("Cradit")
    local Section = Tab:NewSection("UI")
    Section:NewKeybind("Hide UI", "KeybindInfo", Enum.KeyCode.P, function()
	Library:ToggleUI()
end)
