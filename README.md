-- Verifica se é Blox Fruits
if not table.find({2753915549, 4442272183, 7449423635}, game.PlaceId) then
    return warn("Abacaxi Hub: Esse jogo não é Blox Fruits.")
end

-- Evita execução duplicada
if getgenv().abacaxi_already_loaded then return end
getgenv().abacaxi_already_loaded = true

local CoreGui = game:GetService("CoreGui")
local Players = game:GetService("Players")
local player = Players.LocalPlayer

-- Remove versão anterior da UI
pcall(function()
    CoreGui:FindFirstChild("AbacaxiHub"):Destroy()
end)

-- UI Principal
local gui = Instance.new("ScreenGui", CoreGui)
gui.Name = "AbacaxiHub"
gui.ResetOnSpawn = false

-- Fundo
local background = Instance.new("Frame", gui)
background.Size = UDim2.new(1, 0, 1, 0)
background.BackgroundColor3 = Color3.fromRGB(10, 10, 15)

-- Título
local title = Instance.new("TextLabel", background)
title.Text = "🍍 Abacaxi Hub 🍍"
title.Size = UDim2.new(1, 0, 0, 60)
title.Position = UDim2.new(0, 0, 0, 20)
title.BackgroundTransparency = 1
title.TextColor3 = Color3.fromRGB(255, 255, 0)
title.Font = Enum.Font.FredokaOne
title.TextScaled = true

-- Botão Auto-Farm (placeholder)
local btn = Instance.new("TextButton", background)
btn.Size = UDim2.new(0, 250, 0, 50)
btn.Position = UDim2.new(0.5, -125, 0.5, -25)
btn.BackgroundColor3 = Color3.fromRGB(255, 200, 0)
btn.TextColor3 = Color3.new(0, 0, 0)
btn.Font = Enum.Font.GothamBold
btn.Text = "Ativar Auto-Farm"
btn.TextScaled = true

-- Canto arredondado
local corner1 = Instance.new("UICorner", background)
corner1.CornerRadius = UDim.new(0, 12)
local corner2 = Instance.new("UICorner", btn)
corner2.CornerRadius = UDim.new(0, 12)

-- Clique no botão
btn.MouseButton1Click:Connect(function()
    print("Auto-Farm ainda não implementado")
    btn.Text = "Auto-Farm em breve 🍍"
end)

-- Efeito de gradiente
local gradient = Instance.new("UIGradient", background)
gradient.Color = ColorSequence.new({
    ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 165, 0)),
    ColorSequenceKeypoint.new(1, Color3.fromRGB(255, 255, 0))
})
gradient.Rotation = 45
