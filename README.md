# BDCraft

> [!IMPORTANT]
> If you encounter any Bugs, errors, or you are simply confused, join the [Ballsdex Developers Discord](https://discord.gg/QyHVf4bxqW) and ask for help in the #3rd-party-support channel.

> [!Tip]
> Read howtouse.txt to understand how to use this package.

BDCraft is a Ballsdex package forked from @Mitoooooooopo's Ballsdex crafting package.

## BDCraft vs Crafting-package-BD

Here is a list of differences between BDCraft and the original repository:

1. DexI support
2. Bulk commands
3. Revamped menus
4. Code improvements.

## Installation

### DexI

You can install BDCraft with DexI.

```bash
dexi add Dotsian/Crafting-BD
```

### Manual

#### Step 1

copy the folder `crafting` to your `BallsDex-DiscordBot/ballsdex/packages`

#### Step 2 
open your config.yml scroll down until your see 
`packages` and add it there 
![IMG_20250506_154729](https://github.com/user-attachments/assets/c035eeaf-642d-4630-a5df-aaca6edb58ea)

#### Step 3 
Open your `__main__.py` and edit the 
```py
TORTOISE_ORM = {
    "connections": {"default": os.environ.get("BALLSDEXBOT_DB_URL")},
    "apps": {
        "models": {
            "models": ["ballsdex.core.models"],
            "default_connection": "default",
        },
    },
}
```

To reflect the models in crafting folder ![IMG_20250506_155944](https://github.com/user-attachments/assets/412695ee-d6ca-4f29-bb28-9aa08167b978)

#### Step 4 
copy the folder named `craftings` in to your `BallsDex-DiscordBot/admin_panel` 
![IMG_20250506_161115](https://github.com/user-attachments/assets/3ce13bce-ffd5-4fc3-8754-cad022660036)

Adding screenshot to avoid any confusion

#### Step 5 
Open your `BallsDex-DiscordBot/admin_panel/admin_panel/settings` open `local.py` and add this line 
```py
INSTALLED_APPS.append("craftings")
```
Then at your base admin_panel folder,
Run  

```py
docker compose exec admin-panel python3 manage.py makemigrations craftings
```
Then 

```py
docker compose exec admin-panel python3 manage.py migrate craftings
```
![Screenshot_2025-05-08-15-07-05-36](https://github.com/user-attachments/assets/b78825a4-8076-4c6f-873e-ced65451e7e2)


And Your Done 
> [!IMPORTANT]
> any issue regarding this part feel to dm me or ping me 
