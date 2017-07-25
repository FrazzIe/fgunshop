# fgunshop
Another weapon shop for fivem....with gun licenses!

My gun part of the check inventory function...(Cops FiveM)

```lua
	MySQL.Async.fetchAll("SELECT * FROM gunshop WHERE identifier = '"..identifier.."'", { ['@username'] = identifier }, function (result)
		local strResult = "Weapons of " .. GetPlayerName(target) .. " : "
				
		for _, v in ipairs(result) do
			strResult = strResult .. v.weapon_name .. " - lvl "..v.licenselvl..", "
		end
		local probs = "Weapons of " .. GetPlayerName(target) .. " : "
		if strResult == probs then
			strResult = GetPlayerName(target).." has no weapons"
		end
		TriggerClientEvent("pNotify:SendNotification", source, {
            text = strResult,
            type = "error",
            queue = "left",
            timeout = 20000,
            layout = "centerRight"
        })
	end)
```

![alt text](https://image.prntscr.com/image/S9IY01I9Rmu1ueZOn3unPw.png "Main UI")
![alt text](https://image.prntscr.com/image/T5DpoNDFTmmje8lQOm399w.png "Level 4 submenu")
![alt text](https://image.prntscr.com/image/EiddsIFRS8yD_B79QugacA.png "Sell guns")
![alt text](https://image.prntscr.com/image/bMf3_CVrTiy8e9Pyz4xmFQ.png "Main UI for buying a license")
![alt text](https://image.prntscr.com/image/_QU9At90SYWlEztBPv_ENg.png "Some pNotify stuff")
