-- Load Infinite Yield
loadstring(game:HttpGet('https://githubusercontent.com'))()

-- Wait for it to load, then run commands
task.wait(5) 
local IY = game:GetService("CoreGui"):WaitForChild("IY")

-- Replace 'fly' and 'noclip' with your preferred commands
game:GetService("Players").LocalPlayer.Chatted:Connect(function(msg) end) -- Placeholder
game:GetService("VirtualUser"):CaptureController()

-- Method to run commands automatically
local function runCmd(cmd)
    fireSignal(game:GetService("CoreGui").IY.Main.CommandBar.Focused)
    game:GetService("CoreGui").IY.Main.CommandBar.Text = cmd
    task.wait(0.1)
    -- This part varies by version, but most IY versions use a command bar focus method.
end

runCmd("fly")
runCmd("noclip")

