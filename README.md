
# quick-ghsite

1. Crea un progetto in GitHub, ricordandoti di spuntare 'Inizializza il mio repository con u nfile README' 
2. Vai ai Settings del tuo nuovo progetto
3. Cerca Options -> GitHub Pages e in Source, scegli 'Master branch'. 

Adesso GitHub considererà il tuo branch master come un sito web accessibile con una url del tipo
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


Se quello che vedi corrisponde a quello che pensi git debba spedire su GitHub, aggiungi i file al cosiddetto _stage_ 
sul tuo computer:

```bash
git add .
```

Adesso che i file sono nello _stage_, puoi fare una 'specie di foto' dello stato del tuo progetto che resterà nello storico di git
con questo comando:

```bash
git commit -m "il mio primo commit"
```

Finora hai operato sul tuo computer, il prossimo passo è spedire i file su GitHub. Ma esattamente, dove e come?

Per scoprirlo, scrivi:

```bash
da@da-TravelMate-P238-M:~/Da/prj/quick-ghsite(gh-pages)$ git remote -v

```

Vedrai un output di questo tipo:

```bash
da@da-TravelMate-P238-M:~/Da/prj/quick-ghsite(gh-pages)$ git remote -v
origin  https://github.com/CoderDojoTrento/quick-ghsite.git (fetch)
origin  https://github.com/CoderDojoTrento/quick-ghsite.git (push)

```
Significa che il tuo repository sul tuo computer 'sa' che esiste un repository su GitHub all'indirizzo che vedi, e per 
usare quell'indirizzo puoi usare l'identificativo _origin_.


Adesso che hai trovato dove mandare il codice, puoi effettuare la 'spedizione' eseguendo il comando `git push`:

Il comanda manda il tuo branch corrente (master) al branch `master` che sta sul repository GitHub identificato da `origin` :

```bash
git push origin master
```






git remote add origin https://github.com/CoderDojoTrento/quick-ghsite.git
git push -u origin master


```


Adesso il sito dovrebbe essere disponibile a https://coderdojotrento.github.com/quick-ghsite