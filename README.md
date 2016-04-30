# Overview

With botarena you can run your [warlight1](http://theaigames.com/competitions/warlight-ai-challenge) bot wherever you want and get fast feedback as to whether or not you've improved it or not.

# Launch convention

botarena does not autodetect the runtime environment for your bot. You must provide a `run.sh` script that knows how to launch your bot.

# Solo play

TODO This is broken right now it seems.

This will run your bot against a normal map with only neutral enemies. See how many rounds it takes your bot to conquer the entire map.

    go run arena.go <path_to_run_script>

# Head to head play

This will run two of your bots against each other.

    go run arena.go <path_to_run_script> <path_to_run_script>

You can run the java starter bot against itself by doing this:

    go run arena.go startbot.sh startbot.sh

# Game visualisation

It works like this (sudo is for listening on port 80)

    sudo go run viewer.go
    open http://localhost/competitions/warlight-ai-challenge/games/5724205d4ca80151322b5e57

# Implementation notes

The fight resolution logic assumes the worst luck for the attacker. TODO make it probabilistic to match the actual game?