---
title: Visualizzazioni ad albero
description: Con una visualizzazione albero, gli utenti possono visualizzare e interagire con una raccolta di oggetti organizzata in modo gerarchico, usando una selezione singola o più selezioni.
ms.assetid: f0206485-e028-41d8-9be2-5d59f0a0b677
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c5cb2b6d48a30cba6de2136659231d9d37361621
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104569161"
---
# <a name="tree-views"></a>Visualizzazioni ad albero

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Con una visualizzazione albero, gli utenti possono visualizzare e interagire con una raccolta di oggetti organizzata in modo gerarchico, usando una selezione singola o più selezioni.

In un albero gli oggetti contenenti dati sono denominati nodi foglia e gli oggetti che contengono altri oggetti sono denominati nodi contenitore. Un singolo nodo contenitore principale è denominato nodo radice. Gli utenti possono espandere e comprimere i nodi del contenitore facendo clic sui pulsanti di espansione più e meno.

![screenshot della visualizzazione albero di Esplora risorse ](images/ctrl-tree-views-image1.png)

Una tipica visualizzazione albero.

> [!Note]  
> Le linee guida relative al [layout](vis-layout.md) e ai [menu](cmd-menus.md) vengono presentate in articoli distinti.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

**La presenza di dati gerarchici non significa che è necessario utilizzare una visualizzazione albero.** Molto spesso una [visualizzazione elenco](ctrl-list-views.md) è una scelta più semplice, ma più potente. Visualizzazioni elenco:

-   Supportare diverse visualizzazioni.
-   Supporta l'ordinamento dei dati in base a qualsiasi colonna nella visualizzazione dettagli.
-   Supportare l'organizzazione dei dati in gruppi, formando una gerarchia a due livelli.

**Per utilizzare una visualizzazione elenco, è possibile rendere flat le informazioni gerarchiche utilizzando le tecniche seguenti:**

-   Rimuovere il nodo radice, se presente, perché spesso non è necessario.
-   Usare gruppi di visualizzazione elenco, tabulazioni, [elenchi a discesa](/windows/desktop/uxguide/ctrl-drop)o [intestazioni espandibili](glossary.md) per sostituire i contenitori di primo livello.

    ![screenshot dei gruppi di visualizzazione elenco contenenti elenchi ](images/ctrl-tree-views-image2.png)

    In questo esempio vengono usati i gruppi di visualizzazione elenco per i contenitori di primo livello.

    ![screenshot delle schede usate per i contenitori di primo livello ](images/ctrl-tree-views-image3.png)

    In questo esempio vengono usate le schede per i contenitori di primo livello

    ![screenshot dell'elenco a discesa usato come contenitore ](images/ctrl-tree-views-image4.png)

    In questo esempio viene usato un elenco a discesa per i contenitori di livello superiore.

-   Se un controllo associato Visualizza il contenuto del contenitore selezionato, il controllo può visualizzare livelli inferiori della gerarchia.

    ![screenshot del riquadro del sommario ](images/ctrl-tree-views-image5.png)

    In questo esempio, i contenitori di basso livello vengono visualizzati nella finestra del documento.

**È necessario utilizzare una visualizzazione struttura ad albero se è necessario visualizzare una gerarchia di più di due livelli, escluso il nodo radice.**

Per decidere se una visualizzazione albero è il controllo corretto, prendere in considerazione le domande seguenti:

-   **I dati sono gerarchici?** Se non è così, usa un altro controllo.
-   **La gerarchia presenta almeno tre livelli (senza includere la radice)?** In caso contrario, prendere in considerazione alternative quali gruppi di visualizzazione elenco, tabulazioni, elenchi a discesa o intestazioni espandibili.
-   **Gli elementi contengono dati ausiliari?** In tal caso, è consigliabile utilizzare una visualizzazione elenco nella modalità di visualizzazione dettagli per sfruttare appieno i dati ausiliari.
-   **I dati di livello inferiore sono correlati a sottoattività indipendenti?** In tal caso, è consigliabile visualizzare le informazioni in un controllo associato o in una finestra separata (visualizzata utilizzando i [pulsanti di comando](ctrl-command-buttons.md) o i [collegamenti](ctrl-command-links.md)).
-   **Gli utenti di destinazione sono avanzati?** Gli utenti avanzati hanno più dimestichezza con l'uso degli alberi. Se l'applicazione è destinata agli utenti meno esperti, evitare di utilizzare le visualizzazioni ad albero.
-   **Gli elementi hanno un'unica categorizzazione gerarchica naturale che è familiare alla maggior parte degli utenti?** In tal caso, i dati sono ideali per una visualizzazione albero. Se è necessario disporre di più visualizzazioni o ordinamento, usare invece una visualizzazione elenco.
-   **È necessario che gli utenti visualizzino i dati di basso livello in alcuni scenari, ma non in tutti gli scenari, o in alcuni casi non sempre?** In tal caso, i dati sono ideali per una visualizzazione albero.

> [!Note]  
> A volte un controllo simile a una visualizzazione albero viene implementato utilizzando una visualizzazione elenco. In questi casi, applicare le linee guida in base all'utilizzo, non all'implementazione.

 

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Gli alberi sono destinati a organizzare i dati e a facilitarne l'individuazione, ma è difficile renderli facilmente individuabili in un albero. Tenere presenti i principi seguenti quando si decidono le visualizzazioni albero e la relativa organizzazione.

### <a name="predictability-and-discoverability"></a>Prevedibilità e individuabilità

**Una visualizzazione struttura ad albero è basata sulle relazioni tra oggetti.** Gli alberi funzionano meglio quando gli oggetti formano una relazione chiara, ben nota, che si escludono a vicenda, in cui ogni oggetto viene mappato a un singolo contenitore facile da determinare.

**Un problema significativo è che un oggetto può essere visualizzato in nodi diversi.** Ad esempio, dove gli utenti si aspettano di trovare un dispositivo hardware che riproduce musica, ha un disco rigido di grandi dimensioni e usa una porta USB? Probabilmente in uno o più nodi contenitore diversi, ad esempio Multimedia, archiviazione, USB e possibilmente in risorse hardware. Una soluzione consiste nell'inserire ogni oggetto sotto il singolo contenitore più appropriato, indipendentemente dalle circostanze; un altro approccio consiste nell'inserire ogni oggetto in tutti i contenitori che si applicano. Il primo promuove una gerarchia semplice e pulita e il secondo promuove l'individuabilità di ognuno di essi presenta vantaggi e potenziali problemi.

**Gli utenti potrebbero non comprendere completamente il layout dell'albero, ma formeranno un modello mentale delle relazioni dopo l'interazione con l'albero per un certo periodo di tempo.** Se il modello mentale è errato, comporta confusione. Si supponga, ad esempio, che un lettore musicale sia disponibile nei contenitori multimediali, di archiviazione e USB. Questa disposizione migliora l'individuabilità. Se un utente trova per la prima volta il dispositivo nei dispositivi multimediali, l'utente può concludere che tutti i dispositivi come i lettori musicali vengono visualizzati nel contenitore multimediale. L'utente si aspetterà quindi che i dispositivi simili, ad esempio le fotocamere digitali, vengano visualizzati nel contenitore multimediale e, in caso contrario, diventeranno confusi.

**Quando si progetta un albero, è necessario bilanciare l'individuabilità con un modello utente prevedibile che riduce al minimo la confusione.**

### <a name="breadth-vs-depth"></a>Confronto tra larghezza e profondità

Gli studi di usabilità hanno dimostrato che **gli utenti hanno più successo nella ricerca di oggetti in un albero che è ampio rispetto a un albero che è profondo**, quindi, quando si progetta un albero, è preferibile passare alla profondità. Idealmente, un albero non deve avere più di quattro livelli (senza contare il nodo radice) e gli oggetti utilizzati più di frequente dovrebbero apparire nei primi due livelli.

### <a name="other-principles"></a>Altri principi

-   Quando gli utenti trovano gli elementi cercati, interrompono la ricerca. Non sembrano vedere dove potrebbe essere trovato un oggetto perché non è necessario. Questi utenti possono supporre che il primo percorso trovato sia l'unico percorso.
-   Gli utenti non riescono a trovare oggetti in alberi grandi e complessi. Gli utenti non eseguiranno una ricerca completa e manuale per trovare oggetti in tali alberi; si fermano una volta che pensano di avere speso un lavoro ragionevole. Di conseguenza, gli alberi complessi di grandi dimensioni devono essere aggiunti ad altri metodi di accesso, ad esempio la ricerca di parole, un indice o un filtro.
-   Alcuni programmi consentono agli utenti di creare i propri alberi. Anche se tali alberi progettati in modo automatico potrebbero essere allineati con un modello mentale di un utente, vengono spesso creati in modo casuale e poco gestito. Ad esempio, mentre un file system, un programma di posta elettronica e un elenco di preferiti in genere archiviano tipi simili di informazioni, gli utenti raramente si occupano di organizzarli nello stesso modo.

**Se si esegue una sola operazione...**

Valutare con attenzione i vantaggi e gli svantaggi dell'utilizzo delle visualizzazioni ad albero. La presenza di dati disposti gerarchicamente non significa che è necessario utilizzare una visualizzazione albero.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le visualizzazioni ad albero includono diversi modelli di utilizzo:



|                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Visualizzazioni ad albero solo con nodi contenitore**<br/> Gli utenti possono visualizzare e interagire con un contenitore alla volta. <br/>                        | In genere, queste visualizzazioni ad albero dispongono di un controllo associato che Visualizza il contenuto del contenitore selezionato, in modo che gli utenti possano interagire con un solo contenitore alla volta. <br/> ![screenshot del riquadro del contenitore e del riquadro dei contenuti ](images/ctrl-tree-views-image6.png)<br/> In questo esempio la visualizzazione albero ha solo nodi contenitore. Il contenuto del nodo selezionato viene visualizzato nel controllo visualizzazione elenco associato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Visualizzazioni ad albero con nodi contenitore e foglia**<br/> Gli utenti possono visualizzare e interagire con contenitori e foglie.<br/>                       | In genere, queste visualizzazioni ad albero dispongono di un controllo associato che Visualizza il contenuto del contenitore o foglia selezionato. consentire agli utenti di interagire con le foglie spesso rende necessario supportare più selezioni. <br/> ![screenshot del riquadro visualizzazione albero e del riquadro dei contenuti ](images/ctrl-tree-views-image7.png)<br/> in questo esempio la visualizzazione struttura ad albero include sia nodi contenitore che foglia. Poiché la selezione multipla è supportata, il contenuto degli elementi aperti viene visualizzato utilizzando le [schede](ctrl-tabs.md) nel controllo associato.<br/> in alternativa, la visualizzazione albero può avere un elenco organizzato, in cui i contenitori sono intestazioni e le foglie sono opzioni. <br/> ![screenshot della visualizzazione albero con intestazioni e opzioni ](images/ctrl-tree-views-image8.png)<br/> In questo esempio le foglie dell'albero sono opzioni e i contenitori sono categorie di opzioni.<br/> |
| **Viste albero casella di controllo**<br/> Gli utenti possono selezionare un numero qualsiasi di elementi, incluso None.<br/>                                             | Le caselle di controllo indicano chiaramente che è possibile selezionare più selezioni. usare questo modello di struttura ad albero quando la selezione multipla è essenziale o usata di frequente. <br/> ![screenshot della visualizzazione albero con le caselle di controllo ](images/ctrl-tree-views-image9.png)<br/> In questo esempio, una visualizzazione struttura ad albero di caselle di controllo consente di attivare o disattivare la selezione delle funzionalità.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Generatori visualizzazione albero**<br/> Gli utenti possono creare un albero aggiungendo un contenitore o una foglia alla volta e, facoltativamente, impostando l'ordine.<br/> | Molti alberi possono essere creati o modificati dagli utenti. alcuni alberi sono compilati utilizzando i menu di scelta rapida e il trascinamento della selezione, ad esempio le cartelle in Esplora risorse, mentre altri alberi vengono compilati utilizzando una finestra di dialogo specializzata, ad esempio l'elenco Preferiti in Windows Internet Explorer. <br/> ![screenshot della finestra di dialogo Preferiti ](images/ctrl-tree-views-image10.png)<br/> In questo esempio di Internet Explorer, gli utenti possono creare un proprio elenco di preferiti utilizzando una finestra di dialogo.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| **Visualizzazioni ad albero con metodi di accesso alternativi**<br/> Gli utenti possono trovare oggetti in modi diversi dall'uso di un albero gerarchico.<br/>        | Come indicato in precedenza, gli utenti non riescono a trovare oggetti in alberi grandi e complessi, quindi tali alberi devono essere aggiunti ad altri metodi di accesso, ad esempio una ricerca di parole, un indice o un filtro. <br/> ![screenshot delle schede Sommario, indice e Preferiti ](images/ctrl-tree-views-image11.png)<br/> in questo esempio, gli utenti possono accedere alle informazioni anche usando un sommario, un indice e i Preferiti. per alcuni utenti, le schede indice e cerca possono essere più utili rispetto alla scheda contenuto.<br/> ![screenshot del menu Start di Windows e della casella di ricerca ](images/ctrl-tree-views-image12.png)<br/> In questo esempio, il menu Start di Windows consente inoltre agli utenti di accedere a programmi, file e pagine Web digitando parte del nome nella casella di ricerca.<br/>                                                                                                             |



 

## <a name="guidelines"></a>Indicazioni

### <a name="presentation"></a>Presentazione

-   **All'interno di un contenitore, ordinare gli elementi in un ordine logico.** Ordina i nomi in ordine alfabetico, numeri in ordine numerico e date in ordine cronologico.
-   **Usare l'attributo always show Selection** in modo che gli utenti possano determinare prontamente l'elemento selezionato, anche quando il controllo non ha lo stato attivo per l'input.
-   **Se l'albero funge da Sommario, utilizzare il singolo attributo Expand per semplificare la gestione dell'albero.** In questo modo, viene espansa solo la parte pertinente dell'albero.
-   **Evitare di presentare alberi vuoti.** Se un utente crea un albero, inizializzare l'albero con le istruzioni o gli elementi di esempio che potrebbero essere necessari per gli utenti.

    ![screenshot dell'elenco dei Preferiti di Internet Explorer ](images/ctrl-tree-views-image13.png)

    In questo esempio l'elenco viene presentato inizialmente con esempi.

-   **Non rendere i nodi contenitore comprimibili se gli utenti non hanno motivo di comprimerli.** Questa operazione aggiunge complessità superflua.
-   **Se le prestazioni di caricamento sono un problema, per impostazione predefinita vengono visualizzati solo i contenitori di primo e secondo livello della struttura ad albero.** È quindi possibile caricare dati aggiuntivi su richiesta quando un utente espande i rami nell'albero.
-   **Se gli utenti espandono o comprimono un contenitore, rendere permanente lo stato in modo che abbia effetto la volta successiva che viene visualizzata la visualizzazione albero**, a meno che non sia preferibile che gli utenti inizino nello stato predefinito. La persistenza deve essere basata sulla visualizzazione ad albero, per singolo utente.
-   **Se i contenitori di livello elevato presentano contenuto simile, provare a usare gli indizi visivi per distinguerli.**

    **Non corretto:**

    ![screenshot degli elementi di Outlook con icone diverse ](images/ctrl-tree-views-image14.png)

    In questo esempio la cassetta postale e le cartelle di archiviazione hanno contenuto simile. Quando gli alberi sono ulteriormente espansi, è molto difficile per gli utenti capire dove si trovano nell'albero, causando confusione. L'uso di icone leggermente diverse nelle diverse sezioni risolverebbe questo problema.

-   **Riconsiderare le linee di connessione.** Sebbene queste righe mostrino chiaramente le relazioni tra il contenitore e i nodi foglia, aggiungono confusione visiva senza aiutare significativamente la comprensione. In particolare, non sono utili quando i nodi sono vicini, né aiutano quando i nodi sono così lontani dal fatto che lo scorrimento è necessario.

    **Corretto:**

    ![screenshot della visualizzazione albero con linee di connessione ](images/ctrl-tree-views-image15.png)

    **Migliore:**

    ![screenshot della visualizzazione albero senza linee di connessione ](images/ctrl-tree-views-image16.png)

    Le linee di connessione sono poco utili per facilitare la comprensione.

### <a name="interaction"></a>Interazione

-   **Si consiglia di fornire un comportamento di doppio clic.** Il doppio clic dovrebbe avere lo stesso effetto della selezione di un elemento e dell'esecuzione del comando predefinito.
-   **Rendere ridondante il comportamento di doppio clic.** Deve essere sempre presente un pulsante di comando o un comando del menu di scelta rapida con lo stesso effetto.
-   Se un elemento richiede una spiegazione ulteriore, **fornire la spiegazione in un infotip**.

    ![screenshot dei preferiti con infotip per un elemento ](images/ctrl-tree-views-image17.png)

    In questo esempio, un infotip fornisce ulteriori informazioni.

-   **Fornire menu di scelta rapida dei comandi pertinenti.** Tali comandi includono taglia, copia, incolla, Rimuovi o Elimina, Rinomina e proprietà.
-   **Quando si disabilita una visualizzazione albero, disabilitare anche le etichette e i pulsanti di comando associati.**

### <a name="tree-organization"></a>Organizzazione albero

-   **Usare una struttura gerarchica naturale familiare alla maggior parte degli utenti.**
-   **Se non è possibile usare tale struttura, provare a bilanciare l'individuabilità con un modello utente stimabile che riduce al minimo la confusione.**
-   **Per migliorare in modo sicuro l'individuabilità, inserire un elemento in più contenitori nei casi seguenti:**
    -   L'elemento non è correlato ad altri elementi simili, in modo che gli utenti non vengano confusi da associazioni non corrette.
    -   Solo alcuni di questi elementi sono stati individuati in modo ridondante, quindi l'albero non diventa gonfio.
-   **Utilizzare la struttura gerarchica più semplice che funziona correttamente.** A tale scopo, procedere nel seguente modo:
    -   Posizionare gli oggetti a cui si accede più di frequente nei primi due livelli della struttura ad albero (senza contare il nodo radice) e posizionare gli oggetti a cui si accede meno comunemente più a lungo nella gerarchia.
    -   Eliminare i contenitori non necessari o combinare i contenitori di livello intermedio ridondanti.
-   **Preferisci l'ampiezza rispetto alla profondità.** Idealmente, un albero non deve avere più di quattro livelli e gli oggetti a cui si accede più di frequente dovrebbero apparire nei primi due livelli.
-   **Determinare se è effettivamente necessario un nodo radice.** Fornire un nodo radice se gli utenti hanno la possibilità di eseguire comandi sull'intero albero, possibilmente usando un menu di scelta rapida nel nodo radice. In caso contrario, l'albero è più semplice e più facile da utilizzare senza di esso.
-   **Se l'albero dispone di metodi di accesso alternativi, ad esempio una ricerca di parole o un indice, è possibile ottimizzare l'albero per l'esplorazione concentrandosi sul contenuto più utile.** Con i metodi di accesso alternativi, il contenuto dell'albero non deve essere completo. La semplificazione dell'albero rende più semplice per gli utenti trovare il contenuto più utile.

### <a name="check-box-tree-views"></a>Viste albero casella di controllo

-   Consente **di visualizzare il numero di elementi selezionati al di sotto dell'elenco**, soprattutto se gli utenti hanno la possibilità di selezionare più elementi. Questo feedback aiuta gli utenti a confermare che la selezione è corretta.

    ![screenshot del numero di elementi selezionati ](images/ctrl-tree-views-image18.png)

    In questo esempio, il numero di elementi selezionati viene visualizzato sotto l'albero. È chiaro che due elementi non sono selezionati.

-   Se sono presenti potenzialmente molti elementi e la selezione o la cancellazione di tutti questi elementi è probabile, aggiungere tutti i pulsanti di comando Seleziona tutto e cancella tutti.
-   **Usare le caselle di controllo con stato misto per indicare la selezione parziale degli elementi in un contenitore.**

    **Corretto:**

    ![screenshot della finestra con caselle di controllo con stato misto ](images/ctrl-tree-views-image19.png)

    In questo esempio vengono usate le caselle di controllo con stato misto per indicare la selezione parziale.

## <a name="recommended-sizing-and-spacing"></a>Ridimensionamento e spaziatura consigliati

![screenshot del ridimensionamento e della spaziatura della visualizzazione albero ](images/ctrl-tree-views-image20.png)

Dimensionamento e spaziatura consigliati per i controlli di visualizzazione albero.

-   **Scegliere una larghezza della visualizzazione albero che evita la necessità di scorrimento orizzontale** per la maggior parte degli elementi quando l'albero è completamente espanso.
-   **Includere un ulteriore 30% per adattarsi alla localizzazione.**
-   **Scegliere un'altezza della visualizzazione albero che elimini lo scorrimento verticale non necessario.** Prendere in considerazione la possibilità di rendere una visualizzazione albero leggermente più lunga (o anche più, se lo spazio disponibile è sufficiente) se questa operazione riduce la necessità di una barra di scorrimento verticale.

    **Non corretto:**

    ![screenshot del controllo di visualizzazione ad albero breve e stretto ](images/ctrl-tree-views-image21.png)

    In questo esempio, la visualizzazione albero è leggermente più ampia e più lunga eliminerà le barre di scorrimento nella maggior parte dei casi. In questo albero particolare, è possibile aprire un solo contenitore alla volta.

-   **Se gli utenti traggono vantaggio da una visualizzazione struttura ad albero, rendere ridimensionabili la visualizzazione albero e la finestra padre.** Questa operazione consente agli utenti di modificare le dimensioni della visualizzazione albero in base alle esigenze.

## <a name="labels"></a>Etichette

### <a name="control-labels"></a>Etichette di controllo

-   Tutte le visualizzazioni ad albero necessitano di etichette. Scrivere l'etichetta come una parola o una frase, non come una frase, terminando con i due punti e usando il [testo statico](glossary.md).
-   Assegnare una chiave di accesso univoca. Per le linee guida di assegnazione, vedere [tastiera](inter-keyboard.md).
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Posizionare l'etichetta sopra il controllo e allineare l'etichetta al bordo sinistro del controllo.
-   Per le visualizzazioni ad albero a selezione multipla, scrivere l'etichetta in modo che sia chiaro che è possibile selezionare più selezioni. Le etichette della visualizzazione albero casella di controllo possono essere meno esplicite.

    **Non corretto:**

    ![screenshot della visualizzazione albero con etichetta componenti ](images/ctrl-tree-views-image22.png)

    In questo esempio, l'etichetta non fornisce informazioni su selezione multipla.

    **Migliore:**

    ![screenshot della visualizzazione albero con etichetta ' uno o più' ](images/ctrl-tree-views-image23.png)

    In questo esempio, l'etichetta indica chiaramente che è possibile selezionare più selezioni.

    **Consigliate**

    ![screenshot della visualizzazione albero con caselle di controllo ](images/ctrl-tree-views-image24.png)

    In questo esempio, le caselle di controllo indicano chiaramente che è possibile selezionare più selezioni, quindi l'etichetta non deve essere esplicita.

### <a name="data-text"></a>Testo dati

-   Usare le maiuscole/minuscole come nelle frasi comuni.

### <a name="instructional-text"></a>Testo istruzioni

-   Se è necessario aggiungere testo di istruzioni su una visualizzazione albero, aggiungerlo sopra l'etichetta. Utilizzare frasi complete con la punteggiatura finale.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Le spiegazioni aggiuntive utili ma non necessarie devono essere mantenute brevi. Inserire queste informazioni tra parentesi tra l'etichetta e i due punti, dopo l'istruzione principale se utilizzata anziché un'etichetta o sotto il controllo.

    ![screenshot della spiegazione sotto la visualizzazione albero ](images/ctrl-tree-views-image8.png)

    In questo esempio la spiegazione supplementare è sotto il controllo.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento a visualizzazioni ad albero:

-   Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, ma non includere il carattere di sottolineatura della chiave di accesso o i due punti. Includere l'elenco di parole o l'elenco gerarchico se il contesto richiede la distinzione da elenchi regolari.
-   Per gli elementi della struttura ad albero, usare il testo esatto dell'elemento, inclusa la relativa maiuscola.
-   Vedere le visualizzazioni albero come visualizzazioni ad albero solo nella programmazione e in altri documenti tecnici. In tutti gli altri casi, usare un elenco o un elenco gerarchico perché l'albero dei termini presenta confusione per la maggior parte degli utenti.
-   Per descrivere l'interazione dell'utente, usare SELECT per i dati ed espandere e comprimere per i pulsanti con il segno più e il segno meno.
-   Quando possibile, formattare gli elementi label e Tree usando il testo in grassetto. In caso contrario, inserire l'etichetta e gli elementi tra virgolette solo se necessario per evitare confusione.

Esempio: nell'elenco **Sommario** selezionare **progettazione interfaccia utente**.

Quando si fa riferimento alle caselle di controllo in una visualizzazione struttura ad albero:

-   Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, e includere la casella di controllo parole. Non includere il carattere di sottolineatura della chiave di accesso.
-   Per descrivere l'interazione dell'utente, usare SELECT e Clear.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

Esempio: nell'elenco **elementi di cui eseguire il backup** selezionare la casella di controllo **documenti** .

