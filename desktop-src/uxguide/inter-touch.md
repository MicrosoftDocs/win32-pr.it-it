---
title: Tocco
description: Tutte le applicazioni Windows Microsoft devono avere un'esperienza di tocco ottimale. La creazione di un'esperienza di questo tipo è più semplice di quanto si pensi.
ms.assetid: a87d0726-1c57-4cf8-9e35-4e73a09ff1a3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 68f73b7da9cf33dc20a3c0534044558e514284f024f11609ef9af4760ec79a8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119029754"
---
# <a name="touch"></a>Tocco

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Tutte le applicazioni Windows Microsoft devono avere un'esperienza di tocco ottimale. La creazione di un'esperienza di questo tipo è più semplice di quanto si pensi.

Il tocco si riferisce all'uso di una o più dita per fornire l'input tramite uno schermo del dispositivo e interagire con Windows e le app. Un'app ottimizzata per il tocco ha un'interfaccia utente e un modello di interazione progettati per supportare le aree di contatto più grandi e meno precise, i vari fattori di forma dei dispositivi touch e le numerose posture e punti di controllo che gli utenti potrebbero adottare quando usano un dispositivo a tocco.

![Interazione dell'utente con il tablet tramite tocco](images/inter_touch_image1.jpeg)

Ogni dispositivo di input ha i propri punti di forza. La tastiera è ideale per l'input di testo e per l'esecuzione di comandi con un movimento minimo della mano. Il mouse è ideale per un puntamento efficiente e preciso. Il tocco è ideale per la manipolazione degli oggetti e l'esecuzione di semplici comandi. Una penna è ideale per l'espressione in formato libero, come per la scrittura manuale e il disegno.

Windows 8.1 è ottimizzato per velocità di risposta, accuratezza e facilità d'uso con il tocco, supportando al tempo stesso completamente i metodi di input tradizionali, ad esempio mouse, penna e tastiera. La velocità, l'accuratezza e il feedback tattile forniti dalla modalità di input tradizionale sono familiari e accattivanti per molti utenti e potenzialmente più adatti a scenari di interazione specifici.

È possibile trovare linee guida relative a mouse, penna e accessibilità in argomenti separati.

Quando si pensa all'esperienza di interazione per l'app:

Non presupporre che se un'interfaccia utente funziona bene per un mouse, funziona bene anche per il tocco. Anche se un buon supporto del mouse è un punto di partenza, un'esperienza di tocco ottimale presenta alcuni requisiti aggiuntivi.

Presupporre che se un'interfaccia utente funziona bene per un dito, funziona bene anche per una penna. Rendere l'app toccabile è un ottimo modo per fornire anche un buon supporto per la penna. La differenza principale è che le dita hanno una mancia blunter, quindi necessitano di destinazioni più grandi.

Con il tocco è possibile modificare direttamente gli oggetti e l'interfaccia utente, in modo da ottenere un'esperienza più rapida, naturale e coinvolgente.

## <a name="provide-a-great-touch-experience"></a>Offrire un'esperienza di tocco ottimale

È necessario assicurarsi che gli utenti possano eseguire in modo efficiente attività importanti e critiche usando l'input tocco. Tuttavia, funzionalità specifiche dell'app, ad esempio la manipolazione di testo o pixel, potrebbero non essere adatte al tocco e possono essere riservate al dispositivo di input più adatto.

Se non si ha molta esperienza nello sviluppo di app per il tocco, è meglio imparare a farlo. Ottenere un computer abilitato per il tocco, mettere da parte il mouse e la tastiera e usare solo le dita per interagire con l'app. Se si dispone di un tablet, provare a posizionarlo in posizioni diverse, ad esempio in grembo, in un tavolo o tra le mani mentre si è in piedi. Provare a usarlo con orientamento verticale e orizzontale.

Le app ottimizzate per il tocco che funzionano meglio con l'interazione tramite tocco sono in genere:

-   **Naturale e intuitivo.** Le interazioni sono progettate per corrispondere al modo in cui gli utenti interagiscono con gli oggetti nel mondo reale.
-   **Meno intrusivo.** L'uso del tocco è invisibile all'utente e di conseguenza è molto meno distrazione rispetto alla digitazione o al clic.
-   **Portatile.** I dispositivi touch sono più compatti perché molte attività possono essere completate senza tastiera, mouse, penna o touchpad. Sono anche più flessibili perché non è necessaria una superficie di lavoro.
-   **Diretto e coinvolgente.** Il tocco consente di modificare direttamente gli oggetti sullo schermo.
-   **Meno accurato.** Gli utenti non possono impostare come destinazione gli oggetti con il tocco in modo accurato rispetto a un mouse o una penna.

Il tocco offre un'interazione naturale e reale. La manipolazione diretta e l'animazione completano questa impressione, offrendo agli oggetti un movimento realistico e dinamico e un feedback. Si consideri, ad esempio, un gioco di carte. Non solo è comodo e facile trascinare le carte usando un dito, ma l'esperienza assume un'esperienza coinvolgente nel mondo reale quando è possibile scorrere, planare e ruotare le carte esattamente come si farebbe con un mazzo fisico. E quando si prova a spostare una scheda che non può essere spostata, è meglio fare in modo che la carta si distorsi, ma non impedirne il movimento, e riposta al momento del rilascio, per indicare chiaramente che l'azione è stata riconosciuta ma non può essere eseguita.

Fortunatamente, se l'app è già ben progettata, è facile offrire un'esperienza di tocco ottimale. A questo scopo, un programma ben progettato:

-   **Garantisce che le attività più** importanti possano essere eseguite in modo efficiente usando un dito (almeno le attività che non comportano una grande quantità di digitazione o la manipolazione dettagliata dei pixel).
-   **Usa controlli di grandi dimensioni per il tocco.** I controlli comuni hanno una dimensione minima di 23x23 pixel (13 dLU x 13) e i controlli usati più di frequente sono almeno 40x40 pixel (23 x 22 DLU). Per evitare un comportamento che non risponde, gli elementi dell'interfaccia utente devono avere almeno 5 pixel (3 DLU) di spazio tra di essi. Per gli altri controlli, assicurarsi di avere almeno un obiettivo di clic di almeno 23x23 pixel (13x13 DLU), anche se l'aspetto statico è molto più piccolo. Vedere Ridimensionamento dei controlli standard.
-   **Supporta l'input del mouse.** I controlli interattivi hanno affordance chiari e visibili. Gli oggetti hanno comportamenti standard per le interazioni con il mouse standard (clic singolo e doppio clic, clic con il pulsante destro del mouse, trascinamento del mouse e passaggio del mouse).
-   **Supporta l'input da tastiera.** L'app fornisce assegnazioni standard di tasti di scelta rapida, in particolare per i comandi di spostamento e modifica che possono essere generati anche tramite movimenti tocco.
-   **Garantisce l'accessibilità.** Usa Automazione interfaccia utente o Microsoft Active Accessibility (MSAA) per fornire l'accesso a livello di codice all'interfaccia utente per assistive technology. L'app risponde in modo appropriato alle modifiche di orientamento, tema, impostazioni locali e metriche di sistema.
-   **Elimina le interazioni non necessarie.** Per evitare la perdita di dati o di accesso al sistema, usare i valori predefiniti più sicuri e sicuri. Se la sicurezza e la sicurezza non sono fattori, l'app seleziona l'opzione più probabile o comoda.
-   **Fornisce un equivalente tocco per il passaggio del mouse.** Non fare affidamento sul passaggio del mouse come unico modo per eseguire un'azione.
-   **Assicura che i movimenti siano immediatamente effettive.** Mantenere i punti di contatto sotto le dita dell'utente senza problemi durante tutto il movimento, che fornisce l'effetto del mapping del movimento direttamente al movimento dell'utente.
-   **Usa i movimenti standard quando possibile.** Movimenti personalizzati solo per le interazioni univoche per l'app.
-   **Garantisce che i comandi indesiderati o distruttivi possano essere invertito o corretti.** Le azioni accidentali sono più probabili quando si usa il tocco.

## <a name="guidelines-for-touch-input"></a>Linee guida per l'input tocco

Con il tocco, l Windows app può usare movimenti fisici per emulare la manipolazione diretta degli elementi dell'interfaccia utente.

Quando si progetta un'app abilitata per il tocco, tenere presenti le procedure consigliate seguenti:

**La velocità di risposta è essenziale per la creazione di esperienze di tocco che si senta diretta e coinvolgente.** Per essere diretti, i movimenti devono avere effetto immediato e i punti di contatto di un oggetto devono rimanere sotto le dita dell'utente in modo uniforme durante tutto il movimento. L'effetto dell'input tocco deve essere mappato direttamente al movimento dell'utente, quindi, ad esempio, se l'utente ruota le dita di 90 gradi, anche l'oggetto dovrebbe ruotare di 90 gradi. Qualsiasi ritardo, risposta concisa, perdita di contatto o risultati non accurati elimina la percezione di manipolazione diretta e anche di qualità.

**La coerenza è essenziale per la creazione di esperienze di tocco naturali e intuitive.** Quando gli utenti apprendono un movimento standard, si aspettano che il movimento abbia lo stesso effetto in tutte le app. Per evitare confusione e frustrazione, non assegnare mai significati non standard ai movimenti standard. Usare invece movimenti personalizzati per le interazioni univoche per il programma.

Verrà ora descritto il linguaggio Windows touch, ma prima di procedere, ecco un breve elenco di termini di base per l'input tocco.

-   **Movimento**

    Un movimento è l'azione fisica o il movimento eseguito sul dispositivo di input (dito, dita, penna/stilo, mouse e così via). Ad esempio, per avviare, attivare o richiamare un comando, si usa un tocco con un solo dito per un dispositivo touch o touchpad (equivalente a un clic con il pulsante sinistro del mouse, a un tocco con una penna o a INVIO su una tastiera).

-   **Manipolazione**

    Una manipolazione è la reazione immediata in tempo reale o la risposta che un oggetto o un'interfaccia utente ha a un movimento. Ad esempio, sia i movimenti di scorrimento che di scorrimento rapido causano in genere lo spostamento di un elemento o di un'interfaccia utente.

    Il risultato finale di una manipolazione, come viene manifestato dall'oggetto sullo schermo e nell'interfaccia utente, è l'interazione.

-   **Interazione**

    Le interazioni dipendono dal modo in cui viene interpretata una manipolazione e dal comando o dall'azione che risulta dalla manipolazione. Ad esempio, gli oggetti possono essere spostati usando i movimenti di scorrimento e scorrimento rapido, ma i risultati variano a seconda che sia stata superata una soglia di distanza. La diapositiva può essere usata per trascinare un oggetto o eseguire una panoramica di una visualizzazione mentre lo scorrimento rapido può essere usato per selezionare un elemento o visualizzare una barra dell'app.

### <a name="the-windows-touch-language"></a>Lingua Windows tocco

Windows fornisce un set conciso di interazioni tramite tocco usate in tutto il sistema. L'applicazione coerente di questo linguaggio di tocco rende l'app familiare a ciò che gli utenti conoscono già. Ciò aumenta la fiducia degli utenti rendendo l'app più facile da apprendere e usare. Per altre informazioni sull'implementazione del linguaggio di tocco, vedere Movimenti, manipolazioni e interazioni.

**Tenere premuto per apprendere**

Il movimento tieni premuto visualizza informazioni dettagliate o oggetti visivi didattici (ad esempio, una descrizione comando o un menu di scelta rapida) senza eseguire il commit in un'azione o in un comando. La panoramica è comunque possibile se viene avviato un movimento scorrevole mentre viene visualizzato l'oggetto visivo.

> [!IMPORTANT]
> È possibile premere e tenere premuto per la selezione nei casi in cui è abilitata la panoramica orizzontale e verticale.

 

Stato di immissione: una o due dita in contatto con lo schermo.

Movimento: nessun movimento.

Stato di uscita: l'ultimo dito verso l'alto termina il movimento.

Effetto: visualizzare altre informazioni.

![premere \- il tocco per \- \-learn.png](images/inter-touch-image2.png)

Movimento di pressione e pressione.

**Passaggio del mouse**

Il passaggio del mouse è un'interazione utile perché consente agli utenti di ottenere informazioni aggiuntive tramite suggerimenti prima di avviare un'azione. La visualizzazione di questi suggerimenti fa sì che gli utenti si sentano più sicuri e riduca gli errori.

Sfortunatamente, il passaggio del mouse non è supportato dalle tecnologie di tocco, quindi gli utenti non possono passare il puntatore del mouse quando si usa un dito. La soluzione semplice a questo problema consiste nell'sfruttare appieno il passaggio del mouse, ma solo in modi che non sono necessari per eseguire un'azione. In pratica, ciò significa in genere che l'azione può essere eseguita anche facendo clic, ma non necessariamente nello stesso modo.

![Screenshot che mostra un esempio di interazione al passaggio del mouse accanto a un esempio dell'azione di clic.](images/inter-touch-image13.png)

In questo esempio, gli utenti possono visualizzare la data odierna passando il puntatore del mouse o facendo clic.

**Toccare per l'azione primaria**

Toccando un elemento viene richiamata l'azione primaria, ad esempio l'avvio di un'app o l'esecuzione di un comando.

Stato di immissione: un dito in contatto con lo schermo o il touchpad e alzato prima che si verifichi la soglia di tempo per un'interazione con pressione.

Movimento: nessun movimento.

Stato di uscita: il dito verso l'alto termina il movimento.

Effetto: avviare un'app o eseguire un comando.

![toccare \- il \-primary.png](images/inter-touch-image3.png)

Movimento di tocco.

**Scorrere per eseguire la panoramica**

La diapositiva viene usata principalmente per le interazioni di panoramica, ma può essere usata anche per lo spostamento (in cui la panoramica è vincolata a una direzione), il disegno o la scrittura. La diapositiva può essere usata anche per scegliere come destinazione elementi piccoli e densamente imballati mediante lo scrubbing (scorrendo il dito sugli oggetti correlati, ad esempio i pulsanti di opzione).

Stato di immissione: una o due dita in contatto con lo schermo.

Movimento: trascinare, con eventuali dita aggiuntive rimanenti nella stessa posizione l'una rispetto all'altra.

Stato di uscita: l'ultimo dito verso l'alto termina il movimento.

Effetto: spostare l'oggetto sottostante direttamente e immediatamente mentre le dita si spostano. Assicurarsi di mantenere il punto di contatto sotto il dito durante il movimento.

![toccare \-slide.png](images/inter-touch-image4.png)

Movimento di panoramica.

**Scorrere rapidamente per selezionare, comando e spostare**

Scorrendo il dito a breve distanza, perpendicolare alla direzione di panoramica (in cui la panoramica è vincolata a una direzione), seleziona gli oggetti in un elenco o in una griglia. Visualizzare la barra dell'app con i comandi pertinenti quando vengono selezionati gli oggetti.

Stato di immissione: una o più dita toccano lo schermo.

Movimento: trascinare una breve distanza e alzare prima che si verifichi la soglia di distanza per un'interazione di spostamento.

Stato di uscita: l'ultimo dito verso l'alto termina il movimento.

Effetto: l'oggetto sottostante viene selezionato o spostato oppure viene visualizzata la barra dell'app. Assicurarsi di mantenere il punto di contatto sotto il dito durante il movimento.

![d: \\ sdkenlistment \\ m \- ux design m \- \\ \- ux design images touch \- \\ \\ \-swipe.png](images/inter-touch-image5.png)

Movimento di scorrimento rapido.

**Avvicinamento e allontanamento delle dita per operazioni di zoom**

I movimenti delle dita e delle dita vengono usati per tre tipi di interazioni: zoom ottico, ridimensionamento e zoom semantico.

Lo zoom ottico regola il livello di ingrandimento dell'intera area del contenuto per ottenere una visualizzazione più dettagliata del contenuto. Al contrario, il ridimensionamento è una tecnica per regolare le dimensioni relative di uno o più oggetti all'interno di un'area di contenuto senza modificare la visualizzazione nell'area del contenuto.

Lo zoom semantico è una tecnica ottimizzata per il tocco per la presentazione e lo spostamento di dati strutturati o contenuto all'interno di una singola visualizzazione (ad esempio la struttura di cartelle di un computer, una raccolta di documenti o un album di foto) senza la necessità di panoramica, scorrimento o controlli di visualizzazione albero. Lo zoom semantico offre due diverse visualizzazioni dello stesso contenuto consentendo di visualizzare più dettagli mentre si esegue lo zoom avanti e meno dettagli quando si esegue lo zoom indietro.

Stato di ingresso: due dita in contatto con lo schermo contemporaneamente.

Movimento: le dita si allontanano (allungano) o insieme (avvicinano le dita) lungo un asse.

Stato di uscita: qualsiasi dito verso l'alto termina il movimento.

Effetto: ingrandire o ridurre l'oggetto sottostante direttamente e immediatamente quando le dita si separano o si avvicinano sull'asse. Assicurarsi di mantenere i punti di contatto sotto il dito durante il movimento.

![destinazione \-areazoom.png](images/inter-touch-image6.png)

Movimento di zoom.

**Ruotare per ruotare**

La rotazione con due o più dita causa la rotazione di un oggetto. Ruotare il dispositivo per far ruotare l'intero schermo.

Stato di ingresso: due dita in contatto con lo schermo contemporaneamente.

Movimento: una o entrambe le dita ruotano intorno all'altra, spostandosi perpendicolare alla linea tra di esse.

Stato di uscita: qualsiasi dito verso l'alto termina il movimento.

Effetto: ruotare l'oggetto sottostante nella stessa quantità di rotazione delle dita. Assicurarsi di mantenere i punti di contatto sotto il dito durante il movimento.

![toccare \-turn.png](images/inter-touch-image7.png)

Movimento di rotazione.

La rotazione ha senso solo per determinati tipi di oggetti, quindi non viene mappata a un sistema Windows interazione.

La rotazione viene spesso eseguita in modo diverso da persone diverse. Alcuni preferiscono ruotare un dito intorno a un dito pivot, mentre altri preferiscono ruotare entrambe le dita in un movimento circolare. La maggior parte delle persone usa una combinazione dei due, con un dito che si sposta più dell'altro. Anche se la rotazione uniforme a qualsiasi angolo è l'interazione migliore, in molti contesti, ad esempio la visualizzazione di foto, è meglio stabilirsi alla rotazione di 90 gradi più vicina quando l'utente si lascia andare. Nella modifica di foto è possibile usare una piccola rotazione per raddrizzare la foto.

**Scorrere rapidamente dal bordo per i comandi dell'app**

Scorrendo il dito a breve distanza dal bordo inferiore o superiore dello schermo vengono visualizzati i comandi dell'app in una barra dell'app.

Stato di ingresso: una o più dita toccano la cornice.

Movimento: trascinare una breve distanza sullo schermo e sollevarlo.

Stato di uscita: l'ultimo dito verso l'alto termina il movimento.

Effetto: viene visualizzata la barra dell'app.

![tocco \- scorrere rapidamente in basso \- \-edge.png](images/inter-touch-image8.png)

![tocco \- \- scorrimento \- lateraleedge.png](images/inter-touch-image9.png)

Movimento di scorrimento rapido dal bordo.

Sviluppatori: per altre informazioni, vedere [**Enumerazione DIRECTMANIPULATION \_ CONFIGURATION.**](/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_configuration)

### <a name="control-usage"></a>Controllare l'utilizzo

In questo caso vengono fornite alcune linee guida per ottimizzare i controlli per l'utilizzo del tocco.

-   **Usare controlli comuni.** I controlli più comuni sono progettati per supportare una buona esperienza di tocco.
-   **Scegliere controlli personalizzati progettati per supportare il tocco.** Potrebbero essere necessari controlli personalizzati per supportare le esperienze speciali del programma. Scegliere controlli personalizzati che:
    -   Le dimensioni possono essere sufficientemente grandi da facilitando la destinazione e la manipolazione.
    -   Quando vengono manipolati, spostare e reagire nel modo in cui gli oggetti reali si spostano e reagiscono, ad esempio con un momento di forza e attrito.
    -   Perdoni consentendo agli utenti di correggere facilmente gli errori.
    -   Si perdoni l'inaccurabilità con il clic e il trascinamento. Gli oggetti eliminati vicino alla destinazione devono essere posizionati nella posizione corretta.
    -   Avere un feedback visivo chiaro quando il dito è sopra il controllo.
-   **Usare i controlli vincolati.** I controlli vincolati, ad esempio elenchi e dispositivi di scorrimento, se progettati per la destinazione con tocco semplice, possono essere migliori rispetto ai controlli senza vincoli, ad esempio le caselle di testo, perché riducono la necessità di input di testo.
-   **Specificare i valori predefiniti appropriati.** Selezionare l'opzione più sicura (per evitare la perdita di dati o l'accesso al sistema) e l'opzione più sicura per impostazione predefinita. Se la sicurezza e la sicurezza non sono fattori, selezionare l'opzione più probabile o conveniente, eliminando così l'interazione non necessaria.
-   **Fornire il completamento automatico del testo.** Fornisce un elenco dei valori più probabili, o dei valori di input più recenti, per semplificare molto l'input di testo.
-   **Per le attività importanti che** usano la selezione multipla, se in genere viene usato un elenco a selezione multipla standard, fornire un'opzione per usare un elenco di caselle di controllo.

### <a name="control-sizes-and-touch-targeting"></a>Dimensioni dei controlli e destinazione del tocco

A causa della grande superficie della punta delle dita, i piccoli controlli troppo vicini possono essere difficili da usare con precisione.

Come regola generale, una dimensione di controllo di 23x23 pixel (13 x 13 DLU) è una buona dimensione minima del controllo interattivo per qualsiasi dispositivo di input. Al contrario, i controlli di selezione a 15 x 11 pixel sono troppo piccoli per essere usati in modo efficace con il tocco.

![Screenshot che mostra la larghezza e l'altezza dei pulsanti di selezione verso l'alto e verso il basso, misurando 9 DLAN (15 pixel) di larghezza per 5 DLU (9 pixel).](images/inter-touch-image14.png)

Tenere presente che le dimensioni minime sono realmente basate sull'area fisica, non sulle metriche di layout, ad esempio pixel o DLU. La ricerca indica che l'area di destinazione minima per un'interazione efficiente e accurata con un dito è di 6x6 millimetri (mm). Questa area si traduce in metriche di layout come le seguenti:



| Carattere             | Millimetri | Pixel relativi | DLO  |
|------------------|-------------|-----------------|-------|
| 9 punti Segoe UI | 6x6         | 23x23           | 13x13 |
| Tahoma a 8 punti   | 6x6         | 23x23           | 15x14 |



 

Inoltre, la ricerca mostra che una dimensione minima di 10x10 mm (circa 40 x 40 pixel) consente una maggiore velocità e accuratezza, oltre a essere più comoda per gli utenti. Quando pratico, usare queste dimensioni maggiori per i pulsanti di comando usati per i comandi più importanti o usati di frequente.

L'obiettivo non è avere controlli enormi, ma solo quelli facilmente usati con il tocco.

![Screenshot che mostra la barra Microsoft Word barra degli strumenti con il pulsante "Grammatica & ortografia A B C" evidenziato, con un'altezza di 41 DLU e una larghezza di 40 DLU.](images/inter-touch-image15.png)

In questo esempio, Microsoft Word pulsanti maggiori di 10x10 mm per i comandi più importanti.

![Screenshot che mostra il Windows calcolatore.](images/inter-touch-image16.png)

Questa versione di Calculator usa pulsanti maggiori di 10x10 mm per i comandi usati più di frequente.

Non esistono dimensioni ideali per le destinazioni di tocco. Dimensioni diverse funzionano in situazioni diverse. Le azioni con conseguenze gravi (ad esempio eliminazione e chiusura) o azioni usate di frequente devono usare destinazioni di tocco di grandi dimensioni. Le azioni usate raramente con conseguenze minori possono usare obiettivi di piccole dimensioni.

**Linee guida sulle dimensioni di destinazione per i controlli personalizzati**



| Linee guida per le dimensioni                                                                                 | Descrizione                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![Dimensioni minime consigliate 7x7](images/inter_touch_image10.jpeg)<br/>      | **7x7 mm: dimensioni minime consigliate**<br/> 7x7 mm è una buona dimensione minima se toccare la destinazione errata può essere corretta in uno o due movimenti o entro cinque secondi. La spaziatura interna tra le destinazioni è importante quanto le dimensioni di destinazione.<br/>                               |
| ![Dimensioni consigliate 9x9 per l'accuratezza](images/inter_touch_image11.jpeg)<br/> | **Quando è importante l'accuratezza**<br/> Le azioni di chiusura, eliminazione e altre azioni con conseguenze gravi non possono permettersi tocchi accidentali. Usare destinazioni da 9 x 9 mm se il tocco della destinazione errata richiede più di due movimenti, cinque secondi o una modifica di contesto importante da correggere.<br/>     |
| ![Dimensioni minime di 5x5](images/inter_touch_image12.jpeg)<br/>                  | **Quando semplicemente non si adatta**<br/> Se ci si trova a cercare di adattare le cose, è possibile usare destinazioni da 5 x 5 mm, purché toccare la destinazione errata possa essere corretta con un solo movimento. L'uso di 2 mm di spaziatura interna tra destinazioni è estremamente importante in questo caso.<br/> |



 

**Linee guida sulle dimensioni di destinazione per i controlli comuni**

-   **Per i controlli comuni, usare le dimensioni di controllo consigliate.** Il ridimensionamento consigliato del controllo soddisfa le dimensioni minime di 23x23 pixel (13x13 DLU), ad eccezione delle caselle di controllo e dei pulsanti di opzione (la larghezza del testo compensa in qualche modo), i controlli di selezione (che non sono utilizzabili con il tocco, ma ridondanti) e le barre di divisione.

    ![Screenshot che mostra un esempio di controlli comuni, inclusi i controlli audio, un pulsante "Esplora Internet ora" e una Esplora file finestra.](images/inter-touch-image17.png)

    Le dimensioni di controllo consigliate sono facilmente toccabili.

-   **Per i pulsanti di comando usati per i comandi più importanti o usati di frequente, usare una dimensione minima di 40 x 40 pixel (23 x 22 DLU) quando pratico.** In questo modo si generano velocità e accuratezza migliori, oltre a essere più confortevoli per gli utenti.

    ![Screenshot che mostra più dimensioni del pulsante "Invia" di un messaggio di posta elettronica, con le dimensioni da più piccole a più grandi che iniziano da sinistra a destra.](images/inter-touch-image18.png)

    In qualsiasi momento pratico, usare pulsanti di comando più grandi per comandi importanti o usati di frequente.

-   **Per altri controlli:**

    -   **Usare destinazioni clic di dimensioni maggiori.** Per i controlli di piccole dimensioni, rendere le dimensioni di destinazione maggiori rispetto all'elemento dell'interfaccia utente visibile in modo statico. Ad esempio, i pulsanti icona 16x16 pixel possono avere pulsanti di destinazione del clic di 23 x 23 pixel e gli elementi di testo possono avere rettangoli di selezione di 8 pixel più larghi del testo e 23 pixel di altezza.

        Versione corretta:

        ![Screenshot che mostra una barra degli strumenti con le dimensioni di destinazione corrette.](images/inter-touch-image19.png)

        Non corretto:

        ![Screenshot che mostra un albero U I con un'area di destinazione con dimensioni errati.](images/inter-touch-image20.png)

        Versione corretta:

        ![Screenshot che mostra un albero U I con le dimensioni corrette per l'area di destinazione.](images/inter-touch-image21.png)

        Negli esempi corretti, le destinazioni clic sono più grandi degli elementi dell'interfaccia utente visibili in modo statico.

    -   **Usare destinazioni click ridondanti.** È accettabile che le destinazioni clic siano inferiori alle dimensioni minime se il controllo dispone di funzionalità ridondanti.

        Ad esempio, i triangoli di divulgazione progressiva usati dal controllo visualizzazione albero sono di soli 6x9 pixel, ma la relativa funzionalità è ridondante con le etichette degli elementi associate.

        ![Screenshot che mostra un albero U I con destinazioni click ridondanti.](images/inter-touch-image22.png)

        I triangoli della visualizzazione albero sono troppo piccoli per essere facilmente toccabili, ma sono ridondanti nella funzionalità con le etichette associate più grandi.

        Rispettare le metriche di sistema. Non codificare le dimensioni. Se necessario, gli utenti possono modificare le metriche di sistema o dpi in base alle proprie esigenze. Tuttavia, considerare questo come ultima risorsa perché gli utenti non devono in genere modificare le impostazioni di sistema per rendere utilizzabile l'interfaccia utente.

        ![Screenshot che mostra un'altezza di menu standard a sinistra e un'altezza del menu più grande a destra.](images/inter-touch-image23.png)

        In questo esempio la metrica di sistema per l'altezza del menu è stata modificata.

Modifica di testo

La modifica del testo è una delle interazioni più difficili quando si usa un dito. L'uso di controlli vincolati, valori predefiniti appropriati e completamento automatico elimina o riduce la necessità di immettere testo. Se tuttavia l'app prevede la modifica del testo, è possibile aumentare la produttività degli utenti zoomando automaticamente l'interfaccia utente di input fino al 150% per impostazione predefinita quando si usa il tocco.

Ad esempio, un programma di posta elettronica potrebbe visualizzare l'interfaccia utente con dimensioni normali modificabili, ma zoomare l'interfaccia utente di input al 150% per comporre i messaggi.

![Screenshot che mostra un messaggio di posta elettronica dell'utente.](images/inter-touch-image24.png)

In questo esempio, l'interfaccia utente di input viene ingrandita al 150%.

### <a name="control-layout-and-spacing"></a>Layout e spaziatura dei controlli

La spaziatura tra i controlli è un fattore significativo per rendere i controlli facilmente toccabili. Il targeting è più rapido ma meno preciso quando si usa un dito come dispositivo di puntamento, con conseguente tocco più frequente all'esterno della destinazione prevista. Quando i controlli interattivi vengono posizionati molto vicini ma non sono effettivamente toccati, gli utenti possono fare clic sullo spazio inattivo tra i controlli. Poiché fare clic su spazio inattivo non ha alcun risultato o feedback visivo, gli utenti sono spesso incerti su cosa sia andato storto.

**Regolare dinamicamente la spaziatura in base al dispositivo di input usato.** Ciò è particolarmente utile con l'interfaccia utente temporanea, ad esempio menu e riquadri a comparsa.

**Fornire almeno 5 pixel (3 DLO) di spazio tra le aree di destinazione dei controlli interattivi.** Se i controlli di piccole dimensioni sono troppo spaziosi, l'utente deve toccare con precisione per evitare di toccare l'oggetto errato.

**Rendere i controlli all'interno dei gruppi più facili da distinguere usando più della spaziatura verticale consigliata tra i controlli.** Ad esempio, i pulsanti di opzione con un'altezza di 19 pixel sono più brevi della dimensione minima consigliata di 23 pixel. Quando è disponibile spazio verticale, è possibile ottenere approssimativamente lo stesso effetto del ridimensionamento consigliato aggiungendo altri 4 pixel di spaziatura ai 7 pixel standard.

Versione corretta:

![Screenshot che mostra un esempio standard di spaziatura verticale tra i controlli.](images/inter-touch-image25.png)

Migliore:

![Screenshot che mostra un esempio di controlli con spaziatura più verticale.](images/inter-touch-image26.png)

Nell'esempio migliore, la spaziatura aggiuntiva tra i pulsanti di opzione li rende più facili da distinguere.

In alcune situazioni può essere utile una spaziatura aggiuntiva quando si usa il tocco, ma non quando si usa il mouse o la tastiera. In questi casi, usare una progettazione più semplice solo quando un'azione viene avviata tramite tocco.

**Scegliere un layout che posiziona i controlli vicino alla posizione in cui è più probabile che verranno usati.** Mantenere le interazioni tra attività all'interno di una piccola area quando possibile e individuare i controlli vicino al punto in cui è più probabile che verranno usati. Evitare movimenti della mano a distanza lunga, soprattutto per le attività comuni e per i trascinamenti.

Si consideri che la posizione corrente del puntatore è la più vicina possibile a una destinazione, rendendo semplice l'acquisizione. Di conseguenza, i menu di scelta rapida sfruttano appieno la legge di Fitts, così come le mini-barre degli strumenti usate Microsoft Office.

![Screenshot che mostra un esempio di menu di scelta rapida e una barra degli strumenti Microsoft Office affiancata.](images/inter-touch-image27.png)

**Evitare di posizionare piccoli controlli vicino al bordo dell'app o allo schermo.** Le destinazioni di piccole dimensioni vicino ai bordi possono essere difficili da toccare (le cornice di visualizzazione possono interferire con i movimenti dei bordi). Per assicurarsi che i controlli siano facili da impostare come destinazione quando una finestra è ingrandita, impostarli almeno su 23x23 pixel (13 DLU x 13) o posizionarli al di fuori del bordo della finestra.

**Usare la spaziatura consigliata.** La spaziatura consigliata è touch-friendly. Tuttavia, se l'app può trarre vantaggio da dimensioni e spaziature più grandi, prendere in considerazione il ridimensionamento e la spaziatura consigliati come minimi quando appropriato.

**Fornire almeno 5 pixel (3 DLO) di spazio tra i controlli interattivi.** In questo modo si evita confusione quando gli utenti toccano all'esterno della destinazione prevista.

Prendere in considerazione l'aggiunta di più della spaziatura verticale consigliata all'interno di gruppi di controlli, ad esempio collegamenti di comando, caselle di controllo e pulsanti di opzione, nonché tra i gruppi. In questo modo è più facile distinguerli.

**Prendere in considerazione l'aggiunta dinamica di più della spaziatura verticale consigliata quando un'azione viene avviata tramite tocco.** In questo modo gli oggetti sono più facili da distinguere, ma senza occupare più spazio quando si usa una tastiera o un mouse. Aumentare la spaziatura di un terzo delle dimensioni normali o di almeno 8 pixel.

![image](images/inter-touch-image28.png)

In questo esempio, le jump list Windows 7 della barra delle applicazioni sono più disincise quando vengono visualizzate tramite tocco.

### <a name="interaction"></a>Interazione

L'uso dei controlli corretti consente di accedere solo a un'app ottimizzata per il tocco. È anche necessario prendere in considerazione il modello di interazione generale che questi controlli supportano. Di seguito sono riportate alcune linee guida utili a questo scopo.

-   **Rendere ridondante il passaggio del mouse.** Il passaggio del mouse non è supportato dalla maggior parte delle tecnologie di tocco, quindi gli utenti con tali touchscreen non possono eseguire attività che richiedono il passaggio del mouse.
-   **Per le app che necessitano di input di testo, integrare completamente la funzionalità della tastiera virtuale:**
    -   Fornire i valori predefiniti appropriati per l'input dell'utente.
    -   Fornire suggerimenti di completamento automatico quando appropriato.

    > [!Note]  
    > Sviluppatori: per altre informazioni sull'integrazione della tastiera virtuale, vedi [**ITextInputPanel.**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)

     

-   **Consentire agli utenti di ingrandire l'interfaccia utente del contenuto se il programma ha attività che richiedono la modifica del testo.** È consigliabile ingrandire automaticamente al 150% quando si usa il tocco.
-   **Offrire panoramica e zoom uniformi e reattivi, laddove appropriato.** Ridisegnare rapidamente dopo una panoramica o uno zoom per rimanere reattivi. Questa operazione è necessaria per fare in modo che la manipolazione diretta sia realmente diretta.
-   **Durante una panoramica o uno zoom, assicurarsi che i punti di contatto rimangano sotto il dito durante tutto il movimento.** In caso contrario, la panoramica o lo zoom è difficile da controllare.
-   **Poiché i movimenti vengono memorizzati, assegnare loro significati coerenti tra le app.** Non assegnare significati diversi ai movimenti con semantica fissa. Usare invece un movimento specifico dell'app appropriato.

### <a name="forgiveness"></a>Perdono

La manipolazione diretta rende il tocco naturale, espressivo, efficiente e coinvolgente. Tuttavia, in caso di manipolazione diretta, può essere presente una manipolazione accidentale e quindi la necessità di erre.

Erre è la possibilità di invertire o correggere facilmente un'azione indesiderata. Si crea un'esperienza di tocco con la possibilità di annullare, fornire un buon feedback visivo, avere una netta separazione fisica tra i comandi usati di frequente e i comandi distruttivi e consentire agli utenti di correggere facilmente gli errori. L'associazione a constrained impedisce in primo luogo l'esecuzione di azioni indesiderate, operazione che è possibile eseguire usando controlli vincolati e conferme per azioni rischiose o comandi con conseguenze impreviste.

-   **Specificare un comando Annulla.** È meglio fornire un modo semplice per annullare tutti i comandi, ma l'app potrebbe avere alcuni comandi il cui effetto non può essere annullato.
-   **Quando possibile, fornire un buon feedback sul dito verso il basso, ma non intraprendere azioni fino a quando il dito non viene alzato.** In questo modo gli utenti possono correggere gli errori prima di commetterli.
-   **Quando possibile, consentire agli utenti di correggere facilmente gli errori.** Se un'azione ha effetto sul dito verso l'alto, consentire agli utenti di correggere gli errori scorrendo mentre il dito è ancora in basso.
-   **Quando possibile, indicare che una manipolazione diretta non può essere eseguita con il movimento.** Consentire l'esecuzione dello spostamento, ma fare in modo che l'oggetto si sistema quando viene rilasciato per indicare chiaramente che l'azione è stata riconosciuta ma non può essere eseguita.
-   **Avere una netta separazione fisica tra i comandi usati di frequente e i comandi distruttivi.** In caso contrario, gli utenti potrebbero toccare comandi distruttivi accidentalmente. Un comando viene considerato distruttivo se l'effetto è diffuso e non può essere facilmente annullato o se l'effetto non è immediatamente evidente.
-   **Confermare i comandi per azioni rischiose o comandi con conseguenze impreviste.** A questo scopo, usare una finestra di dialogo di conferma.
-   **Provare a confermare eventuali altre azioni che gli utenti tendono a eseguire accidentalmente quando usano il tocco e che passano inosservate o sono difficili da annullare.** In genere, si tratta di conferme di routine e sono sconsigliate in base al presupposto che gli utenti spesso non rilasciano tali comandi per errore con un mouse o una tastiera. Per evitare conferme non necessarie, presentare queste conferme solo se il comando è stato avviato tramite tocco.

    Le conferme di routine sono accettabili per le interazioni che gli utenti spesso usano accidentalmente tramite tocco.

    Sviluppatori: è possibile distinguere tra eventi del mouse ed eventi di tocco usando l'API [**INPUT \_ MESSAGE \_ SOURCE.**](/windows/win32/api/winuser/ns-winuser-input_message_source)

