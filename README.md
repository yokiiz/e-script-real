local ANIMATION_ID = "507771955"

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")

local animation = Instance.new("Animation")
animation.AnimationId = "rbxassetid://" .. ANIMATION_ID
local animationTrack = humanoid:LoadAnimation(animation)

local function onInputBegan(input, gameProcessed)
    if gameProcessed then return end

    if input.UserInputType == Enum.UserInputType.Keyboard and input.KeyCode == Enum.KeyCode.E then
        if animationTrack.IsPlaying then
            animationTrack:Stop() -- Stop the animation if it's already playing.
        else
            animationTrack:Play() -- Play the animation.
        end
    end
end

game:GetService("UserInputService").InputBegan:Connect(onInputBegan)
