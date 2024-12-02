function Notify(...)
    V1 = {...};
    spawn(function()
        V2 = game.CoreGui:FindFirstChild("Notification");
        if V2 then
            V2:Destroy();
        end
        
        V3 = Instance.new("ScreenGui");
        V3.Name = "Notification";
        V3.Parent = game.CoreGui;

        if protect_gui then
            protect_gui(V3);
        end
        
        V4 = Instance.new("TextLabel", V3);
        V4.Text = V1[1];
        V4.Size = UDim2.new(0, 200, 0, 50);
        V4.Position = UDim2.new(0.5, -100, 1, -50);
        V4.BackgroundColor3 = Color3.fromRGB(30, 30, 30);
        V4.TextColor3 = Color3.new(1, 1, 1);
        V4.BackgroundTransparency = 0.5;

        Instance.new("UICorner", V4).CornerRadius = UDim.new(0, 6);
        cloneref(game:GetService("TweenService")):Create(
            V4,
            TweenInfo.new(0.5, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
            {Position = UDim2.new(0.5, -100, 0.9, -25)}
        ):Play();

        wait(V1[2]);
        V3:Destroy();
    end);
end;

function Sound(...)
    V1 = {...};
    V2 = Instance.new("Sound");
    V2.SoundId = "rbxassetid://" .. V1[1];
    V2.Parent = game.CoreGui;
    V2.Volume = V1[2];
    V2:Play();
end;
