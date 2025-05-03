local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()

local Window = Fluent:CreateWindow({
    Title = "SniperX hub Alpha" .. Fluent.Version,
    TabWidth = 160, Size = UDim2.fromOffset(580, 460), Theme = "Dark"
})

local Tabs = {
Main = Window:AddTab({ Title = "scripts" }),
Settings = Window:AddTab({ Title = "Settings", Icon = "settings" })
}

Tabs.Main:AddParagraph({ Title = "Sniper hub", Content = "ABA SCRIPTS! Se os scripts não funcionarem é porque estão fora do ar!" })

Tabs.Main:AddButton({
Title = "Pulo Infinito",
Callback = function()
Fluent:Notify({
Title = "Carregando...",
Content = "Executando script: Pulo Infinito",
Duration = 3
})
loadstring(game:HttpGet("https://raw.githubusercontent.com/djmscript/infinite-jump/master/main.lua"))()
end
})

Tabs.Main:AddButton({
Title = "Infinite Yield",
Callback = function()
Fluent:Notify({
Title = "Carregando...",
Content = "Executando script: Infinite Yield",
Duration = 3
})
loadstring(game:HttpGet("https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source"))()
end
})


-- ATENÇÃO este script esta em CRIAÇÃO se caso algo acontecer com boce ou com sua conta bem o ploblema é seu recomendamos não usar até a SniperX hub Alpha test mudar para SniperX hub cmp
