                local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/ionlyusegithubformcmods/1-Line-Scripts/main/Mobile%20Friendly%20Orion')))()
                
                local Window = OrionLib:MakeWindow({Name = "Slap Battles", HidePremium = true, IntroEnabled = false, SaveConfig = true, ConfigFolder = "OrionTest"})

                local Tab = Window:MakeTab({
                    Name = "Home",
                    Icon = "http://www.roblox.com/asset/?id=",
                    PremiumOnly = false
                })

                local Tab2 = Window:MakeTab({
                    Name = "Ability Spams",
                    Icon = "http://www.roblox.com/asset/?id=",
                    PremiumOnly = false
                })

                local Tab3 = Window:MakeTab({
                    Name = "Antis",
                    Icon = "http://www.roblox.com/asset/?id=",
                    PremiumOnly = false
                })
 
                local Tab4 = Window:MakeTab({
                    Name = "Misc",
                    Icon = "http://www.roblox.com/asset/?id=",
                    PremiumOnly = false
                })

                local Tab5 = Window:MakeTab({
                    Name = "Badges",
                    Icon = "http://www.roblox.com/asset/?id=",
                    PremiumOnly = false
                })

                local Tab6 = Window:MakeTab({
                    Name = "Player",
                    Icon = "http://www.roblox.com/asset/?id=",
                    PremiumOnly = false
                })

                local Tab8 = Window:MakeTab({
                    Name = "Hubs",
                    Icon = "http://www.roblox.com/asset/?id=",
                    PremiumOnly = false
                })

Tab:AddLabel("If you have problems then message Guy that exists#1915")

Tab:AddButton({
	Name = "Destroy GUI",
	Callback = function()
      		OrionLib:Destroy()
  	end    
})
                
Tab2:AddLabel("A lot of these work in the lobby")
Tab2:AddLabel("Don't manually use ability while the spam is running")

                Tab2:AddToggle({
                    Name = "Rhythm Explosion Spam (WORKS WITH ALL GLOVES)",
                    Default = false,
                    Callback = function(Value)
_G.RhythmSpam = Value
while _G.RhythmSpam do
game:GetService("ReplicatedStorage").rhythmevent:FireServer("AoeExplosion",0)
task.wait()
end
                    end    
                })
                Tab2:AddToggle({
                    Name = "Home Run Spam",
                    Default = false,
                    Callback = function(Value)
_G.HomeRunSpam = Value
while _G.HomeRunSpam do
game:GetService("ReplicatedStorage").HomeRun:FireServer({["start"] = true})
game:GetService("ReplicatedStorage").HomeRun:FireServer({["finished"] = true})
task.wait()
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Home Run Max Charge Spam",
                    Default = false,
                    Callback = function(Value)
_G.HomeRunSpam = Value
while _G.HomeRunSpam do
local args = {
    [1] = {
        ["start"] = true
    }
}
game:GetService("ReplicatedStorage").HomeRun:FireServer(unpack(args))
wait(3.05)
                    end    
end
                })

                Tab2:AddToggle({
                    Name = "Shukuchi Spam",
                    Default = false,
                    Callback = function(Value)
_G.ShukuchiSpam = Value
while _G.ShukuchiSpam do
local LocalPlayer = game.Players.LocalPlayer
local players = game.Players:GetChildren()
local RandomPlayer = players[math.random(1, #players)]
repeat RandomPlayer = players[math.random(1, #players)] until RandomPlayer ~= LocalPlayer
repeat RandomPlayer = players[math.random(1, #players)] until RandomPlayer.Character.isInArena.Value == true
PersonToKill = RandomPlayer
game:GetService("ReplicatedStorage").SM:FireServer(PersonToKill)
wait(0.01)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Slicer Spam",
                    Default = false,
                    Callback = function(Value)
_G.SlicerSpam = Value
while _G.SlicerSpam do
game:GetService("ReplicatedStorage").Slicer:FireServer("sword")
game:GetService("ReplicatedStorage").Slicer:FireServer("slash", CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position) * CFrame.Angles(-5.66729e-11, 0.000832287, -1.10219e-10), Vector3.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Rotation))
wait(5.1)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "ðŸ—¿ Spam",
                    Default = false,
                    Callback = function(Value)
_G.MoaiSpam = Value
while _G.MoaiSpam do
game:GetService("ReplicatedStorage"):WaitForChild("GeneralAbility"):FireServer(CFrame.new(math.random(-70, 63), -5.72293854, math.random(-90, 93), 0.151493087, -8.89114702e-08, 0.988458335, 1.45089563e-09, 1, 8.97272727e-08, -0.988458335, -1.21589121e-08, 0.151493087))
wait(3.05)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Rob Spam",
                    Default = false,
                    Callback = function(Value)
_G.RobSpam = Value
while _G.RobSpam do
game:GetService("ReplicatedStorage"):WaitForChild("rob"):FireServer()
wait(15)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Kraken Spam",
                    Default = false,
                    Callback = function(Value)
_G.KrakenSpam = Value
while _G.KrakenSpam do
game:GetService("ReplicatedStorage").KrakenArm:FireServer()
wait(5)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Psycho Spam",
                    Default = false,
                    Callback = function(Value)
_G.PsychoSpam = Value
while _G.PsychoSpam do
game:GetService("ReplicatedStorage").Psychokinesis:InvokeServer({["grabEnabled"] = true})
task.wait()
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Killstreak Soul Snatcher Spam",
                    Default = false,
                    Callback = function(Value)
_G.KillstreakSpam = Value
while _G.KillstreakSpam do
game:GetService("ReplicatedStorage").KSABILI:FireServer()
wait(6.1)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Bus Spam",
                    Default = false,
                    Callback = function(Value)
_G.BusSpam = Value
while _G.BusSpam do
game:GetService("ReplicatedStorage").busmoment:FireServer()
wait(5.2)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Mitten Spam",
                    Default = false,
                    Callback = function(Value)
_G.MittenSpam = Value
while _G.MittenSpam do
game:GetService("ReplicatedStorage").MittenA:FireServer()
wait(5.2)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Fort Spam",
                    Default = false,
                    Callback = function(Value)
_G.FortSpam = Value
while _G.FortSpam do
game:GetService("ReplicatedStorage").Fortlol:FireServer()
wait(3.05)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Defense Spam",
                    Default = false,
                    Callback = function(Value)
_G.DefenseSpam = Value
while _G.DefenseSpam do
game:GetService("ReplicatedStorage").Barrier:FireServer()
wait(0.25)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Bomb Spam",
                    Default = false,
                    Callback = function(Value)
_G.BombSpam = Value
while _G.BombSpam do
game:GetService("ReplicatedStorage").BombThrow:FireServer()
wait(2.5)
game:GetService("ReplicatedStorage").BombThrow:FireServer()
wait(4.2)
end
                    end    
                })

              Tab2:AddToggle({
                    Name = "Replica Spam",
                    Default = false,
                    Callback = function(Value)
_G.ReplicaSpam = Value
while _G.ReplicaSpam do
game:GetService("ReplicatedStorage").Duplicate:FireServer()
wait(5.2)
end
                    end    
                })
             
                Tab2:AddToggle({
                    Name = "Pusher Spam",
                    Default = false,
                    Callback = function(Value)
_G.PusherSpam = Value
while _G.PusherSpam do
game:GetService("ReplicatedStorage").PusherWall:FireServer()
wait(5.2)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Jet Spam",
                    Default = false,
                    Callback = function(Value)
_G.JetSpam = Value
while _G.JetSpam do
local LocalPlayer = game.Players.LocalPlayer
local players = game.Players:GetChildren()
local RandomPlayer = players[math.random(1, #players)]
repeat RandomPlayer = players[math.random(1, #players)] until RandomPlayer ~= LocalPlayer
repeat RandomPlayer = players[math.random(1, #players)] until RandomPlayer.Character.isInArena.Value == true
PersonToKill = RandomPlayer
game:GetService("ReplicatedStorage").AirStrike:FireServer(PersonToKill.Character)
wait(5.2)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Tableflip Spam",
                    Default = false,
                    Callback = function(Value)
_G.TableflipSpam = Value
while _G.TableflipSpam do
game:GetService("ReplicatedStorage").GeneralAbility:FireServer()
wait(3.05)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Rocky Spam",
                    Default = false,
                    Callback = function(Value)
_G.RockySpam = Value
while _G.RockySpam do
game:GetService("ReplicatedStorage").RockyShoot:FireServer()
wait(6.2)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Timestop Spam",
                    Default = false,
                    Callback = function(Value)
_G.TimestopSpam = Value
while _G.TimestopSpam do
game:GetService("ReplicatedStorage").TimestopJump:FireServer()
game:GetService("ReplicatedStorage").Timestopchoir:FireServer()
game:GetService("ReplicatedStorage").Timestop:FireServer()
wait(50.2)
end
                    end    
                })
                
                Tab2:AddToggle({
                    Name = "Za Hando Spam",
                    Default = false,
                    Callback = function(Value)
_G.ZahandoSpam = Value
while _G.ZahandoSpam do
game:GetService("ReplicatedStorage").Erase:FireServer()
wait(5.1)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Baller Spam",
                    Default = false,
                    Callback = function(Value)
_G.BallerSpam = Value
while _G.BallerSpam do
game:GetService("ReplicatedStorage").GeneralAbility:FireServer()
wait(4.2)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Stun Spam",
                    Default = false,
                    Callback = function(Value)
_G.StunSpam = Value
while _G.StunSpam do
game:GetService("ReplicatedStorage").StunR:FireServer(game:GetService("Players").LocalPlayer.Character.Stun)
wait(10.2)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Glitch Spam",
                    Default = false,
                    Callback = function(Value)
_G.GlitchSpam = Value
while _G.GlitchSpam do
game:GetService("ReplicatedStorage").GeneralAbility:FireServer()
wait(4.2)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Stop Spam",
                    Default = false,
                    Callback = function(Value)
_G.StopSpam = Value
while _G.StopSpam do
game:GetService("ReplicatedStorage").STOP:FireServer(true)
wait(4.2)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Track Spam",
                    Default = false,
                    Callback = function(Value)
_G.TrackSpam = Value
while _G.TrackSpam do
 local LocalPlayer = game.Players.LocalPlayer
local players = game.Players:GetChildren()
local RandomPlayer = players[math.random(1, #players)]
repeat RandomPlayer = players[math.random(1, #players)] until RandomPlayer ~= LocalPlayer
PersonToKill = RandomPlayer
game:GetService("ReplicatedStorage").GeneralAbility:FireServer(PersonToKill.Character)
wait(10.2)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Track Orbit",
                    Default = false,
                    Callback = function(Value)
_G.TrackSpam = Value
while _G.TrackSpam do
game:GetService("ReplicatedStorage").GeneralAbility:FireServer(game:GetService("Players").LocalPlayer.Character)
wait(10.2)
end
                    end    
                })
                
                Tab2:AddToggle({
                    Name = "Mail Spam",
                    Default = false,
                    Callback = function(Value)
_G.MailSpam = Value
while _G.MailSpam do
game:GetService("ReplicatedStorage").MailSend:FireServer()
wait(3.2)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Shard Spam",
                    Default = false,
                    Callback = function(Value)
_G.ShardSpam = Value
while _G.ShardSpam do
game:GetService("ReplicatedStorage").Shards:FireServer()
wait(4.2)
end
                    end    
                })
                
                Tab2:AddToggle({
                    Name = "Swapper Spam",
                    Default = false,
                    Callback = function(Value)
_G.SwapperSpam = Value
while _G.SwapperSpam do
game:GetService("ReplicatedStorage").SLOC:FireServer()
wait(5.2)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Bubble Spam",
                    Default = false,
                    Callback = function(Value)
_G.BubbleSpam = Value
while _G.BubbleSpam do
game:GetService("ReplicatedStorage").BubbleThrow:FireServer()
wait(3.05)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Slapple Spam",
                    Default = false,
                    Callback = function(Value)
_G.SlappleSpam = Value
while _G.SlappleSpam do
game:GetService("ReplicatedStorage").funnyTree:FireServer(game.Players.LocalPlayer.Character.HumanoidRootPart.Position)
wait(3.05)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Kinetic Spam",
                    Default = false,
                    Callback = function(Value)
_G.KineticSpam = Value
while _G.KineticSpam do
game:GetService("ReplicatedStorage").KineticExpl:FireServer(game:GetService("Players").LocalPlayer.Character.Kinetic, game.Players.LocalPlayer.Character.HumanoidRootPart.Position)
wait(9.2)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Dominance Spam",
                    Default = false,
                    Callback = function(Value)
_G.DominanceSpam = Value
while _G.DominanceSpam do
game:GetService("ReplicatedStorage").DominanceAc:FireServer(game.Players.LocalPlayer.Character.HumanoidRootPart.Position)
wait(3.05)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Shield Spam",
                    Default = false,
                    Callback = function(Value)
_G.ShieldSpam = Value
while _G.ShieldSpam do
game:GetService("ReplicatedStorage").GeneralAbility:FireServer()
wait(3.05)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Redacted Spam",
                    Default = false,
                    Callback = function(Value)
_G.RedactedSpam = Value
while _G.RedactedSpam do
game:GetService("ReplicatedStorage").Well:FireServer()
wait(5.2)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Duelist Spam",
                    Default = false,
                    Callback = function(Value)
_G.DuelistSpam = Value
while _G.DuelistSpam do
game:GetService("ReplicatedStorage").DuelistAbility:FireServer()
wait(5.05)
end
                    end    
                })
                
                Tab2:AddToggle({
                    Name = "Sentry Spam",
                    Default = false,
                    Callback = function(Value)
_G.SentrySpam = Value
while _G.SentrySpam do
game:GetService("ReplicatedStorage").Sentry:FireServer()
wait(5.2)
end
                    end    
                })
                
                Tab2:AddToggle({
                    Name = "Brick Spam",
                    Default = false,
                    Callback = function(Value)
_G.BrickSpam = Value
while _G.BrickSpam do
game:GetService("ReplicatedStorage").lbrick:FireServer()
wait(1.05)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Trap Spam",
                    Default = false,
                    Callback = function(Value)
_G.TrapSpam = Value
while _G.TrapSpam do
game:GetService("ReplicatedStorage").funnyhilariousbeartrap:FireServer()
wait(3.05)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Woah Spam",
                    Default = false,
                    Callback = function(Value)
_G.WoahSpam = Value
while _G.WoahSpam do
game:GetService("ReplicatedStorage").VineThud:FireServer()
wait(5.2)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Ping Pong Spam",
                    Default = false,
                    Callback = function(Value)
_G.PingPongSpam = Value
while _G.PingPongSpam do
game:GetService("ReplicatedStorage").GeneralAbility:FireServer()
wait(8)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Spam Recall VFX",
                    Default = false,
                    Callback = function(Value)
_G.RecallVFXSpam = Value
while _G.RecallVFXSpam do
game:GetService("ReplicatedStorage").Recall:InvokeServer(game:GetService("Players").LocalPlayer.Character.Recall)
wait(3.05)
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Spam Sleep",
                    Default = false,
                    Callback = function(Value)
_G.SleepSpam = Value
while _G.SleepSpam do
game:GetService("ReplicatedStorage").ZZZZZZZSleep:FireServer()
task.wait()
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Spam Default Sound",
                    Default = false,
                    Callback = function(Value)
_G.DefaultSoundSpam = Value
while _G.DefaultSoundSpam do
game:GetService("ReplicatedStorage").b:FireServer("ReplicateSound")
task.wait()
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Spam Error Sound (Works with all gloves)",
                    Default = false,
                    Callback = function(Value)
_G.ErrorSoundSpam = Value
while _G.ErrorSoundSpam do
game.ReplicatedStorage.ErrorDeath:FireServer()
task.wait()
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Spam Slicer Sound",
                    Default = false,
                    Callback = function(Value)
_G.SlicerSoundSpam = Value
while _G.SlicerSoundSpam do
game:GetService("ReplicatedStorage").Slicer:FireServer("sword")
task.wait()
end
                    end    
                })
                
                Tab2:AddToggle({
                    Name = "Spam Space Sound",
                    Default = false,
                    Callback = function(Value)
_G.SpaceSoundSpam = Value
while _G.SpaceSoundSpam do
game:GetService("ReplicatedStorage").ZeroGSound:FireServer()
task.wait()
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Spam Ghost Sound",
                    Default = false,
                    Callback = function(Value)
_G.GhostSoundSpam = Value
while _G.GhostSoundSpam do
game.ReplicatedStorage.Ghostinvisibilityactivated:FireServer()
    game.ReplicatedStorage.Ghostinvisibilitydeactivated:FireServer()
task.wait()
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Spam Thanos Sound",
                    Default = false,
                    Callback = function(Value)
_G.ThanosSoundSpam = Value
while _G.ThanosSoundSpam do
game:GetService("ReplicatedStorage").Illbeback:FireServer()
task.wait()
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Spam Golden Sound",
                    Default = false,
                    Callback = function(Value)
_G.GoldenSoundSpam = Value
while _G.GoldenSoundSpam do
game:GetService("ReplicatedStorage").Goldify:FireServer(true)
task.wait()
end
                    end    
                })

                Tab2:AddToggle({
                    Name = "Spam Charge Sound",
                    Default = false,
                    Callback = function(Value)
_G.ChargeSoundSpam = Value
while _G.ChargeSoundSpam do
game:GetService("ReplicatedStorage").GeneralAbility:FireServer(game:GetService("Players").LocalPlayer.Character.Charge)
wait(3.05)
end
                    end    
                })

Tab4:AddButton({
	Name = "Kick player (Needs Za Hando) (Inconsistent)",
	Callback = function()
OGWS = game.Players.LocalPlayer.Character.Humanoid.WalkSpeed
OGJP = game.Players.LocalPlayer.Character.Humanoid.JumpPower
for i,v in pairs(game.Workspace.Lobby.brazil:GetChildren()) do
                    if v.ClassName == "Part" then
                        v.CanTouch = false
                    end
                end
game:GetService("ReplicatedStorage").Erase:FireServer()
wait(0.47)
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 0
game.Players.LocalPlayer.Character.Humanoid.JumpPower = 0
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = workspace.Spot.CFrame * CFrame.new(1022,213.8,1498)
wait(3.5)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.workspace.Arena.Rock.CFrame
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = OGWS
game.Players.LocalPlayer.Character.Humanoid.JumpPower = OGJP
for i,v in pairs(game.Workspace.Lobby.brazil:GetChildren()) do
                    if v.ClassName == "Part" then
                        v.CanTouch = true
                    end
                end
                    end    
                })

Tab4:AddButton({
	Name = "View Testing Server (Good for glove leaking)",
	Callback = function()
local teleportFunc = queueonteleport or queue_on_teleport or syn and syn.queue_on_teleport
if teleportFunc then
    teleportFunc([[
        if not game:IsLoaded() then
            game.Loaded:Wait()
        end
        local localPlr = game:GetService("Players").LocalPlayer
        repeat wait() until localPlr
game:GetService("GuiService"):ClearError()
    ]])
end
game:GetService("TeleportService"):Teleport(9020359053)
                    end    
                })

Tab4:AddButton({
	Name = "View Slap Royale Testing Server",
	Callback = function()
local teleportFunc = queueonteleport or queue_on_teleport or syn and syn.queue_on_teleport
if teleportFunc then
    teleportFunc([[
        if not game:IsLoaded() then
            game.Loaded:Wait()
        end
        local localPlr = game:GetService("Players").LocalPlayer
        repeat wait() until localPlr
        game:GetService("RunService").RenderStepped:Connect(function()
            game:GetService("GuiService"):ClearError()
        end)
    ]])
end
game:GetService("TeleportService"):Teleport(9412268818)
                    end    
                })

Tab4:AddButton({
	Name = "Testing Server Freecam",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/ionlyusegithubformcmods/1-Line-Scripts/main/SB%20Freecam"))()
                    end    
                })

Tab4:AddButton({
	Name = "Testing Server Freecam (Mobile)",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/zephyr10101/CameraSpy/main/Script", true))()
                    end    
                })

Tab4:AddButton({
	Name = "Slap Farm (This copies the script, put it in autoexec)",
	Callback = function()
setclipboard("loadstring(game:HttpGet('https://raw.githubusercontent.com/ionlyusegithubformcmods/1-Line-Scripts/main/Slap%20Farm'))()")
                    end    
                })

Tab4:AddButton({
	Name = "Start Slap Farm (Take the script out of autoexec to stop)",
	Callback = function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/ionlyusegithubformcmods/1-Line-Scripts/main/Slap%20Farm'))()
                    end    
                })

Tab4:AddToggle({
                    Name = "Slap Aura (Credits to R2O)",
                    Default = false,
                    Callback = function(bool)
getgenv().SlapAura = bool
            if bool == true then
                while getgenv().SlapAura do
                    task.wait(.005)
                        pcall(function()
                        for Index, Player in next, game.Players:GetPlayers() do
                            if Player ~= game.Players.LocalPlayer and Player.Character and Player.Character:FindFirstChild("entered") then
                                if Player.Character:FindFirstChild("Head") then
                                if Player.Character.Head:FindFirstChild("UnoReverseCard") == nil and Player.Character:FindFirstChild("rock") == nil then 
                                    if game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
                                    local Magnitude = (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - Player.Character.HumanoidRootPart.Position).Magnitude
                                    if 25 >= Magnitude then
                                        shared.gloveHits[getGlove()]:FireServer(Player.Character:WaitForChild("Head"))
                                end
                                    end
                            end
                                end
                        end
                        end
                    end)
                end
            end
end
                })

Tab4:AddButton({
	Name = "Give reaper 20 kills (Use after they slap you)",
	Callback = function()
for i = 1, 20 do
        game:GetService("ReplicatedStorage"):WaitForChild("HumanoidDied"):FireServer(x,false)
wait()
end
                    end    
                })

                Tab4:AddToggle({
                    Name = "Rhythm Note Spam + Auto Press (Equip Rhythm)",
                    Default = false,
                    Callback = function(Value)
_G.RhythmNoteSpam = Value
while _G.RhythmNoteSpam do
game.Players.LocalPlayer.PlayerGui.Rhythm.LocalScript.Disabled = false
game.Players.LocalPlayer.PlayerGui.Rhythm.LocalScript.Disabled = true
game.Players.LocalPlayer.Character.Rhythm:Activate()
task.wait()
end
                    end    
                })

Tab4:AddToggle({
                    Name = "Auto Enter Arena",
                    Default = false,
                    Callback = function(Value)
local localPlr = game:GetService("Players").LocalPlayer
getgenv().AutoEnterArena = Value
      while getgenv().AutoEnterArena == true do
       wait(.001)
if not localPlr.Character:FindFirstChild("entered") and localPlr.Character:FindFirstChild("HumanoidRootPart") then
firetouchinterest(game.Players.LocalPlayer.Character:WaitForChild("Head"), workspace.Lobby.Teleport1.TouchInterest.Parent, 0)
firetouchinterest(game.Players.LocalPlayer.Character:WaitForChild("Head"), workspace.Lobby.Teleport1.TouchInterest.Parent, 1)
    end
end
end,
                })

Tab4:AddToggle({
                    Name = "Remove Nametag (Breaks killstreak) (Credits to R2O)",
                    Default = false,
                    Callback = function(bool)
Auto_Remove = bool
        if bool == true then
        game.Players.LocalPlayer.Character:FindFirstChild("Head").Nametag.TextLabel:Destroy()
            task.wait()
            game.Players.LocalPlayer.CharacterAdded:Connect(function()
                if Auto_Remove == true then
                repeat task.wait()
                until game.Players.LocalPlayer.Character:FindFirstChild("Head")
                game.Players.LocalPlayer.Character:FindFirstChild("Head").Nametag.TextLabel:Destroy()
                end
            end)
        end
end
                })

Tab4:AddButton({
	Name = "Free Emotes(Type /e emotename) (Credits to R2O)",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/ionlyusegithubformcmods/1-Line-Scripts/main/SB%20Emotes"))()
                    end    
                })

Tab4:AddButton({
	Name = "Turn glove into a block (Doesn't work with all gloves)",
	Callback = function()
for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
if v:IsA("Tool") then
if v.Glove.Mesh or v.Glove.Cuff.Mesh then
v.Glove.Mesh:Destroy()
v.Glove.Cuff.Mesh:Destroy()
end
end
end
                    end    
                })

Tab4:AddButton({
	Name = "Infinite Golden (Use in arena)",
	Callback = function()
game:GetService("ReplicatedStorage").Goldify:FireServer(true)
                    end    
                })

                Tab4:AddToggle({
                    Name = "Infinite Reverse",
                    Default = false,
                    Callback = function(Value)
_G.InfReverse = Value
while _G.InfReverse do
game:GetService("ReplicatedStorage").ReverseAbility:FireServer()
wait(6)
end
                    end    
                })

Tab4:AddToggle({
                    Name = "Rainbow Character (Needs Golden)",
                    Default = false,
                    Callback = function(Value)
_G.Rainbow = Value
while _G.Rainbow do
local randomnumber = math.random(1004, 1032)
local args = {
    [1] = false,
    [2] = BrickColor.new(randomnumber)
}

game:GetService("ReplicatedStorage").Goldify:FireServer(unpack(args))
task.wait(0.075)
end
end
                })

local function GetClosestPlayer()
   local bestdistance,player = nil,nil
   pcall(function()
       for i,v in pairs(game.Players:GetPlayers()) do
           if v == game.Players.LocalPlayer then continue end
           local distance = (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - v.Character.HumanoidRootPart.Position).magnitude
           if bestdistance == nil and player == nil then
               bestdistance = distance
               player = v
           elseif bestdistance > distance then
               player = v
               bestdistance = distance
           end
       end
       if bestdistance > radius then
          player = nil 
       end
   end)
   return player
end

Tab4:AddButton({
	Name = "TP to Safe spot",
	Callback = function()
      		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = workspace.Spot.CFrame * CFrame.new(0,50,0)
  	end    
})

Tab4:AddButton({
	Name = "TP back to arena",
	Callback = function()
      		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.workspace.Arena.Rock.CFrame
  	end    
})

Tab8:AddButton({
	Name = "CherryUi's Slap Battles GUI",
	Callback = function()
      		loadstring(game:HttpGet("https://raw.githubusercontent.com/RandomScriptr3/gggggggg/main/lolez.txt", true))()
  	end    
})

Tab8:AddButton({
	Name = "R2O",
	Callback = function()
      		loadstring(game:HttpGet(("https://raw.githubusercontent.com/cheesynob39/R2O/main/Main.lua")))()
  	end    
})

Tab8:AddButton({
	Name = "dizzy hub",
	Callback = function()
      		loadstring(game:HttpGet("https://raw.githubusercontent.com/dizyhvh/rbx_scripts/main/dizzy_hub/scripts/slap_battles.lua"))()
  	end    
})

Tab6:AddSlider({
	Name = "Walkspeed",
	Min = 20,
	Max = 1000,
	Default = 20,
	Color = Color3.fromRGB(0,162,255),
	Increment = 1,
	ValueName = "WS",
	Callback = function(Value)
		game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
Walkspeed = Value
	end    
})

Tab6:AddToggle({
	Name = "Loop Walkspeed",
	Default = false,
	Callback = function(bool)
autoSet1 = bool
        if bool == true then
            while autoSet1 do
                task.wait()
                local Character = workspace:WaitForChild(game.Players.LocalPlayer.Name)
                if Character:FindFirstChild("Humanoid") ~= nil and Character.Humanoid.WalkSpeed ~= Walkspeed then
                    Character:FindFirstChild("Humanoid").WalkSpeed = Walkspeed
                end
            end
        end
	end    
})

Tab6:AddSlider({
	Name = "Jumppower",
	Min = 50,
	Max = 1000,
	Default = 50,
	Color = Color3.fromRGB(255,154,0),
	Increment = 1,
	ValueName = "JP",
	Callback = function(Value)
		game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
Jumppower = Value
	end    
})

Tab6:AddToggle({
	Name = "Loop Jumppower",
	Default = false,
	Callback = function(bool)
autoSet1 = bool
        if bool == true then
            while autoSet1 do
                task.wait()
                local Character = workspace:WaitForChild(game.Players.LocalPlayer.Name)
                if Character:FindFirstChild("Humanoid") ~= nil and Character.Humanoid.WalkSpeed ~= Jumppower then
                    Character:FindFirstChild("Humanoid").WalkSpeed = Jumppower
                end
            end
        end
	end    
})

Tab5:AddButton({
                    Name = "Get [REDACTED] (Credits to R2O)",
Callback = function()
local Door = 1
if not game:GetService("BadgeService"):UserHasBadgeAsync(game.Players.LocalPlayer.UserId, 2124847850) and 5000 <= game.Players.LocalPlayer.leaderstats.Slaps.Value then
    repeat
    task.wait(.25)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.PocketDimension.Doors[Door].CFrame
    Door = Door + 1
    print(Door)
    wait(5)
    until game:GetService("BadgeService"):UserHasBadgeAsync(game.Players.LocalPlayer.UserId, 2124847850)
else 
game.StarterGui:SetCore("SendNotification", {
                Title = "Error";
                Duration = 5;
                Text = "You already have [ R E D A C T E D ]!";
            })
game.StarterGui:SetCore("SendNotification", {
                Title = "Error";
                Duration = 5;
                Text = "Or you don't have 5K slaps.";
            })
    print("You already have [ R E D A C T E D ]!")
    print("Or you don't have 5K slaps.")
end
end
                    })

Tab5:AddButton({
	Name = "Get Elude (Credit to R2O)",
	Callback = function()
Place = game.PlaceId
Server = game.JobId
local teleportFunc = queueonteleport or queue_on_teleport or syn and syn.queue_on_teleport
if teleportFunc then
    teleportFunc([[
        if not game:IsLoaded() then
            game.Loaded:Wait()
        end
        local localPlr = game:GetService("Players").LocalPlayer
        repeat wait() until localPlr
        game:GetService("RunService").RenderStepped:Connect(function()
            localPlr.Character.HumanoidRootPart.CFrame = CFrame.new(-502.336, 14.228, -179.597)
        end)
game:GetService("TeleportService"):TeleportToPlaceInstance(Place, Server, game.Players.LocalPlayer)
    ]])
end
game:GetService("TeleportService"):Teleport(11828384869)
  	end    
})

Tab5:AddButton({
	Name = "Get Counter (Use when in maze)",
	Callback = function()
fireclickdetector(game.Workspace.CounterLever.ClickDetector)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0,100,0)
wait(0.2)
game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true
wait(121)
for i,v in pairs(workspace.Maze:GetDescendants()) do
if v:IsA("ClickDetector") then
fireclickdetector(v)
end
end
  	end    
})

Tab5:AddButton({
	Name = "Get Chain (Needs 1k slaps) (Credit to R2O)",
	Callback = function()
Place = game.PlaceId
Server = game.JobId
local teleportFunc = queueonteleport or queue_on_teleport or syn and syn.queue_on_teleport
if teleportFunc then
    teleportFunc([[
        if not game:IsLoaded() then
            game.Loaded:Wait()
        end
        local localPlr = game:GetService("Players").LocalPlayer
        repeat wait() until localPlr
local decal_codes = {
    ["http://www.roblox.com/asset/?id=9648769161"] = "4",
    ["http://www.roblox.com/asset/?id=9648765536"] = "2",
    ["http://www.roblox.com/asset/?id=9648762863"] = "3",
    ["http://www.roblox.com/asset/?id=9648759883"] = "9",
    ["http://www.roblox.com/asset/?id=9648755440"] = "8",
    ["http://www.roblox.com/asset/?id=9648752438"] = "2",
    ["http://www.roblox.com/asset/?id=9648749145"] = "8",
    ["http://www.roblox.com/asset/?id=9648745618"] = "3",
    ["http://www.roblox.com/asset/?id=9648742013"] = "7",
    ["http://www.roblox.com/asset/?id=9648738553"] = "8",
    ["http://www.roblox.com/asset/?id=9648734698"] = "2",
    ["http://www.roblox.com/asset/?id=9648730082"] = "6",
    ["http://www.roblox.com/asset/?id=9648723237"] = "3",
    ["http://www.roblox.com/asset/?id=9648718450"] = "6",
    ["http://www.roblox.com/asset/?id=9648715920"] = "6",
    ["http://www.roblox.com/asset/?id=9648712563"] = "2"
}
    for i,v in ipairs(game:GetService("Workspace").Map:WaitForChild("CodeBrick"):WaitForChild("SurfaceGui"):GetDescendants()) do
        if v.Name == 'IMGTemplate' then
            local decal_url = tostring(v.Image)
            local code = decal_codes[decal_url]
            if 0 < #game:GetService("Workspace").Map:WaitForChild("OriginOffice").Door.Keypad.Display.SurfaceGui.TextLabel.Text then
                fireclickdetector(game:GetService("Workspace").Map:WaitForChild("OriginOffice").Door.Keypad.Buttons.Reset.ClickDetector)
            end
            task.wait(.2)
            fireclickdetector(game:GetService("Workspace").Map:WaitForChild("OriginOffice").Door.Keypad.Buttons[code].ClickDetector)
        end
    end
    task.wait(.2)
    fireclickdetector(game:GetService("Workspace").Map:WaitForChild("OriginOffice").Door.Keypad.Buttons.Enter.ClickDetector)
game:GetService("TeleportService"):TeleportToPlaceInstance(Place, Server, game.Players.LocalPlayer)
    ]])
end
game:GetService("TeleportService"):Teleport(9431156611)
  	end    
})

Tab5:AddButton({
	Name = "Get Tycoon (Credits to R2O)",
	Callback = function()
      		repeat task.wait(.005)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = workspace.Arena.Plate.CFrame * CFrame.new(0,-2,0)
until game.Players.LocalPlayer.PlayerGui.PlateIndicator.TextLabel.Text == "Plate Counter: 600"
                    end    
                })

Tab5:AddButton({
	Name = "Get Trap (Only 20 mins)",
	Callback = function()
for i = 1, 200 do
game:GetService("ReplicatedStorage").lbrick:FireServer()
game.Players.LocalPlayer.PlayerGui.BRICKCOUNT.ImageLabel.TextLabel.Text = game.Players.LocalPlayer.PlayerGui.BRICKCOUNT.ImageLabel.TextLabel.Text + 1;
wait(Random.new():NextNumber(1.05,1.30))
game:GetService("ReplicatedStorage").lbrick:FireServer()
game.Players.LocalPlayer.PlayerGui.BRICKCOUNT.ImageLabel.TextLabel.Text = game.Players.LocalPlayer.PlayerGui.BRICKCOUNT.ImageLabel.TextLabel.Text + 1;
wait(Random.new():NextNumber(1.05,1.30))
game:GetService("ReplicatedStorage").lbrick:FireServer()
game.Players.LocalPlayer.PlayerGui.BRICKCOUNT.ImageLabel.TextLabel.Text = game.Players.LocalPlayer.PlayerGui.BRICKCOUNT.ImageLabel.TextLabel.Text + 1;
wait(Random.new():NextNumber(1.05,1.30))
game:GetService("ReplicatedStorage").lbrick:FireServer()
game.Players.LocalPlayer.PlayerGui.BRICKCOUNT.ImageLabel.TextLabel.Text = game.Players.LocalPlayer.PlayerGui.BRICKCOUNT.ImageLabel.TextLabel.Text + 1;
wait(Random.new():NextNumber(1.05,1.30))
game:GetService('VirtualInputManager'):SendKeyEvent(true,'E',false,x)
wait(Random.new():NextNumber(1.05,1.30))
end
                    end    
                })

Tab5:AddToggle({
	Name = "Brick Farm (Use if the 20m version doesnt work)",
	Default = false,
	Callback = function(Value)
game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = Value
		_G.Brickfarm = Value
while _G.Brickfarm do
game:GetService('VirtualInputManager'):SendKeyEvent(true,'E',false,x)
task.wait(5.01)
endÄƒ
	end    
})

Tab5:AddToggle({
                    Name = "Bob Farm (Credits to R2O)",
                    Default = false,
                    Callback = function(bool)
bobFarm = bool
        if bool == true then
            while bobFarm do
                task.wait()
                    if getGlove() == "Replica" and bobFarm and not game:GetService("BadgeService"):UserHasBadgeAsync(game.Players.LocalPlayer.UserId, 2125950512) then
                    game.ReplicatedStorage.Duplicate:FireServer()
                    task.wait()
                    tick = os.time()
                    repeat task.wait()
                    until os.time() - tick >= 5.2
                    end
            end
            else
            task.wait(10.2)
        end
                    end    
                })

Tab5:AddButton({
	Name = "Get Brazil badge",
	Callback = function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.workspace.Lobby.brazil.portal.CFrame
                    end    
                })

Tab5:AddButton({
	Name = "Get court evidence badge",
	Callback = function()
fireclickdetector(game.Workspace.Lobby.Scene.knofe.ClickDetector)
                    end    
                })

Tab5:AddButton({
	Name = "Get duck badge",
	Callback = function()
fireclickdetector(game.Workspace.Arena["default island"]["Rubber Ducky"].ClickDetector)
                    end    
                })

Tab5:AddButton({
	Name = "Get The Lone Orange badge",
	Callback = function()
fireclickdetector(game.Workspace.Arena.island5.Orange.ClickDetector)
                    end    
                })

Tab3:AddToggle({
                    Name = "Anti Admins (Credits to R2O)",
                    Default = false,
                    Callback = function(bool)
antiAdmins = bool
    if bool == true then
        game.Players.PlayerAdded:Connect(function(Plr)
            if Plr:GetRankInGroup(9950771) and 2 <= Plr:GetRankInGroup(9950771) and antiAdmins then
                game.Players.LocalPlayer:Kick("Admin/High Rank Player Detected")
            end
        end)
    end
end
})

Tab3:AddToggle({
                    Name = "Anti Ragdoll (This will reset your character)",
                    Default = false,
                    Callback = function(Value)
if Value == true then
game.Players.LocalPlayer.Character.Humanoid.Health = 0
end
wait(4)
game.Players.LocalPlayer.Character:WaitForChild("Ragdolled").Changed:Connect(function()
if game.Players.LocalPlayer.Character:WaitForChild("Ragdolled").Value == true and Value == true then
repeat task.wait()
game.Players.LocalPlayer.Character.Torso.Anchored = true
until game.Players.LocalPlayer.Character:WaitForChild("Ragdolled").Value == false
game.Players.LocalPlayer.Character.Torso.Anchored = false
end
end)
                    end    
                })

               Tab3:AddToggle({
                    Name = "Anti Void",
                    Default = false,
                    Callback = function(Value)
game.Workspace.dedBarrier.CanCollide = Value
                    end    
                })

               Tab3:AddToggle({
                    Name = "Anti Death Barriers",
                    Default = false,
                    Callback = function(Value)
if Value == true then
for i,v in pairs(game.Workspace.DEATHBARRIER:GetChildren()) do
                    if v.ClassName == "Part" and v.Name == "BLOCK" then
                        v.CanTouch = false
                    end
                end
workspace.DEATHBARRIER.CanTouch = false
workspace.DEATHBARRIER2.CanTouch = false
workspace.dedBarrier.CanTouch = false
workspace.ArenaBarrier.CanTouch = false
workspace.AntiDefaultArena.CanTouch = false
else
for i,v in pairs(game.Workspace.DEATHBARRIER:GetChildren()) do
                    if v.ClassName == "Part" and v.Name == "BLOCK" then
                        v.CanTouch = true
                    end
                end
workspace.DEATHBARRIER.CanTouch = true
workspace.DEATHBARRIER2.CanTouch = true
workspace.dedBarrier.CanTouch = true
workspace.ArenaBarrier.CanTouch = true
workspace.AntiDefaultArena.CanTouch = true
end
                    end    
                })

               Tab3:AddToggle({
                    Name = "Anti Brazil",
                    Default = false,
                    Callback = function(Value)
if Value == true then
for i,v in pairs(game.Workspace.Lobby.brazil:GetChildren()) do
                    if v.ClassName == "Part" then
                        v.CanTouch = false
                    end
                end
else
for i,v in pairs(game.Workspace.Lobby.brazil:GetChildren()) do
                    if v.ClassName == "Part" then
                        v.CanTouch = true
                    end
                end
end
                    end    
                })

               Tab3:AddToggle({
                    Name = "Anti Cube of Death",
                    Default = false,
                    Callback = function(Value)
if Value == true then
        workspace.Arena.CubeOfDeathArea["the cube of death(i heard it kills)"].CanTouch = false
        else
                workspace.Arena.CubeOfDeathArea["the cube of death(i heard it kills)"].CanTouch = true
        end
                    end    
                })

               Tab3:AddToggle({
                    Name = "Anti Squid",
                    Default = false,
                    Callback = function(Value)
if Value == true then
        game.Players.LocalPlayer.PlayerGui.SquidInk.Enabled = false
        else
        game.Players.LocalPlayer.PlayerGui.SquidInk.Enabled = true
        end
                    end    
                })

               Tab3:AddToggle({
                    Name = "Anti Hallow Jack",
                    Default = false,
                    Callback = function(Value)
        if Value == true then
            game.Players.LocalPlayer.PlayerScripts.HallowJackAbilities.Disabled = true
        else
            game.Players.LocalPlayer.PlayerScripts.HallowJackAbilities.Enabled = true
        end
                    end    
                })

               Tab3:AddToggle({
                    Name = "Anti Conveyor",
                    Default = false,
                    Callback = function(Value)
        if Value == true then
            game.Players.LocalPlayer.PlayerScripts.ConveyorVictimized.Disabled = true
        else
            game.Players.LocalPlayer.PlayerScripts.ConveyorVictimized.Enabled = true
        end
                    end    
                })

               Tab3:AddToggle({
                    Name = "Anti Brick",
                    Default = false,
                    Callback = function(Value)
while Value == true do
for i,v in pairs(game.Workspace:GetChildren()) do
                    if v.Name == "Union" then
                        v.CanTouch = false
                    end
                end
task.wait()
end
                    end    
                })

               Tab3:AddToggle({
                    Name = "Anti [REDACTED]",
                    Default = false,
                    Callback = function(Value)
        if Value == true then
            game.Players.LocalPlayer.PlayerScripts.Well.Disabled = true
        else
            game.Players.LocalPlayer.PlayerScripts.Well.Enabled = true
        end
                    end    
                })

               Tab3:AddToggle({
                    Name = "Anti Za Hando (Credits to R2O)",
                    Default = false,
                    Callback = function(bool)
getgenv().AntiZaHando = bool
        if bool == true then
            while getgenv().AntiZaHando do
                wait(.001)
                for i,v in pairs(game.Workspace:GetChildren()) do
                    if v.ClassName == "Part" and v.Name == "Part" then
                        v:Destroy()
                    end
                end
            end
        end
                    end    
                })

               Tab3:AddToggle({
                    Name = "Anti Reaper (Credits to R2O)",
                    Default = false,
                    Callback = function(bool)
getgenv().AntiReaper = bool
        if bool == true then
            while getgenv().AntiReaper do
                wait(.001)
                for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
                    if v.Name == "DeathMark" then
                    game:GetService("ReplicatedStorage").ReaperGone:FireServer(game:GetService("Players").LocalPlayer.Character.DeathMark)
                    game:GetService("Lighting"):WaitForChild("DeathMarkColorCorrection"):Destroy() 
                    end 
                end
            end
        end
                    end    
                })

               Tab3:AddToggle({
                    Name = "Anti Pusher (Credits to R2O)",
                    Default = false,
                    Callback = function(bool)
getgenv().AntiPusher = bool
        if bool == true then
            while getgenv().AntiPusher do
                wait(.001)
                for i,v in pairs(game.Workspace:GetChildren()) do
                    if v.Name == "wall" then
                    v.CanCollide = false
                    end
                end
            end
        end
                    end    
                })

               Tab3:AddToggle({
                    Name = "Anti Booster (Credits to R2O)",
                    Default = false,
                    Callback = function(bool)
antiBooster = bool
        if bool == true then
            if game.Workspace[game.Players.LocalPlayer.Name]:FindFirstChild("BoosterObject", 1) then
                game.Workspace[game.Players.LocalPlayer.Name]:FindFirstChild("BoosterObject", 1):Destroy()
            end
            task.wait()
            game.Workspace[game.Players.LocalPlayer.Name].DescendantAdded:Connect(function(v)
                if antiBooster == true then
                    if v.Name == "BoosterObject" then
                        task.wait(.1)
                        v:Destroy()
                    end
                end
            end)
        end
                    end    
                })

               Tab3:AddToggle({
                    Name = "Anti Mail (Credits to R2O)",
                    Default = false,
                    Callback = function(bool)
antiMail = bool
        if bool == true then
            game.Players.LocalPlayer.PlayerGui.DescendantAdded:Connect(function(UI)
                if antiMail == true then
                    if UI.Name == "MailPopup" then
                        UI.Frame.Visible = false
                        task.wait()
                        game.Players.LocalPlayer.Character.Head.MailIcon:Destroy()
                    end
                end
            end)
        else
        if game.Players.LocalPlayer.PlayerGui:FindFirstChild("MailPopup") then
            game.Players.LocalPlayer.PlayerGui.MailPopup.Frame.Visible = true
            task.wait()
        end
        end
                    end    
                })

               Tab3:AddToggle({
                    Name = "Anti Stun (Credits to R2O)",
                    Default = false,
                    Callback = function(bool)
antiStun = bool
        if bool == true then
            while antiStun do
            task.wait()
            if game.Players.LocalPlayer.Character:FindFirstChild("Humanoid") and game.Players.LocalPlayer.Character.Humanoid.PlatformStand == true and not Farming and not allFarming and not game.Players.LocalPlayer.Character.Ragdolled.Value == true and game.Workspace:FindFirstChild("Shockwave") then
                game.Players.LocalPlayer.Character.Humanoid.PlatformStand = false
            end
            end
        end
                    end    
                })

               Tab3:AddToggle({
                    Name = "Anti Megarock/Custom (Credits to R2O)",
                    Default = false,
                    Callback = function(bool)
        AntiRock = bool
        if bool == true then
            while AntiRock do
                task.wait(.1)
        for _, Instance in pairs(game.Workspace:GetDescendants()) do
            if Instance.Name == "rock" and Instance.CanTouch == true then
                Instance.CanTouch = false
                Instance.CanQuery = false
            end
        end
            end
        else
        task.wait(.1)  
        for _, Instance in pairs(game.Workspace:GetDescendants()) do
            if Instance.Name == "rock" and Instance.CanTouch == false then
                task.wait()
                Instance.CanTouch = true
                Instance.CanQuery = true
            end
        end
        end
                    end    
                })
local Gloves = loadstring(game:HttpGet("https://raw.githubusercontent.com/ionlyusegithubformcmods/1-Line-Scripts/main/More%20Gloves.lua"))()
Player = game.Players.LocalPlayer.Character.Name
end
