---
title: Test del Kit di certificazione app Windows
description: Di seguito sono riportati i dettagli del test per certificare le app dekstop.
ms.assetid: FA160F46-C266-4F89-B77F-166FEA9ED96B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a353eef0cd73fecac275b750345b3dd97d05dc87
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300238"
---
# <a name="windows-app-certification-kit-tests"></a>Test del Kit di certificazione app Windows

Di seguito sono riportati i dettagli del test per certificare le app dekstop. Per informazioni, vedere [uso del kit di certificazione app Windows](using-the-windows-app-certification-kit.md).

-   [Installazione reversibile pulita](#clean-reversible-install)
-   [Eseguire l'installazione nel test delle cartelle corrette](#install-to-the-correct-folders-test)
-   [Test di file con firma digitale](#digitally-signed-file-test)
-   [Supporto di Windows test x64](#support-x64-windows-test)
-   [Verifica della versione del sistema operativo](#os-version-checking-test)
-   [Test controllo dell'account utente (UAC)](#user-account-control-uac-test)
-   [Attenersi ai messaggi di gestione riavvio del sistema](#adhere-to-system-restart-manager-messages)
-   [Test in modalità provvisoria](#safe-mode-test)
-   [Test della sessione multiutente](#multiuser-session-test)
-   [Arresti anomali e blocchi test](#crashes-and-hangs-test)
-   [Test di compatibilità e resilienza](#compatibility-and-resiliency-test)
-   [Test delle procedure consigliate per la sicurezza di Windows](#windows-security-best-practices-test)
-   [Test delle funzionalità di sicurezza di Windows](#windows-security-features-test)
-   [Test DPI elevato](#high-dpi-test)

## <a name="clean-reversible-install"></a>Installazione reversibile pulita

Installa e disinstalla l'app e verifica la presenza di file e voci del registro di sistema residui.

-   Sfondo
    -   Un'installazione pulita e reversibile consente agli utenti di distribuire e rimuovere app. Per superare questo test, l'app deve eseguire le operazioni seguenti:
        -   L'app non impone il riavvio del sistema subito dopo l'installazione o la disinstallazione dell'app. *Un processo di installazione o disinstallazione di un'app non deve mai richiedere un riavvio del sistema subito dopo il completamento. Se questa operazione richiede il riavvio del sistema, gli utenti dovrebbero essere in grado di riavviare il sistema con la loro convenienza.*
        -   L'app non dipende dai nomi file brevi 8,3 (SFN). *I processi di installazione e disinstallazione dell'app devono essere in grado di usare nomi di file lunghi e percorsi di cartelle.*
        -   L'app non blocca l'installazione o la disinstallazione invisibile all'utente
        -   L'app esegue le voci necessarie nel registro di sistema. *Strumenti di inventario Windows e strumenti di telemetria richiedono informazioni complete sulle app installate. I programmi di installazione delle app devono creare le voci corrette del registro di sistema per consentire il rilevamento e la disinstallazione.*
    -   Se si usa un programma di installazione basato su MSI, MSI crea automaticamente le voci del registro di sistema seguenti. Se non si utilizza un programma di installazione MSI, durante l'installazione è necessario che il modulo di installazione crei le seguenti voci del registro di sistema:
        -   DisplayName
        -   InstallLocation
        -   Publisher
        -   UninstallString
        -   Proprietà VersionMajor o MajorVersion
        -   VersionMinor o MinorVersion
    -   L'app deve rimuovere tutte le voci in Installazione applicazioni.
-   Dettagli del test
    -   Questo test controlla i processi di installazione e disinstallazione dell'applicazione per il comportamento richiesto.
-   Azione correttiva
    -   Esaminare la progettazione e il comportamento dell'app in base ai requisiti descritti in precedenza.

## <a name="install-to-the-correct-folders-test"></a>Eseguire l'installazione nel test delle cartelle corrette

Verifica che l'app scriva i file di programma e di dati nelle cartelle corrette.

-   Sfondo
    -   Per accedere ai dati e alle impostazioni necessarie per proteggere i dati e le impostazioni dell'utente da accessi non autorizzati, è necessario che le app siano configurate correttamente per le cartelle di sistema e per utente.
-   Cartelle programmi
    -   Per impostazione predefinita, l'app deve essere installata nella cartella programmi (% ProgramFiles% per app native a 32 bit e a 64 bit e% ProgramFiles (x86)% per le app a 32 bit in esecuzione su x64).
    -   **Nota:** L'app non deve archiviare i dati utente o i dati dell'app in una cartella programmi a causa delle autorizzazioni di sicurezza configurate per questa cartella.
    -   Gli ACL nelle cartelle di sistema di Windows consentono solo agli account Administrator di leggere e scrivere su di essi. Di conseguenza, gli account utente standard non avranno accesso a queste cartelle. La virtualizzazione dei file consente tuttavia alle app di archiviare un file, ad esempio un file di configurazione, in un percorso di sistema generalmente scrivibile solo dagli amministratori. L'esecuzione di programmi come utente standard in questa situazione può causare un errore se non riesce ad accedere a un file necessario.
    -   Per assicurarsi che le app possano accedere ai propri dati, le app devono usare [cartelle note](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)) .
    -   **Nota:** Windows offre la virtualizzazione dei file per migliorare la compatibilità delle app ed eliminare i problemi quando le app vengono eseguite come utente standard in Windows. L'app non deve basarsi sulla virtualizzazione disponibile nelle versioni future di Windows.
-   Cartelle di dati delle app specifiche dell'utente
    -   Nelle installazioni "per computer", l'app non deve scrivere dati specifici dell'utente durante l'installazione. I dati di installazione specifici dell'utente devono essere scritti solo quando un utente avvia l'app per la prima volta. Questo perché non esiste una posizione utente corretta in cui archiviare i dati al momento dell'installazione. I tentativi da un'app di modificare i comportamenti di associazione predefiniti a livello di computer dopo l'installazione non saranno riusciti. Al contrario, i valori predefiniti devono essere richiesti a livello di utente, impedendo a più utenti di sovrascrivere le impostazioni predefinite.
    -   Tutti i dati dell'app esclusivi per un utente specifico e che non devono essere condivisi con altri utenti del computer devono essere archiviati in \\ <username> \\ AppData.
    -   Tutti i dati dell'app che devono essere condivisi tra gli utenti del computer devono essere archiviati in ProgramData.
-   Altre cartelle di sistema e chiavi del registro di sistema
    -   L'app non deve mai scrivere direttamente nella directory e nelle sottodirectory di Windows. Usare i metodi corretti per installare i file, ad esempio i tipi di carattere o i driver, in queste directory.
    -   Le app non devono essere avviate automaticamente all'avvio, ad esempio aggiungendo una voce a una o più di queste posizioni:
        -   Chiavi di esecuzione del registro di sistema HKLM e o HKCU in software \\ Microsoft \\ Windows \\ CurrentVersion
        -   Chiavi di esecuzione del registro di sistema HKLM e o HKCU in software \\ Wow6432Node \\ Microsoft \\ Windows \\ CurrentVersion
        -   Menu Start Tutti iprogrammi > STARTUP
-   Dettagli del test
    -   Questo test verifica che l'app usi i percorsi specifici nella file system fornita da Windows per archiviare i programmi e i componenti software, i dati delle app condivise e i dati delle app specifici di un utente.
-   Azioni correttive
    -   Esaminare il modo in cui l'app usa le cartelle del sistema e assicurarsi che le utilizzino correttamente.
-   Eccezioni e deroghe
    -   Una deroga è necessaria per le applicazioni desktop che scrivono nella Global Assembly Cache (GAC) (le app .NET devono tenere private le dipendenze di assembly e archiviarle nella directory dell'app, a meno che non sia necessario condividere un assembly in modo esplicito).
    -   L'installazione nella cartella programmi non è un requisito per i pacchetti SW desktop per ottenere il logo SW, solo nella categoria nozioni fondamentali SW.

## <a name="digitally-signed-file-test"></a>Test di file con firma digitale

Verifica i file eseguibili e i driver di dispositivo per verificare che dispongano di una firma digitale valida.

-   Sfondo
    -   I file con firma digitale consentono di verificare se il file è originale e di rilevare se il file è stato manomesso.
    -   L'imposizione della firma del codice in modalità kernel è una funzionalità di Windows nota anche come integrità del codice (CI). CI migliora la sicurezza di Windows verificando l'integrità di un file ogni volta che viene caricato in memoria. CI rileva se il codice dannoso ha modificato un file binario di sistema e genera un evento di diagnostica e di log di controllo del sistema quando la firma di un modulo kernel non riesce a verificare correttamente.
    -   Se l'app richiede autorizzazioni elevate, la richiesta di elevazione dei privilegi Visualizza informazioni contestuali sul file eseguibile che richiede l'accesso con privilegi elevati. A seconda che l'app sia firmata con Authenticode, l'utente può visualizzare la richiesta di consenso o la richiesta di credenziali.
    -   I nomi sicuri impediscono a terze parti di falsificare il codice, purché la chiave privata rimanga protetta. Il .NET Framework verifica la firma digitale durante il caricamento o l'installazione dell'assembly nella GAC. Senza l'accesso alla chiave privata, un utente malintenzionato non può modificare il codice e firmarlo di nuovo.
-   Dettagli del test
    -   Tutti i file eseguibili, ad esempio quelli con estensioni di file con estensione exe, dll, ocx, sys, cpl, DRV e SCR, devono essere firmati con un certificato Authenticode.
    -   Tutti i driver in modalità kernel installati dall'app devono avere una firma Microsoft ottenuta tramite il programma WHQL o DRS. Tutti i driver di filtro file system devono essere firmati con WHQL.
-   Azione correttiva
    -   Firmare i file eseguibili dell'applicazione.
    -   Usare makecert.exe per generare un certificato o ottenere una chiave di firma del codice da una delle autorità di certificazione (CA) commerciali, ad esempio VeriSign, Thawte o una CA Microsoft.
-   Eccezioni e deroghe
    -   Le deroghe verranno considerate solo per i ridistribuibili di terze parti non firmati. Per consentire la concessione di questa deroga, è necessaria una prova di comunicazione che richiede una versione firmata dei ridistribuibili.
    -   I pacchetti software aggiunti al valore del dispositivo sono esenti dalla certificazione dei driver in modalità kernel, perché i driver devono essere certificati da certificazione hardware di Windows.

## <a name="support-x64-windows-test"></a>Supporto di Windows test x64

Testare l'app per verificare che il file con estensione exe sia compilato per l'architettura della piattaforma in cui verrà installato.

-   Sfondo
    -   Il file eseguibile deve essere compilato per l'architettura del processore in cui è installato. Alcuni file eseguibili potrebbero essere eseguiti in un'architettura del processore diversa, ma questo non è affidabile.
    -   La compatibilità dell'architettura è importante perché i processi a 32 bit non possono caricare DLL a 64 bit e i processi a 64 bit non possono caricare DLL a 32 bit. Analogamente, le versioni a 64 bit di Windows non supportano l'esecuzione di applicazioni basate su Windows a 16 bit perché gli handle hanno 32 bit significativi in Windows a 64 bit, in modo che non possano essere passati alle applicazioni a 16 bit. Pertanto, il tentativo di avviare un'applicazione a 16 bit avrà esito negativo nelle versioni di Windows a 64 bit.
    -   i driver di dispositivo a 32 bit non possono essere eseguiti su versioni di Windows a 64 bit e pertanto devono essere trasportati nell'architettura a 64 bit.
    -   Per le applicazioni in modalità utente, Windows a 64 bit include WOW64, che consente l'esecuzione di applicazioni Windows a 32 bit nei sistemi che eseguono Windows a 64 bit, anche se con alcune perdite di prestazioni. Non esiste alcun livello di conversione equivalente per i driver di dispositivo.
    -   Per mantenere la compatibilità con le versioni di Windows a 64 bit, le app devono supportare in modo nativo a 64 bit o, almeno, le app basate su Windows a 32 bit devono essere eseguite senza problemi nei sistemi a 64 bit:
        -   Le app e i relativi programmi di installazione non devono contenere codice a 16 bit o basarsi su un componente a 16 bit.
        -   L'installazione dell'app deve rilevare e installare i driver e i componenti appropriati nelle versioni di Windows a 64 bit.
        -   Tutti i plug-in della shell devono essere eseguiti su versioni di Windows a 64 bit.
        -   Le app eseguite nell'emulatore WoW64 non devono tentare di ignorare i meccanismi di virtualizzazione WOW64. Se sono presenti scenari specifici in cui le app devono rilevare se sono in esecuzione in un emulatore WoW64, è necessario chiamare [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process).
-   Dettagli del test
    -   L'app non deve installare file binari a 16 bit. L'app non deve installare un driver in modalità kernel a 32 bit se deve essere eseguito in un computer a 64 bit.
-   Azioni correttive
    -   Compilare i file eseguibili e i driver per l'architettura del processore per cui si desidera installarli.

## <a name="os-version-checking-test"></a>Verifica della versione del sistema operativo

Verifica il modo in cui l'app controlla la versione di Windows in cui è in esecuzione.

-   Sfondo
    -   Le app controllano la versione del sistema operativo verificando la presenza di una versione maggiore o uguale alla versione richiesta per garantire la compatibilità con le versioni future di Windows.
-   Dettagli del test
    -   Simula l'esecuzione dell'app in versioni diverse di Windows per vedere come reagisce.
-   Azioni correttive
    -   Testare la versione corretta di Windows verificando se la versione corrente è maggiore o uguale alla versione necessaria per l'app, il servizio o il driver.
    -   I programmi di installazione driver e i moduli di disinstallazione non devono mai controllare la versione del sistema operativo.
-   Eccezioni e deroghe
    -   Le deroghe verranno prese in considerazione per le app che soddisfano i criteri seguenti: *(si applica solo alla certificazione dell'app desktop)*
        -   App che vengono distribuite come un unico pacchetto che viene eseguito in Windows XP, Windows Vista e Windows 7 ed è necessario controllare la versione del sistema operativo per determinare quali componenti installare in un determinato sistema operativo.
        -   App che controllano solo la versione minima del sistema operativo (solo durante l'installazione, non in fase di esecuzione) usando solo le chiamate API approvate ed elencano il requisito di versione minima nel manifesto dell'applicazione, come richiesto.
        -   App di sicurezza come app antivirus e firewall, utilità di sistema come le utilità di deframmentazione e le app di backup e gli strumenti di diagnostica che controllano la versione del sistema operativo usando solo le chiamate API approvate.

## <a name="user-account-control-uac-test"></a>Test controllo dell'account utente (UAC)

Verifica l'app per verificare che non siano necessarie autorizzazioni inutilmente elevate per l'esecuzione.

-   Sfondo
    -   Un'app che funziona o viene installata solo quando l'utente è un amministratore impone agli utenti di eseguire l'app con autorizzazioni inutilmente elevate, che possono consentire al malware di accedere al computer dell'utente.
    -   Quando gli utenti sono sempre costretti a eseguire app con token di accesso elevati, l'app può fungere da server come punto di ingresso per codice ingannevole o dannoso. Questo malware può modificare facilmente il sistema operativo, o peggio, influire sugli altri utenti. È quasi impossibile controllare un utente con accesso amministratore completo, perché gli amministratori possono installare le app ed eseguire qualsiasi app o script nel computer. I responsabili IT sono sempre alla ricerca di modi per creare "desktop standard", in cui gli utenti accedono come utenti standard. I desktop standard riducono notevolmente i costi help desk e ne riducono l'overhead.
    -   Per la maggior parte delle applicazioni non sono necessari privilegi di amministratore in fase di esecuzione. Un account utente standard dovrebbe essere in grado di eseguirli. Le app di Windows devono avere un manifesto (incorporato o esterno) per definire il livello di esecuzione che indica al sistema operativo i privilegi necessari per eseguire l'app. Il manifesto dell'app si applica solo ai file con estensione exe, non ai file con estensione dll. Il controllo dell'account utente (UAC) non controlla le dll durante la creazione del processo. Le regole UAC non si applicano ai servizi Microsoft. Il manifesto dell'applicazione può essere incorporato o esterno.
    -   Per creare un manifesto, creare un file con il nome <\_ nome app # C1.exe. manifest e archiviarlo nella stessa directory del file exe. Si noti che qualsiasi manifesto esterno viene ignorato se l'app dispone di un manifesto interno.
        -   Ad esempio, <requestedExecutionLevel Level = "" asInvoker \| highestAvailable \| requireAdministrator "" uiAccess = "" true \| false ""/>
        -   Il processo principale dell'app deve essere eseguito come utente standard (**asInvoker**). Tutte le funzionalità amministrative devono essere spostate in un processo separato eseguito con privilegi amministrativi.
        -   Le app rivolte agli utenti che richiedono privilegi elevati devono essere firmate con Authenticode.
-   Dettagli del test
    -   Tutti i exe rivolte agli utenti devono essere contrassegnati con l'attributo asInvoker. Se sono contrassegnati come highestAvailable o requireAdministrator, devono avere una firma Authenticode corretta. Qualsiasi file exe dell'app non deve avere l'attributo uiAccess impostato su true. Qualsiasi file exe che viene eseguito come servizio viene escluso da questo particolare controllo.
-   Azioni correttive
    -   Esaminare il file manifesto dell'app per le voci e i livelli di autorizzazione corretti.
-   Eccezioni e deroghe
    -   È necessaria una deroga per le app che eseguono il processo principale con privilegi elevati (**requireAdministrator** o **highestAvailable**). Il processo principale è il processo che fornisce il punto di ingresso dell'utente all'app.
    -   Le deroghe verranno prese in considerazione per gli scenari seguenti:
        -   Strumenti amministrativi o di sistema con livello di esecuzione impostato su **highestAvailable**, **requireAdministrator** o entrambi.
        -   Solo l'accessibilità o l'App Framework di automazione interfaccia utente imposta il flag uiAccess su TRUE per ignorare l'isolamento dei privilegi dell'interfaccia utente (UIPI). Per avviare correttamente l'utilizzo delle app, questo flag deve essere firmato con Authenticode e deve trovarsi in una posizione protetta nel file system, ad esempio i file di programma.

## <a name="adhere-to-system-restart-manager-messages"></a>Attenersi ai messaggi di gestione riavvio del sistema

Verifica il modo in cui l'app risponde ai messaggi di arresto e riavvio del sistema.

-   Sfondo
    -   Le app devono uscire il più rapidamente possibile quando ricevono una notifica che indica che il sistema è in fase di arresto per offrire un arresto reattivo o un'esperienza di spegnimento per l'utente.
    -   In un arresto critico, le app che restituiscono FALSE a [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) verranno inviate **WM \_ ENDSESSION** e chiuse, mentre quelle che si timeout in risposta a WM \_ QUERYENDSESSION verranno interrotte forzatamente.
-   Dettagli del test
    -   Esamina il modo in cui l'app risponde per arrestare ed uscire i messaggi.
-   Azioni correttive
    -   Se l'app non riesce a eseguire questo test, esaminare il modo in cui gestisce i messaggi di Windows:
        -   [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) con *lParam*  =  **ENDSESSION \_ CLOSEAPP**(0x1): le app desktop devono rispondere (true) immediatamente in preparazione al riavvio. Le app console possono chiamare [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) per ricevere la notifica di arresto. I servizi possono chiamare [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) per ricevere notifiche di chiusura in una routine di gestione.
        -   [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) con *lParam*  =  **ENDSESSION \_ CLOSEAPP**(0x1): le app devono restituire un valore 0 entro 30 secondi e arrestarsi. Come minimo, le app devono essere preparate salvando tutti i dati utente e dichiarare le informazioni necessarie dopo un riavvio.
    -   Le app console che ricevono la notifica degli **\_ \_ eventi di CTRL C** dovrebbero essere arrestate immediatamente. I driver non devono porre il veto a un evento di arresto del sistema.
    -   **Nota:** Le app che devono bloccare l'arresto a causa di un'operazione che non può essere interrotta devono usare [**ShutdownBlockReasonCreate**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasoncreate) per registrare una stringa che ne spiega il motivo. Al termine dell'operazione, l'app deve chiamare [**ShutdownBlockReasonDestroy**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasondestroy) per indicare che è possibile arrestare il sistema.

## <a name="safe-mode-test"></a>Test in modalità provvisoria

Verifica se il driver o il servizio è configurato per l'avvio in modalità provvisoria.

-   Sfondo
    -   La modalità provvisoria consente agli utenti di diagnosticare e risolvere i problemi di Windows. Solo i driver e i servizi necessari per il funzionamento di base del sistema operativo o forniscono servizi di diagnostica e ripristino devono essere caricati in modalità provvisoria. Il caricamento di altri file in modalità provvisoria rende più difficile la risoluzione dei problemi relativi al sistema operativo.
    -   Per impostazione predefinita, solo i driver e i servizi preinstallati con Windows vengono avviati in modalità provvisoria. Tutti gli altri driver e servizi devono essere disabilitati, a meno che il sistema non li richieda per le operazioni di base o per scopi diagnostici e di ripristino.
-   Dettagli del test
    -   I driver installati dall'app non devono essere contrassegnati per il caricamento in modalità provvisoria.
-   Azioni correttive
    -   Se il driver o il servizio non deve essere avviato in modalità provvisoria, rimuovere le voci dell'app dalle chiavi del registro di sistema.
-   Eccezioni e deroghe
    -   I driver e i servizi che devono iniziare in modalità provvisoria richiedono una deroga per la certificazione. La richiesta di deroga deve includere ogni driver e servizio da aggiungere alle chiavi del registro di sistema SafeBoot e descrivere i motivi tecnici per cui il driver o il servizio deve essere eseguito in modalità provvisoria. Il programma di installazione dell'app deve registrare tutti i driver e i servizi in queste chiavi del registro di sistema:
        -   HKLM/System/CurrentControlSet/Control/SafeBoot/minimal
        -   HKLM/System/CurrentControlSet/Control/SafeBoot/Network
-   **Nota:** È necessario testare i driver e i servizi che si desidera avviare in modalità provvisoria per assicurarsi che funzionino in modalità provvisoria senza errori.

## <a name="multiuser-session-test"></a>Test della sessione multiutente

Testare il comportamento dell'app quando viene eseguita in più sessioni nello stesso momento.

-   Sfondo
    -   Gli utenti di Windows devono essere in grado di eseguire sessioni simultanee. Le app devono assicurarsi che, quando vengono eseguite in più sessioni, in locale o in remoto, la funzionalità normale dell'app non venga influenzata negativamente. Le impostazioni e i file di dati dell'app devono essere specifici dell'utente e la privacy e le preferenze dell'utente devono essere limitate alla sessione dell'utente.
-   Dettagli del test
    -   Esegue più istanze simultanee dell'app per testare gli elementi seguenti:
        -   Più istanze di un'app in esecuzione allo stesso tempo sono isolate le une dalle altre.
    -   Ciò significa che i dati utente di un'istanza non sono visibili a un'altra istanza. Il suono in una sessione utente inattiva non dovrebbe essere sentito in una sessione utente attiva. Nei casi in cui più istanze di app usano risorse condivise, l'app deve assicurarsi che non si verifichi un conflitto.
        -   Se l'app è stata installata per più utenti, archivia i dati nelle cartelle corrette e nei percorsi del registro di sistema.
        -   L'app può essere eseguita in più sessioni utente (cambio rapido utente) sia per l'accesso locale che per quello remoto.
    -   Per garantire questo problema, l'app deve controllare altre sessioni di Servizi terminal (TS) per le istanze esistenti dell'app. Se l'app non supporta più sessioni utente o l'accesso remoto, è necessario pronunciarlo chiaramente all'utente quando viene avviato da tale sessione.
-   Azione correttiva
    -   Assicurarsi che l'app non memorizzi le impostazioni o i file di dati a livello di sistema in archivi dati specifici dell'utente, ad esempio profilo utente o HKCU. In caso contrario, tali informazioni non saranno disponibili per altri utenti.
    -   L'app deve installare i file di dati e di configurazione a livello di sistema durante l'installazione e creare i file e le impostazioni specifici dell'utente dopo l'installazione quando un utente lo esegue.
    -   Assicurarsi che l'app non blocchi più sessioni simultanee, in locale o in remoto. L'app non deve dipendere da mutex globali o da altri oggetti denominati per verificare o bloccare più sessioni simultanee.
    -   Se l'app non può consentire più sessioni simultanee per utente, usare spazi dei nomi per utente o per sessione per mutex e altri oggetti denominati.

## <a name="crashes-and-hangs-test"></a>Arresti anomali e blocchi test

Monitoraggio dell'app durante il test per la certificazione per registrare eventuali arresti anomali o blocchi.

-   Sfondo
    -   Gli errori delle app, ad esempio arresti anomali e blocchi, rappresentano un'interruzione significativa per gli utenti e provocano frustrazione. L'eliminazione di tali errori migliora la stabilità e l'affidabilità delle app e, in generale, offre agli utenti una migliore esperienza nell'app. Le app che smettono di rispondere o si arrestano in modo anomalo possono provocare perdite di dati e non offrono un'esperienza utente ottimale.
-   Dettagli del test
    -   Testiamo l'app per verificarne la resilienza e la stabilità per l'intera durata del test di certificazione.
    -   Il kit di certificazione app Windows chiama [**IApplicationActivationManager:: ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication) per avviare le app di Windows Store. Per avviare un’app mediante **ActivateApplication**, è necessario che Controllo dell’account utente sia abilitato e che la risoluzione dello schermo sia almeno 1024 x 768 o 768 x 1024. In assenza di queste due condizioni, l'app non supererà questo test.
-   Azioni correttive
    -   Assicurati che Controllo account utente sia attivato nel computer di prova.
    -   Assicurati che il test venga eseguito su un computer con uno schermo sufficientemente ampio.
    -   Se l'avvio dell'app non riesce e la piattaforma di test soddisfa i prerequisiti di [**ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication), è possibile risolvere il problema esaminando il registro eventi di attivazione. Per individuare le voci pertinenti nel registro eventi:
        1.  Aprire eventvwr.exe e passare al \\ nodo applicazione registri di Windows \\ .
        2.  Filtra la visualizzazione in modo da mostrare gli ID degli eventi: 5900-6000.
        3.  Esamina le voci del registro con l'obiettivo di trovare una spiegazione al fatto che l'app non si è avviata.
    -   Cerca il file che ha causato il problema, identifica l'errore e correggilo. Ricompila ed esegui un nuovo test dell'app.
-   Risorse aggiuntive
    -   [Uso di Application Verifier entro il ciclo di vita di sviluppo del software](https://blogs.msdn.com/b/ntdebugging/archive/2014/01/13/debugging-a-windows-8-1-store-app-crash-dump.aspx)
    -   [Application Verifier]( https://go.microsoft.com/fwlink/p/?LinkId=708300)
    -   [Utilizzo di Application Verifier](https://www.microsoft.com/?ref=go)
    -   [DLL AppInit](https://www.microsoft.com/?ref=go)
    -   [Ridurre al minimo il tempo di avvio (app di Windows Store scritte in C#/VB/C++ e XAML)](/previous-versions/windows/apps/hh994639(v=win.10))

## <a name="compatibility-and-resiliency-test"></a>Test di compatibilità e resilienza

-   Sfondo
    -   Questo controllo convaliderà due aspetti di un'app, ovvero i file eseguibili principali dell'app, ad esempio il punto di ingresso dell'app rivolti all'utente deve essere manifestato per la compatibilità, oltre a dichiarare il GUID destro. Per supportare questo nuovo test, il report avrà un sottonodo sotto la "compatibilità & resilienza". L'app avrà esito negativo se una o entrambe le condizioni risultano mancanti.
-   Dettagli test
    -   **Compatibilità:** Le app devono essere completamente funzionali senza usare le modalità di compatibilità di Windows, i messaggi AppHelp o altre correzioni per la compatibilità. Un manifesto di compatibilità consente a Windows di fornire all'app il comportamento di compatibilità corretto nelle diverse versioni del sistema operativo
    -   **AppInit:** Le app non devono elencare le dll da caricare nella \_ chiave del registro di sistema HKEY locale del software del \_ computer \\ \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows \\ AppInit \_ dll.
    -   **Switchback:** L'applicazione deve fornire il manifesto Switchback. Se il manifesto non è presente, il kit di certificazione app Windows genera un messaggio di avviso. Il kit di certificazione app Windows verificherà anche che il manifesto includa un GUID del sistema operativo valido.
-   Azioni correttive
    -   Correggere il componente dell'app che usa la correzione della compatibilità.
    -   Assicurarsi che l'app non si basi sulle correzioni di compatibilità per le funzionalità.
    -   Verificare che l'app venga manifestata e che la sezione compatibilità includa i valori appropriati
-   Informazioni aggiuntive
    -   Per altre informazioni, vedere [DLL AppInit](/previous-versions/windows/apps/hh994639(v=win.10)) .

## <a name="windows-security-best-practices-test"></a>Test delle procedure consigliate per la sicurezza di Windows

-   Sfondo
    -   Un'app non deve modificare le impostazioni di sicurezza predefinite di Windows
-   Dettagli test
    -   Verifica la sicurezza dell'app eseguendo l'analizzatore della superficie di attacco. L'approccio prevede l'aggiunta di categorie di errore in base ai singoli test. Ad esempio, alcune categorie per i test di sicurezza possono includere:
        -   Errore di inizializzazione
        -   Errore nell'architettura di sicurezza
        -   Possibile errore di overflow del buffer
        -   Errore di arresto anomalo
    -   Per informazioni dettagliate, vedere [qui](/previous-versions/windows/hh920280(v=win.10)).
-   Azioni correttive
    -   Risolvere i problemi e risolvere il problema identificato dai test. Ricompila ed esegui un nuovo test dell'app.

## <a name="windows-security-features-test"></a>Test delle funzionalità di sicurezza di Windows

-   Sfondo
    -   Le applicazioni devono acconsentire esplicitamente alle funzionalità di sicurezza di Windows. La modifica delle protezioni di sicurezza di Windows predefinite può comportare maggiori rischi per gli utenti.
-   Dettagli del test
    -   Testa la sicurezza dell’app tramite l’esecuzione dello strumento BinScope Binary Analyzer. Per informazioni dettagliate, vedere [qui](/previous-versions/windows/hh920280(v=win.10)).
-   Azioni correttive
    -   Risolvere i problemi e risolvere il problema identificato dai test. Ricompila ed esegui un nuovo test dell'app.

## <a name="high-dpi-test"></a>Test DPI elevato

È consigliabile che le app Win32 siano compatibili con DPI. Si tratta della chiave per far apparire l'interfaccia utente dell'app in modo coerente in un'ampia gamma di impostazioni di visualizzazione a DPI elevato. Un'app che non è compatibile con DPI in esecuzione in un'impostazione di visualizzazione a DPI elevata può presentare problemi come il ridimensionamento errato di elementi dell'interfaccia utente, testo ritagliato e immagini sfocate. Esistono due modi per dichiarare che un'app è compatibile con DPI. Uno consiste nel dichiarare DPI.

-   Sfondo
    -   Questo controllo convaliderà due aspetti di un'app, ovvero i file eseguibili principali, ad esempio i punti di ingresso dell'app rivolti agli utenti devono essere manifesti per la compatibilità con DPI elevata e che le API appropriate vengano chiamate per supportare i valori DPI alti. L'app avrà esito negativo se una o entrambe le condizioni risultano mancanti. Questo controllo introdurrà una nuova sezione del report sul desktop. vedere l'esempio seguente.
-   Dettagli test
    -   Il test genera un avviso quando viene rilevato uno dei seguenti elementi:
        -   Il file EXE principale non dichiara la consapevolezza DPI nel manifesto e non chiama l'API SetProcessDPIAware. Se si dimentica di aggiungere il manifesto di sensibilizzazione DPI, avvisare lo sviluppatore.
        -   Il file EXE principale non dichiara la consapevolezza DPI nel manifesto, ma chiama l'API SetProcessDPIAware (avvisa lo sviluppatore che deve usare il manifesto per dichiarare la consapevolezza DPI anziché chiamare l'API).
        -   Il mainEXE dichiara la consapevolezza DPI nel manifesto, ma chiama anche l'API SetProcessDPIAware (avvisa lo sviluppatore che chiama l'API non è necessario).
        -   Per i file binari che non sono exe principali, se chiamano l'API, fornire un avviso (la chiamata all'API non è consigliata).
-   Azioni correttive
    -   L'uso della funzione SetProcessDPIAware () è sconsigliato. Se una DLL memorizza nella cache le impostazioni DPI durante la relativa inizializzazione, la chiamata di SetProcessDPIAware () nell'app può generare un race condition. Non è consigliabile chiamare la funzione SetProcessDPIAware () in una DLL.
-   Informazioni aggiuntive
    -   [Scrittura di app ad alta risoluzione](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))

 

 