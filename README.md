local textChatService = game:GetService("TextChatService")

				textChatService.OnIncomingMessage = function(message: TextChatMessage)

					local properties = Instance.new("TextChatMessageProperties")
					if message.TextSource then

						local player = game:GetService("Players"):GetPlayerByUserId(message.TextSource.UserId)

						properties.PrefixText = "<font color='#008000'>[Lumin User (PE)]</font> " .. message.PrefixText
					end
					return properties
				end
