-- Create a ScreenGui
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "LargeTextGui"
screenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

-- Create a TextLabel
local textLabel = Instance.new("TextLabel")
textLabel.Name = "LargeTextLabel"
textLabel.Parent = screenGui
textLabel.Text = "ur not getting the fucking script dumb nigger" -- Change this to your desired text
textLabel.Size = UDim2.new(0.8, 0, 0.2, 0) -- Adjust size
textLabel.Position = UDim2.new(0.1, 0, 0.4, 0) -- Center the text
textLabel.BackgroundTransparency = 1 -- Make the background transparent
textLabel.TextColor3 = Color3.new(1, 1, 1) -- White text color
textLabel.TextScaled = true -- Scale text to fit the label
textLabel.Font = Enum.Font.SourceSansBold -- Choose font style
