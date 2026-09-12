# Primer Lab de Arquitectura de Software
- Asignatura: IS488 Arquitectura de Software
- Semestre: 2025-I
- Docente: Ing. Luis Adderlin RUIZ HUAMAN
### Sesión: 01 – Configuración del entorno, repositorio y caso de estudio

#### OBJETIVOS DE APRENDIZAJE
Al finalizar esta práctica, el estudiante estará en capacidad de:

• Reconocer la importancia del control de versiones en el ciclo de vida del software.

• Explicar el funcionamiento de Git como sistema de control de versiones distribuido.

• Utilizar los principales comandos de Git para gestionar repositorios locales y remotos.

• Integrar GitHub como plataforma de colaboración para el trabajo en equipo.

• Aplicar buenas prácticas en la gestión de ramas, commits, pull requests y resolución de
conflictos.

### Procesos en Git
 
LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1
$ git config --global user.name "Arascely"

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1
$ git config --global user.email "grissel.rodriguez.27@unsch.edu.pe"

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1
$ git init
Initialized empty Git repository in C:/Users/LABORATORIO/Documents/TallerLab1/.git/

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1 (main)
$ git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1 (main)
$ mkdir GitTaller

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1 (main)
$ cd GitTaller

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (main)
$ git config --global init.defaultBranch main


LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1 (main)
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        GitTaller/

nothing added to commit but untracked files present (use "git add" to track)

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1 (main)
$ echo "#ATallerGit" > README.md

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1 (main)
$ git atatus
git: 'atatus' is not a git command. See 'git --help'.

The most similar command is
        status

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1 (main)
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        GitTaller/
        README.md

nothing added to commit but untracked files present (use "git add" to track)

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1 (main)
$ cd GitTaller
LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (main)
$  echo "#ATallerGit" > README.md

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (main)
$ git add .
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (main)
$ git commit -m "primer commit"
[main (root-commit) 71ef38c] primer commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (main)
$ git remote add origin https://github.com/Arascely/TallerGit.git
error: remote origin already exists.

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (main)
$ git branch -M main

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (main)
$ git push -u origin main
info: please complete authentication in your browser...
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 233 bytes | 233.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Arascely/TallerGit.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (main)
$ git branch
* main

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (cv)
$ git commit -m "Agregar CV"
On branch cv
nothing to commit, working tree clean

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (cv)
$ git push -u origin cv
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'cv' on GitHub by visiting:
remote:      https://github.com/Arascely/TallerGit/pull/new/cv
remote:
To https://github.com/Arascely/TallerGit.git
 * [new branch]      cv -> cv
branch 'cv' set up to track 'origin/cv'.


LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (cv)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (main)
$ git log --oneline
71ef38c (HEAD -> main, origin/main, origin/cv, cv) primer commit

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (main)
$ git log
commit 71ef38cddc9622feb242e4f1e05c60fd8936165e (HEAD -> main, origin/main, origin/cv, cv)
Author: Arascely <grissel.rodriguez.27@unsch.edu.pe>
Date:   Sat Sep 12 10:10:28 2026 -0500

    primer commit
LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (main)
$ git add README.md
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (main)
$ git commit -m "Actualizacion de archivos"
[main cbe8951] Actualizacion de archivos
 2 files changed, 28 insertions(+), 1 deletion(-)
 create mode 100644 index.html

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (main)
$ git push origin main
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 16 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 862 bytes | 862.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Arascely/TallerGit.git
   71ef38c..cbe8951  main -> main

LABORATORIO@DESKTOP-KASER4E MINGW64 ~/Documents/TallerLab1/GitTaller (main)
$ git log
commit cbe8951c6b8ef16f6fa41f68bcc61035b055926a (HEAD -> main, origin/main)
Author: Arascely <grissel.rodriguez.27@unsch.edu.pe>
Date:   Sat Sep 12 10:59:04 2026 -0500

    Actualizacion de archivos

commit 71ef38cddc9622feb242e4f1e05c60fd8936165e (origin/cv, cv)
Author: Arascely <grissel.rodriguez.27@unsch.edu.pe>
Date:   Sat Sep 12 10:10:28 2026 -0500

:
commit cbe8951c6b8ef16f6fa41f68bcc61035b055926a (HEAD -> main, origin/main)
Author: Arascely <grissel.rodriguez.27@unsch.edu.pe>
Date:   Sat Sep 12 10:59:04 2026 -0500

    Actualizacion de archivos

commit 71ef38cddc9622feb242e4f1e05c60fd8936165e (origin/cv, cv)
Author: Arascely <grissel.rodriguez.27@unsch.edu.pe>
Date:   Sat Sep 12 10:10:28 2026 -0500

:
commit cbe8951c6b8ef16f6fa41f68bcc61035b055926a (HEAD -> main, origin/main)
Author: Arascely <grissel.rodriguez.27@unsch.edu.pe>
Date:   Sat Sep 12 10:59:04 2026 -0500

    Actualizacion de archivos

commit 71ef38cddc9622feb242e4f1e05c60fd8936165e (origin/cv, cv)
Author: Arascely <grissel.rodriguez.27@unsch.edu.pe>
Date:   Sat Sep 12 10:10:28 2026 -0500

:
commit cbe8951c6b8ef16f6fa41f68bcc61035b055926a (HEAD -> main, origin/main)
Author: Arascely <grissel.rodriguez.27@unsch.edu.pe>
Date:   Sat Sep 12 10:59:04 2026 -0500

    Actualizacion de archivos

commit 71ef38cddc9622feb242e4f1e05c60fd8936165e (origin/cv, cv)
Author: Arascely <grissel.rodriguez.27@unsch.edu.pe>
Date:   Sat Sep 12 10:10:28 2026 -0500

    primer commit
~
~
~
~
~
~
~
~
~
(END)
commit cbe8951c6b8ef16f6fa41f68bcc61035b055926a (HEAD -> main, origin/main)
Author: Arascely <grissel.rodriguez.27@unsch.edu.pe>
Date:   Sat Sep 12 10:59:04 2026 -0500

    Actualizacion de archivos

commit 71ef38cddc9622feb242e4f1e05c60fd8936165e (origin/cv, cv)
Author: Arascely <grissel.rodriguez.27@unsch.edu.pe>
Date:   Sat Sep 12 10:10:28 2026 -0500

    primer commit
~
~
~
~
~
~
~
~
~
~
(END)
commit cbe8951c6b8ef16f6fa41f68bcc61035b055926a (HEAD -> main, origin/main)
Author: Arascely <grissel.rodriguez.27@unsch.edu.pe>
Date:   Sat Sep 12 10:59:04 2026 -0500

    Actualizacion de archivos

commit 71ef38cddc9622feb242e4f1e05c60fd8936165e (origin/cv, cv)
Author: Arascely <grissel.rodriguez.27@unsch.edu.pe>
Date:   Sat Sep 12 10:10:28 2026 -0500

    primer commit
~
~
~
~
~
~
~
~
~
~
~
(END)
commit cbe8951c6b8ef16f6fa41f68bcc61035b055926a (HEAD -> main, origin/main)
Author: Arascely <grissel.rodriguez.27@unsch.edu.pe>
Date:   Sat Sep 12 10:59:04 2026 -0500

    Actualizacion de archivos

commit 71ef38cddc9622feb242e4f1e05c60fd8936165e (origin/cv, cv)
Author: Arascely <grissel.rodriguez.27@unsch.edu.pe>
Date:   Sat Sep 12 10:10:28 2026 -0500

    primer commit
~
~
~
~
~
~
~
~
~
~
~
~
~
(END)

 
