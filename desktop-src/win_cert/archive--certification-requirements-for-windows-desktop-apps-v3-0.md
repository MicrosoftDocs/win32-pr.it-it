---
title: Archiviare i requisiti di certificazione Windows Desktop Apps v3.0
description: Versione del documento 3.0Document date 29 giugno 2012In questo documento sono contenuti i requisiti tecnici e le qualifica di idoneità che un'app desktop deve soddisfare per partecipare al programma di certificazione app desktop Windows 8.
ms.assetid: 7107EF93-8401-481A-B433-8C36A539D790
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13af9f9cb0464ff7f0f9c57f057685b360d09928
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886273"
---
# <a name="archive-certification-requirements-for-windows-desktop-apps-v30"></a>Archivio: Requisiti di certificazione per Windows Desktop Apps v3.0

**Versione del documento:** 3.0

**Data del documento:** 29 giugno 2012

Questo documento contiene i requisiti tecnici e le qualifica di idoneità che un'app desktop deve soddisfare per partecipare al programma di certificazione app desktop Windows 8 desktop. Per Windows 7, questo programma era noto come programma Windows Software Logo Program.

## <a name="welcome"></a>Benvenuto!

La Windows supporta un ampio ecosistema di prodotti e partner. La visualizzazione del Windows logo sul prodotto rappresenta una relazione e un impegno condiviso per la qualità tra Microsoft e l'azienda. I clienti si affidano Windows marchio del prodotto perché assicurano che soddisfino gli standard di compatibilità e funzionino bene Windows piattaforma. Il passaggio Windows certificazione dell'app consente di presentare l'app nel Centro compatibilità Windows ed è anche un passaggio necessario per elencare un riferimento all'app desktop in Windows Store.

Il Windows App Certification Program è costituito da requisiti tecnici e di programma per garantire che le app di terze parti con il marchio Windows siano facili da installare e affidabili nei PC che eseguono Windows. I clienti sono molto interessati a stabilità, compatibilità, affidabilità, prestazioni e qualità nei sistemi acquistati. Microsoft si concentra sugli investimenti per soddisfare questi requisiti per le app software progettate per l'Windows per i PC. Queste attività includono test di compatibilità per la coerenza dell'esperienza, prestazioni migliorate e sicurezza avanzata nei PC che eseguono Windows software. I test di compatibilità Microsoft sono stati progettati in collaborazione con i partner del settore e sono continuamente migliorati in risposta agli sviluppi del settore e alla domanda dei consumatori.

Il Windows App Certification Kit viene usato per convalidare la conformità a questi requisiti e sostituisce il WSLK usato per la convalida nel programma Windows 7 Software Logo. Il Windows App Certification Kit è uno dei componenti inclusi in Windows Software Development Kit (SDK) per Windows 8. È anche integrato in Microsoft Visual Studio 2012 Express per Windows 8.

## <a name="app-eligibility"></a>Idoneità dell'app

Perché un'app sia idonea Windows 8 la certificazione dell'app desktop, deve soddisfare i criteri seguenti e tutti i requisiti tecnici elencati in questo documento.

-   Deve essere un'app autonoma
-   Deve essere eseguito in un computer Windows 8.1 locale
-   Può essere un componente client di un'app Windows Server certificata
-   Deve essere codice e funzionalità completa

## <a name="1-apps-are-compatible-and-resilient"></a>1. Le app sono compatibili e resilienti

Le volte in cui un'app si arresta in modo anomalo o smette di rispondere causa molte frustrazioni da parte dell'utente. Si prevede che le app siano resilienti e stabili e l'eliminazione di tali errori consente di garantire che il software sia più prevedibile, gestibile, performante e affidabile.<dl> 1.1 L'app non deve assumere una dipendenza dalle Windows di compatibilità, dal messaggio AppHelp e da qualsiasi altra correzione di compatibilità  
1.2 L'app non deve assumere una dipendenza dal runtime VB6  
1.3 L'app non deve caricare DLL arbitrarie per intercettare le chiamate API Win32 usando HKLM \\ Software \\ Microsoft Windows NT \\ \\ CurrentVersion Windows Dll \\ \_ AppInit.  
</dl>

## <a name="2-apps-must-adhere-to-windows-security-best-practices"></a>2. Le app devono rispettare Windows procedure consigliate per la sicurezza

L Windows procedure consigliate per la sicurezza consente di evitare la creazione di esposizione Windows di attacco. Le superfici di attacco sono i punti di ingresso che un utente malintenzionato potrebbe usare per sfruttare il sistema operativo sfruttando le vulnerabilità nel software di destinazione. Una delle peggiori vulnerabilità di sicurezza è l'elevazione dei privilegi.

<dl> 2.1 L'app deve usare ACL sicuri <a href="/windows/desktop/SecAuthZ/access-control-lists">e</a> appropriati per proteggere i file eseguibili  
2.2 L'app deve usare elenchi di controllo di accesso sicuri e <a href="/windows/desktop/SecAuthZ/access-control-lists">appropriati</a> per proteggere le directory  
2.3 L'app deve usare elenchi di controllo di accesso sicuri <a href="/windows/desktop/SecAuthZ/access-control-lists">e</a> appropriati per proteggere le chiavi del Registro di sistema  
2.4 L'app deve <a href="/windows/desktop/SecAuthZ/access-control-lists"></a> usare elenchi di controllo di accesso sicuri e appropriati per proteggere le directory che contengono oggetti  
2.5 L'app deve ridurre l'accesso non amministratore ai servizi vulnerabili a manomissioni  
2.6 L'app deve impedire il riavvio dei servizi con riavvii rapidi più di due volte ogni 24 ore
</dl>**Nota: l'accesso deve essere concesso solo alle entità che lo richiedono.**

Il programma di certificazione app Windows verificherà che le superfici di attacco di Windows non siano esposte verificando che gli ACL e i servizi siano implementati in modo da non mettere a rischio il sistema Windows.

## <a name="3-apps-support-windows-security-features"></a>3. Le app supportano Windows di sicurezza

Il Windows operativo ha molte funzionalità che supportano la sicurezza e la privacy del sistema. Le app devono supportare queste funzionalità per mantenere l'integrità del sistema operativo. Le app compilate in modo non corretto possono causare sovraccarichi del buffer che possono, a sua volta, causare attacchi Denial of Service o consentire l'esecuzione di codice dannoso. <dl> 3.1 L'app non deve usare AllowPartiallyTrustedCallersAttribute (APTCA) per garantire l'accesso sicuro agli assembly con nome sicuro  
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
</dl>**Note: Apps that must block shutdown because of an operation that cannot be interrupted should explain the reason to the user.** Use ShutdownBlockReasonCreate to register a string that explains the reason to the user. When the operation has completed, the app should call ShutdownBlockReasonDestroy to indicate that the system can be shut down.

## <a name="5-apps-must-support-a-clean-reversible-installation"></a>5. Le app devono supportare un'installazione pulita e reversibile

Un'installazione pulita e reversibile consente agli utenti di gestire correttamente (distribuire e rimuovere) le app nei propri sistemi.<dl> 5.1 L'app deve implementare correttamente un'installazione pulita e reversibile <dl> Se l'installazione non riesce, l'app dovrebbe essere in grado di eseguire il rollback e ripristinare lo stato precedente del computer.  
</dl> </dd> 5.2 Your app must never force the user to restart the computer immediately <dl> Il riavvio del computer non dovrebbe mai essere l'unica opzione alla fine di un'installazione o di un aggiornamento. Gli utenti dovrebbero avere la possibilità di riavviare in un secondo momento.  
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

</dd> </dl>

## <a name="6-apps-must-digitally-sign-files-and-drivers"></a>6. Le app devono firmare digitalmente file e driver

Una firma digitale Authenticode consente agli utenti di assicurarsi che il software sia originale. Consente inoltre di rilevare se un file è stato manomesso, ad esempio se è stato infettato da un virus. L'imposizione della firma del codice in modalità kernel è una funzionalità Windows nota come integrità del codice che migliora la sicurezza del sistema operativo verificando l'integrità di un file ogni volta che l'immagine del file viene caricata in memoria. Ci consente di rilevare se codice dannoso ha modificato un file binario di sistema. Genera anche un evento di log di diagnostica e di controllo di sistema quando la firma di un modulo del kernel non viene verificata correttamente. <dl> 6.1 Tutti i file eseguibili (.exe, .dll, ocx, .sys, .cpl, drv, scr) devono essere firmati con un certificato Authenticode  
6.2 Tutti i driver in modalità kernel installati dall'app devono avere una firma Microsoft ottenuta tramite il Windows di certificazione hardware. Tutti i driver di filtro del file system devono essere firmati da Microsoft.  
6.3 Eccezioni e derozioni <dl> Le derozioni verranno considerate solo per i ridistribuibili di terze parti non firmati, esclusi i driver. Per la concessione di questa deroga è necessaria una prova di comunicazione che richiede una versione firmata dei ridistribuibili.  
</dl> </dd> </dl>

## <a name="7-apps-don-t-block-installation-or-app-launch-based-on-an-operating-system-version-check"></a>7. Le app non bloccano l'installazione o l'avvio dell'app in base a un controllo della versione del sistema operativo

È importante che i clienti non siano artificialmente bloccati dall'installazione o dall'esecuzione dell'app quando non sono presenti limitazioni tecniche. In generale, se le app sono state scritte per Windows Vista o versioni successive di Windows, non devono controllare la versione del sistema operativo.<dl> 7.1 L'app non deve eseguire controlli di versione per verificare l'uguaglianza <dl> Se è necessaria una funzionalità specifica, verificare se la funzionalità stessa è disponibile. Se è necessario Windows XP, verificare Windows XP o versione successiva (>= 5.1). In questo modo, il codice di rilevamento continuerà a funzionare nelle versioni future di Windows. I programmi di installazione dei driver e i moduli di disinstallazione non devono mai controllare la versione del sistema operativo.  
</dl> </dd> 7.2 Exceptions and Waivers will be considered for apps meeting the criteria below:

-   App recapitate come un unico pacchetto eseguito anche in Windows XP, Windows Vista e Windows 7 ed è necessario controllare la versione del sistema operativo per determinare quali componenti installare in un determinato sistema operativo.
-   App che controllano solo la versione minima del sistema operativo (solo durante l'installazione, non in fase di esecuzione) usando solo le chiamate API approvate e che elencano correttamente il requisito di versione minima nel manifesto dell'app.
-   App di sicurezza (antivirus, firewall e così via), utilità di sistema (ad esempio deframmentazione, backup e strumenti di diagnostica) che controllano la versione del sistema operativo usando solo le chiamate API approvate.

  
</dl>

## <a name="8-apps-don-t-load-services-or-drivers-in-safe-mode"></a>8. Le app non caricano servizi o driver in modalità sicura

Cassaforte consente agli utenti di diagnosticare e risolvere i Windows. I driver e i servizi non devono essere impostati per il caricamento in modalità sicura, a meno che non siano necessari per operazioni di sistema di base di , ad esempio driver di dispositivo di archiviazione o per scopi diagnostici e di ripristino, ad esempio gli scanner antivirus. Per impostazione predefinita, quando Windows è in modalità provvisoria, vengono avviati solo i driver e i servizi preinstallati con Windows.

-   8.1 Eccezioni ed esenzioni <dl> I driver e i servizi che devono essere avviati in modalità sicura richiedono una deroga. La richiesta di deroga deve includere ogni driver o servizio applicabile che scrive nelle chiavi del Registro di sistema SafeBoot e descrivere i motivi tecnici per cui l'app o il servizio deve essere eseguito in modalità sicura. Il programma di installazione dell'app deve registrare tutti questi driver e servizi usando queste chiavi del Registro di sistema:  
    </dl>
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Minimal
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Network

**Nota:** È necessario testare questi driver e servizi per assicurarsi che funzionino in modalità sicura senza errori.

## <a name="9-apps-must-follow-user-account-control-guidelines"></a>9. Le app devono seguire le linee guida di Controllo dell'account utente

Alcune Windows vengono eseguite nel contesto di sicurezza di un account amministratore e spesso richiedono diritti utente e privilegi Windows utente eccessivi. Il controllo dell'accesso alle risorse consente agli utenti di avere il controllo dei propri sistemi e di proteggerli da modifiche indesiderate. Una modifica indesiderata può essere dannosa, ad esempio un rootkit che assume il controllo del computer, o essere il risultato di un'azione eseguita da utenti con privilegi limitati. La regola più importante per controllare l'accesso alle risorse è fornire il minimo livello di accesso al contesto utente standard necessario a un utente per eseguire le attività necessarie. Le linee guida del controllo dell'account utente forniscono all'app le autorizzazioni necessarie quando sono necessarie per l'app, senza lasciare il sistema costantemente esposto ai rischi per la sicurezza. La maggior parte delle app non richiede privilegi di amministratore in fase di esecuzione e dovrebbe essere eseguita correttamente come utente standard.<dl> 9.1 L'app deve avere un manifesto che definisce i livelli di esecuzione e indica al sistema operativo quali privilegi l'app richiede per l'esecuzione <dl> Il contrassegno del manifesto dell'app si applica solo agli ESE, non alle DLL. Questo perché controllo dell'account utente non controlla le DLL durante la creazione del processo. È anche importante notare che le regole di Controllo dell'account utente non si applicano servizi Microsoft. Il manifesto può essere incorporato o esterno.  
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
</dl>**Note:** If an app does not support multiple user sessions or remote access, it must clearly state this when launched from this kind of session.

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



| Data         | Versione | Descrizione della revisione                   | Collegamento al documento                                                             |
|--------------|---------|----------------------------------------|------------------------------------------------------------------------------|
| 20 dic 2011 | 1.0     | Bozza iniziale del documento per l'anteprima. |                                                                              |
| 26 gennaio 2012 | 1.1     | Eseguire l'aggiornamento alla \# sezione 2.                 | [1.1](archive--certification-requirements-for-windows-desktop-apps-v1-1.md) |
| 31 maggio 2012 | 1.2     | Aggiunta dei risultati del test di riepilogo             | [1.2](archive--certification-requirements-for-windows-desktop-apps-v1-2.md) |
| 29 giugno 2012 | 3.0     | Windows 8 documento finale               | 3.0                                                                          |



 

## <a name="learn-more-about-desktop-app-certification"></a>Altre informazioni sulla certificazione delle app desktop



| Requisito                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Altre informazioni                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Compatibilità e resilienza                                                    | Gli arresti & blocchi sono un'interruzione importante per gli utenti e causano frustrazione. Si prevede che le app siano resilienti e stabili, eliminando tali errori si garantisce che il software sia più prevedibile, gestibile, affidabile e affidabile.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [Windows Vista, Windows 7 e Windows 8 operativi](/previous-versions/windows/it-pro/windows-7/cc722305(v=ws.10))<br/> [Application Verifier](/previous-versions/aa480483(v=msdn.10))<br/> [DLL AppInit](https://support.microsoft.com/kb/197571)<br/> |
| Conformità alle Sicurezza di Windows consigliate                                       | L Windows procedure consigliate per la sicurezza consente di evitare di creare esposizione Windows di attacco. Le superfici di attacco sono i punti di ingresso che un utente malintenzionato potrebbe usare per sfruttare il sistema operativo sfruttando le vulnerabilità nel software di destinazione. Una delle peggiori vulnerabilità della sicurezza è l'elevazione dei privilegi.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | [Attack Surface Analyzer](https://technet.microsoft.com/security/gg749821)<br/> [Elenchi di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists)<br/>                                                                                                                                |
| Supporto Sicurezza di Windows funzionalità                                               | Il Windows operativo ha implementato molte misure per supportare la sicurezza e la privacy del sistema. Le applicazioni devono supportare queste misure per mantenere l'integrità del sistema operativo. Le applicazioni compilate in modo non corretto potrebbero causare sovraccarichi del buffer che a loro volta potrebbero causare attacchi Denial of Service o causare l'esecuzione di codice dannoso.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [Informazioni di riferimento per lo strumento BinScope](https://blogs.microsoft.com/cybertrust/2012/08/15/microsofts-free-security-tools-binscope-binary-analyzer/)<br/>                                                                                                                                             |
| Rispettare i messaggi di System Restart Manager                                       | Quando gli utenti avviano l'arresto, nella maggior parte dei casi desiderano che l'arresto abbia esito positivo. Potrebbero essere in diffibrio di uscire dall'ufficio e "semplicemente volere" che i computer si spegnino. Le app devono rispettare questo volere non bloccando l'arresto. Anche se nella maggior parte dei casi un arresto potrebbe non essere critico, le app devono essere preparate per la possibilità di un arresto critico.                                                                                                                                                                                                                                                                                                                                                                                                                                       | [Modifiche all'arresto dell'applicazione in Windows Vista](/previous-versions/windows/desktop/ms700677(v=vs.85))<br/> [Sviluppo di Gestione riavvio](/previous-versions/bb756958(v=msdn.10))<br/>                                                                              |
| Installazione reversibile pulita                                                   | Un'installazione pulita e reversibile consente agli utenti di gestire (distribuire e rimuovere) correttamente le app nei propri sistemi.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [Procedura: Installare i prerequisiti con un'ClickOnce applicazione](/visualstudio/deployment/how-to-install-prerequisites-with-a-clickonce-application?view=vs-2015)<br/> [Installazione di applicazioni in sistemi a 64 bit](/windows/desktop/WinProg64/application-installation)<br/>                                                |
| Firmare digitalmente file e driver                                                | Una firma digitale Authenticode consente agli utenti di assicurarsi che il software sia originale. Consente inoltre di rilevare se un file è stato manomesso, ad esempio se è stato infettato da un virus. L'imposizione della firma del codice in modalità kernel è una funzionalità di Windows nota come integrità del codice, che migliora la sicurezza del sistema operativo verificando l'integrità di un file ogni volta che l'immagine del file viene caricata in memoria. Ci rileva se il codice dannoso ha modificato un file binario di sistema. Genera anche un evento del log di diagnostica e di controllo del sistema quando la firma di un modulo del kernel non viene verificata correttamente.                                                                                                                                                                            | [Firme digitali per i moduli kernel in Windows](/previous-versions/windows/hardware/design/dn653559(v=vs.85))<br/>                                                                                                                                             |
| Non bloccare l'installazione o l'avvio dell'app in base al controllo della versione del sistema operativo | È importante che i clienti non siano artificialmente bloccati dall'installazione o dall'esecuzione dell'app quando non sono presenti limitazioni tecniche. In generale, se le app sono state scritte per Windows Vista o versioni successive, non dovrebbero avere alcun motivo per controllare la versione del sistema operativo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | [Controllo delle versioni del sistema operativo](../win7appqual/operating-system-versioning.md)<br/>                                                                                                                                                                                           |
| Non caricare servizi e driver in modalità Cassaforte sicurezza                                   | Cassaforte consente agli utenti di diagnosticare e risolvere i Windows. A meno che non sia necessario per operazioni di base del sistema (ad esempio, driver di dispositivo di archiviazione) o per scopi diagnostici e di ripristino (ad esempio, scanner antivirus), i driver e i servizi non devono essere impostati per il caricamento in modalità sicura. Per impostazione predefinita, la modalità sicura non avvia la maggior parte dei driver e dei servizi che non sono stati preinstallati con Windows. Devono rimanere disabilitati a meno che il sistema non li richieda per operazioni di base o per scopi diagnostici e di ripristino.                                                                                                                                                                                                                                                                                         | [Determinazione dell'esecuzione del sistema operativo in Cassaforte predefinita](/windows-hardware/drivers/kernel/determining-whether-the-operating-system-is-running-in-safe-mode)<br/> [Come determinare se il sistema è in esecuzione in modalità Cassaforte da un driver di dispositivo](https://support.microsoft.com/kb/837643)<br/>       |
| Seguire le linee guida di Controllo dell'account utente                                    | Alcune Windows'app vengono eseguite nel contesto di sicurezza di un account amministratore e molte richiedono diritti utente e privilegi Windows privilegi eccessivi. Il controllo dell'accesso alle risorse consente agli utenti di avere il controllo dei propri sistemi contro modifiche indesiderate (una modifica indesiderata può essere dannosa, ad esempio un rootkit che assume il controllo del computer o un'azione da parte di utenti con privilegi limitati, ad esempio un dipendente che installa software vietato in un computer di lavoro). La regola più importante per controllare l'accesso alle risorse è fornire il minimo livello di accesso al contesto utente standard necessario a un utente per eseguire le attività necessarie. Le linee guida di Controllo dell'account utente seguenti forniscono all'app le autorizzazioni necessarie quando necessario, senza lasciare il sistema costantemente esposto ai rischi per la sicurezza. | [Controllo dell'account utente](/windows/desktop/uxguide/winenv-uac)<br/> [Controllo dell'account utente: Linee guida per l'aggiornamento delle applicazioni](/previous-versions/aa480152(v=msdn.10))<br/>                                                                       |
| Installa nelle cartelle corrette per impostazione predefinita                                       | Gli utenti devono avere un'esperienza coerente e sicura con il percorso di installazione predefinito dei file, mantenendo al tempo stesso la possibilità di installare un'app nel percorso scelto. È anche necessario archiviare i dati dell'app nella posizione corretta per consentire a più utenti di usare lo stesso computer senza danneggiare o sovrascrivere i dati e le impostazioni reciproci.                                                                                                                                                                                                                                                                                                                                                                                                                                                          | [Riepilogo dei requisiti di installazione/disinstallazione](/previous-versions/ms954376(v=msdn.10))<br/>                                                                                                                                                                                    |
| Supporto di sessioni multi-utente                                                     | Windows utenti devono essere in grado di eseguire sessioni simultanee senza conflitti o interruzioni.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | [Servizi Desktop remoto di programmazione](/windows/desktop/TermServ/terminal-services-programming-guidelines)<br/>                                                                                                                                                                      |
| Supporto delle versioni x64 di Windows                                                 | Poiché l'hardware a 64 bit diventa sempre più prevalente, gli utenti si aspettano che gli sviluppatori di app possano sfruttare i vantaggi dell'architettura a 64 bit eseguendo la migrazione delle app a 64 bit o che le versioni a 32 bit dell'app vengono eseguite bene nelle versioni a 64 bit di Windows.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [Compatibilità delle applicazioni: Windows Vista a 64 bit](/previous-versions/bb756962(v=msdn.10))<br/>                                                                                                                                                                              |



 

## <a name="see-also"></a>Vedi anche

-   [Windows Programma di certificazione hardware](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))

 

