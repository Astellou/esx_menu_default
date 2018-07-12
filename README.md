# esx_menu_default

source : https://github.com/ESX-Org/esx_menu_default
source : https://github.com/Parow/esx_menu_default

### How to use

Exemple : 

ESX.UI.Menu.Open(

	'default', GetCurrentResourceName(), 'shop',
	{
		css =  'default',
		title =  'Magasin',
		elements = elements
	},

	function(data, menu)
		TriggerServerEvent('esx_shop:buyItem', data.current.value, data.current.price)
	end,

	function(data, menu)
		menu.close()

		CurrentAction =  'shop_menu'
		CurrentActionMsg =  _U('press_menu')
		CurrentActionData = {zone = zone}
	end

)

