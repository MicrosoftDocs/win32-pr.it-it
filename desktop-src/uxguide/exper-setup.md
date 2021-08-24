---
title: Eseguire la configurazione
description: Gli utenti non si diverte a installare il software, quindi le esperienze di configurazione moderne devono essere semplici, efficienti e senza problemi.
ms.assetid: ed0265a6-4c39-4a1f-9493-e316a6519df7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 905411c5ae08d2112943088d514ab300abb19ec2b8081158ebdfd896fc2c61ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119818274"
---
# <a name="setup"></a>Eseguire la configurazione

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Gli utenti non si diverte a installare il software, quindi le esperienze di configurazione moderne devono essere semplici, efficienti e senza problemi.

Il programma di installazione si riferisce in genere all'esperienza di installazione e configurazione iniziale di un programma. Tuttavia, il programma di installazione può anche fare riferimento all'intero ciclo di vita dell'installazione, inclusi l'installazione iniziale, gli aggiornamenti incrementali del programma (ad esempio gli aggiornamenti della versione o i Service Pack), il ripristino e la disinstallazione.

La maggior parte degli utenti considera la configurazione come un'operazione necessaria, da eseguire il più rapidamente possibile. Lo scopo dell'installazione del programma è usarlo, non prendere decisioni innumerabili sulla configurazione e sull'utilizzo o, ancora peggiore, dedicare molto tempo a rispondere alle domande personali usate per scopi di registrazione o marketing.

![Screenshot che mostra una finestra di dialogo di installazione con quattro opzioni.](images/exper-setup-image1.png)

Un'esperienza di configurazione semplificata.

L'esperienza di configurazione combinata con il primo uso del programma è nota come prima esperienza. Il programma deve offrire agli utenti una prima esperienza semplificata. Ogni domanda o passaggio che non è necessario o potrebbe essere posticipato ne ritarda l'uso del programma. I programmi di installazione troppo complessi sono reliquie di un'età diversa.

**Nota:** Le linee guida relative alla [prima esperienza di](exper-first-exper.md) utilizzo di un programma e delle procedure [guidate](win-wizards.md) sono presentate in articoli separati.

## <a name="is-this-the-right-user-interface"></a>Si tratta dell'interfaccia utente giusta?

Anche se tutti i Windows Microsoft necessitano di un programma di installazione, è possibile scegliere dove inserire le impostazioni del programma:

-   Eseguire la configurazione
-   Primo uso del programma
-   Opzioni di programma centralizzate
-   Nel contesto dell'uso della funzionalità

**Configurazione**

Presentare le impostazioni nel programma di installazione se:

-   Le impostazioni corrette sono necessarie per usare il programma e si applicano a tutti gli utenti.
-   L'uso delle impostazioni predefinite non è accettabile, perché non esiste un'impostazione predefinita sicura, è probabile che gli utenti scenzino impostazioni non predefinite o che le impostazioni predefinite richiedano il consenso dell'utente.
-   Gli utenti devono, ma non è probabile, modificare le impostazioni importanti dopo l'installazione.

**Primo uso del programma**

Presentare le impostazioni al primo utilizzo del programma se:

-   Le impostazioni corrette sono necessarie per usare il programma e si applicano ai singoli utenti.
-   L'uso delle impostazioni predefinite non è accettabile, perché non esiste un'impostazione predefinita sicura, è probabile che gli utenti scenzino impostazioni non predefinite o che le impostazioni predefinite richiedano il consenso dell'utente.
-   Gli utenti devono, ma non è probabile, modificare le impostazioni importanti usando le opzioni del programma.
-   Le impostazioni personalizzano un'esperienza di base o un'esperienza fondamentale per l'identificazione personale di un utente con il programma.

Per tali impostazioni, è probabile che gli utenti esereranno scelte migliori all'interno del contesto del programma rispetto all'installazione.

**Opzioni di programma centralizzate**

Presentare le impostazioni nella finestra di dialogo [delle opzioni del programma](win-property-win.md) se si verificano tutte le condizioni seguenti:

-   Esistono impostazioni predefinite che funzionano bene per la maggior parte degli utenti.
-   Sono disponibili molte impostazioni che si applicano a funzionalità e attività.
-   È più probabile che gli utenti si aspettino di trovare le impostazioni in una posizione centralizzata.

**Nel contesto dell'uso della funzionalità**

Presentare le impostazioni nel contesto pertinente se si verificano tutte le condizioni seguenti:

-   Esistono impostazioni predefinite che funzionano bene per la maggior parte degli utenti.
-   Esiste un numero ridotto di impostazioni indipendenti per una funzionalità specifica.
-   È più probabile che gli utenti si aspettino di trovare le impostazioni con la funzionalità associata rispetto a una posizione centralizzata.
-   Esiste una posizione ovvia nell'interfaccia utente per accedere alle impostazioni.

Con un'attenta attenzione al posizionamento delle impostazioni di configurazione, è possibile ridurre il carico di lavoro per gli utenti durante la prima esperienza con il programma.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

### <a name="design-a-lightweight-setup"></a>Progettare una configurazione leggera

Welcome, next, next, next, next, next, install, finish, congratulations! Questa esperienza di configurazione è familiare? In passato, i programmi di installazione adottano questo tipo di progettazione inefficiente: una lunga sequenza di schermate, che invita gli utenti in una sequenza di clic senza senso solo per attraversarla.

Se gli utenti descrivono la configurazione del programma con parole come rapide e semplici, stanno sicuramente evoluzionando l'esperienza. Preferirebbe usare il programma anziché configurarlo.

**Esaminare la progettazione dell'installazione per domande, opzioni, pagine e percorsi non fondamentali e non fare altro che eliminarli.** Eseguire ricerche degli utenti per individuare le opzioni effettivamente necessarie per gli utenti e assicurarsi che non fare clic con attenzione sul pulsante Avanti in tutte le pagine. Rinviare le opzioni o le domande che vengono più trattate nel contesto del programma in esecuzione.

Molti programmi di installazione offrono pagine standard non perché sono necessarie o utili, ma perché sono standard. Ad esempio, le pagine di benvenuto, le pagine di riepilogo e le pagine di congratulazioni spesso aggiungono solo clic. Al contrario, il programma di installazione deve aggiungere pagine solo se sono necessarie per completare l'attività di installazione. Per linee guida sui tipi di pagine di configurazione e su come valutarli, vedere [Tipi di pagina](#page-types) più avanti in questo articolo.

![Screenshot della prima pagina di configurazione della procedura ](images/exper-setup-image2.png)

In questo esempio, il programma di installazione elimina la tradizionale pagina di benvenuto e diventa subito aziendale.

Anche se potrebbe essere necessario offrire diversi rami di configurazione (un'esperienza rapida e tipica e un'esperienza personalizzata più controllabile), assicurarsi di disporre di opzioni personalizzate sufficienti per garantire la complessità aggiuntiva. Non aggiungere rami a meno che non sia necessario. Alcune opzioni non importanti in un ramo personalizzato suggeriscono la necessità di riorganizzare la progettazione dell'installazione.

Un altro motivo per semplificare la configurazione è che gli utenti inesperti a volte sovraanalizzano le opzioni, temendo che una scelta errata possa essere irreversibile o distruttiva. Forzando gli utenti a prendere decisioni su ciò che non comprendono o a cui non è a cui si è a conoscenza, possono renderli insodetti, incompetenti e persino frustranti. Non è una buona prima impressione. È meglio farlo in modo rapido, a proprio agio e in sicurezza esplorando le funzionalità del programma e prendendo decisioni migliori sulle opzioni di funzionalità in quel momento. Per altre linee guida, vedere [Configurazione della struttura più](#streamlining-setup) avanti in questo articolo.

Cercare di rendere l'esperienza di installazione [il più semplice possibile, ma non più semplice.](/previous-versions//dn742474(v=vs.85)) I programmi destinati a utenti altamente tecnici potrebbero richiedere una configurazione complessa. Ad esempio, il team Microsoft SQL Server ha scoperto che gli amministratori di database preferiscono mantenere il controllo su molte opzioni di installazione, ad esempio i percorsi dei file. Inoltre, SQL Server è un'applicazione aziendale di grandi dimensioni, con una serie di componenti che differiscono notevolmente per scopo e funzionalità. Per semplicità, quindi, la configurazione deve riflettere la complessità del prodotto e le aspettative e le esigenze degli utenti.

Tuttavia, tali programmi di installazione complessi dovrebbero essere l'eccezione, non la regola. La maggior Windows programmi deve cercare di avviare il processo di installazione con un singolo passaggio semplice.

### <a name="setup-phases"></a>Fasi di configurazione

I programmi di installazione ben progettati consentono agli utenti di eseguire altre attività durante l'attività di download e copia di file dispendiosa in termini di tempo. Per l'esecuzione automatica, i programmi di installazione sono progettati per avere quattro fasi separate:

-   **Fase decisionale.** Gli utenti indicano come desiderano che il programma sia installato e configurato.
-   **Fase di download.** Per i programmi scaricati da Internet. Se il programma ha più applicazioni o versioni, gli utenti indicano cosa scaricare durante la fase decisionale.
-   **Fase di installazione.** Il programma di installazione copia i file e apporta le modifiche di configurazione appropriate.
-   **Fase di completamento.** Tutti i dettagli, i passaggi o i problemi rimanenti vengono risoluzione.

Poiché la fase di installazione potrebbe richiedere molto tempo, questa fase deve essere progettata per essere eseguita fino al completamento senza alcun coinvolgimento dell'utente. Ciò significa che tutte le domande devono essere poste durante la fase decisionale e tutti i problemi che si verificano devono essere accodati e affrontati nella fase di completamento. **Se la fase di installazione richiede più di un minuto, si supponga che gli utenti esee stiano eseguendo altre operazioni durante le fasi di download e installazione.**

**Non corretto:**

![screenshot di € install auto-reporting?' dialogo ](images/exper-setup-image3.png)

In questo esempio, il programma di installazione interrompe lo stato di avanzamento per porre una domanda che avrebbe dovuto essere posta durante la fase decisionale.

### <a name="present-helpful-progress"></a>Presentare lo stato di avanzamento utile

Se gli utenti attendono con paziente attesa la fase di installazione dell'esperienza di installazione, ad esempio osservando un indicatore di stato fino al suo completamento apparente, solo per osservare la reimpostazione e la ripartizione dell'indicatore di stato, c'è un vero senso di soddisfazione. Lo stato di avanzamento segnalato era fuorviante e in definitiva inutile.

Una variazione in questo scenario difficile è l'installazione "brinksmanship": gli utenti vedono il completamento dello stato di avanzamento, ad esempio il 99%, ma sono obbligati ad attendere una quantità di tempo sproporzionata prima di arrivare infine al 100%. Quindi, in termini di ciò che è più importante per l'utente, una promessa implicita sulla quantità di tempo di attesa, l'attestazione del 99% di completamento è indotta.

Durante le fasi di download e installazione, gli utenti hanno in genere due aspetti da sapere: se devono attendere o eseguire altre operazioni e la configurazione verrà eseguita a breve. Anche se nel processo di configurazione sono presenti variabili sufficienti per impedire di fornire informazioni di stato perfettamente accurate, il feedback sullo stato di avanzamento deve essere sufficientemente accurato per rispondere a queste due domande e impostare le aspettative appropriate. Oltre a un indicatore di stato, è possibile includere una breve affermazione sul tempo complessivo previsto per il processo.

![Screenshot della finestra di dialogo che mostra lo stato di avanzamento dell'installazione ](images/exper-setup-image4.png)

In questo esempio la pagina di stato include una breve dichiarazione generale sul tempo necessario per l'installazione.

I programmi di installazione efficaci usano gli barre di stato in modo efficace per fornire agli utenti informazioni utili sullo stato di avanzamento del programma di installazione. Per altre linee guida, vedere [ProgressBars](progress-bars.md).

### <a name="design-for-all-setup-scenarios"></a>Progettare per tutti gli scenari di configurazione

I programmi di installazione moderni devono essere progettati per gestire un'ampia gamma di scenari di installazione:

-   L'utente del programma lo sta installando da un disco o da una condivisione file di rete.
-   L'utente del programma lo sta scaricando dal Web.
-   Un OEM (Original Equipment Manufacturer) include il programma nel computer dello stabilimento.
-   Un professionista IT sta installando il programma in molti computer in un'organizzazione.
-   Un utente diverso dall'utente sta installando il programma , ad esempio un padre per conto di un figlio o un collega che usa lo stesso computer di un altro collega.

In questi scenari, non è consigliabile presupporre che gli utenti installino sempre il programma per se stessi (rendendo inappropriate le opzioni relative alle preferenze personali), monitorino attentamente il processo (rendendo importante l'installazione automatica) o vogliano anche un'interfaccia utente grafica per l'attività.

### <a name="dont-forget-the-uninstall-experience"></a>Non dimenticare l'esperienza di disinstallazione

Per completare il ciclo di vita dell'installazione del software, gli utenti devono essere in grado di rimuovere il software non necessario o non più necessario. Ciò è particolarmente importante se il programma non è stato installato automaticamente, ad esempio se è stato precaricato nel computer.

### <a name="handle-technical-support-strategically"></a>Gestire il supporto tecnico in modo strategico

L'installazione del programma è l'unica attività che tutti gli utenti devono completare correttamente. Se gli utenti non riescono a installare il programma, è necessario fornire loro un costoso supporto tecnico oppure non sono più gli utenti.

Progettare il programma di installazione per fornire al team di supporto tecnico le funzionalità e le informazioni necessarie per consentire agli utenti di eseguire correttamente l'installazione. Questi dettagli in genere non devono essere esposti agli utenti, ma devono essere immediatamente accessibili quando necessario.

**Non corretto:**

![Screenshot dell'etichetta che mostra il nome del server com ](images/exper-setup-image5.png)

In questo esempio l'indicatore di stato mostra dettagli significativi solo per il supporto tecnico.

Mantenere semplice l'esperienza utente normale, senza ingombrare le informazioni che hanno valore solo per il supporto tecnico. Registrare invece le informazioni di supporto in un file di log del programma di installazione. E ancora più importante, aiutare gli utenti a evitare la necessità di supporto tecnico con messaggi di errore chiari e concisi che spiegano i problemi e forniscono soluzioni pratiche. Se necessario, fornire collegamenti ad articoli della Guida. Valutare la possibilità di fornire un'opzione di ripristino al programma di installazione per ripristinare file o impostazioni mancanti o danneggiati.

**Se si eservino solo tre operazioni...**

1.  1. Rendere la configurazione il più semplice e leggera possibile. Tenere presente che gli utenti non apprezzano la configurazione, ma la apprezzano. Esaminare con attenzione ogni domanda, opzione, pagina e percorso e tagliare tutto ciò che non è essenziale per completare la configurazione.
2.  2. Progettare per tutti gli scenari di installazione, incluse le installazioni automatica, le installazioni con script e la disinstallazione. Per installazioni automatica efficienti, assicurarsi che vi sia una netta separazione tra le fasi di installazione.
3.  3. Progettare il programma di installazione in modo che gli utenti possano risolvere i problemi di configurazione da soli, ma anche registrare le informazioni necessarie per il supporto tecnico nel caso specifico. Tenere presente che la configurazione è l'unica attività che tutti gli utenti devono completare correttamente.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Applicare le linee guida standard della procedura guidata per i programmi di installazione guidata.** Usare queste linee guida per determinare una buona progettazione della pagina, una navigazione efficace, etichette di controllo efficaci, l'uso di istruzioni principali e l'uso della Guida.
-   **Consente agli utenti di riavviare il programma di installazione dal punto in cui si sono erti se richiede molto input dell'utente o se il completamento richiede molto tempo.** Se gli utenti riavviano il programma dopo la chiusura prima del completamento, ripristinare l'input utente precedente e riavviare il programma di installazione in cui è stata interrotta.
-   **Non visualizzare le finestre di installazione ingrandite.** La visualizzazione di una finestra di configurazione ingrandita presuppone che gli utenti dia la loro attenzione indivisa alla configurazione, il che è improbabile. Scegliere invece una dimensione appropriata per il contenuto per mantenere un aspetto semplice.

### <a name="windows-integration"></a>Windows integrazione

-   **Assegnare al file di installazione il nome "Setup.exe".** "Install.exe" è un'alternativa accettabile. Ciò consente Windows (e gli utenti) di riconoscere il file come programma di installazione.
    -   **Eccezione:** Per i programmi scaricati da Internet, aiutare gli utenti a gestire e organizzare la cartella Download includendo il nome del programma nel nome del file di installazione. Ad esempio, SetupVisualStudioExpress2008.exe.
-   **Copiare i file di programma nei percorsi file system posizione.** In questo modo gli utenti e Windows trovare e organizzare meglio i file. Per altre informazioni, vedere le linee guida [per l'utilizzo Windows dello spazio dei nomi del file system.](../fileio/naming-a-file.md#namespaces)

### <a name="user-account-control"></a>Controllo dell'account utente

-   **Firmare digitalmente il file eseguibile di installazione.** I file eseguibili firmati presentano molti vantaggi, incluso l'uso di un'interfaccia utente più specifica per l'elevazione dei privilegi del controllo dell'account utente. Per informazioni sulla firma dei file, vedere [Introduzione alla firma del codice.](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   **Se una configurazione potrebbe richiedere l'elevazione dei privilegi, elevare i privilegi il più tardi possibile.** Visualizzare l'interfaccia utente di elevazione dei privilegi solo dopo che l'utente ha eseguito il commit a un'opzione che richiede l'elevazione dei privilegi. In genere, l'interfaccia utente di elevazione dei privilegi viene visualizzata durante la fase di installazione, non nella fase decisionale. Tuttavia, se un'installazione richiede sempre l'elevazione dei privilegi, elevare i privilegi al punto di ingresso.
-   **Richiedere sempre l'elevazione dei privilegi per la disinstallazione.** In questo modo si impedisce al malware di disinstallare software critico senza che gli utenti lo sappiano.
-   **Dopo l'elevazione dei privilegi, rimanere elevati fino a quando i privilegi elevati non sono più necessari.** Gli utenti non devono elevare più volte i privilegi per completare l'installazione di un programma.
-   **Se sono necessari privilegi speciali per l'installazione, verificare le credenziali dell'utente e segnalare eventuali problemi nella prima o nella seconda pagina.** Non consentire agli utenti di eseguire molto lavoro solo per scoprire di non avere le credenziali corrette per completare l'installazione.
-   **Richiedere i privilegi minimi possibili.** Ad esempio, gli amministratori non sono in grado di installare software che richiede credenziali di amministratore di dominio.

Per altre linee guida, vedere [Controllo dell'account utente.](winenv-uac.md)

### <a name="restarting-windows"></a>Riavvio Windows

-   **Evitare di riavviare Windows.** La maggior parte dei programmi deve essere installata senza riavviare Windows. Il motivo principale per cui le installazioni o gli aggiornamenti del programma richiedono un riavvio del sistema è che alcuni dei file coinvolti sono attualmente usati da un programma in esecuzione. In questo caso, un'alternativa migliore consiste nel rendere gli utenti consapevoli della situazione, consentire agli utenti di chiudere questi programmi e ripetere l'azione. Per altre informazioni su come evitare i riavvii, vedere [Gestione riavvio.](../rstmgr/restart-manager-portal.md)
-   **Se il programma di installazione deve essere riavviato Windows:**
    -   **Usare un singolo riavvio.** Ritardare il riavvio richiesto da tutti i prerequisiti fino a quando il programma e i relativi aggiornamenti non vengono installati completamente.
    -   **Consentire agli utenti di determinare quando si verifica.** Non riavviare automaticamente Windows, perché gli utenti potrebbero perdere il lavoro. Assicurarsi che sia chiaro agli utenti che hanno la possibilità di scegliere.

        **Non corretto:**

        ![Screenshot della finestra di dialogo con riavvio e annullamento ](images/exper-setup-image6.png)

        In questo esempio gli utenti non sembrano avere la possibilità di scegliere quando riavviare Windows.

    -   **Se l'utente sceglie di non riavviare Windows immediatamente, presentare eventuali commenti finali come esito positivo, non come errore.** Anche se tecnicamente l'installazione non è stata completata fino al riavvio, dal punto di vista dell'utente ha avuto esito positivo.

### <a name="streamlining-setup"></a>Configurazione della struttura

-   **Quando possibile, avviare il processo di installazione con un unico passaggio.** Ad esempio, invece di aggiungere una pagina separata nel programma di installazione per le condizioni di licenza, è possibile fornire un collegamento a esse. Se si collegano alle condizioni:
    -   Formulare il pulsante di commit come "Accetto e installa" per richiedere il consenso esplicito per accettare le condizioni di licenza.
    -   Assicurarsi che il collegamento al contratto di licenza non possa essere interrotto collegando un file locale al programma di installazione anziché a una pagina Web.
    -   Consente di stampare il contratto di licenza dalla relativa finestra di visualizzazione.
-   **Eliminare le opzioni e le domande non necessarie.**
    -   Posticipare le opzioni più appropriate per il primo utilizzo del programma o della funzionalità.

        ![Screenshot della finestra di dialogo con l'opzione delle impostazioni personalizzate ](images/exper-setup-image7.png)

        In questo esempio, Windows Media Player presenta le opzioni di privacy per utente al primo uso del programma.

    -   Non porre domande agli utenti sullo stato del sistema. Rilevare queste informazioni automaticamente e chiedere agli utenti di verificare solo se c'è un motivo per modificare.
    -   Non porre domande sui dettagli non importanti. Per i programmi Windows, ad esempio, è possibile presupporre che sia necessario copiare i file di programma nella cartella Programmi.

        **Non corretto:**

        ![Screenshot della finestra di dialogo con il percorso di installazione ](images/exper-setup-image8.png)

        In questo esempio il programma di installazione deve essere semplificato eliminando la richiesta di input del percorso del file. Data la dimensione del programma, la maggior parte degli utenti non è importante e fare semplicemente clic su Avanti.

    -   Non chiedere l'autorizzazione per eseguire comunque le cose da non fare. Ad esempio, la maggior parte dei programmi non deve includere un'opzione per inserire l'icona del programma sul desktop.
    -   Non confermare l'annullamento della configurazione. Se gli utenti fa clic su Annulla durante l'installazione, presupporre che l'annullamento sia stato intenzionale e chiudere il programma senza conferma. Se si rischia di perdere tempo o impegno significativo, consentire agli utenti di riavviare il programma di installazione e riprendere dal punto in cui si sono ermati.

-   **Ottimizzare per l'installazione automatica.**
    -   Presentare tutte le opzioni e le domande durante la fase decisionale.
    -   Per le fasi di download e installazione, ritardare la richiesta di input dell'utente per eventuali problemi riscontrati fino alla fine della fase. In questo modo, gli utenti possono lasciare l'installazione automatica fino a quando non tornano per comodità.
-   **Eliminare le pagine non necessarie.** Se la maggior parte degli utenti fa sempre clic su Avanti in una pagina, è consigliabile eliminare la pagina. Per linee guida sull'eliminazione di determinati tipi di pagine, vedere [Tipi di pagina.](#page-types)
-   **Eliminare il testo non necessario.**
    -   Rimuovere il testo ridondante dalle istruzioni e dalle etichette.
    -   Non illustrare i concetti di Windows di utilizzo, ad esempio:
        -   Come interagire con i controlli (esempi: per iniziare, fare clic su Avanti; Per altre opzioni, fare clic su Opzioni. Per altre informazioni, fare clic su ? .
        -   Funzionamento delle procedure guidate (ad esempio: per rivedere o modificare le impostazioni, fare clic su Indietro).
        -   Funzionamento del programma di installazione (ad esempio: questo programma copierà i file di programma nel disco rigido...).
-   **Eliminare il lavoro non necessario.**
    -   Specificare valori predefiniti validi:
        -   In genere, selezionare la risposta più sicura e privata come predefinita.
        -   Se la sicurezza e la privacy non sono fattori, selezionare la risposta più probabile o comoda.

            ![Screenshot della finestra di dialogo con il nome e la società visualizzati ](images/exper-setup-image9.png)

            In questo esempio il nome utente e l'organizzazione forniti per impostazione predefinita vengono ottenuti dal Registro di sistema.

        -   Se un'opzione è fortemente consigliata, è consigliabile selezionarla per impostazione predefinita o aggiungere "(consigliato)" alla relativa etichetta.

    -   Consente di far avanzare automaticamente le pagine quando una pagina non contiene input e l'attività viene eseguita correttamente, ad esempio con le pagine di download, installazione, avanzamento e aggiornamento. Al termine del passaggio, rimanere in queste pagine solo per visualizzare i problemi.
    -   Quando possibile, avviare automaticamente il programma al termine della configurazione, anziché visualizzare la pagina Congratulazioni o Completamento. Quando l'installazione viene eseguita in modo interattivo, presupporre che l'utente installi il programma per eseguirlo immediatamente, quindi l'esecuzione del programma è il feedback migliore per mostrare che l'installazione è stata completata. L'esecuzione automatica del programma non è pratica quando il programma di installazione installa più di un programma (ad esempio, una suite costituita da molti programmi), quando l'installazione non viene eseguita in modo interattivo o quando il processo di installazione non viene completato dopo l'installazione.

### <a name="page-types"></a>Tipi di pagina

**Pagine di benvenuto e Attività iniziali**

-   **Eliminare le pagine di benvenuto.** Anche se è un'ottima scelta, gli utenti in genere possono fare clic su Avanti senza leggere. E poiché gli utenti in genere ignorano queste pagine senza leggere, il testo non fa altro che indicare l'ovvio, per impostazione predefinita.

    **Non corretto:**

    ![Screenshot della schermata iniziale con avanti e annulla ](images/exper-setup-image10.png)

    In questo esempio l'utente non può fare altro che fare clic su Avanti.

-   **Usare una Attività iniziali solo se è necessario informare gli utenti sui prerequisiti per l'installazione.** Tali prerequisiti includono l'installazione del software o dell'hardware necessario, l'esecuzione delle modifiche e degli aggiornamenti di configurazione del sistema necessari, l'esecuzione di un backup del sistema per la protezione dalla perdita di dati o l'acquisizione delle informazioni necessarie che l'utente probabilmente non dovrebbe avere già.
-   **Quando possibile, fornire la possibilità di eseguire i prerequisiti direttamente dal programma di installazione.** Gli utenti devono eseguire i passaggi manualmente solo se non esiste un'alternativa.
-   Se non viene usata una Attività iniziali iniziale, includere il nome e la descrizione del programma nella prima pagina del **programma di installazione.** È possibile usare la lingua di benvenuto come testo introduttivo, purché lo scopo della pagina sia chiaro.

**Pagine delle condizioni di licenza**

-   **Scrivere le condizioni di licenza usando testo chiaro e conciso.** Usare il linguaggio normale. Evitare "legalese".
-   **Presentare usando un formato facile da leggere e analizzare.** Non usare lunghi passi di testo in maiuscolo.

    **Non corretto:**

    ![Screenshot delle condizioni di licenza in maiuscolo ](images/exper-setup-image11.png)

    In questo esempio, il testo maiuscolo e le dimensioni grandi del carattere rendono i termini difficili da leggere, forzando gli utenti a scorrere più del necessario.

-   **Richiedere il consenso esplicito per accettare le condizioni di licenza.** L'accettazione della licenza non deve mai essere selezionata per impostazione predefinita. Se i pulsanti di opzione vengono usati per indicare l'accettazione, lasciare deselezionate le opzioni per impostazione predefinita e richiedere agli utenti di accettare le condizioni prima di abilitare il pulsante Avanti.

    ![Screenshot della finestra di dialogo con il pulsante Avanti in grigio ](images/exper-setup-image12.png)

    In questo esempio il pulsante Avanti viene disabilitato finché gli utenti non accettano esplicitamente le condizioni di licenza.

-   **Non richiedere agli utenti di scorrere fino alla fine del testo delle condizioni di licenza prima che il pulsante Avanti sia abilitato.** Ciò impone agli utenti un carico superfluo per comprendere il motivo per cui il pulsante Avanti è disabilitato.
-   **Specificare un comando Stampa, con** un pulsante di comando o un menu di scelta rapida. Presentare i termini in un formato ottimizzato per la stampa.

**Pagine di registrazione del prodotto**

-   **Richiedere agli utenti di registrarsi solo se devono per usare il programma.** Spiegare chiaramente perché gli utenti devono registrarsi.
-   **Fornire la registrazione facoltativa solo se è presente un vantaggio utente chiaro,** ad esempio per notificare agli utenti gli aggiornamenti del prodotto. Lasciare deselezionata questa opzione per impostazione predefinita.
-   **Consentire agli utenti di registrarsi in un secondo momento.** Fornire un massimo di tre promemoria e consentire agli utenti di ignorare i promemoria con un solo clic.

**Pagine di ambito (tipiche, personalizzate o minime)**

-   **Preferisce eliminare questa pagina.** Si supponga che la maggior parte degli utenti voglia l'esperienza di configurazione tipica e progettare tale esperienza in modo che funzioni bene per la maggior parte degli utenti.
-   Se è necessario includere una pagina di ambito:
    -   **Spiegare le differenze tra le opzioni in termini di funzionalità e spazio su disco.** Gli utenti si affidano alla chiarezza delle informazioni nella pagina dell'ambito per assicurarsi di fare la scelta giusta.
    -   **Assicurarsi che le opzioni personalizzate siano necessarie solo per una piccola percentuale di utenti, mentre la maggior parte degli utenti può ignorarle in tutta sicurezza.** In caso contrario, le opzioni devono essere nel percorso di installazione tipico.
    -   **Se gli utenti scelgono opzioni personalizzate, selezionare le opzioni di installazione tipiche per impostazione predefinita.** Gli utenti considerano l'installazione tipica come baseline e vogliono personalizzarlo aggiungendo o rimuovendo opzioni da tale baseline.
-   Se è necessario usare un'opzione di installazione personalizzata, valutare la possibilità di usare il ridimensionamento e il posizionamento dei pulsanti relativi per guidare la maggior parte degli utenti **all'installazione tipica.**

    ![Screenshot della finestra di dialogo con pulsante di installazione di grandi dimensioni ](images/exper-setup-image13.png)

    In questo esempio, la progettazione della pagina conferma visivamente il fatto che la maggior parte degli utenti deve scegliere l'installazione tipica.

**Pagine di input**

-   **Ridurre il numero di opzioni di installazione eseguendo l'operazione giusta per impostazione predefinita.** Per informazioni su come eliminare le opzioni, vedere [Configurazione della struttura.](#streamlining-setup)
-   **Specificare valori predefiniti accettabili quando possibile.** Scegliere impostazioni predefinite protette e private e accettabili per la maggior parte degli utenti senza modifiche.
-   **A meno che il programma non abbia requisiti insoliti, cercare di avere una singola pagina di domande e opzioni.** Se tuttavia il programma richiede diverse pagine di domande e opzioni, visualizzarle nel flusso della pagina principale della procedura guidata. Non provare a ridurre tecnicamente il numero di pagine inserendo le opzioni nelle finestre di dialogo o usando le schede.
-   ![Screenshot della finestra di dialogo di installazione con quattro opzioni ](images/exper-setup-image14.png)
-   In questo esempio le opzioni sono limitate a una singola pagina.
-   **Convalidare l'input appena possibile:**
    -   Proibire i caratteri non validi all'immissione.
    -   Usare [i numeri di riferimento](ctrl-balloons.md) per segnalare problemi con le caselle di testo non valide.
    -   Convalidare i campi correlati in una pagina quando gli utenti fa clic su Avanti.
    -   Convalidare i campi correlati tra le pagine di input non appena vengono rilevati problemi.
-   **Assegnare a tutti i percorsi di file modificabili un pulsante Sfoglia.** Consente agli utenti di specificare i percorsi di rete.
-   **Per la pagina di input finale, etichettare il pulsante di commit Installa e non Avanti.** Gli utenti non devono essere sorprese dall'avvio dell'installazione. Prima del punto di commit, assicurarsi che gli utenti possano modificare facilmente le impostazioni.

**Avviare le pagine di installazione**

-   **Eliminare questa pagina se non ha altro scopo che riepilogare le scelte precedenti e iniziare l'installazione.** Se le pagine di input sono chiare e sono poche, non è necessario riepilogarle. La pagina di input finale deve invece avere il pulsante Installa, che porta direttamente alla pagina di stato.
-   **Per le installazioni complesse destinate ai professionisti IT, fornire una pagina di installazione con un elenco completo delle modifiche che verranno eseguite dal programma di installazione.** Molti professionisti IT hanno un controllo rigoroso sulla gestione delle modifiche, quindi devono conoscere in dettaglio l'effetto dell'installazione del programma.

**Pagine di stato**

-   **Fornire sempre una pagina di stato,** anche se il programma viene installato rapidamente. Specificare una pagina di stato separata per [la fase di download,](#setup-phases) se disponibile. Disabilitare i pulsanti Indietro (o Indietro) e Avanti mentre la configurazione è in corso, ma lasciare il pulsante Annulla abilitato e reattivo.

    ![Screenshot della finestra di dialogo con l'indicatore di stato ](images/exper-setup-image15.png)

    Pagina di stato tipica.

-   **Usare un singolo indicatore di stato determinato.** Seguire le linee [guida dell'indicatore di stato determinate,](progress-bars.md)tra cui:
    -   Indicare chiaramente il completamento. Non lasciare che un indicatore di stato passi al 100% a meno che l'operazione non sia stata completata.
    -   Non riavviare lo stato di avanzamento. Un indicatore di stato perde il valore se viene riavviato (ad esempio perché viene completato un passaggio dell'operazione) perché gli utenti non hanno modo di sapere quando l'operazione verrà completata. In alternativa, tutti i passaggi nell'operazione condividono una parte dello stato di avanzamento e fare in modo che l'indicatore di stato passi al completamento una sola volta.
-   **Fornire una descrizione concisa del passaggio corrente sopra l'indicatore di stato.** Per le installazioni rapide, tale testo non è necessario. l'indicatore di stato da solo è sufficiente. Per le installazioni che richiedono un minuto o più, il testo può essere utile per gli utenti che partecipano alla configurazione.
    -   **Usare frammenti di frase, che in genere iniziano con un verbo e terminano con i puntini di sospensione.** Esempi: copia di file, installazione dei componenti necessari.
    -   **Posizionare il testo sopra la barra, non sotto.**

        **Non corretto:**

        ![Screenshot del testo visualizzato sotto l'indicatore di stato ](images/exper-setup-image16.png)

        In questo esempio il testo esplicativo dovrebbe essere visualizzato sopra l'indicatore di stato.

    -   **Evitare di ingombrare la pagina di stato con dettagli non necessari.** Questa pagina non è per [il supporto](#handle-technical-support-strategically)tecnico, quindi non è necessario visualizzare i GUID di registrazione o i file specifici copiati.

        **Non corretto:**

        ![Screenshot del GUID visualizzato sull'indicatore di stato ](images/exper-setup-image17.png)

        In questo esempio, i dettagli tecnici, ad esempio i GUID, sono inutili per gli utenti.

**Pagine di errore**

-   **Se l'installazione non riesce con un problema significativo, visualizzare una pagina di errore che spiega i problemi insieme a passaggi pratici per risolverli.** Visualizzare la pagina con un'icona di errore. Non usare una finestra di dialogo a questo scopo.

    ![Screenshot della pagina di errore e dell'icona ](images/exper-setup-image18.png)

    In questo esempio l'errore di installazione viene spiegato in una pagina di errore, insieme ad alcuni passaggi per risolvere il problema.

-   **Se l'installazione viene completata con un piccolo problema ripristinabile, presentare il problema come attività aggiuntiva anziché come errore.** Usare un linguaggio positivo, orientato al successo, incoraggiante, non termini come errore, errore o problema. Non usare un'icona di errore.

**Pagine di completamento/congratulazioni**

-   **Quando si installa un singolo programma in modo interattivo, avviare il programma (e chiudere l'installazione guidata) per indicare la corretta installazione, anziché visualizzare una pagina di completamento. Eccezioni:**
    -   Le configurazioni eseguite dalla riga di comando non devono avviare i programmi.
    -   Gli aggiornamenti automatici (ad esempio, Windows) non devono avviare i programmi.
    -   L'installazione di Criteri di gruppo non deve avviare i programmi.
    -   Qualsiasi scenario di installazione professionale IT (perché non viene installato per uso personale).
-   **Se il programma di installazione include passaggi di completamento dopo l'installazione, elencarli in una pagina Completamento.** Tuttavia, per giustificare una pagina di completamento, assicurarsi che gli utenti esercitino probabilmente i passaggi e che i passaggi siano autenticamente dichiarati (ovvero non sono ovvi).

    **Non corretto:**

    ![Screenshot della pagina che mostra che la configurazione è stata completata ](images/exper-setup-image19.png)

    In questo esempio, una pagina di completamento non necessaria indica l'ovvio. Windows L'aggiornamento viene eseguito automaticamente, quindi gli utenti non possono eseguirlo manualmente.

-   **Quando si installa una suite di programmi, visualizzare una pagina Completamento per indicare l'esito positivo e tutti i passaggi successivi che potrebbero essere necessari.**

    ![Screenshot della pagina finale della configurazione di Office Suite ](images/exper-setup-image20.png)

    In questo esempio il programma di installazione ha installato più programmi, quindi non ha senso avviare automaticamente un programma specifico. Una pagina Di completamento è più appropriata.

### <a name="leaving-users-in-control"></a>Lasciare gli utenti sotto controllo

-   **Non raccogliere informazioni personali, ad esempio quella usata per scopi di marketing.** Il programma di installazione non è un'opportunità per eseguire il push del proprio programma, effettuare il cross-selling di altre offerte di programma o condurre ricerche di mercato; è possibile danneggiare la relazione di trust con gli utenti in questo modo.
-   **Non forzare gli utenti a rifiutare esplicitamente l'installazione di funzionalità facoltative.** Consentire loro di [acconsentire esplicitamente.](glossary.md) Ad esempio, gli utenti devono scegliere in modo esplicito di installare un Windows desktop.
-   **Consentire agli utenti di aggiungere o rimuovere funzionalità facoltative usando il programma di installazione dopo la configurazione iniziale.** Gli utenti possono eseguire questa attività usando **l'elemento Disinstalla o modifica del pannello** di controllo di un programma.
-   **Per le iniziative di miglioramento dell'esperienza del cliente, spiegare quali dati vengono trasmessi, come vengono usati e per quanto tempo vengono conservati.** A questo scopo, usare un collegamento a un argomento della Guida relativo all'informativa sulla privacy.
-   **Evitare di usare** il suono, perché molti scenari di installazione sono incustoditi e perché il suono può distrarre inutilmente anche durante le installazioni partecipate.

### <a name="security"></a>Sicurezza

-   **Per la configurazione basata su Internet, fornire automaticamente gli aggiornamenti della sicurezza durante la configurazione iniziale.** Gli utenti non devono eseguire l'aggiornamento come passaggio separato.
-   **Evitare di consigliare agli utenti di disattivare i firewall come prerequisito per l'installazione del programma.**
-   Se è necessario disattivare un firewall, eseguire le operazioni seguenti:
    -   **Limitare la durata di questa condizione al più breve tempo possibile.**
    -   **Indicare in modo esplicito quando gli utenti possono riattivare il firewall.**

### <a name="uninstall"></a>Disinstallare

-   **La disinstallazione deve rimuovere tutte le tracce di un programma, incluse le seguenti:**
    -   File di programma, incluso il programma di installazione.
    -   menu Start voci.
    -   Icone del desktop e Avvio veloce icone (se presenti).
    -   Impostazioni del Registro di sistema.
    -   Associazioni di file.
-   **La disinstallazione deve lasciare i seguenti elementi:**
    -   I file creati dall'utente, ad esempio i file di documento.
    -   Librerie a collegamento dinamico condivise archiviate nella cartella System.

### <a name="help-and-support"></a>Guida e supporto

-   **Progettare il programma di installazione in modo che non necessiti della Guida ponendo domande chiare e auto-esplicativi.** Riservare la Guida per domande avanzate che traggono vantaggio da ulteriori spiegazioni.
-   **Non usare file Leggimi.** Questi file sono ora obsoleti e gli utenti non li leggono comunque. Fornire invece contenuto online, se necessario.
-   **Collegamento agli argomenti appropriati della Guida o alla risoluzione dei problemi relativi ai messaggi di errore di installazione.** Assicurarsi che il contenuto della Guida sia un percorso chiaro per risolvere il problema. Per altre informazioni, vedere [Messaggi di errore](mess-error.md).
-   **Creare file di log per acquisire informazioni utili al supporto tecnico.** Non ingombrare l'interfaccia utente di configurazione con dettagli relativi al supporto tecnico che non hanno significato per la maggior parte degli utenti. Usare invece i file di log a questo scopo.

### <a name="text"></a>Testo

-   **Essere concisi.** Le procedure guidate di installazione spesso sovrascindono le funzionalità e le opzioni, usando blocchi di testo difficili da analizzare rapidamente. **Eccezioni:**
    -   Scrivere tutti gli acronimi. La configurazione è spesso la prima esperienza degli utenti con il programma, quindi non presupporre che comprenda il gergo, ad esempio gli acronimi.
    -   Illustrare terminologia e concetti sconosciuti, preferibilmente sul posto, ma usando argomenti della Guida, se necessario.
-   **Preferire un tono descrittivo e professionale; evitare un tono troppo tecnico.**

**Non corretto:**

Limitare l'installazione per utente.

**Corretto:**

Installare solo per l'utente.

-   Non usare ora nelle etichette dei pulsanti di comando perché l'immediatezza del comando può essere data per scontata.
    -   **Eccezione:** Se necessario, usare ora per distinguere i comandi che avviano un'attività dai comandi che eseguono immediatamente un'attività.

![Screenshot del pulsante di download ](images/exper-setup-image21.png)

In questo esempio, facendo clic sul pulsante di comando si passa a una finestra o a una pagina che consente agli utenti di eseguire il download.

![Screenshot del pulsante Scarica adesso ](images/exper-setup-image22.png)

In questo esempio, facendo clic sul pulsante di comando viene eseguito immediatamente il download.

Un solo comando in un flusso di attività deve essere etichettato con ora. Ad esempio, un **comando Scarica ora** non deve mai essere seguito da un altro comando Scarica **ora.**

-   Usare le condizioni di licenza, non il contratto di licenza, il contratto di licenza, il contratto di licenza con l'utente finale o il contratto di licenza.

Per altre linee guida, vedere [Stile e tono.](text-style-tone.md)

## <a name="documentation"></a>Documentazione

-   Come verbo, la configurazione è di due parole. come aggettivo o sostantivo, la configurazione è una parola.
-   Il programma di installazione è in maiuscolo e non viene sillabato.
-   Usare installa per fare riferimento all'aggiunta di hardware o software a un sistema di computer.
-   Non usare install come sostantivo. Usare invece l'installazione.
-   Usare il riavvio, non il riavvio. Indicare che è il computer, non un programma, a riavviare.

 

 