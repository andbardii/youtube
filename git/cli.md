# Tutti i Comandi da Terminale - Corso Git Italiano Lezione 05

- Configurazione di Git

git config --global user.name "il-tuo-nome"     Configura il nome utente per i commit.
git config --global user.email "la-tua-email"   Configura l'email dell'utente.


- Gestione del repository

git clone "url-repo"                            Clona un repository remoto sul computer locale.
git init                                        Inizializza un nuovo repository Git locale.
git status                                      Mostra lo stato delle modifiche nel repository.
git add "file"                                  Aggiunge un file all’area di staging.
git add .                                       Aggiunge tutti i file all'area di staging.
git commit -m "messaggio-commit"                Crea un commit con un messaggio descrittivo.
git log                                         Mostra la cronologia dei commit.
git show "commit-id"                            Mostra i dettagli di un commit specifico.


- Gestione dei branch

git branch                                      Elenca tutti i branch locali.
git branch -r                                   Elenca tutti i branch locali e remoti.
git branch "nome-branch"                        Crea un nuovo branch.
git checkout "nome-branch"                      Passa a un branch esistente.
git checkout -b "nome-branch"                   Crea e passa a un nuovo branch.
git merge "nome-branch"                         Unisce un branch specificato con il branch attuale.
git branch -d "nome-branch"                     Elimina un branch.


- Sincronizzazione con un repository remoto

git remote add origin "url-repo"                Aggiunge un repository remoto e lo chiama "origin".
git fetch                                       Scarica gli aggiornamenti dal repository remoto.
git pull                                        Scarica e unisce gli aggiornamenti dal repository remoto.
git push origin "nome-branch"                   Carica i commit locali sul repository remoto.


- Gestione delle modifiche

git diff                                        Mostra le differenze con l’ultima versione.
git reset "file"                                Rimuove un file dall’area di staging.
git reset --hard                                Reset della directory di lavoro e della sua storia.


- Ripristino delle modifiche

git checkout -- "file"                          Ripristina un file modificato all'ultima versione.
git revert "commit-id"                          Crea un nuovo commit che ne annulla uno precedente.


- Rimozione dei file

git rm "file"                                   Rimuove un file dalla directory e dall’area di staging.
git rm --cached "file"                          Rimuove un file dallo staging, mantenendolo in locale.


- Stashing delle modifiche

git stash                                       Salva temporaneamente le modifiche non committate.
git stash apply                                 Applica le modifiche salvate dallo stash.
git stash drop                                  Elimina lo stash applicato.
