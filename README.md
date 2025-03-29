local players = game:GetService("Players")
local player = players.LocalPlayer
local teams = game:GetService("Teams")
local replicatedStorage = game:GetService("ReplicatedStorage")
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/PresidentZuyi/S/refs/heads/main/C"))()

MakeWindow({
    Hub = {
        Title = "Abuya Private Script Bye Faheem X QhalishÂ=>(¥)",
        Animation = "Enjoy!=="
    },
    Key = {
        KeySystem = false,
        Title = "Abuya Official Hub <  (¥)",
        Description = ">Private Script Rivals. BLR>=",
        KeyLink = "blob:https://paste.sh/81e1f9a8-eb32-4fbf-906d-96edcad9c53e",
        Keys = {"lagikaujauh", "Abuya", "19226", "1", "private1"},
        Notifi = {
            Notifications = true,
            CorrectKey = "Correct",
            Incorrectkey = "False=<",
            CopyKeyLink = "Copied Link"
        }
    }
})

MinimizeButton({
    Image = "rbxassetid://3845386987",
    Size = {40, 40},
    Color = Color3.fromRGB(10, 10, 10),
    Corner = true,
    Stroke = true,
    StrokeColor = Color3.fromHSV(0.5, 1, 1)
})

MakeNotifi({
    Title = "Executed!",
    Text = "Boom!",
    Time = 5
})

local Main = MakeTab({Name = "No cooldown"})

AddButton(Main, {
    Name = "¥ No Ability Cooldownv1",
    Callback = function()
        local AbilityController = require(game:GetService("ReplicatedStorage").Controllers.AbilityController)
        local OriginalAbilityCooldown

        OriginalAbilityCooldown = hookfunction(AbilityController.AbilityCooldown, function(Self)
            return
        end)

        game:GetService("StarterGui"):SetCore("SendNotification", {
            Title = "Join Abuya Hub For Updates!",
            Text = "No Cooldown Script Completed",
            Button1 = "W Faheem!",
            Button2 = "W Qhalish!",
            Duration = 5
        })
    end
})

local Main = MakeTab({Name = "STYLE AND FLOW"})

local sectionStyle = AddSection(Main, {"Styles ( Most of them work with skills sometimes it's false)"})

local function set_style(desired_style)
    if player:FindFirstChild("PlayerStats") then
        local playerStats = player.PlayerStats
        if playerStats:FindFirstChild("Style") then
            playerStats.Style.Value = desired_style
        end
    end
end

local function set_flow(desired_flow)
    if player:FindFirstChild("PlayerStats") then
        local playerStats = player.PlayerStats
        if playerStats:FindFirstChild("Flow") then
            playerStats.Flow.Value = desired_flow
        end
    end
end

local styleId

local StyleTextBox = AddTextBox(Main, {
    Name = "Style Name",
    Default = "",
    TextDisappear = false,
    PlaceholderText = "PUT NAME",
    ClearText = true,
    Callback = function(value)
        styleId = value
    end
})

AddButton(Main, {
    Name = "GET THE STYLE",
    Description = "DONT SPAM! Really don't space after you type example: Kurona()no space.",
    Callback = function()
        if styleId and styleId ~= "" then
            set_style(styleId)
            MakeNotifi({
                Title = "SUCCESS",
                Text = " by W Faheem",
                Time = 5
            })
        else
            MakeNotifi({
                Title = "WRONG PLS BE CAREFULLY WHEN TYPING NO SPACE",
                Text = "By W Qhalish",
                Time = 5
            })
        end
    end
})

local sectionFlow = AddSection(Main, {"Flows"})

local flow_name

local FlowTextBox = AddTextBox(Main, {
    Name = "Flow Name",
    Default = "",
    TextDisappear = false,
    PlaceholderText = "PUT NAME",
    ClearText = true,
    Callback = function(value)
        flow_name = value
    end
})

AddButton(Main, {
    Name = "GET THE FLOW",
    Description = "DONT SPAM! May bug.",
    Callback = function()
        if flow_name and flow_name ~= "" then
            set_flow(flow_name)
            MakeNotifi({
                Title = "SUCCESS",
                Text = "By W Faheem",
                Time = 5
            })
        else
            MakeNotifi({
                Title = "WRONG PLS BE CAREFULLY WHEN TYPE.",
                Text = "By W Qhalish",
                Time = 5
            })
        end
    end
})

local sectionFlow2 = AddSection(Main, {"Flows Function"})

local localPlayer = game:GetService("Players").LocalPlayer
