local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
local InterfaceManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/InterfaceManager.lua"))()

-- Criação da janela com tecla de minimizar
local Window = Fluent:CreateWindow({
    Title = "Sniper Hub alpha version " .. Fluent.Version,
    TabWidth = 160,
    Size = UDim2.fromOffset(580, 460),
    Theme = "Dark",
    MinimizeKey = Enum.KeyCode.LeftControl
})

-- Tabs
local Tabs = {
    Main = Window:AddTab({ Title = "scripts" }),
    Settings = Window:AddTab({ Title = "Settings", Icon = "settings" })
}

-- Interface flutuante (ícone de reabrir)
InterfaceManager:SetLibrary(Fluent)
InterfaceManager:SetFolder("SniperHub") -- pasta onde as configs são salvas
InterfaceManager:BuildInterfaceSection(Tabs.Settings)
InterfaceManager:ApplyToWindow(Window)

-- Aviso inicial
Tabs.Main:AddParagraph({ Title = "Sniper hub", Content = "ABA SCRIPTS! Se os scripts não funcionarem é porque estão fora do ar!" })

-- Botão: Pulo Infinito
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

-- Botão: Infinite Yield
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

