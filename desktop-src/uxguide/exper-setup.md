---
title: Configurazione
description: Gli utenti non possono installare software, quindi le esperienze di installazione moderne devono essere semplici, efficienti e senza problemi.
ms.assetid: ed0265a6-4c39-4a1f-9493-e316a6519df7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 4e5de6f15dd797dd1d1362d1b515122b78c770f4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104555188"
---
# <a name="setup"></a>Configurazione

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Gli utenti non possono installare software, quindi le esperienze di installazione moderne devono essere semplici, efficienti e senza problemi.

Il programma di installazione di solito si riferisce all'esperienza di installazione e configurazione iniziale di un programma. Tuttavia, il programma di installazione può anche fare riferimento a un intero ciclo di vita dell'installazione, tra cui installazione iniziale, aggiornamenti del programma incrementale (ad esempio aggiornamenti della versione o Service Pack), ripristino e disinstallazione.

La maggior parte degli utenti considera la configurazione come un male necessario, per essere eseguita il più rapidamente possibile. Il punto di installazione del programma è quello di usarlo, non di prendere decisioni innumerabili sulla configurazione e sull'utilizzo oppure, peggio ancora, per dedicare molto tempo a rispondere alle domande personali usate a scopo di registrazione o marketing.

![Screenshot che mostra una finestra di dialogo di installazione con quattro opzioni.](images/exper-setup-image1.png)

Un'esperienza di installazione semplificata.

L'esperienza di installazione combinata con il primo utilizzo del programma è nota come prima esperienza. Il programma dovrebbe fornire una prima esperienza semplificata per gli utenti. Ogni domanda o passaggio non necessario o posticipato ritarda l'utilizzo del programma. I programmi di installazione eccessivamente complessi sono reliquie da un periodo di tempo diverso.

**Nota:** Le linee guida relative alla [prima esperienza](exper-first-exper.md) con un programma e [procedure guidate](win-wizards.md) sono presentate in articoli distinti.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente corretta?

Sebbene tutti i programmi di Microsoft Windows necessitino di una sorta di programma di installazione, è possibile scegliere dove inserire le impostazioni del programma:

-   Configurazione
-   Primo utilizzo del programma
-   Opzioni di programma centralizzate
-   Nel contesto di utilizzo della funzionalità

**Configurazione**

Impostazioni presenti nel programma di installazione se:

-   Le impostazioni corrette sono necessarie per usare il programma e si applicano a tutti gli utenti.
-   L'uso delle impostazioni predefinite non è accettabile perché non è disponibile alcun valore predefinito sicuro. è probabile che gli utenti scelgano impostazioni che non sono quelle predefinite oppure che le impostazioni predefinite richiedano il consenso dell'utente.
-   Gli utenti devono, ma probabilmente, modificare le impostazioni importanti dopo l'installazione.

**Primo utilizzo del programma**

Impostazioni presenti nel primo utilizzo del programma se:

-   Le impostazioni corrette sono necessarie per usare il programma e si applicano a singoli utenti.
-   L'uso delle impostazioni predefinite non è accettabile perché non è disponibile alcun valore predefinito sicuro. è probabile che gli utenti scelgano impostazioni che non sono quelle predefinite oppure che le impostazioni predefinite richiedano il consenso dell'utente.
-   Gli utenti devono, ma probabilmente, modificare le impostazioni importanti usando le opzioni del programma.
-   Le impostazioni consentono di personalizzare un'esperienza di base o una chiave cruciale per l'identificazione personale di un utente con il programma.

Per queste impostazioni, è probabile che gli utenti effettuino scelte migliori all'interno del contesto del programma rispetto all'installazione.

**Opzioni di programma centralizzate**

Presenta le impostazioni nella finestra di [dialogo Opzioni](win-property-win.md) del programma se si verificano tutte le condizioni seguenti:

-   Sono disponibili impostazioni predefinite che funzionano correttamente per la maggior parte degli utenti.
-   Sono disponibili molte impostazioni che si applicano a tutte le funzionalità e le attività.
-   È più probabile che gli utenti trovino le impostazioni in una posizione centralizzata.

**Nel contesto di utilizzo della funzionalità**

Presentare le impostazioni nel contesto pertinente se si verificano tutte le condizioni seguenti:

-   Sono disponibili impostazioni predefinite che funzionano correttamente per la maggior parte degli utenti.
-   Per una funzionalità specifica è disponibile un numero ridotto di impostazioni autosufficienti.
-   È più probabile che gli utenti trovino le impostazioni con la funzionalità associata rispetto a una posizione centralizzata.
-   L'interfaccia utente (UI) può accedere alle impostazioni in un punto ovvio.

Con particolare attenzione al posizionamento delle impostazioni di configurazione, è possibile ridurre il carico di lavoro degli utenti durante la prima esperienza con il programma.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="design-a-lightweight-setup"></a>Progettare un'installazione leggera

Benvenuti, avanti, avanti, avanti, avanti, avanti, installazione, fine, congratulazioni! L'esperienza di installazione ha un suono familiare? Storicamente, i programmi di installazione hanno adottato questo tipo di progettazione inefficiente, ovvero una sequenza di schermate che consente agli utenti di accedere a una sequenza di clic insensata.

Se gli utenti descrivono la configurazione del programma con parole come rapide e semplici, sono sicuramente lodate dall'esperienza. Si preferisce usare il programma piuttosto che configurarlo.

**Esaminare la progettazione della configurazione per le domande, le opzioni, le pagine e i percorsi non essenziali, evitando di eliminarli.** Eseguire ricerche utente per individuare le opzioni effettivamente necessarie per gli utenti e assicurarsi che non stiano facendo clic sul pulsante avanti in tutte le pagine. Rinviare le opzioni o le domande più indicate nel contesto del programma in esecuzione.

Molti programmi di installazione offrono pagine standard non perché sono necessari o utili, ma perché sono standard. Ad esempio, le pagine di benvenuto, le pagine di riepilogo e le pagine di congratulazioni spesso aggiungono solo clic. Al contrario, il programma di installazione deve aggiungere pagine solo se sono necessarie per completare l'attività di installazione. Per le linee guida sui tipi di pagine di installazione e su come valutarle, vedere [tipi di pagina](#page-types) più avanti in questo articolo.

![screenshot della prima pagina di installazione di ProClarity ](images/exper-setup-image2.png)

In questo esempio, il programma di installazione Elimina la pagina di benvenuto tradizionale e si avvicina al business.

Anche se potrebbe essere necessario offrire diversi rami di configurazione (un'esperienza rapida, tipica e un'esperienza personalizzata più controllabile), assicurarsi di disporre di un numero sufficiente di opzioni personalizzate per garantire la complessità aggiuntiva. Non aggiungere Branch a meno che non sia necessario. Alcune opzioni non importanti in un ramo personalizzato suggeriscono la necessità di riorganizzare la progettazione del programma di installazione.

Un altro motivo per semplificare la configurazione è che gli utenti inesperti talvolta sovraanalizzano le opzioni, temendo che una scelta errata possa essere irreversibile o distruttiva. Forzare gli utenti a prendere decisioni in merito alle cose che non sono in grado di comprendere o a cui si è interessati potrebbe essere ansioso, incompetente e persino frustrato. Non è una buona idea. È preferibile fare in modo che vengano avviati rapidamente, in modo confortevole e sicuro mentre esplorano le funzionalità del programma e prendere decisioni migliori sulle opzioni di funzionalità in quel momento. Per altre linee guida, vedere [semplificare la configurazione](#streamlining-setup) più avanti in questo articolo.

Sforzarsi di rendere l'esperienza di installazione più [semplice possibile, ma non più semplice](/previous-versions//dn742474(v=vs.85)). I programmi destinati ad utenti altamente tecnici possono richiedere una configurazione complessa. Ad esempio, il team di Microsoft SQL Server ha scoperto che gli amministratori di database preferiscono mantenere il controllo su molte opzioni di installazione, ad esempio i percorsi dei file. Inoltre, SQL Server è un'applicazione aziendale di grandi dimensioni, con un numero di componenti che variano notevolmente a scopo e funzionalità. Quindi, anche se si vuole semplificare le operazioni, il programma di installazione deve riflettere la complessità del prodotto e le aspettative e le esigenze degli utenti.

Tuttavia, tali programmi di installazione complessi dovrebbero essere l'eccezione, non la regola. La maggior parte dei programmi Windows dovrebbe impegnarsi per avviare il processo di installazione con un semplice passaggio.

### <a name="setup-phases"></a>Fasi di installazione

I programmi di installazione ben progettati consentono agli utenti di eseguire altre attività durante l'attività che richiede molto tempo per il download e la copia dei file. Per l'esecuzione automatica, i programmi di installazione sono progettati per avere quattro fasi separate:

-   **Fase decisionale.** Gli utenti indicano come desiderano che il programma sia installato e configurato.
-   **Fase di download.** Per i programmi scaricati da Internet. Se il programma dispone di più applicazioni o versioni, gli utenti indicano gli elementi da scaricare durante la fase decisionale.
-   **Fase di installazione.** Il programma di installazione copia i file e apporta le modifiche di configurazione appropriate.
-   **Fase di completamento.** Vengono risolti tutti i dettagli, i passaggi o i problemi rimanenti.

Poiché la fase di installazione potrebbe richiedere molto tempo, questa fase deve essere progettata per essere eseguita fino al completamento senza alcun intervento da parte dell'utente. Ciò significa che tutte le domande devono essere poste durante la fase decisionale e tutti i problemi che si verificano dovrebbero essere accodati e gestiti nella fase di completamento. **Se il completamento della fase di installazione richiede più di un minuto, si supponga che gli utenti effettuino altre operazioni durante le fasi di download e installazione.**

**Non corretto:**

![Screenshot di $ install auto-Reporting?' dialogo ](images/exper-setup-image3.png)

In questo esempio, il programma di installazione interrompe lo stato di avanzamento per porre una domanda che dovrebbe essere stata richiesta durante la fase di decisione.

### <a name="present-helpful-progress"></a>Stato utile presente

Se gli utenti attendono pazientemente la fase di installazione dell'esperienza di installazione, probabilmente osservando un indicatore di stato fino al suo completamento apparente, solo per verificare la reimpostazione dell'indicatore di stato e ricominciare, c'è un vero senso di comtraye. Lo stato di avanzamento segnalato è fuorviante e, infine, non ha alcun significato.

Una variante di questo scenario doloroso è l'installazione di "brinksmanship": gli utenti vedono il raggiungimento dello stato di avanzamento, ad indicare il completamento del 99%, ma sono costretti ad attendere un periodo di tempo sproporzionato prima di ottenere il completamento del 100%. Quindi, in termini di ciò che è più importante per l'utente, una promessa implicita sull'intervallo di tempo di attesa, l'attestazione del 99% di completamento è ingannevole.

Durante le fasi di download e installazione, gli utenti in genere hanno due aspetti da sapere: devono attendere o eseguire un'altra operazione e il programma di installazione verrà eseguito a breve. Sebbene esistano variabili sufficienti nel processo di installazione per evitare di fornire informazioni accurate sullo stato di avanzamento, il feedback sullo stato di avanzamento deve essere sufficientemente accurato per rispondere a queste due domande e impostare le aspettative appropriate. Oltre a un indicatore di stato, è possibile includere una breve istruzione sul tempo complessivo previsto per il processo.

![screenshot della finestra di dialogo che mostra lo stato dell'installazione ](images/exper-setup-image4.png)

In questo esempio, nella pagina stato è inclusa una breve dichiarazione generale sul tempo che l'installazione potrebbe richiedere.

I programmi di installazione validi utilizzano le barre di stato in modo efficiente per fornire agli utenti informazioni utili sullo stato del programma di installazione. Per altre linee guida, vedere [indicatori di stato](progress-bars.md).

### <a name="design-for-all-setup-scenarios"></a>Progettazione per tutti gli scenari di installazione

I programmi di installazione moderni devono essere progettati per gestire diversi scenari di installazione:

-   L'utente del programma lo installa da un disco o da una condivisione file di rete.
-   L'utente del programma lo Scarica dal Web.
-   Un produttore di apparecchiature originale (OEM) include il programma nel computer in cui si trova la factory.
-   Un professionista IT installa il programma su molti computer in un'organizzazione.
-   Un utente diverso dall'utente installa il programma (ad esempio, un elemento padre per conto di un figlio o un collaboratore che usa lo stesso computer di un altro collaboratore).

Considerati questi scenari, non è necessario presupporre che gli utenti stiano installando sempre il programma per se stessi (rendendo le opzioni non appropriate per le preferenze personali), monitorando il processo in modo accurato (rendendo l'installazione automatica importante) o anche un'interfaccia utente grafica per l'attività.

### <a name="dont-forget-the-uninstall-experience"></a>Non dimenticare l'esperienza di disinstallazione

Per completare il ciclo di vita della configurazione del software, gli utenti devono essere in grado di rimuovere il software che non vogliono o non sono più necessari. Questo è particolarmente importante se il programma non è stato installato autonomamente, ad esempio se è stato precaricato nel computer.

### <a name="handle-technical-support-strategically"></a>Gestire il supporto tecnico in modo strategico

L'installazione del programma è l'unica attività che tutti gli utenti devono completare correttamente. Se gli utenti non riescono a installare il programma, è necessario fornire supporto tecnico costoso o non più utenti.

Progettare il programma di installazione per fornire al team di supporto tecnico le funzionalità e le informazioni necessarie per consentire agli utenti di installare correttamente. Questi dettagli non devono essere in genere esposti agli utenti, ma dovrebbero essere prontamente accessibili quando necessario.

**Non corretto:**

![screenshot dell'etichetta che mostra il nome del server com ](images/exper-setup-image5.png)

In questo esempio, l'indicatore di stato Mostra i dettagli significativi solo per il supporto tecnico.

Mantenere la normale esperienza utente semplice: non ingombrarla con informazioni con un valore solo per il supporto tecnico. Registrare invece le informazioni di supporto in un file di log dell'installazione. E, ancora più importante, aiutare gli utenti a evitare la necessità di supporto tecnico con messaggi di errore chiari e concisi che illustrano correttamente i problemi e forniscono soluzioni pratiche. Quando necessario, fornire i collegamenti agli articoli della guida. Provare a fornire un'opzione di ripristino al programma di installazione per ripristinare i file o le impostazioni mancanti o danneggiati.

**Se si eseguono solo tre operazioni...**

1.  1. Configurare il più semplice e leggero possibile. Tenere presente che gli utenti non godono della configurazione. Esaminare attentamente ogni domanda, opzione, pagina e percorso ed eliminare tutto ciò che non è essenziale per completare la configurazione.
2.  2. Progettazione per tutti gli scenari di installazione, incluse le installazioni automatiche, le installazioni con script e la disinstallazione. Per le installazioni automatiche efficienti, assicurarsi che esista una netta separazione tra le fasi di installazione.
3.  3. Progettare il programma di installazione in modo che gli utenti possano risolvere i problemi di installazione autonomamente, ma anche registrare le informazioni necessarie per il supporto tecnico solo nel caso. Tenere presente che il programma di installazione è l'unica attività che tutti gli utenti devono completare correttamente.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Applicare le linee guida della procedura guidata standard per i programmi di installazione basati su procedure guidate.** Usare queste linee guida per determinare una struttura di pagina ottimale, una navigazione efficace, etichette di controllo valide, l'uso di istruzioni principali e l'uso della guida.
-   **Consentire agli utenti di riavviare il programma di installazione in cui si è interrotto se richiede un numero elevato di input dell'utente o richiede molto tempo per il completamento.** Se gli utenti riavviano il programma dopo averlo chiuso prima del completamento, ripristinare l'input dell'utente precedente e riavviare il percorso in cui è stata arrestata.
-   **Non visualizzare le finestre di installazione ingrandite.** La visualizzazione di una finestra di installazione ingrandita presuppone che gli utenti forniscano un'attenzione indivisa, che è improbabile. Scegliere invece una dimensione appropriata per il contenuto in modo da mantenere un aspetto semplice.

### <a name="windows-integration"></a>Integrazione di Windows

-   **Denominare il file di installazione "Setup.exe".** "Install.exe" è un'alternativa accettabile. Questo consente a Windows (e agli utenti) di riconoscere il file come programma di installazione.
    -   **Eccezione:** Per i programmi scaricati da Internet, consentire agli utenti di gestire e organizzare la cartella Downloads includendo il nome del programma nel nome del file di installazione. Ad esempio, SetupVisualStudioExpress2008.exe.
-   **Copiare i file di programma nei percorsi di file system corretti.** Questa operazione consente a utenti e Windows di trovare e organizzare i file in modo più efficace. Per ulteriori informazioni, vedere le [linee guida sull'utilizzo dello spazio dei nomi del file System Windows](../fileio/naming-a-file.md#namespaces).

### <a name="user-account-control"></a>Controllo dell'account utente

-   **Firmare digitalmente il file eseguibile di installazione.** Gli eseguibili firmati presentano molti vantaggi, tra cui l'uso di un'interfaccia utente di elevazione del controllo dell'account utente. Per informazioni sulla firma dei file, vedere [Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).
-   **Se un'installazione potrebbe richiedere un'elevazione, elevare il più tardi possibile.** Visualizzare l'interfaccia utente di elevazione solo dopo che l'utente ha eseguito il commit in un'opzione che richiede l'elevazione. In genere, l'interfaccia utente di elevazione viene visualizzata durante la fase di installazione, non la fase decisionale. Tuttavia, se un'installazione richiede sempre l'elevazione dei privilegi, elevare al punto di ingresso.
-   **Richiedi sempre l'elevazione per la disinstallazione.** In questo modo si impedisce al malware di disinstallare software critico senza che gli utenti ne siano a conoscenza.
-   **Una volta elevato, rimane elevato fino a quando non sono più necessari privilegi elevati.** Per eseguire un'installazione completa di un programma, gli utenti non dovrebbero dover elevare più volte.
-   **Se per l'installazione sono necessari privilegi speciali, verificare le credenziali dell'utente e segnalare eventuali problemi nella prima o nella seconda pagina.** Non consentire agli utenti di eseguire molto lavoro solo per scoprire che non dispongono delle credenziali corrette per completare l'installazione.
-   **Richiedere i privilegi minimi possibili.** Ad esempio, gli amministratori sono riluttanti a installare software che richiede credenziali di amministratore di dominio.

Per altre linee guida, vedere [controllo dell'account utente](winenv-uac.md).

### <a name="restarting-windows"></a>Riavvio di Windows

-   **Evitare il riavvio di Windows.** La maggior parte dei programmi dovrebbe essere installata senza riavviare Windows. Il motivo principale per cui gli aggiornamenti o le installazioni del programma richiedono un riavvio del sistema è che alcuni file interessati sono attualmente utilizzati da un programma in esecuzione. In questo caso, un'alternativa migliore consiste nel rendere gli utenti consapevoli della situazione, consentire agli utenti di chiudere questi programmi, quindi ripetere l'operazione. Per ulteriori informazioni su come evitare i riavvii, vedere [Gestione riavvio](../rstmgr/restart-manager-portal.md).
-   **Se il programma di installazione deve riavviare Windows:**
    -   **Usare un solo riavvio.** Ritardare il riavvio richiesto da tutti i prerequisiti finché il programma e i relativi aggiornamenti non sono completamente installati.
    -   **Consentire agli utenti di determinare quando si verifica.** Non riavviare automaticamente Windows, perché gli utenti potrebbero perdere il lavoro. Assicurarsi che sia chiaro agli utenti che hanno una scelta.

        **Non corretto:**

        ![screenshot della finestra di dialogo con riavvio e annullamento ](images/exper-setup-image6.png)

        In questo esempio gli utenti non hanno la possibilità di scegliere quando riavviare Windows.

    -   **Se l'utente sceglie di non riavviare immediatamente Windows, presentare il feedback finale come esito positivo, non un errore.** Sebbene tecnicamente l'installazione non venga completata fino al riavvio, l'operazione ha avuto esito positivo dal punto di vista dell'utente.

### <a name="streamlining-setup"></a>Ottimizzazione della configurazione

-   **Quando si pratica, avviare il processo di installazione con un solo passaggio.** Ad esempio, anziché aggiungere una pagina separata nel programma di installazione per le condizioni di licenza, è possibile fornire un collegamento a tali pagine. Se ci si collega ai termini:
    -   Per richiedere il consenso esplicito per accettare le condizioni di licenza, utilizzare il pulsante commit come "Accetto e installa".
    -   Verificare che il collegamento al contratto di licenza non possa essere suddiviso collegando un file locale al programma di installazione anziché una pagina Web.
    -   Consente di stampare il contratto di licenza dalla relativa finestra di visualizzazione.
-   **Elimina le opzioni e le domande superflue.**
    -   Posticipare le opzioni più appropriate per il primo utilizzo del programma o della funzionalità.

        ![screenshot della finestra di dialogo con l'opzione impostazioni personalizzate ](images/exper-setup-image7.png)

        In questo esempio, Windows Media Player presenta le opzioni di privacy per singolo utente al primo utilizzo del programma.

    -   Non porre domande agli utenti sullo stato del sistema. Rilevare automaticamente queste informazioni e richiedere agli utenti di verificare solo se esiste un motivo per la modifica.
    -   Non porre domande su dettagli irrilevanti. Per i programmi Windows tipici, ad esempio, è preferibile presupporre che sia necessario copiare i file di programma nella cartella programmi.

        **Non corretto:**

        ![screenshot della finestra di dialogo con percorso di installazione ](images/exper-setup-image8.png)

        In questo esempio, il programma di installazione deve essere semplificato eliminando la richiesta di input del percorso del file. Date le dimensioni del programma, la maggior parte degli utenti non è rilevante e semplicemente fare clic su Avanti.

    -   Non chiedere le autorizzazioni necessarie per eseguire le operazioni necessarie. La maggior parte dei programmi, ad esempio, non deve includere un'opzione per inserire l'icona del programma sul desktop.
    -   Non confermare l'annullamento dell'installazione. Se gli utenti fanno clic su Annulla durante l'installazione, si supponga che l'annullamento sia intenzionale e che il programma venga chiuso senza conferma. In tal caso, si rischia di perdere tempo o impegno significativo, consentire agli utenti di riavviare il programma di installazione e di scegliere il punto in cui si è interrotto.

-   **Ottimizza per l'installazione automatica.**
    -   Presentare tutte le opzioni e le domande durante la fase decisionale.
    -   Per le fasi di download e installazione, ritardo che richiede l'input dell'utente per qualsiasi problema riscontrato fino alla fine della fase. In questo modo, gli utenti possono lasciare l'installazione automatica fino a quando non ritornano per comodità.
-   **Elimina le pagine non necessarie.** Se la maggior parte degli utenti fa sempre clic su avanti in una pagina, provare a eliminare la pagina. Per linee guida sull'eliminazione di determinati tipi di pagine, vedere [tipi di pagina](#page-types).
-   **Eliminare il testo non necessario.**
    -   Rimuovere il testo ridondante da istruzioni ed etichette.
    -   Non spiegare i concetti di base sull'utilizzo di Windows, ad esempio:
        -   Come interagire con i controlli (esempi: per iniziare, fare clic su Avanti; Per altre opzioni, fare clic su opzioni. Per ulteriori informazioni, fare clic su?.
        -   Funzionamento delle procedure guidate (esempio: se si desidera rivedere o modificare le impostazioni, fare clic su indietro).
        -   Funzionamento del programma di installazione (esempio: il programma copia i file di programma nel disco rigido...).
-   **Eliminare il lavoro superfluo.**
    -   Specificare valori predefiniti validi:
        -   In genere, selezionare la risposta più sicura e privata come predefinita.
        -   Se la sicurezza e la privacy non sono fattori, selezionare la risposta più probabile o pratica.

            ![screenshot della finestra di dialogo con il nome e la società visualizzati ](images/exper-setup-image9.png)

            In questo esempio, il nome utente e l'organizzazione forniti per impostazione predefinita vengono ottenuti dal registro di sistema.

        -   Se un'opzione è fortemente consigliata, è consigliabile selezionarla per impostazione predefinita o aggiungere "(scelta consigliata)" all'etichetta.

    -   Avanza automaticamente le pagine quando una pagina non ha input e l'attività viene eseguita correttamente, ad esempio con pagine di download, installazione, avanzamento e aggiornamenti. Al termine del passaggio, rimanere in queste pagine solo per mostrare i problemi.
    -   Quando si è pratici, avviare il programma automaticamente al termine dell'installazione, anziché visualizzare una pagina di congratulazioni o di completamento. Quando l'installazione viene eseguita in modo interattivo, si supponga che l'utente stia installando il programma per eseguirlo immediatamente, quindi l'esecuzione del programma è il miglior feedback per mostrare che l'installazione è stata completata. L'esecuzione automatica del programma non è pratica quando il programma di installazione installa più di un programma, ad esempio un gruppo costituito da molti programmi, quando l'installazione non viene eseguita in modo interattivo o quando il processo di installazione non viene completato dopo l'installazione.

### <a name="page-types"></a>Tipi di pagina

**Pagine di benvenuto e Introduzione**

-   **Elimina le pagine di benvenuto.** Sebbene sia un'ottima idea, gli utenti in genere fanno semplicemente clic su Avanti senza leggere. E dal momento che gli utenti ignorano in genere le pagine senza leggere, il testo è poco più che dichiarare il chiaro, da progettazione.

    **Non corretto:**

    ![screenshot della schermata iniziale con Next e Cancel ](images/exper-setup-image10.png)

    In questo esempio non è necessario eseguire alcuna operazione per l'utente, ma fare clic su Avanti.

-   **Utilizzare una pagina di Introduzione solo se è necessario informare gli utenti sui prerequisiti per l'installazione di.** Tali prerequisiti includono l'installazione di software o hardware necessari, l'esecuzione di modifiche e aggiornamenti della configurazione di sistema necessari, l'esecuzione di un backup del sistema per la protezione dalla perdita di dati o l'ottenimento di informazioni necessarie che l'utente probabilmente non avrà già.
-   **Ogni volta che è possibile, fornire la possibilità di eseguire i prerequisiti direttamente dal programma di installazione.** Gli utenti devono eseguire manualmente la procedura solo se non esiste un'alternativa.
-   Se non viene usata una pagina iniziale o una pagina Introduzione, **includere il nome e la descrizione del programma in qualsiasi altra pagina del programma di installazione.** È possibile utilizzare il linguaggio di benvenuto come testo introduttivo purché lo scopo della pagina sia chiaro.

**Pagine relative alle condizioni di licenza**

-   **Scrivere le condizioni di licenza utilizzando testo chiaro e conciso.** Usare la lingua normale. Evitare "legalese".
-   **Presentare usando un formato facile da leggere e analizzare.** Non usare i passaggi lunghi del testo in maiuscolo.

    **Non corretto:**

    ![screenshot delle condizioni di licenza in maiuscolo ](images/exper-setup-image11.png)

    In questo esempio, il testo maiuscolo e le dimensioni del carattere grande rendono difficili la lettura dei termini, forzando gli utenti a scorrere più del necessario.

-   **Richiedere il consenso esplicito per accettare le condizioni di licenza.** L'accettazione della licenza non deve mai essere selezionata per impostazione predefinita. Se vengono usati pulsanti di opzione per indicare l'accettazione, lasciare le opzioni deselezionate per impostazione predefinita e richiedere agli utenti di accettare i termini prima di abilitare il pulsante Avanti.

    ![screenshot della finestra di dialogo con pulsante avanti in grigio ](images/exper-setup-image12.png)

    In questo esempio il pulsante Avanti è disabilitato fino a quando gli utenti non accettano esplicitamente le condizioni di licenza.

-   **Non richiedere agli utenti di scorrere fino alla fine del testo delle condizioni di licenza prima che sia abilitato il pulsante Avanti.** Questa operazione impone agli utenti un carico inutile per comprendere il motivo per cui il pulsante Avanti è disabilitato.
-   **Fornire un comando stampa,** con un pulsante di comando o un menu di scelta rapida. Presentare i termini in un formato ottimizzato per la stampa.

**Pagine di registrazione del prodotto**

-   **Richiedere agli utenti di registrarsi solo se devono usare il programma.** Spiega chiaramente i motivi per cui gli utenti devono registrarsi.
-   **Fornire la registrazione facoltativa solo se è presente un vantaggio utente chiaro,** ad esempio per notificare agli utenti gli aggiornamenti del prodotto. Lasciare deselezionata questa opzione per impostazione predefinita.
-   **Consente agli utenti di effettuare la registrazione in un secondo momento.** Fornire un massimo di tre promemoria e consentire agli utenti di ignorare i promemoria con un solo clic.

**Pagine ambito (tipico, personalizzato o minimo)**

-   **Si preferisce eliminare questa pagina.** Si supponga che la maggior parte degli utenti desideri l'esperienza di installazione tipica (e progettare tale esperienza in modo che funzioni correttamente per la maggior parte degli utenti).
-   Se è necessario includere una pagina ambito:
    -   **Illustrare le differenze tra le opzioni in termini di funzionalità e spazio su disco.** Gli utenti si basano sulla chiarezza delle informazioni nella pagina ambito per assicurarsi che la scelta sia corretta.
    -   **Assicurarsi che le opzioni personalizzate siano necessarie solo per una piccola percentuale di utenti, mentre la maggior parte degli utenti può ignorarle in modo sicuro.** In caso contrario, le opzioni devono trovarsi nel percorso di installazione tipico.
    -   **Se gli utenti scelgono opzioni personalizzate, selezionare per impostazione predefinita le opzioni di installazione tipiche.** Gli utenti considerano l'installazione tipica come la linea di base e vogliono personalizzare aggiungendo o rimuovendo le opzioni da tale Baseline.
-   Se è necessario usare un'opzione di installazione personalizzata, è **consigliabile usare il ridimensionamento e il posizionamento dei pulsanti relativi per guidare la maggior parte degli utenti nell'installazione tipica.**

    ![screenshot della finestra di dialogo con pulsante di installazione grande ](images/exper-setup-image13.png)

    In questo esempio, la progettazione della pagina rinforza visivamente il fatto che la maggior parte degli utenti deve optare per l'installazione tipica.

**Pagine di input**

-   **Per impostazione predefinita, ridurre il numero di opzioni di installazione.** Per informazioni su come eliminare le opzioni, vedere [semplificare l'installazione](#streamlining-setup).
-   **Fornire valori predefiniti accettabili quando possibile.** Scegliere le impostazioni predefinite sicure e private e sono accettabili per la maggior parte degli utenti senza alcuna modifica.
-   **A meno che il programma non abbia requisiti insoliti, cercare di avere una singola pagina di domande e opzioni.** Tuttavia, se il programma richiede diverse pagine di domande e opzioni, visualizzarle nel flusso della pagina principale della procedura guidata. Non provare a ridurre il numero di pagine tecnicamente inserendo opzioni nelle finestre di dialogo o usando le schede.
-   ![screenshot della finestra di dialogo del programma di installazione con quattro opzioni ](images/exper-setup-image14.png)
-   In questo esempio, le opzioni sono limitate a una singola pagina.
-   **Convalidare l'input il prima possibile:**
    -   Impedisci la immissione di caratteri non validi.
    -   Usare i [palloni](ctrl-balloons.md) per segnalare problemi con caselle di testo non valide.
    -   Convalidare i campi correlati in una pagina quando gli utenti fanno clic su Avanti.
    -   Convalidare i campi correlati tra le pagine di input non appena possono essere rilevati problemi.
-   **Assegnare a tutti i percorsi di file modificabili un pulsante Sfoglia.** Consente agli utenti di specificare i percorsi di rete.
-   **Per la pagina di input finale, etichettare l'installazione del pulsante di commit, non successivo.** Quando viene avviata l'installazione, gli utenti non devono essere sorpresi da. Prima del punto di commit, verificare che gli utenti possano modificare facilmente le impostazioni.

**Avvia pagine di installazione**

-   **Eliminare questa pagina se non ha scopi diversi da riepilogare le scelte precedenti e iniziare l'installazione.** Se le pagine di input sono chiare e pochi numeri, non è necessario riepilogarle. Al contrario, la pagina di input finale deve avere il pulsante Installa, che conduce direttamente alla pagina di stato.
-   **Per installazioni complesse destinate a professionisti IT, fornire una pagina di installazione con un elenco completo delle modifiche che verranno eseguite dal programma di installazione.** Molti professionisti IT hanno un controllo rigoroso per la gestione delle modifiche, quindi è necessario che gli effetti dell'installazione del programma siano dettagliati.

**Pagine di stato**

-   **Fornire sempre una pagina di stato,** anche se il programma viene installato rapidamente. Specificare una pagina di stato separata per [la fase di download](#setup-phases) , se disponibile. Disabilitare i pulsanti indietro (o precedente) e avanti mentre è in corso l'installazione, ma lasciare il pulsante Annulla abilitato e reattivo.

    ![screenshot della finestra di dialogo con indicatore di stato ](images/exper-setup-image15.png)

    Una tipica pagina di stato.

-   **Utilizzare un singolo indicatore di stato determinato.** Seguire le [linee guida relative all'indicatore di stato](progress-bars.md), tra cui:
    -   Indica chiaramente il completamento. Non lasciare che un indicatore di stato vada al 100%, a meno che l'operazione non sia stata completata.
    -   Non riavviare lo stato di avanzamento. Un indicatore di stato perde il suo valore se viene riavviato (forse perché un passaggio nell'operazione viene completato) perché gli utenti non hanno modo di sapere quando l'operazione verrà completata. Al contrario, tutti i passaggi dell'operazione condividono una parte dello stato di avanzamento e l'indicatore di stato passa al completamento una volta.
-   **Fornire una descrizione concisa del passaggio corrente sopra l'indicatore di stato.** Per le installazioni rapide, il testo non è necessario; l'indicatore di stato da solo è sufficiente. Per le installazioni che richiedono un minuto o più, il testo può essere utile per gli utenti che partecipano alla configurazione.
    -   **Usare i frammenti di frase, in genere a partire da un verbo e terminando con i puntini di sospensione.** Esempi: copia dei file in corso..., installazione dei componenti richiesti in corso...
    -   **Posizionare il testo sopra la barra, non sotto.**

        **Non corretto:**

        ![screenshot del testo visualizzato nell'indicatore di stato ](images/exper-setup-image16.png)

        In questo esempio il testo esplicativo verrà visualizzato sopra l'indicatore di stato.

    -   **Evitare di ingombrare la pagina di stato con dettagli superflui.** Questa pagina non è per il [supporto tecnico](#handle-technical-support-strategically), quindi non è necessario visualizzare i GUID di registrazione o i file specifici copiati.

        **Non corretto:**

        ![screenshot del GUID visualizzato sull'indicatore di stato ](images/exper-setup-image17.png)

        In questo esempio, i dettagli tecnici, ad esempio i GUID, non sono significativi per gli utenti.

**Pagine di errore**

-   **Se l'installazione ha esito negativo e si verifica un problema significativo, visualizzare una pagina di errore in cui vengono illustrati i problemi e i passaggi pratici per risolverli.** Visualizza la pagina con un'icona di errore. Non usare una finestra di dialogo a questo scopo.

    ![screenshot della pagina di errore e dell'icona ](images/exper-setup-image18.png)

    In questo esempio, l'errore di installazione viene illustrato in una pagina di errore, insieme ad alcuni passaggi per risolvere il problema.

-   **Se il programma di installazione viene completato con un problema irreversibile secondario, presentare il problema come attività aggiuntiva anziché come errore.** Usa un linguaggio positivo, orientato al successo, incoraggiante, non termini come errori, errori o problemi. Non usare un'icona di errore.

**Pagine Congratulazioni/completamento**

-   **Quando si installa un singolo programma in modo interattivo, avviare il programma (e chiudere l'installazione guidata) per indicare che l'installazione è stata completata, anziché visualizzare una pagina di completamento. Eccezioni**
    -   Le configurazioni eseguite dalla riga di comando non devono avviare i programmi.
    -   Gli aggiornamenti automatici (ad esempio, Windows Update) non devono avviare i programmi.
    -   L'installazione di criteri di gruppo non deve avviare i programmi.
    -   Eventuali scenari di installazione di professionisti IT, perché non vengono installati per uso personale.
-   **Se il programma di installazione include passaggi di completamento dopo l'installazione, elencarli in una pagina di completamento.** Tuttavia, per giustificare una pagina di completamento, assicurarsi che gli utenti siano in grado di eseguire la procedura e che i passaggi debbano essere effettivamente dichiarati, ovvero non sono evidenti.

    **Non corretto:**

    ![screenshot della pagina che mostra la configurazione completata ](images/exper-setup-image19.png)

    In questo esempio, una pagina di completamento non necessaria indica l'ovvio. Windows Update viene eseguito automaticamente, quindi non esiste alcun motivo per consentire agli utenti di eseguirlo manualmente.

-   **Quando si installa una suite di programmi, visualizzare una pagina di completamento per indicare l'esito positivo e tutti i passaggi successivi che potrebbero essere necessari.**

    ![screenshot della pagina finale dell'installazione di Office Suite ](images/exper-setup-image20.png)

    In questo esempio, il programma di installazione ha installato più programmi, quindi non ha senso avviare automaticamente un determinato programma. Una pagina di completamento è più appropriata.

### <a name="leaving-users-in-control"></a>Gestione degli utenti

-   **Non raccogliere informazioni personali, ad esempio quelle usate per scopi di marketing.** Il programma di installazione non è un'opportunità per effettuare il push di una propria agenda, cross-selling di altre offerte di programmi o condurre ricerche di mercato; è possibile danneggiare la relazione di trust con gli utenti in questo modo.
-   **Non forzare gli utenti a rifiutare esplicitamente l'installazione di funzionalità facoltative.** Consentire loro di [acconsentire esplicitamente](glossary.md) . Ad esempio, gli utenti devono scegliere esplicitamente di installare un gadget desktop di Windows.
-   **Consente agli utenti di aggiungere o rimuovere funzionalità opzionali utilizzando il programma di installazione dopo l'installazione iniziale.** Gli utenti possono eseguire questa attività usando l'elemento **Disinstalla o modifica un programma** del pannello di controllo.
-   **Per le iniziative di analisi utilizzo software, descrivere i dati trasmessi, il modo in cui vengono usati e il tempo di mantenimento.** Utilizzare un collegamento a un argomento della Guida informativa sulla privacy a questo scopo.
-   **Evitare l'uso di suoni,** perché molti scenari di installazione sono automatici e perché il suono può essere inutilmente distracting anche durante le installazioni.

### <a name="security"></a>Sicurezza

-   **Per la configurazione basata su Internet, fornire automaticamente gli aggiornamenti della sicurezza durante l'installazione iniziale.** Gli utenti non devono eseguire l'aggiornamento come passaggio separato.
-   **Evitare di consigliare che gli utenti disattivino i firewall come prerequisito per l'installazione del programma.**
-   Se è necessario disattivare un firewall, procedere come segue:
    -   **Limitare la durata di questa condizione a più breve tempo possibile.**
    -   **Indica in modo esplicito quando gli utenti possono riattivare il firewall.**

### <a name="uninstall"></a>Disinstallare

-   **Uninstall deve rimuovere tutte le tracce di un programma, incluse le seguenti:**
    -   File di programma, incluso il programma di installazione.
    -   Voci del menu Start.
    -   Icone del desktop e icone di avvio veloce (se presenti).
    -   Impostazioni del registro di sistema.
    -   Associazioni di file.
-   **La disinstallazione dovrebbe rimanere dietro quanto segue:**
    -   File creati dall'utente, ad esempio file di documento.
    -   Librerie a collegamento dinamico condivise archiviate nella cartella di sistema.

### <a name="help-and-support"></a>Guida e supporto

-   **Progettare il programma di installazione in modo che non richieda assistenza ponendo domande chiare e esplicative.** Riservare assistenza per domande avanzate che possono realmente trarre vantaggio da ulteriori spiegazioni.
-   **Non usare i file Leggimi.** Questi file sono ora obsoleti e gli utenti non li leggono comunque. Fornire invece il contenuto online, se necessario.
-   **Collegamento agli argomenti della Guida appropriati o alla risoluzione dei problemi relativi ai messaggi di errore di installazione.** Verificare che il contenuto della guida fornisca un percorso chiaro per la risoluzione del problema. Per ulteriori informazioni, vedere [messaggi di errore](mess-error.md).
-   **Creare file di log per acquisire informazioni utili per il supporto tecnico.** Non ingombrare l'interfaccia utente di configurazione con i dettagli relativi al supporto tecnico, che non sono significativi per la maggior parte degli utenti. Usare invece i file di log per questo scopo.

### <a name="text"></a>Testo

-   **Essere concisi.** Le procedure guidate di installazione spesso sovrascrivono le funzionalità e le opzioni, usando blocchi di testo difficili da analizzare rapidamente. **Eccezioni**
    -   Digitano tutti gli acronimi. Il programma di installazione è spesso la prima esperienza degli utenti con il programma, quindi non presupporre che comprendano un gergo come gli acronimi.
    -   Spiegare la terminologia e i concetti non noti, preferibilmente disponibili, ma usando gli argomenti della guida, se necessario.
-   **Preferisci un tono descrittivo e professionale; evitare un tono troppo tecnico.**

**Non corretto:**

Limitare l'installazione in base ai singoli utenti.

**Corretto:**

Installa solo per me.

-   Non usare ora nelle etichette dei pulsanti di comando perché l'immediatezza del comando può essere eseguita per la concessione.
    -   **Eccezione:** Quando necessario, utilizzare ora per distinguere i comandi che avviano un'attività da comandi che eseguono immediatamente un'attività.

![screenshot del pulsante di download ](images/exper-setup-image21.png)

In questo esempio, facendo clic sul pulsante di comando si passa a una finestra o a una pagina che consente agli utenti di eseguire il download.

![screenshot del pulsante Scarica ora ](images/exper-setup-image22.png)

In questo esempio, facendo clic sul pulsante di comando, il download viene eseguito immediatamente.

A questo punto è necessario etichettare un solo comando in un flusso attività. Un comando **Scarica ora** , ad esempio, non deve mai essere seguito da un altro comando **Scarica ora** .

-   Utilizzare le condizioni di licenza, non il contratto di licenza, il contratto di licenza con l'utente finale o il contratto di licenza.

Per altre linee guida, vedere [stile e tono](text-style-tone.md).

## <a name="documentation"></a>Documentazione

-   Come verbo, la configurazione è costituita da due parole. come aggettivo o sostantivo, il programma di installazione è una parola.
-   Il programma di installazione è in maiuscolo e non è sillabato.
-   Utilizzare installa per fare riferimento all'aggiunta di hardware o software a un sistema di computer.
-   Non usare Install come nome. In alternativa, usare l'installazione.
-   Usare riavvia, non riavviare. Indica che si tratta del computer, non di un programma, che sta per essere riavviato.

 

 