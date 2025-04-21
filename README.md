# OS_USER
Avant de compiler et lancer le projet, il faut avoir installé les dépendances suivantes :

- gcc

- SDL2

- SDL2_image

- SDL2_ttfp

- thread

- Homebrew

Sous Debian/Ubuntu :

```sudo apt install libsdl2-dev libsdl2-image-dev libsdl2-ttf-dev build-essential```

sous macOS avec Homebrew :

```brew install sdl2 sdl2_image sdl2_ttf```

et maintenant il faut aller dans le dossier concerné et :

pour compiler le serveur :

```gcc -o server server.c```

pour compiler le client : 

```gcc -o sh13 sh13.c `sdl2-config --cflags --libs` -lSDL2_image -lSDL2_ttf -pthread```


pour lancer le serveur : 

```./server 1234```

pour lancer les clients : 

```./sh13 127.0.0.1 1234 127.0.0.1 2000 joueur1```

```./sh13 127.0.0.1 1234 127.0.0.1 2001 joueur2```

```./sh13 127.0.0.1 1234 127.0.0.1 2002 joueur3```

```./sh13 127.0.0.1 1234 127.0.0.1 2003 joueur4```
