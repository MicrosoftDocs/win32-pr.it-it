---
title: Penna
description: Tutte le applicazioni di Microsoft Windows devono essere abilitate per la scrittura. Questa operazione è più semplice di quanto pensi.
ms.assetid: 45635d5a-c9ff-47d0-89ef-a9c48ac67594
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 35994f345306bd3a270f8d8cf9760e7d07183941
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103885919"
---
# <a name="pen"></a>Penna

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Tutte le applicazioni di Microsoft Windows devono essere abilitate per la scrittura. Questa operazione è più semplice di quanto pensi.

Input penna indica il modo in cui Windows consente di interagire direttamente con un computer tramite una penna. È possibile utilizzare una penna per puntare e anche per i movimenti, l'immissione di testo semplice e l'acquisizione di riflessioni in formato libero nell'input penna digitale.

La penna utilizzata per l'input ha un suggerimento smussato, che supporta il puntatore preciso, la scrittura o il disegno nell'input penna. La penna può anche avere un pulsante di penna facoltativo (usato per eseguire i clic con il pulsante destro del mouse) e la gomma (usata per cancellare l'input penna). La maggior parte delle penne supporta il passaggio del mouse

![Figura di una penna tipica ](images/inter-pen-image1.png)

Una penna tipica.

Quando la penna viene utilizzata per la grafia, i tratti dell'utente possono essere convertiti in testo utilizzando il riconoscimento della grafia. I tratti possono essere conservati esattamente come sono stati scritti, con il riconoscimento eseguito in background per supportare la ricerca e la copia come testo. Tali tratti non convertiti sono detti input penna digitale.

![screenshot della grafia nella pagina OneNote ](images/inter-pen-image2.png)

Esempio di input penna.

La maggior parte dei programmi Windows è già intuitiva in quanto è possibile usare una penna anziché un mouse, la penna funziona senza problemi per le attività e le interazioni più importanti e il programma risponde ai movimenti. Un programma diventa semplice da usare per la scrittura quando supporta l'input di testo scritto a mano. Un programma diventa abilitato per l'input penna quando è in grado di gestire l'input penna direttamente, anziché richiedere che i tratti della penna vengano convertiti in testo o spostamenti del mouse equivalenti. In questo modo gli utenti possono scrivere, creare e aggiungere commenti in un input penna digitale di alta qualità. La raccolta di input penna è diversa dalla raccolta di eventi del mouse, perché l'input penna richiede una risoluzione più elevata e una frequenza di campionamento superiore e può anche aggiungere nuance con pressione e inclinazione. Per informazioni sulla creazione di programmi intuitivi e abilitati per l'input penna, vedere integrazione di input [penna](/previous-versions/windows/desktop/ms700674(v=vs.85)) e [input di testo tramite Pen](/previous-versions/windows/desktop/ms695501(v=vs.85)).

Quando si posiziona una penna, è meno necessario un cursore perché il suggerimento rappresenta se stesso. Tuttavia, per l'assistenza mirata, Windows fornisce un piccolo cursore penna che indica la posizione corrente della penna. A differenza del puntatore del mouse che sostituisce, il cursore della penna non è necessario a meno che la penna non si trovi vicino alla visualizzazione, quindi scompare dopo alcuni secondi di inattività per consentire una visualizzazione senza ostacoli delle informazioni.

La maggior parte dei programmi compatibili con la penna supporta i movimenti. Un gesto è uno spostamento rapido della penna su una schermata che il computer interpreta come un comando, anziché come movimento del mouse, scrittura o disegno. Uno dei movimenti più rapidi e semplici da eseguire è un gesto rapido. Un gesto rapido è un semplice movimento che comporta la navigazione o un comando di modifica. I gesti rapidi per la navigazione includono trascinamento, trascinamento, spostamento indietro e spostamento avanti, mentre la modifica di gesti rapidi include copia, incolla, Annulla ed Elimina.

Tutti i puntatori eccetto il puntatore occupato hanno una posizione sensibile a un solo pixel che definisce la posizione dello schermo esatta del puntatore. L'area sensibile determina l'oggetto interessato dall'interazione. Gli oggetti definiscono una zona sensibile, ovvero l'area in cui l'area sensibile è considerata sull'oggetto. In genere, la zona sensibile coincide con i bordi di un oggetto, ma potrebbe essere più grande per semplificare l'interazione.

**Poiché una penna può puntare più precisamente a un dito, se l'interfaccia utente funziona bene per il tocco, funzionerà anche per una penna.** Di conseguenza, questo articolo è incentrato principalmente sull'aggiunta del supporto Pen ai programmi che sono già stati progettati per il tocco.

**Nota:** Le linee guida relative a [mouse](inter-mouse.md), [accessibilità](inter-accessibility.md)e [tocco](inter-touch.md) sono presentate in articoli distinti.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

L'uso di una penna per l'input ha le seguenti caratteristiche:

-   **Naturale e intuitivo.** Tutti sanno come puntare e toccare con una penna. Le interazioni tra oggetti sono progettate per corrispondere al modo in cui gli utenti interagiscono con gli oggetti nel mondo reale in modo coerente.
-   **Espressivo.** I tratti di una penna sono facili da controllare, rendendo più semplice la scrittura, il disegno, lo sketch, il disegno e l'annotazione di un mouse.
-   **Altre informazioni personali.** Proprio come una nota scritta a mano o una firma è più personale di una digitata, l'uso di una nota o firma scritta digitalmente è anche più personale.
-   **Meno intrusivo.** L'uso di una penna è invisibile e, di conseguenza, è molto meno distrazione rispetto alla digitazione o alla selezione, soprattutto in situazioni sociali quali riunioni.
-   **Portabile.** Un computer con una funzionalità di penna può essere più compatto perché la maggior parte delle attività può essere completata senza tastiera, mouse o touchpad. Può essere più flessibile perché non richiede una superficie di lavoro. Consente nuove posizioni e scenari per l'utilizzo di un computer.
-   **Diretta e accattivante.** L'uso di una penna ti permette di interagire direttamente con gli oggetti sullo schermo, mentre l'uso di un mouse o di un touchpad richiede sempre la coordinazione dei movimenti della mano con movimenti del puntatore sullo schermo distinti che possono essere indiretti dal confronto.

**Tutti i programmi Windows dovrebbero avere una corretta esperienza di penna.** Gli utenti devono essere in grado di eseguire in modo efficiente le attività più importanti del programma usando una penna. Alcune attività, ad esempio la digitazione o la manipolazione dettagliata dei pixel, non sono appropriate per una penna, ma dovrebbero essere almeno possibili.

Fortunatamente, se il programma è già ben progettato ed è semplice da usare, fornire un buon supporto per la penna è facile. A questo scopo, un programma ben progettato:

-   **Dispone del supporto del mouse valido.** I controlli interattivi hanno affordances evidenti e visibili e hanno gli Stati del passaggio del mouse per il feedback del puntatore. Gli oggetti hanno comportamenti standard per le interazioni con il mouse standard (solo e doppio clic con il pulsante destro del mouse, fare clic con il pulsante destro del mouse, trascinare e passare il mouse). La [forma del puntatore](inter-mouse.md) cambia in modo appropriato per indicare il tipo di manipolazione diretta.
-   **Dispone del supporto della tastiera valido.** Il programma rende gli utenti efficienti fornendo le assegnazioni dei tasti di scelta rapida standard, in particolare per i comandi di navigazione e modifica che possono essere generati anche tramite movimenti.
-   **Dispone di controlli sufficientemente grandi per il tocco.** I controlli hanno una dimensione minima di 23x23 pixel (unità di dialogo 13x13 \[ dlu \] ) e i controlli usati più di frequente sono almeno 40x40 pixel (23x22 DLU). Per evitare un comportamento non rispondente, non dovrebbero esserci piccoli gap tra le destinazioni in cui gli elementi dell'interfaccia utente devono essere spaziati, in modo che le destinazioni adiacenti tocchino o dispongano almeno di 5 pixel (3 DLU) di spazio tra di esse.
-   **È accessibile.** USA Microsoft Active Accessibility (MSAA) per fornire l'accesso a livello di codice all'interfaccia utente per le tecnologie per l'accesso facilitato. Il programma risponde in modo appropriato alle modifiche della metrica del tema e del sistema.
-   **Funziona bene e sembra valido in 120 dpi (punti per pollice),** ovvero la risoluzione predefinita consigliata per i computer abilitati per la penna.
-   **USA i controlli comuni.** La maggior parte dei controlli comuni è progettata per supportare una buona esperienza di penna. Se necessario, il programma usa controlli personalizzati ben implementati progettati per supportare la semplice selezione di destinazioni e la manipolazione interattiva.
-   **Usa controlli vincolati.** Quando è progettato per la destinazione semplice, i controlli vincolati come gli elenchi e i dispositivi di scorrimento possono essere migliori di quelli non vincolati, come le caselle di testo, perché riducono la necessità di input di testo.
-   **Fornisce i valori predefiniti appropriati.** Il programma seleziona il più sicuro (per evitare la perdita di dati o l'accesso al sistema) e l'opzione più sicura per impostazione predefinita. Se la sicurezza e la sicurezza non sono fattori, il programma seleziona l'opzione più probabile o pratica, eliminando così l'interazione non necessaria.
-   **Fornisce il completamento automatico del testo.** Fornisce un elenco di valori di input più probabili o di recente per semplificare notevolmente l'input di testo.

Sfortunatamente, il contrario è vero anche se il programma non è ben progettato, i suoi difetti saranno particolarmente evidenti per gli utenti che usano una penna.

### <a name="model-for-pen-interaction"></a>Modello per l'interazione con la penna

Se non si ha familiarità con l'uso di una penna, l'introduzione migliore consiste nell'acquisire familiarità con. Ottenere un computer abilitato per la penna, posizionare il mouse e la tastiera ed eseguire le attività normalmente eseguite utilizzando solo una penna. Assicurarsi di provare entrambi i programmi abilitati per l'input penna, ad esempio Windows Journal, e i programmi che non sono abilitati per l'input penna. Se si dispone di un Tablet PC, provare a tenerlo in posizioni diverse, ad esempio in un secondo momento, in una tabella o nelle braccia mentre si è in piedi. Provare a usarlo con orientamento verticale e orizzontale e tenendo la penna per la scrittura e solo per puntare, a sinistra e a destra.

Quando si prova a usare una penna, si scoprirà che:

-   **I controlli di piccole dimensioni sono difficili da usare.** Le dimensioni dei controlli influiscono significativamente sulla possibilità di interagire in modo efficace. I controlli 10x10 pixel funzionano ragionevolmente per una penna, ma i controlli più grandi sono ancora più comodi da usare. Ad esempio, i [controlli di selezione](ctrl-spin-controls.md) (15x11 pixel) sono troppo piccoli per essere usati facilmente con una penna.
-   **La manualità è un fattore.** A volte è possibile che si desideri visualizzare o interagire tra loro. Ad esempio, per gli utenti a destra i menu di scelta rapida sono difficili da usare se appaiono a destra del punto di clic, quindi è meglio se vengono visualizzati a sinistra. Windows consente agli utenti di indicare la loro manualità nell'elemento del pannello di controllo Impostazioni Tablet PC.
-   **La località delle attività è utile.** Sebbene sia possibile spostare il puntatore su uno schermo da 14 pollici con un movimento del mouse da 3 pollici, per usare una penna è necessario spostare la mano a un massimo di 14 centimetri. Lo scorrere ripetutamente tra destinazioni che si distinguono in modo più semplice può essere noioso, quindi è preferibile tenere le interazioni tra le attività all'interno dell'intervallo quando possibile. I menu di scelta rapida sono pratici perché non richiedono spostamento manuale.
-   **La selezione e l'input di testo sono difficili.** Un input di testo lungo è particolarmente difficile con una penna, quindi il completamento automatico e i valori di testo predefiniti accettabili possono semplificare le attività. La selezione del testo può anche essere abbastanza complessa, quindi le attività sono più semplici quando non richiedono un posizionamento preciso del cursore.
-   **I piccoli obiettivi vicini al bordo dello schermo possono essere molto difficili da toccare.** Alcune cornici di visualizzazione sporgono e alcune tecnologie touchscreen sono meno sensibili ai bordi, rendendo i controlli più difficili da usare. Ad esempio, i pulsanti Riduci a icona, Ingrandisci/Ripristina e Chiudi sulla barra del titolo possono essere più difficili da usare quando una finestra è ingrandita.

### <a name="control-location"></a>Posizione del controllo

La località delle attività riduce i noiosi spostamenti ripetuti tra le schermate. Per ridurre al minimo i movimenti di mano, individuare i controlli vicini alla posizione in cui verranno usati con maggiore probabilità.

**Non corretto:**

![screenshot della tavolozza dei colori separati dagli strumenti ](images/inter-pen-image3.png)

In questo esempio di Windows XP, la tavolozza dei colori è troppo lontana da dove è probabile che venga utilizzata.

Tenere presente che la posizione corrente dell'utente è la più vicina a una destinazione, rendendola semplice da acquisire. In questo modo, i menu di scelta rapida sfruttano appieno la [legge di Fitts](inter-mouse.md), così come le mini-barre degli strumenti utilizzate da Microsoft Office.

![screenshot dei puntatori vicino ai menu ](images/inter-pen-image4.png)

Il percorso corrente del puntatore è sempre il più semplice da acquisire.

Gli obiettivi più piccoli vicino al bordo dello schermo possono essere difficili da usare, quindi evitare di posizionare piccoli controlli vicino ai bordi della finestra. Per assicurarsi che i controlli siano di facile destinazione quando una finestra viene ingrandita, impostarli almeno 23x23 pixel (13x13 DLU) o posizionarli fuori dal bordo della finestra.

### <a name="pen-interactions"></a>Interazioni con le penne

**Movimenti di sistema**

I movimenti di sistema sono definiti e gestiti da Windows. Di conseguenza, tutti i programmi Windows possono accedervi. Questi movimenti hanno messaggi equivalenti del mouse, della tastiera e del comando dell'applicazione:



| Movimento di sistema                                                           | Messaggio equivalente sintetizzato                                              |
|------------------------------------------------------------|-----------------------------------------------|
| Hover (se supportato)<br/>                          | Passaggio del mouse<br/>                        |
| Toccare (in basso e in alto)<br/>                               | Clic con il pulsante sinistro del mouse<br/>                   |
| Doppio tocco (in basso e su due volte)<br/>                  | Doppio clic con il pulsante sinistro del mouse<br/>            |
| Premere e tenere premuto (giù, Sospendi, su)<br/>                | Clic con il pulsante destro del mouse<br/>                  |
| Trascina (giù, sposta, su)<br/>                           | Trascinare il mouse verso sinistra<br/>                    |
| Premere, tenere premuto e trascinare (giù, Sospendi, sposta, su)<br/>   | Trascinare con il pulsante destro del mouse<br/>                   |
| Selezionare (giù, sposta su oggetti selezionabili, su)<br/> | Selezione del mouse<br/>                       |



 

**Sviluppatori:** Per ulteriori informazioni, vedere [enumerazione SystemGesture](/previous-versions/ms552724(v=vs.100)).

**I gesti rapidi**

I gesti rapidi sono movimenti semplici approssimativamente equivalenti ai tasti di scelta rapida. I gesti rapidi per la navigazione includono trascinamento, trascinamento, spostamento indietro e spostamento avanti. La modifica di gesti rapidi include copia, incolla, Annulla ed Elimina. Per usare i gesti rapidi, il programma deve solo rispondere ai comandi correlati alle sequenze di tasti.

![Diagramma che mostra i movimenti rapidi e le relative assegnazioni predefinite in Windows 7.](images/inter-pen-image5.png)

Gli otto movimenti rapidi e le relative assegnazioni predefinite in Windows 7. I gesti rapidi per la navigazione sono stati modificati in modo da corrispondere alla panoramica (dove si sposta l'oggetto con il movimento) invece di scorrere (dove l'oggetto si sposta nella direzione opposta del movimento).

![Figura di movimenti di movimento rapido, ad esempio movimento ](images/inter-pen-image6.png)

Gli otto movimenti rapidi e le relative assegnazioni predefinite in Windows Vista.

I gesti rapidi per la navigazione hanno un mapping naturale, quindi sono facili da imparare e ricordare. I gesti rapidi per la modifica sono diagonali che richiedono maggiore precisione e i relativi mapping non sono come naturali (scorrere rapidamente verso il cestino da eliminare, scorrere rapidamente nella direzione della freccia indietro per annullare), quindi questi non sono abilitati per impostazione predefinita. Tutte le azioni Flick possono essere personalizzate usando l'elemento del pannello di controllo dei dispositivi di input e penna.



| Flick                                     | Messaggio equivalente sintetizzato                                                            |
|--------------------------------------|-------------------------------------------------------------|
| Scorri a sinistra<br/>                | Comando di invio (comando indietro per Windows Vista)<br/> |
| Scorri a destra<br/>               | Back Command (comando diretto per Windows Vista)<br/> |
| Scorri verso l'alto<br/>                  | Scorrimento della tastiera verso il basso<br/>                             |
| Scorri verso il basso<br/>                | Scorrimento tastiera su<br/>                               |
| Scorri verso l'alto-sinistra diagonale<br/>    | Eliminazione da tastiera<br/>                                  |
| Scorri in basso a sinistra diagonale<br/>  | Annulla tastiera<br/>                                    |
| Scorri in alto a destra diagonale<br/>   | Copia della tastiera<br/>                                    |
| Scorri in basso a destra diagonale<br/> | Incolla da tastiera<br/>                                   |



 

**Movimenti dell'applicazione**

Le applicazioni possono definire e gestire anche altri movimenti. Il riconoscitore di movimento Microsoft è in grado di riconoscere più di [40 movimenti](../tablet/application-gestures-and-semantic-behavior.md). Per usare i movimenti dell'applicazione, il programma deve definire i movimenti che riconosce e quindi gestire gli eventi risultanti.

**Velocità di risposta e coerenza**

**La velocità di risposta è essenziale per la creazione di esperienze di penna che si ritengono dirette e accattivanti.** Per sentirsi direttamente, i movimenti devono essere applicati immediatamente e i punti di contatto di un oggetto devono rimanere sotto la penna senza problemi durante il movimento. Qualsiasi ritardo, risposta frammentata, perdita di contatto o risultati non accurati Elimina la percezione della manipolazione diretta e anche della qualità.

**La coerenza è essenziale per la creazione di esperienze di penna che hanno un aspetto naturale e intuitivo.** Quando gli utenti imparano un gesto standard, si aspettano che questo movimento abbia lo stesso effetto in tutti i programmi applicabili. Per evitare confusione e frustrazione, non assegnare mai significati non standard a movimenti standard. Usare invece movimenti personalizzati per le interazioni univoche del programma.

**Modifica di input penna e testo**

La modifica di input penna e testo è tra le interazioni più complesse quando si usa una penna. L'uso di controlli vincolati, i valori predefiniti appropriati e il completamento automatico eliminano o riducono la necessità di immettere testo. Tuttavia, se il programma prevede la modifica di testo o input penna, **è possibile aumentare la produttività degli utenti eseguendo automaticamente lo zoom dell'interfaccia utente di input fino al 150% per impostazione predefinita quando viene usata una penna.**

Ad esempio, un programma di posta elettronica potrebbe visualizzare l'interfaccia utente a dimensioni normali, ma ingrandire l'interfaccia utente di input fino al 150% per comporre i messaggi.

![screenshot del messaggio di Outlook in un tipo di carattere grande ](images/inter-pen-image7.png)

In questo esempio, l'interfaccia utente di input viene ingrandita al 150%.

**Se si eseguono solo quattro operazioni...**

1.  1. Fai in modo che i tuoi programmi Windows abbiano un'esperienza di penna ottimale. Gli utenti devono essere in grado di eseguire in modo efficiente le attività più importanti del programma usando una penna, almeno le attività che non comportano una grande quantità di tipizzazione o manipolazione dettagliata dei pixel.
2.  2. Si consiglia di aggiungere il supporto per la scrittura, il disegno e l'aggiunta di commenti direttamente tramite input penna negli scenari più rilevanti.
3.  3. Per creare un'esperienza diretta e accattivante, fare in modo che i movimenti abbiano effetto immediato, che i punti di contatto sotto la penna dell'utente siano uniformi nel corso del movimento e che l'effetto del mapping dei movimenti venga effettuato direttamente sul movimento dell'utente.
4.  4. Per creare un'esperienza naturale e intuitiva, supportare i movimenti standard appropriati e assegnare loro significati standard. Usare i movimenti personalizzati per le interazioni univoche del programma.

## <a name="guidelines"></a>Indicazioni

### <a name="control-usage"></a>Controllare l'utilizzo

-   **Preferisci usare i controlli comuni.** La maggior parte dei controlli comuni è progettata per supportare una buona esperienza di penna.
-   **Preferisce i controlli vincolati.** Usare controlli vincolati come elenchi e dispositivi di scorrimento laddove possibile, anziché controlli non vincolati come caselle di testo, per ridurre la necessità di input di testo.
-   **Fornire i valori predefiniti appropriati.** Selezionare il più sicuro (per evitare la perdita di dati o l'accesso al sistema) e l'opzione più sicura per impostazione predefinita. Se la sicurezza e la sicurezza non sono fattori, selezionare l'opzione più probabile o comoda, eliminando così l'interazione non necessaria.
-   **Fornire il completamento automatico del testo.** Fornire un elenco di valori di input più probabili o di recente per semplificare notevolmente l'input di testo.
-   **Per le attività importanti che usano la selezione multipla, se normalmente viene usato un elenco di selezione multipla standard, fornire un'opzione per l'uso di un elenco di caselle di controllo.**
-   **Rispettare le metriche di sistema.** Usare le metriche di sistema per tutte le dimensioni non hardwire dimensioni. Se necessario, gli utenti possono modificare la metrica del sistema o il valore dpi per adattarlo alle proprie esigenze. Tuttavia, considerarlo come ultima risorsa perché gli utenti in genere non devono modificare le impostazioni di sistema per rendere utilizzabile l'interfaccia utente.

![screenshot dei menu con dimensioni normali e grandi ](images/inter-pen-image8.png)

In questo esempio la metrica di sistema per l'altezza del menu è stata modificata.

### <a name="control-sizing-layout-and-spacing"></a>Ridimensionamento, layout e spaziatura del controllo

-   **Per i controlli comuni, usare le dimensioni del controllo consigliate.** Queste dimensioni sono sufficienti per un'esperienza di penna ottimale, fatta eccezione per i controlli di selezione, che non sono utilizzabili con una penna ma sono ridondanti.
-   **Scegliere un layout in cui posizionare i controlli vicino alla posizione in cui verranno usati con maggiore probabilità.** Mantieni le interazioni tra le attività all'interno di una piccola area, quando possibile. Evitare movimenti di mano a lungo distanza, in particolare per le attività comuni e per i trascinamenti.
-   **Utilizzare la spaziatura consigliata.** La spaziatura consigliata è compatibile con le penne.
-   **I controlli interattivi devono essere toccati o preferibilmente avere almeno 5 pixel (3 DLU) di spazio tra di essi.** In questo modo si evita confusione quando gli utenti toccano al di fuori della destinazione prevista.
-   **Prendere in considerazione l'aggiunta di una spaziatura verticale consigliata all'interno di gruppi di controlli,** ad esempio i collegamenti ai comandi, le caselle di controllo e i pulsanti di opzione, oltre che tra i gruppi. In questo modo risulta più semplice distinguere.

### <a name="interaction"></a>Interazione

-   **Per i programmi progettati per accettare la grafia, abilitare l'impostazione predefinita di Inking.** Il valore predefinito di Inking consente agli utenti di immettere input penna semplicemente iniziando a scrivere, senza dover toccare, fornire un comando o eseguire operazioni particolari. Questa operazione consente di ottenere l'esperienza più naturale con una penna. Per i programmi non progettati per accettare la grafia, gestire input penna nelle caselle di testo come selezione.
-   **Consente agli utenti di ingrandire l'interfaccia utente del contenuto** se il programma include attività che richiedono la modifica del testo. Si consiglia di applicare lo zoom automatico al 150% quando viene usata una penna.
-   **Poiché i movimenti vengono memorizzati, assegnare loro significati coerenti tra i programmi.** Non assegnare significati diversi ai movimenti con semantica fissa. Usare invece un movimento appropriato specifico del programma.

### <a name="handedness"></a>Mano

-   **Se una finestra è contestuale, visualizzarla sempre accanto all'oggetto da cui è stata avviata.** Inserirlo in modo che l'oggetto di origine non sia coperto dalla finestra.
    -   Se visualizzata utilizzando il mouse, quando possibile posizionare la finestra contestuale offset verso il basso e verso destra.

        ![Figura della finestra contestuale situata a destra dell'oggetto ](images/inter-pen-image9.png)

        Mostra le finestre contestuali accanto all'oggetto da cui è stato avviato.

    -   Se viene visualizzato utilizzando una penna, quando possibile posizionare la finestra contestuale in modo che non venga coperta da parte dell'utente. Per gli utenti a destra, visualizzare a sinistra; in caso contrario, viene visualizzato a destra.

        ![Figura della finestra contestuale posizionata a sinistra dell'oggetto ](images/inter-pen-image10.png)

        Quando si usa una penna, Mostra anche le finestre contestuali in modo che non siano coperte dalla mano dell'utente.

-   **Sviluppatori:** È possibile distinguere tra gli eventi del mouse e gli eventi di penna usando l'API [GetMessageExtraInfo](../tablet/system-events-and-mouse-messages.md) . È possibile determinare la [manualità](/previous-versions/ms819495(v=msdn.10)) dell'utente usando l'API [SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ GETMENUDROPALIGNMENT.

### <a name="forgiveness"></a>Perdono

-   **Consente di specificare un comando Annulla.** Idealmente, è necessario fornire l'annullamento per tutti i comandi, ma il programma potrebbe avere alcuni comandi il cui effetto non può essere annullato.
-   **Fornire commenti e suggerimenti utili per il passaggio del mouse.** Indica chiaramente quando la penna si trova su una destinazione selezionabile. Questo feedback è un ottimo modo per impedire la manipolazione accidentale.
-   **Ogni volta che è possibile, fornire commenti e suggerimenti su Pen Down, ma non eseguire azioni fino a quando non si sposta o si applica una penna.** Questa operazione consente agli utenti di correggere gli errori prima di crearli.
-   **Quando si pratica, consentire agli utenti di correggere facilmente gli errori.** Se un'azione viene applicata alla penna, consentire agli utenti di correggere gli errori scorrendo mentre la penna è ancora inattiva.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento all'input penna:

-   Fare riferimento a un dispositivo di input stilo a forma di penna. Alla prima menzione, usare Tablet Pen.
-   Fare riferimento al pulsante sul lato di una penna come pulsante della penna, non sul pulsante a forma di bottle.
-   Fare riferimento in modo generico alla tastiera, al mouse, alla trackball, alla penna o al dito come dispositivo di input.
-   Per documentare le procedure specifiche per l'uso di una penna, usare il tocco e il doppio tocco anziché fare clic su. Toccare significa per premere lo schermo e quindi sollevare prima di un periodo di attesa. Potrebbe non essere usato per generare un clic del mouse. Per le interazioni che non coinvolgono la penna, continuare a usare fare clic su.

