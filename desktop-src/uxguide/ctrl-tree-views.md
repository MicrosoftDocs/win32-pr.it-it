---
title: Visualizzazioni albero
description: Con una visualizzazione albero, gli utenti possono visualizzare e interagire con una raccolta di oggetti disposti gerarchicamente, usando una selezione singola o più selezioni.
ms.assetid: f0206485-e028-41d8-9be2-5d59f0a0b677
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ade51b421350dc90bf72e2ff1a683bf1d352f7c1
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524495"
---
# <a name="tree-views"></a>Visualizzazioni albero

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Con una visualizzazione albero, gli utenti possono visualizzare e interagire con una raccolta di oggetti disposti gerarchicamente, usando una selezione singola o più selezioni.

In un albero, gli oggetti che contengono dati sono denominati nodi foglia e gli oggetti che contengono altri oggetti sono denominati nodi contenitore. Un singolo nodo contenitore di primo livello è denominato nodo radice. Gli utenti possono espandere e comprimere i nodi contenitore facendo clic sui pulsanti di espansione più e meno.

![Screenshot della visualizzazione albero di Esplora risorse ](images/ctrl-tree-views-image1.png)

Visualizzazione albero tipica.

> [!Note]  
> Le linee guida [relative al layout](vis-layout.md) e ai [menu](cmd-menus.md) sono presentate in articoli separati.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

**La presenza di dati gerarchici non significa che è necessario usare una visualizzazione albero.** Molto spesso una [visualizzazione elenco](ctrl-list-views.md) è una scelta più semplice, ma più potente. Visualizzazioni elenco:

-   Supporto di diverse visualizzazioni.
-   Supporto dell'ordinamento dei dati in base a una delle colonne nella visualizzazione Dettagli.
-   Supportare l'organizzazione dei dati in gruppi, formando una gerarchia a due livelli.

**Per usare una visualizzazione elenco, è possibile appiattire le informazioni gerarchiche usando le tecniche seguenti:**

-   Rimuovere il nodo radice, se presente, perché spesso non è necessario.
-   Usare gruppi di visualizzazione elenco, schede, [elenchi a](/windows/desktop/uxguide/ctrl-drop)discesa o intestazioni [espandibili](glossary.md) per sostituire i contenitori di primo livello.

    ![Screenshot dei gruppi di visualizzazione elenco contenenti elenchi ](images/ctrl-tree-views-image2.png)

    In questo esempio i gruppi di visualizzazione elenco vengono usati per i contenitori di primo livello.

    ![Screenshot delle schede usate per i contenitori di primo livello ](images/ctrl-tree-views-image3.png)

    In questo esempio le schede vengono usate per i contenitori di primo livello

    ![Screenshot dell'elenco a discesa usato come contenitore ](images/ctrl-tree-views-image4.png)

    In questo esempio viene usato un elenco a discesa per i contenitori di primo livello.

-   Se un controllo associato visualizza il contenuto del contenitore selezionato, tale controllo può visualizzare i livelli inferiori della gerarchia.

    ![Screenshot del riquadro del sommario ](images/ctrl-tree-views-image5.png)

    In questo esempio i contenitori di basso livello vengono visualizzati nella finestra del documento.

**È necessario usare una visualizzazione albero se è necessario visualizzare una gerarchia di più di due livelli (senza includere il nodo radice).**

Per decidere se una visualizzazione albero è il controllo più opportuno, considerare queste domande:

-   **I dati sono gerarchici?** Se non è così, usa un altro controllo.
-   **La gerarchia ha almeno tre livelli (senza includere la radice)?** In caso contrario, prendere in considerazione alternative, ad esempio gruppi di visualizzazione elenco, schede, elenchi a discesa o intestazioni espandibili.
-   **Gli elementi hanno dati ausiliari?** In tal caso, è consigliabile usare una visualizzazione elenco in modalità di visualizzazione Dettagli per sfruttare appieno i dati ausiliari.
-   **I dati di livello inferiore sono correlati a sottoattività indipendenti?** In tal caso, è consigliabile visualizzare le informazioni in un controllo associato o in una finestra separata (visualizzata tramite pulsanti [di comando](ctrl-command-buttons.md) o [collegamenti).](ctrl-command-links.md)
-   **Gli utenti di destinazione sono avanzati?** Gli utenti avanzati sono più esperti nell'uso degli alberi. Se l'applicazione è destinata a utenti non esperti, evitare di usare le visualizzazioni albero.
-   **Gli elementi hanno un'unica categorizzazione gerarchica naturale e familiare alla maggior parte degli utenti?** In tal caso, i dati sono ideali per una visualizzazione albero. Se sono necessarie più visualizzazioni o ordinamenti, usare invece una visualizzazione elenco.
-   **Gli utenti devono visualizzare i dati di livello inferiore in alcuni scenari, ma non in tutti, ma non sempre?** In tal caso, i dati sono ideali per una visualizzazione albero.

> [!Note]  
> In alcuni casi un controllo simile a una visualizzazione albero viene implementato usando una visualizzazione elenco. In questi casi, applicare le linee guida in base all'utilizzo, non all'implementazione.

 

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Gli alberi sono concepiti per organizzare i dati e semplificare l'individuazione, ma è difficile rendere facilmente individuabili i dati all'interno di un albero. Quando si decidono le visualizzazioni albero e l'organizzazione, tenere presenti i principi seguenti.

### <a name="predictability-and-discoverability"></a>Prevedibilità e individuabilità

**Una visualizzazione albero è basata sulle relazioni tra gli oggetti.** Gli alberi funzionano meglio quando gli oggetti formano una relazione chiara, nota e che si escludono a vicenda in cui ogni oggetto viene mappato a un singolo contenitore facile da determinare.

**Un problema significativo è che un oggetto può essere visualizzato in nodi diversi.** Ad esempio, dove gli utenti si aspettano di trovare un dispositivo hardware che riproduce musica, ha un disco rigido di grandi dimensioni e usa una porta USB? Ad esempio, in uno dei diversi nodi contenitore, ad esempio Multimediali, Archiviazione, USB ed eventualmente in Risorse hardware. Una soluzione consiste nell'inserire ogni oggetto nel singolo contenitore più appropriato indipendentemente dalle circostanze; un altro approccio consiste nell'inserire ogni oggetto in tutti i contenitori applicabili. Il primo promuove una gerarchia semplice e pulita e il secondo promuove l'individuabilità, ognuno dei quali presenta vantaggi e potenziali problemi.

**Gli utenti potrebbero non comprendere completamente il layout dell'albero, ma formeranno un modello psichico delle relazioni dopo aver interagito con l'albero per un po' di tempo.** Se il modello psichiale non è corretto, si genera confusione. Si supponga, ad esempio, che un lettore musicale sia disponibile nei contenitori Multimediali, Archiviazione e USB. Questa disposizione migliora l'individuabilità. Se un utente trova per la prima volta il dispositivo in Contenuti multimediali, può concludere che tutti i dispositivi, ad esempio i lettori musicali, vengono visualizzati nel contenitore Multimedia. L'utente si aspetta quindi che dispositivi simili, ad esempio fotocamere digitali, vengano visualizzati nel contenitore Multimedia e, in caso contrario, si confonde.

**La sfida nella progettazione di un albero consiste nel bilanciare l'individuabilità con un modello utente prevedibile che riduce al minimo la confusione.**

### <a name="breadth-vs-depth"></a>Ampiezza e profondità

Gli studi sull'usabilità hanno dimostrato che gli utenti hanno maggiore successo nella ricerca di oggetti in un albero ampio rispetto **a** un albero che è profondo, pertanto quando si progetta un albero è preferibile la navigazione rispetto alla profondità. Idealmente, un albero non deve avere più di quattro livelli (senza contare il nodo radice) e gli oggetti a cui si accede più di frequente devono essere visualizzati nei primi due livelli.

### <a name="other-principles"></a>Altri principi

-   Quando gli utenti trovano ciò che cercano, smettino di cercare. Non vengono cercati per vedere dove potrebbe essere trovato un oggetto perché non è necessario. Questi utenti possono presupporre che il primo percorso trovato sia l'unico.
-   Gli utenti hanno difficoltà a trovare oggetti in alberi complessi di grandi dimensioni. Gli utenti non eseguiranno una ricerca manuale e esaustiva per trovare gli oggetti in tali alberi; si fermano quando si pensa di aver expended un impegno ragionevole. Di conseguenza, gli alberi complessi di grandi dimensioni devono essere integrati con altri metodi di accesso, ad esempio la ricerca di parole, un indice o il filtro.
-   Alcuni programmi consentono agli utenti di creare alberi personalizzati. Anche se questi alberi auto-progettati potrebbero essere allineati con il modello psichico dell'utente, vengono spesso creati in modo infafago e non gestiti correttamente. Ad esempio, mentre un file system, un programma di posta elettronica e un elenco Preferiti archiviano in genere tipi simili di informazioni, gli utenti raramente si preoccupano di organizzarli nello stesso modo.

**Se si fa una sola cosa...**

Valutare attentamente i vantaggi e gli svantaggi dell'uso delle visualizzazioni albero. Disporre dati disposti gerarchicamente non significa che è necessario usare una visualizzazione albero.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le visualizzazioni albero hanno diversi modelli di utilizzo:



| Utilizzo                           |    Esempio                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Visualizzazioni albero con solo nodi contenitore**<br/> gli utenti possono visualizzare e interagire con un contenitore alla volta. <br/>                        | In genere, a queste visualizzazioni albero è associato un controllo che visualizza il contenuto del contenitore selezionato, in modo che gli utenti possano interagire con un solo contenitore alla volta. <br/> ![Screenshot del riquadro contenitore e del riquadro contenuto ](images/ctrl-tree-views-image6.png)<br/> In questo esempio la visualizzazione albero include solo nodi contenitore. Il contenuto del nodo selezionato viene visualizzato nel controllo visualizzazione elenco associato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Visualizzazioni albero con contenitore e nodi foglia**<br/> gli utenti possono visualizzare e interagire con contenitori e file.<br/>                       | In genere, a queste visualizzazioni albero è associato un controllo che visualizza il contenuto del contenitore o della foglia selezionata. Consentendo agli utenti di interagire con le foglia spesso è necessario supportare la selezione multipla. <br/> ![Screenshot del riquadro della visualizzazione albero e del riquadro del contenuto ](images/ctrl-tree-views-image7.png)<br/> In questo esempio la visualizzazione albero include sia nodi contenitore che nodi foglia. Poiché la selezione multipla è supportata, il contenuto degli elementi aperti viene visualizzato usando [le schede](ctrl-tabs.md) nel controllo associato.<br/> in alternativa, la visualizzazione albero può avere un elenco organizzato, in cui i contenitori sono intestazioni e le foglia sono opzioni. <br/> ![Screenshot della visualizzazione albero con intestazioni e opzioni ](images/ctrl-tree-views-image8.png)<br/> In questo esempio le foglia dell'albero sono opzioni e i contenitori sono categorie di opzioni.<br/> |
| **Visualizzazioni albero delle caselle di controllo**<br/> gli utenti possono selezionare un numero qualsiasi di elementi, incluso nessuno.<br/>                                             | Le caselle di controllo indicano chiaramente che è possibile selezionare più elementi. usare questo modello di albero quando la selezione multipla è essenziale o comune. <br/> ![Screenshot della visualizzazione albero con caselle di controllo ](images/ctrl-tree-views-image9.png)<br/> In questo esempio, una visualizzazione albero di caselle di controllo consente di attivare o disattivare la selezione delle funzionalità.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Generatori di visualizzazione albero**<br/> Gli utenti possono creare un albero aggiungendo un contenitore o una foglia alla volta e impostando facoltativamente l'ordine.<br/> | Molti alberi possono essere creati o modificati dagli utenti. alcuni alberi vengono creati usando i menu di scelta rapida e il trascinamento della selezione (ad esempio le cartelle in Esplora finestre), mentre altri alberi vengono creati usando una finestra di dialogo specializzata, ad esempio l'elenco Preferiti in Windows Internet Explorer. <br/> ![Screenshot della finestra di dialogo Preferiti ](images/ctrl-tree-views-image10.png)<br/> In questo esempio da Internet Explorer, gli utenti possono creare un proprio elenco di Preferiti usando una finestra di dialogo.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| **Visualizzazioni albero con metodi di accesso alternativi**<br/> gli utenti possono trovare oggetti in modi diversi dall'uso di un albero gerarchico.<br/>        | Come accennato in precedenza, gli utenti hanno difficoltà a trovare oggetti in alberi complessi di grandi dimensioni, quindi tali alberi devono essere integrati con altri metodi di accesso, ad esempio una ricerca di parole, un indice o un filtro. <br/> ![Screenshot del contenuto, dell'indice e delle schede Preferiti ](images/ctrl-tree-views-image11.png)<br/> In questo esempio, gli utenti possono anche accedere alle informazioni usando un sommario, un indice e i Preferiti. Per alcuni utenti, le schede indice e ricerca possono essere più utili rispetto alla scheda contenuto.<br/> ![Screenshot del menu Start e della casella di ricerca di Windows ](images/ctrl-tree-views-image12.png)<br/> In questo esempio, Windows menu Start consente anche agli utenti di accedere a programmi, file e pagine Web digitando parte del nome nella casella di ricerca.<br/>                                                                                                             |



 

## <a name="guidelines"></a>Indicazioni

### <a name="presentation"></a>Presentazione

-   **All'interno di un contenitore ordinare gli elementi in un ordine logico.** Ordinare i nomi in ordine alfabetico, i numeri in ordine numerico e le date in ordine cronologico.
-   **Usare l'attributo Mostra sempre selezione** in modo che gli utenti possano determinare rapidamente l'elemento selezionato, anche quando il controllo non ha lo stato attivo per l'input.
-   **Se l'albero funge da sommario, usare l'attributo Espansione singola per semplificare la gestione dell'albero.** In questo modo, viene espansa solo la parte pertinente dell'albero.
-   **Evitare di presentare alberi vuoti.** Se un utente crea un albero, inizializzare l'albero con istruzioni o elementi di esempio che potrebbero essere necessari agli utenti.

    ![Screenshot dell'elenco preferiti di Internet Explorer ](images/ctrl-tree-views-image13.png)

    In questo esempio l'elenco viene inizialmente presentato con esempi.

-   **Non rendere comprimibile i nodi contenitore se gli utenti non hanno alcun motivo per comprimerli.** In questo modo si aggiunge una complessità non necessaria.
-   **Se le prestazioni del carico sono un problema, visualizzare solo i contenitori di primo e secondo livello dell'albero per impostazione predefinita.** È quindi possibile caricare dati aggiuntivi su richiesta quando un utente espande i rami nell'albero.
-   **Se gli** utenti espandono o comprendono un contenitore, rendere persistente tale stato in modo che venga reso attivo alla successiva visualizzazione albero, a meno che gli utenti non preferiscano iniziare con lo stato predefinito. La persistenza deve essere basata su una visualizzazione per albero, per utente.
-   **Se i contenitori di alto livello hanno contenuti simili, è consigliabile usare gli indizi visivi per differenziarli.**

    **Non corretto:**

    ![Screenshot degli elementi di Outlook con icone diverse ](images/ctrl-tree-views-image14.png)

    In questo esempio, le cartelle Cassetta postale e Archivio hanno contenuto simile. Dopo l'ulteriore espansione degli alberi, è molto difficile per gli utenti sapere dove si trova nell'albero, con una confusione. L'uso di icone leggermente diverse nelle diverse sezioni risolverebbe questo problema.

-   **Riconsiderare le linee di connessione.** Anche se queste righe mostrano chiaramente le relazioni tra i nodi contenitore e foglia, aggiungono confusione visiva senza facilitare in modo significativo la comprensione. In particolare, non sono utili quando i nodi sono vicini tra loro, né aiutano quando i nodi sono così distanti che è necessario lo scorrimento.

    **Corretto:**

    ![Screenshot della visualizzazione albero con linee di connessione ](images/ctrl-tree-views-image15.png)

    **Migliore:**

    ![Screenshot della visualizzazione albero senza connettere le linee ](images/ctrl-tree-views-image16.png)

    Le linee di connessione fanno poco per facilitare la comprensione.

### <a name="interaction"></a>Interazione

-   **Valutare la possibilità di fornire il comportamento del doppio clic.** Il doppio clic dovrebbe avere lo stesso effetto della selezione di un elemento e dell'esecuzione del comando predefinito.
-   **Rendere ridondante il comportamento del doppio clic.** Deve essere sempre presente un pulsante di comando o un comando del menu di scelta rapida che ha lo stesso effetto.
-   Se un elemento richiede ulteriori spiegazioni, **fornire la spiegazione in un infotip**.

    ![Screenshot dei Preferiti con suggerimento per un elemento ](images/ctrl-tree-views-image17.png)

    In questo esempio, un infotip fornisce altre informazioni.

-   **Fornire menu di scelta rapida dei comandi pertinenti.** Tali comandi includono Taglia, Copia, Incolla, Rimuovi o Elimina, Rinomina e Proprietà.
-   **Quando si disabilita una visualizzazione albero, disabilitare anche le etichette e i pulsanti di comando associati.**

### <a name="tree-organization"></a>Organizzazione albero

-   **Usare una struttura gerarchica naturale familiare alla maggior parte degli utenti.**
-   **Se non è possibile usare una struttura di questo tipo, provare a bilanciare l'individuabilità con un modello utente prevedibile che riduce al minimo la confusione.**
-   **Per migliorare in modo sicuro l'individuabilità, inserire un elemento in più contenitori quando:**
    -   L'elemento non è correlato ad altri elementi simili, pertanto gli utenti non vengono confusi da associazioni non corrette.
    -   Esistono solo alcuni di questi elementi con ridondanza (quindi l'albero non diventa gonfio).
-   **Usare la struttura gerarchica più semplice che funzioni correttamente.** A tale scopo, procedere nel seguente modo:
    -   Posizionare gli oggetti a cui si accede più di frequente nei primi due livelli dell'albero (senza contare il nodo radice) e posizionare gli oggetti a cui si accede meno di frequente più in basso nella gerarchia.
    -   Eliminare i contenitori di livello intermedio ridondanti o combinarli.
-   **Preferire l'ampiezza rispetto alla profondità.** Idealmente, un albero non deve avere più di quattro livelli e gli oggetti a cui si accede più di frequente devono essere visualizzati nei primi due livelli.
-   **Determinare se è effettivamente necessario un nodo radice.** Fornire un nodo radice se gli utenti necessitano della possibilità di eseguire comandi sull'intero albero (possibilmente usando un menu di scelta rapida nel nodo radice). In caso contrario, l'albero è più semplice e facile da usare senza di esso.
-   **Se l'albero ha metodi di accesso alternativi, ad esempio una ricerca di parole o un indice, ottimizzare l'albero per l'esplorazione concentrandosi sul contenuto più utile.** Con metodi di accesso alternativi, il contenuto dell'albero non deve essere completo. Semplificare l'albero rende più semplice per gli utenti trovare il contenuto più utile.

### <a name="check-box-tree-views"></a>Visualizzazioni albero delle caselle di controllo

-   **Visualizzare il numero di elementi selezionati sotto l'elenco,** soprattutto se è probabile che gli utenti selezionano più elementi. Questo feedback consente agli utenti di confermare che la selezione è corretta.

    ![Screenshot del numero di elementi selezionati ](images/ctrl-tree-views-image18.png)

    In questo esempio il numero di elementi selezionati viene visualizzato sotto l'albero . È chiaro che due elementi non sono selezionati.

-   Se sono presenti potenzialmente molti elementi e la selezione o la cancellazione di tutti gli elementi è probabile, aggiungere Seleziona tutto e Cancella tutti i pulsanti di comando.
-   **Usare le caselle di controllo a stato misto per indicare la selezione parziale degli elementi in un contenitore.**

    **Corretto:**

    ![Screenshot della finestra con caselle di controllo con stato misto ](images/ctrl-tree-views-image19.png)

    In questo esempio le caselle di controllo dello stato misto vengono usate per indicare la selezione parziale.

## <a name="recommended-sizing-and-spacing"></a>Dimensioni e spaziatura consigliate

![Screenshot del ridimensionamento e della spaziatura della visualizzazione ad albero ](images/ctrl-tree-views-image20.png)

Dimensioni e spaziatura consigliate per i controlli visualizzazione albero.

-   **Scegliere una larghezza della visualizzazione albero che eviti la necessità** di scorrimento orizzontale per la maggior parte degli elementi quando l'albero è completamente espanso.
-   **Includere un ulteriore 30% per supportare la localizzazione.**
-   **Scegliere un'altezza della visualizzazione albero che elimini lo scorrimento verticale non necessario.** È consigliabile rendere leggermente più lunga una visualizzazione albero (o anche di più se è disponibile spazio) in caso di riduzione della necessità di una barra di scorrimento verticale.

    **Non corretto:**

    ![Screenshot del controllo visualizzazione struttura ad albero breve e stretto ](images/ctrl-tree-views-image21.png)

    In questo esempio, rendere la visualizzazione albero leggermente più ampia e più lunga eliminerebbe le barre di scorrimento nella maggior parte dei casi. In questo particolare albero è possibile aprire un solo contenitore alla volta.

-   **Se gli utenti traggono vantaggio dall'estensione della visualizzazione albero, rendere ridimensionabile la visualizzazione albero e la relativa finestra padre.** In questo modo, gli utenti possono modificare le dimensioni della visualizzazione albero in base alle esigenze.

## <a name="labels"></a>Etichette

### <a name="control-labels"></a>Etichette di controllo

-   Tutte le visualizzazioni albero necessitano di etichette. Scrivere l'etichetta come parola o frase, non come frase, che termina con due punti e usando testo [statico](glossary.md).
-   Assegnare una chiave di accesso univoca. Per le linee guida per l'assegnazione, [vedere Tastiera](inter-keyboard.md).
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Posizionare l'etichetta sopra il controllo e allineare l'etichetta al bordo sinistro del controllo.
-   Per le visualizzazioni albero a selezione multipla, scrivere l'etichetta in modo che sia chiaro che è possibile selezionare più elementi. Le etichette della visualizzazione albero delle caselle di controllo possono essere meno esplicite.

    **Non corretto:**

    ![Screenshot della visualizzazione albero con l'etichetta dei componenti ](images/ctrl-tree-views-image22.png)

    In questo esempio l'etichetta non fornisce informazioni sulla selezione multipla.

    **Migliore:**

    ![Screenshot della visualizzazione albero con etichetta "uno o più" ](images/ctrl-tree-views-image23.png)

    In questo esempio, l'etichetta indica chiaramente che è possibile selezionare più elementi.

    **Miglior:**

    ![Screenshot della visualizzazione albero con caselle di controllo ](images/ctrl-tree-views-image24.png)

    In questo esempio le caselle di controllo indicano chiaramente che è possibile selezionare più elementi, quindi l'etichetta non deve essere esplicita.

### <a name="data-text"></a>Testo dei dati

-   Usare le maiuscole/minuscole come nelle frasi comuni.

### <a name="instructional-text"></a>Testo informativo

-   Se è necessario aggiungere testo informativo su una visualizzazione albero, aggiungerlo sopra l'etichetta. Usare frasi complete con punteggiatura finale.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Le spiegazioni supplementari utili ma non necessarie devono essere mantenute brevi. Inserire queste informazioni tra parentesi tra l'etichetta e i due punti, dopo l'istruzione main se usata al posto di un'etichetta o sotto il controllo.

    ![Screenshot della spiegazione sotto la visualizzazione albero ](images/ctrl-tree-views-image8.png)

    In questo esempio la spiegazione supplementare è sotto il controllo .

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle visualizzazioni albero:

-   Usare il testo esatto dell'etichetta, inclusa la combinazione di maiuscole e minuscole, ma non includere il carattere di sottolineatura o i due punti della chiave di accesso. Includere l'elenco di parole o l'elenco gerarchico se il contesto richiede una distinzione dagli elenchi regolari.
-   Per gli elementi della struttura ad albero, usare il testo esatto dell'elemento, inclusa l'uso di maiuscole e minuscole.
-   Fare riferimento alle visualizzazioni albero come visualizzazioni albero solo nella programmazione e in altre documentazione tecnica. In qualsiasi altro luogo, usare l'elenco o l'elenco gerarchico perché l'albero dei termini crea confusione per la maggior parte degli utenti.
-   Per descrivere l'interazione dell'utente, usare select per i dati ed espandere e comprimere per i pulsanti più e meno.
-   Quando possibile, formattare l'etichetta e gli elementi della struttura ad albero usando il testo in grassetto. In caso contrario, inserire l'etichetta e gli elementi tra virgolette solo se necessario per evitare confusione.

Esempio: **nell'elenco Contenuto** selezionare Interfaccia utente **Progettazione**.

Quando si fa riferimento alle caselle di controllo in una visualizzazione albero:

-   Usare il testo esatto dell'etichetta, inclusa l'uso di maiuscole e minuscole, e includere la casella di controllo delle parole. Non includere il carattere di sottolineatura della chiave di accesso.
-   Per descrivere l'interazione dell'utente, usare select e clear.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

Esempio: **nell'elenco Elementi di cui eseguire il backup** selezionare la **Documenti** di controllo.

