---
title: Finestre di dialogo (nozioni di base sulla progettazione)
description: Una finestra di dialogo è una finestra secondaria che consente agli utenti di eseguire un comando, chiedere agli utenti una domanda o fornire agli utenti informazioni o commenti e suggerimenti sullo stato di avanzamento.
ms.assetid: 2ded9f30-d45f-4027-a85d-4e7d0e412793
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0db9d705cb697cdad9ed29dad86faf5f96665dd5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104550809"
---
# <a name="dialog-boxes-design-basics"></a>Finestre di dialogo (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Una finestra di dialogo è una finestra secondaria che consente agli utenti di eseguire un comando, chiedere agli utenti una domanda o fornire agli utenti informazioni o commenti e suggerimenti sullo stato di avanzamento.

![screenshot che identifica gli elementi della finestra di dialogo ](images/win-dialog-box-image1.png)

Una tipica finestra di dialogo.

Le finestre di dialogo sono costituite da una barra del titolo (per identificare il comando, la funzionalità o il programma da cui proviene una finestra di dialogo), un'istruzione principale facoltativa (per spiegare l'obiettivo dell'utente con la finestra di dialogo), vari controlli nell'area del contenuto (per presentare le opzioni) e i pulsanti di commit (per indicare la modalità di commit dell'utente nell'attività

Le finestre di dialogo presentano due tipi fondamentali:

-   Le **finestre di dialogo modali** richiedono il completamento e la chiusura degli utenti prima di continuare con la finestra proprietaria. Queste finestre di dialogo vengono usate in modo ottimale per attività critiche o non frequenti che richiedono il completamento prima di continuare.
-   Le **finestre di dialogo non modali** consentono agli utenti di passare dalla finestra di dialogo alla finestra proprietaria e viceversa. Queste finestre di dialogo sono ideali per le attività frequenti, ripetitive e in corso.

**Una finestra di dialogo attività è una finestra di dialogo implementata utilizzando la finestra di dialogo attività Application Programming Interface (API).** Sono costituiti dalle parti seguenti, che possono essere assemblate in un'ampia gamma di combinazioni:

-   **Barra del titolo** per identificare la funzionalità dell'applicazione o del sistema da cui proviene la finestra di dialogo.
-   Un' **istruzione principale**, con un'icona facoltativa, per identificare l'obiettivo dell'utente con la finestra di dialogo.
-   Un' **area di contenuto** per i controlli e le informazioni descrittive.
-   Un' **area di comando** per i pulsanti di commit, incluso un pulsante Annulla e altre opzioni facoltative e non visualizzare questa <item> Controlla nuovamente.
-   **Area a piè** di pagina per spiegazioni e informazioni aggiuntive facoltative, in genere destinate a utenti meno esperti.

![Screenshot di una finestra di dialogo attività tipica ](images/win-dialog-box-image2.png)

Una tipica finestra di dialogo attività.

**Le finestre di dialogo delle attività sono consigliate quando appropriato perché sono facili da creare e ottengono un aspetto coerente.** Per le finestre di dialogo delle attività è necessario Windows Vista o versione successiva, quindi non sono adatte per le versioni precedenti di Microsoft Windows.

Un riquadro attività è simile a una finestra di dialogo, ad eccezione del fatto che viene visualizzato in un riquadro della finestra anziché in una finestra separata. Di conseguenza, i riquadri attività hanno una finestra di dialogo più diretta e contestuale. Anche se tecnicamente non sono gli stessi, i **riquadri attività sono così simili alle finestre di dialogo in cui sono presentate le linee guida in questo articolo**.

![Screenshot di un riquadro attività tipico ](images/win-dialog-box-image3.png)

Un riquadro attività tipico.

Le [finestre delle proprietà](win-property-win.md) sono un tipo specializzato di finestra di dialogo utilizzata per visualizzare e modificare le proprietà di un oggetto, di una raccolta di oggetti o di un programma. Inoltre, le finestre delle proprietà supportano in genere diverse attività, mentre le finestre di dialogo supportano in genere una singola attività o un solo passaggio in un'attività. Poiché il loro utilizzo è specializzato, le **finestre delle proprietà sono descritte in un set di linee guida diverso**.

Le finestre di dialogo possono contenere [tabulazioni](ctrl-tabs.md)e, in tal caso, sono denominate finestre di dialogo a schede. Le finestre delle proprietà sono determinate dalla presentazione delle proprietà, non dall'utilizzo delle schede.

**Nota:** Le linee guida relative a [layout](vis-layout.md), [Gestione finestre](win-window-mgt.md), finestre di dialogo comuni, [finestre delle proprietà](win-property-win.md), [procedure guidate](win-wizards.md), [conferme](mess-confirm.md), [messaggi di errore](mess-error.md)e messaggi di [avviso](mess-warn.md) sono presentate in articoli distinti.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere, prendi in considerazione queste domande:

-   **Lo scopo è fornire agli utenti informazioni, chiedere agli utenti una domanda o consentire agli utenti di selezionare le opzioni per eseguire un comando o un'attività?** In caso contrario, utilizzare un'altra interfaccia utente (UI).
-   **Lo scopo è visualizzare e modificare le proprietà di un oggetto, di una raccolta di oggetti o di un programma?** In caso affermativo, usare invece una [finestra delle proprietà](win-property-win.md) o una [barra degli strumenti](cmd-toolbars.md) .
-   **Lo scopo è presentare una raccolta di comandi o strumenti?** In tal caso, utilizzare una barra degli strumenti o una [finestra della tavolozza](glossary.md).
-   **Lo scopo è verificare che l'utente voglia procedere con un'azione?** C'è un motivo chiaro per non continuare e una ragionevole probabilità che a volte gli utenti non lo siano? In tal caso, utilizzare una [conferma](mess-confirm.md).
-   **Lo scopo è fornire un messaggio di errore o di avviso?** In tal caso, utilizzare un [messaggio di errore](mess-error.md) o un messaggio di [avviso](mess-warn.md).
-   Scopo di:
    -   Apri file
    -   Salva file
    -   Apri cartelle
    -   Trova o Sostituisci testo
    -   Stampare un documento
    -   Selezionare gli attributi di una pagina stampata
    -   Selezionare un tipo di carattere
    -   Scegliere un colore
    -   Cerca un file, una cartella, un computer o una stampante
    -   Ricerca di utenti, computer o gruppi in Microsoft Active Directory
    -   Richiedere un nome utente e una password?

In caso affermativo, usare invece la [finestra di dialogo comune](win-common-dlg.md) appropriata. Molte di queste finestre di dialogo comuni sono estendibili.

-   **Lo scopo è quello di eseguire un'attività in più passaggi che richiede più di una singola finestra?** In caso affermativo, usare invece un [flusso attività](glossary.md) o una [procedura guidata](win-wizards.md) .
-   **Lo scopo è informare gli utenti di un evento di sistema o programma che non è correlato all'attività dell'utente corrente, che non richiede un'azione immediata da parte dell'utente e che gli utenti possono ignorarli liberamente?** In caso affermativo, usare invece una [notifica](mess-notif.md) .
-   **Lo scopo è mostrare lo stato del programma?** In caso affermativo, usare invece una [barra di stato](ctrl-status-bars.md) .
-   **È preferibile usare l'interfaccia utente sul posto?** Le finestre di dialogo possono suddividere il flusso dell'utente richiedendo attenzione. In alcuni casi l'interruzioni del flusso è giustificato, ad esempio quando l'utente deve eseguire un'azione che si trova al di fuori del contesto corrente. In altri casi, un approccio migliore consiste nel presentare l'interfaccia utente nel contesto, direttamente con l'interfaccia utente sul posto (ad esempio un riquadro attività) o su richiesta usando la [divulgazione progressiva](ctrl-progressive-disclosure-controls.md).
-   **Lo scopo è la visualizzazione di un problema di input utente non critico o di una condizione speciale?** In caso affermativo, usare invece un [fumetto](ctrl-balloons.md) .
-   **Per i flussi di attività, è preferibile usare un'altra pagina?** In genere si vuole che un'attività scorra da una pagina all'altra all'interno di un'unica finestra. Usare le finestre di dialogo per confermare i comandi sul posto, ottenere l'input per i comandi sul posto e per eseguire attività secondarie autonome che vengono eseguite meglio in modo indipendente e all'esterno del flusso attività principale.
-   **Per la selezione di opzioni, è probabile che gli utenti modifichino le opzioni?** In caso contrario, prendere in considerazione le alternative, ad esempio:
    -   Utilizzando le opzioni predefinite senza richiedere, ma consentendo agli utenti di apportare modifiche in un secondo momento.
    -   Specificando una versione con opzioni (ad esempio, **Print...** in un menu) e una versione senza opzioni, ad esempio **stampa** sulla barra degli strumenti. Generalmente, i comandi della barra degli strumenti devono essere immediati ed evitare la visualizzazione delle finestre di dialogo
-   **Per la selezione di opzioni, è disponibile un modo più semplice e diretto per presentare le opzioni?** In tal caso, prendere in considerazione le alternative, ad esempio:
    -   Utilizzando un [pulsante di suddivisione](ctrl-command-buttons.md) per selezionare le variazioni di un comando.
    -   Uso di un sottomenu per comandi, caselle di controllo, pulsanti di opzione ed elenchi semplici.

![Screenshot che mostra un menu e un sottomenu.](images/win-dialog-box-image4.png)

![Screenshot di un menu e di un sottomenu ](images/win-dialog-box-image5.png)

In questi esempi vengono utilizzati i sottomenu anziché le finestre di dialogo per le selezioni semplici.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Quando vengono usate correttamente, le finestre di dialogo sono un ottimo modo per offrire potenza e flessibilità al programma. Quando vengono usate in modo improprio, le finestre di dialogo sono un modo semplice per infastidire gli utenti, interrompere il flusso e far sentire il programma indiretto e noioso da usare. **Nelle finestre di dialogo modali è richiesta l'attenzione degli utenti.** Le finestre di dialogo sono spesso più facili da implementare rispetto alle interfacce utente alternative, quindi tendono a essere sovrautilizzate.

**Una finestra di dialogo è particolarmente efficace quando le relative caratteristiche di progettazione corrispondono all'utilizzo.** La progettazione di una finestra di dialogo dipende in gran parte dal suo scopo (per offrire opzioni, porre domande, fornire informazioni o commenti e suggerimenti), digitare (modale o non modale) e l'interazione dell'utente (obbligatoria, risposta facoltativa o riconoscimento), mentre il suo utilizzo è determinato in gran parte dal contesto (avviato dall'utente o dal programma), dalla probabilità dell'azione dell'utente e dalla

Per progettare finestre di dialogo efficaci, utilizzare in modo efficace gli elementi seguenti:

-   Testo della finestra di dialogo
-   Istruzioni principali
-   Non visualizzare <item> opzione di nuovo

**Se si esegue una sola operazione...**

Assicurarsi che la progettazione della finestra di dialogo (determinata in base allo scopo, al tipo e all'interazione dell'utente) corrisponda all'utilizzo (determinato dal contesto, dalla probabilità di azione dell'utente e dalla frequenza dello schermo).

## <a name="usage-patterns"></a>Modelli di utilizzo

Nelle finestre di dialogo sono disponibili diversi modelli di utilizzo:

-   Le finestre di dialogo delle domande (usando i pulsanti) chiedono agli utenti una singola domanda o per confermare un comando e usano risposte semplici in pulsanti di comando disposti orizzontalmente.
-   Le finestre di dialogo delle domande (usando i collegamenti ai comandi) chiedono agli utenti una singola domanda o di selezionare un'attività da eseguire e usano risposte dettagliate nei collegamenti ai comandi disposti verticalmente.
-   Le finestre di dialogo Choice presentano gli utenti con un set di opzioni, in genere per specificare un comando in modo più completo. Diversamente dalle finestre di dialogo delle domande, le finestre di dialogo scelte possono porre più domande.
-   Le finestre di dialogo di stato presentano agli utenti il feedback sullo stato di avanzamento durante un'operazione di lunga durata (più di cinque secondi), insieme a un comando per annullare o arrestare l'operazione.
-   Le finestre di dialogo informative visualizzano le informazioni richieste dall'utente.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Non usare finestre di dialogo scorrevoli.** Non usare finestre di dialogo che richiedono l'uso di una barra di scorrimento per essere visualizzate completamente durante il normale utilizzo. Riprogettare invece la finestra di dialogo. Prendere in considerazione l'uso della [divulgazione](ctrl-progressive-disclosure-controls.md) o delle [schede](ctrl-tabs.md)progressive.
-   **Non si dispone di una barra dei menu o di una barra di stato.** Fornire invece l'accesso ai comandi e allo stato direttamente nella finestra di dialogo o usando i menu di scelta rapida sui controlli pertinenti.

    -   **Eccezione:** Le barre dei menu sono accettabili quando viene usata una finestra di dialogo per implementare una finestra primaria, ad esempio un'utilità.

    **Non corretto:**

    ![Screenshot di una finestra di dialogo con una barra dei menu ](images/win-dialog-box-image6.png)

    In questo esempio, trova certificati è una finestra di dialogo non modale con una barra dei menu.

-   Se una finestra di dialogo richiede attenzione immediata e il programma non è attivo, **lampeggiare il pulsante della barra delle applicazioni tre volte per attirare l'attenzione e lasciarlo evidenziato.** Non eseguire altre operazioni: non ripristinare o attivare la finestra e non riprodurre effetti acustici. Al contrario, rispettare la selezione dello stato della finestra dell'utente e consentire all'utente di attivare la finestra quando è pronta.
-   Per altre linee guida ed esempi, vedere [barra delle applicazioni](winenv-taskbar.md).

### <a name="modal-dialog-boxes"></a>Finestre di dialogo modali

-   **Utilizzare per attività critiche o non frequenti che richiedono il completamento prima di continuare.**
-   Usare un [modello con commit ritardato](glossary.md) in modo che le modifiche non abbiano effetto fino al commit esplicito.
-   **Implementare utilizzando una finestra di dialogo attività quando appropriato per ottenere un aspetto coerente.** Le finestre di dialogo delle attività richiedono Windows Vista o versione successiva, quindi non sono adatte per le versioni precedenti di Windows.

### <a name="modeless-dialog-boxes"></a>Finestre di dialogo non modali

-   **Da usare per attività frequenti, ripetitive e in corso.**
-   Usare un [modello di commit immediato](glossary.md) in modo che le modifiche abbiano effetto immediato.
-   Per le finestre di dialogo non modali, utilizzare un pulsante di comando Chiudi esplicito nella finestra di dialogo per chiudere la finestra. Per entrambi, utilizzare un pulsante Chiudi sulla barra del titolo per chiudere la finestra.
-   **Provare a rendere ancorabili le finestre di dialogo non modali.** Le finestre di dialogo non modali ancorabili consentono un posizionamento più flessibile.

![Screenshot di una finestra di dialogo non modale ancorabile ](images/win-dialog-box-image7.png)

Alcune finestre di dialogo non modali utilizzate nel Microsoft Office sono ancorabili.

### <a name="multiple-dialog-boxes"></a>Più finestre di dialogo

-   **Non visualizzare più di una finestra di dialogo di scelta di proprietà alla volta dalla finestra di dialogo di scelta del proprietario.** La visualizzazione di più di uno rende il significato dei pulsanti di commit difficili da comprendere per gli utenti. È possibile visualizzare altri tipi di finestre di dialogo, ad esempio le finestre di dialogo delle domande, in base alle esigenze.
-   **Per una sequenza di finestre di dialogo correlate, è consigliabile utilizzare una finestra di dialogo a più pagine, se possibile.** Usare singole finestre di dialogo se non sono chiaramente correlate.

### <a name="multi-page-dialog-boxes"></a>Finestre di dialogo a più pagine

-   Utilizzare una finestra di dialogo a più pagine anziché singole finestre di dialogo quando si dispone della seguente sequenza di pagine correlate:
    -   Una singola pagina di input (facoltativo)
    -   Pagina di stato
    -   Una singola pagina di risultati

La pagina di input è facoltativa perché l'attività potrebbe essere stata avviata altrove. **In questo modo si ottiene un'esperienza stabile, semplice e leggera.**

![Screenshot di un indicatore di stato ](images/win-dialog-box-image8.png)

![screenshot del messaggio ' nessun problema trovato ' ](images/win-dialog-box-image9.png)

In questo esempio, la diagnostica di rete Windows è costituita dalle pagine stato e risultati.

-   **Non usare una finestra di dialogo a più pagine se la pagina di input è una finestra di dialogo standard.** In questo caso la coerenza di utilizzo di una finestra di dialogo standard è più importante.
-   **Non usare pulsanti avanti o indietro e non avere più di tre pagine.** Le finestre di dialogo a più pagine sono destinate a attività in un singolo passaggio con feedback. Non sono [procedure guidate](win-wizards.md), che vengono usate per le attività in più passaggi. Le procedure guidate presentano un comportamento indiretto intenso rispetto alle finestre di dialogo a più pagine.
-   **Nella pagina input usare i pulsanti di comando o i collegamenti ai comandi specifici per avviare l'attività.**
-   **Utilizzare un pulsante Annulla nelle pagine di input e di stato e un pulsante Chiudi nella pagina risultati.**

**Sviluppatori:** È possibile creare finestre di dialogo di attività a più pagine usando il messaggio di [ \_ \_ pagina di spostamento TDM](../controls/tdm-navigate-page.md) .

### <a name="presentation"></a>Presentazione

Per semplificare l'individuazione e l'accesso delle finestre di dialogo, associare chiaramente la finestra di dialogo alla relativa origine e utilizzare più monitor:

-   **Visualizzare inizialmente le finestre di dialogo "centrate" nella parte superiore della finestra proprietaria.** Per la visualizzazione successiva, provare a visualizzarla nell'ultima posizione, relativa alla finestra proprietaria, se questa operazione è probabilmente più pratica.

![diagramma della finestra di dialogo centrata sulla finestra sottostante ](images/win-dialog-box-image10.png)

Concentrare inizialmente i dialoghi nella parte superiore della finestra proprietaria.

-   **Se una finestra di dialogo è contestuale, visualizzarla accanto all'oggetto da cui è stata avviata.** Tuttavia, posizionarlo fuori dalla modalità (preferibilmente offset verso il basso e verso destra) in modo che l'oggetto non sia coperto dalla finestra di dialogo.

![diagramma dell'offset della finestra di dialogo verso il basso e verso destra ](images/win-dialog-box-image11.png)

Le proprietà di un oggetto vengono visualizzate accanto all'oggetto.

-   **Per le finestre di dialogo non modali, visualizzare inizialmente nella parte superiore della finestra proprietaria per facilitarne l'individuazione.** Se l'utente attiva la finestra proprietaria, questa potrebbe nascondere la finestra di dialogo non modale.
-   **Se necessario, modificare la posizione iniziale in modo che l'intera finestra di dialogo sia visibile all'interno del monitor di destinazione.** Se una finestra ridimensionabile è più grande del monitor di destinazione, ridurla per adattarla.
-   **Quando una finestra di dialogo viene visualizzata nuovamente, provare a visualizzarla nello stesso stato dell'ultimo accesso.** Al termine, salvare il monitoraggio usato, le dimensioni della finestra, la posizione e lo stato (ingrandito rispetto al ripristino). Durante la rivisualizzazione ripristinare le dimensioni, la posizione e lo stato della finestra di dialogo salvata utilizzando il monitor appropriato. Si consiglia inoltre di fare in modo che questi attributi vengano mantenuti tra le istanze del programma in base ai singoli utenti.
-   **Per le finestre ridimensionabili, impostare una dimensione minima della finestra se è presente una dimensione al di sotto della quale il contenuto non è più utilizzabile.** Provare a modificare la presentazione per rendere il contenuto utilizzabile a dimensioni inferiori.

![screenshot dei pulsanti del lettore multimediale centrato ](images/win-dialog-box-image12.png)

In questo esempio, Windows Media Player modifica il formato quando la finestra diventa troppo piccola per il formato standard.

-   **Non usare l'attributo always on top.**
    -   **Eccezione:** Utilizzare solo quando una finestra di dialogo implementa un'operazione essenzialmente modale, ma deve essere sospesa brevemente per accedere alla finestra proprietaria. Ad esempio, durante il controllo ortografico di un documento, è possibile che gli utenti lascino occasionalmente la finestra di dialogo controllo ortografico e accedano al documento per correggere gli errori.

Per ulteriori informazioni ed esempi, vedere [gestione della finestra](win-window-mgt.md).

### <a name="title-bars"></a>Barre del titolo

-   **Le finestre di dialogo non hanno icone della barra del titolo.** Le icone della barra del titolo vengono usate come distinzione visiva tra le finestre [primarie](glossary.md) e le [finestre secondarie](glossary.md).
    -   **Eccezione:** Se viene utilizzata una finestra di dialogo per implementare una finestra primaria, ad esempio un'utilità, che viene quindi visualizzata sulla barra delle applicazioni, è presente un'icona della barra del titolo. In questo caso, ottimizzare il titolo per la visualizzazione sulla barra delle applicazioni, inserendo prima di tutto le informazioni di distinzione.
-   **Nelle finestre di dialogo è sempre presente un pulsante Chiudi.** Anche le finestre di dialogo non modali possono avere un pulsante Riduci a icona. Le finestre di dialogo ridimensionabili possono avere un pulsante Ingrandisci.
-   **Non disabilitare il pulsante Chiudi.** Un pulsante Chiudi consente agli utenti di mantenere il controllo consentendo loro di chiudere le finestre che non vogliono.
    -   **Eccezione:** Per le finestre di dialogo di stato, è possibile disabilitare il pulsante Chiudi se l'attività deve essere eseguita fino al completamento per ottenere uno stato valido o impedire la perdita di dati.
-   **Il pulsante Chiudi sulla barra del titolo deve avere lo stesso effetto del pulsante Annulla o Chiudi** nella finestra di dialogo. Non assegnare mai lo stesso effetto di OK.
-   Se la didascalia e l'icona della barra del titolo sono già visualizzate in un modo importante nella parte superiore della finestra, è possibile nascondere la didascalia e l'icona della barra del titolo per evitare la ridondanza. Tuttavia, è comunque necessario impostare un titolo appropriato internamente per l'uso da Windows.

### <a name="interaction"></a>Interazione

-   **Quando vengono visualizzate, le finestre di dialogo avviate dall'utente devono sempre prendere lo stato attivo per l'input.** Le finestre di dialogo avviate dal programma non devono assumere lo stato attivo per l'input perché l'utente potrebbe interagire con un'altra finestra. Tale interazione erroneamente indirizzata alla finestra di dialogo può avere conseguenze impreviste.
-   **Assegnare lo stato attivo per l'input iniziale al controllo che gli utenti con maggiore probabilità interagiranno prima**, che è in genere (ma non sempre) il primo controllo interattivo. Evitare di assegnare lo stato attivo per l'input iniziale a un collegamento alla guida.
-   **Per la navigazione tramite tastiera, l'ordine di tabulazione deve essere propagata in ordine logico, in genere da sinistra verso destra, dall'alto verso il basso.** In genere l'ordine di tabulazione segue l'ordine di lettura, ma è consigliabile eseguire le eccezioni seguenti:

    -   Inserire i controlli più comunemente utilizzati in precedenza in ordine di tabulazione.
    -   Inserire i collegamenti della guida nella parte inferiore di una finestra di dialogo, dopo i pulsanti di commit in ordine di tabulazione.

    Quando si assegna l'ordine, si supponga che gli utenti visualizzino le finestre di dialogo per lo scopo previsto; quindi, ad esempio, gli utenti visualizzano le finestre di dialogo scelte per scegliere, non esaminare e fare clic su Annulla.

-   **Premendo il tasto ESC viene sempre chiusa una finestra di dialogo attiva.** Questo vale per le finestre di dialogo con annullamento o chiusura e anche se Annulla è stato rinominato per chiudere perché i risultati non possono più essere annullati.

**Chiavi di accesso**

-   **Laddove possibile, assegnare chiavi di accesso univoche a tutti i controlli interattivi o alle relative etichette.** Le [caselle di testo](ctrl-text-boxes.md) di sola lettura sono controlli interattivi (poiché gli utenti possono scorrerli e copiare testo) in modo da trarre vantaggio dalle chiavi di accesso. **Non assegnare chiavi di accesso a:**
    -   **Pulsanti OK, Annulla e Chiudi.** Per le chiavi di accesso vengono usati Enter e ESC. Tuttavia, assegnare sempre una chiave di accesso a un controllo che significa OK o Annulla, ma con un'etichetta diversa.

        ![screenshot della finestra di dialogo Elimina file ](images/win-dialog-box-image13.png)

        In questo esempio il pulsante di commit positivo ha una chiave di accesso assegnata.

    -   **Etichette del gruppo.** In genere, i singoli controlli all'interno di un gruppo vengono assegnati alle chiavi di accesso, quindi l'etichetta del gruppo non ne ha bisogno. Tuttavia, se è presente una carenza di chiavi di accesso, assegnare una chiave di accesso all'etichetta del gruppo e non ai singoli controlli.
    -   **Pulsanti della Guida generici,** a cui è possibile accedere con F1.
    -   **Etichette di collegamento.** Spesso sono presenti troppi collegamenti per assegnare chiavi di accesso univoche e i caratteri di sottolineatura usati spesso per indicare i collegamenti nascondono i caratteri di sottolineatura della chiave di accesso. Accedere ai collegamenti con il tasto TAB.
    -   **Nomi delle schede.** Le tabulazioni vengono ciclate con CTRL + TAB e CTRL + MAIUSC + TAB.
    -   **Pulsanti Sfoglia con etichetta "...".** A questi pulsanti di esplorazione non è possibile assegnare chiavi di accesso in modo univoco.
    -   **Controlli senza etichetta,** ad esempio controlli di selezione, pulsanti di comando grafici e controlli di divulgazione progressivi senza etichetta.
    -   **Testo statico senza etichetta o etichette per i controlli che non sono interattivi,** ad esempio le barre di stato.

-   **Laddove possibile, assegnare le chiavi di accesso per i comandi usati di frequente in base alle assegnazioni di chiavi di accesso standard**. Sebbene le assegnazioni di chiavi di accesso coerenti non siano sempre possibili, sono certamente preferite soprattutto per le finestre di dialogo di uso frequente.
-   **Assegnare prima di tutto i pulsanti di accesso per assicurarsi che abbiano le assegnazioni di chiavi standard.** Se non è disponibile un'assegnazione di chiave standard, usare la prima lettera della prima parola. La chiave di accesso per i pulsanti Sì e no commit, ad esempio, deve essere sempre "Y" e "N", indipendentemente dagli altri controlli della finestra di dialogo.
-   **Per semplificare la ricerca delle chiavi di accesso, assegnare le chiavi di accesso a un carattere che viene visualizzato all'inizio dell'etichetta,** idealmente il primo carattere, anche se è presente una parola chiave che viene visualizzata più avanti nell'etichetta.
-   **Preferisce caratteri con larghezze ampie,** ad esempio w, m e lettere maiuscole.
-   **Preferisce una consonante distinta o una vocale,** ad esempio "x" in uscita.
-   **Evitare l'uso di caratteri che rendono difficile la visualizzazione della sottolineatura,** ad esempio (dal più problematico al meno problematico):
    -   Lettere con una sola larghezza di pixel, ad esempio i e l.
    -   Lettere con discendenti, ad esempio g, j, p, q e y.
    -   Lettere accanto a una lettera con un discendente.

Per altre linee guida ed esempi, vedere [tastiera](inter-keyboard.md).

### <a name="progress-dialogs"></a>Finestre di dialogo di stato

Per le attività a esecuzione prolungata, **si supponga che gli utenti eseguano un'altra operazione durante il completamento dell'attività**. Progettare l'attività per l'esecuzione automatica.

-   **Presentare agli utenti la finestra di dialogo per il feedback dello stato di avanzamento se un'operazione richiede più di cinque secondi per il completamento**, insieme a un comando per annullare o arrestare l'operazione.
    -   **Eccezione:** Per le procedure guidate e i flussi di attività, utilizzare una finestra di dialogo modale per lo stato di avanzamento solo se l'attività rimane nella stessa pagina (anziché avanzare a un'altra pagina) e gli utenti non possono eseguire operazioni in attesa. In caso contrario, utilizzare una pagina stato o uno stato di avanzamento sul posto.
-   Se l'operazione è un'attività a esecuzione prolungata (oltre 30 secondi) e può essere eseguita in background, utilizzare una finestra di dialogo di stato non modale in modo che gli utenti possano continuare a utilizzare il programma in attesa.
-   Finestre di dialogo di avanzamento non modale:
    -   Avere un pulsante Riduci a icona sulla barra del titolo.
    -   Vengono visualizzati sulla barra delle applicazioni.
-   Implementare le finestre di dialogo di avanzamento non modale in modo che continuino a essere eseguite anche se la finestra proprietaria è chiusa.

![screenshot della finestra di dialogo Copia con indicatore di stato ](images/win-dialog-box-image14.png)

In questo esempio, la copia del file continua anche se la finestra proprietaria è chiusa.

-   **Fornire un pulsante di comando per arrestare l'operazione se il completamento richiede più di alcuni secondi oppure non è possibile completare mai il tentativo.** Etichetta il pulsante Annulla se l'annullamento restituisce l'ambiente allo stato precedente (senza effetti collaterali); in caso contrario, etichettare il pulsante Interrompi per indicare che lascia intatta l'operazione parzialmente completata. È possibile modificare l'etichetta del pulsante da Annulla per arrestarsi durante l'operazione, se a un certo punto non è possibile ripristinare lo stato precedente dell'ambiente.

![screenshot della finestra di dialogo con pulsante Annulla ](images/win-dialog-box-image15.png)

In questo esempio, l'arresto della diagnosi dei problemi non ha alcun effetto collaterale.

-   **Fornire un pulsante di comando per sospendere l'operazione se sono necessari più di alcuni minuti per il completamento e la capacità degli utenti di svolgere il lavoro.** Questa operazione non impone all'utente di scegliere se completare l'attività e di svolgere il proprio lavoro.
-   **Raccogliere quante più informazioni possibile prima di avviare l'attività.**
-   **Se vengono rilevati problemi reversibili, gli utenti devono gestire tutti i problemi individuati alla fine dell'attività.** Se ciò non è pratico, gli utenti possono gestire i problemi non appena si verificano.
-   **Non abbandonare le attività come risultato di errori reversibili.**

![screenshot della finestra di dialogo con il pulsante Riprova ](images/win-dialog-box-image16.png)

In questo esempio Esplora risorse consente agli utenti di continuare l'attività dopo un errore reversibile.

-   **Indica i problemi ruotando l'indicatore di stato rosso.**

![screenshot dell'indicatore di stato e pulsante Riprova ](images/win-dialog-box-image17.png)

In questo esempio un disco rimovibile è stato rimosso durante la copia di un file.

-   **Se i risultati sono chiaramente evidenti per gli utenti, chiudere la finestra di dialogo di stato automaticamente al termine del processo.** In caso contrario, utilizzare il feedback solo per segnalare problemi:
    -   Per visualizzare commenti e suggerimenti semplici, visualizzare i commenti e i suggerimenti nella finestra di dialogo di stato e modificare il pulsante Annulla per chiudere.
    -   Per visualizzare commenti dettagliati, chiudere la finestra di dialogo stato e visualizzare una finestra di dialogo informativa.

**Non usare una notifica per il feedback di completamento.** Usare una finestra di dialogo di stato o una [notifica di esito positivo dell'azione](mess-notif.md), ma non entrambe.

**Tempo rimanente**

-   **Usare i formati di ora seguenti.** Iniziare con il primo dei formati seguenti, in cui l'unità di tempo più grande non è zero, quindi passare al formato successivo quando l'unità di tempo più grande diventa zero.

**Per gli indicatori di stato:**

**Se le informazioni correlate vengono visualizzate nel formato due punti:**

Tempo rimanente: h ore, m minuti

Tempo rimanente: m minuti, s secondi

Tempo rimanente: s secondi

**Se lo spazio sullo schermo è Premium:**

ore h, m minuti rimanenti

m min, s sec rimanenti

secondi rimanenti

**In caso contrario**

ore h, m minuti rimanenti

m minuti, s secondi rimanenti

secondi rimanenti

**Per le barre del titolo:**

HH: mm rimanenti

mm: SS rimanenti

0: SS rimanenti

Questo formato compatto Mostra prima le informazioni più importanti, in modo che non vengano troncate sulla barra delle applicazioni.

-   **Rendere accurate le stime, ma non dare una precisione falsa.** Se l'unità più grande è di ore, concedere minuti (se significativo) ma non secondi.

**Non corretto:**

hh ore, mm minuti, ss secondi

-   **Tenere aggiornata la stima.** Aggiornare le stime rimanenti almeno ogni 5 secondi.
-   **Concentrarsi sul tempo rimanente, in** quanto si tratta delle informazioni che gli utenti si occupano maggiormente. Fornire tempo totale trascorso solo quando sono presenti scenari in cui è utile il tempo trascorso, ad esempio quando è probabile che l'attività venga ripetuta. Se il tempo rimanente stimato è associato a un indicatore di stato, non è presente un testo con percentuale di completamento perché tali informazioni vengono trasmesse dall'indicatore di stato.
-   **Essere grammaticamente corretti.** Usare unità singolari quando il numero è uno.

**Non corretto:**

1 minuto, 1 secondo

-   **Usare le maiuscole/minuscole come nelle frasi comuni.**

Per ulteriori informazioni ed esempi, vedere la pagina relativa agli [indicatori di stato](progress-bars.md).

### <a name="icons-and-graphics"></a>Icone e grafica

**Grafica**

-   **Non usare elementi grafici di grandi dimensioni che non sono in grado di riempire lo spazio con Eye Candy.** In alternativa, Mantieni l'aspetto semplice.

**Non corretto:**

![screenshot della finestra di dialogo con un grafico di grandi dimensioni ](images/win-dialog-box-image18.png)

In questo esempio, l'immagine di grandi dimensioni non ha alcun effetto.

**Icone della barra del titolo**

-   **Le finestre di dialogo non hanno icone della barra del titolo.**
    -   **Eccezione:** Se viene utilizzata una finestra di dialogo per implementare una finestra primaria, ad esempio un'utilità, che viene quindi visualizzata sulla barra delle applicazioni, è presente un'icona della barra del titolo.

**Icone del corpo**

-   **Scegliere l'icona del corpo in base al modello di progettazione:**



|                                      |                                                                                                                            |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| **Modello**<br/>               | **Icona corpo**<br/>                                                                                                   |
| **Finestre di dialogo delle domande**<br/>      | Programma, funzionalità, oggetto, icona di avviso (se è possibile perdita di dati o accesso al sistema), avviso di sicurezza o nessuno.<br/> |
| **Finestre di dialogo scelte**<br/>        | Nessuna.<br/>                                                                                                           |
| **Finestre di dialogo di stato**<br/>      | None (ma può avere un'animazione).<br/>                                                                               |
| **Finestre di dialogo informative**<br/> | Nessuna.<br/>                                                                                                           |



 

-   **Non corretto:**

![screenshot della finestra di dialogo con icona di avviso ](images/win-dialog-box-image19.png)

In questo esempio, un'icona di avviso viene utilizzata erroneamente per una domanda che non implica la perdita potenziale di dati o l'accesso al sistema.

- **Si consiglia di usare le icone per consentire agli utenti di riconoscere visivamente le funzionalità del programma.** Questa tecnica è particolarmente efficace quando le icone sono facilmente riconoscibili e vengono usate in diverse posizioni all'interno del programma.

![screenshot della finestra di dialogo Preferiti con icona a stella ](images/win-dialog-box-image20.png)

In questo esempio, l'icona a stella gialla rappresenta i Preferiti. L'icona è facilmente riconoscibile e viene usata in modo coerente in tutte le finestre per rappresentare i Preferiti.

-   **Usare le icone per consentire agli utenti di riconoscere l'oggetto in questione.**

![screenshot della finestra di dialogo con icona PowerPoint ](images/win-dialog-box-image21.png)

In questo esempio, l'icona dell'oggetto consente agli utenti di riconoscere il tipo di file aperto o salvato.

-   **Prendere in considerazione l'uso delle icone per semplificare la comprensione delle funzionalità.**

![immagini di frecce che mostrano come posizionare il monitoraggio ](images/win-dialog-box-image22.png)

In questo esempio, queste icone consentono agli utenti di visualizzare l'effetto delle proprie funzionalità.

-   **Utilizzare un'icona nelle finestre di dialogo informazioni per la personalizzazione dell'applicazione.**

![screenshot della finestra di dialogo informazioni su con logo Windows ](images/win-dialog-box-image23.png)

In questo esempio viene usata una bitmap nella casella About (informazioni) per identificare e personalizzare l'applicazione.

**Icone a piè di pagina**

-   **Se si dispone di una nota a piè di pagina, provare a usare un'icona a piè di pagina per riepilogare l'oggetto della nota.**

![screenshot della finestra di dialogo con icona a piè di pagina ](images/win-dialog-box-image24.png)

In questo esempio, l'icona a piè di pagina indica che la domanda presenta implicazioni di sicurezza.

-   **Non usare un'icona a piè di pagina che ripete l'icona del corpo.**
-   **Non usare le icone degli errori o delle informazioni standard.** Le condizioni di errore devono essere trasmesse attraverso l'icona del corpo e le note a piè di pagina sono sempre per informazioni, rendendo ridondante l'icona delle informazioni. Tuttavia, è possibile usare l'icona di avviso standard e lo scudo di sicurezza giallo per segnalare agli utenti le conseguenze rischiose.

Per ulteriori informazioni ed esempi, vedere [Icone](vis-icons.md).

### <a name="commit-buttons"></a>Pulsanti di commit

**Note:**

-   Queste linee guida non si applicano ai dialoghi delle domande usando i collegamenti ai comandi, perché tale modello usa i collegamenti al comando anziché i pulsanti.
-   \[Eseguire questa operazione \] e \[ non eseguire \] le risposte in modo positivo e negativo, rispettivamente, all'istruzione principale.

**Generale**

-   **Scegliere i pulsanti commit in base al modello di progettazione:**

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td><strong>Modello</strong><br/></td>
    <td><strong>Pulsanti di commit</strong><br/></td>
    </tr>
    <tr class="even">
    <td><strong>Finestre di dialogo delle domande (usando i pulsanti)</strong><br/></td>
    <td>Uno dei seguenti set di comandi concisi: Yes/No, Yes/No/Cancel, [do it]/Cancel, [do it]/[not do it], [do it]/[not do it]/Cancel.<br/></td>
    </tr>
    <tr class="odd">
    <td><strong>Finestre di dialogo delle domande (usando i collegamenti)</strong><br/></td>
    <td>Annulla.<br/></td>
    </tr>
    <tr class="even">
    <td><strong>Finestre di dialogo scelte</strong><br/></td>
    <td><ul>
    <li>Finestre di dialogo modali: OK/Annulla o [do it]/Cancel</li>
    <li>Finestre di dialogo non modali: pulsante Chiudi nella finestra di dialogo e nella barra del titolo</li>
    <li>Riquadro attività: pulsante Chiudi sulla barra del titolo</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><strong>Finestre di dialogo di stato</strong><br/></td>
    <td>Usare Annulla se restituisce l'ambiente allo stato precedente (senza effetto collaterale); in caso contrario, utilizzare Interrompi.<br/></td>
    </tr>
    <tr class="even">
    <td><strong>Finestre di dialogo informative</strong><br/></td>
    <td>Quasi.<br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   **Tutti i pulsanti commit eccetto Apply determinano la chiusura della finestra di dialogo.**
-   **Non confermare i pulsanti di commit.** Questa operazione inutilmente può essere molto fastidiosa. **Eccezioni**

    -   L'azione è potenzialmente catastrofica.
    -   L'azione è chiaramente incoerente con altre azioni.
    -   Se non è corretta, l'azione può comportare una perdita significativa di dati, tempo o impegno per conto dell'utente.

    Per altre linee guida ed esempi, vedere [conferme](mess-confirm.md).

-   **Non disabilitare i pulsanti di commit. Eccezioni**
    -   **Se gli utenti devono elevare per apportare una modifica, disabilitare i pulsanti di commit positivi fino a quando l'utente non apporta una modifica.** In questo modo si impedisce agli utenti di elevare solo la chiusura di una finestra forzando il clic su Annulla.
    -   Per ulteriori eccezioni, vedere la pagina relativa alla [disabilitazione o alla rimozione di controlli rispetto a messaggi di errore](#disabling-or-removing-controls-vs-giving-error-messages).
-   **Allinea a destra i pulsanti di commit in una singola riga nella parte inferiore della finestra di dialogo,** ma sopra l'area della nota. Eseguire questa operazione anche se è presente un singolo pulsante di commit (ad esempio OK).

    **Non corretto:**

    ![screenshot del messaggio con pulsante OK centrato ](images/win-dialog-box-image25.png)

    In questo esempio il pulsante OK non è centrato correttamente.

-   **Presentare i pulsanti commit nell'ordine seguente:**
    1.  OK/ \[ \] /Yes
    2.  \[Non \] /No
    3.  Annulla
    4.  Applica (se presente)
    5.  Guida (se presente)
-   **Se sono presenti molti pulsanti di commit correlati, consolidarli usando i pulsanti di divisione**.
-   **Avere una netta separazione dai pulsanti di commit (che chiudono la finestra) e da tutti gli altri pulsanti di comando (ad esempio Advanced).**

**Risposta alle istruzioni principali**

-   **Usare i pulsanti di commit positivi che sono risposte specifiche all'istruzione principale, anziché etichette generiche, ad esempio OK o Sì/No.** Gli utenti devono essere in grado di comprendere le opzioni leggendo il testo del pulsante da solo. **Eccezioni**
    -   Utilizzare Close per le finestre di dialogo che non dispongono di impostazioni, ad esempio le finestre di dialogo informative. Non usare mai Close per le finestre di dialogo con impostazioni.
    -   Usare OK quando le risposte "specifiche" sono ancora generiche, ad esempio Save, SELECT o Choose. Utilizzare OK quando si modifica un'impostazione specifica o una raccolta di impostazioni.
    -   **Per le finestre di dialogo legacy senza un'istruzione principale, è possibile utilizzare etichette generiche, ad esempio OK.** Spesso tali finestre di dialogo non sono progettate per eseguire un'attività specifica, impedendo risposte più specifiche.
    -   Alcune attività richiedono un maggior numero di letture e una lettura attenta per consentire agli utenti di prendere decisioni informate. Questo è in genere il caso di [conferme](mess-confirm.md). **In questi casi, è possibile usare intenzionalmente le etichette dei pulsanti di commit generici per forzare gli utenti a leggere le istruzioni principali e a prevenire decisioni affrettate.**

        **Corretto:**

        ![screenshot del messaggio con pulsanti Sì e no](images/win-dialog-box-image26.png)

        In questo esempio, l'uso dei pulsanti Sì/no commit impone agli utenti di leggere almeno l'istruzione principale.

-   In **alternativa, è possibile aggiungere la parola "comunque" all'etichetta del pulsante di commit positivo per indicare che la finestra di dialogo presenta un motivo per non continuare** e che gli utenti devono leggere attentamente il dialogo prima di procedere.

    **Corretto:**

    ![screenshot del messaggio e pulsante Disinstalla comunque ](images/win-dialog-box-image27.png)

    In questo esempio viene aggiunto "comunque" all'etichetta del pulsante commit per indicare che gli utenti devono procedere con cautela.

-   **Usare Annulla o Chiudi per i pulsanti di commit negativi anziché risposte specifiche all'istruzione principale.** Spesso gli utenti si rendono conto che non desiderano eseguire un'attività una volta visualizzata una finestra di dialogo. Se Cancel o Close sono stati rietichettati per risposte specifiche, gli utenti dovrebbero leggere attentamente tutti i pulsanti commit per determinare la modalità di annullamento. **L'assegnazione di etichette all'annullamento e alla chiusura li rende più facili da trovare. Eccezioni**
    -   **Non usare Yes/Cancel.** Usare sempre Yes/No come coppia.
    -   **Usare una risposta specifica quando l'annullamento è ambiguo.**
-   **Non eseguire il mapping di etichette generiche al significato specifico con il testo nell'area del contenuto.** Usare invece etichette di pulsanti di commit specifiche o una finestra di dialogo di domanda usando i collegamenti se le etichette sono lunghe.

    **Non corretto:**

    ![screenshot del messaggio con utilizzo non chiaro dei pulsanti ](images/win-dialog-box-image28.png)

    In questo esempio, è stato eseguito il mapping di OK per continuare, viene eseguito il mapping dell'annullamento per rimanere nella pagina.

**Pulsanti Sì e no**

-   **Preferisce risposte specifiche ai pulsanti Sì e no.** Sebbene non esistano problemi con l'uso di sì e No, le risposte specifiche possono essere interpretate più rapidamente, ottenendo un processo decisionale efficace. Tuttavia, le [conferme](mess-confirm.md) hanno in genere i pulsanti Sì e No per fare in [modo che gli](mess-confirm.md) utenti diano la conferma prima di rispondere.
-   **Usare i pulsanti Sì e no solo per rispondere alle domande sì o no.** L'istruzione principale deve essere naturalmente espressa come domanda sì o no. Non usare mai OK e Annulla per domande sì o no.

    **Non corretto:**

    ![Screenshot che mostra un messaggio con ' OK ' per una domanda sì-no.](images/win-dialog-box-image29.png)

    **Corretto:**

    ![screenshot del messaggio con Sì per la stessa domanda ](images/win-dialog-box-image30.png)

    **Migliore:**

    ![screenshot del messaggio con esecuzione per la stessa domanda ](images/win-dialog-box-image31.png)

    In questi esempi, sì e no sono risposte ottimali a Sì e a nessuna domanda, ma le risposte specifiche sono ancora migliori.

-   **Provare a formulare l'istruzione principale come una domanda sì o no se i pulsanti di commit con una formulazione specifica si rivolgono a lunghe o scomode.** In alternativa, è possibile usare i collegamenti ai comandi per risposte più lunghe (cinque parole o più) all'istruzione principale.

    **Non corretto:**

    ![screenshot del messaggio con etichette dei pulsanti di Wordy ](images/win-dialog-box-image32.png)

    **Corretto:**

    ![screenshot del messaggio con etichette dei pulsanti Sì/No ](images/win-dialog-box-image33.png)

    Il formulazione specifica nell'esempio errato è troppo lungo, quindi nell'esempio corretto viene usato Yes e no.

-   **Non usare i pulsanti Sì e no se il significato di nessuna risposta non è chiaro.** In caso affermativo, usare invece risposte specifiche.

**Pulsanti OK**

-   **Nelle finestre di dialogo modali fare clic su OK per applicare i valori, eseguire l'attività e chiudere la finestra.**
-   **Non usare i pulsanti OK per rispondere alle domande.**
-   **Non assegnare chiavi di accesso a OK, perché immettere è la chiave di accesso per il pulsante predefinito.** In questo modo le altre chiavi di accesso risultano più semplici da assegnare.
-   **Etichetta OK pulsanti corretti.** Il pulsante OK dovrebbe essere etichettato OK, non OK o OK.
-   **Non usare i pulsanti OK per gli errori o gli avvisi.** I problemi non sono mai OK. In alternativa, utilizzare Close.

    **Non corretto:**

    ![screenshot del messaggio con il pulsante OK ](images/win-dialog-box-image34.png)

    In questo esempio, è necessario utilizzare Close anziché OK.

-   **Non usare i pulsanti OK nelle finestre di dialogo non modali.** Piuttosto, le finestre di dialogo non modali devono usare pulsanti di commit specifici dell'attività, ad esempio find. Tuttavia, alcune finestre di dialogo non modali richiedono solo un pulsante Chiudi.

**Pulsanti Annulla**

-   **Se si fa clic su Annulla, vengono ignorate tutte le modifiche, si annulla l'attività, si chiude la finestra e si ripristina lo stato precedente dell'ambiente, senza alcun effetto collaterale.** Per le finestre di dialogo di selezione nidificata, facendo clic su Annulla nella finestra di dialogo di scelta del proprietario si abbandonano anche le modifiche apportate dalle finestre di dialogo di proprietà
-   **Fornire un pulsante Annulla per consentire agli utenti di abbandonare in modo esplicito le modifiche.** Per le finestre di dialogo è necessario un punto di uscita chiaro. Non dipendere dagli utenti che trovano il pulsante Chiudi sulla barra del titolo.

    -   **Eccezione:** Non specificare un pulsante Annulla per le finestre di dialogo senza impostazioni. In questo caso i pulsanti OK e Chiudi hanno lo stesso effetto di Annulla.

    **Non corretto:**

    ![screenshot del messaggio con solo pulsante OK ](images/win-dialog-box-image35.png)

    In questo esempio, se si dispone solo di un pulsante Chiudi sulla barra del titolo, viene visualizzato come se gli utenti non hanno una scelta.

-   **Non usare i pulsanti Annulla per rispondere alle domande.**

    **Non corretto:**

    ![screenshot del messaggio con OK per Sì, nessuna domanda ](images/win-dialog-box-image36.png)

    In questo esempio OK e Annulla vengono erroneamente usati per rispondere a una domanda sì o no.

-   **Non assegnare chiavi di accesso per l'annullamento, perché ESC è il tasto di accesso.** In questo modo le altre chiavi di accesso risultano più semplici da assegnare.
-   **Non usare i pulsanti Annulla nelle finestre di dialogo non modali.** Usare invece Close.
-   **Non disabilitare il pulsante Annulla.** Gli utenti devono essere sempre in grado di annullare le finestre di dialogo.
    -   **Eccezione:** È possibile disabilitare il pulsante Annulla in una finestra di dialogo di stato se si verifica un periodo durante il quale l'operazione non può essere annullata. Tuttavia, una soluzione migliore consiste nel progettare tali operazioni in modo da essere sempre annullabili.

**Chiudi pulsanti**

-   **Usare i pulsanti Chiudi per le finestre di dialogo non modali, nonché le finestre di dialogo modali che non possono essere annullate.**
-   **Se si fa clic su Chiudi si chiude la finestra di dialogo, lasciando gli effetti collaterali esistenti.** Non usare done perché non è una costruzione imperativa. Per le finestre di dialogo di selezione nidificata, facendo clic su Chiudi nella finestra di dialogo scelta proprietario viene mantenuta qualsiasi modifica apportata dalle finestre di dialogo di proprietà
-   **Inserire un pulsante Chiudi esplicito nel corpo della finestra di dialogo.** Per le finestre di dialogo è necessario un punto di uscita chiaro. Non dipendere dagli utenti che trovano il pulsante Chiudi sulla barra del titolo.
-   **Verificare che il pulsante Chiudi sulla barra del titolo abbia lo stesso effetto di Annulla o Chiudi.**
-   **Non assegnare chiavi di accesso per chiudere, perché ESC è la chiave di accesso.** In questo modo le altre chiavi di accesso risultano più semplici da assegnare.

**Pulsanti applica**

-   **Non usare pulsanti applica nelle finestre di dialogo che non sono finestre delle proprietà o pannelli di controllo.** Il pulsante Applica significa applicare le modifiche in sospeso, ma lasciare aperta la finestra. Questa operazione consente agli utenti di valutare le modifiche prima di chiudere la finestra. Tuttavia, solo la finestra delle proprietà e i pannelli di controllo hanno questa esigenza.

    **Non corretto:**

    ![screenshot della finestra di dialogo con il pulsante applica ](images/win-dialog-box-image37.png)

    In questo esempio, una finestra di dialogo di scelta ha inutilmente un pulsante Applica.

**Pulsanti di commit per le finestre di dialogo indirette**

**Nota:** Le finestre di dialogo indirette vengono visualizzate fuori contesto, come risultato indiretto di un'attività o il risultato di un problema con un processo di sistema o in background. Per le finestre di dialogo indirette, il pulsante Annulla è ambiguo perché potrebbe significare annullare la finestra di dialogo o annullare l'intera attività.

-   **Se gli utenti devono annullare la finestra di dialogo e l'attività, assegnare i pulsanti commit per eseguire entrambe le operazioni.** Etichetta il pulsante che annulla la finestra di dialogo con una risposta negativa all'istruzione principale. Etichetta il pulsante che annulla l'intera attività con Annulla. Con Annulla è possibile utilizzare la finestra di dialogo in molti contesti.

    **Corretto:**

    ![screenshot della finestra di dialogo con Save/not save ](images/win-dialog-box-image38.png)

    In questo esempio, questa finestra di dialogo viene visualizzata da Windows Paint come risultato di un comando New o Exit quando il grafico non è stato salvato. Non salvare chiude la finestra di dialogo senza salvare, mentre Annulla Annulla il comando nuovo o Esci.

    **Non corretto:**

    ![screenshot della finestra di dialogo con i pulsanti Sì/No ](images/win-dialog-box-image39.png)

    In questo esempio, non è possibile annullare l'attività (chiudendo la barra dei collegamenti dell'ufficio) che ha portato a visualizzare questa finestra di dialogo. Per questa finestra di dialogo è necessario un pulsante Annulla.

-   **Se gli utenti devono semplicemente annullare la finestra di dialogo, ma non l'attività, utilizzare un pulsante con una risposta specifica negativa all'istruzione principale** e non avere un pulsante Annulla.

    ![screenshot della finestra di dialogo con esecuzione/non esecuzione ](images/win-dialog-box-image24.png)

    In questo esempio, questa finestra di dialogo viene visualizzata indirettamente come risultato della navigazione a una pagina Web in cui viene installato un controllo ActiveX. L'uso di Cancel è ambiguo, quindi non viene utilizzato.

Per ulteriori informazioni ed esempi, vedere [pulsanti di comando](ctrl-command-buttons.md).

### <a name="command-links"></a>Collegamenti ai comandi

-   **Presentare un set di comandi lunghi usando i collegamenti ai comandi, invece dei pulsanti di comando o una combinazione di pulsanti di opzione e un pulsante OK.** Questa operazione consente agli utenti di rispondere con un solo clic. Tuttavia, questo approccio funziona solo per una singola domanda.
-   **Presentare prima i collegamenti ai comandi usati più di frequente.** L'ordine risultante dovrebbe approssimativamente rispettare la probabilità di utilizzo, ma anche un flusso logico.
    -   **Eccezione:** I collegamenti ai comandi che comportano l'operazione devono essere inseriti per primi.
-   Se un collegamento al comando richiede un'ulteriore spiegazione, **fornire una spiegazione aggiuntiva.** Le spiegazioni aggiuntive descrivono perché gli utenti potrebbero voler scegliere il comando o cosa accade se si sceglie il comando.
-   **Non usare spiegazioni aggiuntive che siano riformulazioni di testo del collegamento del comando.** Usare una spiegazione aggiuntiva solo quando non è possibile rendere il collegamento di un comando di chiara interpretazione. Fornire una spiegazione aggiuntiva per un collegamento al comando non significa che è necessario fornirli per tutti i comandi.

![screenshot della finestra di dialogo con le opzioni di annotazione del testo ](images/win-dialog-box-image40.png)

In questo esempio la spiegazione supplementare descrive le implicazioni di una delle opzioni.

-   **Utilizzare frasi che iniziano con un verbo, senza la punteggiatura finale.**
-   **Se si consiglia di usare un comando, è consigliabile aggiungere "(scelta consigliata)" all'etichetta.** Assicurarsi di aggiungere all'etichetta di collegamento, non la spiegazione aggiuntiva.
-   **Se un comando è destinato solo agli utenti avanzati, è consigliabile aggiungere "(Advanced)" all'etichetta.** Assicurarsi di aggiungere all'etichetta di collegamento, non la spiegazione aggiuntiva.
-   **Fornire sempre un pulsante Annulla esplicito**. Non usare un collegamento di comando a questo scopo.

**Non corretto:**

![screenshot della finestra di dialogo con il collegamento non uscire ](images/win-dialog-box-image41.png)

In questo esempio, nella finestra di dialogo viene utilizzato un collegamento al comando anziché un pulsante Annulla.

Per ulteriori informazioni ed esempi, vedere [collegamenti ai comandi](ctrl-command-links.md).

### <a name="dont-show-this-item-again"></a>Non visualizzare <item> nuovo

-   **Provare a usare un'opzione non visualizzare <item> più questo messaggio per consentire agli utenti di disattivare una finestra di dialogo ricorrente, solo se non è disponibile un'alternativa migliore.** È sempre meglio visualizzare la finestra di dialogo se gli utenti ne hanno effettivamente bisogno o semplicemente eliminarla.
-   **Usare questa formulazione specifica Replace <item> con l'elemento specifico.** Ad esempio, non visualizzare più questo promemoria. Quando si fa riferimento a una finestra di dialogo in generale, usare non visualizzare più questo messaggio.
-   **Indica chiaramente quando verrà usato l'input dell'utente per i valori predefiniti futuri** aggiungendo la frase seguente nell'opzione: le selezioni verranno usate per impostazione predefinita in futuro.
-   **Non selezionare l'opzione per impostazione predefinita. Se la finestra di dialogo deve essere visualizzata una sola volta, eseguire questa operazione senza richiedere.** Non usare questa opzione come scusa per infastidire gli utenti per assicurarsi che il comportamento predefinito non sia fastidioso.

**Non corretto:**

![screenshot del messaggio che richiede una domanda superflua ](images/win-dialog-box-image42.png)

In questo esempio, il messaggio deve essere visualizzato solo una volta. Non è necessario richiedere.

-   **Rendere l'impostazione permanente in base ai singoli utenti.**
-   **Se gli utenti selezionano l'opzione e fanno clic su Annulla, questa opzione ha effetto.** Questa impostazione è una meta-opzione, quindi non segue il comportamento di annullamento standard di senza effetto collaterale. Si noti che se gli utenti non vogliono visualizzare la finestra di dialogo in futuro, è molto probabile che vogliano annullarla.
-   Se gli utenti potrebbero dover ripristinare queste finestre di dialogo, fornire un comando **Ripristina messaggi** nella finestra di dialogo Opzioni del programma.

### <a name="ask-me-later"></a>Richiedi in seguito

-   Specificare questa opzione per ignorare una finestra di dialogo solo quando:
    -   **La finestra di dialogo è indiretta**, quindi è probabile che gli utenti siano incentrati su un'altra attività.
    -   **Gli utenti devono rispondere ma non immediatamente**, in modo che possano continuare a lavorare.
    -   Per **la domanda è necessario un pensiero o un impegno sufficiente** , in modo che gli utenti possano prendere decisioni migliori in caso di maggiore tempo.
    -   **La finestra di dialogo o l'opzione verrà visualizzata automaticamente in un secondo momento** , in modo che gli utenti vengano effettivamente richiesti in un secondo momento.
-   **Non corretto:**
-   ![screenshot del messaggio con l'opzione Richiedi più tardi ](images/win-dialog-box-image43.png)
-   In questo esempio, la domanda è abbastanza semplice che l'aggiunta di un'opzione Richiedi in seguito ne complica solo l'operazione.
-   In caso contrario, si prevede che gli utenti rispondano ora, ma consentono loro di chiudere la finestra di dialogo normalmente con Annulla o Chiudi. Se utilizzata correttamente, questa opzione dovrebbe essere rara.

### <a name="morefewer"></a>Più o meno

-   **Usare pulsanti di divulgazione progressivi più o meno per mostrare o nascondere le opzioni, i comandi o i dettagli avanzati o usati raramente che gli utenti di destinazione non sono in genere necessari.** Questa operazione semplifica la finestra di dialogo per l'utilizzo tipico. Non nascondere le opzioni, i comandi o le informazioni utilizzate comunemente perché gli utenti potrebbero non trovarli.

![screenshot della finestra di dialogo con un pulsante altre opzioni ](images/win-dialog-box-image24.png)

In questo esempio le opzioni usate raramente sono nascoste per impostazione predefinita.

-   **Non usare controlli più o meno a meno che non ci siano più dettagli da mostrare.** Non solo riformulare le stesse informazioni in un formato diverso.
-   **Non usare più o meno controlli per visualizzare la guida.** Usare invece i collegamenti della guida o le note a piè di pagina.
-   **Con le finestre di dialogo delle attività, evitare di combinare un numero maggiore o minore di controlli con non visualizzare più questo messaggio <item> .** Questa combinazione ha un aspetto imbarazzante.
-   Per le linee guida sulle etichette, vedere [divulgazione progressiva](ctrl-progressive-disclosure-controls.md).

### <a name="footnotes"></a>Note a piè di pagina

-   **Utilizzare note a piè di pagina per informazioni non essenziali per lo scopo di una finestra di dialogo, ma che gli utenti potrebbero risultare utili per prendere decisioni.** La maggior parte degli utenti dovrebbe essere in grado di ignorare le note a piè di pagina e prendere decisioni informate nella risposta alla finestra di dialogo.

![screenshot della finestra di dialogo con chiarimenti a piè di pagina ](images/win-dialog-box-image44.png)

In questo esempio le informazioni sulla nota a piè di pagina sono supplementari, non essenziali.

### <a name="disabling-or-removing-controls-vs-giving-error-messages"></a>Disabilitazione o rimozione di controlli e assegnazione di messaggi di errore

-   Quando un controllo non viene applicato nel contesto corrente, prendere in considerazione le opzioni seguenti:
    -   **Rimuovere il controllo quando non esiste alcun modo per consentire agli utenti di abilitarlo oppure gli utenti non si aspettano che venga applicato e il suo stato non cambia di frequente.** Questa operazione semplifica la finestra di dialogo e gli utenti non lo perdono. La presenza di un controllo visualizzato e scompare spesso è fastidioso.
    -   **Disabilitare il controllo quando gli utenti si aspettano che venga applicato o il suo stato viene modificato frequentemente e gli utenti possono facilmente dedurre il motivo per cui il controllo è disabilitato.** Un esempio di deduzione facile è la disabilitazione di un pulsante di commit quando è presente una sola casella di testo vuota che richiede input. È possibile usare i [palloni](ctrl-balloons.md) per visualizzare problemi di input utente non critici con caselle di testo ed elenchi a discesa modificabili. Tuttavia, se il problema non può essere spiegato con un fumetto o include più controlli, la deduzione non sarà più semplice.
    -   **In caso contrario, lasciare il controllo abilitato, ma fornire un messaggio di errore quando viene usato in modo non corretto.** La disabilitazione in questo caso renderebbe difficile per gli utenti comprendere il motivo per cui il controllo è disabilitato. Gli utenti dovranno determinare il problema tramite la sperimentazione e la logica dedottiva. È preferibile solo fornire un messaggio di errore utile per spiegare in modo esplicito il problema.
-   **Suggerimento:** Se non si è certi che sia necessario disabilitare un controllo o fornire un messaggio di errore, iniziare componendo il messaggio di errore che si potrebbe assegnare. Se il messaggio di errore contiene informazioni utili che gli utenti di destinazione non possono dedurre rapidamente, lasciare il controllo abilitato e restituire l'errore. In caso contrario, disabilitare il controllo.
-   **Se si disabilita un controllo, disabilitare anche tutti i controlli associati**, ad esempio l'etichetta, le spiegazioni aggiuntive o i pulsanti di comando. Tuttavia, non disabilitare le relative [caselle di gruppo](ctrl-group-boxes.md), l'etichetta di gruppo o la spiegazione del gruppo, se presenti.

![screenshot della finestra di dialogo con controlli in grigio ](images/win-dialog-box-image45.png)

In questo esempio, anche le etichette della casella di testo disabilitate sono disabilitate, ma l'etichetta del gruppo e la spiegazione del gruppo non lo sono.

### <a name="required-input"></a>Input richiesto

-   Per indicare che gli utenti devono fornire informazioni in un controllo, prendere in considerazione le opzioni seguenti:
    -   **Non indicare alcun valore, ma è necessario gestire l'input mancante con i messaggi di errore.** Questo approccio riduce il disordine e funziona bene se la maggior parte degli input è facoltativa o se gli utenti non sono in grado di ignorare i controlli, mantenendo al minimo il numero di messaggi di errore.
    -   **Indica l'input obbligatorio usando un asterisco all'inizio dell'etichetta.** Spiegare l'asterisco usando uno dei seguenti:

        -   Una nota a piè di pagina nella parte inferiore dell'area di contenuto che indica un \* input obbligatorio.
        -   Descrizione comando sull'asterisco che indica l'input richiesto.

        Questo approccio funziona bene se non sono presenti molti controlli necessari, ma è scarso se la maggior parte dei controlli è necessaria.

        ![screenshot delle etichette delle caselle di testo con asterischi ](images/win-dialog-box-image46.png)

        In questo esempio, gli asterischi vengono usati per indicare l'input richiesto.

    -   **Se tutti i controlli richiedono input, dichiarare "tutti gli input necessari" in una posizione appropriata nella parte superiore dell'area di contenuto.** Questo approccio riduce il disordine per questo caso specifico.
    -   **Indica gli input facoltativi con "(facoltativo)" dopo l'etichetta.** Questo approccio funziona bene se la maggior parte degli input è obbligatoria, ma in caso contrario.

-   **Per coerenza, provare a usare lo stesso metodo per indicare l'input necessario per tutto il programma.** In particolare, indicare un input obbligatorio o facoltativo, in base alle esigenze, ma evitare di usare entrambi all'interno dello stesso programma.

### <a name="error-handling"></a>Gestione degli errori

-   Evitare gli errori usando i controlli vincolati all'input utente valido. È anche possibile ridurre il numero di errori fornendo valori predefiniti ragionevoli.
-   Convalidare l'input utente il prima possibile e mostrare gli errori nel modo più appropriato possibile al punto di input.
-   **Usare la gestione degli errori non modale (errori sul posto o palloncini) per i problemi di input dell'utente.**
    -   **Usare i palloni per i problemi di input utente singoli e non critici rilevati in una casella di testo o immediatamente dopo che una casella di testo perde lo stato attivo.** Le mongolfiere non richiedono lo spazio disponibile sullo schermo o il layout dinamico necessario per visualizzare i messaggi sul posto. Visualizzare solo un singolo fumetto alla volta. Poiché il problema non è critico, non è necessaria alcuna icona di errore. Quando si fa clic su un pallone, quando il problema viene risolto o dopo un timeout.

        ![screenshot del messaggio "carattere non corretto" ](images/win-dialog-box-image47.png)

        In questo esempio un fumetto indica un problema di input mentre è ancora nel controllo.

-   **Usare errori sul posto per il rilevamento degli errori ritardati**, in genere errori trovati facendo clic su un pulsante di commit. Non usare errori sul posto per le impostazioni di cui viene immediatamente eseguito il commit. Possono essere presenti più errori sul posto alla volta. Usare il testo normale e un'icona di errore 16x16 pixel, inserendoli direttamente accanto al problema quando possibile. Gli errori sul posto non vengono rilevati a meno che l'utente non venga sottoposto a commit e non vengono rilevati altri errori.

    ![screenshot della finestra di dialogo con due messaggi di errore ](images/win-dialog-box-image48.png)

    In questo esempio viene usato un errore sul posto per un errore rilevato facendo clic sul pulsante commit.

-   **Utilizzare la gestione degli errori modale (finestre di dialogo delle attività o finestre di messaggio) per tutti gli altri problemi,** inclusi errori che coinvolgono più controlli, oppure errori non contestuale o non di input trovati facendo clic su un pulsante di commit.
-   **Quando viene rilevato e segnalato un problema di input, impostare lo stato attivo per l'input sul primo controllo con i dati non corretti.** Se necessario, scorrere il controllo nella visualizzazione.

Per ulteriori informazioni ed esempi, vedere [messaggi di errore](mess-error.md) e [palloncini](ctrl-balloons.md).

### <a name="help"></a>Help

-   Quando si fornisce assistenza agli utenti, tenere presenti le seguenti opzioni (elencate nell'ordine di preferenza):
    -   Assegnare etichette interattive ai controlli. È più probabile che gli utenti leggano le etichette sui controlli interattivi rispetto a qualsiasi altro testo.
    -   Fornire spiegazioni nel contesto usando [etichette di testo statiche](text-ui.md).
    -   Fornire un collegamento alla Guida specifico per un argomento della Guida pertinente.
-   **Individuare i collegamenti della guida nella parte inferiore dell'area del contenuto della finestra di dialogo.** Se nella finestra di dialogo è presente una nota a piè di pagina e il collegamento alla guida è correlato, inserire il collegamento alla guida nella nota.

    ![screenshot della finestra di dialogo con collegamento alla guida ](images/win-dialog-box-image40.png)

    In questo esempio, il collegamento alla guida si applica all'intera finestra di dialogo.

    -   **Eccezione:** Se una finestra di dialogo include diversi gruppi distinti di impostazioni che includono argomenti della guida separati (probabilmente all'interno di caselle di gruppo), individuare i collegamenti della guida nella parte inferiore dei gruppi.

-   **Non usare collegamenti all'argomento della Guida generici o vaghi o pulsanti della Guida generici.** Spesso gli utenti ignorano la guida generica.

Per ulteriori informazioni ed esempi, vedere la [Guida](winenv-help.md)di.

### <a name="default-values"></a>Valori predefiniti

-   Includere un pulsante di commit predefinito in ogni finestra di dialogo.
-   Per le finestre di dialogo della domanda:
    -   **Selezionare il più sicuro (per evitare la perdita di dati o l'accesso al sistema), la risposta più sicura è l'impostazione predefinita.** Se la sicurezza e la sicurezza non sono fattori, selezionare la risposta più probabile o pratica.
        -   **Eccezione:** Non creare una risposta distruttiva per impostazione predefinita, a meno che non esista un modo semplice e ovvio per annullare il comando.
-   Per le finestre di dialogo Choice:
    -   Per i valori predefiniti iniziali, **selezionare il più sicuro (per evitare la perdita di dati o l'accesso al sistema) e la maggior parte dei valori sicuri per ogni controllo.** Se la sicurezza e la sicurezza non sono fattori, selezionare le opzioni più probabili o convenienti.
    -   Per i valori predefiniti successivi, **selezionare nuovamente le opzioni selezionate in precedenza se è probabile che tali valori vengano ripetuti ed è sicuro e sicuro.** In caso contrario, selezionare i valori predefiniti iniziali.

![screenshot della finestra di dialogo Stampa ](images/win-dialog-box-image49.png)

In questo esempio, è più probabile che gli utenti scelgano le stesse impostazioni di stampa dell'ultima volta. Tuttavia, è probabile che il numero di copie desiderate venga modificato, quindi questa impostazione non viene riselezionata.

## <a name="recommended-sizing-and-spacing&quot;></a>Ridimensionamento e spaziatura consigliati

-   **Supporta la risoluzione minima dello schermo di Windows Vista di 800 x 600 pixel.** I layout possono essere ottimizzati per le finestre ridimensionabili con una risoluzione dello schermo di 1024 x 768 pixel.
-   **Usare le finestre ridimensionabili ogni volta che è possibile evitare le barre di scorrimento e i dati troncati.** Windows con contenuto dinamico ed elenchi sfrutta al meglio le finestre ridimensionabili.
-   **Le finestre a dimensione fissa devono essere completamente visibili e dimensionate per adattarsi all'area di lavoro.**
-   **Le finestre ridimensionabili possono essere ottimizzate per risoluzioni più elevate, ma ridimensionate in base alle esigenze in fase di visualizzazione per la risoluzione effettiva dello schermo.**
-   **Scegliere le dimensioni predefinite della finestra appropriate per il relativo contenuto.** Se è possibile utilizzare lo spazio in modo efficiente, non è necessario utilizzare dimensioni della finestra iniziale maggiori.

## <a name=&quot;text&quot;></a>Testo

### <a name=&quot;general&quot;></a>Generale

-   **Rimuovere il testo ridondante.** Cercare il testo ridondante nei titoli, le istruzioni principali, le istruzioni aggiuntive, le aree di contenuto, i collegamenti ai comandi e i pulsanti di commit. In genere, lasciare il testo completo nelle istruzioni e nei controlli interattivi e rimuovere qualsiasi ridondanza dalle altre posizioni.
-   **Usare la formulazione positiva.** La formulazione positiva è più semplice da comprendere per gli utenti.

**Corretto:**

Abilitare la condivisione di file e stampanti?

**Non corretto:**

Disabilitare la condivisione di file e stampanti?

Tuttavia, la formulazione deve corrispondere al comando associato, anche se il comando è con frase negativa. quindi, ad esempio, usare Disable per confermare un comando Disable.

-   **Se necessario, utilizzare la parola &quot;finestra&quot; per fare riferimento alla finestra di dialogo.**
-   **Usare la seconda persona (&quot;u/your") per indicare agli utenti cosa fare** nell'area principale dell'istruzione e del contenuto. Spesso la seconda persona è implicita.

**Esempi:**

Scegliere le immagini che si desidera stampare

Scegliere un account

-   **Usare la prima persona ("I/o/My") per consentire agli utenti di indicare al programma cosa fare** nei controlli nell'area di contenuto che rispondono all'istruzione principale.

**Esempio:** Stampa le foto sulla mia fotocamera.

### <a name="dialog-box-titles"></a>Titoli della finestra di dialogo

-   **Utilizzare il titolo per identificare il comando, la funzionalità o il programma da cui proviene una finestra di dialogo.**
    -   Se la finestra di dialogo viene avviata dall'utente, identificarla usando il nome del comando o della funzionalità. **Eccezioni**
        -   Se una finestra di dialogo viene visualizzata da molti comandi diversi, provare a usare il nome del programma.
        -   Se il titolo è ridondante con l'istruzione principale, usare invece il nome del programma.
    -   Se si tratta di un programma o di un sistema avviato (e di conseguenza non contestuale), identificarlo utilizzando il nome del programma o della funzionalità per fornire il contesto.
    -   Non usare il titolo per spiegare cosa fare nella finestra di dialogo che è lo scopo dell'istruzione principale.
-   Usare il nome di comando esatto per i nomi basati su comandi, ma non includere i puntini di sospensione se ne esiste uno. Se necessario, è possibile includere il titolo del menu del comando per comporre un titolo valido. Esempio: per un oggetto... in un menu Inserisci, usare l'oggetto Insert del titolo.
-   **Se nella barra delle applicazioni viene visualizzata una finestra di dialogo non modale, ottimizzare il titolo per la visualizzazione sulla barra delle applicazioni,** inserendo prima di tutto le informazioni di distinzione. Esempi: "66% completo" e "3 promemoria".
-   **Non includere le parole "Dialog" o "Progress" nel titolo.** Questo è implicito e la sua uscita rende più semplice l'analisi da parte degli utenti.
-   Usare l'uso [di maiuscole in stile titolo](glossary.md)senza la punteggiatura finale.

### <a name="main-instructions"></a>Istruzioni principali

-   **Utilizzare l'istruzione principale per illustrare in modo conciso le operazioni da eseguire nella finestra di dialogo.** L'istruzione deve essere un'istruzione, una direzione imperativa o una domanda specifica. Le istruzioni valide comunicano l'obiettivo dell'utente con la finestra di dialogo piuttosto che concentrarsi esclusivamente sui meccanismi di manipolazione.
-   **Omettere l'istruzione principale quando l'unica cosa che si può dire è ovvia.** In questi casi, il contenuto della finestra di dialogo è di chiara interpretazione. Ad esempio, le finestre di dialogo di apertura e salvataggio file comuni non necessitano di un'istruzione principale, in quanto il contesto e la progettazione ne fanno evidente la loro finalità.
-   **Omettere le etichette dei controlli che riportano l'istruzione principale.** In questo caso, l'istruzione principale accetta il tasto di accesso.

**Accettabile:**

![screenshot della casella di testo con etichetta ridondante ](images/win-dialog-box-image50.png)

In questo esempio, l'etichetta della casella di testo è semplicemente una ripubblicazione dell'istruzione principale.

**Migliore:**

![screenshot della stessa casella di testo con un'etichetta ](images/win-dialog-box-image51.png)

In questo esempio, l'etichetta ridondante viene rimossa, quindi l'istruzione principale accetta il tasto di accesso.

-   **Usare concise solo una singola frase completa.** Riduci l'istruzione principale alle informazioni essenziali. Se è necessario spiegare altre informazioni, utilizzare l'istruzione supplementare.
-   **Quando possibile, usare verbi specifici.** Verbi specifici (esempi: Connetti, Salva, installa) sono più significativi per gli utenti rispetto a quelli generici (esempi: configurazione, gestione, impostazione).
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   **Non includere i periodi finali se l'istruzione è un'istruzione.** Se l'istruzione è una domanda, includere un punto interrogativo finale.
-   **Per le finestre di dialogo dello stato di avanzamento, utilizzare una frase gerundio per spiegare brevemente l'operazione in corso,** terminando con i puntini di sospensione. Esempio: stampa delle immagini in corso...
-   **Suggerimento:** È possibile valutare un'istruzione principale immaginando ciò che si potrebbe dire a un amico. Se la risposta con l'istruzione principale è non naturale, non utile o imbarazzante, rielaborare l'istruzione.

### <a name="supplemental-instructions"></a>Istruzioni supplementari

-   **Quando necessario, utilizzare un'istruzione supplementare facoltativa per presentare informazioni aggiuntive utili per comprendere o utilizzare la pagina.** È possibile fornire informazioni più dettagliate e definire la terminologia.
-   **Se l'aspetto della finestra di dialogo è programma o avviato dal sistema (e di conseguenza non contestuale), utilizzare l'istruzione supplementare per spiegare il motivo per cui è stata visualizzata la finestra di dialogo.** Per tali finestre di dialogo, il contesto non è in genere ovvio.
-   **Non ripetere l'istruzione principale con una formulazione leggermente diversa.** Omettere invece l'istruzione supplementare se non è più necessario aggiungere.
-   Usare frasi complete, maiuscole e minuscole in stile frase e punteggiatura finale.

### <a name="command-links"></a>Collegamenti ai comandi

-   **Scegliere testo conciso collegamento che comunica chiaramente e distingue il collegamento del comando.** Dovrebbe essere di chiara comprensione e corrispondere all'istruzione principale. Gli utenti non devono necessariamente determinare il significato del collegamento o la differenza rispetto ad altri collegamenti.
-   **Avviare sempre i collegamenti del comando con un verbo.**
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Non usare punteggiatura finale.
-   **Se necessario, fornire altre spiegazioni usando le frasi complete e la punteggiatura finale.** Tuttavia, aggiungere queste spiegazioni solo quando necessario non aggiungere spiegazioni a tutti i collegamenti ai comandi solo perché è necessario un solo collegamento al comando.

Per ulteriori informazioni ed esempi, vedere linee guida sui [collegamenti di comando](ctrl-command-links.md) .

### <a name="commit-buttons"></a>Pulsanti di commit

-   **Usare etichette di pulsanti di commit specifiche che hanno un significato autonomo e sono una risposta all'istruzione principale.** Idealmente, gli utenti non devono leggere nient'altro per comprendere l'etichetta. È molto più probabile che gli utenti leggano le etichette dei pulsanti di comando rispetto al testo statico.
-   **Avviare le etichette dei pulsanti di commit con un verbo. Le eccezioni sono OK, sì e no.**
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Non usare punteggiatura finale.
-   Assegnare una [chiave di accesso](glossary.md)univoca.
    -   **Eccezione:** Non assegnare chiavi di accesso ai pulsanti OK e Annulla perché le chiavi di accesso sono Enter e ESC. In questo modo le altre chiavi di accesso risultano più semplici da assegnare.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle finestre di dialogo:

-   In programmazione e altri documenti tecnici, fare riferimento alle finestre di dialogo come finestre di dialogo. In tutti gli altri casi, fare riferimento alle finestre di dialogo in base al titolo. Se la barra del titolo è nascosta, fare riferimento alla finestra di dialogo usando l'istruzione principale.
-   Se è necessario fare riferimento a una finestra di dialogo in generale, utilizzare la finestra nella documentazione dell'utente. È possibile fare riferimento a una semplice finestra di dialogo o a una conferma come messaggio.
-   Usare il testo esatto del titolo o dell'istruzione principale, inclusa la relativa maiuscola.
-   Quando possibile, formattare il titolo usando il testo in grassetto. In caso contrario, inserire il titolo racchiuso tra virgolette solo se necessario per evitare confusione.

Esempio: in **sicurezza di Windows** fare clic su **altre opzioni**.

