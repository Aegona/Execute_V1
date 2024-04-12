

local Execute_ui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local TextBox = Instance.new("TextBox")
local UIAspectRatioConstraint = Instance.new("UIAspectRatioConstraint")
local UITextSizeConstraint = Instance.new("UITextSizeConstraint")
local TextButton = Instance.new("TextButton")
local UICorner_2 = Instance.new("UICorner")
local UIAspectRatioConstraint_2 = Instance.new("UIAspectRatioConstraint")
local UITextSizeConstraint_2 = Instance.new("UITextSizeConstraint")
local UIAspectRatioConstraint_3 = Instance.new("UIAspectRatioConstraint")
local Toggle = Instance.new("TextButton")
local UICorner_3 = Instance.new("UICorner")
local UIGradient = Instance.new("UIGradient")
local UIAspectRatioConstraint_4 = Instance.new("UIAspectRatioConstraint")
local UITextSizeConstraint_3 = Instance.new("UITextSizeConstraint")

--Properties:

Execute_ui.Name = "Execute_ui"
Execute_ui.Parent = game.CoreGui
Execute_ui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Frame.Parent = Execute_ui
Frame.BackgroundColor3 = Color3.fromRGB(62, 62, 62)
Frame.BorderColor3 = Color3.fromRGB(0, 0, 0)
Frame.BorderSizePixel = 0
Frame.Position = UDim2.new(0.371995807, 0, 0.315789461, 0)
Frame.Size = UDim2.new(0.255485892, 0, 0.368421048, 0)

UICorner.Parent = Frame

TextBox.Parent = Frame
TextBox.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
TextBox.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextBox.BorderSizePixel = 0
TextBox.Position = UDim2.new(0.0265848674, 0, 0.0612244904, 0)
TextBox.Size = UDim2.new(0.946830273, 0, 0.588435352, 0)
TextBox.Font = Enum.Font.SourceSans
TextBox.Text = ""
TextBox.TextColor3 = Color3.fromRGB(255, 255, 255)
TextBox.TextScaled = true
TextBox.TextSize = 14.000
TextBox.TextWrapped = true
TextBox.TextXAlignment = Enum.TextXAlignment.Left
TextBox.TextYAlignment = Enum.TextYAlignment.Top

UIAspectRatioConstraint.Parent = TextBox
UIAspectRatioConstraint.AspectRatio = 2.676

UITextSizeConstraint.Parent = TextBox
UITextSizeConstraint.MaxTextSize = 14

TextButton.Parent = Frame
TextButton.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextButton.BorderSizePixel = 0
TextButton.Position = UDim2.new(0.0265848674, 0, 0.724489808, 0)
TextButton.Size = UDim2.new(0.946830273, 0, 0.170068026, 0)
TextButton.Font = Enum.Font.Unknown
TextButton.Text = "EXECUTE"
TextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton.TextScaled = true
TextButton.TextSize = 14.000
TextButton.TextWrapped = true

UICorner_2.Parent = TextButton

UIAspectRatioConstraint_2.Parent = TextButton
UIAspectRatioConstraint_2.AspectRatio = 9.260

UITextSizeConstraint_2.Parent = TextButton
UITextSizeConstraint_2.MaxTextSize = 50

UIAspectRatioConstraint_3.Parent = Frame
UIAspectRatioConstraint_3.AspectRatio = 1.663

Toggle.Name = "Toggle"
Toggle.Parent = Execute_ui
Toggle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Toggle.BorderColor3 = Color3.fromRGB(0, 0, 0)
Toggle.BorderSizePixel = 0
Toggle.Position = UDim2.new(0.135841176, 0, 0.16165413, 0)
Toggle.Size = UDim2.new(0.0433646813, 0, 0.106516294, 0)
Toggle.Font = Enum.Font.Unknown
Toggle.Text = "Toggle"
Toggle.TextColor3 = Color3.fromRGB(0, 0, 0)
Toggle.TextScaled = true
Toggle.TextSize = 14.000
Toggle.TextWrapped = true

UICorner_3.CornerRadius = UDim.new(0, 80)
UICorner_3.Parent = Toggle

UIGradient.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(131, 131, 131)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))}
UIGradient.Rotation = 105
UIGradient.Parent = Toggle

UIAspectRatioConstraint_4.Parent = Toggle
UIAspectRatioConstraint_4.AspectRatio = 0.976

UITextSizeConstraint_3.Parent = Toggle
UITextSizeConstraint_3.MaxTextSize = 35

-- Scripts:

local function UQBW_fake_script() -- TextButton.LocalScript 
	local script = Instance.new('LocalScript', TextButton)

	
	
	script.Parent.MouseButton1Click:Connect(function()
		local TextBox = script.Parent.Parent.TextBox
		local scriptText = TextBox.Text
		local success, result = pcall(loadstring(scriptText))
	
		if success then
			print("Script executed successfully")
			--[[
			game.StarterGui:SetCore("SendNotification", {
				Title = "Script executed successfully";
				Text = "Script Runing...";
				Icon = "rbxassetid://12900311398";
			})
			--]]
		else
			warn("Error executing script:", result)
			--[[
			game.StarterGui:SetCore("SendNotification", {
				Title = "Error executing script";
				Text = result;
				Icon = "rbxassetid://2592670412";
			})
			--]]
		end
	end)
	
end
coroutine.wrap(UQBW_fake_script)()
local function USTEW_fake_script() -- Frame.LocalScript 
	local script = Instance.new('LocalScript', Frame)

	frem = script.Parent.Parent.Frame
	frem.Draggable = true
	frem.Active = true
	frem.Selectable = true
end
coroutine.wrap(USTEW_fake_script)()
local function DKFMQHR_fake_script() -- Toggle.LocalScript 
	local script = Instance.new('LocalScript', Toggle)

	frem = script.Parent
	frem.Draggable = true
	frem.Active = true
	frem.Selectable = true
end
coroutine.wrap(DKFMQHR_fake_script)()
local function QMGBY_fake_script() -- Toggle.LocalScript 
	local script = Instance.new('LocalScript', Toggle)

	script.Parent.MouseButton1Click:Connect(function()
		if script.Parent.Parent.Frame.Visible == true then
			script.Parent.Parent.Frame.Visible = false
		elseif script.Parent.Parent.Frame.Visible == false then
			script.Parent.Parent.Frame.Visible = true
		else
			return
		end
	end)
end
coroutine.wrap(QMGBY_fake_script)()
