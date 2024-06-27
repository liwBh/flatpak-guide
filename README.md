# Flatpak Guia 
Flatpak es una tecnología para la distribución y ejecución de aplicaciones en Linux. Fue diseñado para proporcionar un entorno de sandbox seguro para aplicaciones, así como para permitir la distribución de software independiente de la distribución de Linux que estés utilizando. 

* [Flatpak oficial](https://flatpak.org/)

## Instalación de Flatpak
```
  sudo apt update
  sudo apt install flatpak
```

* Ver la versión de Flatpak
```
  flatpak --version
```

* Actualizar dependecias rotas
```
  sudo flatpak repair
```

* Actualizar la información de metadatos (appstream) de los remotos:
```
  flatpak update
  flatpak update --appstream
```

## Comandos de Flatpak

### Repositorios

* Listar remotos instalados
```
  flatpak remote-list
```

* Lista de remotos con información detallada
```
  flatpak remote-list -d
```

* Listar Aplicaciones de remotos
```
  flatpak remote-ls
```

* Agregar remotos
```
  flatpak remote-add --if-not-exists <nombre_remoto> <url>
```

* Modificar remotos, prioridad 1 es la más baja, influye en la prioridad de las aplicaciones
```
  flatpak remote-modify <nombre_remote> --prio <numero_prioridad>
```

* Actualizar remotos
```
  flatpak update 
``` 

* Eliminar remotos, se eliminan las aplicaciones instaladas de ese remoto
```
  flatpak remote-delete <nombre_remote>
```

* Eliminar remotos sin eliminar aplicaciones
```
  flatpak remote-delete --no-related <nombre_remote>
```

* Eliminar remotos sin eliminar aplicaciones y sin confirmación
```
  flatpak remote-delete --no-related --force <nombre_remote>
```

### Aplicaciones

* Listar aplicaciones instaladas
```
  flatpak list
```

* Buscar aplicaciones
```
  flatpak search <nombre_aplicacion>
```

* Instalar aplicaciones
```
  flatpak install <nombre_aplicacion>
```

* Listar Aplicaciones de remotos
```
  flatpak remote-ls
```

* Eliminar aplicaciones
```
  flatpak uninstall <nombre_aplicacion>
```

* Ejecutar aplicaciones
```
  flatpak run <nombre_aplicacion>
```

## Remotos de Flatpak

* Flathub: Es el repositorio oficial de Flatpak, en el se encuentran aplicaciones de todo tipo.
```
  flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

* Flathub Beta: Repositorio de aplicaciones en fase beta
```
  flatpak remote-add --if-not-exists flathub-beta https://flathub.org/beta-repo/flathub-beta.flatpakrepo
```

* KDE: Repositorio de aplicaciones de KDE
```
  flatpak remote-add --if-not-exists kdeapps --from https://distribute.kde.org/kdeapps.flatpakrepo
```

* Elementary: Repositorio de aplicaciones de Elementary OS
```
  flatpak remote-add --if-not-exists elementary --from https://flatpak.elementary.io/repo.flatpakrepo
```

* 

## Documentación Instalación Flathub

* [Flatpak](https://docs.flathub.org/docs/for-users/installation)