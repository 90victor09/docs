|stub| General
==============

Get Server Regions
------------------

Request
~~~~~~~

.. code-block:: http

    POST https://discordapp.com/api/voice/regions

Parameters
^^^^^^^^^^

Response
~~~~~~~~

An array of objects. Below is an example of a response with one location. There should be six objects, one for each server location: Amsterdam, London, Singapore, Sydney, US East, US West.

.. code-block:: json

    [
        {
            "sample_hostname": "us-west3.discord.gg",
            "sample_port": 80,
            "id": "us-west",
            "name": "US West"
        }
    ]



???
---

Request
~~~~~~~

.. code-block:: http

    PATCH https://discordapp.com/api/voice/ice

Parameters
^^^^^^^^^^

Response
~~~~~~~~

.. code-block:: json

    {
    }
    
Events
------------------

VOICE_STATE_UPDATE
~~~~~~~

Someone (including you) has joined the voice channel.

.. code-block:: json

    {
        "s": 1,
        "op": 0,
        "d": {
            "user_id": "11122233344455566",
            "suppress": false,
            "session_id": "aaaabbbbccccddddeeeeffffgggghhhh",
            "self_mute": false,
            "self_deaf": false,
            "mute": false,
            "guild_id": "11122233344455566",
            "deaf": false,
            "channel_id": "11122233344455566"
        }
    }

VOICE_SERVER_UPDATE
~~~~~~~

You have joined the voice channel.

.. code-block:: json

    {
        "s": 1,
        "op": 0,
        "d": {
            "token":"aaabbbcccdddeeef",
            "guild_id":"11122233344455566",
            "endpoint":"amsterdam13.discord.gg:80"
        }
    }
