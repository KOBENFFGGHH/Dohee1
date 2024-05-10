Shop:Dropdown("Select Melee", ---ของUi
{
    "Black Leg [$150,000 Beli]",
    "Electro [$550,000 Beli]",
    "Fishman Karate [$750,000 Beli]",
    "Dragon Claw [$1,500 Fragments]",
    "Superhuman [$3,000,000 Beli]",
    "Death Step [$5,000 Fragments + $5,000,000 Beli]",
    "Sharkman Karate [$5,000 Fragments + $2,500,000 Beli]",
    "Electric Claw [$5,000 Fragments + $3,000,000 Beli]",
    "Dragon Talon [$5,000 Fragments + $3,000,000 Beli]",
    "God Human [$5,000 Fragments + $5,000,000 Beli]",
    "Sanguine Art [$5,000 Fragments + $5,000,000 Beli]"
    }
, function(value)---ของUi

        _G.SelectMelee = value

end)---ของUi

Shop:Button("Buy Selected Melee", function()--ของUi

    if _G.SelectMelee == "Black Leg [$150,000 Beli]" then
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBlackLeg")
    elseif _G.SelectMelee == "Electro [$550,000 Beli]" then
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectro")
    elseif _G.SelectMelee == "Fishman Karate [$750,000 Beli]" then
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyFishmanKarate")
    elseif _G.SelectMelee == "Dragon Claw [$1,500 Fragments]" then
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","1")
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","2")
    elseif _G.SelectMelee == "Superhuman [$3,000,000 Beli]" then
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySuperhuman")
    elseif _G.SelectMelee == "Death Step [$5,000 Fragments + $5,000,000 Beli]" then
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep")
    elseif _G.SelectMelee == "Sharkman Karate [$5,000 Fragments + $2,500,000 Beli]" then
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate",true)
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate")
    elseif _G.SelectMelee == "Electric Claw [$5,000 Fragments + $3,000,000 Beli]" then
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectricClaw")
    elseif _G.SelectMelee == "Dragon Talon [$5,000 Fragments + $3,000,000 Beli]" then
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDragonTalon")
    elseif _G.SelectMelee == "God Human [$5,000 Fragments + $5,000,000 Beli]" then
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyGodhuman")
    elseif _G.SelectMelee == "Sanguine Art [$5,000 Fragments + $5,000,000 Beli]" then
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySanguineArt", true)
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySanguineArt")
    end

end)---ของui
