local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("كلزق", "GrapeTheme")
local Tab = Window:NewTab("Main ")
local Section = Tab:NewSection("شاليه محمد ")

Section:NewButton("شغل هاذا اول ", "", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/H20CalibreYT/SystemBroken/main/script"))()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source"))()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/VR7ss/OMK/refs/heads/main/VR7-ON-TOP"))()
end)

Section:NewButton("شغل هاذا بعده", "", function()
    loadstring(game:HttpGet("https://gist.githubusercontent.com/amroffaads/54277157b77455d610973ec3756a22aa/raw/28fea5aa42ed1e58b999707fc08aacf61945d91e/1st"))()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/SnoobG/Lua-Script-s/refs/heads/main/Tvon"))()
end)

Section:NewButton("Desync x", "", function()
    local P1000ToggleKey = "x" -- Change that to whatever keybind: "t"


--[[

	hue hue hue

	hue hue hue
	
	hue hue hue
	
	hue hue hue


--]]


--// Services
checkcaller = checkcaller
newcclosure = newcclosure
hookmetamethod = hookmetamethod

local PastedSources = false
local BruhXD = game:GetService("RunService")
local LocalPlayer = game:GetService("Players").LocalPlayer
local Bullshit = LocalPlayer:GetMouse()


--// Toggles
Bullshit.KeyDown:Connect(function(SayNoToOblivity)
	if SayNoToOblivity == string.lower(P1000ToggleKey) then
		pcall(function()
			if PastedSources == false then
				PastedSources = true
				print("Enabled P1000")
			elseif PastedSources == true then
				PastedSources = false
				print("Disabled P1000")
			end
		end)
	end
end)

Bullshit.KeyDown:Connect(function(SayNoToOblivity)
	if SayNoToOblivity == ("=") then
		game:GetService("TeleportService"):Teleport(game.PlaceId, LocalPlayer) 
	end
end)


--// Desync_Source
function RandomNumberRange(a)
	return math.random(-a * 0, a * 0) / 0
end

function RandomVectorRange(a, b, c)
	return Vector3.new(RandomNumberRange(a), RandomNumberRange(b), RandomNumberRange(c))
end


local DesyncTypes = {}
BruhXD.Heartbeat:Connect(function()
	if PastedSources == true then
		DesyncTypes[1] = LocalPlayer.Character.HumanoidRootPart.CFrame
		DesyncTypes[2] = LocalPlayer.Character.HumanoidRootPart.AssemblyLinearVelocity

		local SpoofThis = LocalPlayer.Character.HumanoidRootPart.CFrame

		SpoofThis = SpoofThis * CFrame.new(Vector3.new(0, 0, 0))
		SpoofThis = SpoofThis * CFrame.Angles(math.rad(RandomNumberRange(0.1)), math.rad(RandomNumberRange(0.1)), math.rad(RandomNumberRange(0.1)))

		LocalPlayer.Character.HumanoidRootPart.CFrame = SpoofThis

		LocalPlayer.Character.HumanoidRootPart.AssemblyLinearVelocity = Vector3.new(1, 1, 1) * 16384

		BruhXD.RenderStepped:Wait()

		LocalPlayer.Character.HumanoidRootPart.CFrame = DesyncTypes[1]
		LocalPlayer.Character.HumanoidRootPart.AssemblyLinearVelocity = DesyncTypes[2]
	end
end)


--// Hook_CFrame
local XDDDDDD = nil
XDDDDDD = hookmetamethod(game, "__index", newcclosure(function(self, key)
	if PastedSources == true then
		if not checkcaller() then
			if key == "CFrame" and PastedSources == true and LocalPlayer.Character and LocalPlayer.Character:FindFirstChild("HumanoidRootPart") and LocalPlayer.Character:FindFirstChild("Humanoid") and LocalPlayer.Character:FindFirstChild("Humanoid").Health > 0 then
				if self == LocalPlayer.Character.HumanoidRootPart then
					return DesyncTypes[1] or CFrame.new()
				elseif self == LocalPlayer.Character.Head then
					return DesyncTypes[1] and DesyncTypes[1] + Vector3.new(0, LocalPlayer.Character.HumanoidRootPart.Size / 2 + 0.5, 0) or CFrame.new()
				end
			end
		end
	end
	return XDDDDDD(self, key)
end))
end)

Section:NewButton("Desync auto", "", function()
    getgenv().VelocityChanger = true
getgenv().Velocity = Vector3.new(2e9,2e9,2e9)

local Players     = game:GetService("Players")
local RunService  = game:GetService("RunService")
local LocalPlayer = Players.LocalPlayer
local Character   = LocalPlayer.Character
local RootPart    = Character:FindFirstChild("HumanoidRootPart")
local Heartbeat, RStepped, Stepped = RunService.Heartbeat, RunService.RenderStepped, RunService.Stepped

LocalPlayer.CharacterAdded:Connect(function(NewCharacter)
   Character = NewCharacter
end)

local RVelocity, YVelocity = nil, 0.1

while true do
   if VelocityChanger then
       if (not RootPart) or (not RootPart.Parent) or (not RootPart.Parent.Parent) then
           RootPart = Character:FindFirstChild("HumanoidRootPart")
       else
           RVelocity = RootPart.Velocity
           RootPart.Velocity = type(Velocity) == "vector" and Velocity or Velocity(RVelocity)
           RStepped:wait()
           RootPart.Velocity = RVelocity
       end
   end
   Heartbeat:wait()
end
	end)

    Section:NewButton("anti Bang", "", function()
        local lib = loadstring(game:HttpGet("https://raw.githubusercontent.com/m1kp0/libraries/refs/heads/main/m1kpe0_lime"))()
local wind = lib:Window("anti bang")

wind:Button("kill banger", function()
    local plr = game.Players.LocalPlayer
    local hrp = plr.Character.HumanoidRootPart
    local old_cframe = hrp.CFrame
    workspace.FallenPartsDestroyHeight = -10000
    hrp.CFrame = CFrame.new(0, -1000, 0)
    task.wait(1)
    hrp.CFrame = old_cframe
    workspace.FallenPartsDestroyHeight = -100
end)
end)

local Tab = Window:NewTab("oThers")
local Section = Tab:NewSection("Other Games")

Section:NewButton("Fling All (Wont Stop!!!) ", "", function()
    --actually for doll house but, its the same one the prison skids use

wait() if not game:IsLoaded() then game.Loaded:Wait() end

local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer
local rservice = game:GetService("RunService")

coroutine.resume(coroutine.create(function() while wait() do pcall(function() for _,z in next, Players:GetPlayers() do if z ~= LocalPlayer then for _,v in next, z.Backpack:GetDescendants() do if v:IsA'Sound' then v.TimePosition = nil end end end end end) end end)) 
coroutine.resume(coroutine.create(function() while wait() do pcall(function() for _,z in next, Players:GetPlayers() do if z ~= LocalPlayer then if z.Character and z.Character:FindFirstChildOfClass("Tool") then for _,v in next, z.Character:GetDescendants() do if v:IsA'Sound' then v.TimePosition = nil end end end end end end) end end))

local function SkidFling(TargetPlayer)
    local Character = LocalPlayer.Character
    local Humanoid = Character:FindFirstChildOfClass("Humanoid")
    local RootPart = Humanoid.RootPart
    
    local TCharacter = TargetPlayer.Character
    local THumanoid
    local TRootPart
    local THead
    local Accessory
    local Handle
    
    if TCharacter:FindFirstChildOfClass("Humanoid") then
        THumanoid = TCharacter:FindFirstChildOfClass("Humanoid")
    end
    if THumanoid and THumanoid.RootPart then
        TRootPart = THumanoid.RootPart
    end
    if TCharacter:FindFirstChild("Head") then
        THead = TCharacter.Head
    end
    if TCharacter:FindFirstChildOfClass("Accessory") then
        Accessory = TCharacter:FindFirstChildOfClass("Accessory")
    end
    if Accessoy and Accessory:FindFirstChild("Handle") then
        Handle = Accessory.Handle
    end
    
    if Character and Humanoid and RootPart then
        if THead then
            workspace.CurrentCamera.CameraSubject = THead
        elseif not THead and Handle then
            workspace.CurrentCamera.CameraSubject = Handle
        else
            workspace.CurrentCamera.CameraSubject = THumanoid
        end
        if not TCharacter:FindFirstChildWhichIsA("BasePart") then
            return
        end
        local function FPos(BasePart,Pos,Ang)
            RootPart.CFrame = CFrame.new(BasePart.Position) * Pos * Ang
            RootPart.Velocity = Vector3.new(9e8,9e8,9e8)
            RootPart.RotVelocity = Vector3.new(9e8,9e8,9e8)
        end
        local function SFBasePart(BasePart)
            local TimeToWait = 1
            local Time = tick()
            local Angle = 0
            
            repeat
                if RootPart and THumanoid then
                    if BasePart.Velocity.Magnitude < 30 then
                        Angle = Angle + 10
                        FPos(BasePart,CFrame.new(0,1.5,0) + THumanoid.MoveDirection * BasePart.Velocity.Magnitude / 5,CFrame.Angles(math.rad(Angle),0,0))
                        game:GetService("RunService").Heartbeat:wait()

                        FPos(BasePart,CFrame.new(0,1.5,0) + THumanoid.MoveDirection * BasePart.Velocity.Magnitude / 1.25,CFrame.Angles(math.rad(Angle),0,0))
                        game:GetService("RunService").Heartbeat:wait()

                        FPos(BasePart,CFrame.new(0,-1.5,0) + THumanoid.MoveDirection * BasePart.Velocity.Magnitude / 1.25,CFrame.Angles(math.rad(Angle),0,0))
                        game:GetService("RunService").Heartbeat:wait()
                        
                    else
                        FPos(BasePart,CFrame.new(0,-1.5,0),CFrame.Angles(math.rad(-30),0,0))
                        game:GetService("RunService").Heartbeat:wait()

                    end
                else
                    break
                end
            until BasePart.Velocity.Magnitude > 1000 or BasePart.Parent ~= TargetPlayer.Character or TargetPlayer.Parent ~= Players or not TargetPlayer.Character == TCharacter or THumanoid.Sit or Humanoid.Health <= 0 or tick() > Time + TimeToWait
        end
        workspace.FallenPartsDestroyHeight = 0/0
        local BV = Instance.new("BodyVelocity")
        BV.Parent = RootPart
        BV.Velocity = Vector3.new(9e9,9e9,9e9)
        BV.MaxForce = Vector3.new(1/0, 1/0, 1/0)
        if TRootPart and THead then
            if (TRootPart.CFrame.p - THead.CFrame.p).Magnitude > 5 then
                SFBasePart(THead)
            else
                SFBasePart(TRootPart)
            end
        elseif TRootPart and not THead then
            SFBasePart(TRootPart)
        elseif not TRootPart and THead then
            SFBasePart(THead)
        elseif not TRootPart and not THead and Accessory and Handle then
            SFBasePart(Handle)
        else
        end
        BV:Destroy()
        for _,x in next, Character:GetDescendants() do
            if x:IsA("BasePart") then
                x.Velocity,x.RotVelocity = Vector3.new(),Vector3.new()
            end
        end
        Humanoid:ChangeState("GettingUp")
        workspace.CurrentCamera.CameraSubject = Humanoid
    end
end

rservice.Stepped:Connect(function()
    if LocalPlayer.Character and LocalPlayer.Character:FindFirstChildOfClass("Humanoid") then
        if LocalPlayer.Character:FindFirstChildOfClass("Humanoid").Sit == true then
            LocalPlayer.Character:FindFirstChildOfClass("Humanoid"):ChangeState("Jumping")
        end
        for _,z in next, LocalPlayer.Character:GetChildren() do if z:IsA'BasePart' then z.CanCollide = false end end
    end
end)
coroutine.resume(coroutine.create(function()
    while wait() do
        pcall(function()
            for _,z in pairs(Players:GetPlayers()) do
                if z ~= LocalPlayer then
                    if LocalPlayer.Character and LocalPlayer.Character:FindFirstChildOfClass("Humanoid") and z and z.Character and z.Character:FindFirstChildOfClass("Humanoid").Sit == false then
                        SkidFling(z)
                        wait(0)
                    end
                end
            end
        end)
    end
end))
end)

Section:NewButton("Executer Any Script) ", "", function()
    -- Crear la GUI y los elementos principales
local ScreenGui = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local ExecuteButton = Instance.new("TextButton")
local ScriptBox = Instance.new("TextBox")
local CloseButton = Instance.new("TextButton")
local TitleLabel = Instance.new("TextLabel")
local UICorner = Instance.new("UICorner")
local UIStroke = Instance.new("UIStroke")
local TweenService = game:GetService("TweenService")

-- Propiedades de ScreenGui
ScreenGui.Name = "FancyExecutor"
ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ResetOnSpawn = false

-- Propiedades iniciales de MainFrame (pequeño para la animación)
MainFrame.Name = "MainFrame"
MainFrame.Parent = ScreenGui
MainFrame.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
MainFrame.Size = UDim2.new(0, 0, 0, 0)
MainFrame.Position = UDim2.new(0.5, 0, 0.5, 0) -- Centramos inicialmente
MainFrame.AnchorPoint = Vector2.new(0.5, 0.5)
MainFrame.ClipsDescendants = true
MainFrame.Active = true
MainFrame.Draggable = true

-- Agregar bordes redondeados al MainFrame
UICorner.Parent = MainFrame
UICorner.CornerRadius = UDim.new(0, 20)

-- Agregar un trazo al MainFrame
UIStroke.Parent = MainFrame
UIStroke.Thickness = 2
UIStroke.Color = Color3.fromRGB(105, 105, 105)

-- Propiedades de TitleLabel
TitleLabel.Name = "TitleLabel"
TitleLabel.Parent = MainFrame
TitleLabel.BackgroundTransparency = 1
TitleLabel.Position = UDim2.new(0.05, 0, 0.05, 0)
TitleLabel.Size = UDim2.new(0.9, 0, 0.1, 0)
TitleLabel.Font = Enum.Font.GothamBold
TitleLabel.Text = "ITz_48-sultan"
TitleLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TitleLabel.TextSize = 24
TitleLabel.TextWrapped = true

-- Propiedades de ScriptBox
ScriptBox.Name = "ScriptBox"
ScriptBox.Parent = MainFrame
ScriptBox.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
ScriptBox.Position = UDim2.new(0.05, 0, 0.2, 0)
ScriptBox.Size = UDim2.new(0.9, 0, 0.6, 0)
ScriptBox.Font = Enum.Font.Code
ScriptBox.Text = "حط سكربتك هنا :)"
ScriptBox.TextColor3 = Color3.fromRGB(200, 200, 200)
ScriptBox.TextSize = 14
ScriptBox.TextWrapped = true
ScriptBox.ClearTextOnFocus = true
ScriptBox.TextXAlignment = Enum.TextXAlignment.Left
ScriptBox.TextYAlignment = Enum.TextYAlignment.Top

-- Agregar bordes redondeados al ScriptBox
local ScriptBoxCorner = Instance.new("UICorner", ScriptBox)
ScriptBoxCorner.CornerRadius = UDim.new(0, 20)

-- Propiedades de ExecuteButton
ExecuteButton.Name = "ExecuteButton"
ExecuteButton.Parent = MainFrame
ExecuteButton.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
ExecuteButton.Position = UDim2.new(0.3, 0, 0.85, 0)
ExecuteButton.Size = UDim2.new(0.4, 0, 0.1, 0)
ExecuteButton.Font = Enum.Font.GothamBold
ExecuteButton.Text = "تشغيل"
ExecuteButton.TextColor3 = Color3.fromRGB(255, 255, 255)
ExecuteButton.TextSize = 16

-- Agregar bordes redondeados al ExecuteButton
local ExecuteButtonCorner = Instance.new("UICorner", ExecuteButton)
ExecuteButtonCorner.CornerRadius = UDim.new(0, 20)

-- Acción al hacer clic en el botón de ejecutar
ExecuteButton.MouseButton1Click:Connect(function()
    local scriptText = ScriptBox.Text
    -- Intenta ejecutar el script
    local success, err = pcall(function()
        loadstring(scriptText)()
    end)

    -- Si ocurre un error, mostrarlo en la consola
    if not success then
        warn("Error al ejecutar el script: " .. tostring(err))
    end
end)

-- Propiedades de CloseButton
CloseButton.Name = "CloseButton"
CloseButton.Parent = MainFrame
CloseButton.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
CloseButton.Position = UDim2.new(0.9, -30, 0.05, 0)
CloseButton.Size = UDim2.new(0, 35, 0, 35)
CloseButton.Font = Enum.Font.GothamBold
CloseButton.Text = "X"
CloseButton.TextColor3 = Color3.fromRGB(255, 255, 255)
CloseButton.TextSize = 14

-- Agregar bordes redondeados al CloseButton
local CloseButtonCorner = Instance.new("UICorner", CloseButton)
CloseButtonCorner.CornerRadius = UDim.new(0, 20)

-- Acción al hacer clic en el botón de cerrar
CloseButton.MouseButton1Click:Connect(function()
    ScreenGui:Destroy() -- Cierra la GUI eliminándola
end)

-- Animación de apertura del MainFrame (desde el centro hacia todos los lados)
local tweenInfo = TweenInfo.new(1.5, Enum.EasingStyle.Quint, Enum.EasingDirection.Out)
local expandTween = TweenService:Create(MainFrame, tweenInfo, {
    Size = UDim2.new(0, 400, 0, 250),
    Position = UDim2.new(0.5, 0, 0.5, 0)
})

expandTween:Play()
end)

Section:NewButton("VR7-", "", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/VR7ss/OMK/refs/heads/main/VR7-ON-TOP"))()
end)

Section:NewButton("sYsTem-bRokEn", "", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/H20CalibreYT/SystemBroken/main/script"))()
end)

Section:NewButton("1st -1", "", function()
    loadstring(game:HttpGet("https://gist.githubusercontent.com/amroffaads/54277157b77455d610973ec3756a22aa/raw/28fea5aa42ed1e58b999707fc08aacf61945d91e/1st"))()
end)

Section:NewButton("1st -2", "", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/fscript4u/script1stbyamroand787/refs/heads/main/1st%200.7"))()
end)

Section:NewButton("Tvon", "", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/SnoobG/Lua-Script-s/refs/heads/main/Tvon"))()
end)

local Tab = Window:NewTab("Admins ")
local Section = Tab:NewSection("Admins-Scripts")

Section:NewButton("IY", "", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source"))()
end)

Section:NewButton("Nameless v1", "", function()
    loadstring(game:HttpGet("https://github.com/FilteringEnabled/NamelessAdmin/blob/main/Source?raw=true"))()
end)

Section:NewButton("Nameless v2", "", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/ltseverydayyou/Nameless-Admin/main/Source.lua"))()
end)

local Tab = Window:NewTab("RaNdom ")
local Section = Tab:NewSection("raNdoM-Scripts")

Section:NewButton("Reset-Hotkey", "", function()
    game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(KeyPressed)
        if KeyPressed == "r" then
        game.Players.LocalPlayer.Character.Humanoid.Health = 0
    end
    end)
end)
