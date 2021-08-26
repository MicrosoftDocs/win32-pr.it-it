---
title: Requisiti di certificazione desktop
description: Versione documento 10Document date 29 luglio 2015In questo documento sono contenuti i requisiti tecnici e le qualifica di idoneità che un'app desktop deve soddisfare per partecipare al programma di certificazione app desktop Windows 10.
ms.assetid: 0F19774E-5258-4152-BBD7-9C37A05C7F69
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4e78de8aef47479cdeb286b3c179a9a3c0520af4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879682"
---
# <a name="certification-requirements-for-windows-desktop-apps"></a>Requisiti di certificazione per Windows desktop

**Versione del documento:** 10

**Data del documento:** 29 luglio 2015

Questo documento contiene i requisiti tecnici e le qualifica di idoneità che un'app desktop deve soddisfare per partecipare al programma Windows 10 Di certificazione app desktop.

## <a name="welcome"></a>Benvenuto!

La Windows supporta un ampio ecosistema di prodotti e partner. La visualizzazione del logo Windows sul prodotto rappresenta una relazione e un impegno condiviso per la qualità tra Microsoft e l'azienda. I clienti si Windows il marchio del prodotto perché assicurano che soddisfi gli standard di compatibilità e funzionino bene Windows piattaforma. Il passaggio Windows certificazione dell'app consente di presentare l'app nel Centro compatibilità Windows ed è possibile visualizzare il logo di certificazione nel sito.

Il programma di certificazione app Windows è costituito da requisiti tecnici e di programma per garantire che le app di terze parti con il marchio Windows siano facili da installare e affidabili nei PC che eseguono Windows. I clienti sono molto interessati a stabilità, compatibilità, affidabilità, prestazioni e qualità nei sistemi acquistati. Microsoft si concentra sugli investimenti per soddisfare questi requisiti per le app software progettate per l'Windows per i PC. Queste attività includono test di compatibilità per la coerenza dell'esperienza, prestazioni migliorate e sicurezza avanzata nei PC che eseguono Windows software. I test di compatibilità Microsoft sono stati progettati in collaborazione con i partner del settore e sono continuamente migliorati in risposta agli sviluppi del settore e alla domanda dei consumatori.

Il kit di certificazione app Windows viene usato per convalidare la conformità a questi requisiti e sostituisce le versioni precedenti del kit usate per la convalida in Windows 7, Windows 8 o Windows 8.1. Il Windows App Certification Kit è uno dei componenti inclusi in Windows Software Development Kit (SDK) per Windows 10.

## <a name="app-eligibility"></a>Idoneità dell'app

Perché un'app sia idonea Windows 10 la certificazione dell'app desktop, deve soddisfare i criteri seguenti e tutti i requisiti tecnici elencati in questo documento.

-   Deve essere un'app autonoma
-   Deve essere eseguito in un computer Windows 10 locale
-   Può essere un componente client di un'app Windows Server certificata
-   Deve essere codice e funzionalità completa
-   Non deve comunicare con le app Windows Store tramite meccanismi locali, anche tramite file e chiavi del Registro di sistema, ad eccezione degli scenari aziendali supportati
-   Non deve compromettere o compromettere la sicurezza o la funzionalità del Windows sistema
-   Deve avere un nome univoco e non deve essere registrato da altri utenti
-   Tutti i componenti esterni devono essere certificati separatamente o conformi al kit di Windows app
-   Deve avere un'opzione di rifiuto esplicito per tutte le app in bundle

Se l'app desktop viene inviata alla categoria di prodotti anti-virus e/o anti-spyware (ad esempio, antimalware), deve essere conforme alle LINEE GUIDA DELLA PIATTAFORMA ANTIMALWARE. Prima dell'invio, è necessario che la licenza e l'INSERZIONE DELL'API ANTIMALWARE DI WINDOWS 10 siano state firmate e applicate. Il partner deve essere membro di o avere ricercatori membri di e in una delle organizzazioni elencate nel contratto. La funzionalità deve essere certificata Windows 10 da una delle organizzazioni elencate nel contratto. L'app deve essere stata testata almeno una volta negli ultimi 12 mesi e certificata per il rilevamento e la pulizia.

## <a name="1-apps-are-compatible-and-resilient"></a>1. Le app sono compatibili e resilienti

Le volte in cui un'app si arresta in modo anomalo o smette di rispondere causa molte frustrazioni da parte dell'utente. Si prevede che le app siano resilienti e stabili e l'eliminazione di tali errori consente di garantire che il software sia più prevedibile, gestibile, performante e affidabile.<dl> 1.1 L'app non deve assumere una dipendenza Windows modalità di compatibilità, messaggio AppHelp e altre correzioni di compatibilità  
1.2 L'app deve avere un manifesto di compatibilità e usare i GUID appropriati per le versioni supportate di Windows  
1.3 L'app deve essere in grado di riconoscere DPI usando il manifesto dell'assembly dell'applicazione anziché chiamando SetProcessDPIAware  
1.4 L'app non deve assumere una dipendenza dal runtime VB6  
1.5 L'app non deve caricare DLL arbitrarie per intercettare le chiamate API Win32 usando HKLM \\ Software \\ Microsoft Windows NT \\ \\ CurrentVersion Windows Dll \\ \_ AppInit.  
</dl>

## <a name="2-apps-must-adhere-to-windows-security-best-practices"></a>2. Le app devono rispettare Windows procedure consigliate per la sicurezza

L Windows procedure consigliate per la sicurezza consente di evitare la creazione di esposizione Windows di attacco. Le superfici di attacco sono i punti di ingresso che un utente malintenzionato potrebbe usare per sfruttare il sistema operativo sfruttando le vulnerabilità nel software di destinazione. Una delle peggiori vulnerabilità di sicurezza è l'elevazione dei privilegi.

Si noti che i test 2.1 2.6 sono applicabili solo alle app desktop testate in Windows 7, Windows 8 o Windows 8.1.<dl> 2.1 L'app deve usare ACL sicuri [e](/windows/desktop/SecAuthZ/access-control-lists) appropriati per proteggere i file eseguibili  
2.2 L'app deve usare elenchi di controllo di accesso sicuri e [appropriati](/windows/desktop/SecAuthZ/access-control-lists) per proteggere le directory  
2.3 L'app deve usare elenchi di controllo di accesso sicuri [e](/windows/desktop/SecAuthZ/access-control-lists) appropriati per proteggere le chiavi del Registro di sistema  
2.4 L'app deve [](/windows/desktop/SecAuthZ/access-control-lists) usare elenchi di controllo di accesso sicuri e appropriati per proteggere le directory che contengono oggetti  
2.5 L'app deve ridurre l'accesso non amministratore ai servizi vulnerabili a manomissioni  
2.6 L'app deve impedire il riavvio dei servizi con riavvii rapidi più di due volte ogni 24 ore  
</dl>

**Nota: l'accesso deve essere concesso solo alle entità che lo richiedono.**

Il Windows App Certification Program verificherà che le superfici di attacco di Windows non siano esposte verificando che gli ACL e i servizi siano implementati in modo da non mettere a rischio il sistema Windows.

## <a name="3-apps-support-windows-security-features"></a>3. Le app supportano Windows di sicurezza

Il Windows sistema operativo ha molte funzionalità che supportano la sicurezza e la privacy del sistema. Le app devono supportare queste funzionalità per mantenere l'integrità del sistema operativo. Le app compilate in modo non corretto possono causare sovraccarichi del buffer che possono, a sua volta, causare attacchi Denial of Service o consentire l'esecuzione di codice dannoso. <dl> 3.1 L'app non deve usare AllowPartiallyTrustedCallersAttribute (APTCA) per garantire l'accesso sicuro agli assembly con nome sicuro  
3.2 L'app deve essere compilata usando il flag /SafeSEH per garantire la gestione sicura delle eccezioni  
3.3 L'app deve essere compilata usando il flag /NXCOMPAT per impedire l'esecuzione dei dati  
3.4 L'app deve essere compilata usando il flag /DYNAMICBASE per la casualizzazione del layout dello spazio indirizzi (ASLR)  
3.5 L'app non deve leggere/scrivere le sezioni pe condivise  
</dl>

## <a name="4-apps-must-adhere-to-system-restart-manager-messages"></a>4. Le app devono rispettare i messaggi di System Restart Manager

Quando gli utenti avviano l'arresto, in genere hanno un forte desiderio di vedere l'arresto riuscito; possono avere fretta di uscire dall'ufficio e vogliono solo che i computer si spegnino. Le app devono rispettare questo desiderio non bloccando l'arresto. Anche se nella maggior parte dei casi, un arresto potrebbe non essere critico, le app devono essere preparate per la possibilità di un arresto critico.<dl> 4.1 L'app deve gestire gli arresti critici in modo appropriato <dl> In un arresto critico, le app che restituiscono FALSE a WM QUERYENDSESSION verranno inviate a WM ENDSESSION e chiuse, mentre quelle con timeout in risposta a \_ \_ WM \_ QUERYENDSESSION verranno terminate.  
</dl> </dd> 4.2 A GUI app must return TRUE immediately in preparation for a restart <dl> WM \_ QUERYENDSESSION con LPARAM = ENDSESSION \_ CLOSEAPP(0x1).  
Le app console possono chiamare SetConsoleCtrlHandler per specificare la funzione che gestirà le notifiche di arresto. Le app di servizio possono chiamare RegisterServiceCtrlHandlerEx per specificare la funzione che riceverà le notifiche di arresto.  
</dl> </dd> 4.3 Your app must return 0 within 30 seconds and shut down <dl> WM \_ ENDSESSION con LPARAM = ENDSESSION \_ CLOSEAPP(0x1).  
Come minimo, l'app deve prepararsi salvando i dati utente e indicando le informazioni necessarie dopo un riavvio.  
</dl> </dd> 4.4 Console apps that receive the CTRL\_C\_EVENT notification should shut down immediately  
4.5 Drivers must not veto a system shutdown event  
</dl>
<strong>Nota: le app che devono bloccare l'arresto a causa di un'operazione che non può essere interrotta devono spiegare il motivo all'utente.</strong> Usare ShutdownBlockReasonCreate per registrare una stringa che spiega il motivo all'utente. Al termine dell'operazione, l'app deve chiamare ShutdownBlockReasonDestroy per indicare che il sistema può essere arrestato.

## <a name="5-apps-must-support-a-clean-reversible-installation"></a>5. Le app devono supportare un'installazione pulita e reversibile

Un'installazione pulita e reversibile consente agli utenti di gestire correttamente (distribuire e rimuovere) le app nei propri sistemi.<dl> 5.1 L'app deve implementare correttamente un'installazione pulita e reversibile <dl> Se l'installazione non riesce, l'app dovrebbe essere in grado di eseguire il rollback e ripristinare lo stato precedente del computer.  
</dl> </dd> 5.2 Your app must never force the user to restart the computer immediately <dl> Il riavvio del computer non dovrebbe mai essere l'unica opzione al termine di un'installazione, disinstallazione o aggiornamento. Gli utenti dovrebbero avere la possibilità di riavviare in un secondo momento.  
</dl> </dd> 5.3 Your app must never be dependent on 8.3 short file names (SFN)  
5.4 Your app must never block silent install/uninstall  
5.5 Your app installer must create the correct registry entries to allow successful detection and uninstalls <dl> Windows strumenti di inventario e di telemetria richiedono informazioni complete sulle app installate. Se si usa un programma di installazione basato su MSI, msi crea automaticamente le voci del Registro di sistema seguenti. Se non si usa un programma di installazione msi, il modulo di installazione deve creare le voci del Registro di sistema seguenti durante l'installazione:  
</dl>

-   DisplayName
-   InstallLocation
-   Publisher
-   UninstallString
-   VersionMajor o MajorVersion
-   VersionMinor o MinorVersion

</dd> 5.6 The app must remove all of its entries from Add/ Remove Programs upon uninstall  
</dl>

## <a name="6-apps-must-digitally-sign-files-and-drivers"></a>6. Le app devono firmare digitalmente file e driver

Una firma digitale Authenticode consente agli utenti di assicurarsi che il software sia originale. Consente inoltre di rilevare se un file è stato manomesso, ad esempio se è stato infettato da un virus. L'imposizione della firma del codice in modalità kernel è una funzionalità Windows nota come integrità del codice ,che migliora la sicurezza del sistema operativo verificando l'integrità di un file ogni volta che l'immagine del file viene caricata in memoria. Ci consente di rilevare se codice dannoso ha modificato un file binario di sistema. Genera anche un evento di log di diagnostica e di controllo di sistema quando la firma di un modulo del kernel non viene verificata correttamente. <dl> 6.1 Tutti i file eseguibili (.exe, .dll, ocx, .sys, .cpl, drv, scr) devono essere firmati con un certificato Authenticode  
6.2 Tutti i driver in modalità kernel installati dall'app devono avere una firma Microsoft ottenuta tramite il Windows di certificazione hardware. Tutti i driver di filtro del file system devono essere firmati da Microsoft.  
6.3 Eccezioni ed esenzioni <dl> Le derozioni verranno considerate solo per i ridistribuibili di terze parti non firmati, esclusi i driver. Per la concessione di questa deroga è necessaria una prova di comunicazione che richiede una versione firmata dei ridistribuibili.  
</dl> </dd> </dl>

## <a name="7-apps-dont-block-installation-or-app-launch-based-on-an-operating-system-version-check"></a>7. Le app non bloccano l'installazione o l'avvio dell'app in base a un controllo della versione del sistema operativo

È importante che i clienti non siano artificialmente bloccati dall'installazione o dall'esecuzione dell'app quando non sono presenti limitazioni tecniche. In generale, se le app sono state scritte per Windows Vista o versioni successive di Windows, non devono controllare la versione del sistema operativo.<dl> 7.1 L'app non deve eseguire controlli di versione per verificare l'uguaglianza <dl> Se è necessaria una funzionalità specifica, verificare se la funzionalità stessa è disponibile. Se è necessario Windows 7, cercare Windows 7 o versione successiva (>= 6.2). In questo modo, il codice di rilevamento continuerà a funzionare nelle versioni future di Windows. I programmi di installazione dei driver e i moduli di disinstallazione non devono mai controllare la versione del sistema operativo.  
</dl> </dd> 7.2 Exceptions and Waivers will be considered for apps meeting the criteria below:

-   App fornite come un unico pacchetto eseguito anche in Windows 7, Windows 8 e Windows 8.1 e che devono controllare la versione del sistema operativo per determinare quali componenti installare in un determinato sistema operativo.
-   App che controllano solo la versione minima del sistema operativo (solo durante l'installazione, non in fase di esecuzione) usando solo le chiamate API approvate e che elencano correttamente il requisito di versione minima nel manifesto dell'app.
-   App di sicurezza (antivirus, firewall e così via), utilità di sistema (ad esempio deframmentazione, backup e strumenti di diagnostica) che controllano la versione del sistema operativo usando solo le chiamate API approvate.


</dl>

## <a name="8-apps-dont-load-services-or-drivers-in-safe-mode"></a>8. Le app non caricano servizi o driver in modalità sicura

Cassaforte consente agli utenti di diagnosticare e risolvere i Windows. I driver e i servizi non devono essere impostati per il caricamento in modalità sicura, a meno che non siano necessari per operazioni di sistema di base di , ad esempio driver di dispositivo di archiviazione o per scopi diagnostici e di ripristino, ad esempio gli scanner antivirus. Per impostazione predefinita, quando Windows è in modalità provvisoria, vengono avviati solo i driver e i servizi preinstallati con Windows.

-   8.1 Eccezioni ed esenzioni <dl> I driver e i servizi che devono essere avviati in modalità sicura richiedono una deroga. La richiesta di deroga deve includere ogni driver o servizio applicabile che scrive nelle chiavi del Registro di sistema SafeBoot e descrivere i motivi tecnici per cui l'app o il servizio deve essere eseguito in modalità sicura. Il programma di installazione dell'app deve registrare tutti questi driver e servizi usando queste chiavi del Registro di sistema:  
    </dl>
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Minimal
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Network

**Nota:** È necessario testare questi driver e servizi per assicurarsi che funzionino in modalità sicura senza errori.

## <a name="9-apps-must-follow-user-account-control-guidelines"></a>9. Le app devono seguire le linee guida di Controllo dell'account utente

Alcune Windows vengono eseguite nel contesto di sicurezza di un account amministratore e spesso richiedono diritti utente e privilegi Windows utente eccessivi. Il controllo dell'accesso alle risorse consente agli utenti di avere il controllo dei propri sistemi e di proteggerli da modifiche indesiderate. Una modifica indesiderata può essere dannosa, ad esempio un rootkit che assume il controllo del computer, o essere il risultato di un'azione eseguita da utenti con privilegi limitati. La regola più importante per controllare l'accesso alle risorse è fornire il minimo livello di accesso al contesto utente standard necessario a un utente per eseguire le attività necessarie. Le linee guida per il controllo dell'account utente forniscono a un'app le autorizzazioni necessarie quando sono necessarie per l'app, senza lasciare il sistema costantemente esposto ai rischi per la sicurezza. La maggior parte delle app non richiede privilegi di amministratore in fase di esecuzione e dovrebbe essere eseguita correttamente come utente standard.<dl> 9.1 L'app deve avere un manifesto che definisce i livelli di esecuzione e indica al sistema operativo quali privilegi l'app richiede per l'esecuzione <dl> Il contrassegno del manifesto dell'app si applica solo agli ESE, non alle DLL. Questo perché controllo dell'account utente non controlla le DLL durante la creazione del processo. È anche importante notare che le regole di Controllo dell'account utente non si applicano servizi Microsoft. Il manifesto può essere incorporato o esterno.  
Per creare un manifesto, creare un file con il nome <app>.exe.manifest e archiviarlo nella stessa directory del file \_ EXE. Si noti che qualsiasi manifesto esterno viene ignorato se l'app ha un manifesto interno. Ad esempio:  
<requestedExecutionLevel level=""asInvoker \| highestAvailable \| requireAdministrator"" uiAccess="true \| false""/>  
</dl> </dd> 9.2 Your app s main process must be run as a standard user (asInvoker). <dl> Le funzionalità amministrative devono essere spostate in un processo separato eseguito con privilegi amministrativi. Le app rivolte agli utenti, ad esempio quelle accessibili tramite il gruppo di programmi nel menu Start e che richiedono l'elevazione dei privilegi devono essere firmate con Authenticode.  
</dl> </dd> 9.3 Exceptions and Waivers <dl> È necessaria una deroga per le app che eseguono il processo principale con privilegi elevati (requireAdministrator o highestAvailable). Il processo principale viene identificato come punto di ingresso dell'utente per l'app. Le derove verranno considerate per gli scenari seguenti:

-   Strumenti amministrativi o di sistema con livello di esecuzione impostato su highestAvailable e/o requireAdministrator
-   Solo l'app del framework di accessibilità o automazione interfaccia utente imposta il flag uiAccess su true per ignorare l'isolamento dei privilegi dell'interfaccia utente. Per avviare correttamente l'utilizzo delle app, questo flag deve essere firmato con Authenticode e deve risiedere in un percorso protetto nel file system, ad esempio Programmi.


</dl> </dd> </dl>

## <a name="10-apps-must-install-to-the-correct-folders-by-default"></a>10. Le app devono essere installate nelle cartelle corrette per impostazione predefinita

Gli utenti devono avere un'esperienza coerente e sicura con il percorso di installazione predefinito dei file, mantenendo al tempo stesso la possibilità di installare un'app nel percorso preferito. È anche necessario archiviare i dati dell'app nella posizione corretta per consentire a più utenti di usare lo stesso computer senza danneggiare o sovrascrivere i dati e le impostazioni reciproci. Windows fornisce percorsi specifici nel file system per archiviare programmi e componenti software, dati delle app condivise e dati delle app specifici di un utente<dl> 10.1 L'app deve essere installata nella cartella Programmi per impostazione predefinita <dl> Per le app native a 32 bit e a 64 bit in %ProgramFiles% e %ProgramFiles(x86)% per le app a 32 bit in esecuzione su x64. I dati utente o i dati dell'app non devono mai essere archiviati in questo percorso a causa delle autorizzazioni di sicurezza configurate per questa cartella.  
</dl> </dd> 10.2 Your app must avoid starting automatically on startup <dl> Ad esempio, l'app non deve impostare uno dei valori seguenti:  
</dl>

-   Chiavi di esecuzione del Registro di sistema HKLM e, o HKCU, in Software \\ Microsoft \\ Windows \\ CurrentVersion
-   Chiavi di esecuzione del Registro di sistema HKLM e o HKCU in Software \\ Wow6432Node \\ Microsoft \\ windows \\ CurrentVersion
-   Start Menu AllPrograms > STARTUP

</dd> 10.3 Your app data, which must be shared among users on the computer, should be stored within ProgramData  
10.4 Your app s data that is exclusive to a specific user and that is not to be shared with other users of the computer, must be stored in Users\\&lt;username&gt;\\AppData  
10.5 Your app must never write directly to the "Windows" directory and or subdirectories <dl> Usare i metodi corretti per l'installazione di file, ad esempio tipi di carattere o driver.  
</dl> </dd> 10.6 Your app must write user data at first run and not during the installation in  per-machine  installations <dl> Quando l'app è installata, non esiste un percorso utente corretto in cui archiviare i dati. I tentativi da parte di un'app di modificare i comportamenti di associazione predefiniti a livello di computer dopo l'installazione avranno esito negativo. Le impostazioni predefinite devono invece essere dichiarate a livello di singolo utente, impedendo a più utenti di sovrascrivere le impostazioni predefinite degli altri utenti.  
</dl> </dd> 10.7 Exceptions and Waivers <dl> È necessaria una deroga per le app che scrivono nella Global Assembly Cache (GAC) .NET, che devono mantenere private le dipendenze degli assembly e archiviarle nella directory dell'app, a meno che la condivisione di un assembly non sia esplicitamente necessaria.  
</dl> </dd> </dl>

## <a name="11-apps-must-support-multi-user-sessions"></a>11. Le app devono supportare sessioni multi-utente

Windows utenti devono essere in grado di eseguire sessioni simultanee senza conflitti o interruzioni.<dl> 11.1 L'app deve garantire che, durante l'esecuzione in più sessioni in locale o in remoto, la normale funzionalità dell'app non sia influenzata negativamente  
11.2 Le impostazioni e i file di dati dell'app non devono essere mantenuti tra gli utenti  
11.3 La privacy e le preferenze dell'utente devono essere isolate per la sessione dell'utente  
11.4 Le istanze dell'app devono essere isolate l'una dall'altra <dl> Ciò significa che i dati utente di un'istanza non sono visibili a un'altra istanza dell'app. I suoni in una sessione utente inattiva non devono essere uditi in una sessione utente attiva. Nei casi in cui più istanze dell'app usano risorse condivise, l'app deve assicurarsi che non si sia verificata un conflitto.  
</dl> </dd> 11.5 Apps that are installed for multiple users must store data in the correct folder(s) and registry locations <dl> Fare riferimento ai requisiti di Controllo dell'account utente.  
</dl> </dd> 11.6 User apps must be able to run in multiple user sessions (Fast User Switching) for both local and remote access  
11.7 Your app must check other terminal service (TS) sessions for existing instances of the app  
</dl>
<strong>Nota:</strong> Se un'app non supporta più sessioni utente o l'accesso remoto, deve indicarlo chiaramente quando viene avviato da questo tipo di sessione.

## <a name="12-apps-must-support-x64-versions-of-windows"></a>12. Le app devono supportare le versioni x64 di Windows

Poiché l'hardware a 64 bit diventa più comune, gli utenti si aspettano che gli sviluppatori di app possano sfruttare i vantaggi dell'architettura a 64 bit eseguendo la migrazione delle app a 64 bit o che le versioni a 32 bit dell'app vengono eseguite bene nelle versioni a 64 bit di Windows.<dl> 12.1 L'app deve supportare in modo nativo le app a 64 bit o, come minimo, le app a 32 bit basate su Windows devono essere eseguite senza problemi nei sistemi a 64 bit per mantenere la compatibilità con le versioni a 64 bit di Windows  
12.2 L'app e i relativi programmi di installazione non devono contenere codice a 16 bit o basarsi su componenti a 16 bit  
12.3 La configurazione dell'app deve rilevare e installare i driver e i componenti appropriati per l'architettura a 64 bit  
12.4 Tutti i plug-in della shell devono essere eseguiti in versioni a 64 bit di Windows  
12.5 L'app in esecuzione nell'emulatore WoW64 non deve tentare di invertire o ignorare i meccanismi di virtualizzazione Wow64 <dl> Se esistono scenari specifici in cui le app devono rilevare se sono in esecuzione nell'emulatore WoW64, devono eseguire questa operazione chiamando IsWow64Process.  
</dl> </dd> </dl>

## <a name="conclusion"></a>Conclusione

Con l'evolversi di questi requisiti, si noteranno le modifiche nella cronologia delle revisioni riportata di seguito. I requisiti stabili sono fondamentali per eseguire il lavoro migliore, quindi l'obiettivo è garantire che le modifiche apportate siano sostenibile e continuare a proteggere e migliorare le app.

Grazie ancora per aver preso parte al nostro impegno a offrire esperienze di clienti eccezionali.

## <a name="revision-history"></a>Cronologia delle revisioni



| Data          | Versione | Descrizione della revisione                   | Collegamento al documento                                                                 |
|---------------|---------|----------------------------------------|----------------------------------------------------------------------------------|
| 20 dic 2011  | 1.0     | Bozza iniziale del documento per l'anteprima. |                                                                                  |
| 26 gennaio 2012  | 1.1     | Eseguire l'aggiornamento alla \# sezione 2.                 | [1.1](archive--certification-requirements-for-windows-desktop-apps-v1-1.md)     |
| 31 maggio 2012  | 1.2     | Aggiunta dei risultati del test di riepilogo             | [1.2](archive--certification-requirements-for-windows-desktop-apps-v1-2.md)     |
| 29 giugno 2012  | 3.0     | Windows 8 documento finale               | [3.0](archive--certification-requirements-for-windows-desktop-apps-v3-0.md)     |
| 18 giugno 2013  | 3.1     | Windows 8.1 documento                   | [3.1](archive--certification-requirements-for-windows-desktop-apps-v3-1.md)     |
| 20 febbraio 2014  | 3.2     | Aggiornamento interno                        |                                                                                  |
| 18 marzo 2014  | 3.3     | Windows 8.1 Update 1                   | [3.3](https://www.bing.com/search?q=3.3) |
| 29 luglio 2015 | 10      | Windows 10 Aggiornamento                      | 10                                                                               |





## <a name="learn-more-about-desktop-app-certification"></a>Altre informazioni sulla certificazione delle app desktop



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Requisito</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>Compatibilità e resilienza</td>
<td>Gli arresti & blocchi anomali sono un'interruzione importante per gli utenti e causano frustrazione. Si prevede che le app siano resilienti e stabili, eliminando tali errori si garantisce che il software sia più prevedibile, gestibile, performante e affidabile.<br/> Il punto di ingresso dell'app rivolto all'utente deve essere manifestato per motivi di compatibilità e deve dichiarare il GUID corretto. <br/> I punti di ingresso dell'app per l'utente devono essere manifestati per il riconoscimento HIGH-DPI e le API appropriate vengono chiamate per supportare HIGH-DPI.<br/> Per altre informazioni, vedere:
<ul>
<li><a href="https://support.microsoft.com/kb/197571">DLL AppInit</a></li>
<li><a href="/windows/desktop/w8cookbook/application--executable--manifest">Manifesto dell'app (eseguibile)</a></li>
<li><a href="/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows">Scrittura di applicazioni Win32 ad alta DPI</a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Attenersi alle Sicurezza di Windows consigliate</td>
<td>L Windows procedure consigliate per la sicurezza consente di evitare la creazione di esposizione Windows di attacco. Le superfici di attacco sono i punti di ingresso che un utente malintenzionato potrebbe usare per sfruttare il sistema operativo sfruttando le vulnerabilità nel software di destinazione. Una delle peggiori vulnerabilità di sicurezza è l'elevazione dei privilegi.<br/> Per altre informazioni, vedere:
<ul>
<li><a href="https://technet.microsoft.com/security/gg749821">Attack Surface Analyzer</a></li>
<li><a href="/windows/desktop/SecAuthZ/access-control-lists">Elenchi di controllo di accesso</a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Supporto Sicurezza di Windows funzionalità</td>
<td>Il Windows operativo ha implementato molte misure per supportare la sicurezza e la privacy del sistema. Le applicazioni devono supportare queste misure per mantenere l'integrità del sistema operativo. Le applicazioni compilate in modo non corretto potrebbero causare sovraccarichi del buffer che a loro volta potrebbero causare attacchi Denial of Service o causare l'esecuzione di codice dannoso. Per altre informazioni, vedere le informazioni <a href="https://blogs.microsoft.com/cybertrust/2012/08/15/microsofts-free-security-tools-binscope-binary-analyzer/">di riferimento sullo strumento BinScope.</a></td>
</tr>
<tr class="odd">
<td>Rispettare i messaggi di System Restart Manager</td>
<td>Quando gli utenti avviano l'arresto, nella maggior parte dei casi, hanno un forte desiderio di vedere l'arresto riuscito; possono avere fretta di uscire dall'ufficio e &quot; vogliono solo che i computer si &quot; spegnino. Le app devono rispettare questo desiderio non bloccando l'arresto. Anche se nella maggior parte dei casi, un arresto potrebbe non essere critico, le app devono essere preparate per la possibilità di un arresto critico.</td>
</tr>
<tr class="even">
<td>Installazione reversibile pulita</td>
<td>Un'installazione pulita e reversibile consente agli utenti di gestire correttamente (distribuire e rimuovere) le app nei propri sistemi. Per altre informazioni, <a href="/visualstudio/deployment/how-to-install-prerequisites-with-a-clickonce-application?view=vs-2015">vedere Procedura: Installare i prerequisiti con un'ClickOnce app.</a></td>
</tr>
<tr class="odd">
<td>Firmare digitalmente file e driver</td>
<td>Una firma digitale Authenticode consente agli utenti di assicurarsi che il software sia originale. Consente inoltre di rilevare se un file è stato manomesso, ad esempio se è stato infettato da un virus. L'imposizione della firma del codice in modalità kernel è una funzionalità Windows nota come integrità del codice che migliora la sicurezza del sistema operativo verificando l'integrità di un file ogni volta che l'immagine del file viene caricata in memoria. Ci consente di rilevare se codice dannoso ha modificato un file binario di sistema. Genera anche un evento di log di diagnostica e di controllo di sistema quando la firma di un modulo del kernel non viene verificata correttamente.<br/></td>
</tr>
<tr class="even">
<td>Non bloccare l'installazione o l'avvio dell'app in base al controllo della versione del sistema operativo</td>
<td>È importante che i clienti non siano artificialmente bloccati dall'installazione o dall'esecuzione dell'app quando non sono presenti limitazioni tecniche. In generale, se le app sono state scritte Windows Vista o versioni successive, non dovrebbero avere alcun motivo per controllare la versione del sistema operativo. Per altre informazioni, vedere <a href="/windows/desktop/Win7AppQual/operating-system-versioning">Controllo delle versioni del sistema operativo.</a></td>
</tr>
<tr class="odd">
<td>Non caricare servizi e driver in modalità Cassaforte predefinita</td>
<td>Cassaforte consente agli utenti di diagnosticare e risolvere i Windows. A meno che non sia necessario per operazioni di base del sistema (ad esempio, driver di dispositivo di archiviazione) o per scopi diagnostici e di ripristino (ad esempio, antivirus), i driver e i servizi non devono essere impostati per il caricamento in modalità sicura. Per impostazione predefinita, la modalità provvisoria non avvia la maggior parte dei driver e dei servizi che non sono stati preinstallati con Windows. Devono rimanere disabilitate a meno che il sistema non le richieda per operazioni di base o per scopi diagnostici e di ripristino.<br/> Per altre informazioni, vedere:
<ul>
<li><a href="/windows-hardware/drivers/kernel/determining-whether-the-operating-system-is-running-in-safe-mode">Determinare se il sistema operativo è in esecuzione in Cassaforte predefinita</a></li>
<li><a href="https://support.microsoft.com/kb/837643">Come determinare se il sistema è in esecuzione in modalità Cassaforte da un driver di dispositivo</a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Seguire le linee guida per il controllo dell'account utente</td>
<td>Alcune Windows'app vengono eseguite nel contesto di sicurezza di un account amministratore e molte richiedono diritti utente e Windows privilegi elevati. Il controllo dell'accesso alle risorse consente agli utenti di avere il controllo dei propri sistemi contro modifiche indesiderate(una modifica indesiderata può essere dannosa, ad esempio un rootkit che prende furtivamente il controllo del computer o un'azione da parte di utenti con privilegi limitati, ad esempio un dipendente che installa software proibito in un computer di lavoro). La regola più importante per controllare l'accesso alle risorse è fornire il minimo livello di accesso al contesto utente standard necessario per consentire a un utente di eseguire le attività necessarie. Le linee guida del controllo dell'account utente seguenti forniscono all'app le autorizzazioni necessarie quando necessario, senza lasciare il sistema costantemente esposto ai rischi per la sicurezza.<br/> Per altre informazioni, vedere:
<ul>
<li><a href="/windows/desktop/uxguide/winenv-uac">Controllo dell'account utente</a></li>
<li><a href="/previous-versions/aa480152(v=msdn.10)">Controllo dell'account utente: Linee guida per l'aggiornamento delle applicazioni</a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Eseguire l'installazione nelle cartelle corrette per impostazione predefinita</td>
<td>Gli utenti devono avere un'esperienza coerente e sicura con il percorso di installazione predefinito dei file, mantenendo la possibilità di installare un'app nel percorso scelto. È anche necessario archiviare i dati dell'app nella posizione corretta per consentire a più utenti di usare lo stesso computer senza danneggiare o sovrascrivere i dati e le impostazioni dell'altro. Per altre informazioni, vedere <a href="/previous-versions/ms954376(v=msdn.10)">Riepilogo dei requisiti di installazione/disinstallazione.</a></td>
</tr>
<tr class="even">
<td>Supporto di sessioni multi-utente</td>
<td>Windows utenti devono essere in grado di eseguire sessioni simultanee senza conflitti o interruzioni. Per altre informazioni, vedere Linee <a href="/windows/desktop/TermServ/terminal-services-programming-guidelines">guida Servizi Desktop remoto programmazione .</a></td>
</tr>
<tr class="odd">
<td>Supporto delle versioni x64 di Windows</td>
<td>Poiché l'hardware a 64 bit diventa sempre più diffuso, gli utenti si aspettano che gli sviluppatori di app possano sfruttare i vantaggi dell'architettura a 64 bit eseguendo la migrazione delle app a 64 bit o che le versioni a 32 bit dell'app si esercitino bene nelle versioni a 64 bit di Windows.</td>
</tr>
</tbody>
</table>





## <a name="see-also"></a>Vedi anche

-   [Windows Programma di certificazione hardware](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))
-   [Come usare il kit di certificazione Windows app](./using-the-windows-app-certification-kit.md)
