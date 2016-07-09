MinePass API
============

Player API
----------

The player API is designed for services to query a list of worlds and servers a player has access to.
Game launchers auto-populating a list of multi-player servers would be a prime example.

**Using the API**

Submit a GET request to ``https://api.minepass.net/player-api/v1/info`` using HTTP authentication.
Use the **Player's IGN** as the username, and the **API KEY** from the player's dashboard as the password.

**Sample Response**::

  {
    player: {
      uuid: '119d15fe-566e-45e4-b467-fba85a707310',
      name: 'johndoe',
      realm: 'os',
      worlds: [
        {
          name: 'World 1',
          uuid: 'c76ef9c7-dbf6-4232-9c0b-5e7e827f644b',
          pass_name: 'Visitor',
          pass_code: 'V',
          role_name: 'World Moderator',
          role_code: 'A02',
          servers: [
            {
              name: 'Server #1',
              address: 'mc-1234.gamr.link'
            }
          ]
        }
      ]
    }
  }
