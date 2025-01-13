-- Replace 'YOUR_ANIMATION_ID' with your actual animation asset ID.
local ANIMATION_ID = "507771955"

-- Get the player's character and humanoid.
local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")

-- Load the animation.
local animation = Instance.new("Animation")
animation.AnimationId = "rbxassetid://" .. ANIMATION_ID
local animationTrack = humanoid:LoadAnimation(animation)

-- Function to play the animation when 'E' is pressed.
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

-- Connect the InputBegan event.
game:GetService("UserInputService").InputBegan:Connect(onInputBegan)
