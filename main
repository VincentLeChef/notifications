local TweenService = game:GetService("TweenService")

local a = Instance.new("ScreenGui")
a.Name = "?"
a.ResetOnSpawn = false
a.Parent = game:GetService("CoreGui")

local function text(text, s)
    local waitingtime = s or 3
    coroutine.wrap(function()
        local TextLabel = Instance.new("TextLabel")
        TextLabel.Parent = a
        TextLabel.AnchorPoint = Vector2.new(0.5, 0.5)
        TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        TextLabel.BorderSizePixel = 0
        TextLabel.Position = UDim2.new(0.5, 0, 0.800000012, 0)
        TextLabel.Size = UDim2.new(0, 0, 0, 30)
        TextLabel.Font = Enum.Font.SourceSansLight
        TextLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
        TextLabel.TextSize = 20.000
        for i = 1,#text + 1 do
            local v = game:GetService("TextService"):GetTextSize(text:sub(1, i), 20, Enum.Font.SourceSansLight, Vector2.new(9e9, 9e9))
            TextLabel.Text = text:sub(1, i)
            TweenService:Create(TextLabel, TweenInfo.new(0.01), {Size = UDim2.new(0, v.x + 30, 0, v.y + 10)}):Play()
            wait(0.03)
        end
        wait(waitingtime)
        TextLabel.Text = ""
        TweenService:Create(TextLabel, TweenInfo.new(0.2), {Size = UDim2.new(0,0,0,0)}):Play()
        wait(0.2)
        TextLabel:Destroy()
    end)()
end 

--text() is the command
