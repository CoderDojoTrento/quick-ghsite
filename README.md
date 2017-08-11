
# quick-ghsite

1. Crea un progetto in GitHub, ricordandoti di crocettare 'Initialize this repository with a README' 
2. Vai ai Settings del tuo nuovo progetto
3. Cerca Options -> GitHub Pages e in Source, scegli 'Master branch'. 

Adesso GitHub considererà il tuo repository come un sito web accessibile con una url del tipo
https://coderdojotrento.github.io/quick-ghsite/

Fatto ! Già adesso puoi editare il file README.md direttamente online, e anche uploadare nuovi file come per esempio immagini.

Il README.md è scritto in formato MarkDown, e GitHub riuscirà automaticamente a convertirlo al volo in file html 
quando viene visualizzato online, ma naturalmente puoi anche scrivere direttamente file html da zero.


# Collegare il progetto sul tuo computer a GitHub

Se vuoi, puoi collegare il progetto sul tuo computer a GitHub. Per farlo, sul tuo computer apri la console e digita:

```bash
git clone https://github.com/CoderDojoTrento/altra-prova.git
```

mettendo la URL del progetto online che trovi cliccando sul pulsante verde 'Clone or download'

Adesso aggiungi dei file alla directory appena creata sul disco

Controlla cosa git pensa che tu abbia appena aggiunto:

```bash
git status
```


Se quello che vedi corrisponde a quello che pensi git debba spedire su GitHub, aggiungi i file al cosiddetto _stage_ , un posto 
'di transito' che risiede sul tuo computer:

```bash
git add .
```

Tipicamente nello 'stage' puoi aggiungere e togliere roba senza preoccuparti troppo delle conseguenze. Una volta che nello 
sviluppo raggiungi un punto fermo, in cui pensi di aver risolto almeno un piccolo problema, puoi fare una 'specie di foto'
 dello stato del tuo progetto che resterà nello storico di git sul tuo computer con questo comando:

```bash
git commit -m "il mio primo commit"
```

Finora hai operato sul tuo computer, il prossimo passo è spedire 'la foto del progetto' su GitHub. Ma esattamente, dove e come
spediamo il tutto?

Per scoprire il dove, scrivi:

```bash
git remote -v

```

Vedrai un output di questo tipo:

```bash

origin  https://github.com/CoderDojoTrento/quick-ghsite.git (fetch)
origin  https://github.com/CoderDojoTrento/quick-ghsite.git (push)

```
Significa che il repository sul tuo computer 'sa' che esiste un repository su GitHub all'indirizzo che vedi, e per 
usare quell'indirizzo puoi usare l'identificativo più corto _origin_


Adesso che hai trovato dove mandare 'la foto del progetto', puoi effettuare la 'spedizione' eseguendo il comando `git push`:

Il comanda manda il tuo branch corrente (master) al branch `master` che sta sul repository GitHub identificato da `origin` :

```bash
git push origin master
```


Adesso il sito dovrebbe essere disponibile ad una URL tipo https://coderdojotrento.github.com/quick-ghsite