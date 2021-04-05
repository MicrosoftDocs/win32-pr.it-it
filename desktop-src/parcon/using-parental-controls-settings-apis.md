---
description: Uso delle API delle impostazioni dei controlli padre
ms.assetid: 77a239e9-1cec-4710-b673-7d0cebd502e9
title: Uso delle API delle impostazioni dei controlli padre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dde4827dfe3ed5ee7eec6787744e6ff92f18775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757754"
---
# <a name="using-parental-controls-settings-apis"></a>Uso delle API delle impostazioni dei controlli padre

Le impostazioni vengono discusse prima della registrazione, perché la registrazione è condizionale nelle impostazioni dell'utente.

## <a name="wmi-api-settings-writeread"></a>Lettura/scrittura delle impostazioni dell'API WMI

L'API WMI fornisce accesso non astratto (non elaborato) a tutte le impostazioni di cui è stata creata un'istanza dall'infrastruttura dei controlli padre come definito nel file di schema Wpcsprov. mof. L'archivio impostazioni esiste nello \\ \\ \\ \\ spazio dei nomi WindowsParentalControls applicazioni CIMV2 radice, con le seguenti definizioni di classe che definiscono uno schema. Sono indicati gli elementi di estendibilità.

Per computer:

-   WpcSystemSettings (un'istanza)
    -   Metodi AddUser () e RemoveUser () per creare ed eliminare le impostazioni dei controlli padre per un determinato SID, rispettivamente.
    -   Proprietà per il sistema di classificazione dei giochi correnti, nonché rilevamento e notifiche relative al controllo amministrativo dei log.
    -   Estensibilità: proprietà per le applicazioni HTTP di sola lettura e di lettura/scrittura e di esenzione URL per il filtro di contenuti Web, l'ID di sostituzione del filtro del contenuto Web e l'ID e il percorso della DLL della risorsa del nome e il numero di eventi di log personalizzato e la registrazione del nome dell'intestazione
-   WpcRatingsSystem (un'istanza per ogni sistema di classificazione installato)
    -   WpcRating (un'istanza per ogni livello di classificazione).
    -   WpcRatingDescriptor (un'istanza per ogni descrittore di classificazione).
-   Estensibilità: WpcExtension (un'istanza per ogni collegamento di estensibilità del pannello dei controlli padre).
    -   Proprietà per GUID, sottosistema, ID, percorso risorse immagine, percorso risorsa immagine stato disabilitato, percorso eseguibile, percorso DLL risorse nome visualizzato e ID, percorso e ID DLL risorse sottotitolo e ID.

Utente per controllo:

-   WpcUserSettings (un'istanza per ogni utente controllato)
    -   Proprietà per il SID proprietario, il flag di attivazione/disattivazione dei controlli padre, il flag di accesso/disattivazione, il flag per i limiti di tempo di attivazione/disattivazione, il flag di abilitazione delle sostituzioni, la maschera degli orari di accesso e il flag generale
    -   In Windows 8 la proprietà esistente rappresenta la prima mezz'ora per ogni ora. È stata aggiunta una nuova proprietà di mezz'ora per rappresentare la seconda metà di ogni ora. È stata introdotta una nuova proprietà aggiuntiva per rappresentare il limite di tempo giornaliero.

        **Windows 7 e Windows Vista:** Le restrizioni del timer supportano la granularità di 1 ora.

-   WpcWebSettings (un'istanza per ogni utente controllato)
    -   Proprietà per SID proprietario, flag on/off filtro, livello filtro, flag bloccato download file, flag bloccato siti non classificati.
-   WpcUrlOverride (un'istanza per URL consentita o negata in modo esplicito nell'elenco di override URL usato come elenco Consenti/blocca per il filtraggio del contenuto Web)
    -   Proprietà per il SID proprietario, l'URL interessato, lo stato consentito/bloccato.
-   WpcAppOverride (un'istanza per percorso è consentita in modo esplicito nell'elenco di override delle applicazioni per restrizioni applicazione generali)
    -   Proprietà per il SID proprietario. ID regola più sicuro, percorso dell'applicazione.
-   WpcGamesSettings (un'istanza per ogni utente controllato)
    -   Proprietà per il SID proprietario, il flag dei giochi consentiti, il GUID del sistema di classificazione per queste impostazioni, Consenti flag giochi senza classificazione, ID della classificazione massima consentita nel sistema corrente, raccolta di descrittori negati.
-   WpcGameOverride (un'istanza per ogni ID applicazione consentita o negata in modo esplicito)
    -   Proprietà per il SID proprietario, ID applicazione che identifica il gioco, stato consentito/negato.

## <a name="data-representation-notes"></a>Note sulla rappresentazione dei dati

Diverse impostazioni nello schema sono vincolate dal file con estensione MOF con attributo non \_ null. Non possono essere impostati su una variante null. Per tutti i tipi non matrice, il codice dei controlli padre Inizializza i valori. Per le matrici, è possibile scrivere stati vuoti utilizzando una variante null, una variante vuota o una matrice Variant con dimensione zero. Il provider WMI normalizza tutti questi in una rappresentazione di stato variant null durante la lettura.

## <a name="user-interface-extensibility-link-notes"></a>Note sul collegamento di estendibilità dell'interfaccia utente

Per registrare un collegamento di estendibilità dell'interfaccia utente, è necessario specificare le informazioni seguenti:

-   GUID: più collegamenti possono condividere lo stesso GUID se fanno parte di un pacchetto o di un gruppo comune.
-   Sottosistema: progettato per indicare le classificazioni dei tipi di collegamento, ad esempio gruppi o applicazioni compatibili autonome
-   Nome percorso della DLL della risorsa e ID: specifica la risorsa per il nome visualizzato da visualizzare per il collegamento.
-   ID e percorso della DLL della risorsa del sottotitolo: specifica la risorsa per il testo aggiuntivo sotto il nome.
-   Percorso immagine: percorso completo di una bitmap di 24 × 24 pixel (BMP) con 8 bit per pixel profondità di colore e preferibilmente un canale alfa. Questa operazione viene specificata in modo coerente con le estensioni della shell: <file system path> , <negative resource ID> . Ad esempio: C: \\ Windows \\ system32 \\Wpccpl.dll,-20.
-   Percorso immagine disabilitato: uguale al percorso dell'immagine precedente, ad eccezione della variante della bitmap che mostra lo stato disabilitato. Questa immagine viene visualizzata quando il controllo parentale è disattivato.
-   Percorso exe: percorso completo di un file eseguibile da richiamare tramite ShellExecute (). Questo percorso deve essere specificato con barre rovesciate oppure il collegamento non richiamerà il file eseguibile. L'aggiunta di un token% SID% dopo il percorso exe determinerà l'esecuzione del collegamento che sostituisce la stringa SID per l'utente per cui è attualmente in corso la visualizzazione della pagina Hub. Il file eseguibile può quindi utilizzare la stringa SID per gestire la funzionalità per l'utente specificato.

La disinstallazione dell'applicazione deve rimuovere una registrazione del collegamento di estensibilità.

## <a name="web-extensibility-link-and-web-content-filter-override-notes"></a>Note sull'override del filtro del contenuto Web e del collegamento di estendibilità Web

Impostando la proprietà FilterID sullo stesso GUID di un collegamento di estendibilità dell'interfaccia utente registrato esistente, il collegamento visualizzato verrà innalzato di livello da un collegamento generico in altre impostazioni al collegamento per le restrizioni Web esclusive. Si tratta di un'impostazione a livello di computer, quindi il filtro del contenuto Web incluso in LSP ignorerà tutti i filtri per tutti gli utenti controllati. È necessario impostare un nome descrittivo anche nella proprietà FilterName, specificata da un percorso alla DLL della risorsa e all'ID.

Il sistema di controlli padre consiglia quanto segue da qualsiasi filtro Web che esegue l'override:

-   Rispettare lo stato generale dei controlli padre per un utente.
-   Rispettare le impostazioni di report attività per un utente.
-   Monitorare la proprietà FilterID. Se viene modificato dal GUID specificato dal fornitore, un altro filtro ha assunto la proprietà e il filtro del fornitore dovrebbe disabilitarsi. È stata aggiunta un'interfaccia COM per ridurre l'overhead del controllo periodico di questa modifica rispetto a una chiamata WMI.
-   Si consiglia vivamente di rispettare le voci dell'elenco di esenzioni per l'applicazione HTTP di sola lettura e di lettura/scrittura e di URL.
-   È consigliabile rispettare l'elenco di override URL per utente (Consenti/blocca elenco).
-   Essere affidabili per il cambio rapido degli utenti.

I controlli padre non inseriscono alcuna limitazione sulla modalità di collegamento di un filtro di contenuto Web o di altro a Windows per l'implementazione del filtro. I fornitori possono sfruttare gli investimenti correnti o le tecnologie preferite (LSP, TDI, other).

La disinstallazione del filtro del fornitore deve annullare la registrazione delle voci FilterID e FilterName. Questa operazione viene eseguita impostando FilterID su GUID \_ null e FilterName su una variante null. Il filtro contenuto Web interno verrà quindi riabilitato.

Si noti che la riabilitazione del filtro Web in-box filtra solo le nuove sessioni e non le sessioni attive da prima del Commuter.

## <a name="web-content-filter-allowblock-list-exportimport-format"></a>Formato di esportazione/importazione dell'elenco di contenuti Web consentiti/bloccati

Questa funzionalità non è supportata in Windows 8.

**Windows 7 e Windows Vista:** Questa funzionalità è supportata.

<WebAddresses>

<URL AllowBlock="1">https://alloweddomain.com/</URL>

<URL AllowBlock="1">https://allowedurl.com/allowed/default.html</URL>

<URL AllowBlock="2">https://blockeddomain.com/</URL>

<URL AllowBlock="2">https://blockedurl.com/blocked/default.html</URL>

</WebAddresses>

## <a name="application-restrictions-override-notes"></a>Note sulle limitazioni dell'applicazione override

Le limitazioni dell'applicazione vengono impostate in base ai singoli utenti per consentire binari o percorsi specifici. Se è stato configurato un nuovo utente controllato dal padre e le restrizioni dell'applicazione sono necessarie per l'utente, è consigliabile usare la chiave di esecuzione di Windows nel registro di sistema con una piccola applicazione contrassegnata come richiesta di elevazione delle richieste distribuita per scrivere le sostituzioni. Questo comporterà una richiesta di credenziali monouso per configurare le sostituzioni per l'utente, dopo le quali i file binari di destinazione per le sostituzioni non saranno più fastidiosi per gli utenti a causa dell'ulteriore richiesta di override da parte dell'amministratore.

## <a name="actions-required-for-settings-changes-to-become-effective"></a>Le azioni necessarie per modificare le impostazioni diventano effettive

Se un amministratore modifica le impostazioni per un utente standard connesso, viene generato un messaggio di avviso. Indica che le modifiche apportate alle impostazioni potrebbero non essere effettive fino a quando l'utente controllato non si disconnette e si torna nuovamente. Si tratta di una progettazione conservativa. La maggior parte delle impostazioni avrà effetto quasi immediatamente mentre l'utente controllato è connesso. Un'eccezione è relativa ai giochi, in cui le impostazioni diverranno effettive al successivo avvio di Esplora giochi o alla chiamata del gioco.

## <a name="sample-code"></a>Codice di esempio

Gli esempi di C++ sono disponibili nell'SDK che illustra l'uso delle funzionalità di estensibilità delle impostazioni. Vedere la sezione Esempi di controlli padre.

## <a name="independent-test-tools"></a>Strumenti di test indipendenti

L'ispezione di classi e istanze è facilitata dal plug-in wmimgmt. msc e dallo strumento Wbemtest.exe.

## <a name="64-bit-considerations"></a>Considerazioni su 64 bit

le versioni del sistema operativo Windows a 64 bit includono attualmente sia un provider WMI a 32 bit che un provider 64 bit.

## <a name="general-code-development-and-debugging"></a>Sviluppo e debug di codice generale

Se si usa Visual Studio per lo sviluppo del codice di gestione delle impostazioni, il debug locale richiederà l'esecuzione di Visual Studio con diritti di amministratore (richiamando con Esegui come amministratore usando la riga di comando o con il pulsante destro del mouse). Ciò è dovuto all'isolamento dei processi e dei messaggi implementato da UAC.

## <a name="minimum-compliance-api-settings-read"></a>Lettura impostazioni API di conformità minime

### <a name="interfaces-and-methods"></a>Interfacce e metodi

L'API di conformità controllata dal file di intestazione Wpcapi. h fornisce un accesso semplificato in sola lettura alle seguenti impostazioni usando le interfacce COM.

I metodi dell'interfaccia radice di [**IWindowsParentalControls**](/windows/desktop/api/Wpcapi/nn-wpcapi-iwindowsparentalcontrols) forniscono l'accesso a:

-   Metodi di IWPCSettings:
    -   IsLoggingRequired (): la creazione di report attività è configurata su on per l'utente?
    -   GetLastSettingsChangeTime (): l'applicazione può essere a conoscenza se sono stati modificati i criteri di impostazione rispetto a un controllo precedente.
    -   Getrestrictions (): consente di leggere se le restrizioni Web, i limiti di tempo, le restrizioni del gioco o le restrizioni dell'applicazione sono impostate su on.
-   Metodi di IWPCWebSettings:
    -   GetSettings (): recupera i flag per i filtri on o off e i download bloccati.
    -   RequestURLOverride (): inserisce una richiesta nel meccanismo di sostituzione dell'amministratore (approvazione over the Shoulder) che presenterà una finestra di dialogo contenente gli URL da approvare.
-   Metodi di IWPCGamesSettings:
    -   Blocked (): per un determinato ID applicazione del gioco, è il gioco bloccato dai controlli padre e per quale motivo.
-   GetVisibility (): fornisce informazioni sul fatto che l'interfaccia utente dei controlli padre sia attualmente nascosta.
-   GetWebFilterInfo (): fornisce un'interfaccia per ottenere l'ID del filtro del contenuto Web attualmente attivo.

### <a name="sample-code"></a>Codice di esempio

Gli esempi di C++ sono disponibili nell'SDK che illustra l'uso dell'API di conformità. Vedere la sezione Esempi di controlli padre.

 

 



