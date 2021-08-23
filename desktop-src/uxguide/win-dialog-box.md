---
title: Finestre di dialogo (nozioni di base sulla progettazione)
description: Una finestra di dialogo è una finestra secondaria che consente agli utenti di eseguire un comando, porre una domanda o fornire agli utenti informazioni o commenti sullo stato di avanzamento.
ms.assetid: 2ded9f30-d45f-4027-a85d-4e7d0e412793
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2fe9b7545961f7e06b1edf1656531779d5122b339d0cf16294e5ef5c4be9a69f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031164"
---
# <a name="dialog-boxes-design-basics"></a>Finestre di dialogo (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Una finestra di dialogo è una finestra secondaria che consente agli utenti di eseguire un comando, porre una domanda o fornire agli utenti informazioni o commenti sullo stato di avanzamento.

![Screenshot che identifica gli elementi della finestra di dialogo ](images/win-dialog-box-image1.png)

Finestra di dialogo tipica.

Le finestre di dialogo sono costituite da una barra del titolo (per identificare il comando, la funzionalità o il programma da cui proveniva una finestra di dialogo), un'istruzione principale facoltativa (per spiegare l'obiettivo dell'utente con la finestra di dialogo), vari controlli nell'area del contenuto (per presentare le opzioni) e pulsanti di commit (per indicare come l'utente vuole eseguire il commit nell'attività).

Le finestre di dialogo hanno due tipi fondamentali:

-   **Le finestre di dialogo modali** richiedono agli utenti di completare e chiudere prima di continuare con la finestra proprietaria. Queste finestre di dialogo sono più usate per attività critiche o poco frequenti che richiedono il completamento prima di continuare.
-   **Le finestre di dialogo non modali** consentono agli utenti di passare dalla finestra di dialogo alla finestra proprietaria in base alle esigenze. Queste finestre di dialogo sono più usate per attività frequenti, ripetitive e in corso.

**Una finestra di dialogo attività è una finestra di dialogo implementata tramite l'API (Application Programming Interface) della finestra di dialogo attività.** Sono costituite da parti seguenti, che possono essere assemblate in un'ampia gamma di combinazioni:

-   Barra **del titolo per** identificare l'applicazione o la funzionalità di sistema da cui proveniva la finestra di dialogo.
-   Istruzione **principale,** con un'icona facoltativa, per identificare l'obiettivo dell'utente con la finestra di dialogo.
-   Area **di contenuto per** informazioni descrittive e controlli.
-   **Un'area dei** comandi per i pulsanti di commit, tra cui un pulsante Annulla, e le opzioni Facoltative Altre opzioni e Non visualizzare questa opzione <item> controlla di nuovo.
-   Area **delle note a piè di** pagina per spiegazioni e informazioni aggiuntive facoltative, in genere destinate a utenti meno esperti.

![Screenshot di una tipica finestra di dialogo attività ](images/win-dialog-box-image2.png)

Una tipica finestra di dialogo di attività.

**I dialoghe attività sono consigliati ogni volta che sono appropriati perché sono facili da creare e hanno un aspetto coerente.** I dialoghe attività richiedono Windows Vista o versioni successive, quindi non sono adatti per le versioni precedenti di Microsoft Windows.

Un riquadro attività è simile a una finestra di dialogo, ad eccezione del fatto che viene presentato all'interno di un riquadro della finestra anziché in una finestra separata. Di conseguenza, i riquadri attività hanno un aspetto più diretto e contestuale rispetto alle finestre di dialogo. Anche se tecnicamente non sono uguali, i riquadri attività sono così simili alle finestre di dialogo che le linee guida sono presentate **in questo articolo.**

![Screenshot di un tipico riquadro attività ](images/win-dialog-box-image3.png)

Riquadro attività tipico.

[Le finestre delle](win-property-win.md) proprietà sono un tipo specializzato di finestra di dialogo usata per visualizzare e modificare le proprietà per un oggetto, una raccolta di oggetti o un programma. Inoltre, le finestre delle proprietà supportano in genere diverse attività, mentre le finestre di dialogo in genere supportano una singola attività o passaggio in un'attività. Poiché il loro utilizzo è specializzato, **le finestre delle proprietà sono coperte da un set diverso di linee guida.**

Le finestre di dialogo possono [avere schede](ctrl-tabs.md)e, in tal caso, sono denominate finestre di dialogo a schede. Le finestre delle proprietà sono determinate dalla presentazione delle proprietà, non dall'uso delle schede.

**Nota:** Le linee guida relative [](mess-warn.md) al [layout,](vis-layout.md)alla gestione delle finestre, alle finestre di dialogo comuni, alle finestre delle proprietà, alle procedure guidate, alle conferme, ai messaggi di errore e ai messaggi di avviso vengono presentate in articoli separati. [](win-window-mgt.md) [](win-property-win.md) [](win-wizards.md) [](mess-confirm.md) [](mess-error.md)

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere, prendi in considerazione queste domande:

-   **Lo scopo è fornire agli utenti informazioni, porre una domanda agli utenti o consentire agli utenti di selezionare le opzioni per eseguire un comando o un'attività?** In caso contrario, usare un'altra interfaccia utente.
-   **Lo scopo è visualizzare e modificare le proprietà di un oggetto, di una raccolta di oggetti o di un programma?** In caso contrario, usare una [finestra delle proprietà o](win-property-win.md) una barra [degli](cmd-toolbars.md) strumenti.
-   **Lo scopo è presentare una raccolta di comandi o strumenti?** In tal caso, usare una barra degli strumenti o [una finestra del riquadro.](glossary.md)
-   **Lo scopo è verificare che l'utente voglia procedere con un'azione?** C'è un motivo chiaro per non procedere e una ragionevole probabilità che a volte gli utenti non lo siano? In tal caso, usare una [conferma](mess-confirm.md).
-   **Lo scopo è fornire un messaggio di errore o di avviso?** In tal caso, usare un [messaggio di errore o](mess-error.md) un messaggio di [avviso](mess-warn.md).
-   Lo scopo è:
    -   Aprire i file
    -   Salvare i file
    -   Aprire cartelle
    -   Trovare o sostituire testo
    -   Stampare un documento
    -   Selezionare gli attributi di una pagina stampata
    -   Selezionare un tipo di carattere
    -   Scegliere un colore
    -   Cercare un file, una cartella, un computer o una stampante
    -   Cercare utenti, computer o gruppi in Microsoft Active Directory
    -   Richiedere un nome utente e una password?

In tal caso, usare la finestra di [dialogo comune](win-common-dlg.md) appropriata. Molti di questi dialoghe comuni sono estendibili.

-   **Lo scopo è eseguire un'attività in più passaggi che richiede più di una singola finestra?** In tal caso, usare invece [un flusso di attività](glossary.md) o una [procedura](win-wizards.md) guidata.
-   **Lo scopo è informare gli utenti di un evento di sistema o di programma non correlato all'attività utente corrente, che non richiede un'azione immediata dell'utente e gli utenti possono ignorare liberamente?** In caso contrario, usare [una notifica.](mess-notif.md)
-   **Lo scopo è mostrare lo stato del programma?** In caso contrario, usare una [barra di](ctrl-status-bars.md) stato.
-   **È preferibile usare l'interfaccia utente sul posto?** Le finestre di dialogo possono interrompere il flusso dell'utente richiedendo attenzione. A volte tale interruzione nel flusso è giustificata, ad esempio quando l'utente deve eseguire un'azione esterna al contesto corrente. In altri casi, un approccio migliore consiste nel presentare l'interfaccia utente nel contesto, direttamente con l'interfaccia utente sul posto (ad esempio un riquadro attività) o su richiesta usando la diffusione [progressiva.](ctrl-progressive-disclosure-controls.md)
-   **Lo scopo è visualizzare un problema di input utente non critico o una condizione speciale?** In caso contrario, usare un [fumetto.](ctrl-balloons.md)
-   **Per i flussi di attività, è preferibile usare un'altra pagina?** In genere si vuole che un'attività scorrono da una pagina all'altro all'interno di una singola finestra. Usare le finestre di dialogo per confermare i comandi sul posto, ottenere l'input per i comandi sul posto ed eseguire attività secondarie autonome che vengono eseguite in modo indipendente e all'esterno del flusso di attività principale.
-   **Per la selezione delle opzioni, è probabile che gli utenti cambino le opzioni?** In caso contrario, prendere in considerazione alternative, ad esempio:
    -   Uso delle opzioni predefinite senza chiedere, ma consentendo agli utenti di apportare modifiche in un secondo momento.
    -   Fornire una versione con opzioni (ad esempio, **Stampa...** in un menu) e una versione senza opzioni (ad esempio, **Stampa** sulla barra degli strumenti). In genere, i comandi della barra degli strumenti devono essere immediati ed evitare la visualizzazione di finestre di dialogo.
-   **Per la selezione delle opzioni, esiste un modo più semplice e diretto per presentare le opzioni?** In tal caso, prendere in considerazione alternative, ad esempio:
    -   Uso di [un pulsante di divisione](ctrl-command-buttons.md) per selezionare le varianti di un comando.
    -   Uso di un sottomenu per comandi, caselle di controllo, pulsanti di opzione ed elenchi semplici.

![Screenshot che mostra un menu e un sottomenu.](images/win-dialog-box-image4.png)

![Screenshot di un menu e di un sottomenu ](images/win-dialog-box-image5.png)

In questi esempi vengono usati sottomenu anziché finestre di dialogo per selezioni semplici.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Se usate correttamente, le finestre di dialogo sono un ottimo modo per offrire potenza e flessibilità al programma. In caso di uso improprio, le finestre di dialogo sono un modo semplice per infastidire gli utenti, interrompere il flusso e rendere il programma indiretto e noioso da usare. **Le finestre di dialogo modali richiedono l'attenzione degli utenti.** Le finestre di dialogo sono spesso più facili da implementare rispetto a quelle alternative, quindi tendono a essere sovrautilizzate.

**Una finestra di dialogo è più efficace quando le caratteristiche di progettazione corrispondono al relativo utilizzo.** La progettazione di una finestra di dialogo è in gran parte determinata dallo scopo (offrire opzioni, porre domande, fornire informazioni o commenti), digitare (modale o non modale) e l'interazione dell'utente (richiesta, risposta facoltativa o riconoscimento), mentre il relativo utilizzo è in gran parte determinato dal contesto (avviato dall'utente o dal programma), dalla probabilità di azione dell'utente e dalla frequenza di visualizzazione.

Per progettare finestre di dialogo efficaci, usare in modo efficace gli elementi seguenti:

-   Testo della finestra di dialogo
-   Istruzioni principali
-   Non visualizzare questo <item> opzione again

**Se si fa una sola cosa...**

Assicurarsi che la progettazione della finestra di dialogo (determinata dallo scopo, dal tipo e dall'interazione dell'utente) corrisponda all'utilizzo (determinato dal contesto, dalla probabilità di azione dell'utente e dalla frequenza di visualizzazione).

## <a name="usage-patterns"></a>Modelli di utilizzo

Le finestre di dialogo hanno diversi modelli di utilizzo:

-   Le finestre di dialogo delle domande (con i pulsanti) porre agli utenti una singola domanda o confermare un comando e usare risposte semplici in pulsanti di comando disposti orizzontalmente.
-   Le finestre di dialogo delle domande (con collegamenti di comando) poneno agli utenti una singola domanda o selezionano un'attività da eseguire e usano risposte dettagliate in collegamenti di comando disposti verticalmente.
-   Le finestre di dialogo di scelta presentano agli utenti un set di scelte, in genere per specificare un comando in modo più completo. A differenza dei dialoghe di domande, i dialoghe di scelta possono porre più domande.
-   Le finestre di dialogo di stato presentano agli utenti un feedback sullo stato di avanzamento durante un'operazione di lunga durata (più di cinque secondi), insieme a un comando per annullare o arrestare l'operazione.
-   Le finestre di dialogo in formato informativo visualizzano le informazioni richieste dall'utente.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Non usare finestre di dialogo scorrevoli.** Non usare finestre di dialogo che richiedono l'uso di una barra di scorrimento per essere visualizzate completamente durante il normale utilizzo. Riprogettare la finestra di dialogo. È consigliabile usare [la diffusione progressiva](ctrl-progressive-disclosure-controls.md) o [le schede](ctrl-tabs.md).
-   **Non avere una barra dei menu o una barra di stato.** Fornire invece l'accesso ai comandi e allo stato direttamente nella finestra di dialogo stessa o usando i menu di scelta rapida nei controlli pertinenti.

    -   **Eccezione:** Le barre dei menu sono accettabili quando si usa una finestra di dialogo per implementare una finestra primaria, ad esempio un'utilità .

    **Non corretto:**

    ![Screenshot di una finestra di dialogo con una barra dei menu ](images/win-dialog-box-image6.png)

    In questo esempio Trova certificati è una finestra di dialogo non modabile con una barra dei menu.

-   Se una finestra di dialogo richiede attenzione immediata e il programma non è attivo, eseguire il flash del pulsante della barra delle applicazioni tre volte per attirare l'attenzione e **lasciarlo evidenziato.** Non eseguire altre operazioni: non ripristinare o attivare la finestra e non riprodurre alcun effetto sonoro. Al contrario, rispettare la selezione dello stato della finestra dell'utente e consentire all'utente di attivare la finestra quando è pronto.
-   Per altre linee guida ed esempi, vedere Barra [delle applicazioni.](winenv-taskbar.md)

### <a name="modal-dialog-boxes"></a>Finestre di dialogo modali

-   **Usare per le attività critiche o non frequenti che richiedono il completamento prima di continuare.**
-   Usare un modello [di commit ritardato in](glossary.md) modo che le modifiche non vengono applicate fino a quando non viene eseguito il commit in modo esplicito.
-   **Implementare usando una finestra di dialogo attività ogni volta che è appropriato per ottenere un aspetto coerente.** Le finestre di dialogo attività Windows Vista o versioni successive, quindi non sono adatte per le versioni precedenti di Windows.

### <a name="modeless-dialog-boxes"></a>Finestre di dialogo non modali

-   **Usare per attività frequenti, ripetitive e in corso.**
-   Usare un [modello di commit immediato in](glossary.md) modo che le modifiche si apportare immediatamente.
-   Per le finestre di dialogo non modali, usare un pulsante di comando Chiudi esplicito nella finestra di dialogo per chiudere la finestra. Per entrambi, usare un pulsante Chiudi sulla barra del titolo per chiudere la finestra.
-   **È consigliabile rendere ancorabili le finestre di dialogo non modali.** Le finestre di dialogo non modali ancorabili consentono un posizionamento più flessibile.

![Screenshot di una finestra di dialogo ancorabile e non modale ](images/win-dialog-box-image7.png)

Alcune finestre di dialogo non modali usate in Microsoft Office sono ancorabili.

### <a name="multiple-dialog-boxes"></a>Più finestre di dialogo

-   **Non visualizzare più di una finestra di dialogo di scelta di proprietà alla volta da una finestra di dialogo di scelta del proprietario.** La visualizzazione di più pulsanti rende difficile per gli utenti comprendere il significato dei pulsanti di commit. È possibile visualizzare altri tipi di finestre di dialogo, ad esempio le finestre di dialogo delle domande, in base alle esigenze.
-   **Per una sequenza di finestre di dialogo correlate, è consigliabile usare un dialogo a più pagine, se possibile.** Usare singoli dialoghe se non sono chiaramente correlati.

### <a name="multi-page-dialog-boxes"></a>Finestre di dialogo a più pagine

-   Usare una finestra di dialogo a più pagine anziché singole finestre di dialogo quando si dispone della sequenza di pagine correlate seguente:
    -   Una singola pagina di input (facoltativa)
    -   Pagina di stato
    -   Una singola pagina dei risultati

La pagina di input è facoltativa perché l'attività potrebbe essere stata avviata in un'altra posizione. **In questo modo, l'esperienza risultante ha un aspetto stabile, semplice e leggero.**

![Screenshot di un indicatore di stato ](images/win-dialog-box-image8.png)

![Screenshot del messaggio "Nessun problema trovato" ](images/win-dialog-box-image9.png)

In questo esempio, Windows diagnostica di rete è costituito da pagine di stato e risultati.

-   **Non usare una finestra di dialogo a più pagine se la pagina di input è una finestra di dialogo standard.** In questo caso è più importante la coerenza dell'uso di un dialogo standard.
-   **Non usare i pulsanti Avanti o Indietro e non hanno più di tre pagine.** Le finestre di dialogo a più pagine sono per le attività in un singolo passaggio con commenti e suggerimenti. Non sono procedure [guidate,](win-wizards.md)che vengono usate per le attività in più passaggi. Le procedure guidate hanno un aspetto molto intenso e indiretto rispetto alle finestre di dialogo a più pagine.
-   **Nella pagina di input usare pulsanti di comando o collegamenti di comando specifici per avviare l'attività.**
-   **Usare un pulsante Annulla nelle pagine di input e di stato e un pulsante Chiudi nella pagina dei risultati.**

**Sviluppatori:** È possibile creare finestre di dialogo di attività a più pagine usando il [messaggio \_ TDM NAVIGATE \_ PAGE.](../controls/tdm-navigate-page.md)

### <a name="presentation"></a>Presentazione

Per semplificare l'individuazione e l'accesso delle finestre di dialogo, associare chiaramente il dialogo all'origine e usare correttamente più monitor:

-   **Visualizzare inizialmente le finestre di dialogo "centrate" nella parte superiore della finestra del proprietario.** Per la visualizzazione successiva, è consigliabile visualizzarla nell'ultima posizione (relativa alla finestra del proprietario) se questa operazione è probabilmente più pratica.

![Diagramma della finestra di dialogo centrata sulla finestra dietro di essa ](images/win-dialog-box-image10.png)

Centrare inizialmente le finestre di dialogo nella parte superiore della finestra proprietaria.

-   **Se un dialogo è contestuale, visualizzarlo accanto all'oggetto da cui è stato avviato.** Tuttavia, posizionarlo fuori dal modo (preferibilmente scostamento verso il basso e verso destra) in modo che l'oggetto non sia coperto dal dialogo.

![Diagramma dell'offset della finestra di dialogo verso il basso e verso destra ](images/win-dialog-box-image11.png)

Le proprietà di un oggetto vengono visualizzate accanto all'oggetto .

-   **Per le finestre di dialogo non modali, la visualizzazione viene inizialmente visualizzata sopra la finestra del proprietario per semplificarne l'individuazione.** Se l'utente attiva la finestra proprietaria, il dialogo non modali potrebbe essere nascosto.
-   **Se necessario, modificare la posizione iniziale in modo che l'intero dialogo sia visibile all'interno del monitor di destinazione.** Se una finestra ridimensionabile è più grande del monitor di destinazione, ridurla per adattarla.
-   **Quando una finestra di dialogo viene visualizzata nuovamente, è consigliabile visualizzarla nello stesso stato dell'ultimo accesso.** Alla chiusura, salvare il monitoraggio usato, le dimensioni della finestra, la posizione e lo stato (ingrandito o ripristinato). Quando viene visualizzato nuovamente, ripristinare le dimensioni, la posizione e lo stato della finestra di dialogo salvati usando il monitoraggio appropriato. Valutare anche la possibilità di rendere questi attributi persistenti tra le istanze del programma per singolo utente.
-   **Per le finestre ridimensionabili, impostare una dimensione minima della finestra se è presente una dimensione inferiore alla quale il contenuto non è più utilizzabile.** Valutare la possibilità di modificare la presentazione per rendere il contenuto utilizzabile in dimensioni più piccole.

![Screenshot dei pulsanti del lettore multimediale centrato ](images/win-dialog-box-image12.png)

In questo esempio, Windows Media Player modifica il formato quando la finestra diventa troppo piccola per il formato standard.

-   **Non usare l'attributo Always On Top.**
    -   **Eccezione:** Usare solo quando una finestra di dialogo implementa un'operazione essenzialmente modale, ma deve essere sospesa brevemente per accedere alla finestra proprietaria. Ad esempio, quando si esegue il controllo ortografico di un documento, gli utenti possono occasionalmente lasciare la finestra di dialogo di controllo ortografico e accedere al documento per correggere gli errori.

Per altre informazioni ed esempi, vedere [Gestione delle finestre.](win-window-mgt.md)

### <a name="title-bars"></a>Barre del titolo

-   **Le finestre di dialogo non hanno icone della barra del titolo.** Le icone della barra del titolo vengono usate come distinzione visiva tra [le finestre primarie e](glossary.md) le finestre [secondarie.](glossary.md)
    -   **Eccezione:** Se una finestra di dialogo viene usata per implementare una finestra primaria (ad esempio un'utilità ) e pertanto viene visualizzata sulla barra delle applicazioni, ha un'icona della barra del titolo. In questo caso, ottimizzare il titolo per la visualizzazione sulla barra delle applicazioni inserendo concisamente le informazioni distintive.
-   **Le finestre di dialogo hanno sempre un pulsante Chiudi.** Le finestre di dialogo non modali possono anche avere un pulsante Riduci a icona. Le finestre di dialogo ridimensionabili possono avere un pulsante Ingrandisci.
-   **Non disabilitare il pulsante Chiudi.** La presenza di un pulsante Chiudi consente agli utenti di mantenere il controllo consentendo loro di chiudere le finestre che non vogliono.
    -   **Eccezione:** Per le finestre di dialogo di stato, è possibile disabilitare il pulsante Chiudi se l'attività deve essere eseguita fino al completamento per ottenere uno stato valido o impedire la perdita di dati.
-   **Il pulsante Chiudi sulla barra del titolo dovrebbe avere lo stesso** effetto del pulsante Annulla o Chiudi nella finestra di dialogo. Non assegnargli mai lo stesso effetto di OK.
-   Se la didascalia e l'icona della barra del titolo sono già visualizzate in modo prominente nella parte superiore della finestra, è possibile nascondere la didascalia e l'icona della barra del titolo per evitare ridondanza. Tuttavia, è comunque necessario impostare internamente un titolo appropriato per l'uso da parte di Windows.

### <a name="interaction"></a>Interazione

-   **Quando vengono visualizzate, le finestre di dialogo avviate dall'utente devono sempre assumere lo stato attivo per l'input.** Le finestre di dialogo avviate dal programma non devono assumere lo stato attivo per l'input perché l'utente potrebbe interagire con un'altra finestra. Tale interazione non indiretta nella finestra di dialogo può avere conseguenze impreviste.
-   **Assegnare lo stato attivo per l'input** iniziale al controllo con cui è più probabile che gli utenti interagiscano con first , che in genere è (ma non sempre) il primo controllo interattivo. Evitare di assegnare lo stato attivo di input iniziale a un collegamento alla Guida.
-   **Per la navigazione tramite tastiera, l'ordine di tabulazione deve essere in ordine logico, in genere da sinistra a destra, dall'alto verso il basso.** In genere l'ordine di tabulazione segue l'ordine di lettura, ma è consigliabile effettuare queste eccezioni:

    -   Inserire i controlli usati più di frequente in precedenza nell'ordine di tabulazione.
    -   Inserire i collegamenti della Guida nella parte inferiore di una finestra di dialogo, dopo i pulsanti di commit nell'ordine di tabulazione.

    Quando si assegna l'ordine, si supponga che gli utenti visualizzano le finestre di dialogo per lo scopo previsto; pertanto, ad esempio, gli utenti visualizzano le finestre di dialogo di scelta per effettuare scelte, non per esaminare e fare clic su Annulla.

-   **Premendo ESC viene sempre chiusa una finestra di dialogo attiva.** Questo vale per le finestre di dialogo con Cancel o Close e anche se Cancel è stato rinominato in Close perché i risultati non possono più essere annullati.

**Chiavi di accesso**

-   **Quando possibile, assegnare chiavi di accesso univoche a tutti i controlli interattivi o alle relative etichette.** [Le caselle di testo di sola](ctrl-text-boxes.md) lettura sono controlli interattivi (perché gli utenti possono scorrerle e copiare testo) in modo che possano trarre vantaggio dai tasti di scelta. **Non assegnare chiavi di accesso a:**
    -   **Pulsanti OK, Annulla e Chiudi.** I tasti INVIO e ESC vengono usati per le chiavi di accesso. Tuttavia, assegnare sempre un tasto di scelta a un controllo che indica OK o Annulla, ma con un'etichetta diversa.

        ![Screenshot della finestra di dialogo Elimina file ](images/win-dialog-box-image13.png)

        In questo esempio, al pulsante commit positivo è assegnata una chiave di accesso.

    -   **Raggruppare le etichette.** In genere, ai singoli controlli all'interno di un gruppo vengono assegnate chiavi di accesso, quindi l'etichetta del gruppo non ne richiede una. Tuttavia, in caso di mancanza di chiavi di accesso, assegnare una chiave di accesso all'etichetta del gruppo e non ai singoli controlli.
    -   **Pulsanti della Guida generica,** a cui si accede con F1.
    -   **Collegare le etichette.** Spesso sono presenti troppi collegamenti per assegnare chiavi di accesso univoche e i caratteri di sottolineatura spesso usati per indicare i collegamenti nascondono i caratteri di sottolineatura dei tasti di scelta. Accedere invece ai collegamenti con il tasto TAB.
    -   **Nomi delle schede.** Le schede vengono visualizzate in ciclo usando CTRL+TAB e CTRL+MAIUSC+TAB.
    -   **Pulsanti di esplorazione con etichetta "...".** Questi pulsanti Sfoglia non possono essere assegnati in modo univoco alle chiavi di accesso.
    -   **Controlli senza etichetta, ad** esempio controlli di selezione, pulsanti di comando grafici e controlli di divulgazione progressiva senza etichetta.
    -   **Testo statico non etichettato o etichette per i controlli non interattivi,** ad esempio le barre di stato.

-   **Quando possibile, assegnare le chiavi di accesso per i comandi di uso comune in base alle Assegnazioni di tasti di accesso standard**. Anche se le assegnazioni coerenti dei tasti di scelta non sono sempre possibili, sono sicuramente preferibili soprattutto per le finestre di dialogo usate di frequente.
-   **Assegnare prima le chiavi di accesso ai pulsanti di commit per assicurarsi che siano assegnate alle chiavi standard.** Se non è presente un'assegnazione di chiave standard, usare la prima lettera della prima parola. Ad esempio, il tasto di scelta per i pulsanti Sì e No commit deve essere sempre "Y" e "N", indipendentemente dagli altri controlli nella finestra di dialogo.
-   **Per semplificare** l'individuazione dei tasti di scelta, assegnare i tasti di scelta a un carattere visualizzato all'inizio dell'etichetta, idealmente il primo carattere, anche se è presente una parola chiave che viene visualizzata più avanti nell'etichetta.
-   **Preferisce caratteri con larghezze ampie,** ad esempio w, m e lettere maiuscole.
-   **Preferire una consonante distintiva o una vocale,** ad esempio "x" in Exit.
-   **Evitare di usare caratteri che rendono difficile la sottolineatura,** ad esempio (dal più problematico al meno problematico):
    -   Lettere di larghezza di un solo pixel, ad esempio i e l.
    -   Lettere con discendenti, ad esempio g, j, p, q e y.
    -   Lettere accanto a una lettera con un discendente.

Per altre linee guida ed esempi, vedere [Tastiera](inter-keyboard.md).

### <a name="progress-dialogs"></a>Finestre di dialogo di stato

Per le attività con esecuzione lunga, si supponga che **gli utenti eseereranno altre operazioni mentre l'attività sta completando**. Progettare l'attività per l'esecuzione automatica.

-   **Presentare agli utenti la finestra di dialogo** feedback sullo stato se un'operazione richiede più di cinque secondi per il completamento, insieme a un comando per annullare o arrestare l'operazione.
    -   **Eccezione:** Per le procedure guidate e i flussi di attività, usare una finestra di dialogo modale per lo stato di avanzamento solo se l'attività rimane nella stessa pagina (anziché passare a un'altra pagina) e gli utenti non possono eseguire operazioni durante l'attesa. In caso contrario, usare una pagina di stato o lo stato sul posto.
-   Se l'operazione è un'attività a esecuzione lunga (oltre 30 secondi) e può essere eseguita in background, usare una finestra di dialogo di stato non modabile in modo che gli utenti possano continuare a usare il programma durante l'attesa.
-   Finestre di dialogo di stato non modali:
    -   Fare clic sul pulsante Riduci a icona sulla barra del titolo.
    -   Vengono visualizzati sulla barra delle applicazioni.
-   Implementare le finestre di dialogo di stato non modali in modo che continuino a essere eseguite anche se la finestra del proprietario è chiusa.

![Screenshot della finestra di dialogo copia con l'indicatore di stato ](images/win-dialog-box-image14.png)

In questo esempio la copia del file continua anche se la finestra del proprietario è chiusa.

-   **Fornire un pulsante di comando per arrestare l'operazione se il completamento richiede più di pochi secondi o può non essere mai completato.** Etichettare il pulsante Annulla se l'annullamento riporta l'ambiente allo stato precedente (senza effetti collaterali); In caso contrario, etichettare il pulsante Arresta per indicare che l'operazione parzialmente completata rimane invariata. È possibile modificare l'etichetta del pulsante da Annulla a Arresta nel mezzo dell'operazione, se a un certo punto non è possibile ripristinare lo stato precedente dell'ambiente.

![Screenshot della finestra di dialogo con il pulsante Annulla ](images/win-dialog-box-image15.png)

In questo esempio, l'arresto della diagnosi del problema non ha alcun effetto collaterale.

-   **Fornire un pulsante di comando per sospendere l'operazione se il completamento richiede più di alcuni minuti e compromettere la capacità degli utenti di eseguire il lavoro.** Questa operazione non forza l'utente a scegliere tra il completamento dell'attività e l'esecuzione del lavoro.
-   **Raccogliere tutte le informazioni che è possibile prima di avviare l'attività.**
-   **Se vengono rilevati problemi ripristinabili, fare in modo che gli utenti si occupino di tutti i problemi rilevati alla fine dell'attività.** Se questo non è pratico, fare in modo che gli utenti si occupino dei problemi non appena si verificano.
-   **Non abbandonare le attività in seguito a errori ripristinabili.**

![Screenshot della finestra di dialogo con il pulsante Riprova ](images/win-dialog-box-image16.png)

In questo esempio, Windows Explorer consente agli utenti di continuare con l'attività dopo un errore ripristinabile.

-   **Indicare i problemi attivando l'indicatore di stato in rosso.**

![screenshot dell'indicatore di stato e riprovare ](images/win-dialog-box-image17.png)

In questo esempio un disco rimovibile è stato rimosso durante una copia di file.

-   **Se i risultati sono chiaramente evidenti per gli utenti, chiudere automaticamente la finestra di dialogo di stato al completamento.** In caso contrario, usare il feedback solo per segnalare i problemi:
    -   Per visualizzare commenti e suggerimenti semplici, visualizzare il feedback nella finestra di dialogo di stato e modificare il pulsante Annulla in Chiudi.
    -   Per visualizzare commenti e suggerimenti dettagliati, chiudere la finestra di dialogo di stato e visualizzare una finestra di dialogo informativo.

**Non usare una notifica per il feedback sul completamento.** Usare una finestra di dialogo di stato o una [notifica di operazione riuscita,](mess-notif.md)ma non entrambe.

**Tempo rimanente**

-   **Usare i formati di ora seguenti.** Iniziare con il primo dei formati seguenti in cui l'unità di tempo più grande non è zero, quindi passare al formato successivo quando l'unità di tempo più grande diventa zero.

**Per le barre di stato:**

**Se le informazioni correlate vengono visualizzate in formato due punti:**

Tempo rimanente: ore h, m minuti

Tempo rimanente: m minuti, s secondi

Tempo rimanente: s secondi

**Se lo spazio sullo schermo è premium:**

h hrs, m min rimanenti

m mins, s secs remaining

s secondi rimanenti

**In caso contrario:**

ore h, m minuti rimanenti

m minuti, s secondi rimanenti

s secondi rimanenti

**Per le barre del titolo:**

hh:mm rimanente

mm:ss remaining

0:ss rimanenti

Questo formato compatto mostra prima le informazioni più importanti in modo che non sia troncato sulla barra delle applicazioni.

-   **Fare in modo che le stime siano accurate, ma non fornire false precisione.** Se l'unità più grande è di ore, assegnare minuti (se significativi) ma non secondi.

**Non corretto:**

hh hours, mm minutes, ss seconds

-   **Mantenere aggiornata la stima.** Aggiornare le stime del tempo rimanente almeno ogni 5 secondi.
-   **Concentrarsi sul tempo rimanente** perché si tratta delle informazioni più importanti per gli utenti. Assegnare il tempo trascorso totale solo in alcuni scenari in cui il tempo trascorso è utile, ad esempio quando è probabile che l'attività sia ripetuta. Se la stima del tempo rimanente è associata a un indicatore di stato, non avere il testo completo della percentuale perché queste informazioni vengono trasmesse dall'indicatore di stato stesso.
-   **Essere grammaticalmente corretti.** Usare unità singolari quando il numero è uno.

**Non corretto:**

1 minuto, 1 secondo

-   **Usare le maiuscole/minuscole come nelle frasi comuni.**

Per altre informazioni ed esempi, vedere [ProgressBars](progress-bars.md).

### <a name="icons-and-graphics"></a>Icone e grafica

**Grafica**

-   **Non usare grafica di grandi dimensioni che non ha alcuno scopo oltre a riempire lo spazio con gli occhi.** In alternativa, mantenere l'aspetto semplice.

**Non corretto:**

![Screenshot della finestra di dialogo con un elemento grafico di grandi dimensioni ](images/win-dialog-box-image18.png)

In questo esempio, l'immagine di grandi dimensioni non ha alcun scopo.

**Icone della barra del titolo**

-   **Le finestre di dialogo non hanno icone della barra del titolo.**
    -   **Eccezione:** Se una finestra di dialogo viene usata per implementare una finestra primaria (ad esempio un'utilità ) e pertanto viene visualizzata sulla barra delle applicazioni, ha un'icona della barra del titolo.

**Icone del corpo**

-   **Scegliere l'icona del corpo in base al modello di progettazione:**



| Modello | Icona Corpo |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| **Dialoghe di domande**<br/>      | Programma, funzionalità, oggetto, icona di avviso (in caso di potenziale perdita di dati o accesso al sistema), avviso di sicurezza o nessuno.<br/> |
| **Finestre di dialogo di scelta**<br/>        | Nessuno.<br/>                                                                                                           |
| **Finestre di dialogo di stato**<br/>      | Nessuno (ma può avere un'animazione).<br/>                                                                               |
| **Dialoghe in formato informativo**<br/> | Nessuno.<br/>                                                                                                           |



 

-   **Non corretto:**

![Screenshot della finestra di dialogo con l'icona di avviso ](images/win-dialog-box-image19.png)

In questo esempio, un'icona di avviso viene usata erroneamente per una domanda che non comporta una potenziale perdita di dati o accesso al sistema.

- **È consigliabile usare le icone per consentire agli utenti di riconoscere visivamente le funzionalità del programma.** Questa tecnica è più efficace quando le icone sono facilmente riconoscibili e usate in diverse posizioni all'interno del programma.

![Screenshot della finestra di dialogo Preferiti con l'icona a forma di stella ](images/win-dialog-box-image20.png)

In questo esempio l'icona a stella gialla rappresenta Preferiti. L'icona è facilmente riconoscibile e viene usata in modo coerente Windows per rappresentare i Preferiti.

-   **Usare le icone per consentire agli utenti di riconoscere l'oggetto in questione.**

![Screenshot della finestra di dialogo con l'icona di PowerPoint ](images/win-dialog-box-image21.png)

In questo esempio l'icona dell'oggetto consente agli utenti di riconoscere il tipo di file aperto o salvato.

-   **È consigliabile usare le icone per rendere le funzionalità di auto-esplicativo.**

![Immagini di frecce che mostrano come posizionare il monitoraggio ](images/win-dialog-box-image22.png)

In questo esempio queste icone consentono agli utenti di visualizzare l'effetto delle funzionalità.

-   **Usare un'icona nelle finestre di dialogo About Box per la personalizzazione dell'applicazione.**

![Screenshot della finestra di dialogo Informazioni su con il logo di Windows ](images/win-dialog-box-image23.png)

In questo esempio viene usata una bitmap in About Box per identificare e modificare l'applicazione.

**Icone delle note a piè di pagina**

-   **Se si dispone di una nota a piè di pagina, è consigliabile usare un'icona a piè di pagina per riepilogare l'oggetto della nota.**

![Screenshot della finestra di dialogo con l'icona della nota a piè di pagina ](images/win-dialog-box-image24.png)

In questo esempio l'icona della nota a piè di pagina indica che la domanda ha implicazioni per la sicurezza.

-   **Non usare un'icona di nota a piè di pagina che ripete l'icona del corpo.**
-   **Non usare le icone standard relative a errori o informazioni.** Le condizioni di errore devono essere comunicate tramite l'icona del corpo e le note a piè di pagina sono sempre per informazioni, rendendo ridondante l'icona delle informazioni. Tuttavia, è possibile usare l'icona di avviso standard e lo shield di sicurezza giallo per avvisare gli utenti di conseguenze rischiose.

Per altre informazioni ed esempi, vedere [Icone.](vis-icons.md)

### <a name="commit-buttons"></a>Pulsanti di commit

**Note:**

-   Queste linee guida non si applicano alle finestre di dialogo delle domande usando i collegamenti ai comandi, perché questo modello usa collegamenti di comando anziché pulsanti.
-   \[Eseguire questa operazione e non eseguire questa operazione sono rispettivamente risposte affermative e negative \] \[ \] all'istruzione principale.

**Generale**

-   **Scegliere i pulsanti di commit in base al modello di progettazione:**

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
    <td><strong>Finestre di dialogo domanda (con pulsanti)</strong><br/></td>
    <td>Uno dei seguenti set di comandi concisi: Yes/No, Yes/No/Cancel, [Do it]/Cancel, [Do it]/[Don't do it], [Do it]/[Don't do it]/[Don't do it]/Cancel.<br/></td>
    </tr>
    <tr class="odd">
    <td><strong>Finestre di dialogo per le domande (tramite collegamenti)</strong><br/></td>
    <td>Annulla.<br/></td>
    </tr>
    <tr class="even">
    <td><strong>Finestre di dialogo di scelta</strong><br/></td>
    <td><ul>
    <li>Finestre di dialogo modali: OK/Annulla o [Sì]/Annulla</li>
    <li>Finestre di dialogo non modali: pulsante Chiudi nella finestra di dialogo e nella barra del titolo</li>
    <li>Riquadro attività: pulsante Chiudi sulla barra del titolo</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><strong>Finestre di dialogo di stato</strong><br/></td>
    <td>Usare Cancel se riporta l'ambiente allo stato precedente (senza alcun effetto collaterale); In caso contrario, usare Stop.<br/></td>
    </tr>
    <tr class="even">
    <td><strong>Dialoghe in formato informativo</strong><br/></td>
    <td>Quasi.<br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   **Tutti i pulsanti di commit tranne Applica comportano la chiusura della finestra di dialogo.**
-   **Non confermare i pulsanti di commit.** Inutilmente, questa operazione può essere molto fastidiosa. **Eccezioni:**

    -   L'azione è potenzialmente catastrofica.
    -   L'azione è chiaramente incoerente con altre azioni.
    -   Se non è corretta, l'azione può comportare una perdita significativa di dati, tempo o lavoro richiesto per conto dell'utente.

    Per altre linee guida ed esempi, vedere [Conferme.](mess-confirm.md)

-   **Non disabilitare i pulsanti di commit. Eccezioni:**
    -   **Se gli utenti devono elevare i privilegi per apportare una modifica, disabilitare i pulsanti di commit positivo fino a quando l'utente non apporta una modifica.** In questo modo si impedisce agli utenti di elevare solo per chiudere una finestra forzandoli a fare clic su Annulla.
    -   Per altre eccezioni, vedere Disabilitazione o rimozione di controlli e [invio di messaggi di errore.](#disabling-or-removing-controls-vs-giving-error-messages)
-   **Allinea a destra i pulsanti di commit in una singola riga nella parte** inferiore della finestra di dialogo, ma sopra l'area della nota a piè di pagina. Eseguire questa operazione anche se è presente un singolo pulsante di commit, ad esempio OK.

    **Non corretto:**

    ![Screenshot del messaggio con il pulsante OK centrato ](images/win-dialog-box-image25.png)

    In questo esempio il pulsante OK è centrato in modo errato.

-   **Presentare i pulsanti di commit nell'ordine seguente:**
    1.  OK/ \[ Do it \] /Yes
    2.  \[Non eseguire questa operazione \] /No
    3.  Annulla
    4.  Applica (se presente)
    5.  Guida (se presente)
-   **Se sono presenti molti pulsanti di commit correlati, consolidarli usando i pulsanti di menu suddivisi**.
-   **Avere una netta separazione dai pulsanti di commit (che chiudono la finestra) e da tutti gli altri pulsanti di comando (ad esempio Avanzate).**

**Risposta alle istruzioni principali**

-   **Usare pulsanti di commit positivi che sono risposte specifiche all'istruzione principale, anziché etichette generiche, ad esempio OK o Sì/No.** Gli utenti devono essere in grado di comprendere le opzioni leggendo solo il testo del pulsante. **Eccezioni:**
    -   Usare Chiudi per le finestre di dialogo che non hanno impostazioni, ad esempio le finestre di dialogo in formato informativo. Non usare mai Chiudi per le finestre di dialogo con impostazioni.
    -   Usare OK quando le risposte "specifiche" sono ancora generiche, ad esempio Salva, Seleziona o Scegli. Usare OK quando si modifica un'impostazione specifica o una raccolta di impostazioni.
    -   **Per le finestre di dialogo legacy senza un'istruzione principale, è possibile usare etichette generiche, ad esempio OK.** Spesso tali finestre di dialogo non sono progettate per eseguire un'attività specifica, impedendo risposte più specifiche.
    -   Alcune attività richiedono una lettura più attenta e più attenta per consentire agli utenti di prendere decisioni informate. Ciò avviene in genere con [le conferme](mess-confirm.md). **In questi casi, è possibile usare le etichette generiche dei pulsanti di commit per forzare gli utenti a leggere le istruzioni principali e impedire decisioni rapide.**

        **Corretto:**

        ![Screenshot del messaggio con pulsanti Sì e No](images/win-dialog-box-image26.png)

        In questo esempio, l'uso dei pulsanti di commit Sì/No impone agli utenti di leggere almeno l'istruzione principale.

-   In alternativa, è possibile aggiungere la parola **"comunque"** all'etichetta del pulsante commit positivo per indicare che la finestra di dialogo presenta un motivo per non procedere e che gli utenti devono leggere attentamente la finestra di dialogo prima di procedere.

    **Corretto:**

    ![Screenshot del messaggio e pulsante Disinstalla comunque ](images/win-dialog-box-image27.png)

    In questo esempio viene aggiunto "comunque" all'etichetta del pulsante commit per indicare che gli utenti devono procedere con attenzione.

-   **Usare Cancel o Close per i pulsanti di commit negativo anziché risposte specifiche all'istruzione principale.** Spesso gli utenti si rendono conto di non voler eseguire un'attività quando visualizzano una finestra di dialogo. Se l'opzione Annulla o Chiudi è stata rietichettata in base a risposte specifiche, gli utenti devono leggere attentamente tutti i pulsanti di commit per determinare come annullare. **L'etichettaTura di Annulla e Chiudi consente di trovarle in modo coerente. Eccezioni:**
    -   **Non usare Sì/Annulla.** Usare sempre Sì/No come coppia.
    -   **Usare una risposta specifica quando Cancel è ambiguo.**
-   **Non eseguire il mapping di etichette generiche al significato specifico con il testo nell'area del contenuto.** Usare invece etichette specifiche del pulsante di commit o una finestra di dialogo di domande con collegamenti se le etichette sono lunghe.

    **Non corretto:**

    ![Screenshot del messaggio con l'uso poco chiaro dei pulsanti ](images/win-dialog-box-image28.png)

    In questo esempio viene eseguito il mapping di OK a Continua, Cancel viene mappato a Remain on Page.

**Pulsanti Sì e No**

-   **Preferire risposte specifiche ai pulsanti Sì e No.** Anche se non c'è niente di sbagliato nell'uso di Sì e No, risposte specifiche possono essere comprese più rapidamente, determinando un processo decisionale efficiente. Tuttavia, [le conferme](mess-confirm.md) hanno in genere i pulsanti Sì e No per fare in modo che gli utenti dia un po' [di tempo prima](mess-confirm.md) di rispondere.
-   **Usare i pulsanti Sì e No solo per rispondere a domande sì o no.** L'istruzione principale deve essere espressa naturalmente come domanda sì o no. Non usare mai OK e Annulla per domande sì o no.

    **Non corretto:**

    ![Screenshot che mostra un messaggio con un 'OK' per una domanda sì-no.](images/win-dialog-box-image29.png)

    **Corretto:**

    ![screenshot del messaggio con sì per la stessa domanda ](images/win-dialog-box-image30.png)

    **Migliore:**

    ![screenshot del messaggio con l'esecuzione per la stessa domanda ](images/win-dialog-box-image31.png)

    In questi esempi, Sì e No sono risposte buone a domande sì e no, ma risposte specifiche sono ancora migliori.

-   **Prendere in considerazione la formulazione dell'istruzione principale come domanda sì o no se i pulsanti di commit con formulazione specifica sono lunghi o difficili.** In alternativa, è possibile usare i collegamenti di comando per risposte più lunghe (cinque o più parole) all'istruzione principale.

    **Non corretto:**

    ![screenshot del messaggio con etichette di pulsanti wordy ](images/win-dialog-box-image32.png)

    **Corretto:**

    ![Screenshot del messaggio con etichette di pulsante Sì/No ](images/win-dialog-box-image33.png)

    La formulazione specifica nell'esempio non corretto è troppo lunga, quindi l'esempio corretto usa Sì e No.

-   **Non usare i pulsanti Sì e No se il significato della risposta No non è chiaro.** In tal caso, usare risposte specifiche.

**Pulsanti OK**

-   **Nelle finestre di dialogo modali, fare clic su OK significa applicare i valori, eseguire l'attività e chiudere la finestra.**
-   **Non usare i pulsanti OK per rispondere alle domande.**
-   **Non assegnare i tasti di scelta a OK, perché INVIO è la chiave di accesso per il pulsante predefinito.** In questo modo le altre chiavi di accesso sono più facili da assegnare.
-   **Etichettare correttamente i pulsanti OK.** Il pulsante OK dovrebbe avere l'etichetta OK, non OK o OK.
-   **Non usare i pulsanti OK per gli errori o gli avvisi.** I problemi non sono mai ok. In alternativa, usare Close.

    **Non corretto:**

    ![Screenshot del messaggio con il pulsante OK ](images/win-dialog-box-image34.png)

    In questo esempio è necessario usare Close anziché OK.

-   **Non usare i pulsanti OK nelle finestre di dialogo non modali.** Le finestre di dialogo non modali devono invece usare pulsanti di commit specifici dell'attività, ad esempio Trova. Tuttavia, alcune finestre di dialogo non modali richiedono solo un pulsante Chiudi.

**Pulsanti Annulla**

-   **Fare clic su Annulla significa abbandonare tutte le modifiche, annullare l'attività, chiudere la finestra e ripristinare lo stato precedente dell'ambiente, senza lasciare alcun effetto collaterale.** Per le finestre di dialogo di scelta annidate, se si fa clic su Annulla nella finestra di dialogo di scelta del proprietario, vengono abbandonate anche le modifiche apportate dalle finestre di dialogo di scelta di proprietà.
-   **Specificare un pulsante Annulla per consentire agli utenti di abbandonare le modifiche in modo esplicito.** Le finestre di dialogo necessitano di un punto di uscita chiaro. Non dipendere dal fatto che gli utenti trovino il pulsante Chiudi sulla barra del titolo.

    -   **Eccezione:** Non specificare un pulsante Annulla per le finestre di dialogo senza impostazioni. In questo caso, i pulsanti OK e Chiudi hanno lo stesso effetto di Annulla.

    **Non corretto:**

    ![Screenshot del messaggio solo con il pulsante OK ](images/win-dialog-box-image35.png)

    In questo esempio, se sulla barra del titolo è presente solo un pulsante Chiudi, viene visualizzato come se gli utenti non fossero autorizzati a scegliere.

-   **Non usare i pulsanti Annulla per rispondere alle domande.**

    **Non corretto:**

    ![screenshot del messaggio con ok per una domanda sì-no ](images/win-dialog-box-image36.png)

    In questo esempio, OK e Annulla vengono usati in modo errato per rispondere a una domanda Sì o No.

-   **Non assegnare le chiavi di accesso a Annulla, perché ESC è la chiave di accesso.** In questo modo le altre chiavi di accesso sono più facili da assegnare.
-   **Non usare i pulsanti Annulla nelle finestre di dialogo non modali.** Usare invece Close.
-   **Non disabilitare il pulsante Annulla.** Gli utenti devono essere sempre in grado di annullare le finestre di dialogo.
    -   **Eccezione:** È possibile disabilitare il pulsante Annulla in una finestra di dialogo di stato se è presente un periodo durante il quale l'operazione non può essere annullata. Tuttavia, una soluzione migliore consiste nel progettare tali operazioni in modo che siano sempre annullabili.

**Pulsanti chiudi**

-   **Usare i pulsanti Chiudi per le finestre di dialogo non modali, nonché per le finestre di dialogo modali che non possono essere annullate.**
-   **Fare clic su Chiudi per chiudere la finestra di dialogo, lasciando eventuali effetti collaterali esistenti.** Non usare Done perché non è una costruzione imperativa. Per le finestre di dialogo di scelta annidate, se si fa clic su Chiudi nella finestra di dialogo di scelta del proprietario, tutte le modifiche apportate dalle finestre di dialogo di scelta di proprietà vengono mantenute.
-   **Inserire un pulsante Chiudi esplicito nel corpo della finestra di dialogo.** Le finestre di dialogo necessitano di un punto di uscita chiaro. Non dipendere dal fatto che gli utenti trovino il pulsante Chiudi sulla barra del titolo.
-   **Assicurarsi che il pulsante Chiudi sulla barra del titolo abbia lo stesso effetto di Annulla o Chiudi.**
-   **Non assegnare chiavi di accesso a Chiudi, perché ESC è la chiave di accesso.** In questo modo le altre chiavi di accesso sono più facili da assegnare.

**Applicare i pulsanti**

-   **Non usare i pulsanti Applica nelle finestre di dialogo che non sono finestre delle proprietà o pannelli di controllo.** Il pulsante Applica significa applicare le modifiche in sospeso, ma lasciare aperta la finestra. In questo modo gli utenti possono valutare le modifiche prima di chiudere la finestra. Tuttavia, solo la finestra delle proprietà e i pannelli di controllo hanno questa esigenza.

    **Non corretto:**

    ![Screenshot della finestra di dialogo con il pulsante Applica ](images/win-dialog-box-image37.png)

    In questo esempio, una finestra di dialogo di scelta include in modo inutile un pulsante Applica.

**Pulsanti di commit per le finestre di dialogo indirette**

**Nota:** Le finestre di dialogo indirette vengono visualizzate fuori contesto, come risultato indiretto di un'attività o come risultato di un problema con un sistema o un processo in background. Per le finestre di dialogo indirette, il pulsante Annulla è ambiguo perché potrebbe significare annullare la finestra di dialogo o annullare l'intera attività.

-   **Se gli utenti devono annullare sia la finestra di dialogo che l'attività, assegnare i pulsanti di commit per eseguire entrambe le operazioni.** Etichettare il pulsante che annulla la finestra di dialogo con una risposta negativa all'istruzione principale. Etichettare il pulsante che annulla l'intera attività con Annulla. L'uso di Annulla consente di utilizzare la finestra di dialogo in molti contesti.

    **Corretto:**

    ![Screenshot della finestra di dialogo con salva/non salva ](images/win-dialog-box-image38.png)

    In questo esempio questa finestra di dialogo viene visualizzata da Windows Paint come risultato di un comando New o Exit quando l'elemento grafico non è stato salvato. Non salvare chiude la finestra di dialogo senza salvare, mentre Annulla annulla il comando Nuovo o Esci.

    **Non corretto:**

    ![Screenshot della finestra di dialogo con pulsanti Sì/No ](images/win-dialog-box-image39.png)

    In questo esempio non è possibile annullare l'attività (chiusura Office barra dei collegamenti) che ha portato alla visualizzazione di questa finestra di dialogo. Per questa finestra di dialogo è necessario un pulsante Annulla.

-   **Se gli utenti devono** semplicemente annullare la finestra di dialogo ma non l'attività, usare un pulsante con una risposta negativa specifica all'istruzione principale e non avere un pulsante Annulla.

    ![Screenshot della finestra di dialogo con run/don't run ](images/win-dialog-box-image24.png)

    In questo esempio questa finestra di dialogo viene visualizzata indirettamente come risultato del passaggio a una pagina Web che installa un controllo ActiveX controllo . In questo caso l'uso di Cancel sarebbe ambiguo, quindi viene usato Don't run (Non eseguire).

Per altre informazioni ed esempi, vedere [Pulsanti di comando.](ctrl-command-buttons.md)

### <a name="command-links"></a>Collegamenti di comando

-   **Presentare un set di comandi lunghi usando i collegamenti di comando, anziché pulsanti di comando o una combinazione di pulsanti di opzione e un pulsante OK.** In questo modo gli utenti possono rispondere con un solo clic. Tuttavia, questo approccio funziona solo per una singola domanda.
-   **Presentare prima i collegamenti ai comandi usati più di frequente.** L'ordine risultante deve seguire approssimativamente la probabilità di utilizzo, ma avere anche un flusso logico.
    -   **Eccezione:** I collegamenti di comando che comportano l'esecuzione di tutti gli elementi devono essere posizionati per primi.
-   Se un collegamento al comando richiede un'ulteriore spiegazione, **fornire una spiegazione supplementare.** Le spiegazioni supplementari descrivono il motivo per cui gli utenti potrebbero voler scegliere il comando o cosa accade se si sceglie il comando.
-   **Non usare spiegazioni supplementari che siano rielevazioni di parole del collegamento al comando.** Usare una spiegazione supplementare solo quando non è possibile rendere autoesplicativo un collegamento al comando. Fornire una spiegazione supplementare per un collegamento di comando non significa che è necessario specificarli per tutti i comandi.

![Screenshot della finestra di dialogo con opzioni di notazione del testo ](images/win-dialog-box-image40.png)

In questo esempio la spiegazione supplementare descrive le implicazioni di una delle opzioni.

-   **Usare frasi che iniziano con un verbo, senza terminare la punteggiatura.**
-   **Se un comando è fortemente consigliato, è consigliabile aggiungere "(consigliato)" all'etichetta.** Assicurarsi di aggiungere all'etichetta del collegamento, non la spiegazione supplementare.
-   **Se un comando è destinato solo agli utenti avanzati, è consigliabile aggiungere "(advanced)" all'etichetta.** Assicurarsi di aggiungere all'etichetta del collegamento, non la spiegazione supplementare.
-   **Specificare sempre un pulsante Annulla esplicito.** Non usare un collegamento di comando a questo scopo.

**Non corretto:**

![Screenshot della finestra di dialogo con il collegamento Non uscire ](images/win-dialog-box-image41.png)

In questo esempio la finestra di dialogo usa un collegamento di comando anziché un pulsante Annulla.

Per altre informazioni ed esempi, vedere [Collegamenti ai comandi.](ctrl-command-links.md)

### <a name="dont-show-this-item-again"></a>Non visualizzare questo <item> di nuovo

-   **È consigliabile usare l'opzione Non visualizzare più questa opzione per consentire agli utenti di eliminare una finestra di dialogo ricorrente solo se non esiste <item> un'alternativa migliore.** È sempre meglio visualizzare la finestra di dialogo se gli utenti ne hanno effettivamente bisogno o semplicemente eliminarla in caso contrario.
-   **Usare questa formulazione specifica sostituire <item> con l'elemento specifico.** Ad esempio, Non visualizzare più questo promemoria. Quando si fa riferimento a una finestra di dialogo in generale, usare Non visualizzare più questo messaggio.
-   **Indicare chiaramente quando verrà usato l'input** dell'utente per i valori predefiniti futuri aggiungendo la frase seguente sotto l'opzione : Le selezioni verranno usate per impostazione predefinita in futuro.
-   **Non selezionare l'opzione per impostazione predefinita. Se la finestra di dialogo deve essere effettivamente visualizzata una sola volta, eseguire questa operazione senza chiedere conferma.** Non usare questa opzione per infastidire gli utenti e assicurarsi che il comportamento predefinito non sia fastidioso.

**Non corretto:**

![screenshot del messaggio che pone domande non necessarie ](images/win-dialog-box-image42.png)

In questo esempio il messaggio deve essere visualizzato una sola volta. Non è necessario chiedere.

-   **Rendere persistente l'impostazione per ogni utente.**
-   **Se gli utenti selezionano l'opzione e fa clic su Annulla, questa opzione ha effetto.** Questa impostazione è una meta-opzione, quindi non segue il comportamento standard di annullamento di senza lasciare alcun effetto collaterale. Si noti che se gli utenti non vogliono visualizzare il dialogo in futuro, è probabile che vogliano annullarlo.
-   Se gli utenti potrebbero dover ripristinare queste finestre di dialogo, specificare un **comando** Ripristina messaggi nella finestra di dialogo Opzioni del programma.

### <a name="ask-me-later"></a>Richiedi in seguito

-   Specificare questa opzione per chiudere una finestra di dialogo solo quando:
    -   **La finestra di dialogo è indiretta,** pertanto è probabile che gli utenti siano incentrati su un'altra attività.
    -   **Gli utenti devono rispondere, ma non immediatamente,** in modo che possano continuare a lavorare.
    -   **La domanda richiede un impegno o un impegno sufficiente** in modo che gli utenti potrebbero prendere decisioni migliori se hanno più tempo.
    -   **La finestra di dialogo o l'opzione verrà visualizzata automaticamente in un secondo momento,** in modo che gli utenti siano effettivamente invitati in un secondo momento.
-   **Non corretto:**
-   ![Screenshot del messaggio con l'opzione Chiedi conferma in un secondo momento ](images/win-dialog-box-image43.png)
-   In questo esempio la domanda è abbastanza semplice da complicare solo l'aggiunta di un'opzione Chiedi in un secondo momento.
-   In caso contrario, si prevede che gli utenti rispondano ora, ma consentono loro di chiudere normalmente la finestra di dialogo con Annulla o Chiudi. Se usata correttamente, questa opzione dovrebbe essere rara.

### <a name="morefewer"></a>Più o meno

-   **Usare i pulsanti Diffusione progressiva più o meno per mostrare o nascondere opzioni, comandi o dettagli avanzati o usati raramente che in genere non sono necessari per gli utenti.** Questa operazione semplifica la finestra di dialogo per l'utilizzo tipico. Non nascondere le opzioni, i comandi o le informazioni di uso comune perché gli utenti potrebbero non trovarle.

![Screenshot della finestra di dialogo con il pulsante Altre opzioni ](images/win-dialog-box-image24.png)

In questo esempio le opzioni usate raramente sono nascoste per impostazione predefinita.

-   **Non usare più o meno controlli a meno che non ci siano effettivamente più dettagli da visualizzare.** Non è sufficiente ripristinare le stesse informazioni in un formato diverso.
-   **Non usare più o meno controlli per visualizzare la Guida.** Usare invece i collegamenti della Guida o le note a piè di pagina.
-   **Con le finestre di dialogo delle attività, evitare di combinare più/meno controlli con Non visualizzare <item> più.** Questa combinazione ha un aspetto scomodo.
-   Per le linee guida sull'etichettatura, vedere [Divulgazione progressiva.](ctrl-progressive-disclosure-controls.md)

### <a name="footnotes"></a>Note a piè di pagina

-   **Usare le note a piè di pagina per informazioni non essenziali per lo scopo di una finestra di dialogo, ma che gli utenti possono risultare utili per prendere decisioni.** La maggior parte degli utenti deve essere in grado di ignorare le note a piè di pagina e prendere decisioni informate nella risposta alla finestra di dialogo.

![Screenshot della finestra di dialogo con nota a piè di pagina chiarificante ](images/win-dialog-box-image44.png)

In questo esempio, le informazioni sulle note a piè di pagina sono supplementari, non essenziali.

### <a name="disabling-or-removing-controls-vs-giving-error-messages"></a>Disabilitazione o rimozione di controlli e invio di messaggi di errore

-   Quando un controllo non si applica nel contesto corrente, prendere in considerazione le opzioni seguenti:
    -   **Rimuovere il controllo quando gli utenti non possono abilitarlo o non si aspettano che si applivi e il relativo stato non cambi di frequente.** In questo modo la finestra di dialogo viene semplificata e gli utenti non la mancheranno. La visualizzazione e la scomparsa di un controllo spesso è fastidioso.
    -   **Disabilitare il controllo quando gli utenti prevedono l'applicazione o il relativo stato cambia di frequente e gli utenti possono facilmente dedurre il motivo per cui il controllo è disabilitato.** Un esempio di facile deduzione è la disabilitazione di un pulsante di commit quando è presente una singola casella di testo vuota che richiede qualsiasi input. È possibile usare [i fumetto per](ctrl-balloons.md) visualizzare problemi di input utente non critici con caselle di testo ed elenchi a discesa modificabili. Tuttavia, se il problema non può essere spiegato con un fumetto o coinvolge più controlli, la deduzione non sarebbe più semplice.
    -   **In caso contrario, lasciare il controllo abilitato, ma fornire un messaggio di errore quando viene usato in modo non corretto.** La disabilitazione in questo caso renderebbe difficile agli utenti comprendere il motivo per cui il controllo è disabilitato. Gli utenti saranno costretti a determinare il problema tramite la sperimentazione e la logica deducibile. È meglio solo fornire un messaggio di errore utile per spiegare il problema in modo esplicito.
-   **Suggerimento:** Se non si è certi che sia necessario disabilitare un controllo o inviare un messaggio di errore, iniziare componendo il messaggio di errore che è possibile fornire. Se il messaggio di errore contiene informazioni utili che gli utenti di destinazione probabilmente non dedurranno rapidamente, lasciare il controllo abilitato e fornire l'errore. In caso contrario, disabilitare il controllo .
-   **Se si disabilita un controllo, disabilitare anche tutti** i controlli associati, ad esempio l'etichetta, le spiegazioni supplementari o i pulsanti di comando. Tuttavia, non disabilitare le caselle [di gruppo,](ctrl-group-boxes.md)l'etichetta di gruppo o la spiegazione del gruppo, se presenti.

![Screenshot della finestra di dialogo con controlli in grigio ](images/win-dialog-box-image45.png)

In questo esempio sono disabilitate anche le etichette delle caselle di testo disabilitate, ma non l'etichetta del gruppo e la spiegazione del gruppo.

### <a name="required-input"></a>Input richiesto

-   Per indicare che gli utenti devono fornire informazioni in un controllo , considerare le opzioni seguenti:
    -   **Non indicare nulla, ma gestire l'input obbligatorio mancante con messaggi di errore.** Questo approccio riduce l'ingombro e funziona correttamente se la maggior parte dell'input è facoltativa o se gli utenti probabilmente non ignorano i controlli, mantenendo così basso il numero di messaggi di errore.
    -   **Indicare l'input richiesto usando un asterisco all'inizio dell'etichetta.** Spiegare l'asterisco usando:

        -   Nota a piè di pagina nella parte inferiore dell'area del contenuto che indica \* Input obbligatorio.
        -   Descrizione comando sull'asterisco che indica Input obbligatorio.

        Questo approccio funziona bene se non sono presenti molti controlli obbligatori, ma in modo non utile se è necessaria la maggior parte dei controlli.

        ![Screenshot delle etichette delle caselle di testo con asterischi ](images/win-dialog-box-image46.png)

        In questo esempio vengono usati asterischi per indicare l'input richiesto.

    -   **Se tutti i controlli richiedono l'input, immettere "Tutti gli input necessari" in una posizione appropriata nella parte superiore dell'area del contenuto.** Questo approccio riduce l'ingombro per questo caso specifico.
    -   **Indicare gli input facoltativi con "(facoltativo)" dopo l'etichetta.** Questo approccio funziona correttamente se la maggior parte dell'input è necessaria, ma in caso contrario non è così.

-   **Per coerenza, provare a usare lo stesso metodo per indicare l'input richiesto in tutto il programma.** In particolare, indicare l'input obbligatorio o facoltativo in base alle esigenze, ma evitare di usare entrambi all'interno dello stesso programma.

### <a name="error-handling"></a>Gestione degli errori

-   Evitare gli errori usando controlli vincolati all'input utente valido. È anche possibile ridurre il numero di errori fornendo valori predefiniti ragionevoli.
-   Convalidare l'input dell'utente appena possibile e visualizzare gli errori il più possibile al punto di input.
-   **Usare la gestione degli errori non modali (errori sul posto o fumetto) per i problemi di input dell'utente.**
    -   **Usare i palloncino per i problemi di input utente non critici rilevati in una casella di testo o immediatamente dopo che una casella di testo perde lo stato attivo.** I fumetto non richiedono lo spazio disponibile sullo schermo o il layout dinamico necessario per visualizzare i messaggi sul posto. Consente di visualizzare un solo fumetto alla volta. Poiché il problema non è critico, non è necessaria alcuna icona di errore. I palloncini vengono visualizzati quando si fa clic, quando il problema viene risolto o dopo un timeout.

        ![Screenshot del messaggio "carattere non corretto" ](images/win-dialog-box-image47.png)

        In questo esempio, un fumetto indica un problema di input mentre è ancora nel controllo .

-   Usare gli errori sul posto per il rilevamento degli errori **ritardati,** in genere gli errori rilevati facendo clic su un pulsante di commit. Non usare errori sul posto per le impostazioni di cui viene eseguito immediatamente il commit. Possono essere presenti più errori sul posto contemporaneamente. Usare testo normale e un'icona di errore di 16x16 pixel, posizionandoli direttamente accanto al problema, quando possibile. Gli errori sul posto non vengono visualizzati a meno che l'utente non eserciti il commit e non vengano trovati altri errori.

    ![Screenshot della finestra di dialogo con due messaggi di errore ](images/win-dialog-box-image48.png)

    In questo esempio viene usato un errore sul posto per un errore rilevato facendo clic sul pulsante commit.

-   Usare la gestione degli errori modale (finestre di dialogo di attività o finestre di messaggio) per tutti gli altri **problemi,** inclusi gli errori che coinvolgono più controlli o sono errori non contestuali o non di input trovati facendo clic su un pulsante di commit.
-   **Quando viene rilevato e segnalato un problema di input, impostare lo stato attivo per l'input sul primo controllo con i dati non corretti.** Scorrere il controllo nella visualizzazione, se necessario.

Per altre informazioni ed esempi, vedere [Messaggi di errore](mess-error.md) e [balloon](ctrl-balloons.md).

### <a name="help"></a>Help

-   Quando si fornisce assistenza all'utente, considerare le opzioni seguenti (elencate nell'ordine di preferenza):
    -   Assegnare etichette descrittive ai controlli interattivi. È più probabile che gli utenti leggono le etichette nei controlli interattivi rispetto a qualsiasi altro testo.
    -   Fornire spiegazioni nel contesto usando etichette [di testo statiche.](text-ui.md)
    -   Fornire un collegamento specifico della Guida a un argomento della Guida pertinente.
-   **Individuare i collegamenti della Guida nella parte inferiore dell'area del contenuto della finestra di dialogo.** Se la finestra di dialogo contiene una nota a piè di pagina e il collegamento Guida è correlato, inserire il collegamento Guida all'interno della nota a piè di pagina.

    ![Screenshot della finestra di dialogo con collegamento alla Guida ](images/win-dialog-box-image40.png)

    In questo esempio il collegamento Guida si applica all'intera finestra di dialogo.

    -   **Eccezione:** Se in una finestra di dialogo sono presenti diversi gruppi distinti di impostazioni con argomenti della Guida separati,ad esempio all'interno di caselle di gruppo, individuare i collegamenti della Guida nella parte inferiore dei gruppi.

-   **Non usare collegamenti a argomenti della Guida generici o generici o pulsanti generici della Guida.** Gli utenti spesso ignorano la Guida generica.

Per altre informazioni ed esempi, vedere [la Guida.](winenv-help.md)

### <a name="default-values"></a>Valori predefiniti

-   Includere un pulsante di commit predefinito in ogni finestra di dialogo.
-   Per le finestre di dialogo delle domande:
    -   **Selezionare la risposta più sicura (per evitare la perdita di dati o l'accesso al sistema), la risposta più sicura come predefinita.** Se la sicurezza e la sicurezza non sono fattori, selezionare la risposta più probabile o conveniente.
        -   **Eccezione:** Non impostare una risposta distruttiva come predefinita a meno che non sia disponibile un modo semplice ed ovvio per annullare il comando.
-   Per le finestre di dialogo di scelta:
    -   Per i valori predefiniti iniziali, selezionare i valori più sicuri (per evitare la perdita di dati o l'accesso al sistema) e la maggior parte dei valori **sicuri per ogni controllo.** Se la sicurezza e la sicurezza non sono fattori, selezionare le opzioni più probabili o convenienti.
    -   Per i valori predefiniti successivi, selezionare di nuovo le opzioni selezionate in precedenza se è probabile che tali valori siano ripetuti e questa operazione **è sicura e sicura.** In caso contrario, selezionare i valori predefiniti iniziali.

![Screenshot della finestra di dialogo stampa ](images/win-dialog-box-image49.png)

In questo esempio, è molto probabile che gli utenti scelgo le stesse impostazioni di stampa dell'ultima volta. Tuttavia, è probabile che il numero di copie desiderato cambi, quindi questa impostazione non viene riselezionata.

## <a name="recommended-sizing-and-spacing&quot;></a>Dimensioni e spaziatura consigliate

-   **Supportare la risoluzione Windows dello schermo di Vista minima di 800 x 600 pixel.** I layout possono essere ottimizzati per le finestre ridimensionabili usando una risoluzione dello schermo di 1024 x 768 pixel.
-   **Usare le finestre ridimensionabili ogni volta che è pratico per evitare barre di scorrimento e dati troncati.** Windows contenuto dinamico e gli elenchi traggono il massimo vantaggio dalle finestre ridimensionabili.
-   **Le finestre a dimensione fissa devono essere completamente visibili e ridimensionate per adattarsi all'interno dell'area di lavoro.**
-   **Le finestre ridimensionabili possono essere ottimizzate per risoluzioni più elevate, ma ridimensionate in base alle esigenze in fase di visualizzazione fino alla risoluzione effettiva dello schermo.**
-   **Scegliere le dimensioni predefinite della finestra appropriate per il contenuto.** Se è possibile usare lo spazio in modo efficace, non è necessario usare dimensioni di finestra iniziali maggiori.

## <a name=&quot;text&quot;></a>Testo

### <a name=&quot;general&quot;></a>Generale

-   **Rimuovere il testo ridondante.** Cercare testo ridondante in titoli, istruzioni principali, istruzioni supplementari, aree di contenuto, collegamenti ai comandi e pulsanti di commit. In genere, lasciare il testo completo nelle istruzioni e nei controlli interattivi e rimuovere la ridondanza dalle altre posizioni.
-   **Usare formulazioni positive.** La formulazione positiva è più facile da comprendere per gli utenti.

**Corretto:**

Si vuole abilitare la condivisione di file e stampanti?

**Non corretto:**

Disabilitare la condivisione di file e stampanti?

Tuttavia, la formulazione deve corrispondere al comando associato, anche se il comando è con frase negativa; quindi, ad esempio, usare disable per confermare un comando Disable.

-   **Se necessario, usare la parola &quot;finestra&quot; per fare riferimento alla finestra di dialogo stessa.**
-   **Usare la seconda persona (&quot;you/your")** per indicare agli utenti cosa fare nell'area principale dell'istruzione e del contenuto. Spesso la seconda persona è implicita.

**Esempi:**

Scegliere le immagini da stampare

Scegliere un account

-   **Usare la prima persona ("I/me/my")** per consentire agli utenti di indicare al programma cosa fare nei controlli nell'area del contenuto che rispondono all'istruzione principale.

**Esempio:** Stampare le foto sulla fotocamera.

### <a name="dialog-box-titles"></a>Titoli delle finestre di dialogo

-   **Usare il titolo per identificare il comando, la funzionalità o il programma da cui viene visualizzata una finestra di dialogo.**
    -   Se la finestra di dialogo viene avviata dall'utente, identificarla usando il nome del comando o della funzionalità. **Eccezioni:**
        -   Se una finestra di dialogo viene visualizzata da molti comandi diversi, è consigliabile usare il nome del programma.
        -   Se tale titolo sarebbe ridondante con l'istruzione main, usare invece il nome del programma.
    -   Se è avviato dal programma o dal sistema (e quindi fuori contesto), identificarlo usando il nome del programma o della funzionalità per fornire il contesto.
    -   Non usare il titolo per spiegare cosa fare nella finestra di dialogo che è lo scopo dell'istruzione principale.
-   Usare il nome esatto del comando per i nomi basati su comandi, ma non includere i puntini di sospensione, se presenti. Se necessario, è possibile includere il titolo del menu del comando per comporre un titolo. Esempio: per un oggetto ... in un menu Inserisci usare il titolo Inserisci oggetto.
-   **Se sulla barra delle applicazioni** viene visualizzata una finestra di dialogo non modali, ottimizzare il titolo per la visualizzazione sulla barra delle applicazioni inserendo concisamente le informazioni distintive. Esempi: "66% completato" e "3 promemoria".
-   **Non includere le parole "dialog" o "progress" nel titolo.** Ciò è implicito e lasciarlo disattivato semplifica l'analisi da parte degli utenti.
-   Usare [l'uso di maiuscole e minuscole](glossary.md)in stile titolo senza terminare la punteggiatura.

### <a name="main-instructions"></a>Istruzioni principali

-   **Usare l'istruzione principale per spiegare concisamente cosa fare nella finestra di dialogo.** L'istruzione deve essere un'istruzione specifica, una direzione imperativa o una domanda. Le buone istruzioni comunicano l'obiettivo dell'utente con il dialogo anziché concentrarsi esclusivamente sui meccanismi di modifica.
-   **Omettere l'istruzione principale quando l'unica cosa che si può dire è ovvia.** In questi casi, il contenuto della finestra di dialogo è auto-esplicativo. Ad esempio, le finestre di dialogo Comuni Apri file e Salva file non necessitano di un'istruzione principale perché il contesto e la progettazione rendono evidente lo scopo.
-   **Omettere le etichette di controllo che restate l'istruzione principale.** In questo caso, l'istruzione principale accetta la chiave di accesso.

**Accettabile:**

![Screenshot della casella di testo con etichetta ridondante ](images/win-dialog-box-image50.png)

In questo esempio l'etichetta della casella di testo è solo una riezione dell'istruzione principale.

**Migliore:**

![Screenshot della stessa casella di testo con un'etichetta ](images/win-dialog-box-image51.png)

In questo esempio l'etichetta ridondante viene rimossa, quindi l'istruzione principale accetta la chiave di accesso.

-   **Usare concisa una sola frase completa.** L'istruzione principale è in grado di visualizzare le informazioni essenziali. Se è necessario spiegare altro, usare l'istruzione supplementare.
-   **Usare verbi specifici quando possibile.** Verbi specifici (ad esempio: connect, save, install) sono più significativi per gli utenti rispetto a quelli generici (ad esempio: configure, manage, set).
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   **Non includere i periodi finali se l'istruzione è un'istruzione .** Se l'istruzione è una domanda, includere un punto interrogativo finale.
-   **Per i dialoghe di stato, usare** una frase gerund che spiega brevemente l'operazione in corso, terminando con i puntini di sospensione. Esempio: Stampa delle immagini in corso...
-   **Suggerimento:** È possibile valutare un'istruzione principale immaginando ciò che si potrebbe dire a un amico. Se rispondere con l'istruzione principale sarebbe innaturale, poco utile o scomodo, rielaborare l'istruzione.

### <a name="supplemental-instructions"></a>Istruzioni supplementari

-   **Se necessario, usare un'istruzione supplementare facoltativa per presentare informazioni aggiuntive utili per comprendere o usare la pagina.** È possibile fornire informazioni più dettagliate e definire la terminologia.
-   **Se l'aspetto della finestra di dialogo è avviato dal programma o dal sistema (e quindi fuori contesto), usare l'istruzione supplementare per spiegare perché è stata visualizzata la finestra di dialogo.** Per tali dialoghe, il contesto non è in genere ovvio.
-   **Non ripetere l'istruzione principale con una formulazione leggermente diversa.** Omettere invece l'istruzione supplementare se non sono presenti altre istruzioni da aggiungere.
-   Usare frasi complete, lettere maiuscole in stile frase e punteggiatura finale.

### <a name="command-links"></a>Collegamenti ai comandi

-   **Scegliere un testo di collegamento conciso che comunichi chiaramente e differenzia ciò che fa il collegamento di comando.** Deve essere auto-esplicativo e corrispondere all'istruzione principale. Gli utenti non devono capire cosa significa realmente il collegamento o in che modo è diverso da altri collegamenti.
-   **Avviare sempre i collegamenti ai comandi con un verbo.**
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Non usare punteggiatura finale.
-   **Se necessario, fornire un'ulteriore spiegazione usando frasi complete e terminando la punteggiatura.** Tuttavia, aggiungere tali spiegazioni solo quando necessario, non aggiungere spiegazioni a tutti i collegamenti di comando solo perché un collegamento di comando ne ha bisogno.

Per altre informazioni ed esempi, vedere Linee [guida per il collegamento ai](ctrl-command-links.md) comandi.

### <a name="commit-buttons"></a>Pulsanti di commit

-   **Usare etichette specifiche dei pulsanti di commit che hanno senso e che sono una risposta all'istruzione principale.** Idealmente, gli utenti non devono leggere altro per comprendere l'etichetta. È molto più probabile che gli utenti leggono le etichette dei pulsanti di comando rispetto al testo statico.
-   **Avviare le etichette dei pulsanti di commit con un verbo. Le eccezioni sono OK, Sì e No.**
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Non usare punteggiatura finale.
-   Assegnare una chiave [di accesso univoca](glossary.md).
    -   **Eccezione:** Non assegnare i tasti di scelta ai pulsanti OK e Annulla perché i tasti di scelta sono INVIO e ESC. In questo modo le altre chiavi di accesso sono più facili da assegnare.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle finestre di dialogo:

-   Nella programmazione e in altri documenti tecnici, fare riferimento alle finestre di dialogo come finestre di dialogo. In qualsiasi altra posizione, fare riferimento alle finestre di dialogo in base al titolo. Se la barra del titolo è nascosta, fare riferimento alla finestra di dialogo usando l'istruzione principale.
-   Se è necessario fare riferimento a una finestra di dialogo in generale, usare window nella documentazione dell'utente. È possibile fare riferimento a un semplice dialogo di domande o a una conferma come messaggio.
-   Usare il titolo esatto o il testo dell'istruzione principale, inclusa la relativa maiuscola.
-   Quando possibile, formattare il titolo usando il testo in grassetto. In caso contrario, inserire il titolo tra virgolette solo se necessario per evitare confusione.

Esempio: in **Sicurezza di Windows** fare clic su **Altre opzioni**.

