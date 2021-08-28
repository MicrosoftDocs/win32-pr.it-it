---
title: Test del Kit di certificazione app Windows
description: Di seguito sono riportati i dettagli del test per la certificazione delle app dekstop.
ms.assetid: FA160F46-C266-4F89-B77F-166FEA9ED96B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1ec63fee4a9410b261ed29dc44cf8934906984
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885973"
---
# <a name="windows-app-certification-kit-tests"></a>Test del Kit di certificazione app Windows

Di seguito sono riportati i dettagli del test per la certificazione delle app dekstop. Per informazioni, vedere Using the Windows App Certification Kit (Uso [del kit Windows app).](using-the-windows-app-certification-kit.md)

-   [Installazione reversibile pulita](#clean-reversible-install)
-   [Test dell'installazione nelle cartelle corrette](#install-to-the-correct-folders-test)
-   [Test di file con firma digitale](#digitally-signed-file-test)
-   [Supporto del test Windows x64](#support-x64-windows-test)
-   [Test di controllo della versione del sistema operativo](#os-version-checking-test)
-   [Test del controllo dell'account utente](#user-account-control-uac-test)
-   [Rispettare i messaggi di System Restart Manager](#adhere-to-system-restart-manager-messages)
-   [Cassaforte test della modalità](#safe-mode-test)
-   [Test di sessione multiutente](#multiuser-session-test)
-   [Test si arresta in modo anomalo e si blocca](#crashes-and-hangs-test)
-   [Test di compatibilità e resilienza](#compatibility-and-resiliency-test)
-   [Sicurezza di Windows test delle procedure consigliate](#windows-security-best-practices-test)
-   [Test delle funzionalità di sicurezza di Windows](#windows-security-features-test)
-   [Test con valori DPI alti](#high-dpi-test)

## <a name="clean-reversible-install"></a>Installazione reversibile pulita

Installa e disinstalla l'app e verifica la presenza di file residui e voci del Registro di sistema.

-   Sfondo
    -   Un'installazione pulita e reversibile consente agli utenti di distribuire e rimuovere le app. Per superare questo test, l'app deve eseguire le operazioni seguenti:
        -   L'app non forza il riavvio del sistema immediatamente dopo l'installazione o la disinstallazione dell'app. *Il processo di installazione o disinstallazione di un'app non deve mai richiedere un riavvio del sistema subito dopo il completamento. Se ciò richiede il riavvio del sistema, gli utenti devono essere in grado di riavviare il sistema per comodità.*
        -   L'app non dipende dai nomi di file brevi (SFN) 8.3. *I processi di installazione e disinstallazione dell'app devono essere in grado di usare nomi di file lunghi e percorsi di cartella.*
        -   L'app non blocca l'installazione/disinstallazione invisibile all'utente
        -   L'app crea le voci necessarie nel Registro di sistema. *Windows strumenti di inventario e di telemetria richiedono informazioni complete sulle app installate. I programmi di installazione delle app devono creare le voci del Registro di sistema corrette per consentire il rilevamento e la disinstallazione.*
    -   Se si usa un programma di installazione basato su MSI, MSI crea automaticamente le voci del Registro di sistema riportate di seguito. Se non si usa un programma di installazione MSI, il modulo di installazione deve creare le voci del Registro di sistema seguenti durante l'installazione:
        -   DisplayName
        -   InstallLocation
        -   Publisher
        -   UninstallString
        -   VersionMajor o MajorVersion
        -   VersionMinor o MinorVersion
    -   L'app deve rimuovere tutte le relative voci in Installazione applicazioni.
-   Dettagli del test
    -   Questo test controlla il comportamento richiesto nei processi di installazione e disinstallazione dell'app.
-   Azione correttiva
    -   Esaminare la progettazione e il comportamento dell'app in base ai requisiti descritti in precedenza.

## <a name="install-to-the-correct-folders-test"></a>Test dell'installazione nelle cartelle corrette

Verifica che l'app scrive il programma e i file di dati nelle cartelle corrette.

-   Sfondo
    -   Le app devono essere cartelle di sistema e per utente in modo corretto in modo da poter accedere ai dati e alle impostazioni necessarie proteggendo al tempo stesso i dati e le impostazioni dell'utente da accessi non autorizzati.
-   Cartelle Programmi
    -   L'app deve essere installata nella cartella Programmi per impostazione predefinita (%ProgramFiles% per le app native a 32 bit e a 64 bit e %ProgramFiles(x86)% per le app a 32 bit in esecuzione su x64.
    -   **Nota:** L'app non deve archiviare i dati utente o i dati dell'app in una cartella Programmi a causa delle autorizzazioni di sicurezza configurate per questa cartella.
    -   Gli ACL nelle Windows di sistema consentono solo agli account amministratore di leggere e scrivere in essi. Di conseguenza, gli account utente standard non avranno accesso a queste cartelle. La virtualizzazione dei file, tuttavia, consente alle app di archiviare un file, ad esempio un file di configurazione, in un percorso di sistema generalmente scrivibile solo dagli amministratori. L'esecuzione di programmi come utente standard in questa situazione può causare un errore se non è in grado di accedere a un file necessario.
    -   Le app devono [usare Cartelle](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)) note per assicurarsi che possano accedere ai dati.
    -   **Nota: Windows** la virtualizzazione dei file per migliorare la compatibilità delle app ed eliminare i problemi quando le app vengono eseguite come utente standard in Windows. L'app non deve basarsi sulla virtualizzazione presente nelle versioni future di Windows.
-   Cartelle di dati delle app specifiche dell'utente
    -   Nelle installazioni "per computer", l'app non deve scrivere dati specifici dell'utente durante l'installazione. I dati di installazione specifici dell'utente devono essere scritti solo quando un utente avvia l'app per la prima volta. Ciò è dovuto al fatto che non esiste un percorso utente corretto in cui archiviare i dati al momento dell'installazione. I tentativi da parte di un'app di modificare i comportamenti di associazione predefiniti a livello di computer dopo l'installazione avranno esito negativo. Le impostazioni predefinite devono invece essere dichiarate a livello di singolo utente, impedendo a più utenti di sovrascrivere le impostazioni predefinite degli altri utenti.
    -   Tutti i dati dell'app esclusivi di un utente specifico e non devono essere condivisi con altri utenti del computer devono essere archiviati nel nome \\ &lt; utente Utente &gt; \\ AppData.
    -   Tutti i dati dell'app che devono essere condivisi tra gli utenti nel computer devono essere archiviati in ProgramData.
-   Altre cartelle di sistema e chiavi del Registro di sistema
    -   L'app non deve mai scrivere direttamente nella directory Windows directory e o nelle sottodirectory. Usare i metodi corretti per l'installazione di file, ad esempio tipi di carattere o driver, in queste directory.
    -   Le app non devono essere avviate automaticamente all'avvio, ad esempio aggiungendo una voce a uno o più di questi percorsi:
        -   Chiavi di esecuzione del Registro di sistema HKLM e, o HKCU, in Software \\ Microsoft \\ Windows \\ CurrentVersion
        -   Chiavi di esecuzione del Registro di sistema HKLM e o HKCU in Software \\ Wow6432Node \\ Microsoft \\ windows \\ CurrentVersion
        -   Start Menu AllPrograms > STARTUP
-   Dettagli del test
    -   Questo test verifica che l'app usi percorsi specifici nel file system fornito da Windows per archiviare programmi e componenti software, dati delle app condivise e dati dell'app specifici di un utente.
-   Azioni correttive
    -   Esaminare il modo in cui l'app usa le cartelle del sistema e assicurarsi che le usi correttamente.
-   Eccezioni ed esenzioni
    -   È necessaria una deroga per le app desktop che scrivono nella Global Assembly Cache (GAC). Le app .NET devono mantenere private le dipendenze degli assembly e archiviarle nella directory dell'app, a meno che non sia esplicitamente necessaria la condivisione di un assembly.
    -   L'installazione nella cartella Programmi Non è un requisito per i pacchetti SW desktop per ottenere il logo SW, solo nella categoria CONCETTI FONDAMENTALI SW.

## <a name="digitally-signed-file-test"></a>Test di file con firma digitale

Verifica i file eseguibili e i driver di dispositivo per verificare che abbia una firma digitale valida.

-   Sfondo
    -   I file con firma digitale rendono possibile verificare che il file sia originale e rilevare se il file è stato manomesso.
    -   L'imposizione della firma del codice in modalità kernel è Windows funzionalità di sicurezza avanzata nota anche come integrità del codice. Ci migliora la sicurezza dei Windows verificando l'integrità di un file ogni volta che viene caricato in memoria. Ci rileva se il codice dannoso ha modificato un file binario di sistema e genera un evento del log di diagnostica e di controllo del sistema quando la firma di un modulo kernel non viene verificata correttamente.
    -   Se l'app richiede autorizzazioni elevate, la richiesta di elevazione dei privilegi visualizza informazioni contestuali sul file eseguibile che richiede l'accesso con privilegi elevati. A seconda che l'app sia firmata con Authenticode, l'utente potrebbe visualizzare la richiesta di consenso o la richiesta di credenziali.
    -   I nomi sicuri impediscono a terze parti di eseguire lo spoofing del codice, purché la chiave privata sia protetta. Il .NET Framework verifica la firma digitale quando carica l'assembly o la installa nella GAC. Senza l'accesso alla chiave privata, un utente malintenzionato non può modificare il codice e firmarlo di nuovo.
-   Dettagli del test
    -   Tutti i file eseguibili, ad esempio quelli con estensioni di file .exe, .dll, ocx, .sys, .cpl, drv e scr, devono essere firmati con un certificato Authenticode.
    -   Tutti i driver in modalità kernel installati dall'app devono avere una firma Microsoft ottenuta tramite il programma WHQL o DRS. Tutti file system driver di filtro devono essere firmati WHQL.
-   Azione correttiva
    -   Firmare i file eseguibili dell'app.
    -   Usare makecert.exe per generare un certificato o ottenere una chiave di firma del codice da una delle autorità di certificazione (CA) commerciali, ad esempio VeriSign, Thawte o una CA Microsoft.
-   Eccezioni ed esenzioni
    -   Le derozioni verranno considerate solo per i ridistribuibili di terze parti non firmati. Per la concessione di questa deroga è necessaria una prova di comunicazione che richiede una versione firmata dei ridistribuibili.
    -   I pacchetti software a valore aggiunto del dispositivo sono esenti dalla certificazione del driver in modalità kernel, perché i driver devono essere certificati in Windows certificazione hardware.

## <a name="support-x64-windows-test"></a>Supporto di test Windows x64

Testare l'app per assicurarsi che il .exe sia compilato per l'architettura della piattaforma in cui verrà installata.

-   Sfondo
    -   Il file eseguibile deve essere compilato per l'architettura del processore in cui è installato. Alcuni file eseguibili potrebbero essere eseguiti in un'architettura del processore diversa, ma non è affidabile.
    -   La compatibilità dell'architettura è importante perché i processi a 32 bit non possono caricare DLL a 64 bit e i processi a 64 bit non possono caricare DLL a 32 bit. Analogamente, le versioni a 64 bit di Windows non supportano l'esecuzione di applicazioni basate su Windows a 16 bit perché gli handle hanno 32 bit significativi su Windows Windows a 64 bit, quindi non possono essere passati alle applicazioni a 16 bit. Pertanto, il tentativo di avviare un'applicazione a 16 bit avrà esito negativo nelle versioni a 64 bit di Windows.
    -   I driver di dispositivo a 32 bit non possono essere eseguiti in versioni a 64 bit di Windows e pertanto devono essere portati all'architettura a 64 bit.
    -   Per le applicazioni in modalità utente, il Windows a 64 bit include WOW64, che consente l'esecuzione di applicazioni Windows a 32 bit in sistemi che eseguono Windows a 64 bit, anche se con una certa perdita di prestazioni. Non esiste alcun livello di traduzione equivalente per i driver di dispositivo.
    -   Per mantenere la compatibilità con le versioni a 64 bit di Windows, le app devono supportare in modo nativo a 64 bit o, come minimo, le app basate su Windows a 32 bit devono essere eseguite senza problemi nei sistemi a 64 bit:
        -   Le app e i relativi programmi di installazione non devono contenere codice a 16 bit o basarsi su componenti a 16 bit.
        -   La configurazione dell'app deve rilevare e installare i driver e i componenti appropriati nelle versioni a 64 bit Windows.
        -   Tutti i plug-in della shell devono essere eseguiti in versioni a 64 bit di Windows.
        -   Le app eseguite nell'emulatore WoW64 non devono tentare di ignorare i meccanismi di virtualizzazione Wow64. Se esistono scenari specifici in cui le app devono rilevare se sono in esecuzione in un emulatore WoW64, devono eseguire questa operazione chiamando [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process).
-   Dettagli del test
    -   L'app non deve installare file binari a 16 bit. L'app non deve installare un driver in modalità kernel a 32 bit se deve essere eseguito in un computer a 64 bit.
-   Azioni correttive
    -   Compilare i file eseguibili e i driver per l'architettura del processore per cui si desidera installarli.

## <a name="os-version-checking-test"></a>Test di controllo della versione del sistema operativo

Verifica il modo in cui l'app verifica la versione Windows in cui è in esecuzione.

-   Sfondo
    -   Le app verificano la versione del sistema operativo testando una versione maggiore o uguale alla versione richiesta per garantire la compatibilità con le versioni future di Windows.
-   Dettagli del test
    -   Simula l'esecuzione dell'app in versioni diverse Windows per vedere come reagisce.
-   Azioni correttive
    -   Testare la versione corretta di Windows verificando se la versione corrente è maggiore o uguale alla versione richiesta dall'app, dal servizio o dal driver.
    -   I programmi di installazione dei driver e i moduli di disinstallazione non devono mai controllare la versione del sistema operativo.
-   Eccezioni e derozioni
    -   Le derozioni verranno considerate per le app che soddisfano i criteri *seguenti: (Si applica solo alla certificazione delle app desktop)*
        -   App recapitate come un unico pacchetto eseguito in Windows XP, Windows Vista e Windows 7 ed è necessario controllare la versione del sistema operativo per determinare quali componenti installare in un determinato sistema operativo.
        -   App che controllano solo la versione minima del sistema operativo (solo durante l'installazione, non in fase di esecuzione) usando solo le chiamate API approvate ed elencano il requisito di versione minima nel manifesto dell'app in base alle esigenze.
        -   App di sicurezza come app antivirus e firewall, utilità di sistema come utilità di deframmentazione e app di backup e strumenti di diagnostica che controllano la versione del sistema operativo usando solo le chiamate API approvate.

## <a name="user-account-control-uac-test"></a>Test del controllo dell'account utente

Testa l'app per verificare che non siano necessarie autorizzazioni inutilmente elevate per l'esecuzione.

-   Sfondo
    -   Un'app che opera o viene installata solo quando l'utente è un amministratore forza gli utenti a eseguire l'app con autorizzazioni inutilmente elevate, che possono consentire al malware di accedere al computer dell'utente.
    -   Quando gli utenti sono sempre costretti a eseguire app con token di accesso elevati, l'app può essere server come punto di ingresso per codice ingannevolo o dannoso. Questo malware può modificare facilmente il sistema operativo o, in caso contrario, influire su altri utenti. È quasi impossibile controllare un utente con accesso amministratore completo, perché gli amministratori possono installare le app ed eseguire qualsiasi app o script nel computer. I responsabili IT sono sempre alla ricerca di modi per creare "desktop standard" in cui gli utenti a log on come utenti standard. I desktop standard riducono notevolmente help desk costi e riducono il sovraccarico IT.
    -   La maggior parte delle applicazioni non richiede privilegi di amministratore in fase di esecuzione. Un account utente standard deve essere in grado di eseguirli. Windows app devono avere un manifesto (incorporato o esterno) per definire il livello di esecuzione che indica al sistema operativo i privilegi necessari per eseguire l'app. Il manifesto dell'app si applica solo .exe file, non .dll file. Controllo dell'account utente non controlla le DLL durante la creazione del processo. Le regole del controllo dell'account utente non si applicano servizi Microsoft. Il manifesto dell'app può essere incorporato o esterno.
    -   Per creare un manifesto, creare un file con il nome <app name>.exe.manifest e archiviarlo nella stessa directory del \_ file EXE. Si noti che qualsiasi manifesto esterno viene ignorato se l'app ha un manifesto interno.
        -   Ad esempio, <requestedExecutionLevel level=""asInvoker \| highestAvailable \| requireAdministrator"" uiAccess=""true \| false""/>
        -   Il processo principale dell'app deve essere eseguito come utente standard (**asInvoker**). Tutte le funzionalità amministrative devono essere spostate in un processo separato che viene eseguito con privilegi amministrativi.
        -   Le app rivolte agli utenti che richiedono privilegi elevati devono essere firmate con Authenticode.
-   Dettagli del test
    -   Tutti gli exe dell'utente devono essere contrassegnati con l'attributo asInvoker. Se sono contrassegnati come highestAvailable o requireAdministrator, devono essere firmati correttamente come authenticode. Qualsiasi file exe dell'app non deve avere l'attributo uiAccess impostato su true. Qualsiasi file exe eseguito come servizio è escluso da questo particolare controllo.
-   Azioni correttive
    -   Esaminare il file manifesto dell'app per le voci e i livelli di autorizzazione corretti.
-   Eccezioni e derozioni
    -   È necessaria una deroga per le app che eseguono il processo principale con privilegi elevati (**requireAdministrator** o **highestAvailable**). Il processo principale è il processo che fornisce il punto di ingresso dell'utente all'app.
    -   Le derove verranno considerate per gli scenari seguenti:
        -   Strumenti amministrativi o di sistema con il livello di esecuzione impostato su **highestAvailable,** **requireAdministrator** o entrambi.
        -   Solo l'app framework di accessibilità o automazione interfaccia utente imposta il flag uiAccess su TRUE per ignorare l'isolamento dei privilegi dell'interfaccia utente. Per avviare correttamente l'utilizzo delle app, questo flag deve essere firmato Authenticode e deve risiedere in un percorso protetto nel file system, ad esempio Programmi.

## <a name="adhere-to-system-restart-manager-messages"></a>Rispettare i messaggi di System Restart Manager

Verifica la risposta dell'app ai messaggi di arresto e riavvio del sistema.

-   Sfondo
    -   Le app devono uscire il più rapidamente possibile quando viene notificata l'arresto del sistema per offrire un'esperienza di arresto reattivo o di spegnimento per l'utente.
    -   In un arresto critico, le app che restituiscono FALSE a [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) verranno inviate **a WM \_ ENDSESSION** e chiuse, mentre quelle in timeout in risposta a WM QUERYENDSESSION verranno terminate \_ forzatamente.
-   Dettagli del test
    -   Esamina il modo in cui l'app risponde ai messaggi di arresto e di uscita.
-   Azioni correttive
    -   Se l'app non supera questo test, esaminare come gestisce questi Windows messaggi:
        -   [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) con *LPARAM*  =  **ENDSESSION \_ CLOSEAPP**(0x1): le app desktop devono rispondere (TRUE) immediatamente in preparazione del riavvio. Le app console possono chiamare [**SetConsoleCtrlHandler per**](/windows/console/setconsolectrlhandler) ricevere la notifica di arresto. I servizi possono chiamare [**RegisterServiceCtrlHandlerEx per**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) ricevere notifiche di arresto in una routine del gestore.
        -   [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) con *LPARAM*  =  **ENDSESSION \_ CLOSEAPP**(0x1): le app devono restituire un valore 0 entro 30 secondi e arrestarsi. Come minimo, le app devono prepararsi salvando i dati utente e indicando le informazioni necessarie dopo un riavvio.
    -   Le app console che ricevono la **notifica CTRL \_ C \_ EVENT** devono essere arrestate immediatamente. I driver non devono avere il veto su un evento di arresto del sistema.
    -   **Nota:** Le app che devono bloccare l'arresto a causa di un'operazione che non può essere interrotta devono usare [**ShutdownBlockReasonCreate**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasoncreate) per registrare una stringa che spiega il motivo all'utente. Al termine dell'operazione, l'app deve chiamare [**ShutdownBlockReasonDestroy**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasondestroy) per indicare che il sistema può essere arrestato.

## <a name="safe-mode-test"></a>test Cassaforte modalità di controllo

Verifica se il driver o il servizio è configurato per l'avvio in modalità provvisoria.

-   Sfondo
    -   Cassaforte consente agli utenti di diagnosticare e risolvere i problemi con Windows. Solo i driver e i servizi necessari per il funzionamento di base del sistema operativo o fornire servizi di diagnostica e ripristino devono essere caricati in modalità sicura. Il caricamento di altri file in modalità provvisoria rende più difficile risolvere i problemi con il sistema operativo.
    -   Per impostazione predefinita, solo i driver e i servizi preinstallato con Windows in modalità provvisoria. Tutti gli altri driver e servizi devono essere disabilitati a meno che il sistema non li richieda per operazioni di base o per scopi diagnostici e di ripristino.
-   Dettagli del test
    -   I driver installati dall'app non devono essere contrassegnati per il caricamento in modalità provvisoria.
-   Azioni correttive
    -   Se il driver o il servizio non deve essere avviato in modalità provvisoria, rimuovere le voci dell'app dalle chiavi del Registro di sistema.
-   Eccezioni e derozioni
    -   I driver e i servizi che devono essere avviati in modalità provvisoria richiedono la certificazione di una deroga. La richiesta di rinuncia deve includere ogni driver e servizio da aggiungere alle chiavi del Registro di sistema SafeBoot e descrivere i motivi tecnici per cui il driver o il servizio deve essere eseguito in modalità sicura. Il programma di installazione dell'app deve registrare tutti questi driver e servizi in queste chiavi del Registro di sistema:
        -   HKLM/System/CurrentControlSet/Control/SafeBoot/Minimal
        -   HKLM/System/CurrentControlSet/Control/SafeBoot/Network
-   **Nota:** È necessario testare i driver e i servizi da avviare in modalità provvisoria per assicurarsi che funzionino in modalità provvisoria senza errori.

## <a name="multiuser-session-test"></a>Test di sessione multiutente

Testare il comportamento dell'app quando viene eseguita in più sessioni contemporaneamente.

-   Sfondo
    -   Windows utenti devono essere in grado di eseguire sessioni simultanee. Le app devono garantire che quando vengono eseguite in più sessioni, in locale o in remoto, la normale funzionalità dell'app non sia influenzata negativamente. Le impostazioni dell'app e i file di dati devono essere specifici dell'utente e la privacy e le preferenze dell'utente devono essere limitate alla sessione dell'utente.
-   Dettagli del test
    -   Esegue più istanze simultanee dell'app per testare quanto segue:
        -   Più istanze di un'app in esecuzione contemporaneamente sono isolate l'una dall'altra.
    -   Ciò significa che i dati utente di un'istanza non sono visibili a un'altra istanza. L'audio in una sessione utente inattiva non deve essere ascoltato in una sessione utente attiva. Nei casi in cui più istanze dell'app usano risorse condivise, l'app deve assicurarsi che non si sia verificata un conflitto.
        -   Se l'app è stata installata per più utenti, archivia i dati nelle cartelle e nei percorsi corretti del Registro di sistema.
        -   L'app può essere eseguita in più sessioni utente (Cambio rapido utente) sia per l'accesso locale che per l'accesso remoto.
    -   A tale scopo, l'app deve controllare altre sessioni del servizio terminal (TS) per le istanze esistenti dell'app. Se l'app non supporta più sessioni utente o l'accesso remoto, deve dirlo chiaramente all'utente quando viene avviata da una sessione di questo tipo.
-   Azione correttiva
    -   Assicurarsi che l'app non archivi i file di dati a livello di sistema o le impostazioni negli archivi dati specifici dell'utente, ad esempio profilo utente o HKCU. In caso contrario, le informazioni non saranno disponibili per altri utenti.
    -   L'app deve installare i file di dati e di configurazione a livello di sistema durante l'installazione e creare i file e le impostazioni specifici dell'utente dopo l'installazione quando un utente la esegue.
    -   Assicurarsi che l'app non blocchi più sessioni simultanee, in locale o in remoto. L'app non deve dipendere da mutex globali o altri oggetti denominati per verificare o bloccare più sessioni simultanee.
    -   Se l'app non può consentire più sessioni simultanee per utente, usare spazi dei nomi per utente o per sessione per mutex e altri oggetti denominati.

## <a name="crashes-and-hangs-test"></a>Test si arresta in modo anomalo e si blocca

Monitoraggio dell'app durante il test per la certificazione per registrare eventuali arresti anomali o blocchi.

-   Sfondo
    -   Gli errori delle app, ad esempio arresti anomali e blocchi, sono un'interruzione importante per gli utenti e causano frustrazione. L'eliminazione di questi errori migliora la stabilità e l'affidabilità dell'app e, in generale, offre agli utenti un'esperienza di app migliore. Le app che smettono di rispondere o si arrestano in modo anomalo possono provocare perdite di dati e non offrono un'esperienza utente ottimale.
-   Dettagli del test
    -   Testiamo l'app per verificarne la resilienza e la stabilità per l'intera durata del test di certificazione.
    -   Il Windows kit di certificazione dell'app chiama [**IApplicationActivationManager::ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication) per avviare Windows app di Store. Per avviare un’app mediante **ActivateApplication**, è necessario che Controllo dell’account utente sia abilitato e che la risoluzione dello schermo sia almeno 1024 x 768 o 768 x 1024. In assenza di queste due condizioni, l'app non supererà questo test.
-   Azioni correttive
    -   Assicurati che Controllo account utente sia attivato nel computer di prova.
    -   Assicurati che il test venga eseguito su un computer con uno schermo sufficientemente ampio.
    -   Se l'app non viene avviata e la piattaforma di test soddisfa i prerequisiti di [**ActivateApplication,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication)è possibile risolvere il problema esaminando il registro eventi di attivazione. Per individuare le voci pertinenti nel registro eventi:
        1.  Aprire eventvwr.exe e passare al nodo applicazione \\ Windows \\ log.
        2.  Filtra la visualizzazione in modo da mostrare gli ID degli eventi: 5900-6000.
        3.  Esamina le voci del registro con l'obiettivo di trovare una spiegazione al fatto che l'app non si è avviata.
    -   Cerca il file che ha causato il problema, identifica l'errore e correggilo. Ricompila ed esegui un nuovo test dell'app.
-   Risorse aggiuntive
    -   [Uso di Application Verifier all'interno del ciclo di vita dello sviluppo software](https://blogs.msdn.com/b/ntdebugging/archive/2014/01/13/debugging-a-windows-8-1-store-app-crash-dump.aspx)
    -   [Application Verifier]( https://go.microsoft.com/fwlink/p/?LinkId=708300)
    -   [Uso di Application Verifier](https://www.microsoft.com/?ref=go)
    -   [DLL AppInit](https://www.microsoft.com/?ref=go)
    -   [Ridurre al minimo il tempo di avvio (app di Windows Store scritte in C#/VB/C++ e XAML)](/previous-versions/windows/apps/hh994639(v=win.10))

## <a name="compatibility-and-resiliency-test"></a>Test di compatibilità e resilienza

-   Sfondo
    -   Questo controllo convaliderà due aspetti di un'app, i file eseguibili principali dell'app, ad esempio il punto di ingresso dell'app rivolto all'utente, devono essere manifestati per motivi di compatibilità, nonché dichiarare il GUID corretto. Per supportare questo nuovo test, il report avrà un sottonodo in "Compatibilità & resilienza". L'app avrà esito negativo se una o entrambe queste condizioni non sono presenti.
-   Dettagli test
    -   **Compatibilità:** Le app devono essere completamente funzionali senza usare Windows modalità di compatibilità, messaggi di AppHelp o altre correzioni di compatibilità. Un manifesto di compatibilità Windows fornire all'app il comportamento di compatibilità corretto nelle diverse versioni del sistema operativo
    -   **AppInit:** Le app non devono elencare le DLL da caricare nella chiave del Registro di sistema HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion Windows \\ \\ AppInit \_ DLLs.
    -   **Switchback:** L'applicazione deve fornire il manifesto di switchback. Se il manifesto non è presente, Windows kit di certificazione dell'app restituisce un messaggio di avviso. Windows App Certification Kit verificherà anche che il manifesto contenga un GUID del sistema operativo valido.
-   Azioni correttive
    -   Correggere il componente dell'app che usa la correzione di compatibilità.
    -   Assicurarsi che l'app non si basa sulle correzioni di compatibilità per le relative funzionalità.
    -   Verificare che l'app sia manifeste e che la sezione di compatibilità includa i valori appropriati
-   Informazioni aggiuntive
    -   Per [altre informazioni, vedere DLL AppInit.](/previous-versions/windows/apps/hh994639(v=win.10))

## <a name="windows-security-best-practices-test"></a>Sicurezza di Windows test delle procedure consigliate

-   Sfondo
    -   Un'app non deve modificare le impostazioni di sicurezza Windows predefinite
-   Dettagli test
    -   Testa la sicurezza dell'app eseguendo Attack Surface Analyzer. L'approccio consiste nell'aggiungere categorie di errori per ogni test. Ad esempio, alcune categorie per il test di sicurezza possono includere:
        -   Errore di inizializzazione
        -   Errore dell'architettura di sicurezza
        -   Possibile errore di overflow del buffer
        -   Errore di arresto anomalo del sistema
    -   Per informazioni dettagliate, vedere [qui](/previous-versions/windows/hh920280(v=win.10)).
-   Azioni correttive
    -   Risolvere e risolvere il problema identificato dai test. Ricompila ed esegui un nuovo test dell'app.

## <a name="windows-security-features-test"></a>Windows test delle funzionalità di sicurezza

-   Sfondo
    -   Le applicazioni devono acconsentire esplicitamente Windows di sicurezza. La modifica delle protezioni di sicurezza di Windows predefinite può comportare maggiori rischi per gli utenti.
-   Dettagli del test
    -   Testa la sicurezza dell’app tramite l’esecuzione dello strumento BinScope Binary Analyzer. Per informazioni dettagliate, vedere [qui](/previous-versions/windows/hh920280(v=win.10)).
-   Azioni correttive
    -   Risolvere e risolvere il problema identificato dai test. Ricompila ed esegui un nuovo test dell'app.

## <a name="high-dpi-test"></a>Test con valori DPI alti

È consigliabile che le app Win32 siano in grado di riconoscere DPI. È fondamentale fare in modo che l'interfaccia utente dell'app sia coerente in un'ampia gamma di impostazioni di visualizzazione con valori DPI alti. Un'app non in grado di riconoscere DPI in esecuzione in un'impostazione di visualizzazione con valori DPI elevati può avere problemi come il ridimensionamento non corretto degli elementi dell'interfaccia utente, il testo ritagliato e le immagini sfocate. Esistono due modi per dichiarare che un'app è in grado di riconoscere DPI. Uno è dichiarare DPI.

-   Sfondo
    -   Questo controllo convaliderà due aspetti di un'app: i file eseguibili principali, ad esempio i punti di ingresso dell'app rivolti all'utente, devono essere manifesti per la sensibilità ai valori DPI alti e le API appropriate vengono chiamate per supportare valori DPI alti. L'app avrà esito negativo se mancano una o entrambe queste condizioni. Questo controllo introdurrà una nuova sezione nel report desktop. Vedere l'esempio riportato di seguito.
-   Dettagli test
    -   Il test genererà un avviso quando viene rilevato uno degli elementi seguenti:
        -   Il file EXE principale non dichiara il riconoscimento DPI nel manifesto e non chiama l'API SetProcessDPIAware. Avvisare lo sviluppatore se si dimentica di aggiungere il manifesto di consapevolezza DPI.
        -   Il file EXE principale non dichiara il riconoscimento DPI nel manifesto, ma chiama l'API SetProcessDPIAware (avvisa lo sviluppatore che deve usare il manifesto per dichiarare la consapevolezza DPI anziché chiamare l'API).
        -   MainEXE dichiara il riconoscimento DPI nel manifesto, ma chiama anche l'API SetProcessDPIAware (avvisare lo sviluppatore che la chiamata a tale API non è necessaria).
        -   Per i file binari che non sono file EXE principali, se chiamano l'API, fornire un avviso (la chiamata all'API non è consigliata).
-   Azioni correttive
    -   L'uso della funzione SetProcessDPIAware() è sconsigliato. Se una DLL memorizza nella cache le impostazioni DPI durante l'inizializzazione, la chiamata di SetProcessDPIAware() nell'app può generare un race condition. Non è consigliabile chiamare la funzione SetProcessDPIAware() in una DLL.
-   Informazioni aggiuntive
    -   [Scrittura di app con valori DPI elevati](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))

 

 
