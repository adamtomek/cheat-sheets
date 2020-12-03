# Git Cheat Sheet 1.10
* [Odložení](#odložení)
    * [Zobrazení všech odložení](#zobrazení-všech-odložení)
    * [Odložení aktuálních souborů](#odložení-aktuálních-souborů)
    * [Obnovení z odložení](#obnovení-z-odložení)
    * [Odstranění z odložení](#odstranění-z-odložení)
    * [Vytvoření nové větve z obnovení z odložení](#vytvoření-nové-větve-z-obnovení-z-odložení)
* [Tagy](#tagy)
    * [Vytvoření tagu](#vytvoření-tagu)
    * [Nahrání tagu na remote](#nahrání-tagu-na-remote)
    * [Smazání tagu](#smazání-tagu)
* [Větve](#větve)
    * [Smazání větve](#smazání-větve)
* [Vzdálený repozitář](#vzdálený-repozitář)
    * [Zobrazení všech vzdálených repozitářů](#zobrazení-všech-vzdálených-repozitářů)

## Odložení
### Zobrazení všech odložení
```
$ git stash list
```
### Odložení aktuálních souborů
```
$ git stash save <optional_message>
```
### Obnovení z odložení
##### Obdnovení z posledního odložení
```
$ git stash apply
```
##### Obdnovení z daného odložení
```
$ git stash apply stash@{<number_of_stash>}
```
##### Obdnovení z posledního odložení včetně smazání z odložení
```
$ git stash drop
```
##### Obdnovení z daného odložení včetně smazání z odložení
```
$ git stash drop stash@{<number_of_stash>}
```
### Odstranění z odložení
```
$ git stash drop stash@{<number_of_stash>}
```
### Vytvoření nové větve z obnovení z odložení
##### Vytvoření nové větve z obnovení z posledního odložení
```
$ git stash branch <branch_name>
```
##### Vytvoření nové větve z obnovení z daného odložení
```
$ git stash branch <branch_name> stash@{<number_of_stash>}
```

## Tagy
### Vytvoření tagu
##### Vytvoření lokálního tagu
```
$ git tag <tag_name>
```
### Nahrání tagu na remote
##### Nahrání daného tagu na remote
```
$ git push <remote_name> <tag_name>
```
##### Nahrání všech tagů
```
$ git push --tags
```
### Smazání tagu
##### Smazání lokálního tagu
```
$ git tag --delete <tag_name>
```
##### Smazání tagu z remote
```
$ git push --delete <remote_name> <tag_name>
```

## Větve
### Smazání větve
##### Smazání lokální větve
```
$ git branch -d <branch_name>
```
##### Smazání větve z remote
```
$ git push <remote_name> --delete <branch_name>
```
nebo
```
$ git push <remote_name> :<branch_name>
```

## Vzdálený repozitář
### Zobrazení všech vzdálených repozitářů
```
$ git remote -v
```
