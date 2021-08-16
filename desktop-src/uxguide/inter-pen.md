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
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Tutte le applicazioni Windows Microsoft devono essere abilitate per la penna. Questa operazione è più semplice di quanto si pensi.

L'input penna si riferisce Windows modo in cui è possibile interagire direttamente con un computer usando una penna. Una penna può essere usata per puntare e anche per i movimenti, l'immissione di testo semplice e l'acquisizione di opinioni in formato libero nell'input penna.

La penna usata per l'input ha una punta fine e smussato che supporta puntamento, scrittura o disegno a penna precisi. La penna può anche avere un pulsante penna facoltativo (usato per eseguire clic con il pulsante destro del mouse) e una gomma (usata per cancellare l'input penna). La maggior parte delle penne supporta il passaggio del mouse.

![figura di una penna tipica ](images/inter-pen-image1.png)

Penna tipica.

Quando la penna viene usata per la grafia, i tratti dell'utente possono essere convertiti in testo usando il riconoscimento della grafia. I tratti possono essere mantenuti così come sono stati scritti, con il riconoscimento eseguito in background per supportare la ricerca e la copia come testo. Tali tratti non convertiti sono detti input penna.

![Screenshot della scrittura manuale in una pagina di una nota ](images/inter-pen-image2.png)

Esempio di input penna.

La maggior Windows è già compatibile con la penna perché è possibile usare una penna anziché un mouse, la penna funziona senza problemi per le attività e le interazioni più importanti e il programma risponde ai movimenti. Un programma diventa descrittivo per la grafia quando assiste l'input di testo scritto a mano. Un programma diventa abilitato per l'input penna quando può gestire direttamente l'input penna, invece di richiedere che i tratti della penna siano tradotti in testo o movimenti del mouse equivalenti. In questo modo gli utenti possono scrivere, disegnare e aggiungere commenti in un input penna di alta qualità e a flusso libero. La raccolta dell'input penna è diversa dalla raccolta di eventi del mouse, perché l'input penna richiede una risoluzione più elevata e una frequenza di campionamento più elevata e può anche aggiungere sfumature con pressione e inclinazione. Per informazioni sulla creazione di programmi descrittivi e abilitati per l'input penna per la grafia, vedere [Integrazione dell'input penna](/previous-versions/windows/desktop/ms700674(v=vs.85)) e [dell'input di testo tramite l'oggetto Pen.](/previous-versions/windows/desktop/ms695501(v=vs.85))

Quando si posiziona una penna, è meno necessario un cursore perché la punta rappresenta se stessa. Tuttavia, per l'assistenza di destinazione, Windows un piccolo cursore penna che indica la posizione corrente della penna. A differenza del puntatore del mouse che sostituisce, il cursore penna non è necessario, a meno che la penna non sia vicina allo schermo, quindi scompare dopo alcuni secondi di inattività per consentire una visualizzazione non strutturata delle informazioni.

La maggior parte dei programmi che supportano la penna supporta i movimenti. Un movimento è un movimento rapido della penna su uno schermo che il computer interpreta come un comando, anziché come movimento, scrittura o disegno del mouse. Uno dei movimenti più rapidi e semplici da eseguire è un gesto rapido. Un gesto rapido è un movimento semplice che comporta la navigazione o un comando di modifica. I gesti rapidi di spostamento includono trascinamento verso l'alto, trascinamento verso il basso, spostamento indietro e spostamento avanti, mentre i gesti rapidi di modifica includono copia, incolla, annullamento ed eliminazione.

Tutti i puntatori ad eccezione del puntatore occupato hanno un'area sensibile a un singolo pixel che definisce la posizione esatta dello schermo del puntatore. L'area sensibile determina quale oggetto è interessato dall'interazione. Gli oggetti definiscono una zona sensibile, ovvero l'area in cui l'area sensibile viene considerata come sopra l'oggetto. In genere, la zona ad accesso più caldo coincide con i bordi di un oggetto, ma può essere più grande per semplificare l'interazione.

**Poiché una penna può puntare più precisamente di un dito, se l'interfaccia utente funziona bene per il tocco, funzionerà bene anche per una penna.** Di conseguenza, questo articolo è incentrato principalmente sull'aggiunta del supporto penna ai programmi che sono già stati progettati per il tocco.

**Nota:** Le linee guida relative [al mouse,](inter-mouse.md) [all'accessibilità](inter-accessibility.md)e [al tocco](inter-touch.md) sono presentate in articoli separati.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

L'uso di una penna per l'input presenta le caratteristiche seguenti:

-   **Naturale e intuitivo.** Tutti sanno come puntare e toccare con una penna. Le interazioni tra oggetti sono progettate per corrispondere al modo in cui gli utenti interagiscono con gli oggetti nel mondo reale in modo coerente.
-   **Espressivo.** I tratti di una penna sono facili da controllare, semplificando la scrittura, il disegno, lo sketching, il disegno e l'annotazione rispetto all'uso del mouse.
-   **Più personale.** Proprio come una nota o una firma scritta a mano è più personale di una nota digitata, anche l'uso di una nota o di una firma scritta a mano è più personale.
-   **Meno intrusivo.** L'uso di una penna è invisibile all'utente e, di conseguenza, è molto meno distrazione rispetto alla digitazione o al clic, soprattutto in situazioni di social network come le riunioni.
-   **Portatile.** Un computer con funzionalità penna può essere più compatto perché la maggior parte delle attività può essere completata senza tastiera, mouse o touchpad. Può essere più flessibile perché non richiede una superficie di lavoro. Consente nuovi scenari e posizioni per l'uso di un computer.
-   **Diretto e coinvolgente.** L'uso di una penna consente di interagire direttamente con gli oggetti sullo schermo, mentre l'uso di un mouse o di un touchpad richiede sempre di coordinare i movimenti della mano con movimenti separati del puntatore sullo schermo che si sentano indiretti rispetto al confronto.

**Tutti Windows programmi devono avere un'esperienza di penna ottimale.** Gli utenti devono essere in grado di eseguire in modo efficiente le attività più importanti del programma usando una penna. Alcune attività, ad esempio la digitazione o la manipolazione dettagliata dei pixel, non sono appropriate per una penna, ma dovrebbero essere almeno possibili.

Fortunatamente, se il programma è già ben progettato ed è facile da usare per il tocco, è facile fornire un buon supporto per la penna. A questo scopo, un programma ben progettato:

-   **Ha un buon supporto per il mouse.** I controlli interattivi hanno affordance chiari e visibili e hanno stati di passaggio del mouse per il feedback del puntatore. Gli oggetti hanno comportamenti standard per le interazioni con il mouse standard (clic singolo e doppio clic, clic con il pulsante destro del mouse, trascinamento del mouse e passaggio del mouse). La [forma del puntatore](inter-mouse.md) cambia in base alle esigenze per indicare il tipo di manipolazione diretta.
-   **Ha un buon supporto per la tastiera.** Il programma rende gli utenti efficienti fornendo assegnazioni standard di tasti di scelta rapida, in particolare per comandi di navigazione e modifica che possono essere generati anche tramite movimenti.
-   **Dispone di controlli sufficientemente grandi per il tocco.** I controlli hanno una dimensione minima di 23x23 pixel (DLU 13x13 unità di dialogo) e i controlli usati più di frequente sono almeno \[ \] 40x40 pixel (23 x 22 DLU). Per evitare un comportamento che non risponde, non devono esserci piccoli spazi tra le destinazioni in cui gli elementi dell'interfaccia utente devono essere distacchiati, in modo che le destinazioni adiacenti tocchino o presentino almeno 5 pixel (3 DLO) di spazio tra di esse.
-   **È accessibile.** Usa Microsoft Active Accessibility (MSAA) per fornire l'accesso a livello di codice all'interfaccia utente per assistive technology. Il programma risponde in modo appropriato alle modifiche al tema e alle metriche di sistema.
-   Funziona bene e ha un aspetto positivo **in 120 dpi (punti per pollice),** che è la risoluzione dello schermo predefinita consigliata per i computer abilitati per la penna.
-   **Usa controlli comuni.** I controlli più comuni sono progettati per supportare un'esperienza di penna ottimale. Se necessario, il programma usa controlli personalizzati ben implementati progettati per supportare facilità di destinazione e manipolazione interattiva.
-   **Usa controlli vincolati.** Quando sono progettati per una destinazione semplice, i controlli vincolati come elenchi e dispositivi di scorrimento possono essere migliori rispetto ai controlli non vincolati come le caselle di testo, perché riducono la necessità di input di testo.
-   **Fornisce i valori predefiniti appropriati.** Il programma seleziona l'opzione più sicura (per evitare la perdita di dati o l'accesso al sistema) e l'opzione più sicura per impostazione predefinita. Se la sicurezza e la sicurezza non sono fattori, il programma seleziona l'opzione più probabile o comoda, eliminando così l'interazione non necessaria.
-   **Fornisce il completamento automatico del testo.** Fornisce un elenco di valori di input più probabili o recenti per semplificare molto l'input di testo.

Sfortunatamente, il contrario è vero anche se il programma non è ben progettato, le sue lacune saranno particolarmente evidenti per gli utenti che usano una penna.

### <a name="model-for-pen-interaction"></a>Modello per l'interazione con la penna

Se non si ha esperienza con l'uso di una penna, l'introduzione migliore è imparare facendo. Ottenere un computer abilitato per la penna, mettere da parte il mouse e la tastiera ed eseguire le attività normalmente eseguite usando solo una penna. Assicurarsi di provare sia programmi abilitati per l'input penna, ad esempio Windows Journal, che programmi che non sono abilitati per l'input penna. Se si dispone di un Tablet PC, provare a posizionarlo in posizioni diverse, ad esempio in grembo, in un tavolo o tra le mani mentre si è in piedi. Provare a usarlo con orientamento verticale e orizzontale e tenendo la penna per la scrittura e solo per puntare, sia a sinistra che a destra.

Quando si prova a usare una penna, si scoprirà che:

-   **I controlli di piccole dimensioni sono difficili da usare.** Le dimensioni dei controlli influiscono notevolmente sulla possibilità di interagire in modo efficace. I controlli di 10x10 pixel funzionano ragionevolmente per una penna, ma i controlli più grandi sono ancora più comodi da usare. Ad esempio, [i controlli di selezione](ctrl-spin-controls.md) (15x11 pixel) sono troppo piccoli per essere facilmente utilizzati con una penna.
-   **La mani è un fattore.** La mano a volte copre gli elementi che si potrebbe voler visualizzare o con cui interagire. Ad esempio, per i menu di scelta rapida degli utenti con la mano destra è difficile usarli se vengono visualizzati a destra del punto di clic, quindi è meglio se vengono visualizzati a sinistra. Windows consente agli utenti di indicare la propria mano nel Tablet PC Impostazioni pannello di controllo.
-   **La localizzazione delle attività è utile.** Anche se è possibile spostare il puntatore su uno schermo da 14 pollici con un movimento del mouse di 3 pollici, l'uso di una penna richiede di spostare la mano per l'intero 14 pollici. Lo spostamento ripetuto tra destinazioni distanti può essere noioso, quindi è molto meglio mantenere le interazioni tra attività all'interno dell'intervallo di una mano a riposo, quando possibile. I menu di scelta rapida sono utili perché non richiedono alcun movimento della mano.
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

1.  1. Fare in modo che Windows programmi di penna abbia una buona esperienza con la penna. Gli utenti devono essere in grado di eseguire in modo efficiente le attività più importanti del programma usando una penna (almeno quelle attività che non comportano molta digitazione o una manipolazione dettagliata dei pixel).
2.  2. Provare ad aggiungere il supporto per la scrittura, il disegno e l'aggiunta di commenti direttamente usando l'input penna negli scenari più rilevanti.
3.  3. Per creare un'esperienza diretta e coinvolgente, fare in modo che i movimenti abbia effetto immediato, mantenere i punti di contatto sotto la penna dell'utente in modo uniforme durante il movimento e fare in modo che l'effetto del movimento sia mappato direttamente al movimento dell'utente.
4.  4. Per creare un'esperienza naturale e intuitiva, supportare i movimenti standard appropriati e assegnare loro i significati standard. Usare movimenti personalizzati per le interazioni univoche per il programma.

## <a name="guidelines"></a>Indicazioni

### <a name="control-usage"></a>Controllare l'utilizzo

-   **Preferire l'uso di controlli comuni.** I controlli più comuni sono progettati per supportare un'esperienza di penna ottimale.
-   **Preferisce i controlli vincolati.** Usare controlli vincolati come elenchi e dispositivi di scorrimento quando possibile, anziché controlli non vincolati come caselle di testo, per ridurre la necessità di input di testo.
-   **Specificare i valori predefiniti appropriati.** Selezionare l'opzione più sicura (per evitare la perdita di dati o l'accesso al sistema) e l'opzione più sicura per impostazione predefinita. Se la sicurezza e la sicurezza non sono fattori, selezionare l'opzione più probabile o conveniente, eliminando così l'interazione non necessaria.
-   **Fornire il completamento automatico del testo.** Fornire un elenco dei valori di input più probabili o di recente per semplificare l'input di testo.
-   **Per le attività importanti che usano la selezione multipla, se in genere viene usato un elenco a selezione multipla standard, fornire un'opzione per usare un elenco di caselle di controllo.**
-   **Rispettare le metriche di sistema.** Usare le metriche di sistema per tutte le dimensioni e non per le dimensioni hardwire. Se necessario, gli utenti possono modificare le metriche di sistema o dpi in base alle proprie esigenze. Tuttavia, considerare questo come ultima risorsa perché gli utenti non devono in genere modificare le impostazioni di sistema per rendere utilizzabile l'interfaccia utente.

![Screenshot dei menu con ridimensionamento normale e di grandi dimensioni ](images/inter-pen-image8.png)

In questo esempio la metrica di sistema per l'altezza del menu è stata modificata.

### <a name="control-sizing-layout-and-spacing"></a>Ridimensionamento, layout e spaziatura dei controlli

-   **Per i controlli comuni, usare le dimensioni di controllo consigliate.** Queste sono sufficientemente grandi per un'esperienza di penna ottimale, ad eccezione dei controlli di selezione (che non sono utilizzabili con una penna ma sono ridondanti).
-   **Scegliere un layout che inserisca i controlli vicino al punto in cui è più probabile che verranno usati.** Mantenere le interazioni tra attività all'interno di un'area di piccole dimensioni, quando possibile. Evitare movimenti della mano a lunga distanza, in particolare per le attività comuni e per i trascinamenti.
-   **Usare la spaziatura consigliata.** La spaziatura consigliata è di tipo penna.
-   **I controlli interattivi devono toccare o preferibilmente avere almeno 5 pixel (3 DLU) di spazio tra di essi.** In questo modo si evita confusione quando gli utenti toccano all'esterno della destinazione prevista.
-   **È consigliabile aggiungere più** della spaziatura verticale consigliata all'interno di gruppi di controlli, ad esempio collegamenti a comandi, caselle di controllo e pulsanti di opzione, nonché tra i gruppi. In questo modo è più facile differenziarli.

### <a name="interaction"></a>Interazione

-   **Per i programmi progettati per accettare la grafia, abilitare l'input penna predefinito.** L'input penna predefinito consente agli utenti di immettere input penna semplicemente iniziando a scrivere, senza dover toccare, fornire un comando o eseguire operazioni speciali. In questo modo si offre l'esperienza più naturale con una penna. Per i programmi non progettati per accettare la grafia, gestire l'input penna nelle caselle di testo come selezione.
-   **Consentire agli utenti di ingrandire l'interfaccia utente del** contenuto se il programma ha attività che richiedono la modifica del testo. È consigliabile eseguire automaticamente lo zoom al 150% quando si usa una penna.
-   **Poiché i movimenti vengono memorizzati, assegnare loro significati coerenti tra i programmi.** Non assegnare significati diversi ai movimenti con semantica fissa. Usare invece un movimento specifico del programma appropriato.

### <a name="handedness"></a>Manualità

-   **Se una finestra è contestuale, visualizzarla sempre accanto all'oggetto da cui è stata avviata.** Posizionarlo in modo che l'oggetto di origine non sia coperto dalla finestra.
    -   Se viene visualizzato con il mouse, quando possibile posizionare l'offset della finestra contestuale verso il basso e verso destra.

        ![Figura della finestra contestuale posizionata a destra dell'oggetto ](images/inter-pen-image9.png)

        Mostra le finestre contestuali vicino all'oggetto da cui è stato avviato.

    -   Se viene visualizzata con una penna, quando possibile posizionare la finestra contestuale in modo da non essere coperta dalla mano dell'utente. Per gli utenti con mano destra, visualizzare a sinistra; in caso contrario, viene visualizzato a destra.

        ![Figura della finestra contestuale posizionata a sinistra dell'oggetto ](images/inter-pen-image10.png)

        Quando si usa una penna, visualizzare anche le finestre contestuali in modo che non siano coperte dalla mano dell'utente.

-   **Sviluppatori:** È possibile distinguere tra eventi del mouse ed eventi penna usando l'API [GetMessageExtraInfo.](../tablet/system-events-and-mouse-messages.md) È possibile determinare la mano [dell'utente](/previous-versions/ms819495(v=msdn.10)) usando l'API [SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ GETMENUDROPALIGNMENT.

### <a name="forgiveness"></a>Perdono

-   **Fornire un comando di annullamento.** Idealmente, è consigliabile fornire l'annullamento per tutti i comandi, ma il programma potrebbe avere alcuni comandi il cui effetto non può essere annullato.
-   **Fornire un feedback positivo al passaggio del mouse.** Indicare chiaramente quando la penna è su una destinazione selezionabile. Questo feedback è un ottimo modo per evitare la manipolazione accidentale.
-   **Ogni volta che è pratico, fornire un buon feedback sulla penna verso il basso, ma non intraprendere azioni fino a quando non si sposta o si alza la penna.** In questo modo, gli utenti possono correggere gli errori prima di commetterli.
-   **Quando pratico, consentire agli utenti di correggere facilmente gli errori.** Se un'azione ha effetto sulla penna verso l'alto, consentire agli utenti di correggere gli errori scorrendo mentre la penna è ancora in giù.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento all'input penna:

-   Fare riferimento a un dispositivo di input stilo a forma di penna come penna. Per prima cosa, usare la penna del tablet.
-   Fare riferimento al pulsante sul lato di una penna come pulsante della penna, non come pulsante a forma di barra.
-   Fare riferimento genericamente a tastiera, mouse, trackball, penna o dito come dispositivo di input.
-   Usare il tocco (e il doppio tocco) invece di fare clic quando si documentano procedure specifiche per l'uso di una penna. Toccare significa premere lo schermo e quindi alzarsi prima di un periodo di attesa. Può essere usato o meno per generare un clic del mouse. Per le interazioni che non coinvolgono la penna, continuare a usare il clic.

