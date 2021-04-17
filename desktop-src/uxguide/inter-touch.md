---
title: Tocco
description: Tutte le applicazioni Microsoft Windows dovrebbero avere un'esperienza di tocco eccezionale. La creazione di un'esperienza di questo tipo è più semplice di quanto pensi.
ms.assetid: a87d0726-1c57-4cf8-9e35-4e73a09ff1a3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a44a95ad963d3563418ed0492e55606824011f31
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104571485"
---
# <a name="touch"></a>Tocco

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Tutte le applicazioni Microsoft Windows dovrebbero avere un'esperienza di tocco eccezionale. La creazione di un'esperienza di questo tipo è più semplice di quanto pensi.

Il tocco si riferisce all'uso di una o più dita per fornire l'input attraverso la visualizzazione di un dispositivo e interagire con Windows e le app. Un'app ottimizzata per il tocco ha un'interfaccia utente e un modello di interazione progettati per supportare le aree di contatto più grandi, meno precise, i diversi fattori di forma dei dispositivi di tocco e le numerose posture e grip che possono essere adottate dagli utenti quando usano un dispositivo touch.

![Interazione dell'utente con tablet mediante touch](images/inter_touch_image1.jpeg)

Ogni dispositivo di input ha i propri punti di forza. La tastiera è ideale per l'input di testo e per fornire comandi con movimento minimo. Il mouse è la scelta migliore per puntare in modo efficiente e preciso. Il tocco è ideale per la manipolazione degli oggetti e per l'assegnazione di semplici comandi. Una penna è la scelta migliore per l'espressione FreeForm, come per la grafia e il disegno.

Windows 8.1 è ottimizzato per la velocità di risposta, l'accuratezza e la facilità d'uso con il tocco, supportando al tempo stesso i tradizionali metodi di input (ad esempio mouse, penna e tastiera). La velocità, l'accuratezza e il feedback tattile forniti dalle modalità di input tradizionali sono familiari e accattivanti per molti utenti e potenzialmente più adatti a scenari di interazione specifici.

È possibile trovare linee guida relative al mouse, alla penna e all'accessibilità in argomenti distinti.

Quando si pensa all'esperienza di interazione per l'app:

Non presupporre che se un'interfaccia utente funziona correttamente per un mouse, funziona bene anche per il tocco. Sebbene il supporto del mouse sia valido, un'esperienza di tocco ottimale presenta alcuni requisiti aggiuntivi.

Si supponga che se un'interfaccia utente funziona correttamente per un dito, funziona bene anche per una penna. Rendere l'app toccabile è un metodo molto lungo per fornire un supporto efficace per le penne. La differenza principale è che le dita hanno un suggerimento più smussato, quindi richiedono obiettivi più grandi.

Con il tocco è possibile modificare direttamente gli oggetti e l'interfaccia utente, il che rende un'esperienza più rapida, più naturale e accattivante.

## <a name="provide-a-great-touch-experience"></a>Offrire un'esperienza di tocco ottimale

È necessario assicurarsi che gli utenti possano eseguire attività critiche e importanti in modo efficiente tramite l'input tocco. Tuttavia, le funzionalità specifiche dell'app, come il testo o la manipolazione dei pixel, potrebbero non essere adatte per il tocco e possono essere riservate al dispositivo di input più adatto.

Se non si ha molta esperienza nello sviluppo di app touch, è preferibile apprendere. Ottenere un computer abilitato per il tocco, posizionare il mouse e la tastiera e usare solo le dita per interagire con l'app. Se si dispone di un tablet, provare a tenerlo in posizioni diverse, ad esempio in un secondo momento, in una tabella o nelle braccia mentre si è in piedi. Provare a usarlo con orientamento verticale e orizzontale.

Le app ottimizzate per il tocco che funzionano meglio con l'interazione con il tocco sono in genere:

-   **Naturale e intuitivo.** Le interazioni sono progettate per corrispondere al modo in cui gli utenti interagiscono con gli oggetti nel mondo reale.
-   **Meno intrusivo.** L'uso del tocco è invisibile all'utente e, di conseguenza, molto meno distrae rispetto alla digitazione o al clic
-   **Portabile.** I dispositivi touch sono più compatti perché molte attività possono essere completate senza una tastiera, un mouse, una penna o un touchpad. Sono inoltre più flessibili perché non è necessaria una superficie di lavoro.
-   **Diretta e accattivante.** Il tocco consente di modificare direttamente gli oggetti sullo schermo.
-   **Meno accurato.** Gli utenti non possono indirizzare gli oggetti in modo accurato con il tocco, rispetto a un mouse o a una penna.

Touch offre un'interazione naturale e reale. La manipolazione diretta e l'animazione completano questa impressione, offrendo agli oggetti un movimento realistico, dinamico e feedback. Si consideri, ad esempio, un gioco di carte. Non solo è comodo e facile trascinare le schede usando un dito, ma l'esperienza è molto interessante quando è possibile gettare, scivolare e ruotare le schede esattamente come se si trattasse di un mazzo fisico. Quando si tenta di spostare una scheda che non può essere spostata, è consigliabile fare in modo che la scheda si opponga, ma non impedisca lo spostamento e si ristabilisca quando viene rilasciata, per indicare chiaramente che l'azione è stata riconosciuta ma non può essere eseguita.

Fortunatamente, se l'app è già stata progettata correttamente, l'esperienza di tocco è facile. A questo scopo, un programma ben progettato:

-   **Assicura che la maggior parte delle attività più importanti possa essere eseguita in modo efficiente utilizzando un dito** (almeno le attività che non comportano una grande quantità di tipizzazione o manipolazione dettagliata dei pixel).
-   **Usa controlli di grandi dimensioni per il tocco.** I controlli comuni hanno una dimensione minima di 23x23 pixel (13x13 DLU) e i controlli usati più di frequente sono almeno 40x40 pixel (23x22 DLU). Per evitare il comportamento che non risponde, gli elementi dell'interfaccia utente devono avere almeno 5 pixel (3 DLU) di spazio tra di essi. Per gli altri controlli, assicurarsi che abbiano almeno un pixel 23x23 (13x13 DLU) fare clic su destinazione, anche se il relativo aspetto statico è molto più piccolo. Vedere dimensionamento del controllo standard.
-   **Supporta l'input del mouse.** I controlli interattivi hanno affordances evidenti. Gli oggetti hanno comportamenti standard per le interazioni con il mouse standard (solo e doppio clic con il pulsante destro del mouse, fare clic con il pulsante destro del mouse, trascinare e passare il mouse).
-   **Supporta l'input da tastiera.** L'app fornisce le assegnazioni dei tasti di scelta rapida standard, in particolare per i comandi di navigazione e modifica che possono essere generati anche tramite movimenti di tocco.
-   **Garantisce l'accessibilità.** USA automazione interfaccia utente o Microsoft Active Accessibility (MSAA) per fornire l'accesso a livello di codice all'interfaccia utente per le tecnologie per l'accesso facilitato. L'app risponde in modo appropriato alle modifiche all'orientamento, al tema, alle impostazioni locali e alle metriche di sistema.
-   **Elimina le interazioni non necessarie.** Per evitare la perdita di dati o l'accesso al sistema, utilizzare i valori predefiniti più sicuri e più sicuri. Se la sicurezza e la sicurezza non sono fattori, l'app seleziona l'opzione più probabile o più pratica.
-   **Fornisce un equivalente tocco per il passaggio del mouse.** Non fare affidamento sul passaggio del mouse come unico modo per eseguire un'azione.
-   **Assicura che i movimenti abbiano effetto immediato.** Mantieni i punti di contatto sotto le dita dell'utente in tutto il movimento, che fornisce l'effetto del mapping dei movimenti direttamente al movimento dell'utente.
-   **USA i movimenti standard quando possibile.** Movimenti personalizzati solo per le interazioni univoche con l'app.
-   **Garantisce che i comandi indesiderati o distruttivi possano essere invertiti o corretti.** Quando si usa il tocco, è più probabile che vengano eseguite azioni accidentali.

## <a name="guidelines-for-touch-input"></a>Linee guida per l'input tocco

Con il tocco, l'app di Windows può usare i movimenti fisici per emulare la manipolazione diretta degli elementi dell'interfaccia utente.

Prendere in considerazione queste procedure consigliate durante la progettazione dell'app abilitata per il tocco:

**La velocità di risposta è essenziale per la creazione di esperienze di tocco che si ritengono dirette e accattivanti.** Per sentirsi direttamente, i movimenti devono essere applicati immediatamente e i punti di contatto di un oggetto devono rimanere sotto le dita dell'utente in tutto il movimento. L'effetto dell'input di tocco dovrebbe essere mappato direttamente al movimento dell'utente, quindi, ad esempio, se l'utente ruota le dita 90 gradi, l'oggetto deve ruotare anche 90 gradi. Qualsiasi ritardo, risposta frammentata, perdita di contatto o risultati non accurati Elimina la percezione della manipolazione diretta e anche della qualità.

**La coerenza è essenziale per la creazione di esperienze di tocco che hanno un aspetto naturale e intuitivo.** Una volta che gli utenti imparano un gesto standard, si aspettano che questo movimento abbia lo stesso effetto su tutte le app. Per evitare confusione e frustrazione, non assegnare mai significati non standard a movimenti standard. Usare invece movimenti personalizzati per le interazioni univoche del programma.

Verrà ora descritto il linguaggio Windows Touch, ma prima di procedere, ecco un breve elenco di termini di base per l'input tocco.

-   **Movimento**

    Un gesto è l'azione fisica o il movimento eseguito su, o da, il dispositivo di input (dito, dita, penna/stilo, mouse e così via). Ad esempio, per avviare, attivare o richiamare un comando, è possibile usare un singolo tocco del dito per un dispositivo touch o touchpad (equivalente a un clic con il mouse, un tocco con una penna o una tastiera).

-   **Manipolazione**

    Una manipolazione è la reazione immediata, in tempo reale o la risposta di un oggetto o di un'interfaccia utente a un movimento. Ad esempio, sia i movimenti diapositiva che quelli a scorrimento rapido provocano lo spostamento di un elemento o di un'interfaccia utente in qualche modo.

    Il risultato finale di una manipolazione, il modo in cui viene manifestato dall'oggetto sullo schermo e nell'interfaccia utente è l'interazione.

-   **Interazione**

    Le interazioni dipendono dal modo in cui viene interpretata una manipolazione e dal comando o dall'azione risultante dalla manipolazione. Ad esempio, gli oggetti possono essere spostati usando i movimenti diapositiva e scorrimento rapido, ma i risultati variano a seconda che la soglia di distanza venga superata. La diapositiva può essere usata per trascinare un oggetto o una visualizzazione panning mentre è possibile selezionare un elemento o visualizzare una barra dell'app.

### <a name="the-windows-touch-language"></a>Lingua Windows Touch

Windows offre un insieme conciso di interazioni di tocco che vengono utilizzate in tutto il sistema. L'applicazione di questo linguaggio di tocco rende l'app familiare in modo coerente agli utenti che conoscono già. Questo aumenta la confidenza degli utenti rendendo più semplice l'apprendimento e l'utilizzo dell'app. Per altre informazioni sull'implementazione del linguaggio touch, vedere movimenti, manipolazioni e interazioni.

**Premere e tenere premuto per apprendere**

Il movimento di stampa e di attesa Visualizza informazioni dettagliate o elementi visivi di insegnamento, ad esempio una descrizione comando o un menu di scelta rapida, senza eseguire il commit di un'azione o di un comando. Il panning è ancora possibile se viene avviato un movimento scorrevole durante la visualizzazione dell'oggetto visivo.

> [!IMPORTANT]
> È possibile utilizzare la pressione di selezione nei casi in cui sia abilitata la panoramica orizzontale che quella verticale.

 

Stato di ingresso: una o due dita in contatto con lo schermo.

Motion: nessun movimento.

Stato di uscita: l'ultimo dito termina il movimento.

Effetto: visualizzare altre informazioni.

![Toccare \- premere \- per \-learn.png](images/inter-touch-image2.png)

Movimento di stampa e di attesa.

**Passaggio del mouse**

Il passaggio del mouse è un'interazione utile perché consente agli utenti di ottenere informazioni aggiuntive tramite suggerimenti prima di avviare un'azione. Questo suggerimento rende gli utenti più sicuri e riduce gli errori.

Sfortunatamente, il passaggio del mouse non è supportato dalle tecnologie touch, quindi gli utenti non possono passare il mouse quando si usa un dito. La soluzione semplice a questo problema consiste nell'sfruttare al massimo il passaggio del mouse, ma solo in modi che non sono necessari per eseguire un'azione. In pratica, questo significa generalmente che l'azione può essere eseguita anche facendo clic su, ma non necessariamente esattamente nello stesso modo.

![Screenshot che mostra un esempio di interazione con il passaggio del mouse accanto a un esempio di azione di clic.](images/inter-touch-image13.png)

In questo esempio gli utenti possono visualizzare la data odierna spostando il puntatore del mouse o facendo clic su di esso.

**Toccare per l'azione principale**

Il tocco su un elemento richiama l'azione principale, ad esempio l'avvio di un'app o l'esecuzione di un comando.

Stato di ingresso: un dito in contatto con lo schermo o il touchpad ed è stato rimosso prima della soglia di tempo per un'interazione di pressione e pressione.

Motion: nessun movimento.

Stato di uscita: il dito termina il movimento.

Effetto: avviare un'app o eseguire un comando.

![Toccare \- \-primary.png](images/inter-touch-image3.png)

Movimento tap.

**Scorri alla panoramica**

La diapositiva viene utilizzata principalmente per le interazioni di panoramica, ma può essere utilizzata anche per lo spostamento (in cui la panoramica è vincolata a una direzione), il disegno o la scrittura. La diapositiva può essere usata anche per indirizzare elementi piccoli e densamente compressi eseguendo lo scrubbing (facendo scorrere il dito sugli oggetti correlati, ad esempio i pulsanti di opzione).

Stato di ingresso: una o due dita in contatto con lo schermo.

Motion: trascinare, con eventuali dita aggiuntive rimaste nella stessa posizione.

Stato di uscita: l'ultimo dito termina il movimento.

Effetto: spostare l'oggetto sottostante direttamente e immediatamente quando si muovono le dita. Assicurarsi di tenere il punto di contatto sotto il dito in tutto il movimento.

![\-slide.png touch](images/inter-touch-image4.png)

Movimento di panoramica.

**Scorrere rapidamente per selezionare, comando e spostare**

Se si scorre il dito a breve distanza, perpendicolare alla direzione della panoramica (dove il panning è vincolato a una direzione), seleziona gli oggetti in un elenco o in una griglia. Visualizza la barra dell'app con i comandi pertinenti quando sono selezionati oggetti.

Stato di ingresso: una o più dita toccano lo schermo.

Movimento: trascinare una breve distanza e un accuratezza prima della soglia di distanza per un'interazione di spostamento.

Stato di uscita: l'ultimo dito termina il movimento.

Effetto: l'oggetto sottostante è selezionato o spostato oppure viene visualizzata la barra dell'app. Assicurarsi di tenere il punto di contatto sotto il dito in tutto il movimento.

![d: \\ sdkenlistment \\ m \- \- progettare le \\ immagini \- del \- progetto m UX \\ \\ \-swipe.png](images/inter-touch-image5.png)

Gesto di scorrimento.

**Avvicinamento e allontanamento delle dita per operazioni di zoom**

Il pizzico e i movimenti di estensione vengono usati per tre tipi di interazioni: zoom ottico, ridimensionamento e zoom semantico.

Zoom ottico regola il livello di ingrandimento dell'intera area di contenuto per ottenere una visualizzazione più dettagliata del contenuto. Al contrario, il ridimensionamento è una tecnica per modificare la dimensione relativa di uno o più oggetti all'interno di un'area di contenuto senza modificare la visualizzazione nell'area del contenuto.

Lo zoom semantico è una tecnica ottimizzata per il tocco per la presentazione e lo spostamento di dati strutturati o contenuto in una singola visualizzazione, ad esempio la struttura di cartelle di un computer, una raccolta di documenti o un album di foto, senza la necessità di eseguire la panoramica, lo scorrimento o i controlli di visualizzazione ad albero. Lo zoom semantico offre due visualizzazioni diverse dello stesso contenuto, consentendo di visualizzare maggiori dettagli man mano che si esegue lo zoom avanti e meno dettagli.

Stato di ingresso: due dita in contatto con lo schermo allo stesso tempo.

Movimento: le dita si spostano a parte (stretch) o insieme (pizzico) lungo un asse.

Stato di uscita: qualsiasi dito termina il movimento.

Effetto: esegue lo zoom avanti o indietro dell'oggetto sottostante direttamente e immediatamente quando le dita si separano o si avvicinano all'asse. Assicurarsi di tenere i punti di contatto sotto il dito in tutto il movimento.

![areazoom.png di destinazione \-](images/inter-touch-image6.png)

Movimento di zoom.

**Ruotare per ruotare**

La rotazione con due o più dita causa la rotazione di un oggetto. Ruotare il dispositivo per far ruotare l'intero schermo.

Stato di ingresso: due dita in contatto con lo schermo allo stesso tempo.

Motion: una o entrambe le dita ruotano attorno all'altra, spostando la perpendicolare alla riga tra di esse.

Stato di uscita: qualsiasi dito termina il movimento.

Effetto: ruotare l'oggetto sottostante della stessa quantità delle dita ruotate. Assicurarsi di tenere i punti di contatto sotto il dito in tutto il movimento.

![\-turn.png touch](images/inter-touch-image7.png)

Movimento di rotazione.

La rotazione è sensata solo per determinati tipi di oggetti, quindi non è mappata a un'interazione di Windows di sistema.

La rotazione viene spesso eseguita in modo diverso da persone diverse. Alcuni utenti preferiscono ruotare un dito intorno a un dito pivot, mentre altri preferiscono ruotare entrambe le dita in un movimento circolare. La maggior parte degli utenti usa una combinazione di due, con uno spostato di un dito oltre l'altro. Sebbene la rotazione uniforme a qualsiasi angolo sia la migliore interazione, in molti contesti, ad esempio la visualizzazione di foto, è preferibile usare la rotazione di 90 gradi più vicina una volta che l'utente lo lascia. Per la modifica della foto, è possibile usare una piccola rotazione per raddrizzare la foto.

**Scorrere rapidamente dal bordo per i comandi dell'app**

Scorrendo il dito a breve distanza dal bordo inferiore o superiore della schermata vengono visualizzati i comandi dell'app in una barra dell'app.

Stato di ingresso: una o più dita toccano la lunetta.

Movimento: trascinare una breve distanza sullo schermo e sollevare.

Stato di uscita: l'ultimo dito termina il movimento.

Effetto: viene visualizzata la barra dell'app.

![Toccare \-edge.png in \- basso \-](images/inter-touch-image8.png)

![\-edge.png lato tocco sfiorato \- \-](images/inter-touch-image9.png)

Scorrimento del movimento del bordo.

Sviluppatori: per altre informazioni, vedere Enumerazione di [**\_ configurazione DIRECTMANIPULATION**](/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_configuration) .

### <a name="control-usage"></a>Controllare l'utilizzo

In questo articolo vengono fornite alcune linee guida per l'ottimizzazione dei controlli per l'utilizzo del tocco.

-   **Usare i controlli comuni.** I controlli più comuni sono progettati per supportare un'esperienza di tocco ottimale.
-   **Scegliere i controlli personalizzati progettati per supportare il tocco.** Potrebbe essere necessario disporre di controlli personalizzati per supportare le esperienze speciali del programma. Scegliere i controlli personalizzati che:
    -   Può essere dimensionato in modo sufficientemente grande per facilitare la selezione e la modifica.
    -   In caso di manipolazione, spostare e reagire il modo in cui gli oggetti reali si spostano e reagiscono, ad esempio con un momento e un attrito.
    -   Si perdono consentendo agli utenti di correggere facilmente gli errori.
    -   Si perdono di imprecisioni con la selezione e il trascinamento. Gli oggetti che vengono eliminati vicino alla destinazione devono rientrare nella posizione corretta.
    -   Quando il dito si trova sopra il controllo, è possibile ottenere un chiaro feedback visivo.
-   **Usare i controlli vincolati.** I controlli vincolati come gli elenchi e i dispositivi di scorrimento, se progettati per semplificare la destinazione del tocco, possono essere migliori rispetto ai controlli non vincolati, come le caselle di testo, perché riducono la necessità di input di testo.
-   **Fornire i valori predefiniti appropriati.** Selezionare il più sicuro (per evitare la perdita di dati o l'accesso al sistema) e l'opzione più sicura per impostazione predefinita. Se la sicurezza e la sicurezza non sono fattori, selezionare l'opzione più probabile o comoda, eliminando così l'interazione non necessaria.
-   **Fornire il completamento automatico del testo.** Fornisce un elenco di valori più probabili, o i valori di input più recenti, per semplificare notevolmente l'input di testo.
-   **Per le attività importanti che usano la selezione multipla**, se normalmente viene usato un elenco di selezione multipla standard, fornire un'opzione per l'uso di un elenco di caselle di controllo.

### <a name="control-sizes-and-touch-targeting"></a>Dimensioni del controllo e destinazione del tocco

A causa della grande superficie di attacco, i controlli di piccole dimensioni troppo vicini possono risultare difficili da definire come destinazione.

Come regola generale, una dimensione del controllo di 23x23 pixel (13x13 DLU) è una dimensione minima del controllo interattivo per qualsiasi dispositivo di input. Al contrario, i controlli di selezione in 15x11 pixel sono troppo piccoli per essere usati in modo efficace con il tocco.

![Screenshot che mostra la larghezza e l'altezza dei pulsanti di selezione verso l'alto e verso il basso, misurando 9 DLU (15 pixel) in larghezza di 5 DLU (9 pixel) alta.](images/inter-touch-image14.png)

Tenere presente che la dimensione minima è effettivamente basata sull'area fisica, non sulle metriche di layout, ad esempio pixel o DLU. La ricerca indica che l'area di destinazione minima per un'interazione efficace e accurata usando un dito è 6x6 millimetri (mm). Quest'area si traduce in metriche di layout come la seguente:



| Carattere             | Millimetri | Pixel relativi | Dlu  |
|------------------|-------------|-----------------|-------|
| Segoe UI a 9 punti | 6x6         | 23x23           | 13x13 |
| Tahoma a 8 punte   | 6x6         | 23x23           | 15x14 |



 

Inoltre, la ricerca mostra che una dimensione minima di 10x10 mm (circa 40x40 pixel) consente una maggiore velocità e accuratezza e si ritiene più comoda per gli utenti. Quando possibile, usare questa dimensione maggiore per i pulsanti di comando usati per i comandi più importanti o usati di frequente.

L'obiettivo non è quello di avere controlli giganti, solo quelli che sono facilmente utilizzabili con il tocco.

![Screenshot che mostra la barra degli strumenti di Microsoft Word con il pulsante ' A B C ortografia & grammatica ' evidenziato, con un'altezza di 41 DLU e 40 la larghezza della DLU.](images/inter-touch-image15.png)

In questo esempio Microsoft Word usa i pulsanti più grandi di 10x10 mm per i comandi più importanti.

![Screenshot che mostra il calcolatore di Windows.](images/inter-touch-image16.png)

Questa versione del calcolatore usa i pulsanti più grandi di 10x10 mm per i comandi usati più di frequente.

Non sono disponibili dimensioni perfette per le destinazioni touch. Diverse dimensioni funzionano per situazioni diverse. Le azioni con gravi conseguenze (ad esempio delete e Close) o azioni di uso frequente devono usare destinazioni touch di grandi dimensioni. Le azioni usate raramente con conseguenze minori possono usare destinazioni di piccole dimensioni.

**Linee guida sulle dimensioni di destinazione per i controlli personalizzati**



| Linee guida sulle dimensioni                                                                                 | Descrizione                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![dimensioni minime consigliate per 7x7](images/inter_touch_image10.jpeg)<br/>      | **7x7 mm: dimensioni minime consigliate**<br/> 7x7 mm è una dimensione minima valida se il contatto con la destinazione sbagliata può essere corretto in uno o due movimenti o entro cinque secondi. La spaziatura interna tra destinazioni è altrettanto importante delle dimensioni di destinazione.<br/>                               |
| ![dimensioni consigliate di 9x9 per l'accuratezza](images/inter_touch_image11.jpeg)<br/> | **Quando l'accuratezza è importante**<br/> Chiudere, eliminare e altre azioni con gravi conseguenze non possono permettersi tocchi accidentali. Usare le destinazioni 9x9 mm se per toccare la destinazione sbagliata sono necessari più di due movimenti, cinque secondi o una modifica del contesto principale da correggere.<br/>     |
| ![dimensioni minime 5x5](images/inter_touch_image12.jpeg)<br/>                  | **Quando non si adatta**<br/> Se ci si trova a occuparsi di tutto il necessario, è possibile usare le destinazioni 5x5 mm purché il contatto con la destinazione sbagliata possa essere corretto con un solo gesto. In questo caso, l'utilizzo di 2 mm di spaziatura tra destinazioni è estremamente importante.<br/> |



 

**Linee guida sulle dimensioni di destinazione per i controlli comuni**

-   **Per i controlli comuni, usare le dimensioni del controllo consigliate.** Il dimensionamento del controllo consigliato soddisfa le dimensioni minime del pixel 23x23 (13x13 DLU), tranne che per le caselle di controllo e i pulsanti di opzione (la larghezza del testo compensa leggermente), i controlli di selezione (che non sono utilizzabili con il tocco, ma sono ridondanti) e i separatori.

    ![Screenshot che mostra un esempio di controlli comuni, inclusi i controlli audio, un pulsante "Sfoglia Internet Now" e una finestra Esplora file.](images/inter-touch-image17.png)

    Le dimensioni del controllo consigliate sono facilmente toccabili.

-   **Per i pulsanti di comando usati per i comandi più importanti o usati di frequente, usare una dimensione minima di 40x40 pixel (23x22 DLU) ogni volta che è pratica.** In questo modo si ottiene una maggiore velocità e accuratezza e si ritiene più semplice per gli utenti.

    ![Screenshot che Mostra più dimensioni di un pulsante di invio di un messaggio di posta elettronica con le dimensioni più piccole e più grandi a partire da sinistra verso destra.](images/inter-touch-image18.png)

    Quando si pratica, usare pulsanti di comando di dimensioni maggiori per i comandi più importanti o di uso frequente.

-   **Per altri controlli:**

    -   **Utilizzare destinazioni di clic più grandi.** Per i controlli di dimensioni ridotte, le dimensioni di destinazione sono maggiori dell'elemento dell'interfaccia utente visibile in modo statico. Ad esempio, i pulsanti dell'icona 16x16 pixel possono avere un pixel 23x23 clic sui pulsanti di destinazione e gli elementi di testo possono avere rettangoli di selezione di 8 pixel più larghi del testo e 23 pixel di altezza.

        Versione corretta:

        ![Screenshot che mostra una barra degli strumenti con le dimensioni di destinazione corrette.](images/inter-touch-image19.png)

        Non corretto:

        ![Screenshot che mostra un albero a U I con un'area di destinazione di dimensioni non corrette.](images/inter-touch-image20.png)

        Versione corretta:

        ![Screenshot che mostra un albero di U I con le dimensioni corrette per l'area di destinazione.](images/inter-touch-image21.png)

        Negli esempi corretti, le destinazioni di clic sono più grandi degli elementi dell'interfaccia utente visibili in modo statico.

    -   **USA destinazioni di clic ridondanti.** Se il controllo ha funzionalità ridondanti, è accettabile che le destinazioni di clic siano inferiori alle dimensioni minime.

        Ad esempio, i triangoli di divulgazione progressivi usati dal controllo di visualizzazione albero sono solo 6x9 pixel, ma la loro funzionalità è ridondante con le etichette degli elementi associati.

        ![Screenshot che mostra un albero di U I con destinazioni di clic ridondanti.](images/inter-touch-image22.png)

        I triangoli della visualizzazione albero sono troppo piccoli per essere facilmente toccabili, ma sono ridondanti nella funzionalità con le etichette associate più grandi.

        Rispettare le metriche di sistema. Non impostare come hardcoded le dimensioni. Se necessario, gli utenti possono modificare la metrica del sistema o il valore dpi per adattarlo alle proprie esigenze. Tuttavia, considerarlo come ultima risorsa perché gli utenti in genere non devono modificare le impostazioni di sistema per rendere utilizzabile l'interfaccia utente.

        ![Screenshot che mostra un'altezza di menu standard a sinistra e un'altezza di menu più grande a destra.](images/inter-touch-image23.png)

        In questo esempio la metrica di sistema per l'altezza del menu è stata modificata.

Modifica di testo

La modifica del testo è una delle interazioni più complesse quando si usa un dito. L'uso di controlli vincolati, i valori predefiniti appropriati e il completamento automatico eliminano o riducono la necessità di immettere testo. Tuttavia, se l'app include la modifica del testo, è possibile aumentare la produttività degli utenti eseguendo automaticamente lo zoom dell'interfaccia utente di input fino al 150% per impostazione predefinita quando si usa il tocco.

Un programma di posta elettronica, ad esempio, può visualizzare l'interfaccia utente con le dimensioni normali, ma consente di ingrandire l'interfaccia utente di input al 150% per comporre i messaggi.

![Screenshot che mostra un messaggio di posta elettronica.](images/inter-touch-image24.png)

In questo esempio, l'interfaccia utente di input viene ingrandita al 150%.

### <a name="control-layout-and-spacing"></a>Controllare il layout e la spaziatura

La spaziatura tra i controlli rappresenta un fattore significativo per rendere i controlli facilmente toccabili. La destinazione è più veloce ma meno precisa quando si usa un dito come dispositivo di puntamento, causando più spesso il tocco esterno alla destinazione prevista. Quando i controlli interattivi vengono posizionati molto vicino ma non vengono effettivamente toccati, gli utenti possono fare clic sullo spazio inattivo tra i controlli. Poiché facendo clic su spazio inattivo non è possibile ottenere risultati o commenti visivi, gli utenti spesso non sono sicuri di ciò che si è verificato.

**Modificare dinamicamente la spaziatura in base al dispositivo di input utilizzato.** Questa operazione è particolarmente utile con l'interfaccia utente temporanea, ad esempio menu e riquadri a comparsa.

**Fornire un minimo di 5 pixel (3 DLU) di spazio tra le aree di destinazione dei controlli interattivi.** Se i controlli piccoli sono spaziati troppo attentamente, l'utente deve toccare con precisione per evitare di toccare l'oggetto errato.

**Rendere più semplici i controlli all'interno dei gruppi usando più della spaziatura verticale consigliata tra i controlli.** Ad esempio, i pulsanti di opzione a 19 pixel di altezza sono inferiori alle dimensioni minime consigliate di 23 pixel. Quando si dispone di spazio verticale disponibile, è possibile ottenere approssimativamente lo stesso effetto del ridimensionamento consigliato aggiungendo altri 4 pixel di spaziatura ai 7 pixel standard.

Versione corretta:

![Screenshot che mostra un esempio standard di spaziatura verticale tra i controlli.](images/inter-touch-image25.png)

Migliore:

![Screenshot che mostra un esempio di controlli con spaziatura verticale.](images/inter-touch-image26.png)

Nell'esempio migliore, la spaziatura aggiuntiva tra i pulsanti di opzione rende più semplice la differenziazione.

È possibile che si verifichino situazioni in cui la spaziatura aggiuntiva è utile quando si usa il tocco, ma non quando si usa il mouse o la tastiera. In questi casi, usare una progettazione più spaziosa solo quando viene avviata un'azione tramite il tocco.

**Scegliere un layout in cui posizionare i controlli vicino alla posizione in cui verranno usati con maggiore probabilità.** Tenere le interazioni tra le attività all'interno di una piccola area quando possibile e individuare i controlli vicini alla posizione in cui verranno usati con maggiore probabilità. Evitare movimenti di mano a lungo distanza, in particolare per le attività comuni e per i trascinamenti.

Si consideri che la posizione corrente del puntatore è la più vicina possibile a una destinazione, rendendola semplice da acquisire. In questo modo, i menu di scelta rapida sfruttano appieno la legge di Fitts, così come le mini-barre degli strumenti utilizzate da Microsoft Office.

![Screenshot che mostra un esempio di menu di scelta rapida e una mini-barra degli strumenti da Microsoft Office side-by-side.](images/inter-touch-image27.png)

**Evitare di posizionare piccoli controlli vicino al bordo dell'app o della visualizzazione.** Gli obiettivi più piccoli vicino ai bordi possono essere difficili da toccare (le lunette visualizzate possono interferire con i movimenti di bordo). Per assicurarsi che i controlli siano di facile destinazione quando una finestra viene ingrandita, impostarli almeno 23x23 pixel (13x13 DLU) o posizionarli fuori dal bordo della finestra.

**Utilizzare la spaziatura consigliata.** La spaziatura consigliata è compatibile con il tocco. Tuttavia, se l'app può trarre vantaggio da dimensioni e spaziatura maggiori, prendere in considerazione le dimensioni e la spaziatura consigliate per essere minime quando appropriato.

**Fornire almeno 5 pixel (3 DLU) di spazio tra i controlli interattivi.** In questo modo si evita confusione quando gli utenti toccano al di fuori della destinazione prevista.

Prendere in considerazione l'aggiunta di una spaziatura verticale consigliata all'interno di gruppi di controlli, ad esempio i collegamenti ai comandi, le caselle di controllo e i pulsanti di opzione, oltre che tra i gruppi. In questo modo risulta più semplice distinguere.

**Si consiglia di aggiungere in modo dinamico più di una spaziatura verticale consigliata quando viene avviata un'azione mediante il tocco.** Questa operazione rende gli oggetti più semplici da distinguere, ma senza occupare più spazio quando si usa una tastiera o un mouse. Aumentare la spaziatura del terzo della dimensione normale o di almeno 8 pixel.

![image](images/inter-touch-image28.png)

In questo esempio, le Jump List della barra delle applicazioni di Windows 7 sono più ampie quando vengono visualizzate con il tocco.

### <a name="interaction"></a>Interazione

L'uso dei controlli corretti consente di ottenere solo una parte del modo per un'app ottimizzata per il tocco, ma è necessario considerare anche il modello di interazione complessiva supportato da tali controlli. Di seguito sono riportate alcune linee guida utili per questa operazione.

-   **Rendere ridondante il passaggio del mouse.** Il passaggio del mouse non è supportato dalla maggior parte delle tecnologie touch, quindi gli utenti con tali touchscreen non possono eseguire attività che richiedono il passaggio del mouse.
-   **Per le app che necessitano di input di testo, integra completamente la funzionalità tastiera touch** :
    -   Fornire i valori predefiniti appropriati per l'input dell'utente.
    -   Fornire suggerimenti per il completamento automatico quando appropriato.

    > [!Note]  
    > Sviluppatori: per ulteriori informazioni sull'integrazione della tastiera touch, vedere [**ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel).

     

-   **Consente agli utenti di ingrandire l'interfaccia utente del contenuto se il programma include attività che richiedono la modifica del testo.** Quando si usa il tocco, provare ad applicare lo zoom automatico al 150%.
-   **Fornire una panoramica semplice e reattiva e lo zoom laddove appropriato.** Ricreare rapidamente dopo una panoramica o uno zoom per restare reattivi. Questa operazione è necessaria per fare in modo che la manipolazione diretta sia effettivamente diretta.
-   **Durante una panoramica o uno zoom, assicurarsi che i punti di contatto si trovino sotto il dito per tutto il movimento.** In caso contrario, è difficile controllare la panoramica o lo zoom.
-   **Poiché i movimenti vengono memorizzati, assegnare loro significati coerenti tra le app.** Non assegnare significati diversi ai movimenti con semantica fissa. Usare invece un gesto appropriato specifico dell'app.

### <a name="forgiveness"></a>Perdono

La manipolazione diretta rende il tocco naturale, espressivo, efficiente e accattivante. Tuttavia, se è presente una manipolazione diretta, è possibile che si verifichi una manipolazione accidentale e quindi la necessità di un perdono.

Il perdono è la possibilità di invertire o correggere facilmente un'azione indesiderata. È possibile perdonare un'esperienza di tocco grazie all'annullamento, fornendo un buon feedback visivo, con una separazione fisica chiara tra i comandi di uso frequente e i comandi distruttivi e consentendo agli utenti di correggere facilmente gli errori. Associato al perdono impedisce che si verifichino azioni indesiderate, che è possibile eseguire usando controlli vincolati e conferme per azioni rischiose o comandi con conseguenze impreviste.

-   **Consente di specificare un comando Annulla.** È consigliabile fornire un modo semplice per annullare tutti i comandi, ma è possibile che l'app includa alcuni comandi il cui effetto non può essere annullato.
-   **Ogni volta che si pratica, fornire commenti e suggerimenti sul dito, ma non eseguire azioni fino a finger up.** Questa operazione consente agli utenti di correggere gli errori prima di crearli.
-   **Quando si pratica, consentire agli utenti di correggere facilmente gli errori.** Se un'azione ha effetto sul dito, consentire agli utenti di correggere gli errori scorrendo mentre il dito è ancora inattivo.
-   **Quando pratica, indicare che non è possibile eseguire una manipolazione diretta resistendo allo spostamento.** Consentire l'esecuzione del movimento, ma fare in modo che l'oggetto venga riattivato quando viene rilasciato per indicare chiaramente che l'azione è stata riconosciuta ma non può essere eseguita.
-   **Hanno una separazione fisica chiara tra i comandi usati di frequente e i comandi distruttivi.** In caso contrario, gli utenti potrebbero toccare accidentalmente i comandi distruttivi. Un comando è considerato distruttivo se l'effetto è diffuso e non può essere facilmente annullato o l'effetto non è immediatamente percettibile.
-   **Confermare i comandi per azioni rischiose o comandi con conseguenze impreviste.** Per questo scopo, utilizzare una finestra di dialogo di conferma.
-   **Si consiglia di confermare eventuali altre azioni che gli utenti tendono a eseguire accidentalmente quando si usa il tocco, che non possono essere rilevate o sono difficili da annullare.** In genere, sono denominate conferme di routine e sono sconsigliate a seconda del presupposto che gli utenti non debbano spesso emettere tali comandi per errore con il mouse o la tastiera. Per evitare conferme non necessarie, presentare queste conferme solo se il comando è stato avviato utilizzando il tocco.

    Le conferme di routine sono accettabili per le interazioni che spesso gli utenti usano in modo accidentale.

    Sviluppatori: è possibile distinguere tra gli eventi del mouse e gli eventi di tocco usando l'API di [**\_ \_ origine del messaggio di input**](/windows/win32/api/winuser/ns-winuser-input_message_source) .

