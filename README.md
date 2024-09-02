
<h2>🛜 Rofi Network Manager</h2>
Rofi Network Manager is a utility that allows you to conveniently interact with wifi and ethernet networks. It uses nmcli to interact with networks, and rofi to display information.


<h2>🖼️ Review</h2>

![alt text](.meta/main-menu.png)
![alt text](.meta/selecting-wifi-network.png)
![alt text](.meta/wifi-network-management.png)

<h2>👨‍💻 Installation</h2>

1. Cloning the repository: `git clone https://github.com/meowrch/rofi-network-manager.git`
2. Go to the catalog: `cd ./rofi-network-manager`
3. Launching utilities: `sh network-manager.sh`
4. (Optional) For easy access, add the script somewhere in your $PATH.

<h2>⚙️ Polybar Configuration</h2>


```
[module/network-manager]
type = custom/script
interval = 3
exec = "sh PATH_TO_SCRIPT --status --enabled-color "#a6e3a1" --disabled-color "#f38ba8""
click-left = "sh PATH_TO_SCRIPT"
label = "%output%"
format-background = ${colors.sbg}
```

<h2>⚙️ Waybar Configuration</h2>

```
"custom/networkmanager": {
    "exec": "sh PATH_TO_SCRIPT --status --disabled-color \"#f38ba8\" --enabled-color \"#a6e3a1\" | cat",
    "return-type": "raw",
    "format": "{}  ",
    "interval": 3,
    "rotate": 0,
    "on-click": "sh PATH_TO_SCRIPT,
    "tooltip": false
},
```

<h2>📜 License</h2>

This project is released under the **MIT license**, which grants the following permissions:

- Commercial use
- Distribution
- Modification
- Private use

For more convoluted language, see the [**MIT License**](LICENSE)
