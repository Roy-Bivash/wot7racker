# Useful Wargaming API Endpoints

- Get a List of Players Using a Search Query
Retrieve a list of players by providing a search query.

```bash
curl -X GET "https://api.worldoftanks.eu/wot/account/list/?application_id=${app_id}&search=${player_name}"
```

- Get a players details
```bash
curl -X GET "https://api.worldoftanks.eu/wot/account/info/?application_id=${app_id}&account_id=${player_id}"
```

- Get details/stats on all the vehicules played by the player
```bash
curl -X GET "https://api.worldoftanks.eu/wot/account/tanks/?application_id=${app_id}&account_id=${player_id}"
```

- Get all achievements details of a  player
```bash
curl -X GET "https://api.worldoftanks.eu/wot/account/achievements/?application_id=${app_id}&account_id=${player_id}"
```

- Get the list of all the vehicules in the game 
> [!NOTE]
> This method takes longer to respond, create a local database for later use of these data
```bash
curl -X GET "https://api.worldoftanks.eu/wot/encyclopedia/vehicles/?application_id=${app_id}"
```

- Get the vehicle configuration characteristics based on the specified module IDs
```bash
curl -X GET "https://api.worldoftanks.eu/wot/encyclopedia/vehicleprofile/ \
    ?application_id=${app_id} \
    &tank_id=${tank_id} \
    &engine_id=${engine_id} \
    &fields=${fields} \
    &gun_id=${gun_id} \
    &profile_id=${profile_id} \
    &radio_id=${radio_id} \
    &suspension_id=${suspension_id} \
    &turret_id=${turret_id}"
```