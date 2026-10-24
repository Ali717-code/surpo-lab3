# Лабораторная работа 3. Слияние и конфликты

### $ git merge dev
Auto-merging config.txt
CONFLICT (content): Merge conflict in config.txt
Automatic merge failed; fix conflicts and then commit the result.

### $ git status --short
UU config.txt

### $ cat config.txt
title: project
<<<<<<< HEAD
color: blue
=======
color: red
>>>>>>> dev
size: 10

Конфликт разрешён вручную: выбран компромиссный цвет purple.

### $ git log --oneline --graph --all
*   ec8208a Merge dev: конфликт разрешён вручную (color=purple)
|\  
| * 27470ed dev: color=red
* | 8de1729 master: color=blue
|/  
* 5f6366b initial

### $ cat config.txt
title: project
color: purple
size: 10
