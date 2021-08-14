---
title: Penna
description: Tutte le applicazioni Windows Microsoft devono essere abilitate per la penna. Questa operazione è più semplice di quanto si pensi.
ms.assetid: 45635d5a-c9ff-47d0-89ef-a9c48ac67594
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 90c953fe1c287741bec266bfe6516a6a8922692b213292d2f17cccebf561cb0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117853376"
---
# <a name="pen"></a>Penna

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Tutte le applicazioni Windows Microsoft devono essere abilitate per la penna. Questa operazione è più semplice di quanto si pensi.

L'input penna si riferisce Windows modo in cui è possibile interagire direttamente con un computer usando una penna. Una penna può essere usata per puntare e anche per i movimenti, l'immissione di testo semplice e l'acquisizione di commenti in formato libero nell'input penna digitale.

La penna usata per l'input ha una punta fine e smussato che supporta il puntamento, la scrittura o il disegno preciso con input penna. La penna può anche avere un pulsante penna facoltativo (usato per eseguire clic con il pulsante destro del mouse) e una gomma (usata per cancellare l'input penna). La maggior parte delle penna supporta il passaggio del mouse.

![figura di una penna tipica ](images/inter-pen-image1.png)

Penna tipica.

Quando la penna viene usata per la scrittura manuale, i tratti dell'utente possono essere convertiti in testo usando il riconoscimento della grafia. I tratti possono essere mantenuti così come sono stati scritti, con il riconoscimento eseguito in background per supportare la ricerca e la copia come testo. Questi tratti non convertiti sono detti input penna digitale.

![Screenshot della scrittura manuale in una pagina di onenote ](images/inter-pen-image2.png)

Esempio di input penna.

La Windows è già compatibile con la penna in quanto una penna può essere usata al posto del mouse, la penna funziona senza problemi per le attività e le interazioni più importanti e il programma risponde ai movimenti. Un programma diventa facile da scrivere quando assiste l'input di testo scritto a mano. Un programma diventa abilitato per l'input penna quando può gestire direttamente l'input penna, anziché richiedere che i tratti della penna siano convertiti in testo o movimenti del mouse equivalenti. In questo modo gli utenti possono scrivere, disegnare e aggiungere commenti in un input penna digitale di alta qualità a flusso libero. La raccolta dell'input penna è diversa dalla raccolta degli eventi del mouse, perché l'input penna richiede una risoluzione più elevata e una frequenza di campionamento più elevata e può anche aggiungere sfumature con pressione e inclinazione. Per informazioni sulla creazione di programmi con riconoscimento della grafia e abilitati per l'input penna, vedere Integrazione [dell'input penna](/previous-versions/windows/desktop/ms700674(v=vs.85)) e dell'input di testo con [la penna](/previous-versions/windows/desktop/ms695501(v=vs.85)).

Quando si posiziona una penna, è meno necessario un cursore perché la punta rappresenta se stessa. Tuttavia, per l'assistenza di destinazione, Windows un piccolo cursore penna che indica la posizione corrente della penna. A differenza del puntatore del mouse che sostituisce, il cursore penna non è necessario a meno che la penna non sia vicina allo schermo, quindi scompare dopo alcuni secondi di inattività per consentire una visualizzazione non strutturata delle informazioni.

La maggior parte dei programmi che supportano la penna supporta i movimenti. Un movimento è un rapido movimento della penna su uno schermo che il computer interpreta come un comando, anziché come movimento del mouse, scrittura o disegno. Uno dei movimenti più rapidi e semplici da eseguire è un tocco. Un tocco rapido è un semplice movimento che comporta la navigazione o un comando di modifica. I gesti rapidi di navigazione includono trascinamento verso l'alto, trascinamento verso il basso, spostamento indietro e avanzamento, mentre i gesti rapidi di modifica includono copia, incolla, annullamento ed eliminazione.

Tutti i puntatori ad eccezione del puntatore occupato hanno un'area sensibile a pixel singolo che definisce la posizione esatta dello schermo del puntatore. L'area sensibile determina l'oggetto interessato dall'interazione. Gli oggetti definiscono una zona sensibile, ovvero l'area in cui l'area sensibile viene considerata sull'oggetto . In genere, la zona calda coincide con i bordi di un oggetto, ma può essere più grande per semplificare l'interazione.

**Poiché una penna può puntare più precisamente di un dito, se l'interfaccia utente funziona correttamente per il tocco, funzionerà anche per una penna.** Di conseguenza, questo articolo è incentrato principalmente sull'aggiunta del supporto penna ai programmi già progettati per il tocco.

**Nota:** Le linee guida relative [al mouse,](inter-mouse.md) [all'accessibilità](inter-accessibility.md)e [al tocco](inter-touch.md) sono presentate in articoli separati.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

L'uso di una penna per l'input presenta le caratteristiche seguenti:

-   **Naturale e intuitivo.** Tutti sanno come puntare e toccare con una penna. Le interazioni tra oggetti sono progettate per corrispondere al modo in cui gli utenti interagiscono con gli oggetti nel mondo reale in modo coerente.
-   **Espressivo.** I tratti di una penna sono facili da controllare, semplificando la scrittura, il disegno, lo sketch, il disegno e l'annotazione che con il mouse.
-   **Più personale.** Proprio come una nota o una firma scritta a mano è più personale di una firma digitata, anche l'uso di una nota o di una firma scritta a mano digitale è più personale.
-   **Meno invadente.** L'uso di una penna è invisibile all'utente e di conseguenza è molto meno distratto rispetto alla digitazione o al clic, soprattutto in situazioni sociali come le riunioni.
-   **Portatile.** Un computer con funzionalità penna può essere più compatto perché la maggior parte delle attività può essere completata senza tastiera, mouse o touchpad. Può essere più flessibile perché non richiede un'area di lavoro. Consente nuovi scenari e posizioni per l'uso di un computer.
-   **Diretto e coinvolgente.** L'uso di una penna consente di interagire direttamente con gli oggetti sullo schermo, mentre l'uso di un mouse o di un touchpad richiede sempre di coordinare i movimenti della mano con movimenti separati del puntatore su schermo che si sentano indiretti rispetto al confronto.

**Tutti Windows programmi devono avere una buona esperienza con la penna.** Gli utenti devono essere in grado di eseguire le attività più importanti del programma in modo efficiente usando una penna. Alcune attività, ad esempio la digitazione o la manipolazione dettagliata dei pixel, non sono appropriate per una penna, ma dovrebbero essere almeno possibili.

Fortunatamente, se il programma è già ben progettato ed è touch-friendly, fornire un buon supporto penna è facile da fare. A questo scopo, un programma ben progettato:

-   **Ha un buon supporto per il mouse.** I controlli interattivi hanno affordance chiari e visibili e hanno stati di passaggio del mouse per il feedback del puntatore. Gli oggetti hanno comportamenti standard per le interazioni con il mouse standard (singolo e doppio clic a sinistra, clic con il pulsante destro del mouse, trascinamento e passaggio del mouse). La [forma del puntatore](inter-mouse.md) cambia in base alle esigenze per indicare il tipo di manipolazione diretta.
-   **Ha un buon supporto per la tastiera.** Il programma rende gli utenti efficienti fornendo assegnazioni standard dei tasti di scelta rapida, in particolare per i comandi di spostamento e modifica che possono essere generati anche tramite movimenti.
-   **Ha controlli sufficientemente grandi per il tocco.** I controlli hanno una dimensione minima di 23x23 pixel (DLU 13x13 unità di dialogo) e i controlli usati più comunemente sono almeno \[ \] 40 x 40 pixel (DLU 23x22). Per evitare un comportamento non risponde, non devono esserci piccoli spazi tra le destinazioni in cui gli elementi dell'interfaccia utente devono essere spaziati in modo che le destinazioni adiacenti tocchino o presentino almeno 5 pixel (3 DLO) di spazio tra di esse.
-   **È accessibile.** Usa Microsoft Active Accessibility (MSAA) per fornire l'accesso a livello di codice all'interfaccia utente per le tecnologie di assistive. Il programma risponde in modo appropriato alle modifiche al tema e alle metriche di sistema.
-   Funziona bene e ha un aspetto positivo **in 120 dpi (punti per pollice),** ovvero la risoluzione dello schermo predefinita consigliata per i computer abilitati per la penna.
-   **Usa controlli comuni.** I controlli più comuni sono progettati per supportare un'esperienza di penna ottimale. Se necessario, il programma usa controlli personalizzati ben implementati progettati per supportare la facile destinazione e la manipolazione interattiva.
-   **Usa controlli vincolati.** Quando sono progettati per un facile targeting, i controlli vincolati come elenchi e dispositivi di scorrimento possono essere migliori rispetto ai controlli non vincolati come le caselle di testo, perché riducono la necessità di input di testo.
-   **Fornisce i valori predefiniti appropriati.** Il programma seleziona l'opzione più sicura (per evitare la perdita di dati o l'accesso al sistema) e l'opzione più sicura per impostazione predefinita. Se la sicurezza e la sicurezza non sono fattori, il programma seleziona l'opzione più probabile o conveniente, eliminando così l'interazione non necessaria.
-   **Fornisce il completamento automatico del testo.** Fornisce un elenco dei valori di input più probabili o di recente per semplificare l'input di testo.

Sfortunatamente, il contrario è vero anche se il programma non è ben progettato, le sue lacune saranno particolarmente evidenti per gli utenti che usano una penna.

### <a name="model-for-pen-interaction"></a>Modello per l'interazione con la penna

Se non si ha esperienza con l'uso di una penna, l'introduzione migliore è imparare facendo. Ottenere un computer abilitato per la penna, mettere da parte mouse e tastiera ed eseguire le attività normalmente eseguite usando solo una penna. Assicurarsi di provare sia i programmi abilitati per l'input penna, ad esempio Windows Journal, che i programmi che non sono abilitati per l'input penna. Se si dispone di un Tablet PC, provare a posizionarlo in posizioni diverse, ad esempio in grembo, a terra su un tavolo o tra le braccia mentre si è in piedi. Provare a usarlo con orientamento verticale e orizzontale e tenendo la penna per la scrittura e solo per il puntamento, nella mano sinistra e a destra.

Quando si sperimenta l'uso di una penna, si scoprirà che:

-   **I controlli di piccole dimensioni sono difficili da usare.** Le dimensioni dei controlli influiscono notevolmente sulla possibilità di interagire in modo efficace. I controlli di 10x10 pixel funzionano ragionevolmente per una penna, ma i controlli più grandi sono ancora più comodi da usare. Ad esempio, [i controlli di selezione](ctrl-spin-controls.md) (15 x 11 pixel) sono troppo piccoli per poter essere utilizzati facilmente con una penna.
-   **La mania è un fattore.** La mano a volte copre gli elementi che è possibile visualizzare o con cui interagire. Ad esempio, per i menu di scelta rapida degli utenti con la mano destra è difficile usarli se vengono visualizzati a destra del punto di clic, quindi è meglio se vengono visualizzati a sinistra. Windows consente agli utenti di indicare la propria mano nel Tablet PC Impostazioni pannello di controllo.
-   **La localizzazione delle attività è utile.** Anche se è possibile spostare il puntatore su uno schermo da 14 pollici con un movimento del mouse da 3 pollici, l'uso di una penna richiede di spostare la mano per l'intero 14 pollici. Lo spostamento ripetuto tra destinazioni distanti può essere noioso, quindi è molto meglio mantenere le interazioni tra attività all'interno dell'intervallo di una mano a riposo, quando possibile. I menu di scelta rapida sono utili perché non richiedono alcun movimento della mano.
-   **L'input e la selezione del testo sono difficili.** L'input di testo lungo è particolarmente difficile usando una penna, quindi il completamento automatico e i valori di testo predefiniti accettabili possono davvero semplificare le attività. La selezione del testo può anche essere piuttosto difficile, quindi le attività sono più semplici quando non richiedono un posizionamento preciso del cursore.
-   **Le destinazioni di piccole dimensioni vicino al bordo dello schermo possono essere molto difficili da toccare.** Alcune cornici di visualizzazione si protendono e alcune tecnologie touchscreen sono meno sensibili ai bordi, rendendo i controlli vicino al bordo più difficili da usare. Ad esempio, i pulsanti Riduci a icona, Ingrandisci/Ripristina e Chiudi sulla barra del titolo possono essere più difficili da usare quando una finestra è ingrandita.

### <a name="control-location"></a>Posizione di controllo

La localizzazione dell'attività riduce i movimenti ripetuti ripetuti sullo schermo. Per ridurre al minimo i movimenti della mano, individuare i controlli vicini al punto in cui probabilmente verranno usati.

**Non corretto:**

![Screenshot della tavolozza dei colori separata dagli strumenti ](images/inter-pen-image3.png)

In questo esempio Windows XP, la tavolozza dei colori è troppo lontana dalla posizione in cui è probabile che sia usata.

Si consideri che la posizione corrente dell'utente è la più vicina possibile a una destinazione, rendendo semplice l'acquisizione. Di conseguenza, i menu di scelta rapida sfruttano appieno la legge di [Fitts,](inter-mouse.md)così come le mini-barre degli strumenti usate da Microsoft Office.

![Screenshot dei puntatori vicino ai menu ](images/inter-pen-image4.png)

La posizione corrente del puntatore è sempre la più semplice da acquisire.

Le destinazioni di piccole dimensioni vicino al bordo dello schermo possono essere difficili da usare come destinazione, quindi evitare di posizionare piccoli controlli vicino ai bordi della finestra. Per garantire che i controlli siano facili da usare come destinazione quando una finestra è ingrandita, impostarli su almeno 23 x 23 pixel (DLU 13x13) o posizionarli lontano dal bordo della finestra.

### <a name="pen-interactions"></a>Interazioni con la penna

**Movimenti di sistema**

I movimenti di sistema vengono definiti e gestiti da Windows. Di conseguenza, tutti i Windows possono accedervi. Questi movimenti hanno messaggi di comando equivalenti per mouse, tastiera e applicazione:



| Movimento di sistema                                                           | Messaggio equivalente sintetizzato                                              |
|------------------------------------------------------------|-----------------------------------------------|
| Passaggio del mouse (se supportato)<br/>                          | Passaggio del mouse<br/>                        |
| Toccare (verso il basso e verso l'alto)<br/>                               | Clic con il pulsante sinistro del mouse<br/>                   |
| Doppio tocco (due volte verso il basso e verso l'alto)<br/>                  | Doppio clic con il mouse<br/>            |
| Premere e tenere premuto (in basso, in pausa, verso l'alto)<br/>                | Fare clic con il pulsante destro del mouse<br/>                  |
| Trascinare (verso il basso, spostare, verso l'alto)<br/>                           | Trascinamento del mouse a sinistra<br/>                    |
| Premere, tenere premuto e trascinare (verso il basso, sospendere, spostare, verso l'alto)<br/>   | Trascinamento con il mouse<br/>                   |
| Selezionare (verso il basso, spostarsi sugli oggetti selezionabili, verso l'alto)<br/> | Selezione con il mouse<br/>                       |



 

**Sviluppatori:** Per altre informazioni, vedere [Enumerazione SystemGesture](/previous-versions/ms552724(v=vs.100)).

**Flicks**

I gesti rapidi sono movimenti semplici che sono approssimativamente equivalenti ai tasti di scelta rapida. I gesti rapidi di navigazione includono trascinamento verso l'alto, trascinamento verso il basso, spostamento indietro e avanzamento. I gesti rapidi di modifica includono copia, incolla, annullamento ed eliminazione. Per usare i gesti rapidi, il programma deve solo rispondere ai comandi relativi alle sequenze di tasti.

![Diagramma che mostra i movimenti di scorrimento e le relative assegnazioni predefinite in Windows 7.](images/inter-pen-image5.png)

Gli otto movimenti di scorrimento e le relative assegnazioni predefinite Windows 7. I movimenti rapidi di navigazione sono stati modificati in modo da corrispondere alla panoramica (in cui l'oggetto si sposta con il movimento) invece di scorrere (dove l'oggetto si sposta nella direzione opposta del movimento).

![figura dei movimenti di scorrimento, ad esempio il movimento di spostamento ](images/inter-pen-image6.png)

Gli otto movimenti di scorrimento e le relative assegnazioni predefinite in Windows Vista.

I gesti rapidi di navigazione hanno un mapping naturale, quindi sono facili da imparare e ricordare. I gesti rapidi di modifica sono diagonali che richiedono maggiore precisione e i relativi mapping non sono così naturali (scorrere verso il Cestino per eliminare, scorrere verso la freccia Indietro per annullare), quindi non sono abilitati per impostazione predefinita. Tutte le azioni di scorrimento possono essere personalizzate usando l'elemento del pannello di controllo Dispositivi di input e penna.



| Flick                                     | Messaggio equivalente sintetizzato                                                            |
|--------------------------------------|-------------------------------------------------------------|
| Scorrere verso sinistra<br/>                | Comando Avanti (comando Indietro per Windows Vista)<br/> |
| Scorrere verso destra<br/>               | Comando Indietro (comando Inoltra per Windows Vista)<br/> |
| Scorrere rapidamente verso l'alto<br/>                  | Scorrimento da tastiera verso il basso<br/>                             |
| Scorrere rapidamente verso il basso<br/>                | Scorrimento da tastiera verso l'alto<br/>                               |
| Diagonale verso l'alto a sinistra<br/>    | Eliminazione da tastiera<br/>                                  |
| Diagonale verso il basso a sinistra<br/>  | Annullamento da tastiera<br/>                                    |
| Diagonale verso l'alto a destra<br/>   | Copia da tastiera<br/>                                    |
| Diagonale verso il basso a destra<br/> | Incolla da tastiera<br/>                                   |



 

**Movimenti dell'applicazione**

Le applicazioni possono definire e gestire anche altri movimenti. Riconoscimento movimenti Microsoft è in grado di riconoscere [più di 40 movimenti.](../tablet/application-gestures-and-semantic-behavior.md) Per usare i movimenti dell'applicazione, il programma deve definire i movimenti che riconosce e quindi gestire gli eventi risultanti.

**Velocità di risposta e coerenza**

**La velocità di risposta è essenziale per creare esperienze di penna che si senta diretta e coinvolgente.** Per essere diretti, i movimenti devono avere effetto immediato e i punti di contatto di un oggetto devono rimanere sotto la penna senza problemi durante il movimento. Qualsiasi ritardo, risposta sgraziata, perdita di contatto o risultati imprecisi elimina la percezione della manipolazione diretta e anche della qualità.

**La coerenza è essenziale per creare esperienze di penna che si senta naturale e intuitiva.** Dopo aver appreso un movimento standard, gli utenti si aspettano che il movimento abbia lo stesso effetto in tutti i programmi applicabili. Per evitare confusione e frustrazione, non assegnare mai significati non standard ai movimenti standard. Usare invece movimenti personalizzati per le interazioni univoche per il programma.

**Modifica di input penna e testo**

La modifica dell'input penna e del testo è tra le interazioni più difficili quando si usa una penna. L'uso di controlli vincolati, valori predefiniti appropriati e completamento automatico elimina o riduce la necessità di immettere testo. Se tuttavia il programma prevede la modifica di testo o input penna, è possibile aumentare la produttività degli utenti zoomando automaticamente l'interfaccia utente di input fino al **150%** per impostazione predefinita quando si usa una penna.

Ad esempio, un programma di posta elettronica potrebbe visualizzare l'interfaccia utente alle dimensioni normali, ma ingrandire l'interfaccia utente di input al 150% per comporre i messaggi.

![Screenshot del messaggio di Outlook con carattere di grandi dimensioni ](images/inter-pen-image7.png)

In questo esempio, l'interfaccia utente di input viene ingrandita al 150%.

**Se si eservino solo quattro operazioni...**

1.  1. Fare in modo che Windows programmi di penna abbia una buona esperienza con la penna. Gli utenti dovrebbero essere in grado di eseguire in modo efficiente le attività più importanti del programma usando una penna (almeno quelle attività che non comportano molta digitazione o una manipolazione dettagliata dei pixel).
2.  2. Provare ad aggiungere il supporto per la scrittura, il disegno e l'aggiunta di commenti direttamente usando l'input penna negli scenari più rilevanti.
3.  3. Per creare un'esperienza diretta e coinvolgente, fare in modo che i movimenti abbia effetto immediato, mantenere i punti di contatto sotto la penna dell'utente senza problemi durante il movimento e ottenere l'effetto della mappa dei movimenti direttamente sul movimento dell'utente.
4.  4. Per creare un'esperienza naturale e intuitiva, supportare i movimenti standard appropriati e assegnare loro i significati standard. Usare movimenti personalizzati per le interazioni univoche per il programma.

## <a name="guidelines"></a>Indicazioni

### <a name="control-usage"></a>Controllare l'utilizzo

-   **Preferisce l'uso di controlli comuni.** I controlli più comuni sono progettati per supportare un'esperienza di penna ottimale.
-   **Preferisce i controlli vincolati.** Usare controlli vincolati come elenchi e dispositivi di scorrimento quando possibile, invece di controlli non vincolati come le caselle di testo, per ridurre la necessità di input di testo.
-   **Specificare i valori predefiniti appropriati.** Selezionare l'opzione più sicura (per impedire la perdita di dati o l'accesso al sistema) e l'opzione più sicura per impostazione predefinita. Se la sicurezza e la sicurezza non sono fattori, selezionare l'opzione più probabile o comoda, eliminando così l'interazione non necessaria.
-   **Specificare il completamento automatico del testo.** Fornire un elenco dei valori di input più probabili o di recente per semplificare molto l'input di testo.
-   **Per le attività importanti che usano la selezione multipla, se in genere viene usato un elenco a selezione multipla standard, fornire un'opzione per utilizzare un elenco di caselle di controllo.**
-   **Rispettare le metriche di sistema.** Usare le metriche di sistema per tutte le dimensioni non hardwire. Se necessario, gli utenti possono modificare le metriche di sistema o dpi in base alle proprie esigenze. Tuttavia, considerare questa opzione come ultima risorsa perché gli utenti in genere non devono modificare le impostazioni di sistema per rendere utilizzabile l'interfaccia utente.

![Screenshot dei menu con ridimensionamento normale e grande ](images/inter-pen-image8.png)

In questo esempio è stata modificata la metrica di sistema per l'altezza del menu.

### <a name="control-sizing-layout-and-spacing"></a>Controllare il ridimensionamento, il layout e la spaziatura

-   **Per i controlli comuni, usare le dimensioni dei controlli consigliate.** Queste sono sufficientemente grandi per un'esperienza di penna ottimale, ad eccezione dei controlli di selezione (che non sono utilizzabili con una penna ma sono ridondanti).
-   **Scegliere un layout che posiziona i controlli vicino alla posizione in cui è più probabile che verranno usati.** Mantenere le interazioni tra attività all'interno di una piccola area, quando possibile. Evitare movimenti della mano a distanza lunga, soprattutto per le attività comuni e per i trascinamenti.
-   **Usare la spaziatura consigliata.** La spaziatura consigliata è di tipo penna.
-   **I controlli interattivi devono toccare o preferibilmente avere almeno 5 pixel (3 DLU) di spazio tra di essi.** In questo modo si evita confusione quando gli utenti toccano all'esterno della destinazione prevista.
-   **Prendere in considerazione l'aggiunta** di più della spaziatura verticale consigliata all'interno di gruppi di controlli, ad esempio collegamenti di comando, caselle di controllo e pulsanti di opzione, nonché tra i gruppi. In questo modo è più facile distinguerli.

### <a name="interaction"></a>Interazione

-   **Per i programmi progettati per accettare la grafia, abilitare l'input penna predefinito.** L'input penna predefinito consente agli utenti di immettere input penna iniziando a scrivere, senza dover toccare, eseguire un comando o eseguire operazioni speciali. In questo modo si consente l'esperienza più naturale con una penna. Per i programmi non progettati per accettare la grafia, gestire l'input penna nelle caselle di testo come selezione.
-   **Consentire agli utenti di ingrandire l'interfaccia utente del contenuto** se il programma ha attività che richiedono la modifica del testo. È consigliabile ingrandire automaticamente al 150% quando si usa una penna.
-   **Poiché i movimenti vengono memorizzati, assegnare loro significati coerenti tra i programmi.** Non assegnare significati diversi ai movimenti con semantica fissa. Usare invece un movimento specifico del programma appropriato.

### <a name="handedness"></a>Manualità

-   **Se una finestra è contestuale, visualizzarla sempre accanto all'oggetto da cui è stata avviata.** Posizionarlo fuori controllo in modo che l'oggetto di origine non sia coperto dalla finestra.
    -   Se viene visualizzato con il mouse, quando possibile posizionare l'offset della finestra contestuale verso il basso e verso destra.

        ![figura della finestra contestuale posizionata a destra dell'oggetto ](images/inter-pen-image9.png)

        Mostra le finestre contestuali accanto all'oggetto da cui è stato avviato.

    -   Se viene visualizzato con una penna, quando possibile posizionare la finestra contestuale in modo da non essere coperta dalla mano dell'utente. Per gli utenti con la mano destra, visualizzare a sinistra; in caso contrario, viene visualizzato a destra.

        ![figura della finestra contestuale posizionata a sinistra dell'oggetto ](images/inter-pen-image10.png)

        Quando si usa una penna, visualizzare anche le finestre contestuali in modo che non siano coperte dalla mano dell'utente.

-   **Sviluppatori:** È possibile distinguere tra eventi del mouse ed eventi penna usando [l'API GetMessageExtraInfo.](../tablet/system-events-and-mouse-messages.md) È possibile determinare la mano [dell'utente usando](/previous-versions/ms819495(v=msdn.10)) l'API [SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ GETMENUDROPALIGNMENT.

### <a name="forgiveness"></a>Perdono

-   **Specificare un comando di annullamento.** Idealmente, è consigliabile fornire l'annullamento per tutti i comandi, ma il programma potrebbe avere alcuni comandi il cui effetto non può essere annullato.
-   **Fornire un buon feedback al passaggio del mouse.** Indicare chiaramente quando la penna è sopra una destinazione selezionabile. Questo feedback è un ottimo modo per impedire la manipolazione accidentale.
-   **Quando possibile, fornire un buon feedback sulla pressione della penna verso il basso, ma non intraprendere azioni fino a quando uno spostamento o una penna verso l'alto.** In questo modo gli utenti possono correggere gli errori prima di commetterli.
-   **Quando possibile, consentire agli utenti di correggere facilmente gli errori.** Se un'azione ha effetto sulla penna in su, consentire agli utenti di correggere gli errori scorrendo mentre la penna è ancora in giù.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento all'input penna:

-   Fare riferimento a un dispositivo di input dello stilo a forma di penna come penna. Per prima cosa, usare la penna del tablet.
-   Fare riferimento al pulsante sul lato di una penna come pulsante della penna, non come pulsante della penna.
-   Fare riferimento genericamente a tastiera, mouse, trackball, penna o dito come dispositivo di input.
-   Usare il tocco (e il doppio tocco) invece di fare clic quando si documentano procedure specifiche per l'uso di una penna. Toccare significa premere lo schermo e quindi sollevarsi prima di un periodo di attesa. Può essere usato o meno per generare un clic del mouse. Per le interazioni che non coinvolgono la penna, continuare a usare il clic.

