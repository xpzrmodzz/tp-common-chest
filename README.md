-- Script pour téléporter le joueur à workspace.Chests.Common
local function teleportToCommonChest()
    -- Vérifie si le coffre commun existe
    local commonChest = workspace.Chests:FindFirstChild("Common")
    
    if commonChest then
        -- Obtient la position du coffre commun
        local chestPosition = commonChest.Position

        -- Téléporte le joueur à la position du coffre commun
        game.Players.LocalPlayer.Character:MoveTo(chestPosition)
    else
        warn("Le coffre commun n'a pas été trouvé dans workspace.Chests.")
    end
end

-- Appelle la fonction pour se téléporter
teleportToCommonChest()
