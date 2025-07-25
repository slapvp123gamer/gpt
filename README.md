if not table.find({2753915549, 4442272183, 7449423635}, game.PlaceId) then return end
if getgenv().abacaxi_loaded then return end
getgenv().abacaxi_loaded = true

local gui = Instance.new("ScreenGui", game.CoreGui)
gui.Name = "AbacaxiHub"

local main = Instance.new("Frame", gui)
main.Size = UDim2.new(0, 300, 0, 200)
main.Position = UDim2.new(0.5, -150, 0.5, -100)
main.BackgroundColor3 = Color3.fromRGB(20, 20, 30)

local UICorner = Instance.new("UICorner", main)
UICorner.CornerRadius = UDim.new(0, 12)

local title = Instance.new("TextLabel", main)
title.Text = "🍍 Abacaxi Hub 🍍"
title.Size = UDim2.new(1, 0, 0, 40)
title.TextColor3 = Color3.fromRGB(255, 255, 0)
title.BackgroundTransparency = 1
title.Font = Enum.Font.FredokaOne
title.TextScaled = true

local btn = Instance.new("TextButton", main)
btn.Size = UDim2.new(0.8, 0, 0, 40)
btn.Position = UDim2.new(0.1, 0, 0.5, -20)
btn.Text = "Auto-Farm (em breve)"
btn.Font = Enum.Font.GothamBold
btn.TextScaled = true
btn.BackgroundColor3 = Color3.fromRGB(255, 200, 0)
btn.TextColor3 = Color3.new(0, 0, 0)
Instance.new("UICorner", btn)

btn.MouseButton1Click:Connect(function()
	btn.Text = "🍍 em construção 🍍"
end)
