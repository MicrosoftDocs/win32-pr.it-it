---
title: Pannelli di controllo
description: Utilizzare gli elementi del pannello di controllo per consentire agli utenti di configurare le funzionalità a livello di sistema ed eseguire attività correlate. I programmi che dispongono di un'interfaccia utente devono essere configurati direttamente dall'interfaccia utente.
ms.assetid: 845325ef-9f1d-4aa7-a5b0-685fac74a9f8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dde41544f2bf8c920365f160f71dce7e88d89b81
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103968821"
---
# <a name="control-panels"></a>Pannelli di controllo

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Utilizzare gli elementi del pannello di controllo per consentire agli utenti di configurare le funzionalità a livello di sistema ed eseguire attività correlate. I programmi che dispongono di un'interfaccia utente devono essere configurati direttamente dall'interfaccia utente.

Con il pannello di controllo in Microsoft Windows, gli utenti possono configurare le funzionalità a livello di sistema ed eseguire attività correlate. Esempi di configurazione delle funzionalità a livello di sistema includono l'installazione e la configurazione di hardware e software, la sicurezza, la manutenzione del sistema e la gestione degli account utente.

Il termine Pannello di controllo si riferisce all'intera funzionalità del pannello di controllo di Windows. I singoli pannelli di controllo vengono definiti elementi del pannello di controllo. Un elemento del pannello di controllo è considerato di primo livello quando è accessibile direttamente dal pannello di controllo home page o da una pagina di categoria.

![screenshot della categoria voce del pannello di controllo ](images/winenv-ctrl-panels-image1.png)

Un tipico elemento del pannello di controllo.

Il pannello di controllo home page è il punto di ingresso principale per tutti gli elementi del pannello di controllo. Elenca gli elementi in base alla relativa categoria, insieme alle attività più comuni. Viene visualizzato quando gli utenti fanno clic su pannello di controllo nel menu Start.

Una pagina di categoria del pannello di controllo Elenca gli elementi all'interno di una singola categoria, insieme alle attività più comuni. Viene visualizzato quando gli utenti fanno clic sul nome di una categoria nel home page.

Gli elementi del pannello di controllo vengono implementati mediante [flussi attività](glossary.md) o finestre delle proprietà. Per Windows Vista e versioni successive, i flussi attività rappresentano l'interfaccia utente preferita.

**Sviluppatori:** Per informazioni su come creare elementi del pannello di controllo, vedere [elementi del pannello di controllo](/previous-versions//bb776838(v=vs.85)).

**Nota:** Le linee guida correlate alle [finestre delle proprietà](win-property-win.md) vengono presentate in un articolo separato.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere, prendi in considerazione queste domande:

-   **Lo scopo è quello di configurare le funzionalità a livello di sistema?** In caso contrario, usare un altro punto di integrazione. Rendere le funzionalità dell'applicazione configurabili direttamente dall'interfaccia utente usando le finestre di dialogo delle opzioni, anziché usare il pannello di controllo. Per le utilità che non vengono usate per l'installazione, la configurazione o le attività correlate (ad esempio per la risoluzione dei problemi), usare il menu Start come punto di integrazione.
-   **La funzionalità a livello di sistema ha una propria interfaccia utente?** In tal caso, l'interfaccia utente è la posizione in cui gli utenti devono apportare modifiche. Un'utilità di backup di sistema, ad esempio, deve essere configurata dalle opzioni di programma anziché dal pannello di controllo.
-   **Gli utenti dovranno modificare la configurazione spesso?** In tal caso, ad esempio, più volte alla settimana, è possibile prendere in considerazione soluzioni alternative, forse oltre a usare il pannello di controllo. Ad esempio, l'impostazione volume master di Windows può essere configurata direttamente dalla relativa icona nell'area di notifica. Alcune impostazioni possono essere configurate automaticamente. In Esplora risorse, ad esempio, la scheda compatibilità per le proprietà dell'applicazione consente l'esecuzione di un'applicazione in modalità colore 256 anziché richiedere agli utenti di modificare la modalità video manualmente.
-   **I professionisti IT sono utenti di destinazione?** In tal caso, utilizzare uno snap-in di [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) , progettato in modo specifico per le attività di gestione del sistema. In alcuni casi, la soluzione migliore consiste nel disporre di un elemento del pannello di controllo per gli utenti generali e di uno snap-in MMC per i professionisti IT.

    ![screenshot della finestra di gestione computer ](images/winenv-ctrl-panels-image2.png)

    In questo esempio, lo snap-in MMC utenti e gruppi locale fornisce la gestione degli utenti destinata ai professionisti IT. È più probabile che altri utenti usino l'elemento account utente nel pannello di controllo.

-   **La funzionalità è una funzionalità OEM utilizzata solo durante la configurazione iniziale del sistema?** In tal caso, utilizzare il centro di benvenuto di Windows come punto di integrazione.

Gli elementi del pannello di controllo sono necessari perché molte funzionalità a livello di sistema non dispongono di un punto di integrazione più chiaro o diretto. Tuttavia, il pannello di controllo non deve essere visualizzato come "un'unica posizione" per tutte le impostazioni di configurazione. **I programmi che dispongono di un'interfaccia utente devono essere configurati direttamente dall'interfaccia utente anziché dagli elementi del pannello di controllo.**

**Non corretto:**

![screenshot dell'elemento Opzioni Internet del pannello di controllo ](images/winenv-ctrl-panels-image3.png)

In questo esempio, Windows Internet Explorer non deve essere rappresentato nel pannello di controllo, perché la propria interfaccia utente è un punto di integrazione migliore.

### <a name="create-a-new-control-panel-item-or-extend-an-existing-one"></a>Creare un nuovo elemento del pannello di controllo o estenderne uno esistente?

Per decidere, prendi in considerazione queste domande:

-   **La funzionalità può essere espressa come attività in grado di collegarsi a un elemento del pannello di controllo esistente e estensibile?** Gli elementi del pannello di controllo seguenti sono estendibili: dispositivi Bluetooth, schermo, Internet, tastiera, mouse, rete, alimentazione, sistema, wireless (infrarossi).
-   **Le proprietà e le attività sostituiscono le funzionalità dell'elemento del pannello di controllo estendibile esistente?** In tal caso, è necessario estendere l'elemento del pannello di controllo esistente perché ciò comporta un'esperienza utente più semplice. In caso contrario, creare un nuovo elemento del pannello di controllo.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

**Il concetto di pannello di controllo si basa su una metafora del mondo reale.** Un pannello di controllo reale è una raccolta di controlli (manopole, commutatori, misuratori e visualizzazioni) usati per monitorare e controllare un dispositivo. Gli utenti di tali pannelli di controllo necessitano spesso di formazione per capire come usarli.

Diversamente dalle controparti reali, le **progettazioni del pannello di controllo di Windows sono ottimizzate per i primi utenti.** Gli utenti non eseguono la maggior parte delle attività del pannello di controllo molto spesso, quindi non si ricordano in genere come eseguirle ed è necessario riapprenderle ogni volta.

Per progettare un elemento del pannello di controllo utile e facile da usare:

-   Verificare che le proprietà siano necessarie.
-   Presentare le proprietà in termini di obiettivi utente anziché della tecnologia.
-   Presentare le proprietà al livello corretto.
-   Progetta le pagine per attività specifiche.
-   Progettare pagine per utenti standard e amministratori protetti.

Quando si progettano e si valutano gli elementi da includere nel pannello di controllo, determinare le attività comuni eseguite dagli utenti e assicurarsi che esista un percorso chiaro per eseguire tali attività. Gli utenti in genere eseguono i seguenti tipi di attività con gli elementi del pannello di controllo:

-   Configurazione iniziale
-   Modifiche non frequenti (per la maggior parte delle impostazioni)
-   Modifiche frequenti (per alcune impostazioni importanti)
-   Rollback delle impostazioni a uno stato iniziale o precedente
-   Risoluzione dei problemi

**Se si esegue una sola operazione...**

Progettare le pagine del pannello di controllo per attività specifiche e presentarle in termini di obiettivi utente anziché tecnologia.

## <a name="usage-patterns"></a>Modelli di utilizzo

Per gli elementi del pannello di controllo, è possibile usare un flusso attività o una finestra delle proprietà. Ecco i modelli di utilizzo:

### <a name="task-flow-patterns"></a>Modelli di flusso di attività

Gli elementi del flusso di attività usano una pagina Hub per presentare le scelte generali e le pagine spoke per eseguire la configurazione effettiva.

**Pagine hub**

-   Pagine dell'hub basate su attività. Queste pagine dell'hub presentano le attività più comuni. Sono particolarmente utili per alcune attività di uso comune o importanti, in cui gli utenti necessitano di altre indicazioni e spiegazioni. Le pagine hub non dispongono di pulsanti di commit. Le pagine hub basate su attività ibride dispongono anche di alcune proprietà o comandi direttamente su di essi. Le pagine dell'Hub ibrido sono fortemente consigliate quando è più probabile che gli utenti usino il pannello di controllo per accedere a tali proprietà e comandi.
-   Pagine dell'hub basate su oggetti. Queste pagine dell'hub presentano gli oggetti disponibili usando un controllo di visualizzazione elenco. È consigliabile usarli quando possono essere presenti più oggetti. Le pagine hub non dispongono di pulsanti di commit.

**Pagine spoke**

-   Pagine delle attività. Queste pagine spoke presentano un'attività o un passaggio in un'attività con un'istruzione principale specifica basata su attività. Sono particolarmente utili per le attività che traggono vantaggio da indicazioni e spiegazioni aggiuntive.
-   Pagine del modulo. Queste pagine spoke presentano una raccolta di proprietà e attività correlate basate su un'istruzione principale generale. Sono particolarmente utili per le funzionalità che hanno molte proprietà e traggono vantaggio da una presentazione diretta a pagina singola, ad esempio proprietà avanzate.

### <a name="property-sheet-patterns"></a>Modelli della finestra delle proprietà

-   Le finestre delle proprietà vengono usate in modo ottimale negli elementi legacy con molte impostazioni destinate a utenti avanzati. I nuovi elementi possono ottenere lo stesso effetto con un flusso attività usando il modello di pagina form.

## <a name="guidelines"></a>Indicazioni

### <a name="property-sheet-control-panel-items"></a>Elementi del pannello di controllo della finestra delle proprietà

-   **Non utilizzare le finestre delle proprietà per i nuovi elementi del pannello di controllo.** Usare invece i flussi attività per creare un'esperienza uniforme e sfruttare al meglio le funzionalità di categorizzazione e ricerca del pannello di controllo home page.

### <a name="task-flow-control-panel-items"></a>Elementi del pannello di controllo del flusso attività

**Generale**

-   **Mantieni il contenuto e i controlli più importanti visibili senza lo scorrimento.** Gli utenti non scorrono per visualizzare il contenuto della pagina a meno che non dispongano di un motivo per. È possibile rendere sempre visibili i pulsanti di commit inserendoli in un' [area di comando](glossary.md) anziché nell'area del contenuto. Non suddividere le pagine solo per evitare lo scorrimento.
    -   **È possibile scorrere verticalmente pagine lunghe,** purché i controlli più importanti siano visibili senza scorrimento.
    -   **Non usare lo scorrimento orizzontale.** Riprogettare invece il contenuto della pagina e utilizzare lo scorrimento verticale. Le pagine possono avere barre di scorrimento orizzontali solo quando vengono rese molto strette.
-   **Per spostarsi tra le pagine:**
    -   Usare i [collegamenti alle attività](glossary.md) per avviare un'attività.
    -   Usare i collegamenti alle attività o un pulsante Avanti per passare alla pagina successiva in un'attività in più passaggi.
    -   Usare i pulsanti commit per completare un'attività.
    -   Usare il pulsante indietro sulla barra dei menu per tornare alle pagine visualizzate in precedenza. Non aggiungere un pulsante indietro all'area dei comandi.
    -   Utilizzare la barra degli indirizzi per tornare direttamente al pannello di controllo home page.
    -   Usare Visualizza anche collegamenti nel riquadro attività per passare alle pagine di altri elementi del pannello di controllo. In caso contrario, la navigazione deve rimanere all'interno di un singolo elemento del pannello di controllo.
-   **Inserire solo il pannello di controllo home page nella barra degli indirizzi.** Se si fa clic su tale collegamento, viene restituito il pannello di controllo home page, abbandonando il lavoro in corso senza una [conferma](https://msdn.microsoft.com/library/windows/desktop/aa511273.aspx).
-   **Non inserire un pulsante di comando Chiudi nelle pagine del pannello di controllo.** Gli utenti possono chiudere una finestra del pannello di controllo usando il pulsante Chiudi sulla barra del titolo.

**Collegamenti alle attività e pulsanti**

-   **Quando una pagina dispone di un piccolo set di opzioni fisse, utilizzare i collegamenti alle attività anziché una combinazione di pulsanti di opzione e un pulsante Avanti.** Ciò consente agli utenti di selezionare una risposta con un solo clic.
-   È possibile inserire i collegamenti alle attività e i pulsanti nelle posizioni seguenti (in ordine di individuabilità):
    -   [Area di comando](glossary.md) (solo per i pulsanti di comando nelle pagine spoke).
    -   [Area del contenuto](glossary.md):
        -   Pulsanti di comando
        -   Collegamenti alle attività
        -   Altri collegamenti
    -   Collegamenti nel [riquadro attività](glossary.md) (solo pagine hub).
-   **Basare il percorso dei collegamenti alle attività e dei pulsanti di importanza e necessità di individuabilità.**
    -   **Inserire solo i pulsanti commit nell'area comando.**
    -   **Inserire le attività essenziali nell'area del contenuto.** I pulsanti di comando tendono a attirare la massima attenzione, quindi riservarli per i comandi che gli utenti devono vedere. I collegamenti alle attività attirano anche l'attenzione, ma meno dei pulsanti di comando.
    -   **Riservare il riquadro attività e i collegamenti normali per le attività secondarie (meno importanti).** Il riquadro attività è l'area meno individuabile di una pagina attività e i collegamenti semplici non sono visibili come pulsanti di comando e collegamenti alle attività.
-   Per i collegamenti alle attività presentati nell'area del contenuto:
    -   **Se sono presenti più di sette collegamenti, raggruppare i collegamenti in categorie.** Fornire intestazioni per ognuno dei gruppi.
    -   **Per meno di sette collegamenti, presentare i collegamenti in un singolo gruppo senza intestazione.**
-   **Presentare i collegamenti e i pulsanti delle attività in un ordine logico.** Elenca i collegamenti delle attività verticalmente, i pulsanti di comando orizzontalmente.
-   Nelle categorie **dividere i comandi in gruppi correlati.** Presentare i gruppi di attività inserendo prima di tutto il nome usato più di frequente e, all'interno di ogni gruppo, inserire prima le attività più utilizzate. **L'ordine risultante dovrebbe approssimativamente rispettare la probabilità di utilizzo, ma anche un flusso logico.**
    -   **Eccezione:** I collegamenti alle attività che consentono di eseguire tutte le operazioni devono essere posizionati per primi.
-   **Se sono presenti molti collegamenti alle attività, assegnare alle attività più importanti un aspetto più evidente** usando un'icona a forma di pixel 24x24 e due righe di testo. Per le attività meno importanti, usare un'icona in pixel 16x16 o nessuna icona e una singola riga di testo del collegamento.

    ![Screenshot di elementi con icone grandi e piccole ](images/winenv-ctrl-panels-image4.png)

    In questo esempio, ai comandi importanti viene assegnato un aspetto più importante.

-   **Hanno una separazione fisica chiara tra i comandi usati di frequente e i comandi distruttivi.** In caso contrario, gli utenti potrebbero fare clic accidentalmente sui comandi distruttivi. Potrebbe essere necessario riordinare i comandi in modo da mettere insieme i comandi distruttivi.
-   **Fornire il meccanismo per annullare i comandi direttamente nella pagina.** Gli utenti non dovrebbero dover spostarsi altrove per annullare un errore.
-   **Per i collegamenti alle attività, usare tutte le icone del collegamento alle attività predefinite o tutte le icone personalizzate.** Non combinarli. Si consiglia di usare icone personalizzate solo se:
    -   Aiutano gli utenti a comprendere le attività.
    -   Sono conformi agli [standard dell'icona Aero](vis-icons.md).
    -   Hanno un aspetto discreto.

**Finestre di dialogo**

Quando si usano i flussi attività, in genere si vuole che un'attività scorra da una pagina all'altra all'interno di una singola finestra, ma le circostanze seguenti sono eccezioni. Usare le finestre di dialogo nelle circostanze seguenti:

-   Per richiedere agli utenti il nome utente e la password di un amministratore. Utilizzare sempre la finestra di dialogo Gestione credenziali per questo scopo. (Deve essere [modale](glossary.md)).
-   Per confermare un comando sul posto utilizzando una finestra di dialogo attività o di messaggio. (Deve essere modale).
-   Per ottenere l'input per i comandi sul posto, ad esempio per i comandi nuovi, Aggiungi, Salva con nome, Rinomina e stampa.

    ![screenshot della finestra di dialogo Elimina percorsi di rete ](images/winenv-ctrl-panels-image5.png)

    In questo esempio, il comando Delete viene eseguito in una finestra di dialogo anziché in una pagina separata.

-   Per eseguire attività secondarie autonome. Se si usa una finestra secondaria non [modale](glossary.md), le attività possono essere eseguite in modo indipendente e all'esterno del flusso dell'attività principale.

### <a name="hub-pages"></a>Pagine hub

**Generale**

-   Usare le pagine dell'hub basate su attività nei casi seguenti:
    -   **Il numero di attività comunemente utilizzate o importanti è ridotto.**
    -   **La configurazione riguarda uno o due oggetti** (esempi: monitoraggi, tastiera, mouse, controller di gioco).
    -   **La configurazione si applica a livello di sistema** (esempi: data e ora, sicurezza, opzioni di risparmio energia).
-   Usare le pagine di hub basate su oggetti quando:
    -   **La configurazione può coinvolgere diversi oggetti** , ad esempio account utente, connessioni di rete e stampanti.
    -   **La configurazione si applica solo all'oggetto selezionato**.
-   **Non usare una pagina Hub se l'elemento del pannello di controllo include una singola pagina** che contiene tutte le attività e le proprietà necessarie.

**Elenchi di oggetti**

-   **Elencare gli elementi in un ordine logico.** Ordinare gli oggetti denominati in ordine alfabetico, numeri in ordine numerico e date in ordine cronologico.
-   Per gli hub basati su oggetti, **fornire i comandi di visualizzazione oggetti nel riquadro attività se la possibilità di modificare la visualizzazione è importante per le attività**. La possibilità di modificare le visualizzazioni è importante se sono presenti molti oggetti e la presentazione predefinita non funziona correttamente per tutti gli scenari. Gli utenti possono modificare la visualizzazione elenco anche se non sono presenti comandi espliciti tramite il menu di scelta rapida visualizzazione elenco, ma è meno individuabile.

Per altre linee guida sulla presentazione degli elenchi di oggetti, vedere visualizzazione [elenco](ctrl-list-views.md).

**Interazione**

-   **Non inserire pulsanti di commit nelle pagine dell'hub.** Le pagine dell'hub sono fondamentalmente punti di lancio. Gli utenti non devono mai eseguire il commit delle pagine dell'hub. E i pulsanti di commit nelle pagine dell'hub rendono le attività avviate da un hub confuso (gli utenti si chiedono se è necessario eseguire il commit di queste attività).
    -   **Eccezione:** Se per la modifica di un'impostazione è richiesta l' [elevazione](glossary.md)dei privilegi, specificare un pulsante applica con un' [icona scudo di sicurezza](winenv-uac.md). Disabilitare il pulsante commit dopo aver applicato le modifiche.
-   **Si consiglia di inserire le proprietà più utili direttamente nelle pagine hub.** Queste pagine dell'Hub ibrido sono fortemente consigliate quando è più probabile che gli utenti usino il pannello di controllo per accedere a tali proprietà.

    ![screenshot della pagina dell'hub opzioni Power ](images/winenv-ctrl-panels-image6.png)

    In questo esempio, l'elemento del pannello di controllo Opzioni risparmio energia presenta le impostazioni più utili direttamente nella pagina Hub.

-   **Usare un modello di commit immediato per tutte le impostazioni nelle pagine dell'Hub ibrido, in modo che le modifiche vengano apportate immediatamente.** Anche in questo caso, gli utenti non commettono mai una pagina Hub. Se un'impostazione richiede un pulsante di commit, non inserirla in una pagina Hub.
-   **Si consiglia di inserire semplici comandi "One-Step" direttamente nelle pagine dell'hub invece di usare i collegamenti di navigazione.**
-   **Confermare i comandi sul posto i cui effetti non possono essere facilmente annullati.** Utilizzare una [finestra di dialogo attività](win-dialog-box.md) o di [messaggio](glossary.md).

    ![screenshot della finestra di dialogo Conferma eliminazione ](images/winenv-ctrl-panels-image7.png)

    In questo esempio, il comando Delete viene confermato con una finestra di dialogo.

-   **Per le pagine di hub basate su attività, identificare ogni attività con un collegamento all'attività e un'icona.** È anche possibile specificare una descrizione facoltativa per ogni collegamento. Tuttavia, provare a fare in modo che i collegamenti alle attività siano intuitivi e fornire descrizioni facoltative solo ai collegamenti effettivamente necessari.

    ![screenshot della pagina dell'hub prestazioni computer ](images/winenv-ctrl-panels-image8.png)

    In questo esempio, ogni attività dispone di un collegamento all'attività e di un'icona.

-   **Per le pagine dell'hub basate su oggetti, fare clic su Seleziona oggetti, quindi fare doppio clic su Seleziona un oggetto e passa alla pagina predefinita.** La pagina predefinita è in genere una pagina delle proprietà o una pagina di hub basata su attività.
-   **Una pagina Hub basata su oggetti può passare a un hub basato su attività per gli oggetti selezionati.** Tuttavia, questi hub secondari devono essere evitati perché rendono un elemento del pannello di controllo troppo indiretto.

**Riquadri attività**

Utilizzare i riquadri attività per presentare collegamenti a comandi, visualizzazioni ed elementi del pannello di controllo correlati.

-   Per i riquadri attività in hub basati su attività, presentare i collegamenti nell'ordine seguente:
    -   **Comandi secondari**. Presentare attività primarie solo nell'area del contenuto. Utilizzare il riquadro attività per attività secondarie facoltative. Si consideri un'attività primaria se gli utenti devono individuarla in scenari importanti; secondario se è accettabile per gli utenti non individuarlo.
    -   **Vedere anche**. Collegamenti facoltativi che passano agli elementi del pannello di controllo correlati.
-   Per i riquadri attività negli hub basati su oggetti, presentare i collegamenti nell'ordine seguente:
    -   **Visualizzazioni di oggetti**. Collegamenti facoltativi utilizzati per controllare la presentazione degli oggetti.
    -   **Comandi corretti**. Comandi indipendenti dagli oggetti attualmente selezionati.
    -   **Comandi contestuali**. I comandi che dipendono dagli oggetti attualmente selezionati e pertanto non vengono sempre visualizzati.
    -   **Vedere anche**. Collegamenti facoltativi che passano agli elementi del pannello di controllo correlati.
-   **Non usare i riquadri attività nelle pagine spoke.** Diversamente dalle pagine hub, le pagine spoke devono essere incentrate sul completamento dell'attività. Non si vuole incoraggiare gli utenti a uscire prima del completamento.

**Vedere anche collegamenti**

-   **Fornire i collegamenti vedere anche nel riquadro attività per consentire agli utenti di trovare elementi del pannello di controllo correlati o l'elemento del pannello di controllo corretto se hanno quello errato.** È probabile che il collegamento agli elementi utenti venga associato all'elemento del pannello di controllo.

    ![screenshot dei collegamenti del centro operativo ' vedere anche ' ](images/winenv-ctrl-panels-image9.png)

    In questo esempio, l'elemento del pannello di controllo del centro operativo si collega agli elementi del pannello di controllo correlati.

-   **Consente di eseguire il collegamento a una pagina di attività specifica, se è più probabile che gli utenti riconoscano.** In caso contrario, collegarsi all'intero elemento del pannello di controllo. Usare il nome del pannello di controllo senza aggiungere la frase, il pannello di controllo.

### <a name="spoke-pages"></a>Pagine spoke

**Generale**

-   **Usare le pagine delle attività per le attività più comuni o importanti, in cui gli utenti necessitano di altre istruzioni e spiegazioni.**
-   **Utilizzare le pagine del modulo per le funzionalità con numerose impostazioni e trarre vantaggio da una presentazione diretta a pagina singola.** Le attività ideali per tali pagine in genere comportano modifiche ovvie a poche proprietà semplici.
-   **Non usare i riquadri attività nelle pagine spoke.**

**Interazione**

-   **Provare a limitare le attività principali a una singola pagina.** Se è necessaria più di una pagina, è possibile:
    -   **Usare le pagine di spoke intermedie per passaggi aggiuntivi o facoltativi.** Viene eseguito il commit delle pagine intermedie con spoke dalla pagina finale spoke.
    -   **Usare le finestre indipendenti per le attività ausiliarie indipendenti.** Le finestre indipendenti vengono sottoposte a commit autonomamente e indipendentemente dall'attività principale.

Questa operazione mantiene il significato dei pulsanti di commit per l'attività principale chiara e non ambigua. Gli utenti devono sempre essere sicuri di comprendere cosa sta eseguendo il commit.

-   **Non usare vedere anche i collegamenti all'interno di un flusso attività.** Questi collegamenti a elementi del pannello di controllo, ma diversi, correlati. Sebbene la navigazione verso un elemento diverso sia accettabile nelle pagine dell'hub, non è presente nelle pagine spoke, perché questa operazione interrompe l'attività.
-   **Non usare le pagine spoke per semplici input o conferme.** Usare invece le finestre di dialogo modali.

**Interazione (pagine spoke intermedie)**

-   **Usare i collegamenti alle attività o un pulsante Avanti per passare alla pagina successiva.** Il modo per procedere al passaggio successivo dovrebbe essere sempre ovvio.
-   **È possibile disporre di collegamenti di navigazione a passaggi attività facoltativi.** Per evitare confusione quando gli utenti si impegnano nell'attività, le pagine aggiuntive devono essere pagine intermedie all'interno dello stesso elemento del pannello di controllo. Non devono avere pulsanti di commit, ma è necessario eseguirne il commit quando viene eseguito il commit dell'attività principale.

**Interazione (pagine finale spoke)**

-   **Usare i pulsanti commit per completare un'attività.** Usare un [modello di commit ritardato](glossary.md) per le pagine spoke, in modo che le modifiche non vengano apportate fino a quando non viene eseguito il commit esplicito (se gli utenti si spostano con l'indietro, la chiusura o la barra degli indirizzi). I pulsanti commit sono un indizio visivo che l'utente sta per completare un'attività. Non usare i collegamenti a questo scopo.
-   **Non confermare i pulsanti di commit (incluso l'annullamento).** Questa operazione può risultare fastidiosa. Eccezioni:
    -   L'azione ha conseguenze significative e, se non è corretta, non è facilmente risolvibile.
    -   L'azione può causare una perdita significativa del tempo o del lavoro dell'utente.
    -   L'azione è chiaramente incoerente con altre azioni.
-   **Non verificare se gli utenti abbandonano le modifiche** spostandosi indietro, Chiudi o barra degli indirizzi. Tuttavia, è possibile verificare se un'esplorazione potenzialmente non intenzionale può causare una perdita significativa del tempo o del lavoro dell'utente.
-   **Non usare i collegamenti di comando o di navigazione** (compresi i collegamenti vedere anche). Nelle pagine di spoke finale, gli utenti devono completare o annullare in modo esplicito l'attività. Gli utenti non devono essere invitati a spostarsi altrove, perché questa operazione potrebbe annullare l'attività in modo implicito.
-   **Quando gli utenti completano o annullano un'attività, devono essere restituiti alla pagina Hub da cui è stata avviata l'attività.** Se non è presente alcuna pagina di questo tipo, chiudere invece la finestra del pannello di controllo. Non presupporre che le pagine spoke vengano sempre avviate da un'altra pagina.
-   **Rimuovere le pagine "di cui è stato eseguito il commit" non aggiornate dallo stack indietro di Esplora risorse** quando si tornano gli utenti alla pagina da cui è stata avviata l'attività. Quando si fa clic sul pulsante indietro, gli utenti non dovrebbero mai visualizzare le pagine di cui si è già eseguito il commit. Gli utenti devono sempre apportare ulteriori modifiche ripetendo completamente l'attività invece di fare clic su indietro per modificare le pagine non aggiornate.
    -   **Sviluppatori:** È possibile rimuovere queste pagine non aggiornate usando le API ITravelLog:: FindTravelEntry () e ITravelLogEx::D eleteEntry ().

**Pulsanti di commit**

**Nota:** I pulsanti Annulla sono considerati pulsanti di commit.

-   **Confermare le attività usando i pulsanti di commit che sono risposte specifiche all'istruzione principale, anziché etichette generiche come OK.** Le etichette sui pulsanti di commit dovrebbero avere un significato autonomo. Evitare di usare OK perché non è una risposta specifica all'istruzione principale e quindi più facile da fraintendere. Inoltre, OK viene in genere utilizzato con le finestre di dialogo modali e implica la chiusura non corretta della finestra elemento del pannello di controllo.
    -   **Eccezioni**
        -   Utilizzare OK per le pagine che non dispongono di impostazioni.
        -   Usare OK quando la risposta specifica è ancora generica, ad esempio Save, SELECT o Choose, come quando si modifica un'impostazione specifica o una raccolta di impostazioni.
        -   Usare OK se la pagina contiene pulsanti di opzione che sono risposte all'istruzione principale. Per mantenere il modello con commit ritardato, non è possibile usare i collegamenti alle attività in una pagina finale spoke.

            ![screenshot delle restrizioni Web con il pulsante OK ](images/winenv-ctrl-panels-image10.png)

            In questo esempio, i pulsanti di opzione, non i pulsanti di commit, sono risposte all'istruzione principale.
-   **Fornire un pulsante Annulla per consentire agli utenti di abbandonare in modo esplicito le modifiche.** Sebbene gli utenti possano abbandonare un'attività in modo implicito, senza confermare le modifiche, fornire un pulsante Annulla consente loro di ottenere una maggiore fiducia.
    -   **Eccezione:** Non specificare un pulsante Annulla per le attività in cui gli utenti non possono apportare modifiche. Il pulsante OK ha lo stesso effetto di Annulla in questo caso.
-   **Non usare i pulsanti Chiudi, fine o termina commit.** Questi pulsanti vengono in genere utilizzati con le finestre di dialogo modali e implicano erroneamente la chiusura della finestra dell'elemento del pannello di controllo. Gli utenti possono chiudere la finestra usando il pulsante Chiudi sulla barra del titolo. Inoltre, le operazioni completate e complete sono fuorvianti, perché gli utenti vengono restituiti alla pagina da cui l'attività è stata avviata, quindi non sono realmente eseguite.
-   **Non disabilitare i pulsanti di commit.** In caso contrario, gli utenti devono dedurre perché i pulsanti commit sono disabilitati. È preferibile lasciare abilitati i pulsanti di commit e fornire un messaggio di errore utile quando si verifica un problema.
-   **Verificare che i pulsanti commit siano visualizzati nella pagina senza scorrimento.** Se la pagina è molto estesa, è possibile rendere sempre visibili i pulsanti di commit inserendoli in un' [area di comando](glossary.md)anziché nell'area del contenuto.

    ![screenshot della finestra di dialogo AutoPlay ](images/winenv-ctrl-panels-image11.png)

    In questo esempio, le dimensioni dell'area di contenuto sono senza limiti, quindi i pulsanti commit vengono inseriti nell'area dei comandi.

-   Allinea a destra i pulsanti di commit e usa questo ordine (da sinistra a destra): pulsanti di commit positivi, Annulla e applica.

**Pulsanti anteprima**

-   Verificare che **il pulsante Anteprima significhi applicare le modifiche in sospeso ora, ma ripristinare le impostazioni correnti se gli utenti si spostano fuori dalla pagina senza eseguire il commit delle modifiche.**
-   **È possibile utilizzare i pulsanti anteprima in qualsiasi pagina di spoke.** Le pagine hub non necessitano di pulsanti di anteprima perché usano un [modello di commit immediato](glossary.md).
-   **Si consiglia di utilizzare un pulsante anteprima anziché un pulsante Applica per le pagine del pannello di controllo.** I pulsanti anteprima sono più semplici da comprendere per gli utenti e possono essere usati in qualsiasi pagina di spoke.
-   **Fornire un pulsante anteprima solo se la pagina contiene impostazioni (almeno una) con effetti che gli utenti possono vedere.** Gli utenti dovrebbero essere in grado di visualizzare in anteprima una modifica, valutare la modifica e apportare ulteriori modifiche in base a tale valutazione.
-   **Abilitare sempre il pulsante anteprima.**

**Anteprime in tempo reale**

Un elemento del pannello di controllo ha un'anteprima in tempo reale quando l'effetto delle modifiche in una pagina spoke è immediatamente visibile.

-   **Provare a usare l'anteprima in tempo reale per le impostazioni di visualizzazione quando:**
    -   L'effetto è evidente, in genere perché si applica all'intero monitoraggio.
    -   L'effetto può essere applicato senza un ritardo significativo.
    -   L'effetto è sicuro e può essere annullato facilmente.

        ![screenshot della finestra di dialogo Modifica impostazioni colore ](images/winenv-ctrl-panels-image12.png)

        In questo esempio, l'effetto delle impostazioni relative a colore e aspetto di Windows è immediatamente visibile. Questa operazione consente agli utenti di apportare modifiche con il minimo sforzo.

-   **Usare Save Changes e Cancel per i pulsanti commit.** "Salva modifiche" consente di mantenere le impostazioni correnti, mentre Annulla Ripristina le impostazioni originali. Viene utilizzato "Save Changes" anziché OK per chiarire che le modifiche apportate in anteprima non sono state ancora applicate.
-   **Non specificare un pulsante Applica.** L'anteprima in tempo reale rende l'applicazione non necessaria.
-   **Ripristinare eventuali modifiche se gli utenti si spostano** con l'indietro, la chiusura o la barra degli indirizzi. Per mantenere le modifiche, gli utenti devono eseguirne il commit in modo esplicito.

**Pulsanti applica**

-   Verificare che **il pulsante Applica significhi applicare le modifiche in sospeso (effettuate dall'avvio dell'attività o dall'ultima applicazione), ma che rimangano nella pagina corrente.** Questa operazione consente agli utenti di valutare le modifiche prima di procedere ad altre attività.
-   **Usare i pulsanti applica solo nelle pagine di spoke finale.** I pulsanti applica non devono essere utilizzati nelle pagine spoke intermedie per mantenere un modello di commit immediato.
    -   **Eccezione:** È possibile usare i pulsanti applica in una pagina di Hub ibrido Se la modifica di un'impostazione richiede l' [elevazione](glossary.md)dei privilegi. Per altri dettagli, vedere [interazione della pagina Hub](#hub-pages).
-   **Fornire un pulsante applica solo se la pagina contiene impostazioni (almeno una) con effetti che gli utenti possono valutare in modo significativo.** In genere, i pulsanti Applica vengono usati quando le impostazioni rendono visibili le modifiche. Gli utenti devono essere in grado di applicare una modifica, valutare la modifica e apportare ulteriori modifiche in base a tale valutazione.
-   **Abilitare il pulsante applica solo quando sono presenti modifiche in sospeso;** in caso contrario, disabilitarlo.
-   **Assegnare "A" come chiave di accesso.**

### <a name="control-panel-integration"></a>Integrazione con il pannello di controllo

Per integrare l'elemento del pannello di controllo con Windows, è possibile:

-   **Registrare l'elemento del pannello di controllo (inclusi il nome, la descrizione e l'icona)**, in modo che Windows ne sia a conoscenza.
-   Se l'elemento del pannello di controllo è di primo livello (vedere di seguito):
    -   Associarlo alla pagina di **categoria** appropriata.
    -   **Fornire i collegamenti alle attività (inclusi il nome, la descrizione, le parole chiave e la riga di comando)** per indicare le attività primarie e consentire agli utenti di spostarsi direttamente nelle attività.
-   **Fornire i termini di ricerca** per aiutare gli utenti a trovare i collegamenti alle attività usando la funzionalità di ricerca del pannello di controllo.

    Si noti che è possibile fornire queste informazioni solo per singoli elementi del pannello di controllo non è possibile aggiungere o modificare queste informazioni per gli elementi del pannello di controllo esistenti che si estendono.

**Pagine categoria**

-   **Aggiungere l'elemento del pannello di controllo a una pagina di categoria solo se:**

    -   La maggior parte degli utenti ne ha bisogno. Esempio: centro di rete e condivisione
    -   Viene utilizzato molte volte. Esempio: System
    -   Fornisce funzionalità importanti che non sono esposte altrove. Esempio: stampanti

    Gli elementi del pannello di controllo che soddisfano questi criteri vengono definiti di primo livello.

-   **Non aggiungere l'elemento del pannello di controllo a una pagina di categoria se:**

    -   Viene usato raramente o usato per l'installazione singola. Esempio: centro di benvenuto
    -   È destinato a utenti avanzati o professionisti IT. Esempio: gestione dei colori
    -   Non si applica alla configurazione hardware o software corrente. Esempio: Windows SideShow (se non è supportato dall'hardware corrente).

    La rimozione degli elementi del pannello di controllo dalle pagine di categoria rende più semplice trovare gli elementi di primo livello. Dato il loro utilizzo, questi elementi del pannello di controllo sono sufficientemente individuabili tramite i punti di ingresso di ricerca o contestuali.

-   **Associare l'elemento del pannello di controllo di primo livello alla categoria in cui è più probabile che gli utenti la cerchino.** Questa decisione deve essere basata sul test dell'utente.
-   **È consigliabile associare l'elemento del pannello di controllo di primo livello anche alla seconda categoria più probabile.** È consigliabile associare un elemento del pannello di controllo a due categorie se è probabile che gli utenti cerchino le attività principali in più di una posizione.
-   **Non associare l'elemento del pannello di controllo a più di due categorie.** Il valore della categorizzazione viene minato se gli elementi del pannello di controllo vengono visualizzati in diverse categorie.

**Collegamenti alle attività**

-   **Associare l'elemento del pannello di controllo alle attività primarie.** È possibile visualizzare fino a cinque attività in una pagina di categoria, ma per la ricerca del pannello di controllo vengono usate attività aggiuntive. Usare la stessa formulazione usata per i collegamenti alle attività, eventualmente rimuovendo alcune parole per rendere i collegamenti dell'attività più concisi.
-   **È preferibile che i collegamenti alle attività portino in posizioni diverse nell'elemento del pannello di controllo.** La presenza di più collegamenti alla stessa posizione può creare confusione.

**Termini di ricerca**

-   **Registrare i termini di ricerca per l'elemento del pannello di controllo che gli utenti più probabilmente utilizzeranno per descriverlo.** Questi termini di ricerca devono includere:

    -   Funzionalità o oggetti configurati.
    -   Attività primarie.

    Questi termini di ricerca devono essere basati sul test dell'utente.

-   **Includere anche sinonimi comuni per questi termini di ricerca.** Ad esempio, il monitoraggio e la visualizzazione sono sinonimi ed è quindi necessario includere entrambe le parole.
-   **Includere ortografie alternative o interruzioni di parola.** È possibile, ad esempio, che gli utenti cerchino il sito Web e il sito Web. Si consiglia di fornire anche errori di ortografia comuni.
-   **Si considerino i sostantivi singolari e plurali.** La funzionalità di ricerca del pannello di controllo non cerca automaticamente entrambi i form; specificare i moduli per cui gli utenti possono eseguire la ricerca.
-   **USA semplici verbi con tensione presente.** Se si registra Connect come termine di ricerca, la funzionalità di ricerca non cercherà automaticamente le connessioni, le connessioni e le connessioni.
-   **Non preoccuparti del caso.** La funzionalità di ricerca non fa distinzione tra maiuscole e minuscole.

### <a name="standard-users-and-protected-administrators"></a>Utenti standard e amministratori protetti

**Per la modifica di molte impostazioni sono necessari privilegi di amministratore.** Se un processo richiede privilegi di amministratore, Windows Vista e versioni successive richiedono che [gli utenti standard e gli](glossary.md) [amministratori protetti](glossary.md) possano elevare i propri privilegi in modo esplicito. Questa operazione consente di impedire l'esecuzione di codice dannoso con privilegi di amministratore.

Per ulteriori informazioni ed esempi, vedere [controllo dell'account utente](winenv-uac.md).

### <a name="schemes-and-themes"></a>Schemi e temi

Uno schema è una raccolta denominata di impostazioni visive. Un tema è una raccolta denominata di impostazioni nel sistema. Tra gli esempi di schemi e temi sono inclusi la visualizzazione, il mouse, il telefono e il modem, le opzioni di risparmio energia e le opzioni audio e audio.

-   **Consenti agli utenti di creare schemi nei casi seguenti:**

    -   **È probabile che gli utenti modifichino le impostazioni.**
    -   **È più probabile che gli utenti modifichino le impostazioni come una raccolta.**

    Gli schemi sono utili quando gli utenti si trovano in un ambiente diverso, ad esempio in una posizione fisica diversa (paese/area geografica, fuso orario); uso del computer in una situazione diversa (su batterie, ancorato/non ancorato); oppure usare il computer per una funzione diversa (presentazioni, riproduzione video).

-   **Specificare almeno uno schema predefinito.** Lo schema predefinito dovrebbe essere ben denominato e applicabile alla maggior parte degli utenti nella maggior parte dei casi. Gli utenti non devono creare uno schema autonomo.
-   **Fornire un'anteprima o un** altro meccanismo in modo che gli utenti possano visualizzare le impostazioni nello schema.

    ![screenshot della finestra di dialogo personalizzazione ](images/winenv-ctrl-panels-image13.png)

    In questo esempio, l'elemento del pannello di controllo della personalizzazione Mostra un'anteprima delle impostazioni del desktop e dell'aspetto.

-   **Consente di specificare i comandi Salva con nome ed Elimina.** Un comando Rinomina non è necessario che gli utenti possano rinominare gli schemi salvando con il nome desiderato ed eliminando lo schema originale.
-   Se non è possibile applicare le impostazioni senza uno schema, **non consentire agli utenti di eliminare tutti gli schemi.** Gli utenti non devono creare uno schema autonomo.
-   Se gli schemi non sono completamente indipendenti (ad esempio, gli schemi di alimentazione dipendono dalla modalità di funzionamento del computer portatile corrente), **assicurarsi che esista un modo semplice per modificare le impostazioni applicabili a tutti gli schemi.** Ad esempio con combinazioni per il risparmio di energia, assicurarsi che gli utenti possano impostare cosa accade quando il coperchio di un computer portatile viene chiuso in un'unica posizione.

### <a name="miscellaneous"></a>Varie

-   **Utilizzare le estensioni del pannello di controllo per le funzionalità che sostituiscono o estendono le funzionalità di Windows esistenti.** Gli elementi del pannello di controllo seguenti sono estendibili: dispositivi Bluetooth, schermo, Internet, tastiera, mouse, rete, alimentazione, sistema, wireless (infrarossi).

### <a name="default-values"></a>Valori predefiniti

-   **Le impostazioni all'interno di un elemento del pannello di controllo devono riflettere lo stato corrente della funzionalità.** In caso contrario, potrebbe essere fuorviante e potrebbe causare risultati indesiderati. Se, ad esempio, le impostazioni riflettono le raccomandazioni ma non lo stato corrente, gli utenti potrebbero fare clic su Annulla anziché apportare modifiche, pensando che non sono necessarie modifiche.
-   **Scegliere il più sicuro (per evitare la perdita di dati o l'accesso al sistema) e lo stato iniziale più sicuro.** Si supponga che la maggior parte degli utenti non modifichi le impostazioni.
-   **Se la sicurezza e la sicurezza non sono fattori, scegliere lo stato iniziale più probabile o pratico.**

## <a name="text"></a>Testo

### <a name="item-names"></a>Nomi degli elementi

-   **Scegliere un nome descrittivo che comunichi chiaramente e differenzi l'elemento del pannello di controllo.** La maggior parte dei nomi descrive la funzionalità di Windows o l'oggetto da configurare e vengono visualizzati nella visualizzazione classica del pannello di controllo home page.
-   **Non includere le parole "Settings", "Options", "Properties" o "Configuration" nel nome.** Questo è implicito e la sua uscita rende più semplice l'analisi da parte degli utenti.

    **Non corretto:**

    Opzioni di accessibilità

    Impostazioni modem

    Opzioni risparmio energia

    Opzioni internazionali e della lingua

    **Corretto:**

    Accessibilità

    Modem

    Potenza

    Linguaggi e formati regionali

    Negli esempi corretti, le parole non necessarie vengono rimosse.

-   **Se l'elemento del pannello di controllo Configura le funzionalità correlate, elencare solo le funzionalità necessarie per identificare l'elemento ed elencare le funzionalità che più probabilmente verranno riconosciute o usate per prime.**

    **Non corretto:**

    Opzioni cartella

    Opzioni per telefono e modem

    **Corretto:**

    File e cartelle

    Modem

    Negli esempi corretti, le funzionalità principali degli elementi del pannello di controllo hanno una particolare enfasi.

-   Usare l'uso [di maiuscole in stile titolo](glossary.md).

### <a name="page-titles"></a>Titoli di pagina

**Nota:** Come per tutte le finestre di esplorazione, i titoli delle pagine del pannello di controllo vengono visualizzati sulla [barra degli indirizzi](glossary.md), ma non sulla barra del titolo.

-   **Per le pagine hub, usare il nome dell'elemento del pannello di controllo.**
-   **Per le pagine spoke, usare un riepilogo conciso dello scopo della pagina.** Utilizzare l'istruzione principale della pagina se è conciso; in caso contrario, usare una ridisposizione concisa dell'istruzione principale.

    ![screenshot della finestra di dialogo Opzioni risparmio energia ](images/winenv-ctrl-panels-image6.png)

    In questo esempio vengono usate le opzioni di risparmio energia per il titolo della pagina anziché l'istruzione principale.

-   Usare l'uso di maiuscole in stile titolo.

### <a name="task-link-text"></a>Testo collegamento attività

Le linee guida seguenti si applicano ai collegamenti alle pagine delle attività, ad esempio collegamenti alle attività della pagina di categoria, e vedere anche collegamenti.

-   **Scegliere nomi di attività concisi che comunicano chiaramente e differenziano l'attività.** Non è necessario che gli utenti riescano a capire cosa significa realmente l'attività o in che modo si differenzia da altre attività.

    **Non corretto:**

    Modificare le impostazioni di visualizzazione

    **Corretto:**

    Risoluzione dello schermo

    Nell'esempio corretto, la formulazione esprime maggiore precisione.

-   **Consente di mantenere un linguaggio simile tra i collegamenti alle attività e le pagine a cui puntano.** Gli utenti non devono essere sorpresi dalla pagina visualizzata da un collegamento.
-   **Per le pagine delle attività, progettare l'istruzione principale, i pulsanti di commit e i collegamenti alle attività come un set di testo correlato.**

    **Esempi:**

    

    |                              |                                                       |
    |------------------------------|-------------------------------------------------------|
    | Collegamento all'attività:<br/>        | Connettersi a una rete wireless<br/>              |
    | Istruzione principale:<br/> | Scegliere una rete a cui connettersi<br/>             |
    | Pulsante commit:<br/>    | Connessione<br/>                                    |
    | Collegamento all'attività:<br/>        | Configurare i controlli padre<br/>                   |
    | Istruzione principale:<br/> | Scegliere un utente e impostare i controlli padre<br/> |
    | Pulsante commit:<br/>    | Applicare il controllo padre<br/>                     |
    | Collegamento all'attività:<br/>        | Risolvere i conflitti di sincronizzazione<br/>                |
    | Istruzione principale:<br/> | In che modo si desidera risolvere il conflitto?<br/>  |
    | Pulsante commit:<br/>    | Risolvi<br/>                                    |

    

     

    In questi esempi viene illustrata la relazione tra il testo del collegamento all'attività, l'istruzione principale e il testo del pulsante di commit.

-   Mentre le attività iniziano spesso con i verbi, **è consigliabile omettere il verbo sulle pagine di categoria se si tratta di un verbo generico, correlato alla configurazione, che non consente di comunicare l'attività.**

    **Verbi specifici e utili:**

    Add

    Controllo

    Connessione

    Copia

    Create

    Delete

    Disconnetti

    Installazione

    Rimuovi

    Configurazione

    Inizia

    Stop

    Risolvere problemi

    **Verbi generici e non Helper:**

    Regolare

    Modifica

    Choose

    Configurare

    Modifica

    Gestione

    Apri

    Seleziona

    Set

    Select

    Mostra

    Visualizzazione

-   **Se l'attività Configura diverse funzionalità correlate, elencare solo le funzionalità rappresentative del set.** Omettere i dettagli che possono essere facilmente dedotti.

    **Non corretto:**

    Volume altoparlante, mute, icona volume

    Altoparlanti, microfoni, MIDI e schemi audio

    **Corretto:**

    Volume altoparlante

    Altoparlanti e microfoni

    Negli esempi corretti solo le funzionalità rappresentative vengono fornite nel collegamento all'attività.

-   **È consigliabile eseguire la frase delle attività in termini di tecnologia solo se gli utenti di destinazione lo farebbero anche.**

    **Non corretto:**

    Connectoids

    Profondità pixel

    dpi

    **Corretto:**

    Stampanti

    Scanner

    Mouse

    Gli esempi corretti sono termini basati sulla tecnologia che è probabile che gli utenti di destinazione usino, mentre gli esempi non corretti non lo sono.

-   Utilizzare Sostantivi plurali solo se il sistema è in grado di supportare più di uno.
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Non usare punteggiatura finale.

### <a name="main-instructions"></a>Istruzioni principali

-   **Per la pagina Hub, usare l'istruzione principale per spiegare l'obiettivo dell'utente con l'elemento del pannello di controllo.** L'istruzione principale consente agli utenti di determinare se è stato selezionato l'elemento del pannello di controllo appropriato. Tenere presente che gli utenti potrebbero aver selezionato l'elemento del pannello di controllo in errore e stanno effettivamente cercando le impostazioni che fanno parte di un altro elemento del pannello di controllo.

    **Esempi:**

    Mantieni il computer sicuro e aggiornato

    Ottimizza il computer in modo che sia più facile da visualizzare, ascoltare e controllare

-   **Per le pagine spoke, utilizzare l'istruzione principale per illustrare le operazioni da eseguire nella pagina.** L'istruzione deve essere un'istruzione, una direzione imperativa o una domanda specifica. Le istruzioni valide comunicano l'obiettivo dell'utente con la pagina piuttosto che concentrarsi esclusivamente sui meccanismi di manipolazione.

    **Non corretto:**

    Selezionare un'attività di notifica

    **Corretto:**

    Indica come gestire le informazioni in ingresso

    La versione corretta comunica meglio l'obiettivo ottenibile dalla pagina.

-   **Quando possibile, usare verbi specifici.** Verbi specifici sono più significativi per gli utenti rispetto a quelli generici.
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   **Non includere i periodi finali se l'istruzione è un'istruzione.** Se l'istruzione è una domanda, includere un punto interrogativo finale.

### <a name="supplemental-instructions"></a>Istruzioni supplementari

-   **Per la pagina Hub, utilizzare l'istruzione supplementare facoltativa per illustrare ulteriormente lo scopo dell'elemento del pannello di controllo.**
-   **Per le pagine spoke, utilizzare l'istruzione supplementare facoltativa per presentare informazioni aggiuntive utili per comprendere o utilizzare la pagina.** È possibile fornire informazioni più dettagliate e definire la terminologia.
-   Usare frasi complete e [maiuscole/minuscole in stile frase](glossary.md).

### <a name="page-text"></a>Testo della pagina

-   **Non ripubblicare l'istruzione principale nell'area del contenuto.**
-   **Usare la parola "Page" per fare riferimento alla pagina stessa.**
-   **Usare la seconda persona (l'utente) per indicare agli utenti cosa fare** nell'area principale dell'istruzione e del contenuto. Spesso la seconda persona è implicita.

    **Esempio:**

    Scegliere le immagini che si desidera stampare.

-   **Usare la prima persona (i, me, My) per consentire agli utenti di indicare all'elemento del pannello di controllo cosa fare** nell'area del contenuto che risponde all'istruzione principale.

    **Esempio:**

    Stampa le foto sulla mia fotocamera.

### <a name="task-links"></a>Collegamenti alle attività

-   **Scegliere testo conciso collegamento che comunica chiaramente e distingue il collegamento dell'attività.** Dovrebbe essere di chiara comprensione e corrispondere all'istruzione principale. Gli utenti non devono necessariamente determinare il significato del collegamento o la differenza rispetto ad altri collegamenti.
-   **Avviare sempre i collegamenti alle attività con un verbo.**
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Non usare punteggiatura finale.
-   **Se il collegamento dell'attività richiede un'ulteriore spiegazione, fornire la spiegazione in un controllo testo separato usando le** frasi complete e la punteggiatura finale. Tuttavia, aggiungere queste spiegazioni solo quando necessario non aggiungere spiegazioni a tutti i collegamenti delle attività perché ne è necessario un altro collegamento.

Per ulteriori informazioni ed esempi, vedere [collegamenti](ctrl-command-links.md).

### <a name="commit-buttons"></a>Pulsanti di commit

-   **Usare etichette di pulsanti di commit specifiche che hanno un significato autonomo e corrispondono all'istruzione principale.** Idealmente, gli utenti non devono leggere nient'altro per comprendere l'etichetta. È molto più probabile che gli utenti leggano le etichette dei pulsanti di comando rispetto al testo statico.
-   **Avviare sempre le etichette dei pulsanti di commit con un verbo.**
-   **Non usare Close, done o Finish.** Queste etichette dei pulsanti sono più adatte per altri tipi di finestre.
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Non usare punteggiatura finale.
-   Assegnare una [chiave di accesso](glossary.md)univoca.
    -   **Eccezione:** Non assegnare chiavi di accesso ai pulsanti Annulla perché ESC è la chiave di accesso. In questo modo le altre chiavi di accesso risultano più semplici da assegnare.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento all'home page o alle pagine delle categorie del pannello di controllo:

-   Nella documentazione dell'utente, fare riferimento al pannello di controllo, usando le maiuscole e minuscole in stile titolo e omettendo un articolo definito precedente.

    **Esempio:**

    Nel pannello di controllo aprire **Centro sicurezza**.

-   In programmazione e altri documenti tecnici, fare riferimento al pannello di controllo home page e alla pagina delle categorie del pannello di controllo, senza capitalizzare le parole. Un articolo definito precedente è facoltativo.

Per gli elementi del pannello di controllo:

-   Quando si fa riferimento a un singolo elemento del pannello di controllo, usare " \[ nome \] dell'elemento del pannello di controllo nel pannello di controllo" o in genere "elemento del pannello di controllo" nella documentazione dell'utente. Non usare un applet, un programma o un pannello di controllo per fare riferimento a singoli elementi del pannello di controllo.
-   Quando si fa riferimento alla pagina dell'hub di un elemento del pannello di controllo, usare la " \[ pagina Nome elemento del pannello di controllo principale \] ".
-   Quando possibile, formattare il nome del pannello di controllo usando il testo in grassetto. In caso contrario, inserire il nome tra virgolette solo se necessario per evitare confusione.

Esempi:

-   Nel pannello di controllo aprire **controlli padre**.
-   Tornare alla pagina principale dei **controlli padre** .

