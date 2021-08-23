---
title: Proprietà Windows
description: La finestra delle proprietà è il nome collettivo per i tipi seguenti di finestre delle proprietà delle interfacce utente usate per visualizzare e modificare le proprietà di un oggetto o di una raccolta di oggetti in una finestra di dialogo. Controllo proprietà usato per visualizzare e modificare le proprietà di un oggetto o di una raccolta di oggetti in un riquadro. Finestra di dialogo Opzioni utilizzata per visualizzare e modificare le opzioni per un'applicazione.
ms.assetid: 18fc04da-9f84-4a44-9f3d-a9e29b121e7c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 73260459c1dc22ee488233f3c7edebe25203a811a430870fdd4e68e1c2e153ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594384"
---
# <a name="property-windows"></a>Proprietà Windows

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

La finestra delle proprietà è il nome collettivo per i tipi di interfacce utente seguenti:

-   Finestra delle proprietà: usata per **visualizzare e modificare le proprietà di un oggetto o di una raccolta di oggetti in una finestra di dialogo.**
-   Controllo proprietà: usato per **visualizzare e modificare le proprietà di un oggetto o di una raccolta di oggetti in un riquadro**.
-   Finestra di dialogo Opzioni: usata per **visualizzare e modificare le opzioni per un'applicazione.**

Una proprietà per un oggetto è una delle seguenti:

-   Impostazione che gli utenti possono modificare, ad esempio il nome di un file e l'attributo di sola lettura.
-   Attributo di un oggetto che gli utenti non possono modificare direttamente, ad esempio le dimensioni e la data di creazione di un file.

A differenza delle finestre di dialogo (diverse dalle finestre di dialogo di opzioni) e delle procedure guidate, le finestre delle proprietà supportano in genere diverse attività anziché una singola attività.

Le finestre delle proprietà sono in genere organizzate in pagine a cui si accede tramite schede. Le finestre delle proprietà sono spesso associate alle schede (e viceversa), ma le schede **non sono essenziali per le finestre delle proprietà.**

![Screenshot della finestra delle proprietà delle proprietà del documento ](images/win-property-win-image1.png)

Una tipica finestra delle proprietà.

**Nota:** Le linee guida relative [al layout](vis-layout.md) e [alle schede](ctrl-tabs.md) sono presentate in articoli separati.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Per decidere, prendi in considerazione queste domande:

-   **L'impostazione delle proprietà richiede agli utenti di eseguire una sequenza di passaggi fissa e non semplice?** In tal caso, usare invece una [procedura guidata](win-wizards.md) [o un flusso di](glossary.md) attività.
-   **Il contenuto è esclusivamente un'opzione di un'applicazione?** In tal caso, usare una finestra di dialogo di opzioni.
-   **Il contenuto è esclusivamente attributi di un'applicazione?** In tal caso, usare una [casella Informazioni su](glossary.md).
-   **Il contenuto è principalmente delle proprietà di un oggetto (impostazioni o attributi)?** In caso contrario, usare una finestra [di dialogo](win-dialog-box.md) standard o una finestra di dialogo [a schede](glossary.md).
-   È probabile **che gli utenti visualizzano o modificano le proprietà di frequente o in un periodo di tempo prolungato?** In tal caso, usare un controllo proprietà. In caso contrario, utilizzare una finestra delle proprietà.
-   È probabile **che gli utenti visualizzano o modino le proprietà per diversi oggetti contemporaneamente?** In tal caso, usare un controllo proprietà. In caso contrario, utilizzare una finestra delle proprietà.

**Le finestre delle proprietà e i controlli proprietà non sono esclusivi.** È possibile visualizzare le proprietà a cui si accede più di frequente in un controllo proprietà e il set completo nella finestra delle proprietà.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

**Le finestre delle proprietà spesso diventano un dumping per un'ampia gamma di impostazioni di basso livello basate sulla tecnologia.** Troppo spesso queste proprietà sono organizzate in schede, ma non sono progettate per attività o utenti specifici. Di conseguenza, quando gli utenti devono affrontare un'attività in una finestra delle proprietà, spesso non sanno cosa fare.

Per assicurarsi che le finestre delle proprietà siano utili e utilizzabili, seguire questa procedura:

-   Assicurarsi che le proprietà siano necessarie.
-   Presentare le proprietà in termini di obiettivi dell'utente, non di tecnologia.
-   Presentare le proprietà al livello giusto.
-   Progettare pagine per attività specifiche.
-   Progettare pagine per utenti specifici, in particolare utenti limitati (non amministratori).
-   Organizzare le pagine delle proprietà in modo efficiente.

**Se si fa una sola cosa...**

Presentare le proprietà in termini di obiettivi dell'utente, non di tecnologia. Si presenti di spiegare la proprietà e il motivo per cui è utile per un amico. Come è possibile spiegarlo? Quale linguaggio si userebbe? Questo è il linguaggio da usare nelle pagine delle proprietà.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le finestre delle proprietà hanno diversi modelli di utilizzo.

-   Finestre delle proprietà. Le proprietà di un singolo oggetto vengono visualizzate in una finestra di dialogo non modabile.
-   Finestre delle proprietà con più oggetti. Le proprietà per più oggetti vengono visualizzate in una finestra di dialogo non modabile.
-   Finestre delle proprietà delle impostazioni effettive. Le proprietà effettive per un singolo oggetto vengono visualizzate in una finestra di dialogo non modabile.
-   Finestre di dialogo opzioni. Le proprietà di un'applicazione vengono visualizzate in una finestra di dialogo modale.
-   Controlli delle proprietà. Le proprietà per la selezione corrente (un singolo oggetto o gruppo di oggetti) vengono visualizzate in un riquadro della finestra non modabile o in una finestra non ancorata.

Tutti i modelli di finestra delle proprietà, ad eccezione dei controlli proprietà, usano un commit ritardato, vale a dire che le modifiche vengono applicate solo quando gli utenti selezionano OK o Applica. I controlli proprietà usano un commit immediato (le proprietà vengono modificate non appena gli utenti apportano modifiche), quindi non è necessario usare i pulsanti OK, Annulla e Applica.

## <a name="guidelines"></a>Indicazioni

### <a name="property-sheets"></a>Finestre delle proprietà

-   **Visualizzare una finestra delle proprietà quando gli utenti:**
    -   Selezionare il comando Proprietà per un oggetto.
    -   Impostare lo stato attivo per l'input su un oggetto e premere ALT+INVIO.

**Finestre delle proprietà con più oggetti**

-   **Consente di visualizzare le proprietà comuni di tutti gli oggetti selezionati.** Se i valori della proprietà sono diversi, visualizzare i controlli associati a tali valori usando uno stato misto. Vedere le rispettive linee guida per i controlli per l'uso di valori di stato misto.
-   Se l'oggetto selezionato è una raccolta di più oggetti discreti, ad esempio una cartella di file, visualizzare le proprietà del singolo oggetto raggruppato anziché una finestra delle proprietà a più oggetti per gli oggetti **discreti.**

### <a name="options-dialog-boxes"></a>Finestre di dialogo Opzioni

-   **Non separare le opzioni dalla personalizzazione.** Ciò significa che non sono disponibili sia un comando Options che un comando Customize. Gli utenti sono spesso confusi da questa separazione. Accedere invece alla personalizzazione tramite le opzioni.

### <a name="property-pages"></a>pagine delle proprietà

-   **Seguire queste linee guida per l'ordine delle pagine:**
    -   Impostare la pagina Generale o l'equivalente come prima pagina.
    -   Impostare la pagina Avanzate o l'equivalente come ultima pagina.
    -   Per le pagine rimanenti:
        -   Organizzarli in gruppi di pagine correlate.
        -   Ordinare i gruppi in base alla probabilità di utilizzo.
        -   All'interno di ogni gruppo ordinare le pagine in base alle relazioni o in base alla probabilità di utilizzo.
        -   Non è necessario avere così tante pagine che è necessario visualizzarle in ordine alfabetico.
-   **Rendere coerenti le pagine facendo in modo che tutte le proprietà di ogni pagina si relazionano a un unico scopo specifico basato su attività.**
-   **Se lo spazio lo consente, spiegare lo scopo della finestra delle proprietà nella parte superiore della pagina se non è ovvio per gli utenti di destinazione.** Se la pagina viene usata per eseguire una sola attività, formulare il testo come un'istruzione chiara su **come eseguire tale attività.** Usare frasi complete, che terminano con un punto.

    ![Screenshot della finestra delle proprietà delle proprietà del firewall ](images/win-property-win-image2.png)

    In questo esempio lo scopo di Microsoft Windows Firewall è illustrato nella parte superiore della pagina Generale.

-   **Rendere coerente contenuto simile tra le pagine usando percorsi e nomi di controllo coerenti.** Ad esempio, se in più pagine sono presenti caselle Nome, provare a posizionarle nella stessa posizione della pagina e usare etichette coerenti. Contenuto simile non dovrebbe essere in grado di spostarsi da una pagina all'altro.
-   **Posizionare la stessa proprietà nella stessa pagina dell'applicazione.** Ad esempio, non inserire una proprietà Expiration nella scheda Generale per un tipo di oggetto e nella scheda Avanzate per un altro tipo.
-   **Se è probabile che gli utenti inizino con l'ultima pagina visualizzata, rendere persistente la scheda della pagina e selezionarla per impostazione predefinita.** Rendere persistenti le impostazioni in una finestra per proprietà, per utente. In caso contrario, selezionare la prima pagina per impostazione predefinita.
-   **Non rendere le impostazioni in una pagina dipendenti dalle impostazioni di altre pagine.** Inserire invece le impostazioni dipendenti in una singola pagina. La modifica di un'impostazione in una pagina non dovrebbe mai cambiare automaticamente le impostazioni in altre pagine.
    -   **Eccezione:** Se le impostazioni dipendenti sono in due finestre di proprietà diverse, usare etichette di testo statiche per spiegare questa relazione in entrambe le posizioni.
-   **Non scorrere le pagine delle proprietà.** Sia le schede che le barre di scorrimento vengono usate per aumentare l'area effettiva di una finestra, ma un meccanismo dovrebbe essere sufficiente. Invece di usare le barre di scorrimento, è possibile ingrandire le pagine delle proprietà e disaziare le pagine in modo efficiente.

**Prime pagine**

-   Per le proprietà **dell'oggetto, inserire il nome dell'oggetto nella prima pagina.**
-   Se si associano icone [](vis-icons.md) (facoltative) agli oggetti, visualizzare l'icona appropriata nell'angolo **superiore** sinistro della prima pagina.

**Pagine generali**

-   **Evitare le pagine Generali.** Non è necessario avere una pagina Generale. Usare una pagina Generale solo se:
    -   Le proprietà si applicano a diverse attività e sono significative per la maggior parte degli utenti. Non inserire proprietà specializzate o avanzate in una pagina Generale, ma è possibile renderle accessibili tramite un pulsante di comando nella pagina Generale.
    -   Le proprietà non rientrano in una categoria più specifica. In caso contrario, usare tale nome per la pagina.

**Pagine avanzate**

-   **Evitare pagine avanzate.** Usare una pagina Avanzate solo se:
    -   Le proprietà si applicano ad attività non comuni e sono significative principalmente per gli utenti avanzati.
    -   Le proprietà non rientrano in una categoria più specifica. In caso contrario, usare tale nome per la pagina.
-   **Non chiamare proprietà avanzate basate esclusivamente su misure tecnologiche.** Ad esempio, un'opzione di graffatura della stampante può essere una funzionalità avanzata della stampante, ma è significativa per tutti gli utenti, quindi non deve essere in una pagina Avanzate.

### <a name="owned-property-windows"></a>Finestre delle proprietà di proprietà

-   **Non visualizzare più finestre delle proprietà di proprietà da una finestra delle proprietà.** La visualizzazione di più di uno rende difficile comprendere il significato dei pulsanti OK e Annulla. È possibile visualizzare altri tipi di finestre di dialogo ausiliarie, ad esempio i selettori di oggetti, in base alle esigenze.

    **Non corretto:**

    ![Screenshot di tre finestre delle proprietà di proprietà ](images/win-property-win-image3.png)

    In questo esempio, la finestra di dialogo delle opzioni del proprietario ha tre livelli di finestre delle proprietà di proprietà. Di conseguenza, i significati di OK e Cancel confondono.

-   Per le finestre delle proprietà che usano un modello di commit ritardato, assicurarsi che gli utenti possano annullare le modifiche apportate in una finestra delle proprietà di proprietà facendo clic su **Annulla nella finestra proprietaria.**
-   Se una finestra delle proprietà di proprietà richiede un commit immediato, indicare che è stato eseguito il commit delle modifiche rinominando il pulsante Annulla nella finestra **proprietaria su Chiudi.** Ripristinare il pulsante su Annulla se l'utente fa clic su Applica.

    ![Screenshot della finestra delle proprietà con OK e chiudi ](images/win-property-win-image4.png)

    In questo esempio le modifiche ai dizionari personalizzati e alle impostazioni grammaticali non possono essere annullate. È possibile inviare questo feedback agli utenti impostando Annulla su Chiudi.

**Altre finestre di proprietà**

-   Se viene usata una finestra di proprietà per eseguire **un'attività** ausiliaria, non rinominare il pulsante Annulla. Le linee guida precedenti si applicano solo alle finestre delle proprietà di proprietà, non alle finestre di dialogo usate per eseguire attività ausiliarie.

    ![Screenshot della finestra del proprietario e della pulizia del disco ](images/win-property-win-image5.png)

    In questo esempio Pulizia disco è un'attività ausiliaria, quindi le linee guida precedenti non si applicano. Ad esempio, il pulsante Annulla nella finestra proprietaria non deve essere modificato in Chiudi.

-   Se la finestra di proprietà viene usata per eseguire **un'attività** ausiliaria, non chiudere la finestra delle proprietà del proprietario quando si fa clic sul pulsante di comando. In questo modo si disorienta e si presuppone che l'unico motivo per cui l'utente ha visualizzato la finestra delle proprietà fosse eseguire tale comando.

    **Non corretto:**

    ![Screenshot della finestra di dialogo Opzioni ](images/win-property-win-image6.png)

    In questo esempio, se si **fa clic su Proteggi documento in** modo non corretto, la finestra di dialogo Opzioni viene chiusa.

### <a name="tabs"></a>Schede

-   **Usare etichette di tabulazione concise.** Usare una o due parole che descrivono chiaramente il contenuto della pagina. Le etichette più lunghe comportano un uso inefficiente dello spazio dello schermo, soprattutto quando le etichette sono localizzate.
-   **Usare etichette di tabulazione specifiche e significative.** Evitare etichette di tabulazione generiche che potrebbero essere applicate a qualsiasi scheda, ad esempio Generale, Avanzate o Impostazioni.
-   **Usare le schede orizzontali se:**
    -   La finestra delle proprietà include sette o meno schede (incluse le estensioni di terze parti).
    -   **Tutte le schede si adattano a una riga, anche quando l'interfaccia utente è localizzata.**
    -   È possibile usare schede orizzontali nelle altre finestre delle proprietà dell'applicazione.
-   **Usare le tabulazioni verticali se:**

    -   La finestra delle proprietà include otto o più schede , incluse le estensioni di terze parti.
    -   **L'uso di schede orizzontali richiederebbe più di una riga.**
    -   È possibile usare schede verticali nelle altre finestre delle proprietà dell'applicazione.

    ![Screenshot della finestra delle proprietà con schede verticali ](images/win-property-win-image7.png)

    In questo esempio le schede verticali vengono usate per contenere otto o più schede.

-   **Per i controlli proprietà,** per risparmiare spazio, è consigliabile usare un elenco a discesa anziché schede, soprattutto se la scheda corrente viene modificata raramente dall'utente.
-   Se una scheda non si applica al contesto corrente e gli utenti non lo **prevedono, rimuovere la scheda.** Questa operazione semplifica l'interfaccia utente e gli utenti non mancheranno.

    **Non corretto:**

    ![Screenshot della scheda Percorsi file in grigio ](images/win-property-win-image8.png)

    In questo esempio la scheda Percorsi file viene disabilitata in modo errato Microsoft Word 2003 come editor di posta elettronica. La pagina deve essere rimossa perché gli utenti non si aspetterebbe di visualizzare o modificare i percorsi dei file in questo contesto.

-   **Se una scheda non si applica al contesto corrente e gli utenti potrebbero aspettarsi che:**

    -   **Visualizzare la scheda .**
    -   **Disabilitare i controlli nella pagina.**
    -   **Includere il testo che spiega perché i controlli sono disabilitati.**

    Non disabilitare la scheda perché questa operazione non è auto-esplicativa e impedisce l'esplorazione. Inoltre, gli utenti che cercano una proprietà specifica verrebbero costretti a cercare tutte le altre schede.

    ![Screenshot dei controlli di visualizzazione in grigio ](images/win-property-win-image9.png)

    In questo esempio di Word 2003 nessuna delle opzioni Di visualizzazione è applicabile in Layout di lettura. Tuttavia, gli utenti potrebbero aspettarsi che siano applicati in base all'etichetta della scheda, quindi la pagina viene visualizzata ma le opzioni sono disabilitate.

-   **Non assegnare effetti alla modifica delle schede.** La modifica della scheda corrente non dovrebbe mai avere effetti collaterali, applicare le impostazioni o causare un messaggio di errore.
-   **Non annidare le schede o combinare le schede orizzontali con le schede verticali.** Ridurre invece il numero di schede, usare solo le schede verticali o usare un altro controllo, ad esempio un elenco a discesa.
-   **Non usare le schede se una finestra delle proprietà ha una sola scheda e non è estendibile.** Usare una normale finestra di dialogo con OK, Annulla e un pulsante Applica facoltativo. Le finestre delle proprietà estendibili (che possono essere estese da terze parti) devono sempre usare le schede.
-   **Non inserire icone nelle schede.** Le icone in genere aggiungono confusione visiva non necessaria, consumano spazio sullo schermo e spesso non migliorano la comprensione dell'utente. Aggiungere solo icone che sono di aiuto per la comprensione, ad esempio i simboli standard.

    **Non corretto:**

    ![Screenshot delle etichette delle schede con icone ](images/win-property-win-image10.png)

    In questo esempio, la grafica aggiunge confusione visiva non necessaria e fa poco per migliorare la comprensione dell'utente.

-   **Non usare i logo del prodotto per la grafica delle schede.** Le schede non sono per la personalizzazione.
-   **Non scorrere le schede orizzontali.** Lo scorrimento orizzontale non è facilmente individuabile. È tuttavia possibile scorrere le schede verticali.

    **Non corretto:**

    ![Screenshot dell'etichetta della scheda orizzontale troncata ](images/win-property-win-image11.png)

    In questo esempio vengono scorrete le schede orizzontali.

### <a name="command-buttons"></a>Pulsanti di comando

-   **Posizionare i pulsanti di comando che si applicano a tutte le pagine delle proprietà nella parte inferiore della finestra delle proprietà.** Allineare a destra i pulsanti e usare questo ordine (da sinistra a destra): OK, Annulla e Applica.
-   **Posizionare i pulsanti di comando che si applicano solo alle singole pagine delle proprietà direttamente nella pagina delle proprietà.**

### <a name="commit-buttons"></a>Pulsanti di commit

**Pulsanti OK**

-   **Per le finestre delle proprietà del proprietario, il pulsante OK significa applicare le modifiche in sospeso (apportate dopo l'apertura della finestra o l'ultima applicazione) e chiudere la finestra.**
-   **Per le finestre delle proprietà di proprietà, il pulsante OK significa mantenere le modifiche, chiudere la finestra e applicare le modifiche quando vengono applicate le modifiche della finestra proprietaria.**
-   **Non rinominare il pulsante OK.** A differenza di altre finestre di dialogo, le finestre delle proprietà non vengono usate per eseguire un'attività specifica. Se è opportuno rinominare il pulsante OK (ad esempio stampa), la finestra non è una finestra delle proprietà.
-   **Non assegnare una chiave di accesso.**

**Pulsanti Annulla**

-   **Il pulsante Annulla indica l'eliminazione di tutte le modifiche in sospeso (apportate dopo l'apertura della finestra o l'ultima applicazione) e la chiusura della finestra.**
-   **Se non è possibile abbandonare tutte le modifiche in sospeso, rinominare il pulsante Annulla in Chiudi.** Facendo clic su Annulla è necessario abbandonare tutte le modifiche in sospeso.
-   **Se la finestra delle proprietà di proprietà richiede un commit immediato, rinominare il pulsante Annulla nella finestra proprietaria in Chiudi per mostrare che è stato eseguito il commit delle modifiche.**
-   **Non assegnare una chiave di accesso.**

**Applicare pulsanti**

-   **Per le finestre delle proprietà del proprietario, il pulsante Applica significa applicare le modifiche in sospeso (apportate dopo l'apertura della finestra o l'ultima applicazione), ma lasciare aperta la finestra.** Questa operazione consente agli utenti di valutare le modifiche prima di chiudere la finestra delle proprietà.
-   **Per le finestre delle proprietà di proprietà, non usare .** L'uso di un pulsante Applica in una finestra delle proprietà di proprietà rende difficile comprendere il significato dei pulsanti di commit nella finestra delle proprietà del proprietario.
-   **Specificare un pulsante Applica solo se nella finestra delle proprietà sono presenti impostazioni (almeno una) con effetti che gli utenti possono valutare in modo significativo.** In genere, i pulsanti Applica vengono usati quando le impostazioni apportano modifiche visibili. Gli utenti devono essere in grado di applicare una modifica, valutare la modifica e apportare altre modifiche in base a tale valutazione. In caso contrario, rimuovere il pulsante Applica anziché disabilitarlo.

    **Non corretto:**

    ![Screenshot delle proprietà di sistema con il pulsante Applica ](images/win-property-win-image12.png)

    In questo esempio nessuna delle proprietà di sistema ha un effetto visivo, quindi il pulsante Applica non ha alcun valore e deve essere rimosso.

-   **Inserire tutte le impostazioni che gli utenti potrebbero voler applicare nelle pagine proprietarie.** Non usare i pulsanti Applica nelle finestre delle proprietà di proprietà, perché questa operazione crea confusione.
-   **Usare Applica pulsanti solo con le finestre delle proprietà, non con le finestre di dialogo delle opzioni.**
-   **Abilitare il pulsante Applica solo in caso di modifiche in sospeso.** In caso contrario, disabilitarlo.
-   **Assegnare "A" come chiave di accesso.**

**Pulsanti di chiusura**

-   **Se non è possibile abbandonare tutte le modifiche in sospeso, rinominare il pulsante Annulla in Chiudi.** Facendo clic su Annulla è necessario abbandonare tutte le modifiche in sospeso.
-   **Non verificare se gli utenti annullano le modifiche.**
    -   **Eccezione:** Se nella finestra delle proprietà sono disponibili impostazioni che richiedono un impegno [](mess-confirm.md) significativo per l'impostazione e l'utente ha apportato modifiche, è possibile visualizzare una conferma se l'utente fa clic sul pulsante Chiudi sulla barra del titolo. Il motivo è che alcuni utenti presuppongono erroneamente che il pulsante Chiudi sulla barra del titolo abbia lo stesso effetto del pulsante OK.
-   **Ad eccezione del messaggio di conferma, assicurarsi che il pulsante Chiudi sulla barra del titolo abbia lo stesso effetto di Annulla o Chiudi.**

### <a name="page-contents"></a>Contenuto della pagina

-   **Assicurarsi che le proprietà siano necessarie.** Non ingombrare le pagine con proprietà non necessarie solo per evitare di prendere decisioni di progettazione difficili.
-   **Presentare le proprietà in termini di obiettivi dell'utente, non di tecnologia.** Solo perché una proprietà configura una tecnologia specifica non significa che è necessario presentare la proprietà in termini di tale tecnologia.
    -   Se è necessario presentare le impostazioni in termini di tecnologia,ad esempio perché gli utenti riconoscono il nome della tecnologia, includere una breve descrizione del modo in cui l'utente trae vantaggio da tale impostazione.
-   **Presentare le proprietà al livello giusto.** Non è necessario presentare singole impostazioni di basso livello in una pagina delle proprietà, quindi presentare le proprietà a un livello più sensato per gli utenti.
-   **Progettare pagine delle proprietà per attività specifiche.** Determinare le attività che gli utenti eseguiranno e assicurarsi che sia disponibile un percorso chiaro per eseguire tali attività.
-   **Organizzare le pagine** delle proprietà in modo efficiente riducendo il numero di schede, decidendo cosa fare in una pagina in base al raggruppamento logico e alla coerenza e semplificando la presentazione della pagina.

<!-- -->

-   **Se un'opzione è fortemente consigliata, è consigliabile aggiungere "(scelta consigliata)" all'etichetta.**
-   **Specificare un pulsante di comando Ripristina impostazioni predefinite per una pagina delle proprietà o l'intera finestra delle proprietà quando:**

    -   È probabile che gli utenti considerino le impostazioni complesse e difficili da comprendere.
    -   La presenza di impostazioni errate può causare un'interruzione della funzionalità, ma le impostazioni predefinite potrebbero ripristinare la funzionalità.
    -   È più semplice per gli utenti ricominciare da quando l'oggetto non è configurato correttamente.

    ![Screenshot della scheda con il pulsante Ripristina impostazioni predefinite ](images/win-property-win-image13.png)

    In questo esempio le impostazioni Windows firewall sono complesse e possono causare problemi di funzionalità. Se si verifica un problema, spesso è più semplice per gli utenti ricominciare facendo clic su Ripristina impostazioni predefinite.

-   Confermare il comando Ripristina impostazioni predefinite se il relativo effetto non è ovvio o se le impostazioni sono complesse. Indicare la conferma usando i [puntini di sospensione](ctrl-command-buttons.md).
-   **Se appropriato, visualizzare un'anteprima dei risultati di un'impostazione.**

    ![Screenshot degli esempi di puntatore delle proprietà del mouse ](images/win-property-win-image14.png)

    In questo esempio la pagina visualizza un'anteprima degli schemi puntatore. Quando si fa clic su Applica viene visualizzata anche un'anteprima, la visualizzazione di un'anteprima nella pagina è più efficiente per gli utenti.

    ![Screenshot dell'anteprima dei risultati delle impostazioni del tipo di carattere ](images/win-property-win-image15.png)

    In questo esempio la casella Anteprima mostra i risultati delle impostazioni del tipo di carattere. Questo esempio mostra che è possibile visualizzare in anteprima le impostazioni che non sono grafiche.

### <a name="help"></a>Help

-   Quando si fornisce assistenza all'utente, **è consigliabile usare le opzioni seguenti** (elencate nell'ordine di preferenza):
    -   Assegnare etichette descrittive ai controlli interattivi. È più probabile che gli utenti leggono le etichette nei controlli interattivi rispetto a qualsiasi altro testo.
    -   Fornire spiegazioni nel contesto usando etichette di testo statiche.
    -   Fornire un collegamento [specifico a](ctrl-links.md) un argomento della Guida pertinente.
-   **Individuare i collegamenti della Guida nella parte inferiore di ogni pagina.** Se una pagina include diversi gruppi distinti di impostazioni con un argomento della Guida (ad esempio all'interno delle caselle di gruppo), individuare il collegamento Guida nella parte inferiore del gruppo.
-   **Non usare collegamenti a argomenti della Guida generici o generici o pulsanti generici della Guida.** Gli utenti spesso ignorano la Guida generica.

Per altre informazioni ed esempi, vedere [la Guida.](winenv-help.md)

### <a name="standard-users-and-protected-administrators"></a>Utenti standard e amministratori protetti

**Molte impostazioni richiedono privilegi di amministratore per la modifica.** Se un processo richiede privilegi di amministratore, Windows [](glossary.md) e versioni successive richiedono agli utenti [Standard](glossary.md) e agli amministratori protetti di elevare i privilegi in modo esplicito. Questa operazione consente di impedire l'esecuzione di codice dannoso con privilegi di amministratore.

Per altre informazioni ed esempi, vedere [Controllo dell'account utente](winenv-uac.md).

### <a name="default-values"></a>Valori predefiniti

-   **Le impostazioni all'interno di una finestra delle proprietà devono riflettere lo stato corrente dell'applicazione, dell'oggetto o della raccolta di oggetti .** In caso contrario, sarebbe fuorviante e potrebbe causare risultati indesiderati. Ad esempio, se le impostazioni riflettono le raccomandazioni ma non lo stato corrente, gli utenti potrebbero fare clic su Annulla invece di apportare modifiche, ritieni che non siano necessarie modifiche.
-   **Scegliere il più sicuro (per evitare la perdita di dati o l'accesso al sistema) e lo stato iniziale più sicuro.** Si supponga che la maggior parte degli utenti non modificherà le impostazioni.
-   **Se la sicurezza e la sicurezza non sono fattori, scegliere lo stato iniziale più probabile o conveniente.**

## <a name="text"></a>Testo

### <a name="commands"></a>Comandi

-   Per visualizzare le opzioni del programma, usare "Opzioni".
-   Per visualizzare la finestra delle proprietà di un oggetto, usare "Proprietà".
-   Per visualizzare un riepilogo delle impostazioni di personalizzazione del programma di uso comune, usare["Personalizza".](glossary.md)
-   Non usare "Impostazioni" o "Preferenze".
-   Non usare i [puntini di sospensione](ctrl-command-buttons.md) per questi comandi.

### <a name="property-sheet-titles"></a>Titoli della finestra delle proprietà

-   Per un singolo oggetto, usare \[ "Proprietà nome \] oggetto".
    -   Se l'oggetto non ha un nome, usare il nome del tipo dell'oggetto. Ad esempio, Proprietà account utente.
-   Per più oggetti, usare " \[ first object name , \] ... Proprietà."
    -   Se gli oggetti non hanno nomi, usare il nome del tipo degli oggetti. Ad esempio, Proprietà account utente.
    -   Se gli oggetti hanno tipi diversi, usare "Proprietà selezione".
-   Usare [l'uso di maiuscole e minuscole in stile titolo.](glossary.md)
-   Non usare punteggiatura finale.
-   Non usare trattini, ad esempio \[ "nome oggetto \] - Proprietà".

### <a name="property-inspector-titles"></a>Titoli dei controlli proprietà

-   Usare "Proprietà".
-   Usare l'uso di maiuscole e minuscole in stile titolo.
-   Non usare punteggiatura finale.

### <a name="options-dialog-box-titles"></a>Titoli delle finestre di dialogo Opzioni

-   Usare "Opzioni".
-   Usare l'uso di maiuscole e minuscole in stile titolo.
-   Non usare punteggiatura finale.

### <a name="property-page-tab-names"></a>Nomi delle schede della pagina delle proprietà

-   **Usare etichette di tabulazione concise.** Usare una o due parole che descrivono chiaramente il contenuto della pagina. L'uso di nomi di schede più lunghi comporta un uso inefficiente dello spazio sullo schermo, soprattutto quando i nomi delle schede sono localizzati.
-   **Usare etichette di tabulazione specifiche e significative.** Evitare etichette di tabulazione generiche che potrebbero essere applicate a qualsiasi scheda, ad esempio Generale, Avanzate o Impostazioni.
-   Scrivere l'etichetta come frase di una o due parole e non usare la punteggiatura finale.
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Non assegnare una chiave di [accesso univoca.](glossary.md)

### <a name="property-page-text"></a>Testo della pagina delle proprietà

-   Evitare blocchi di testo di grandi dimensioni.
-   Fornire spazio sufficiente per espandere il testo del 30% se verrà localizzato.
-   Non usare testo con frasi come comando nelle finestre delle proprietà. Poiché gli utenti potrebbero voler semplicemente visualizzare le impostazioni, non si vuole chiedere loro di modificare le impostazioni.
-   Usare l'uso di maiuscole e minuscole in stile frase e la punteggiatura finale.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle finestre delle proprietà:

-   Nella programmazione e in altre documentazione tecnica, fare riferimento alle finestre delle proprietà e alle finestre di dialogo delle opzioni come finestre delle proprietà. In qualsiasi altro luogo, usare la finestra di dialogo, in particolare nella documentazione dell'utente.
-   Usare il testo esatto del titolo, inclusa l'uso di maiuscole e minuscole.
-   Per descrivere l'interazione dell'utente, usare apri e chiudi.
-   Quando possibile, formattare il titolo usando il testo in grassetto. In caso contrario, inserire il titolo tra virgolette solo se necessario per evitare confusione.

Quando si fa riferimento alle pagine delle proprietà:

-   Nella programmazione e in altre documentazione tecnica, fare riferimento alle pagine delle proprietà come pagine delle proprietà. In qualsiasi altro luogo, usare tab, in particolare nella documentazione dell'utente.
-   Usare il testo esatto del titolo, inclusa l'uso di maiuscole e minuscole.
-   Per descrivere l'interazione dell'utente, usare fare clic per fare riferimento a una scheda.
-   Quando possibile, formattare il nome usando il testo in grassetto. In caso contrario, inserire il nome tra virgolette solo se necessario per evitare confusione.

 

 