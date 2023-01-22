local server = require(script.MainModule)
game.Players.PlayerAdded:Connect(function(player)
	local settings = {
		["General"] = {
			Prefix = ":"
		},
		["Ranks"] = {
			Moderators = {},
			Administrators = {},
			Owners = {},
			Creators = {"blvckjakey"},
		}
		
	}
	spawn(function()
		server.run(player, settings)
	end)
end)
