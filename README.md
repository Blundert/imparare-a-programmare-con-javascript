<!-- omit in toc -->
# Imparare a programmare con Javascript

Lavorando nel mondo della programmazione ed essendo io stesso uno sviluppatore, spesso e volentieri, mi sono imbattuto ad insegnare alcune cose a persone di diverso livello di conoscenza sul tema. \
Non mi sono mai però approcciato nello spiegare _tutta_ la programmazione ad un neofita che non ne  conosce nulla a riguardo. \
Con questo documento voglio spiegare tutti i concetti base della [programmazione](https://it.wikipedia.org/wiki/Programmazione_(informatica)) utilizzando come linguaggio di riferimento Javascript.

- [Perché Javascript](#perché-javascript)
- [Come scrivere ed eseguire un programma](#come-scrivere-ed-eseguire-un-programma)
  - [Comandi base del terminale](#comandi-base-del-terminale)
  - [Il primo programma: Hello world!](#il-primo-programma-hello-world)
- [Input ed output](#input-ed-output)
- [Tipi predefiniti e variabili](#tipi-predefiniti-e-variabili)
  - [Condizionale](#condizionale)
  - [Cicli while](#cicli-while)
    - [Esercizi](#esercizi)
  - [Cicli for](#cicli-for)
  - [Array](#array)
- [Bibliografia](#bibliografia)

## Perché Javascript

Ho scelto di utilizzare [Javascript](https://it.wikipedia.org/wiki/JavaScript) per spiegare la programmazione per 3 semplici motivi - non del tutto razionali: 

1. è il linguaggio di programmazione che utilizzo principlamente a lavoro;
1. ha una curva di apprendimento molto veloce;
1. ci sono molte risorse online di facile fruizione che possono aiutare a comprendere meglio il linguaggio. Per citarne qualcuna: [w3schools](https://www.w3schools.com/js/default.asp); [MDN](https://developer.mozilla.org/it/docs/Web/JavaScript).

## Come scrivere ed eseguire un programma

Questa guida non è orientata al WEB ma solamente alla programmazione. Utilizzeremo Javascript solamente per studiarne i principi. Quindi, gli strumenti che utilizzeremo saranno:

1. un ambiente di sviluppo integrato (in lingua inglese integrated development environment) cioè un software che ci supporterà nella scrittura dei programmi. In particolare, utilizzeremo [Visual Studio Code](https://code.visualstudio.com/#alt-downloads);
1. [Node.js](https://nodejs.org/it/download/) è una runtime di JavaScript [Open source](https://it.wikipedia.org/wiki/Open_source) multipiattaforma orientato agli eventi per l'esecuzione di codice JavaScript, costruita sul motore JavaScript V8 di Google Chrome. Che tradotto significa: Node.js è un programma che ci permette di eseguire programmi scritti con il liguaggio di programmazione Javascript senza l'utilizzo di un browser. 
1. La [shell o terminale](https://it.wikipedia.org/wiki/Shell_(informatica)) è un programma dotato di un'interfaccia a riga di comando, che viene eseguito all'interno di un [terminale testuale](https://it.wikipedia.org/wiki/Terminale_virtuale). L'utente digita un comando, ovvero richiede l'esecuzione di un programma, e il programma eseguito può interagire con l'utente e/o mostrare dati sul terminale. Noi utilizzeremo la shell per eseguire i nostri programmi, per inserire informazioni nei nostri programmi e per vedere l'esecuzione di questi. 

> Installiamo Visual Studio Code e Node.js prima di passare al prossimo paragrafo. 

### Comandi base del terminale

Nei principali sistemi operativi ([Linux](https://it.wikipedia.org/wiki/Linux), [MacOS](https://it.wikipedia.org/wiki/MacOS) e [Windows](https://it.wikipedia.org/wiki/Windows_10)) è possibile utilizzare la shell dei comandi in modo nativo, perciò senza dove installare nulla oltre a quando proposto di default. 
Per accedere al teminale è necessario: 

- Windows 10: fare clic con il tasto destro del mouse sul menu Start e nel menù a discesa selezionare Windows PowerShell;
- MacOS 10.15: fare clic sull’icona Launchpad nel Dock, scrivere Terminale nel campo di ricerca, quindi fare clic su Terminale;
- Linux ([Ubuntu](https://it.wikipedia.org/wiki/Ubuntu)): fare clic sul pulsante Dash (il pulsante Dash è posizionato nell'angolo superiore sinistro del desktop ed è caratterizzato dal logo di Ubuntu). Digitare la parola chiave terminale, quindi fare clic su Terminale. 

Comandi comuni tra tutti i teminali: 
- `pwd`: vedere il percorso corrente in cui il terminale è posizionato;

### Il primo programma: Hello world!

Una volta installati Visual Studio Code (da ora abbreviato VSC) e Node.js (da ora semplicemente node) saremo pronti per scrivere il nostro primo programma. 

1. Aprire VSC;
1. Nel menù File selezionare New File;
1. Scrivere il seguente testo (da ora in poi il testo che contiene codice sarà indicato come _codice_):
```javascript
var helloWorld = "Hello world!";

console.log(helloWorld);
```
4. Salviamo il file in una posizione che ci aggrada con il nome `hello-world.js`. Fare attenzione all'estenzione `.js`;
1. Aprire il terminale utilizzando quello incorporato con VSC (che non fa altro che utilizzare uno di quelli spiegati sopra): nello stesso menù di File, selezionare invece Terminal e poi fare clic su New Terminal. Si aprirà il prompt dei comandi sotto il file di testo che abbiamo scritto posizionato in una cartella. Per essere consapevoli del path completo eseguire il comando `pwd`. 
1. Utilizzando i comandi spiegati nel paragrafio sopra, ci posizioniamo nella stessa cartella in cui abbiamo salvato il file `hello-world.js`. 
1. Scriviamo il seguente comando nel terminale: 
```
> node hello-world.js
```
8. Vedremo stampato (modo gergale informatico per dire visualizzato) in una nuova riga la stringa 
```
> Hello world!
```

## Input ed output

I programmi devono poter scambiare informazioni con l'esterno ed a questo servono le operazioni di lettura e stampa, dette di [input/output](https://it.wikipedia.org/wiki/Input/output) e abbreviate in i/o.

Un programma comunica con l'esterno per mezzo di dispositivi molto diversi: in un computer moderno, l'input standard è la tastiera, l'output standard è lo schermo, ma un programma potrebbe poter scrivere o leggere da un dispositivo USB o da CD o DVD o semplicemente da un file nella memoria del computer o anche un file che risiede nella memoria di qualche altro computer raggiungibile d quello su cui il programma esegue.

Come abbiamo visto nell'esercizio precedente:

```javascript
var helloWorld = "Hello world!";

console.log(helloWorld);
```

viene fatto utilizzo di `console.log` per poter stampare a video la scritta `Hello world!`. [Console.log](https://developer.mozilla.org/it/docs/Web/API/Console/log) non è altro che un metodo per poter eseguire l'operazione di output del nostro programma. 

Come si può notare non è possibile cambiare o inserire una nuova stringa senza prima modificare il programma, in pratica non è possibile utilizzare l'operazione di input.

Scriviamo un nuovo programma che stampa a video un saluto seguito dal nome di una persona, che andremo a salvare con il nome di `hello.js`. 

```javascript
var myArgs = process.argv.slice(2);
var nomeDellaPersona = myArgs[0];

console.log("Ciao", nomeDellaPersona, "!");
```

Andremo a scrivere poi nel seguente modo il comando nel terminale: 

```
> node hello.js <stringa che vogliamo inserire come parametro>
```
nel concreto:
```
> node hello.js Matteo
```
Dopo l'esecuzione vedremo stampato: 
```
> Ciao Matteo !
```
Se eseguiremo lo stesso comando con un nome diverso, per esempio Leonardo al posto di Matteo vedremo stampato: 
```
> Ciao Leonardo !
```

In questo modo possiamo leggere un parametro dal terminale. Per leggerene più di uno, sarà necessario modificare il nostro programma ancora e cambiare la sintassi dell'esecuzione del comando. \
In particolare, per inserire nel comando più di una parola basta separare i parametri con uno spazio:
```
> node hello.js Matteo Leonardo Alberto
```

Scriviamo un nuovo programma che stampa a video un il nome della persona seguito dalla sua età. Entrambi questi valori saranno letti come input. Andremo a salvare con il file con il nome di `age.js`. 

```javascript
var myArgs = process.argv.slice(2);
var nomeDellaPersona = myArgs[0];
var etaDellaPersona = myArgs[1];

console.log(nomeDellaPersona, "ha la seguente età:", etaDellaPersona);
```

Poniamo particolare attenzione alle righe: 
```javascript
var myArgs = process.argv.slice(2);
var nomeDellaPersona = myArgs[0];
var etaDellaPersona = myArgs[1];
```

`myArgs` è una variabile di tipo `array` (che faremo nei prossimi paragrafici) alla quale vengono assegnati tutti i valori scritti come parametro nell'esecuzione del programma. Per ora ci basta sapere che se richiamata con la seguente sintassi: `myArgs[n]` con `n` il numero del valore sarà possibile ottenere dentro il programma il valore scritto come parametro. 

Facciamo un esempio per spiegare meglio questo concetto: 
```
> node mio-programma.js one two three four
```

myArgs conterrà:
```javascript
myArgs:  [ "one", "two", "three", "four" ]
```

Nel mio programma potrò ottenere i parametri facendo:
```javascript
var parametroUno = myArgs[0]; // "one"
// ...
var parametroQuattro = myArgs[0]; // "four"
```

## Tipi predefiniti e variabili

...

## Istruzioni di base 

...

### Condizionale

...

### Cicli while

...

#### Esercizi

Una serie di esercizi sui cicli while. 

1. Dati due numeri interi, calcolare il quoziente e il resto supponendo che l'esecutore non sappia fare la divisione.

### Cicli for

...

### Array

...

<!-- omit in toc -->
## Algortmi

...

<!-- omit in toc -->
## Funzioni

...

<!-- omit in toc -->
## Ricorsione

...

<!-- omit in toc -->
## Alberi

...

<!-- omit in toc -->
## Programmazione funzionale

...

<!-- omit in toc -->
## Programmazione ad oggetti

...

## Bibliografia

Link utili:

1. https://it.wikipedia.org/wiki/Programmazione_(informatica)
1. https://it.wikipedia.org/wiki/JavaScript
1. https://it.wikipedia.org/wiki/Integrated_development_environment
1. https://it.wikipedia.org/wiki/Open_source
1. https://it.wikipedia.org/wiki/Node.js
1. https://www.laramind.com/blog/cose-un-terminale-accedere-da-mac-e-da-windows/
1. https://it.wikipedia.org/wiki/Terminale_(informatica)
1. https://it.wikipedia.org/wiki/Terminale_virtuale
1. https://it.wikipedia.org/wiki/Shell_(informatica)
1. https://it.admininfo.info/c-mo-abrir-powershell-en-windows-10
1. https://support.apple.com/it-it/guide/terminal/apd5265185d-f365-44cb-8b09-71a064a42125/mac
1. https://www.libreriaprogetto.it/web/libro/9000000000055.php
1. https://www.math.unipd.it/~gilberto/
1. https://it.wikipedia.org/wiki/Input/output
1. https://developer.mozilla.org/it/docs/Web/API/Console/log
1. https://nodejs.org/en/knowledge/command-line/how-to-parse-command-line-arguments/

<!-- omit in toc -->
#### Utility di scrittura

In questo paragrafo mi annoto le utility di Markdown utilizzate in questo documento: 

#

##

###

####

1.
1.


```javascript
```

```bash
```

Link utili: 
1. https://github.com/yzhang-gh/vscode-markdown