# [PROJECT CONTINUES HERE @ Re-Ignited-Phone](https://github.com/Re-Ignited-Development/Re-Ignited-Phone)

---

---

---

### [Downloads page](https://github.com/9SEC/gcphone/releases)

<h2 align="center">Phone for FiveM</h2>

![Image of gcphone1](https://i.imgur.com/naTiBgI.png)
![Image of gcphone2](https://i.imgur.com/LAicovK.png)
![Image of gcphone3](https://i.imgur.com/imWPohA.png)
![Image of gcphone4](https://i.imgur.com/rzWdDMy.png)
![Image of gcphone5](https://i.imgur.com/9h7eiI8.png)

## Features

-   Contact list
-   Sending sms
-   Voice call
-   Anonymous call
-   Bank application
-   Anonymous Chat application
-   Stock exchange application
-   Customizable shell / wallpaper
-   . . .

## Configuration

### Edit file /html/static/config/config.json

```json
{
    "//": "Network name located in the phone bar",
    "reseau": "9SEC",

    "//": "Basic phone color",
    "themeColor": "#303f9f",

    "//": "List of colors for contacts",
    "colors": [
        "#EF5350",
        "#EC407A",
        "#AB47BC",
        "#7E57C2",
        "#5C6BC0",
        "#42A5F5",
        "#29B6F6",
        "#26C6DA",
        "#26A69A",
        "#66BB6A",
        "#9CCC65",
        "#D4E157",
        "#FFCA28",
        "#FFA726",
        "#FF7043",
        "#8D6E63",
        "#78909C"
    ],

    "//": "If false, add a '-' in the number (###-###)",
    "useFormatNumberFrance": false,

    "//": "useWebRTCVocal: false => Appels avec channels de GTA",
    "//": "useWebRTCVocal: true  => Appels avec WebRTC",
    "useWebRTCVocal": true,

    "//": "Configuration of TURN servers to be used",
    "RTCConfig": {
        "iceServers": [
            {
                "urls": ["turn:gannon.ovh"],
                "username": "john",
                "credential": "pass"
            }
        ]
    },

    "//": "List of available wallpapers, location => /html/static/img/background",
    "background": {
        "Calvin & Hobbes": "back001.jpg",
        "Destiny": "back002.jpg",
        "Stormtrooper": "back003.jpg",
        "Custom URL": "URL"
    },
    "//": "Default wallpaper",
    "background_default": {
        "label": "Calvin & Hobbes",
        "value": "back001.jpg"
    },

    "//": "List of available hulls, location => /html/static/img/coque",
    "coque": {
        "Sansumg S8": "s8.png",
        "Iphone X": "iphonex.png",
        "Brick Base": "base.png",
        "Transparent": "transparent.png"
    },
    "//": "Default shell",
    "coque_default": {
        "label": "Sansumg S8",
        "value": "s8.png"
    },

    "//": "Configuration of service calls (Favorite)",
    "serviceCall": [
        {
            "//": "Item name",
            "display": "Police",

            "//": "Optional: Chip color",
            "backgroundColor": "red",

            "//": "Optional: Image of the chip",
            "icon": "/html/static/img/icons_app/bank.png",

            "//": "List of actions available",
            "subMenu": [
                {
                    "//": "Title of the action",
                    "title": "Send a message",

                    "//": "Name of the event trigger in use",
                    "eventName": "esx_addons_gcphone:call",

                    "//": "Optional: 'data' parameter sent with the event",
                    "type": {
                        "number": "police"
                    }
                },
                {
                    "title": "Call the switchboard",
                    "eventName": "gcphone:autoCallNumber",
                    "type": {
                        "number": "911"
                    }
                }
            ]
        },
        {
            "display": "Ambulance",
            "backgroundColor": "red",
            "subMenu": [
                {
                    "title": "Send a message",
                    "eventName": "esx_addons_gcphone:call",
                    "type": {
                        "number": "ambulance"
                    }
                }
            ]
        }
    ],

    "//": "Add default contacts",
    "defaultContacts": [
        {
            "number": "ambulance",
            "display": "AABBUULLAANNCCEE",
            "icon": "/html/static/img/icons_app/bank.png"
        },
        {
            "number": "police",
            "display": "Police",
            "backgroundColor": "blue",
            "letter": "J"
        }
    ],

    "//": "Application configuration",
    "apps": [
        {
            "//": "Application name",
            "name": "Phone",

            "//": "Application icons",
            "icons": "/html/static/img/icons_app/call.png",

            "//": "Application route, DO NOT MODIFY",
            "routeName": "appels",

            "//": "If true, the application will be available on the home page",
            "inHomePage": true,

            "//": "If false, the application is not visible",
            "enabled": true
        },
        {
            "name": "Messages",
            "icons": "/html/static/img/icons_app/sms.png",
            "routeName": "messages",
            "inHomePage": true,

            "//": "Reference to the store, to display a chip under the app icon",
            "puceRef": "nbMessagesUnread"
        },
        {
            "name": "Contacts",
            "icons": "/html/static/img/icons_app/contacts.png",
            "routeName": "contacts",
            "inHomePage": true
        },
        {
            "name": "Settings",
            "icons": "/html/static/img/icons_app/settings.png",
            "routeName": "parametre",
            "inHomePage": true
        },
        {
            "name": "Bank",
            "icons": "/html/static/img/icons_app/bank.png",
            "routeName": "bank",
            "inHomePage": false
        },
        {
            "name": "Exchange",
            "icons": "/html/static/img/icons_app/bourse.png",
            "routeName": "bourse",
            "enabled": true
        },
        {
            "name": "Photo",
            "icons": "/html/static/img/icons_app/photo.png",
            "routeName": "photo"
        },
        {
            "name": "Dark Chat",
            "icons": "/html/static/img/icons_app/tchat.png",
            "routeName": "tchat"
        }
    ],

    "//": "Phone languages configuration",
    "language": {
        "fr_FR": {
            "NAME": "Français",
            "KEY": "VALUE"
        },
        "en_US": {
            "NAME": "English",
            "//": "..."
        },
        "//": "Autre Langue"
    }
}
```

_Don't forget to add the new files in the \_\_ressource.lua_

-   You can change the sounds in \html\static\sound
-   The shells must be in 1000x500px format, The screen area is centered in size 800\*400
-   The Bank & Stock Exchange applications are to be configured according to your scripts

### Fixed telephones can be configured in gcphone/config.lua

```LUA
--[[
  Faites attention à ne pas utiliser un numéro qui entre en conflit avec un joueur
--]]
FixePhone = {
  -- Poste de police
  ['911'] = { name =  "Central Police", coords = { x = 441.2, y = -979.7, z = 30.58 } },

  -- Cabine proche du poste de police
  ['008-0001'] = { name = "Telephone booth", coords = { x = 372.25, y = -965.75, z = 28.58 } },
}
```

## About esx_addons_gcphone

Used to make the connection between the telephone and the esx trades.

Please put esx_addons_gcphone & gcphone before jobs.
Example:

```yml
# ...

start mysql-async
start essentialmode
start esplugin_mysql
start es_extended

start esx_addons_gcphone
start gcphone

start esx_mecanojob
start esx_job2
start esx_job3
# ...
```

## License

[GNU v3](https://opensource.org/licenses/gpl-3.0.html)

9SEC
