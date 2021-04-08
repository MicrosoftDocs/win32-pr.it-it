---
title: Finestre delle proprietà
description: Finestra delle proprietà è il nome collettivo per i tipi seguenti di finestra delle proprietà dell'interfaccia utente utilizzata per visualizzare e modificare le proprietà di un oggetto o di una raccolta di oggetti in una finestra di dialogo. Controllo proprietà utilizzato per visualizzare e modificare le proprietà di un oggetto o di una raccolta di oggetti in un riquadro. Finestra di dialogo Opzioni utilizzata per visualizzare e modificare le opzioni di un'applicazione.
ms.assetid: 18fc04da-9f84-4a44-9f3d-a9e29b121e7c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c255d638f236b4bc4a4f1a6c923eac24421cfe9d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103761213"
---
# <a name="property-windows"></a>Finestre delle proprietà

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

La finestra delle proprietà è il nome collettivo per i tipi di interfacce utente (UI) seguenti:

-   Finestra delle proprietà: utilizzata per **visualizzare e modificare le proprietà di un oggetto o di una raccolta di oggetti in una** finestra di dialogo.
-   Controllo proprietà: usato per **visualizzare e modificare le proprietà di un oggetto o di una raccolta di oggetti in un riquadro**.
-   Finestra di dialogo Opzioni: consente di **visualizzare e modificare le opzioni di un'applicazione**.

Una proprietà per un oggetto può essere una delle seguenti:

-   Impostazione che gli utenti possono modificare, ad esempio il nome di un file e l'attributo di sola lettura.
-   Attributo di un oggetto che gli utenti non possono modificare direttamente, ad esempio le dimensioni di un file e la data di creazione.

A differenza delle finestre di dialogo (diverse dalle finestre di dialogo Opzioni) e delle procedure guidate, le finestre delle proprietà supportano in genere diverse attività anziché una singola attività.

Le finestre delle proprietà sono in genere organizzate in pagine, accessibili tramite schede. Le finestre delle proprietà sono spesso associate a schede (e viceversa), ma le **schede non sono essenziali per le finestre delle proprietà**.

![screenshot della finestra delle proprietà delle proprietà del documento ](images/win-property-win-image1.png)

Una tipica finestra delle proprietà.

**Nota:** Le linee guida relative al [layout](vis-layout.md) e alle [schede](ctrl-tabs.md) sono presentate in articoli distinti.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Per decidere, prendi in considerazione queste domande:

-   **Per impostare le proprietà è necessario che gli utenti eseguano una sequenza di passaggi fissa e non banale?** In caso affermativo, usare invece una [procedura guidata](win-wizards.md) o un [flusso attività](glossary.md) .
-   **Il contenuto è costituito esclusivamente dalle opzioni di un'applicazione?** In tal caso, utilizzare una finestra di dialogo Opzioni.
-   **Il contenuto è costituito esclusivamente dagli attributi di un'applicazione?** In tal caso, utilizzare una [finestra informazioni su](glossary.md).
-   **Il contenuto è principalmente costituito dalle proprietà di un oggetto (impostazioni o attributi)?** In caso contrario, utilizzare una finestra di dialogo [casella](win-dialog-box.md) o una finestra di dialogo a [schede](glossary.md)standard.
-   È probabile che gli utenti possano **visualizzare o modificare le proprietà spesso o in un periodo di tempo prolungato?** In caso affermativo, usare un controllo proprietà; in caso contrario, utilizzare una finestra delle proprietà.
-   È probabile che gli utenti possano **visualizzare o modificare le proprietà per molti oggetti diversi alla volta?** In caso affermativo, usare un controllo proprietà; in caso contrario, utilizzare una finestra delle proprietà.

**Le finestre delle proprietà e i controlli proprietà non sono esclusivi.** È possibile visualizzare le proprietà a cui si accede più di frequente in un controllo proprietà e il set completo nella finestra delle proprietà.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

**Le finestre delle proprietà spesso diventano un terreno di dumping per una dispari gamma di impostazioni basate su tecnologia di basso livello.** Troppo spesso queste proprietà sono organizzate in tabulazioni, ma oltre a quelle non progettate per attività o utenti particolari. Di conseguenza, quando gli utenti sono connessi a un'attività in una finestra delle proprietà, spesso non sanno cosa fare.

Per assicurarsi che le finestre delle proprietà siano utili e utilizzabili, attenersi alla seguente procedura:

-   Verificare che le proprietà siano necessarie.
-   Presentare le proprietà in termini di obiettivi utente, non della tecnologia.
-   Presentare le proprietà al livello corretto.
-   Progetta le pagine per attività specifiche.
-   Progettare pagine per utenti specifici, in particolare utenti con limitazioni (non amministratori).
-   Organizzare le pagine delle proprietà in modo efficiente.

**Se si esegue una sola operazione...**

Presentare le proprietà in termini di obiettivi utente, non della tecnologia. Fingi di spiegare la proprietà e il motivo per cui è utile per un amico. Come si spiegherebbe? Quale lingua usare? Questo è il linguaggio da usare nelle pagine delle proprietà.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le finestre delle proprietà hanno diversi modelli di utilizzo.

-   Finestre delle proprietà. Le proprietà di un singolo oggetto vengono visualizzate in una finestra di dialogo non modale.
-   Finestre delle proprietà di più oggetti. Le proprietà per più oggetti vengono visualizzate in una finestra di dialogo non modale.
-   Finestre delle proprietà delle impostazioni effettive. Le proprietà valide per un singolo oggetto vengono visualizzate in una finestra di dialogo non modale.
-   Finestre di dialogo Opzioni. Le proprietà di un'applicazione vengono visualizzate in una finestra di dialogo modale.
-   Controlli proprietà. Le proprietà per la selezione corrente, ovvero un singolo oggetto o gruppo di oggetti, vengono visualizzate in un riquadro della finestra non modale o in una finestra non ancorata.

Tutti i modelli di finestra delle proprietà, ad eccezione di controlli proprietà, usano un commit ritardato, ovvero le modifiche diventano effettive solo quando gli utenti fanno clic su OK o su applica I controlli proprietà usano un commit immediato (le proprietà vengono modificate non appena gli utenti apportano modifiche), quindi non sono necessari i pulsanti OK, Annulla e applica.

## <a name="guidelines"></a>Indicazioni

### <a name="property-sheets"></a>Finestre delle proprietà

-   **Visualizza una finestra delle proprietà quando gli utenti:**
    -   Selezionare il comando proprietà per un oggetto.
    -   Impostare lo stato attivo per l'input su un oggetto e premere ALT + INVIO.

**Finestre delle proprietà di più oggetti**

-   **Visualizza le proprietà comuni di tutti gli oggetti selezionati.** Se i valori delle proprietà sono diversi, visualizzare i controlli associati a tali valori utilizzando uno stato misto. (Vedere le rispettive linee guida per il controllo per l'uso di valori di stato misto).
-   Se l'oggetto selezionato è una raccolta di più oggetti discreti, ad esempio una cartella di file, **visualizzare le proprietà del singolo oggetto raggruppato anziché una finestra delle proprietà di più oggetti per gli oggetti discreti.**

### <a name="options-dialog-boxes"></a>Finestre di dialogo Opzioni

-   **Non separare le opzioni dalla personalizzazione.** Ovvero, non si dispone sia di un comando Options che di un comando Customize. Spesso gli utenti sono confusi da questa separazione. In alternativa, accedere alla personalizzazione tramite opzioni.

### <a name="property-pages"></a>pagine delle proprietà

-   **Per l'ordine delle pagine, attenersi alle seguenti linee guida:**
    -   Rendere la pagina generale o l'equivalente della prima pagina.
    -   Rendere la pagina avanzata o l'equivalente dell'ultima pagina.
    -   Per le pagine rimanenti:
        -   Organizzarli in gruppi di pagine correlate.
        -   Ordinare i gruppi in base alla probabilità di utilizzo.
        -   All'interno di ogni gruppo, ordinare le pagine in base alle relazioni o alla probabilità di utilizzo.
        -   Non dovrebbe essere presente un numero così elevato di pagine che devono essere visualizzate in ordine alfabetico.
-   **Rendere coerenti le pagine correlando tutte le proprietà di ogni pagina a un singolo scopo specifico basato su attività.**
-   **Se lo spazio è consentito, spiegare lo scopo della finestra delle proprietà nella parte superiore della pagina, se non è ovvio per gli utenti di destinazione.** Se la pagina viene utilizzata per eseguire una sola attività, è **possibile formulare il testo come istruzioni chiare su come eseguire l'attività**. Utilizzare frasi complete che terminano con un punto.

    ![screenshot della finestra delle proprietà del firewall ](images/win-property-win-image2.png)

    In questo esempio, lo scopo di Microsoft Windows Firewall è illustrato nella parte superiore della pagina generale.

-   **Rendere contenuti simili coerenti tra le pagine usando nomi di controllo coerenti e posizioni.** Se, ad esempio, in più pagine sono presenti caselle nome, provare a posizionarle nella stessa posizione della pagina e utilizzare etichette coerenti. Il contenuto simile non dovrebbe rimbalzare da una pagina a una pagina.
-   **Inserire la stessa proprietà nella stessa pagina all'interno dell'applicazione.** Ad esempio, non inserire una proprietà di scadenza nella scheda generale per un tipo di oggetto e nella scheda avanzate per un altro tipo.
-   **Se è probabile che gli utenti inizino con l'ultima pagina visualizzata, rendere permanente la scheda della pagina e selezionarla per impostazione predefinita.** Rendere le impostazioni mantenute in una finestra per ogni proprietà, per ogni utente. In caso contrario, selezionare la prima pagina per impostazione predefinita.
-   **Non rendere le impostazioni in una pagina a seconda delle impostazioni di altre pagine.** In alternativa, inserire le impostazioni dipendenti in un'unica pagina. La modifica di un'impostazione in una pagina non deve mai modificare automaticamente le impostazioni in altre pagine.
    -   **Eccezione:** Se le impostazioni dipendenti si trovano in due finestre delle proprietà diverse, utilizzare le etichette di testo statiche per spiegare la relazione in entrambe le posizioni.
-   **Non scorrere le pagine delle proprietà.** Sia le schede che le barre di scorrimento vengono utilizzate per aumentare l'area effettiva di una finestra, ma un meccanismo dovrebbe essere sufficiente. Anziché utilizzare le barre di scorrimento, rendere le pagine delle proprietà più grandi e disporre le pagine in modo efficiente.

**Prime pagine**

-   Per le proprietà dell'oggetto, **inserire il nome dell'oggetto nella prima pagina.**
-   Se si associano [Icone](vis-icons.md) (facoltative) agli oggetti, **visualizzare l'icona appropriata nell'angolo superiore sinistro** della prima pagina.

**Pagine generali**

-   **Evitare le pagine generali.** Non è necessario disporre di una pagina generale. Utilizzare una pagina generale solo se:
    -   Le proprietà si applicano a diverse attività e sono significative per la maggior parte degli utenti. Non inserire proprietà specializzate o avanzate in una pagina generale, ma è possibile renderle accessibili tramite un pulsante di comando nella pagina generale.
    -   Le proprietà non rientrano in una categoria più specifica. In caso affermativo, usare invece questo nome per la pagina.

**Pagine avanzate**

-   **Evitare le pagine avanzate.** Usare una pagina avanzata solo se:
    -   Le proprietà si applicano alle attività non comuni e sono significative principalmente per gli utenti avanzati.
    -   Le proprietà non rientrano in una categoria più specifica. In caso affermativo, usare invece questo nome per la pagina.
-   **Non chiamare proprietà avanzate basate esclusivamente su misure tecnologiche.** Ad esempio, un'opzione di pinzatura della stampante può essere una funzionalità di stampa avanzata, ma è significativa per tutti gli utenti, quindi non deve trovarsi in una pagina avanzata.

### <a name="owned-property-windows"></a>Finestre delle proprietà di proprietà

-   **Non visualizzare più di una finestra delle proprietà di proprietà da una finestra delle proprietà.** La visualizzazione di più di uno rende il significato dei pulsanti OK e Annulla difficili da comprendere. È possibile visualizzare altri tipi di finestre di dialogo ausiliarie (ad esempio, selezione oggetti) in base alle esigenze.

    **Non corretto:**

    ![Screenshot di tre finestre delle proprietà di proprietà ](images/win-property-win-image3.png)

    In questo esempio, nella finestra di dialogo Opzioni proprietario sono disponibili tre livelli di finestre delle proprietà di proprietà. Di conseguenza, i significati di OK e Cancel sono confusi.

-   Per le finestre delle proprietà che utilizzano un modello con commit ritardato, **assicurarsi che gli utenti possano annullare le modifiche apportate in una finestra delle proprietà di proprietà facendo clic su Annulla nella finestra proprietario.**
-   Se una finestra delle proprietà di proprietà richiede un commit immediato, **indicare che è stato eseguito il commit delle modifiche rinominando il pulsante Annulla nella finestra proprietaria per chiuderla.** Ripristinare il pulsante per annullare se l'utente fa clic su Applica.

    ![screenshot della finestra delle proprietà con OK e Chiudi ](images/win-property-win-image4.png)

    In questo esempio non è possibile annullare le modifiche apportate ai dizionari personalizzati e alle impostazioni della grammatica. È possibile fornire agli utenti questo feedback modificando Annulla per chiudere.

**Altre finestre di proprietà**

-   Se per eseguire un'attività ausiliaria viene usata una finestra di proprietà, **non rinominare il pulsante Annulla.** Le linee guida precedenti si applicano solo alle finestre delle proprietà di proprietà, non alle finestre di dialogo utilizzate per eseguire attività ausiliarie.

    ![screenshot della finestra proprietaria e della pulizia del disco ](images/win-property-win-image5.png)

    In questo esempio, pulitura disco è un'attività ausiliaria, quindi le linee guida precedenti non si applicano. Il pulsante Annulla nella finestra proprietaria, ad esempio, non deve essere modificato per chiudere.

-   Se la finestra di proprietà viene utilizzata per eseguire un'attività ausiliaria, **non chiudere la finestra delle proprietà del proprietario quando si fa clic sul pulsante di comando.** Questa operazione sta disorientando e presuppone che l'unico motivo per cui l'utente ha visualizzato la finestra delle proprietà fosse l'esecuzione del comando.

    **Non corretto:**

    ![screenshot della finestra di dialogo Opzioni ](images/win-property-win-image6.png)

    In questo esempio, facendo clic su **Proteggi documento** si chiude in modo non corretto la finestra di dialogo Opzioni.

### <a name="tabs"></a>Schede

-   **Usare etichette di tabulazione concise.** Usare una o due parole che descrivano chiaramente il contenuto della pagina. Le etichette più lunghe comportano un utilizzo inefficiente dello spazio dello schermo, soprattutto quando le etichette sono localizzate.
-   **Usare etichette di tabulazioni specifiche e significative.** Evitare le etichette di schede generiche che possono essere applicate a qualsiasi scheda, ad esempio generale, avanzata o impostazioni.
-   **USA tabulazioni orizzontali se:**
    -   Nella finestra delle proprietà sono presenti sette o meno schede (incluse le estensioni di terze parti).
    -   **Tutte le schede si adattano a una riga, anche quando l'interfaccia utente è localizzata.**
    -   Le schede orizzontali vengono utilizzate nelle altre finestre delle proprietà dell'applicazione.
-   **Usare le schede verticali se:**

    -   La finestra delle proprietà dispone di otto o più schede (incluse le estensioni di terze parti).
    -   **L'utilizzo di schede orizzontali richiederebbe più di una riga.**
    -   Usare schede verticali nelle altre finestre delle proprietà dell'applicazione.

    ![screenshot della finestra delle proprietà con schede verticali ](images/win-property-win-image7.png)

    In questo esempio, le schede verticali vengono usate per ospitare otto o più schede.

-   **Per i controlli proprietà, per conservare spazio, è consigliabile usare un elenco a discesa anziché le schede**, soprattutto se la scheda corrente viene modificata raramente dall'utente.
-   **Se una scheda non si applica al contesto corrente e gli utenti non lo prevedono, rimuovere la scheda.** Questa operazione semplifica l'interfaccia utente e gli utenti non lo perdono.

    **Non corretto:**

    ![screenshot della scheda percorsi file in grigio ](images/win-property-win-image8.png)

    In questo esempio la scheda percorsi file è disabilitata in modo errato quando si usa Microsoft Word 2003 come editor di posta elettronica. La pagina deve essere rimossa perché gli utenti non si aspettano di visualizzare o modificare i percorsi dei file in questo contesto.

-   **Se una scheda non si applica al contesto corrente e gli utenti potrebbero aspettarsi di:**

    -   **Visualizzare la scheda.**
    -   **Disabilitare i controlli nella pagina.**
    -   **Includere il testo per spiegare il motivo per cui i controlli sono disabilitati.**

    Non disabilitare la scheda perché questa operazione non è intuitiva e impedisce l'esplorazione. Inoltre, gli utenti che cercano una proprietà specifica sono costretti a esaminare tutte le altre schede.

    ![screenshot dei controlli di visualizzazione in grigio ](images/win-property-win-image9.png)

    In questo esempio di Word 2003, nessuna delle opzioni di visualizzazione si applica nel layout di lettura. Tuttavia, gli utenti potrebbero aspettarsi che vengano applicati in base all'etichetta della scheda, in modo che la pagina venga visualizzata, ma le opzioni sono disabilitate.

-   **Non assegnare effetti alle schede modificate.** La modifica della scheda corrente non deve mai avere effetti collaterali, applicare le impostazioni o generare un messaggio di errore.
-   **Non annidare schede o combinare tabulazioni orizzontali con schede verticali.** Ridurre invece il numero di schede, utilizzare solo schede verticali oppure utilizzare un altro controllo, ad esempio un elenco a discesa.
-   **Non usare le schede se una finestra delle proprietà dispone di una sola scheda e non è estendibile.** Utilizzare una normale finestra di dialogo con OK, Annulla e un pulsante Applica facoltativo. Le finestre delle proprietà estendibili, che possono essere estese da terze parti, devono sempre usare le schede.
-   **Non inserire icone nelle schede.** Le icone in genere aggiungono confusione visiva superflua, utilizzano lo spazio dello schermo e spesso non migliorano la comprensione dell'utente. Aggiungere solo le icone che facilitano la comprensione, ad esempio i simboli standard.

    **Non corretto:**

    ![screenshot delle etichette di tabulazione con icone ](images/win-property-win-image10.png)

    In questo esempio, la grafica aggiunge confusione visiva superflua e poco per migliorare la comprensione dell'utente.

-   **Non usare i logo del prodotto per la scheda grafica.** Le schede non sono per la personalizzazione.
-   **Non scorrere le schede orizzontali.** Lo scorrimento orizzontale non è immediatamente individuabile. È tuttavia possibile scorrere le schede verticali.

    **Non corretto:**

    ![cattura di schermata dell'etichetta di tabulazione orizzontale troncata ](images/win-property-win-image11.png)

    In questo esempio vengono visualizzate le schede orizzontali.

### <a name="command-buttons"></a>Pulsanti di comando

-   **Posizionare i pulsanti di comando che si applicano a tutte le pagine delle proprietà nella parte inferiore della finestra delle proprietà.** Allinea a destra i pulsanti e usa questo ordine (da sinistra a destra): OK, Annulla e applica.
-   **Posizionare i pulsanti di comando che si applicano solo alle singole pagine delle proprietà direttamente nella pagina delle proprietà.**

### <a name="commit-buttons"></a>Pulsanti di commit

**Pulsanti OK**

-   **Per le finestre delle proprietà del proprietario, il pulsante OK significa applicare le modifiche in sospeso (effettuate dopo l'apertura della finestra o l'ultima applicazione) e chiudere la finestra.**
-   **Per le finestre delle proprietà di proprietà, il pulsante OK significa Mantieni le modifiche, chiude la finestra e applica le modifiche quando vengono applicate le modifiche della finestra proprietaria.**
-   **Non rinominare il pulsante OK.** A differenza di altre finestre di dialogo, le finestre delle proprietà non vengono usate per eseguire un'attività specifica. Se è opportuno rinominare il pulsante OK (ad esempio, per stampare), la finestra non è una finestra delle proprietà.
-   **Non assegnare una chiave di accesso.**

**Pulsanti Annulla**

-   **Il pulsante Annulla significa eliminare tutte le modifiche in sospeso (effettuate dopo l'apertura della finestra o l'ultima applicazione), quindi chiudere la finestra.**
-   **Se non è possibile abbandonare tutte le modifiche in sospeso, rinominare il pulsante Annulla per chiudere.** Se si fa clic su Annulla è necessario abbandonare tutte le modifiche in sospeso.
-   **Se la finestra delle proprietà di proprietà richiede un commit immediato, rinominare il pulsante Annulla nella finestra proprietaria per chiudere per mostrare che è stato eseguito il commit delle modifiche.**
-   **Non assegnare una chiave di accesso.**

**Pulsanti applica**

-   **Per le finestre delle proprietà del proprietario, il pulsante Applica significa applicare le modifiche in sospeso (effettuate dopo l'apertura della finestra o l'ultima applicazione), ma lasciare aperta la finestra.** Questa operazione consente agli utenti di valutare le modifiche prima di chiudere la finestra delle proprietà.
-   **Per le finestre delle proprietà di proprietà, non usare.** L'uso di un pulsante applica in una finestra delle proprietà di proprietà rende difficile comprendere il significato dei pulsanti di commit nella finestra delle proprietà del proprietario.
-   **Fornire un pulsante applica solo se la finestra delle proprietà contiene impostazioni (almeno una) con effetti che gli utenti possono valutare in modo significativo.** In genere, i pulsanti Applica vengono usati quando le impostazioni rendono visibili le modifiche. Gli utenti devono essere in grado di applicare una modifica, valutare la modifica e apportare ulteriori modifiche in base a tale valutazione. In caso contrario, rimuovere il pulsante Applica anziché disabilitarlo.

    **Non corretto:**

    ![screenshot delle proprietà di sistema con il pulsante applica ](images/win-property-win-image12.png)

    In questo esempio, nessuna delle proprietà di sistema ha un effetto visivo, quindi il pulsante applica non ha alcun valore e deve essere rimosso.

-   **Posizionare tutte le impostazioni che gli utenti potrebbero desiderare di applicare alle pagine proprietario.** Non usare i pulsanti applica nelle finestre delle proprietà di proprietà, perché questa operazione è confusa.
-   **Utilizzare i pulsanti applica solo con le finestre delle proprietà, non con le finestre di dialogo Opzioni.**
-   **Abilitare il pulsante applica solo quando sono presenti modifiche in sospeso**; in caso contrario, disabilitarlo.
-   **Assegnare "A" come chiave di accesso.**

**Chiudi pulsanti**

-   **Se non è possibile abbandonare tutte le modifiche in sospeso, rinominare il pulsante Annulla per chiudere.** Se si fa clic su Annulla è necessario abbandonare tutte le modifiche in sospeso.
-   **Non confermare se gli utenti ignorano le modifiche.**
    -   **Eccezione:** Se nella finestra delle proprietà sono presenti impostazioni che richiedono un impegno significativo per l'impostazione e l'utente ha apportato modifiche, è possibile che venga visualizzata una [conferma](mess-confirm.md) se l'utente fa clic sul pulsante Chiudi sulla barra del titolo. Il motivo è che alcuni utenti presuppongono erroneamente che il pulsante Chiudi sulla barra del titolo abbia lo stesso effetto del pulsante OK.
-   **Ad eccezione del messaggio di conferma, verificare che il pulsante Chiudi sulla barra del titolo abbia lo stesso effetto di Annulla o Chiudi.**

### <a name="page-contents"></a>Contenuto della pagina

-   **Verificare che le proprietà siano necessarie.** Non ingombra le pagine con proprietà non necessarie solo per evitare di prendere decisioni di progettazione difficili.
-   **Presentare le proprietà in termini di obiettivi utente, non della tecnologia.** Solo perché una proprietà configura una tecnologia specifica non significa che è necessario presentare la proprietà in termini di tale tecnologia.
    -   Se è necessario presentare le impostazioni in termini di tecnologia (forse perché gli utenti riconoscono il nome della tecnologia), includere una breve descrizione del modo in cui l'utente trae vantaggio da tale impostazione.
-   **Presentare le proprietà al livello corretto.** Non è necessario presentare singole impostazioni di basso livello in una pagina delle proprietà, quindi presentare le proprietà a un livello appropriato per gli utenti.
-   **Progettare le pagine delle proprietà per attività specifiche.** Determinare le attività che gli utenti eseguiranno e assicurarsi che esista un percorso chiaro per eseguire tali attività.
-   **Organizzare le pagine delle proprietà in modo efficiente** riducendo il numero di schede, decidendo cosa accade in una pagina in base al raggruppamento logico e alla coerenza e semplificando la presentazione della pagina.

<!-- -->

-   **Se un'opzione è fortemente consigliata, provare ad aggiungere "(scelta consigliata)" all'etichetta.**
-   **Specificare un pulsante di comando Ripristina impostazioni predefinite per una pagina delle proprietà o l'intera finestra delle proprietà quando:**

    -   È probabile che gli utenti considerino le impostazioni complesse e difficili da comprendere.
    -   La presenza di impostazioni errate può comportare una funzionalità di rilievo, ma i valori predefiniti possono ripristinare la funzionalità.
    -   È più facile per gli utenti ricominciare quando l'oggetto non è configurato correttamente.

    ![screenshot della scheda con il pulsante Ripristina impostazioni predefinite ](images/win-property-win-image13.png)

    In questo esempio, le impostazioni del Windows Firewall sono complesse e possono causare funzionalità interrotte. Se si verifica un problema, è spesso più facile per gli utenti ricominciare facendo clic su Ripristina impostazioni predefinite.

-   Verificare il comando Ripristina impostazioni predefinite se l'effetto non è ovvio o se le impostazioni sono complesse. Indica la conferma tramite [ellissi](ctrl-command-buttons.md).
-   **Quando appropriato, visualizzare un'anteprima dei risultati di un'impostazione.**

    ![screenshot delle proprietà del mouse esempi di puntatore ](images/win-property-win-image14.png)

    In questo esempio, nella pagina viene visualizzata un'anteprima degli schemi del puntatore. Quando si fa clic su Applica, viene visualizzata anche un'anteprima e l'anteprima della pagina è più efficiente per gli utenti.

    ![screenshot dell'anteprima dei risultati delle impostazioni del tipo di carattere ](images/win-property-win-image15.png)

    In questo esempio, la casella Anteprima Mostra i risultati delle impostazioni del tipo di carattere. Questo esempio mostra che è possibile visualizzare in anteprima le impostazioni che non sono grafiche.

### <a name="help"></a>Help

-   Per fornire assistenza agli utenti, **provare a usare le opzioni seguenti** (elencate nell'ordine di preferenza):
    -   Assegnare etichette interattive ai controlli. È più probabile che gli utenti leggano le etichette sui controlli interattivi rispetto a qualsiasi altro testo.
    -   Fornire spiegazioni nel contesto usando etichette di testo statiche.
    -   Fornire un [collegamento](ctrl-links.md) specifico a un argomento della Guida pertinente.
-   **Individuare i collegamenti della guida nella parte inferiore di ogni pagina.** Se una pagina include diversi gruppi distinti di impostazioni che includono un argomento della guida (forse all'interno di caselle di gruppo), individuare il collegamento alla guida nella parte inferiore del gruppo.
-   **Non usare collegamenti all'argomento della Guida generici o vaghi o pulsanti della Guida generici.** Spesso gli utenti ignorano la guida generica.

Per ulteriori informazioni ed esempi, vedere la [Guida](winenv-help.md)di.

### <a name="standard-users-and-protected-administrators"></a>Utenti standard e amministratori protetti

**Per la modifica di molte impostazioni sono necessari privilegi di amministratore.** Se un processo richiede privilegi di amministratore, Windows e versioni successive richiedono che [gli utenti standard e gli](glossary.md) [amministratori protetti](glossary.md) possano elevare i propri privilegi in modo esplicito. Questa operazione consente di impedire l'esecuzione di codice dannoso con privilegi di amministratore.

Per ulteriori informazioni ed esempi, vedere [controllo dell'account utente](winenv-uac.md).

### <a name="default-values"></a>Valori predefiniti

-   **Le impostazioni all'interno di una finestra delle proprietà devono riflettere lo stato corrente dell'applicazione, dell'oggetto o della raccolta di oggetti.** In caso contrario, potrebbe essere fuorviante e potrebbe causare risultati indesiderati. Se, ad esempio, le impostazioni riflettono le raccomandazioni ma non lo stato corrente, gli utenti potrebbero fare clic su Annulla anziché apportare modifiche, pensando che non sono necessarie modifiche.
-   **Scegliere il più sicuro (per evitare la perdita di dati o l'accesso al sistema) e lo stato iniziale più sicuro.** Si supponga che la maggior parte degli utenti non modifichi le impostazioni.
-   **Se la sicurezza e la sicurezza non sono fattori, scegliere lo stato iniziale più probabile o pratico.**

## <a name="text"></a>Testo

### <a name="commands"></a>Comandi

-   Per visualizzare le opzioni di programma, usare "Opzioni".
-   Per visualizzare la finestra delle proprietà di un oggetto, usare "Properties".
-   Per visualizzare un riepilogo delle impostazioni di personalizzazione del programma usate di frequente, usare "[Personalizza](glossary.md)".
-   Non usare "Impostazioni" o "Preferenze".
-   Non usare [ellissi](ctrl-command-buttons.md) per questi comandi.

### <a name="property-sheet-titles"></a>Titoli della finestra delle proprietà

-   Per un singolo oggetto, usare " \[ proprietà nome oggetto \] ".
    -   Se l'oggetto non dispone di un nome, utilizzare il nome del tipo dell'oggetto. Ad esempio, le proprietà dell'account utente.
-   Per più oggetti, usare il \[ nome di primo oggetto \] ,... Proprietà ".
    -   Se gli oggetti non hanno nomi, usare il nome del tipo degli oggetti. Ad esempio, le proprietà degli account utente.
    -   Se gli oggetti hanno tipi diversi, usare "proprietà selezione".
-   Usare l'uso [di maiuscole in stile titolo](glossary.md).
-   Non usare punteggiatura finale.
-   Non usare trattini, ad esempio " \[ nome oggetto \] -Proprietà".

### <a name="property-inspector-titles"></a>Titoli di controllo proprietà

-   Usare "proprietà".
-   Usare l'uso di maiuscole in stile titolo.
-   Non usare punteggiatura finale.

### <a name="options-dialog-box-titles"></a>Titoli della finestra di dialogo Opzioni

-   Usare "Opzioni".
-   Usare l'uso di maiuscole in stile titolo.
-   Non usare punteggiatura finale.

### <a name="property-page-tab-names"></a>Nomi delle schede della pagina delle proprietà

-   **Usare etichette di tabulazione concise.** Usare una o due parole che descrivano chiaramente il contenuto della pagina. L'utilizzo di nomi di schede più lunghi comporta un uso inefficiente dello spazio dello schermo, soprattutto quando i nomi delle schede sono localizzati.
-   **Usare etichette di tabulazioni specifiche e significative.** Evitare le etichette di schede generiche che possono essere applicate a qualsiasi scheda, ad esempio generale, avanzata o impostazioni.
-   Scrivere l'etichetta come frase a una o due parole e non usare la punteggiatura finale.
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Non assegnare una [chiave di accesso](glossary.md)univoca.

### <a name="property-page-text"></a>Testo della pagina delle proprietà

-   Evitare blocchi di testo di grandi dimensioni.
-   Fornire spazio sufficiente per il testo per espandere il 30% se verrà localizzato.
-   Non usare il testo formulato come comando nelle finestre delle proprietà. Poiché gli utenti potrebbero voler semplicemente visualizzare le impostazioni, non è necessario richiedere loro di modificare le impostazioni.
-   Usare le maiuscole e la punteggiatura finale.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle finestre delle proprietà:

-   In programmazione e altri documenti tecnici, fare riferimento alle finestre delle proprietà e alle finestre di dialogo delle opzioni come finestre delle proprietà. Ovunque, usare la finestra di dialogo, in particolare nella documentazione dell'utente.
-   Usare il testo del titolo esatto, inclusa la relativa maiuscola.
-   Per descrivere l'interazione dell'utente, usare Open e Close.
-   Quando possibile, formattare il titolo usando il testo in grassetto. In caso contrario, inserire il titolo racchiuso tra virgolette solo se necessario per evitare confusione.

Quando si fa riferimento alle pagine delle proprietà:

-   In programmazione e altri documenti tecnici, fare riferimento alle pagine delle proprietà come pagine delle proprietà. In tutti gli altri casi, usare la scheda, in particolare nella documentazione dell'utente.
-   Usare il testo del titolo esatto, inclusa la relativa maiuscola.
-   Per descrivere l'interazione dell'utente, utilizzare fare clic per fare clic su una scheda.
-   Quando possibile, formattare il nome usando il testo in grassetto. In caso contrario, inserire il nome tra virgolette solo se necessario per evitare confusione.

 

 