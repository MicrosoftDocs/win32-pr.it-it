---
title: Pannelli di controllo
description: Usare gli elementi del Pannello di controllo per consentire agli utenti di configurare le funzionalità a livello di sistema ed eseguire attività correlate. I programmi con un'interfaccia utente devono invece essere configurati direttamente dall'interfaccia utente.
ms.assetid: 845325ef-9f1d-4aa7-a5b0-685fac74a9f8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 86226e3643f741d277c0e2864870a7e81c25614a6dd5ba2e01a05c67729c26d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117853547"
---
# <a name="control-panels"></a>Pannelli di controllo

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Usare gli elementi del Pannello di controllo per consentire agli utenti di configurare le funzionalità a livello di sistema ed eseguire attività correlate. I programmi con un'interfaccia utente devono invece essere configurati direttamente dall'interfaccia utente.

Con Pannello di controllo in Microsoft Windows, gli utenti possono configurare funzionalità a livello di sistema ed eseguire attività correlate. Esempi di configurazione delle funzionalità a livello di sistema includono l'installazione e la configurazione di hardware e software, la sicurezza, la manutenzione del sistema e la gestione degli account utente.

Il termine Pannello di controllo si riferisce all'intera Windows Pannello di controllo funzionalità. I singoli pannelli di controllo vengono definiti elementi del Pannello di controllo. Un elemento del Pannello di controllo viene considerato di primo livello quando è direttamente accessibile dal pannello di home page o da una pagina di categoria.

![Screenshot della categoria voce del pannello di controllo ](images/winenv-ctrl-panels-image1.png)

Elemento tipico del Pannello di controllo.

Il pannello di home page è il punto di ingresso principale per tutti gli elementi del Pannello di controllo. Elenca gli elementi in base alla categoria, insieme alle attività più comuni. Viene visualizzato quando gli utenti Pannello di controllo nella menu Start.

Una pagina delle categorie del pannello di controllo elenca gli elementi all'interno di una singola categoria, insieme alle attività più comuni. Viene visualizzato quando gli utenti selezionano un nome di categoria nella home page.

Gli elementi del Pannello di controllo vengono implementati [tramite flussi attività o](glossary.md) finestre delle proprietà. Per Windows Vista e versioni successive, i flussi attività sono l'interfaccia utente preferita.

**Sviluppatori:** Per informazioni su come creare elementi del Pannello di controllo, [vedere Pannello di controllo Items.](/previous-versions//bb776838(v=vs.85))

**Nota:** Le linee guida relative [alle finestre delle](win-property-win.md) proprietà sono presentate in un articolo separato.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere, prendi in considerazione queste domande:

-   **Lo scopo è quello di configurare le funzionalità a livello di sistema?** In caso contrario, usare un altro punto di integrazione. Rendere configurabili le funzionalità dell'applicazione direttamente dall'interfaccia utente usando le finestre di dialogo delle opzioni, anziché Pannello di controllo. Per le utilità che non vengono usate per l'installazione, la configurazione o le attività correlate (ad esempio la risoluzione dei problemi), usare il menu Start come punto di integrazione.
-   **La funzionalità a livello di sistema ha una propria interfaccia utente?** In tal caso, l'interfaccia utente è la posizione in cui gli utenti devono apportare modifiche. Ad esempio, un'utilità di backup del sistema deve essere configurata dalle relative opzioni di programma anziché da Pannello di controllo.
-   **Gli utenti dovranno modificare spesso la configurazione?** In questo caso( ad esempio, più volte alla settimana), prendere in considerazione soluzioni alternative, ad esempio oltre a usare Pannello di controllo. Ad esempio, l'Windows volume master può essere configurata direttamente dalla relativa icona nell'area di notifica. Alcune impostazioni possono essere configurate automaticamente. In Windows Explorer, ad esempio, la scheda Compatibilità per le proprietà dell'applicazione consente l'esecuzione di un'applicazione in modalità a 256 colori anziché richiedere agli utenti di modificare manualmente la modalità video.
-   **Gli utenti di destinazione sono professionisti IT?** In tal caso, usare [Microsoft Management Console snap-in MMC (System](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) Management Snap-in), progettato specificamente per le attività di gestione del sistema. In alcuni casi, la soluzione migliore consiste nell'avere sia un elemento del Pannello di controllo per utenti generici che uno snap-in MMC per i professionisti IT.

    ![Screenshot della finestra di gestione dei computer ](images/winenv-ctrl-panels-image2.png)

    In questo esempio lo snap-in MMC Utenti e gruppi locali fornisce la gestione degli utenti destinata ai professionisti IT. È più probabile che altri utenti usino l'elemento Account utente in Pannello di controllo.

-   **La funzionalità è una funzionalità OEM usata solo durante la configurazione iniziale del sistema?** In tal caso, usare il Windows Centro attività iniziali come punto di integrazione.

Gli elementi del Pannello di controllo sono necessari perché molte funzionalità a livello di sistema non hanno un punto di integrazione più ovvio o diretto. Tuttavia Pannello di controllo non deve essere visualizzato come "un'unica posizione" per tutte le impostazioni di configurazione. **I programmi con un'interfaccia utente devono essere configurati direttamente dall'interfaccia utente invece di usare gli elementi del Pannello di controllo.**

**Non corretto:**

![Screenshot dell'elemento opzioni Internet del Pannello di controllo ](images/winenv-ctrl-panels-image3.png)

In questo esempio, Windows Internet Explorer non deve essere rappresentato in Pannello di controllo, perché la propria interfaccia utente è un punto di integrazione migliore.

### <a name="create-a-new-control-panel-item-or-extend-an-existing-one"></a>Creare un nuovo elemento del Pannello di controllo o estenderne uno esistente?

Per decidere, prendi in considerazione queste domande:

-   **La funzionalità può essere espressa come attività che possono essere collegate a un elemento esistente ed estendibile del Pannello di controllo?** Gli elementi del Pannello di controllo seguenti sono estendibili: Bluetooth Dispositivi, Schermo, Internet, Tastiera, Mouse, Rete, Alimentazione, Sistema, Wireless (a Bluetooth).
-   **Le proprietà e le attività sostituiscono le funzionalità dell'elemento esistente del Pannello di controllo estendibile?** In tal caso, è necessario estendere l'elemento esistente del Pannello di controllo perché ciò comporta un'esperienza utente più semplice. In caso contrario, creare un nuovo elemento del Pannello di controllo.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

**Il Pannello di controllo è basato su una metafora reale.** Un pannello di controllo reale è una raccolta di controlli (manopole, interruttori, misuratori e schermi) usati per monitorare e controllare un dispositivo. Gli utenti di tali pannelli di controllo spesso necessitano di formazione per comprendere come usarli.

A differenza delle controparti reali, le Windows del pannello di controllo sono ottimizzate per gli utenti che si sono **registrati per la prima volta.** Gli utenti non eseguono la maggior parte delle attività del pannello di controllo molto spesso, quindi in genere non ricordano come eseguirle e devono in effetti rilearle ogni volta.

Per progettare un elemento del Pannello di controllo utile e facile da usare:

-   Assicurarsi che le proprietà siano necessarie.
-   Presentare le proprietà in termini di obiettivi utente anziché di tecnologia.
-   Presentare le proprietà al livello giusto.
-   Progettare pagine per attività specifiche.
-   Progettare pagine per utenti standard e amministratori protetti.

Quando si progettano e si valutano gli elementi da includere in Pannello di controllo, determinare le attività comuni eseguite dagli utenti e assicurarsi che vi sia un percorso chiaro per eseguire tali attività. Gli utenti eseguono in genere i tipi di attività seguenti con gli elementi del Pannello di controllo:

-   Configurazione iniziale
-   Modifiche poco frequenti (per la maggior parte delle impostazioni)
-   Modifiche frequenti (per alcune impostazioni importanti)
-   Rollback delle impostazioni a uno stato iniziale o precedente
-   Risoluzione dei problemi

**Se si fa una sola cosa...**

Progettare le pagine del pannello di controllo per attività specifiche e presentarle in termini di obiettivi dell'utente anziché di tecnologia.

## <a name="usage-patterns"></a>Modelli di utilizzo

Per gli elementi del Pannello di controllo, è possibile usare un flusso di attività o una finestra delle proprietà. Ecco i modelli di utilizzo:

### <a name="task-flow-patterns"></a>Modelli di flusso delle attività

Gli elementi del flusso di attività usano una pagina hub per presentare le scelte di alto livello e le pagine spoke per eseguire la configurazione effettiva.

**Pagine dell'hub**

-   Pagine dell'hub basate su attività. Queste pagine dell'hub presentano le attività usate più di frequente. Sono più utili per alcune attività di uso comune o importanti in cui gli utenti necessitano di altre indicazioni e spiegazioni. Le pagine dell'hub non hanno pulsanti di commit. Le pagine dell'hub basate su attività ibride hanno anche alcune proprietà o comandi direttamente su di esse. Le pagine dell'hub ibrido sono fortemente consigliate quando è più probabile che gli utenti usino Pannello di controllo per accedere a tali proprietà e comandi.
-   Pagine dell'hub basate su oggetti. Queste pagine dell'hub presentano gli oggetti disponibili usando un controllo di visualizzazione elenco. Sono più usati quando potrebbero essere presenti più oggetti. Le pagine dell'hub non hanno pulsanti di commit.

**Pagine spoke**

-   Pagine attività. Queste pagine spoke presentano un'attività o un passaggio in un'attività con un'istruzione principale specifica basata su attività. Sono più utili per le attività che traggono vantaggio da indicazioni e spiegazioni aggiuntive.
-   Pagine del modulo. Queste pagine spoke presentano una raccolta di proprietà e attività correlate basate su un'istruzione principale generale. Sono più utili per le funzionalità che hanno molte proprietà e traggono vantaggio da una presentazione diretta a pagina singola, ad esempio le proprietà avanzate.

### <a name="property-sheet-patterns"></a>Modelli della finestra delle proprietà

-   Le finestre delle proprietà sono più usate negli elementi legacy con molte impostazioni destinate agli utenti avanzati. I nuovi elementi possono ottenere lo stesso effetto con un flusso di attività usando il modello di pagina del modulo.

## <a name="guidelines"></a>Indicazioni

### <a name="property-sheet-control-panel-items"></a>Elementi del pannello di controllo della finestra delle proprietà

-   **Non usare le finestre delle proprietà per i nuovi elementi del pannello di controllo.** Usare invece i flussi di attività per creare un'esperienza semplice e usare completamente la funzionalità di categorizzazione e ricerca del pannello di controllo home page.

### <a name="task-flow-control-panel-items"></a>Elementi del pannello di controllo del flusso di attività

**Generale**

-   **Mantenere il contenuto e i controlli più importanti visibili senza scorrere.** Gli utenti non scorreranno per visualizzare il contenuto della pagina a meno che non ne abbia un motivo. È possibile rendere i pulsanti di commit sempre visibili inserendoli in [un'area dei comandi](glossary.md) anziché nell'area del contenuto. Non suddividere le pagine solo per evitare lo scorrimento.
    -   **È possibile scorrere verticalmente pagine lunghe,** purché i controlli più importanti siano visibili senza scorrere.
    -   **Non usare lo scorrimento orizzontale.** Riprogettare invece il contenuto della pagina e usare lo scorrimento verticale. Le pagine possono avere barre di scorrimento orizzontali solo se sono molto ristrette.
-   **Per spostarsi tra le pagine:**
    -   Usare [i collegamenti alle](glossary.md) attività per avviare un'attività.
    -   Usare i collegamenti alle attività o un pulsante Avanti per passare alla pagina successiva in un'attività in più passaggi.
    -   Usare i pulsanti di commit per completare un'attività.
    -   Usare il pulsante Indietro nella barra dei menu per tornare alle pagine visualizzate in precedenza. Non aggiungere un pulsante Indietro all'area dei comandi.
    -   Usare la barra degli indirizzi per tornare direttamente al pannello di controllo home page.
    -   Usare Vedere anche i collegamenti nel riquadro attività per passare alle pagine in altri elementi del Pannello di controllo. In caso contrario, la navigazione deve rimanere all'interno di un singolo elemento del Pannello di controllo.
-   **Inserire solo il pannello di home page nella barra degli indirizzi.** Facendo clic su questo collegamento si torna al pannello di home page, abbandonando qualsiasi lavoro in corso senza una [conferma.](https://msdn.microsoft.com/library/windows/desktop/aa511273.aspx)
-   **Non inserire un pulsante di comando Chiudi nelle pagine del pannello di controllo.** Gli utenti possono chiudere una finestra del pannello di controllo usando il pulsante Chiudi sulla barra del titolo.

**Pulsanti e collegamenti alle attività**

-   **Quando una pagina ha un piccolo set di opzioni fisse, usare i collegamenti alle attività anziché una combinazione di pulsanti di opzione e un pulsante Avanti.** In questo modo gli utenti possono selezionare una risposta con un solo clic.
-   È possibile inserire i collegamenti alle attività e i pulsanti nelle posizioni seguenti (in ordine di individuabilità):
    -   Area [dei comandi](glossary.md) (solo per i pulsanti di comando nelle pagine spoke).
    -   Area [del contenuto:](glossary.md)
        -   Pulsanti di comando
        -   Collegamenti alle attività
        -   Altri collegamenti
    -   Collegamenti nel riquadro [attività (solo](glossary.md) pagine hub).
-   **Basare la posizione dei collegamenti e dei pulsanti delle attività sull'importanza e sulla necessità di individuabilità.**
    -   **Inserire solo i pulsanti di commit nell'area dei comandi.**
    -   **Inserire le attività essenziali nell'area del contenuto.** I pulsanti di comando tendono a attirare maggiormente l'attenzione, quindi riservarli per i comandi che gli utenti devono visualizzare. Anche i collegamenti alle attività richiamano l'attenzione, ma non i pulsanti di comando.
    -   **Riservare il riquadro attività e i collegamenti semplici per le attività secondarie (meno importanti).** Il riquadro attività è l'area meno individuabile di una pagina attività e i collegamenti semplici non sono visibili come pulsanti di comando e collegamenti di attività.
-   Per i collegamenti alle attività presentati nell'area del contenuto:
    -   **Se sono presenti più di sette collegamenti, raggruppare i collegamenti in categorie.** Specificare le intestazioni per ogni gruppo.
    -   **Per meno di sette collegamenti, presentare i collegamenti in un singolo gruppo senza intestazione.**
-   **Presentare i collegamenti e i pulsanti delle attività in un ordine logico.** Elencare i collegamenti alle attività verticalmente, pulsanti di comando orizzontalmente.
-   All'interno **delle categorie, dividere i comandi in gruppi correlati.** Presentare i gruppi di attività posizionando i più comunemente usati per primi e all'interno di ogni gruppo, posizionare prima le attività usate più di frequente. **L'ordine risultante deve seguire approssimativamente la probabilità di utilizzo, ma anche avere un flusso logico.**
    -   **Eccezione:** I collegamenti alle attività che comportano l'esecuzione di tutti gli elementi devono essere posizionati per primi.
-   **Se sono presenti molti collegamenti di attività,** assegnare alle attività più importanti un aspetto più evidente usando un'icona di 24 x 24 pixel e due righe di testo. Per attività meno importanti, usare un'icona di 16x16 pixel o nessuna icona e una singola riga di testo del collegamento.

    ![Screenshot degli elementi con icone grandi e piccole ](images/winenv-ctrl-panels-image4.png)

    In questo esempio, ai comandi importanti viene assegnato un aspetto più evidente.

-   **Avere una netta separazione fisica tra i comandi usati di frequente e i comandi distruttivi.** In caso contrario, gli utenti potrebbero fare clic su comandi distruttivi accidentalmente. Potrebbe essere necessario riordinare i comandi per riunire i comandi distruttivi.
-   **Fornire il meccanismo per annullare i comandi direttamente nella pagina.** Gli utenti non devono spostarsi altrove per annullare un errore.
-   **Per i collegamenti alle attività, usare tutte le icone di collegamento alle attività predefinite o tutte le icone personalizzate.** Non combinarle. Prendere in considerazione l'uso di icone personalizzate solo se:
    -   Consentono agli utenti di comprendere le attività.
    -   Sono conformi agli standard [dell'icona Aero](vis-icons.md).
    -   Hanno un aspetto discreto.

**Finestre di dialogo**

Quando si usano flussi di attività, in genere si vuole che un'attività scorrono da una pagina all'altro all'interno di una singola finestra, ma le circostanze seguenti sono eccezioni. Usare le finestre di dialogo nelle circostanze seguenti:

-   Per richiedere agli utenti un nome utente e una password amministratore. Usare sempre la finestra di dialogo Gestione credenziali a questo scopo. Deve essere [modale.](glossary.md)
-   Per confermare un comando sul posto usando una finestra di dialogo attività o una finestra di messaggio. Deve essere modale.
-   Per ottenere input per i comandi sul posto, ad esempio per i comandi Nuovo, Aggiungi, Salva con nome, Rinomina e Stampa.

    ![Screenshot della finestra di dialogo Elimina percorsi di rete ](images/winenv-ctrl-panels-image5.png)

    In questo esempio il comando Elimina viene eseguito in una finestra di dialogo anziché in una pagina separata.

-   Per eseguire attività secondarie e autonome. [L'uso di una](glossary.md)finestra secondaria non modabile consente di eseguire tali attività in modo indipendente e all'esterno del flusso di attività principale.

### <a name="hub-pages"></a>Pagine dell'hub

**Generale**

-   Usare le pagine dell'hub basato su attività quando:
    -   **È presente un numero ridotto di attività di uso comune o importanti.**
    -   **La configurazione prevede uno o due oggetti** (ad esempio monitoraggi, tastiera, mouse, controller di gioco).
    -   **La configurazione si applica a livello di** sistema (ad esempio, data e ora, sicurezza, opzioni di risparmio energia).
-   Usare le pagine dell'hub basato su oggetti quando:
    -   **La configurazione può includere diversi oggetti** (ad esempio account utente, connessioni di rete, stampanti).
    -   **La configurazione si applica solo all'oggetto selezionato.**
-   **Non usare una pagina hub se l'elemento** del Pannello di controllo ha una singola pagina che contiene tutte le attività e le proprietà coinvolte.

**Elenchi di oggetti**

-   **Elencare gli elementi in un ordine logico.** Ordinare gli oggetti denominati in ordine alfabetico, i numeri in ordine numerico e le date in ordine cronologico.
-   Per gli hub basati su oggetti, fornire i comandi di visualizzazione oggetti nel riquadro attività se la possibilità di modificare la **visualizzazione è importante per le attività**. La possibilità di modificare le visualizzazioni è importante se sono presenti molti oggetti e la presentazione predefinita non funziona bene per tutti gli scenari. Gli utenti possono modificare la visualizzazione elenco anche se non sono presenti comandi espliciti tramite il menu di scelta rapida della visualizzazione elenco, ma è meno individuabile.

Per altre linee guida sulla presentazione di elenchi di oggetti, vedere [List Views](ctrl-list-views.md).

**Interazione**

-   **Non inserire i pulsanti di commit nelle pagine dell'hub.** Le pagine dell'hub sono fondamentalmente punti di avvio. Gli utenti non emettono mai il "commit" delle pagine dell'hub che non vengono mai eseguite con esse. I pulsanti di commit nelle pagine dell'hub confondono le attività avviate da un hub. Gli utenti si chiederanno se è necessario eseguire il commit di tali attività.
    -   **Eccezione:** Se la modifica di un'impostazione [richiede l'elevazione](glossary.md)dei privilegi, fornire un pulsante Applica con l'icona dello [shield di sicurezza](winenv-uac.md). Disabilitare il pulsante commit dopo aver applicato le modifiche.
-   **È consigliabile inserire le proprietà più utili direttamente nelle pagine dell'hub.** Queste pagine dell'hub ibrido sono fortemente consigliate quando è più probabile che gli utenti usino Pannello di controllo per accedere a tali proprietà.

    ![Screenshot della pagina dell'hub opzioni di risparmio energia ](images/winenv-ctrl-panels-image6.png)

    In questo esempio l'Opzioni risparmio energia pannello di controllo contiene le impostazioni più utili direttamente nella pagina dell'hub.

-   **Usare un modello di commit immediato per tutte le impostazioni nelle pagine dell'hub ibrido in modo che le modifiche siano apportate immediatamente.** Anche in questo caso, gli utenti non emettono mai il commit di una pagina dell'hub. Se un'impostazione richiede un pulsante di commit, non inserire il pulsante in una pagina dell'hub.
-   **È consigliabile inserire comandi semplici in "un passaggio" direttamente nelle pagine dell'hub invece di usare i collegamenti di navigazione.**
-   **Confermare i comandi sul posto i cui effetti non possono essere facilmente annullati.** Usare una [finestra di dialogo attività o](win-dialog-box.md) una finestra di [messaggio](glossary.md).

    ![Screenshot della finestra di dialogo conferma eliminazione ](images/winenv-ctrl-panels-image7.png)

    In questo esempio il comando Elimina viene confermato con una finestra di dialogo.

-   **Per le pagine dell'hub basato su attività, identificare ogni attività con un collegamento attività e un'icona.** È anche possibile fornire una descrizione facoltativa per ogni collegamento. Tuttavia, provare a rendere i collegamenti attività auto-esplicativi e fornire descrizioni facoltative solo ai collegamenti effettivamente necessari.

    ![Screenshot della pagina dell'hub delle prestazioni del computer ](images/winenv-ctrl-panels-image8.png)

    In questo esempio ogni attività ha un collegamento all'attività e un'icona.

-   **Per le pagine dell'hub basate su oggetti, il clic singolo seleziona gli oggetti e facendo doppio clic si seleziona un oggetto e si passa alla pagina predefinita.** La pagina predefinita è in genere una pagina delle proprietà o una pagina dell'hub basata su attività.
-   **Una pagina dell'hub basata su oggetti può passare a un hub basato su attività per gli oggetti selezionati.** Tuttavia, è consigliabile evitare questi hub secondari perché fanno in modo che un elemento del Pannello di controllo sia troppo indiretto.

**Riquadri attività**

Usare i riquadri attività per presentare collegamenti a comandi, visualizzazioni ed elementi correlati del Pannello di controllo.

-   Per i riquadri attività negli hub basati su attività, presentare i collegamenti nell'ordine seguente:
    -   **Comandi secondari**. Presentare le attività principali solo nell'area del contenuto. Usare il riquadro attività per le attività secondarie facoltative. Considerare un'attività primaria se gli utenti devono individuarla in scenari importanti. secondario se è accettabile per gli utenti non individuarlo.
    -   **Vedere anche**. Collegamenti facoltativi che passano agli elementi del Pannello di controllo correlati.
-   Per i riquadri attività negli hub basati su oggetti, presentare i collegamenti nell'ordine seguente:
    -   **Visualizzazioni di oggetti**. Collegamenti facoltativi utilizzati per controllare la presentazione degli oggetti .
    -   **Correzione dei comandi**. Comandi indipendenti degli oggetti attualmente selezionati.
    -   **Comandi contestuali**. I comandi che dipendono dagli oggetti attualmente selezionati e pertanto non vengono sempre visualizzati.
    -   **Vedere anche**. Collegamenti facoltativi che passano agli elementi del Pannello di controllo correlati.
-   **Non usare i riquadri attività nelle pagine spoke.** A differenza delle pagine hub, le pagine spoke devono essere incentrate sul completamento dell'attività. Non si vuole incoraggiare gli utenti a spostarsi prima del completamento.

**Vedere anche i collegamenti**

-   **Specificare Visualizza anche i collegamenti nel riquadro attività per consentire agli utenti di trovare gli elementi correlati del Pannello di controllo o l'elemento del Pannello di controllo corretto se è presente quello errato.** È probabile che il collegamento agli elementi che gli utenti associano all'elemento del Pannello di controllo.

    ![Screenshot dei collegamenti centro notifiche 'vedere anche' ](images/winenv-ctrl-panels-image9.png)

    In questo esempio, l'elemento del pannello di controllo centro notifiche si collega agli elementi del Pannello di controllo correlati.

-   **Creare un collegamento a una pagina di attività specifica se è ciò che gli utenti hanno maggiori probabilità di riconoscere.** In caso contrario, collegarsi all'intero elemento del Pannello di controllo. Usare il nome del pannello di controllo senza aggiungere la frase, pannello di controllo.

### <a name="spoke-pages"></a>Pagine spoke

**Generale**

-   **Usare le pagine delle attività per attività di uso comune o importanti in cui gli utenti necessitano di altre indicazioni e spiegazioni.**
-   **Usare le pagine del modulo per le funzionalità con molte impostazioni e che traggono vantaggio da una presentazione diretta a pagina singola.** Le attività ideali per tali pagine comportano in genere modifiche ovvie ad alcune semplici proprietà.
-   **Non usare i riquadri attività nelle pagine spoke.**

**Interazione**

-   **Provare a limitare le attività principali a una singola pagina.** Se sono necessarie più pagine, è possibile:
    -   **Usare pagine spoke intermedie per passaggi aggiuntivi o facoltativi.** Il commit delle pagine spoke intermedie viene eseguito dalla pagina spoke finale.
    -   **Usare finestre indipendenti per attività ausiliarie indipendenti.** Il commit delle finestre indipendenti viene eseguito autonomamente e indipendentemente dall'attività principale.

In questo modo, il significato dei pulsanti di commit per l'attività principale rimane chiaro e non ambiguo. Gli utenti devono avere sempre la certezza di capire a cosa si stanno impegnando.

-   **Non usare i collegamenti Vedere anche all'interno di un flusso di attività.** Questi collegamenti a elementi correlati, ma diversi, del Pannello di controllo. Anche se lo spostamento a un elemento diverso è accettabile nelle pagine dell'hub, non si trova nelle pagine spoke, perché questa operazione interrompe l'attività.
-   **Non usare pagine spoke per semplici input o conferme.** Usare invece le finestre di dialogo modali.

**Interazione (pagine spoke intermedie)**

-   **Usare i collegamenti alle attività o un pulsante Avanti per passare alla pagina successiva.** Il modo per procedere al passaggio successivo dovrebbe essere sempre ovvio.
-   **È possibile avere collegamenti di navigazione a passaggi di attività facoltativi.** Per evitare confusione quando gli utenti emettono il commit all'attività, tali pagine aggiuntive devono essere pagine intermedie all'interno dello stesso elemento del Pannello di controllo. Non devono avere pulsanti di commit, ma devono essere confermati quando viene eseguito il commit dell'attività principale.

**Interazione (pagine spoke finali)**

-   **Usare i pulsanti di commit per completare un'attività.** Usare un modello di [commit ritardato](glossary.md) per le pagine spoke, in modo che le modifiche non siano apportate fino a quando non viene eseguito il commit esplicito (se gli utenti si spostano usando Indietro, Chiudi o la barra degli indirizzi, le modifiche vengono abbandonate). I pulsanti di commit sono un indizio visivo che indica che l'utente sta per completare un'attività. Non usare collegamenti a questo scopo.
-   **Non confermare i pulsanti di commit (incluso Annulla).** Questa operazione può essere fastidiosa. Eccezioni:
    -   L'azione ha conseguenze significative e, se non è corretta, non è facilmente correggibile.
    -   L'azione può comportare una perdita significativa del tempo o dell'impegno dell'utente.
    -   L'azione è chiaramente incoerente con altre azioni.
-   **Non verificare se gli utenti abbandonano le modifiche** passando da Indietro, Chiudi o dalla barra degli indirizzi. Tuttavia, è possibile verificare se una navigazione potenzialmente non intenzionale può comportare una perdita significativa del tempo o dell'impegno dell'utente.
-   **Non usare collegamenti di comando o di navigazione** (inclusi i collegamenti Vedere anche). Nelle pagine spoke finali, gli utenti devono completare o annullare in modo esplicito l'attività. Gli utenti non devono essere invitati a spostarsi altrove, perché questa operazione probabilmente annullerebbe l'attività in modo implicito.
-   **Quando gli utenti completano o annullano un'attività, devono essere inviati nuovamente alla pagina dell'hub da cui è stata avviata l'attività.** Se tale pagina non è presente, chiudere invece la finestra del pannello di controllo. Non presupporre che le pagine spoke siano sempre avviate da un'altra pagina.
-   **Rimuovere le pagine di cui è stato eseguito** il commit non ancora Windows Explorer Back stack quando si riportano gli utenti alla pagina da cui è stata avviata l'attività. Gli utenti non dovrebbero mai visualizzare le pagine di cui è già stato eseguito il commit quando fanno clic sul pulsante Indietro. Gli utenti devono sempre apportare modifiche aggiuntive ripristinando completamente l'attività invece di fare clic su Indietro per modificare le pagine non recenti.
    -   **Sviluppatori:** È possibile rimuovere queste pagine non disponibili usando le API ITravelLog::FindTravelEntry() e ITravelLogEx::D eleteEntry().

**Pulsanti di commit**

**Nota:** I pulsanti Annulla vengono considerati pulsanti di commit.

-   **Confermare le attività usando pulsanti di commit che sono risposte specifiche all'istruzione principale, anziché etichette generiche, ad esempio OK.** Le etichette sui pulsanti di commit dovrebbero avere senso per conto proprio. Evitare di usare OK perché non è una risposta specifica all'istruzione principale e quindi più facile da fraintendere. Inoltre, OK viene in genere usato con le finestre di dialogo modali e implica erroneamente la chiusura della finestra dell'elemento del Pannello di controllo.
    -   **Eccezioni:**
        -   Usare OK per le pagine che non hanno impostazioni.
        -   Usare OK quando la risposta specifica è ancora generica, ad esempio Salva, Seleziona o Scegli, come quando si modifica un'impostazione specifica o una raccolta di impostazioni.
        -   Usare OK se la pagina contiene pulsanti di opzione che sono risposte all'istruzione principale. Per mantenere il modello di commit ritardato, non è possibile usare collegamenti di attività in una pagina spoke finale.

            ![Screenshot delle restrizioni Web con il pulsante OK ](images/winenv-ctrl-panels-image10.png)

            In questo esempio i pulsanti di opzione, non i pulsanti di commit, sono risposte all'istruzione principale.
-   **Specificare un pulsante Annulla per consentire agli utenti di abbandonare le modifiche in modo esplicito.** Anche se gli utenti possono abbandonare in modo implicito un'attività non confermando le modifiche, fornendo un pulsante Annulla è possibile farlo con maggiore attendibilità.
    -   **Eccezione:** Non specificare un pulsante Annulla per le attività in cui gli utenti non possono apportare modifiche. Il pulsante OK ha lo stesso effetto di Cancel in questo caso.
-   **Non usare i pulsanti Chiudi, Fine o Fine commit.** Questi pulsanti vengono in genere usati con le finestre di dialogo modali e implicano erroneamente la chiusura della finestra dell'elemento del Pannello di controllo. Gli utenti possono chiudere la finestra usando il pulsante Chiudi sulla barra del titolo. Inoltre, Done e Finish sono fuorvianti perché gli utenti vengono restituiti alla pagina da cui è stata avviata l'attività, quindi non sono effettivamente completati.
-   **Non disabilitare i pulsanti di commit.** In caso contrario, gli utenti devono dedurre perché i pulsanti di commit sono disabilitati. È meglio lasciare abilitati i pulsanti di commit e fornire un messaggio di errore utile ogni volta che si verifica un problema.
-   **Assicurarsi che i pulsanti di commit vengano visualizzati nella pagina senza scorrere.** Se la pagina è lunga, è possibile rendere i pulsanti di commit sempre visibili inserendoli in [un'area di](glossary.md)comando anziché nell'area del contenuto.

    ![Screenshot della finestra di dialogo riproduzione automatica ](images/winenv-ctrl-panels-image11.png)

    In questo esempio le dimensioni dell'area del contenuto sono illimitate, quindi i pulsanti di commit vengono inseriti nell'area dei comandi.

-   Allineare a destra i pulsanti di commit e usare questo ordine (da sinistra a destra): pulsanti di commit positivi, Annulla e Applica.

**Pulsanti di anteprima**

-   Assicurarsi che il pulsante Anteprima applichi ora le modifiche in sospeso, ma ripristina le impostazioni correnti se gli utenti si allontanano dalla pagina senza eseguire il **commit delle modifiche.**
-   **È possibile usare i pulsanti di anteprima in qualsiasi pagina spoke.** Le pagine dell'hub non necessitano di pulsanti di anteprima perché usano un [modello di commit immediato.](glossary.md)
-   **Provare a usare un pulsante Anteprima invece di un pulsante Applica per le pagine del pannello di controllo.** I pulsanti di anteprima sono più facili da comprendere per gli utenti e possono essere usati in qualsiasi pagina spoke.
-   **Fornire un pulsante Anteprima solo se nella pagina sono disponibili impostazioni (almeno una) con effetti che gli utenti possono visualizzare.** Gli utenti devono essere in grado di visualizzare in anteprima una modifica, valutarne la modifica e apportare altre modifiche in base a tale valutazione.
-   **Abilitare sempre il pulsante Anteprima.**

**Anteprime live**

Un elemento del pannello di controllo ha un'anteprima dinamica quando l'effetto delle modifiche in una pagina spoke può essere visualizzato immediatamente.

-   **È consigliabile usare l'anteprima dinamica per le impostazioni di visualizzazione quando:**
    -   L'effetto è ovvio, in genere perché si applica all'intero monitoraggio.
    -   L'effetto può essere applicato senza ritardi significativi.
    -   L'effetto è sicuro e può essere annullato facilmente.

        ![Screenshot della finestra di dialogo Modifica impostazioni colore ](images/winenv-ctrl-panels-image12.png)

        In questo esempio, l'effetto delle impostazioni Windows colore e aspetto viene visualizzato immediatamente. In questo modo, gli utenti possono apportare modifiche con il minimo sforzo.

-   **Usare Salva modifiche e Annulla per i pulsanti di commit.** "Salva modifiche" mantiene le impostazioni correnti, mentre Annulla ripristina le impostazioni originali. "Salva modifiche" viene usato invece di OK per chiarire che le modifiche in anteprima non sono ancora state applicate.
-   **Non specificare un pulsante Applica.** L'anteprima live rende non necessaria l'opzione Applica.
-   **Ripristinare eventuali modifiche se gli utenti si spostano usando** Indietro, Chiudi o la barra degli indirizzi. Per mantenere le modifiche, gli utenti devono eseguirvi il commit in modo esplicito.

**Applicare pulsanti**

-   Assicurarsi che il pulsante Applica applichi le modifiche in sospeso apportate dall'avvio dell'attività o dall'ultima applicazione, ma rimanga **nella pagina corrente.** Questa operazione consente agli utenti di valutare le modifiche prima di passare ad altre attività.
-   **Usare i pulsanti Applica solo nelle pagine spoke finali.** I pulsanti Applica non devono essere usati nelle pagine spoke intermedie per mantenere un modello di commit immediato.
    -   **Eccezione:** È possibile usare i pulsanti Applica in una pagina dell'hub ibrido se la modifica di un'impostazione richiede [l'elevazione dei privilegi](glossary.md). Per altri dettagli, vedere Interazione [tra le pagine dell'hub.](#hub-pages)
-   **Specificare un pulsante Applica solo se nella pagina sono presenti impostazioni (almeno una) con effetti che gli utenti possono valutare in modo significativo.** In genere, i pulsanti Applica vengono usati quando le impostazioni apportano modifiche visibili. Gli utenti devono essere in grado di applicare una modifica, valutare la modifica e apportare altre modifiche in base a tale valutazione.
-   **Abilitare il pulsante Applica solo in caso di modifiche in sospeso.** In caso contrario, disabilitarlo.
-   **Assegnare "A" come chiave di accesso.**

### <a name="control-panel-integration"></a>Integrazione del pannello di controllo

Per integrare l'elemento del pannello di controllo con Windows, è possibile:

-   **Registrare l'elemento del** pannello di controllo (inclusi il nome, la descrizione e l'icona) in modo che Windows ne sia a conoscenza.
-   Se l'elemento del pannello di controllo è di primo livello (vedere di seguito):
    -   Associarlo alla pagina **della categoria appropriata.**
    -   **Fornire collegamenti alle attività (inclusi il nome,** la descrizione, le parole chiave e la riga di comando) per indicare le attività primarie e consentire agli utenti di passare direttamente alle attività.
-   **Fornire termini di ricerca** per consentire agli utenti di trovare i collegamenti alle attività usando la Pannello di controllo di ricerca.

    Si noti che è possibile fornire queste informazioni solo per singoli elementi del Pannello di controllo che non è possibile aggiungere o modificare per gli elementi esistenti del Pannello di controllo che si estendono.

**Pagine delle categorie**

-   **Aggiungere l'elemento del pannello di controllo a una pagina di categoria solo se:**

    -   La maggior parte degli utenti ne ha bisogno. Esempio: Centro connessioni di rete e condivisione
    -   Viene usato molte volte. Esempio: Sistema
    -   Fornisce funzionalità importanti che non vengono esposte altrove. Esempio: Stampanti

    Gli elementi del pannello di controllo che soddisfano questi criteri vengono definiti elementi di primo livello.

-   **Non aggiungere l'elemento del Pannello di controllo a una pagina di categoria se:**

    -   Viene usato raramente o usato per l'installazione una sola volta. Esempio: Centro attività iniziali
    -   È destinato a utenti esperti o professionisti IT. Esempio: Gestione colori
    -   Non si applica alla configurazione hardware o software corrente. Esempio: Windows SideShow (se non supportato dall'hardware corrente).

    La rimozione di tali elementi del Pannello di controllo dalle pagine delle categorie semplifica la ricerca degli elementi di primo livello. Dato l'utilizzo, questi elementi del Pannello di controllo sono sufficientemente individuabili tramite punti di ingresso contestuali o di ricerca.

-   **Associare l'elemento del Pannello di controllo di primo livello alla categoria in cui gli utenti hanno maggiori probabilità di cercarlo.** Questa decisione deve basarsi sui test utente.
-   **È consigliabile associare l'elemento del Pannello di controllo di primo livello anche alla seconda categoria più probabile.** È consigliabile associare un elemento del Pannello di controllo a due categorie se è probabile che gli utenti debbano cercare le attività principali in più di una posizione.
-   **Non associare l'elemento del Pannello di controllo a più di due categorie.** Il valore della categorizzazione viene compromesso se gli elementi del Pannello di controllo vengono visualizzati in diverse categorie.

**Collegamenti alle attività**

-   **Associare l'elemento del Pannello di controllo alle attività principali.** È possibile visualizzare fino a cinque attività in una pagina Categoria, ma vengono usate attività aggiuntive per la ricerca nel Pannello di controllo. Usare la stessa formulazione utilizzata per i collegamenti alle attività, rimuovendo eventualmente alcune parole per rendere più concisi i collegamenti alle attività.
-   **Preferisci che i collegamenti alle attività conducano a posizioni diverse nell'elemento del Pannello di controllo.** La presenza di più collegamenti alla stessa posizione può generare confusione.

**Termini di ricerca**

-   **Registrare i termini di ricerca per l'elemento del Pannello di controllo che gli utenti probabilmente useranno per descriverlo.** Questi termini di ricerca devono includere:

    -   Funzionalità o oggetti configurati.
    -   Attività principali.

    Questi termini di ricerca devono essere basati sui test utente.

-   **Includere anche i sinonimi comuni per questi termini di ricerca.** Ad esempio, il monitoraggio e la visualizzazione sono sinonimi, quindi è necessario includere entrambe le parole.
-   **Includere ortografie o interruzioni di parola alternative.** Ad esempio, gli utenti potrebbero cercare un sito Web e un sito Web. È consigliabile fornire anche errori di ortografia comuni.
-   **Si considerino forme singolari e sostantivi plurali.** La funzionalità di ricerca del pannello di controllo non cerca automaticamente entrambi i moduli. specificare i moduli per cui gli utenti potrebbero eseguire la ricerca.
-   **Usare semplici verbi presenti.** Se si registra Connetti come termine di ricerca, la funzionalità di ricerca non cerca automaticamente le connessioni, la connessione e la connessione.
-   **Non è necessario preoccuparsi del caso.** La funzionalità di ricerca non fa distinzione tra maiuscole e minuscole.

### <a name="standard-users-and-protected-administrators"></a>Utenti standard e amministratori protetti

**Molte impostazioni richiedono privilegi di amministratore per la modifica.** Se un processo richiede privilegi di amministratore, Windows Vista [](glossary.md) e versioni successive richiedono agli utenti [standard](glossary.md) e agli amministratori protetti di elevare i privilegi in modo esplicito. In questo modo si impedisce l'esecuzione di codice dannoso con privilegi di amministratore.

Per altre informazioni ed esempi, vedere [Controllo dell'account utente.](winenv-uac.md)

### <a name="schemes-and-themes"></a>Schemi e temi

Uno schema è una raccolta denominata di impostazioni visive. Un tema è una raccolta denominata di impostazioni nel sistema. Esempi di schemi e temi includono Display, Mouse, Telefono e Modem, Opzioni risparmio energia e Opzioni audio e audio.

-   **Consentire agli utenti di creare schemi quando:**

    -   **È probabile che gli utenti cambino le impostazioni.**
    -   **È molto probabile che gli utenti cambino le impostazioni come raccolta.**

    Gli schemi sono utili quando gli utenti si verificano in un ambiente diverso, ad esempio una posizione fisica diversa (paese/area geografica, fuso orario); utilizzando il computer in una situazione diversa (su batterie, ancorate/disancosate); o usando il computer per una funzione diversa (presentazioni, riproduzione di video).

-   **Specificare almeno uno schema predefinito.** Lo schema predefinito deve essere ben denominato e si applica alla maggior parte degli utenti nella maggior parte dei casi. Gli utenti non devono creare uno schema personalizzato.
-   **Fornire un'anteprima** o un altro meccanismo in modo che gli utenti possano visualizzare le impostazioni all'interno dello schema.

    ![Screenshot della finestra di dialogo di personalizzazione ](images/winenv-ctrl-panels-image13.png)

    In questo esempio l'elemento del Pannello di controllo Personalizzazione mostra un'anteprima delle impostazioni relative al desktop e all'aspetto.

-   **Specificare i comandi Salva con nome ed Elimina.** Un comando di ridenominazione non è necessario che gli utenti possano rinominare gli schemi salvando con il nome desiderato ed eliminando lo schema originale.
-   Se le impostazioni non possono essere applicate senza uno schema, non consentire agli **utenti di eliminare tutti gli schemi.** Gli utenti non devono creare uno schema personalizzato.
-   Se gli schemi non sono completamente indipendenti (ad esempio, le combinazioni di risparmio energia dipendono dalla modalità di funzionamento corrente del portatile), assicurarsi che sia disponibile un modo semplice per modificare le impostazioni che si applicano a tutti **gli schemi.** Ad esempio, con le combinazioni di risparmio energia, assicurarsi che gli utenti possano impostare cosa accade quando il lunodico di un computer portatile viene chiuso in un'unica posizione.

### <a name="miscellaneous"></a>Varie

-   **Usare Pannello di controllo per le funzionalità che sostituiscono o estendono le Windows esistenti.** Gli elementi del Pannello di controllo seguenti sono estendibili: Bluetooth Dispositivi, Schermo, Internet, Tastiera, Mouse, Rete, Alimentazione, Sistema, Wireless (a Bluetooth).

### <a name="default-values"></a>Valori predefiniti

-   **Le impostazioni all'interno di un elemento del Pannello di controllo devono riflettere lo stato corrente della funzionalità.** In caso contrario, sarebbe fuorviante e potrebbe causare risultati indesiderati. Ad esempio, se le impostazioni riflettono le raccomandazioni ma non lo stato corrente, gli utenti potrebbero fare clic su Annulla invece di apportare modifiche, pensare che non sono necessarie modifiche.
-   **Scegliere lo stato iniziale più sicuro (per evitare la perdita di dati o l'accesso al sistema) e quello più sicuro.** Si supponga che la maggior parte degli utenti non modificherà le impostazioni.
-   **Se la sicurezza e la sicurezza non sono fattori, scegliere lo stato iniziale più probabile o conveniente.**

## <a name="text"></a>Testo

### <a name="item-names"></a>Nomi degli elementi

-   **Scegliere un nome descrittivo che comunichi chiaramente e differenzia le attività dell'elemento del Pannello di controllo.** La maggior parte dei nomi Windows la funzionalità o l'oggetto da configurare e vengono visualizzati nella visualizzazione classica del pannello di controllo home page.
-   **Non includere le parole "Impostazioni", "Opzioni", "Proprietà" o "Configurazione" nel nome.** Ciò è implicito e la sua osunzione rende più semplice l'analisi da parte degli utenti.

    **Non corretto:**

    Opzioni di accessibilità

    Modem Impostazioni

    Opzioni risparmio energia

    Opzioni internazionali e della lingua

    **Corretto:**

    Accessibilità

    Modem

    Elettricità

    Lingue e formati internazionali

    Negli esempi corretti le parole non necessarie vengono rimosse.

-   **Se l'elemento del Pannello di controllo configura le funzionalità correlate, elencare solo le funzionalità necessarie per identificare l'elemento ed elencare le funzionalità che più probabilmente verranno riconosciute o usate per prime.**

    **Non corretto:**

    Opzioni cartella

    Telefono e modem

    **Corretto:**

    File e cartelle

    Modem

    Negli esempi corretti, le funzionalità principali degli elementi del Pannello di controllo vengono sottolineate.

-   Usare [l'uso di maiuscole e minuscole in stile titolo.](glossary.md)

### <a name="page-titles"></a>Titoli delle pagine

**Nota:** Come per tutte le finestre di Explorer, i titoli delle pagine del Pannello di controllo vengono visualizzati sulla barra [degli indirizzi,](glossary.md)ma non sulla barra del titolo.

-   **Per le pagine dell'hub, usare il nome dell'elemento del Pannello di controllo.**
-   **Per le pagine spoke, usare un riepilogo conciso dello scopo della pagina.** Usare l'istruzione principale della pagina se è concisa. in caso contrario, usare una rielimentazione concisa dell'istruzione principale.

    ![Screenshot della finestra di dialogo Opzioni risparmio energia ](images/winenv-ctrl-panels-image6.png)

    In questo esempio viene Opzioni risparmio energia per il titolo della pagina anziché per l'istruzione principale.

-   Usare l'uso di maiuscole e minuscole in stile titolo.

### <a name="task-link-text"></a>Testo collegamento attività

Le linee guida seguenti si applicano ai collegamenti alle pagine delle attività, ad esempio i collegamenti alle attività della pagina Categoria e Vedere anche i collegamenti.

-   **Scegliere nomi di attività concisi che comunicano chiaramente e differenziano l'attività.** Gli utenti non devono capire cosa significa realmente l'attività o in che modo differisce da altre attività.

    **Non corretto:**

    Modificare le impostazioni di visualizzazione

    **Corretto:**

    Risoluzione dello schermo

    Nell'esempio corretto, la formulazione trasmette una maggiore precisione.

-   **Mantenere una lingua simile tra i collegamenti alle attività e le pagine a cui puntano.** Gli utenti non devono essere sorprese dalla pagina visualizzata da un collegamento.
-   **Per le pagine di attività, progettare l'istruzione principale, i pulsanti di commit e i collegamenti alle attività come set di testo correlato.**
    

    | Esempio                             |    Istruzione                                                   |
    |------------------------------|-------------------------------------------------------|
    | Collegamento attività:<br/>        | Connettersi a una rete wireless<br/>              |
    | Istruzione principale:<br/> | Scegliere una rete a cui connettersi<br/>             |
    | Pulsante Commit:<br/>    | Connettere<br/>                                    |
    | Collegamento attività:<br/>        | Configurare il controllo genitori<br/>                   |
    | Istruzione principale:<br/> | Scegliere un utente e configurare Il controllo genitori<br/> |
    | Pulsante Commit:<br/>    | Applicare il controllo genitori<br/>                     |
    | Collegamento attività:<br/>        | Risolvere i conflitti di sincronizzazione<br/>                |
    | Istruzione principale:<br/> | Come si vuole risolvere il conflitto?<br/>  |
    | Pulsante Commit:<br/>    | Risolvi<br/>                                    |

    

     

    Questi esempi illustrano la relazione tra il testo del collegamento all'attività, l'istruzione principale e il testo del pulsante di commit.

-   Anche se le attività spesso iniziano con verbi, è consigliabile omettere il verbo nelle pagine Categoria se si tratta di un verbo generico correlato alla configurazione che non consente di comunicare **l'attività.**

    **Verbi specifici e utili:**

    Add

    Controllo

    Connettere

    Copia

    Create

    Elimina

    Disconnetti

    Installazione

    Rimuovi

    Configurazione

    Inizia

    Stop

    Risolvere problemi

    **Verbi generici e inutili:**

    Regolare

    Modifica

    Choose

    Configurare

    Modifica

    Gestire

    Apri

    Seleziona

    Impostazione

    Seleziona

    Mostra

    Visualizzazione

-   **Se l'attività configura diverse funzionalità correlate, elencare solo le funzionalità rappresentative del set.** Omettere i dettagli che possono essere immediatamente dedosi.

    **Non corretto:**

    Volume voce, disattivazione dell'audio, icona del volume

    Altoparlanti, microfoni, MIDI e schemi audio

    **Corretto:**

    Volume del parlante

    Altoparlanti e microfoni

    Negli esempi corretti vengono fornite solo le funzionalità rappresentative nel collegamento all'attività.

-   **È consigliabile formulare le attività in termini di tecnologia solo se lo farebbe anche gli utenti di destinazione.**

    **Non corretto:**

    Connectoid

    Profondità dei pixel

    dpi

    **Corretto:**

    Stampanti

    Scanner

    Mouse

    Gli esempi corretti sono termini basati sulla tecnologia che gli utenti di destinazione probabilmente useranno, mentre gli esempi non corretti non lo sono.

-   Usare sostantivi plurali solo se il sistema può supportare più di uno.
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Non usare punteggiatura finale.

### <a name="main-instructions"></a>Istruzioni principali

-   **Per la pagina dell'hub, usare l'istruzione principale per spiegare l'obiettivo dell'utente con l'elemento del pannello di controllo.** L'istruzione principale dovrebbe aiutare gli utenti a determinare se è stato selezionato l'elemento del pannello di controllo giusto. Tenere presente che gli utenti potrebbero aver selezionato l'elemento del Pannello di controllo per errore e che in realtà stanno cercando impostazioni che fanno parte di un altro elemento del Pannello di controllo.

    **Esempi:**

    Mantenere il computer sicuro e aggiornato

    Ottimizzare il computer in modo da semplificare la visualizzazione, l'ascolto e il controllo

-   **Per le pagine spoke, usare l'istruzione principale per spiegare cosa fare nella pagina.** L'istruzione deve essere un'istruzione specifica, una direzione imperativa o una domanda. Le buone istruzioni comunicano l'obiettivo dell'utente con la pagina anziché concentrarsi esclusivamente sui meccanismi di modifica.

    **Non corretto:**

    Selezionare un'attività di notifica

    **Corretto:**

    Indicare come gestire le informazioni in ingresso

    La versione corretta comunica meglio l'obiettivo raggiunto dalla pagina.

-   **Usare verbi specifici quando possibile.** Verbi specifici sono più significativi per gli utenti rispetto a quelli generici.
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   **Non includere i periodi finali se l'istruzione è un'istruzione .** Se l'istruzione è una domanda, includere un punto interrogativo finale.

### <a name="supplemental-instructions"></a>Istruzioni supplementari

-   **Per la pagina dell'hub, usare l'istruzione supplementare facoltativa per spiegare ulteriormente lo scopo dell'elemento del Pannello di controllo.**
-   **Per le pagine spoke, usare l'istruzione supplementare facoltativa per presentare informazioni aggiuntive utili per comprendere o usare la pagina.** È possibile fornire informazioni più dettagliate e definire la terminologia.
-   Usare frasi complete e lettere [maiuscole in stile frase.](glossary.md)

### <a name="page-text"></a>Testo della pagina

-   **Non rievalutare l'istruzione principale nell'area del contenuto.**
-   **Usare la parola "page" per fare riferimento alla pagina stessa.**
-   **Usare la seconda persona (l'utente) per indicare** agli utenti cosa fare nell'area principale dell'istruzione e del contenuto. Spesso la seconda persona è implicita.

    **Esempio:**

    Scegliere le immagini da stampare.

-   **Usare la prima persona (I, me, my)** per consentire agli utenti di indicare all'elemento del Pannello di controllo cosa fare nell'area del contenuto che risponde all'istruzione principale.

    **Esempio:**

    Stampare le foto sulla fotocamera.

### <a name="task-links"></a>Collegamenti alle attività

-   **Scegliere un testo di collegamento conciso che comunichi chiaramente e differenzia le operazioni del collegamento all'attività.** Deve essere auto-esplicativo e corrispondere all'istruzione principale. Gli utenti non devono capire cosa significa effettivamente il collegamento o in che modo differisce dagli altri collegamenti.
-   **Avviare sempre i collegamenti alle attività con un verbo.**
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Non usare punteggiatura finale.
-   **Se il collegamento all'attività richiede un'ulteriore spiegazione,** fornire la spiegazione in un controllo di testo separato usando frasi complete e terminando la punteggiatura. Tuttavia, aggiungere tali spiegazioni solo quando necessario, non aggiungere spiegazioni a tutti i collegamenti di attività perché un altro collegamento attività ne richiede uno.

Per altre informazioni ed esempi, vedere [Collegamenti.](ctrl-command-links.md)

### <a name="commit-buttons"></a>Pulsanti di commit

-   **Usare etichette specifiche dei pulsanti di commit che hanno senso e che corrispondono all'istruzione principale.** Idealmente, gli utenti non devono leggere altro per comprendere l'etichetta. È molto più probabile che gli utenti leggono le etichette dei pulsanti di comando rispetto al testo statico.
-   **Avviare sempre le etichette dei pulsanti di commit con un verbo.**
-   **Non usare Chiudi, Fine o Fine.** Queste etichette dei pulsanti sono più adatte per altri tipi di finestre.
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Non usare punteggiatura finale.
-   Assegnare una chiave [di accesso univoca](glossary.md).
    -   **Eccezione:** Non assegnare i tasti di scelta ai pulsanti Annulla, perché ESC è la chiave di accesso. In questo modo le altre chiavi di accesso sono più facili da assegnare.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle pagine home page o categoria del pannello di controllo:

-   Nella documentazione dell'utente fare riferimento Pannello di controllo, usando l'uso di maiuscole/minuscole in stile titolo e omettendo un articolo definito in precedenza.

    **Esempio:**

    In Pannello di controllo aprire Centro **sicurezza.**

-   Nella programmazione e in altri documenti tecnici, fare riferimento alla pagina delle categorie home page e del pannello di controllo, senza lettere maiuscole. Un articolo definito in precedenza è facoltativo.

Per gli elementi del Pannello di controllo:

-   Quando si fa riferimento a un singolo elemento del Pannello di controllo, usare "control panel item name in Pannello di controllo" (Nome dell'elemento del pannello di controllo in Pannello di controllo) o in genere \[ "Pannello di controllo elemento" nella documentazione dell'utente. \] Non usare applet, programma o pannello di controllo per fare riferimento a singoli elementi del Pannello di controllo.
-   Quando si fa riferimento alla pagina hub di un elemento del Pannello di controllo, usare "pagina principale \[ del nome dell'elemento del pannello di \] controllo".
-   Quando possibile, formattare il nome del pannello di controllo usando il testo in grassetto. In caso contrario, inserire il nome tra virgolette solo se necessario per evitare confusione.

Esempi:

-   In Pannello di controllo aprire **Controllo genitori.**
-   Tornare alla pagina principale **controllo genitori.**

