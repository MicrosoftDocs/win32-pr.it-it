---
description: Uso del controllo genitori Impostazioni API
ms.assetid: 77a239e9-1cec-4710-b673-7d0cebd502e9
title: Uso del controllo genitori Impostazioni API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9dd75565559e8fe52413280e35abf076a57ad6
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885821"
---
# <a name="using-parental-controls-settings-apis"></a>Uso del controllo genitori Impostazioni API

Impostazioni vengono discussi prima della registrazione perché la registrazione è condizionale in base alle impostazioni dell'utente.

## <a name="wmi-api-settings-writeread"></a>API WMI Impostazioni scrittura/lettura

L'API WMI fornisce l'accesso non astratto (non elaborato) a tutte le impostazioni di cui è stata creata un'istanza dall'infrastruttura di controllo genitori, come definito nel file di schema Wpcsprov.mof. L'archivio delle impostazioni è presente nello spazio dei nomi \\ \\ radice CIMV2 \\ Applications WindowsParentalControls, con le definizioni di classe \\ seguenti che definiscono uno schema. Vengono notati gli elementi di estendibilità.

Per computer:

-   WpcSystemSettings (un'istanza)
    -   Metodi AddUser() e RemoveUser() per creare ed eliminare rispettivamente le impostazioni di controllo genitori per un SID specificato.
    -   Proprietà per il sistema di classificazione dei giochi corrente in vigore e rilevamento e notifica correlati al controllo amministrativo dei log.
    -   Estendibilità: proprietà per elenchi di esenzioni URL e applicazioni HTTP di sola lettura e di lettura/scrittura per il filtro del contenuto Web, ID di sostituzione e ID DLL risorsa nome e numero di eventi di log personalizzato per i campi e la registrazione del nome dell'intestazione.
-   WpcRatingsSystem (un'istanza per ogni sistema ratings installato)
    -   WpcRating (un'istanza per ogni livello di classificazione).
    -   WpcRatingDescriptor (un'istanza per ogni descrittore di classificazione).
-   Estendibilità: WpcExtension (un'istanza per ogni collegamento di estendibilità del pannello di controllo genitori aggiunto).
    -   Proprietà per GUID, sottosistema, ID, percorso della risorsa immagine, percorso della risorsa immagine di stato disabilitato, percorso eseguibile, percorso DELLA DLL della risorsa nome visualizzato e ID, percorso DLL risorsa sottotitolo e ID.

Per utente controllato:

-   WpcUserSettings (un'istanza per utente controllato)
    -   Proprietà per IL SID proprietario, flag di controllo genitori on/off, flag di accesso/off, flag di attivazione/disasamento dei limiti di tempo, sostituzioni del flag abilitato, maschera dell'orario di accesso e flag di attivazione/disconnessione delle restrizioni generali dell'applicazione.
    -   In Windows 8 la proprietà esistente rappresenta la prima mezz'ora per ogni ora. È stata aggiunta una nuova proprietà di mezz'ora per rappresentare la seconda metà di ogni ora. È stata introdotta una nuova proprietà aggiuntiva per rappresentare il limite di tempo giornaliero.

        **Windows 7 e Windows Vista:** Le restrizioni del timer supportano la granularità di 1 ora.

-   WpcWebSettings (un'istanza per utente controllato)
    -   Proprietà per SID proprietario, flag di filtro on/off, livello di filtro, flag bloccato per download di file, flag bloccato di siti nonrate.
-   WpcUrlOverride (un'istanza per URL consentito o negato in modo esplicito nell'elenco di override dell'URL usato come elenco di elementi consentiti/bloccati per il filtro del contenuto Web)
    -   Proprietà per il SID proprietario, l'URL interessato, lo stato consentito/bloccato.
-   WpcAppOverride (un'istanza per ogni percorso consentita in modo esplicito nell'elenco di override dell'applicazione Restrizioni generali applicazione)
    -   Proprietà per il SID proprietario. ID regola SAFER, percorso dell'applicazione.
-   WpcGamesSettings (un'istanza per utente controllato)
    -   Le proprietà per il SID proprietario, il flag consentito per i giochi, il GUID del sistema ratings per queste impostazioni, consentono il flag di giochi non classificati, l'ID della classificazione massima consentita nel sistema corrente, la raccolta di descrittori negati.
-   WpcGameOverride (un'istanza per ID applicazione consentita o negata in modo esplicito)
    -   Proprietà per il SID proprietario, ID applicazione che identifica il gioco, stato consentito/negato.

## <a name="data-representation-notes"></a>Note sulla rappresentazione dei dati

Diverse impostazioni all'interno dello schema sono vincolate dal file mof con attributo non \_ Null. Non possono essere impostate su una variante Null. Per tutti i tipi non di matrice, il codice di Controllo genitori inizializza i valori. Per le matrici, gli stati vuoti possono essere scritti usando una variante Null, una variante vuota o una matrice di varianti di dimensioni zero. Il provider WMI normalizzerà tutti questi elementi in una rappresentazione dello stato di variante Null in lettura.

## <a name="user-interface-extensibility-link-notes"></a>Interfaccia utente note sul collegamento di estendibilità

L'uso di WMI per registrare un collegamento di estendibilità dell'interfaccia utente richiede la specifica delle informazioni seguenti:

-   GUID: più collegamenti possono condividere lo stesso GUID se fanno parte di un pacchetto o di una suite comune.
-   Sottosistema: destinato a indicare le classificazioni dei tipi di collegamento, ad esempio suite o applicazioni autonome conformi
-   Name resource DLL path and ID :specifica la risorsa per il nome visualizzato da visualizzare per il collegamento.
-   Percorso DLL risorsa sottotitolo e ID: specifica la risorsa per il testo aggiuntivo sotto il nome.
-   Percorso immagine: percorso completo di una bitmap da 24 × 24 pixel (BMP), con una profondità di colore di 8 bit per pixel e preferibilmente un canale alfa. Questo valore viene specificato in modo coerente con le estensioni della shell: <file system path> , <negative resource ID> . Ad esempio: C: \\ Windows \\ System32 \\Wpccpl.dll,-20.
-   Percorso immagine disabilitato: uguale al percorso dell'immagine precedente, ad eccezione della variante della bitmap che mostra lo stato disabilitato. Questa immagine viene visualizzata quando il controllo genitori è disattivato.
-   Percorso exe: percorso completo di un eseguibile da richiamare tramite ShellExecute(). Questo percorso deve essere specificato con barre rovesciate, in caso contrario il collegamento non richiama l'eseguibile. L'aggiunta di un token %SID% dopo il percorso exe comporta l'esecuzione del collegamento sostituendo la stringa SID per l'utente per cui è attualmente visualizzata la pagina dell'hub. Il file eseguibile può quindi usare la stringa SID per gestire le funzionalità per l'utente specificato.

La disinstallazione dell'applicazione deve rimuovere la registrazione di un collegamento di estendibilità.

## <a name="web-extensibility-link-and-web-content-filter-override-notes"></a>Note sull'override del collegamento all'estendibilità Web e del filtro del contenuto Web

Impostando la proprietà FilterID sullo stesso GUID di un collegamento di estendibilità dell'interfaccia utente registrato esistente, il collegamento visualizzato verrà promosso da un collegamento generico in Altro Impostazioni al collegamento Restrizioni Web esclusivo. Si tratta di un'impostazione a livello di computer e pertanto l'LSP filtro contenuto Web predefinito ignora tutti i filtri per tutti gli utenti controllati. Un nome descrittivo deve essere impostato anche nella proprietà FilterName, specificata da un percorso alla DLL e all'ID della risorsa.

Il sistema di controllo genitori consiglia quanto segue da qualsiasi filtro Web che esegue l'override:

-   Rispettare lo stato generale di on/off di Controllo genitori per un utente.
-   Rispettare le Rapporto attività per un utente.
-   Monitorare la proprietà FilterID. Se viene modificato dal GUID specificato del fornitore, un altro filtro è diventato proprietario e il filtro del fornitore deve disabilitare se stesso. È stata aggiunta un'interfaccia COM per ridurre il sovraccarico dovuto al controllo periodico di questa modifica rispetto a una chiamata WMI.
-   È consigliabile rispettare le voci dell'elenco di esenzioni URL e applicazione HTTP di sola lettura e di lettura/scrittura.
-   È consigliabile rispettare l'elenco di override dell'URL per utente (elenco di elementi consentiti/bloccati).
-   Essere affidabili per passare rapidamente da un utente all'altro.

Il controllo genitori non presenta alcuna limitazione al modo in cui un filtro del contenuto Web o di altro tipo si collega Windows l'implementazione del filtro. I fornitori possono sfruttare gli investimenti correnti o le tecnologie preferite (LSP, TDI, altro).

La disinstallazione del filtro del fornitore deve annullare la registrazione delle voci FilterID e FilterName. Questa operazione viene eseguita impostando FilterID su GUID \_ NULL e FilterName su una variante Null. Il filtro del contenuto Web in-box verrà quindi ri-abilitato.

Si noti che la ri abilitazione del filtro Web predefinito filtra solo le nuove sessioni e non le sessioni attive da prima del passaggio.

## <a name="web-content-filter-allowblock-list-exportimport-format"></a>Formato di esportazione/importazione dell'elenco di elementi consentiti/bloccati del filtro contenuto Web

Questa funzionalità non è supportata in Windows 8.

**Windows 7 e Windows Vista:** Questa funzionalità è supportata.

&lt;Indirizzi Web&gt;

<URL AllowBlock="1">https://alloweddomain.com/&lt;/URL&gt;

<URL AllowBlock="1">https://allowedurl.com/allowed/default.html&lt;/URL&gt;

<URL AllowBlock="2">https://blockeddomain.com/&lt;/URL&gt;

<URL AllowBlock="2">https://blockedurl.com/blocked/default.html&lt;/URL&gt;

&lt;/WebAddresses&gt;

## <a name="application-restrictions-override-notes"></a>Note sull'override delle restrizioni dell'applicazione

Le sostituzioni delle restrizioni dell'applicazione vengono impostate in base all'utente per consentire percorsi o file binari specifici. Se viene configurato un nuovo utente con controllo genitori e sono necessarie sostituzioni delle restrizioni dell'applicazione per tale utente, è consigliabile usare la chiave run di Windows nel Registro di sistema con una piccola applicazione contrassegnata come che richiede la distribuzione dell'elevazione dei privilegi per scrivere le sostituzioni. Verrà visualizzata una richiesta di credenziali una sola volta per configurare le sostituzioni per l'utente, dopo di che i file binari di destinazione per le sostituzioni non saranno un problema per gli utenti a causa di ulteriori richieste di sostituzione dell'amministratore.

## <a name="actions-required-for-settings-changes-to-become-effective"></a>Azioni necessarie per Impostazioni le modifiche per diventare effettive

Se un amministratore modifica le impostazioni per un utente standard connesso, viene generato un messaggio di avviso. Indica che le modifiche alle impostazioni potrebbero non essere effettive fino a quando l'utente controllato non si disconnette e torna a eseguire di nuovo l'accesso. Si tratta di una progettazione conservativa. La maggior parte delle impostazioni avrà effetto quasi immediatamente mentre l'utente controllato è connesso. Un'eccezione è per i giochi, in cui le impostazioni saranno effettive alla successiva esecuzione Games Explorer o al tentativo di richiamare il gioco.

## <a name="sample-code"></a>Codice di esempio

Gli esempi C++ sono disponibili nell'SDK che illustra l'uso delle funzionalità di estendibilità delle impostazioni. Vedere la sezione Esempi di controllo genitori.

## <a name="independent-test-tools"></a>Proprietà Strumenti di test

L'ispezione di classi e istanze è facilitata dal plug-in Wmimgmt.msc e dallo Wbemtest.exe strumenti.

## <a name="64-bit-considerations"></a>Considerazioni a 64 bit

Nelle versioni del sistema Windows a 64 bit sono attualmente installati sia un provider WMI a 32 bit che un provider a 64 bit.

## <a name="general-code-development-and-debugging"></a>Sviluppo e debug di codice generali

Se Visual Studio viene usato per lo sviluppo di codice di gestione delle impostazioni, il debug locale richiederà l'esecuzione di Visual Studio con diritti di amministratore (richiamando con Esegui come amministratore tramite la riga di comando o l'opzione di clic con il pulsante destro del mouse). Ciò è dovuto all'isolamento dei processi e dei messaggi implementato dal controllo dell'account utente.

## <a name="minimum-compliance-api-settings-read"></a>Lettura dell'API di conformità Impostazioni minima

### <a name="interfaces-and-methods"></a>Interfacce e metodi

L'API conformità controllata dal file di intestazione Wpcapi.h fornisce un accesso semplificato in sola lettura alle impostazioni seguenti usando le interfacce COM.

[**I metodi dell'interfaccia radice IWindowsParentalControls**](/windows/desktop/api/Wpcapi/nn-wpcapi-iwindowsparentalcontrols) consentono di accedere a:

-   Metodi IWPCSettings:
    -   IsLoggingRequired(): la creazione di report attività è configurata come on per l'utente?
    -   GetLastSettingsChangeTime(): l'applicazione può essere a conoscenza se i criteri delle impostazioni sono stati modificati dopo un controllo precedente.
    -   GetRestrictions(): indica se le restrizioni Web, i limiti di tempo, le restrizioni di gioco o le restrizioni dell'applicazione sono impostate su on.
-   Metodi IWPCWebSettings:
    -   GetSettings(): recupera i flag per filtrare o disattivare e i download sono bloccati.
    -   RequestURLOverride(): immettere una richiesta nel meccanismo di override dell'amministratore (approvazione over-the-shoulder) che presenterà una finestra di dialogo contenente gli URL da approvato.
-   Metodi IWPCGamesSettings:
    -   IsBlocked(): per un ID applicazione di gioco specificato, è il gioco bloccato dai controlli genitori e per quale motivo.
-   GetVisibility(): fornisce informazioni sul fatto che l'interfaccia utente di Controllo genitori sia attualmente nascosta.
-   GetWebFilterInfo(): fornisce un'interfaccia per ottenere l'ID del filtro contenuto Web attualmente attivo.

### <a name="sample-code"></a>Codice di esempio

Gli esempi C++ vengono forniti nell'SDK che illustra l'uso dell'API conformità. Vedere la sezione Esempi di Controllo genitori.

 

 



