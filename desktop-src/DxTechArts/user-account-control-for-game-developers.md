---
title: Controllo dell'account utente per sviluppatori di giochi
description: Questo articolo descrive le linee guida e le procedure consigliate per gli sviluppatori di giochi per usare in modo efficace la funzionalità di sicurezza Controllo dell'account utente (UAC) introdotta in Windows Vista.
ms.assetid: dbac1c07-73dd-f2bc-3c5c-d6160368a88f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cb8b6ac31ef13e3ace4d439c82f4708673aeffb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886069"
---
# <a name="user-account-control-for-game-developers"></a>Controllo dell'account utente per sviluppatori di giochi

Questo articolo descrive le linee guida e le procedure consigliate per gli sviluppatori di giochi per usare in modo efficace la funzionalità di sicurezza Controllo dell'account utente (UAC) introdotta in Windows Vista.

-   [Panoramica del controllo dell'account utente](#overview-of-user-account-control)
-   [Account utente in Windows Vista](#user-accounts-in-windows-vista)
-   [Accesso ai file come utente standard](#file-access-as-a-standard-user)
-   [Accesso al Registro di sistema come utente standard](#registry-access-as-a-standard-user)
-   [Elevazione dei privilegi](#privilege-elevation)
-   [Implicazioni del controllo dell'account utente con CreateProcess()](#uac-implications-with-createprocess)
-   [Impostazione del livello di esecuzione nel manifesto dell'applicazione](#setting-the-execution-level-in-the-application-manifest)
-   [Incorporamento di un manifesto in Visual Studio](#embedding-a-manifest-in-visual-studio)
-   [Compatibilità del controllo dell'account utente con i giochi meno recenti](#uac-compatibility-with-older-games)
-   [Scenari e manifesti legacy](#legacy-scenarios-and-manifests)
-   [Conclusione](#conclusion)
-   [Altre informazioni](#further-reading)

## <a name="overview-of-user-account-control"></a>Panoramica del controllo dell'account utente

Controllo dell'account utente ( UAC), introdotto in Windows Vista, è una funzionalità di sicurezza progettata per impedire a utenti malintenzionati di usare punti deboli o bug rilevati nelle applicazioni ampiamente usate per modificare il sistema operativo o altri programmi installati. Questa operazione viene eseguita eseguendo la maggior parte dei programmi e dei processi come utente Standard (noto anche come utente limitato, utente con restrizioni o utente Least-Privileged) anche se l'account dell'utente corrente dispone di credenziali amministrative. Un processo con privilegi utente standard presenta molte restrizioni intrinseche che impediscono di apportare modifiche a livello di sistema.

Controllo dell'account utente è anche responsabile dell'elevazione dei privilegi di un processo tramite uno schema di autenticazione basato su finestre di dialogo avviato all'esecuzione di determinati processi designati come che richiedono privilegi amministrativi. L'elevazione dei privilegi consente agli amministratori di eseguire la maggior parte delle applicazioni a un livello di privilegi sicuri (come qualsiasi altro utente standard), ma consente anche processi e operazioni che richiedono privilegi amministrativi. Controllo dell'account utente supporta l'autenticazione over the shoulder in modo che un amministratore possa concedere privilegi elevati a un programma mentre un utente standard è attualmente connesso al sistema.

La funzionalità Controllo dell'account utente è abilitata per impostazione predefinita. Anche se un amministratore può disabilitare il controllo dell'account utente a livello di sistema, questa operazione presenta una serie di ramificazioni negative. In primo luogo, ciò consente di attenuare la sicurezza di tutti gli account amministrativi, poiché tutti i processi verrebbero eseguiti con credenziali amministrative, anche quando la maggior parte delle applicazioni non li richiede effettivamente. Con controllo dell'account utente disabilitato, un'applicazione utente standard che espone una vulnerabilità sfruttabile nella sicurezza può potenzialmente essere usata per rubare informazioni private, installare rootkit o spyware, distruggere l'integrità del sistema o ospitare attacchi di tipo malware su altri sistemi. Mentre con il controllo dell'account utente abilitato, l'esecuzione della maggior parte del software come utente standard limita notevolmente i potenziali danni causati da un bug di questo tipo. In secondo luogo, la disattivazione del controllo dell'account utente disabilita molte delle soluzioni alternative per la compatibilità delle applicazioni che consentono agli utenti standard veri di eseguire correttamente un'ampia gamma di applicazioni. La disabilitazione del controllo dell'account utente non deve mai essere consigliata come soluzione alternativa per la compatibilità.

È importante notare che le applicazioni devono cercare di usare i diritti utente standard solo se possibile. Anche se gli amministratori possono elevare facilmente i privilegi di un processo, l'elevazione dei privilegi richiede comunque l'interazione e il riconoscimento dell'utente ogni volta che viene eseguita un'applicazione che richiede credenziali amministrative. Questa elevazione dei privilegi deve essere eseguita anche al momento dell'avvio del programma, pertanto la richiesta di credenziali amministrative anche per una singola operazione richiede l'esposizione del sistema a un rischio maggiore per l'intero tempo di esecuzione dell'applicazione. Gli utenti standard senza alcuna possibilità di elevare i propri privilegi sono comuni anche nelle impostazioni aziendali e della famiglia. "RunAs Administrator" non è una soluzione alternativa per la compatibilità, espone l'utente e il sistema a un maggiore rischio per la sicurezza e crea frustrazione per gli utenti in molte situazioni.

> [!Note]  
> La funzionalità Controllo account utente introdotta in Windows Vista è presente anche in Windows 7. Anche se l'esperienza utente che lavora con le varie funzionalità di sistema è stata migliorata rispetto al controllo dell'account utente, l'impatto sulle applicazioni è fondamentalmente lo stesso. Tutte le raccomandazioni Windows Vista in questo articolo si applicano anche Windows 7. Per informazioni dettagliate sulle modifiche dell'interfaccia utente di Controllo dell'account utente per Windows 7, vedere Interfaccia utente - Aggiornamenti della finestra di [dialogo di controllo dell'account utente](../win7appqual/user-interface---user-account-control-dialog-updates.md).

 

## <a name="user-accounts-in-windows-vista"></a>Account utente in Windows Vista

Windows Vista classifica ogni utente in due tipi di account utente: amministratori e utenti standard.

Un account utente standard è simile a un account utente limitato in Windows XP. Come in Windows XP, un utente standard non può scrivere nella cartella Programmi, non può scrivere nella parte HKEY LOCAL MACHINE del Registro di sistema e non può eseguire attività che modificano il sistema, ad esempio l'installazione di un driver in modalità kernel o l'accesso agli spazi di processo a livello di \_ \_ sistema.

L'account Amministratore è stato modificato in modo significativo Windows è stato rilasciato XP. In precedenza, a tutti i processi avviati da un membro del gruppo Administrators venivano dati privilegi amministrativi. Con controllo dell'account utente abilitato, tutti i processi vengono eseguiti con privilegi utente standard, a meno che non siano specificamente elevati da un amministratore. Questa differenza rende più sicuri gli account nel gruppo Administrators riducendo il rischio di sicurezza rappresentato da potenziali bug nella maggior parte dei programmi.

È importante che tutte le applicazioni, in particolare i giochi, funzionino in modo efficace e responsabile quando vengono eseguite come processo utente standard. Tutte le operazioni che richiedono privilegi amministrativi devono essere eseguite in fase di installazione o da programmi ausiliari che richiedono esplicitamente credenziali amministrative. Sebbene l'elevazione dei privilegi sia piuttosto semplice per un membro del gruppo Administrators, gli utenti standard devono rinviare a un utente con credenziali amministrative l'immissione fisica della password per elevare i privilegi. Poiché gli account protetti dal controllo genitori devono essere utenti standard, si tratta di una situazione molto comune per i giocatori che usano Windows Vista.

Se il gioco sta già lavorando Windows XP con account utente limitati, il passaggio a Controllo account utente in Windows Vista dovrebbe essere molto semplice. La maggior parte di queste applicazioni funzionerà così come sono, anche se è consigliabile aggiungere un manifesto dell'applicazione. I manifesti sono descritti più avanti in questo argomento in [Impostazione del livello di esecuzione nel manifesto dell'applicazione.](#setting-the-execution-level-in-the-application-manifest)

## <a name="file-access-as-a-standard-user"></a>Accesso ai file come utente standard

L'aspetto del gioco più interessato dalle restrizioni degli utenti standard è file system'organizzazione e l'accessibilità. Non si deve mai presupporre che il gioco possa scrivere file nella cartella in cui è installato il gioco. In Windows Vista, ad esempio, i privilegi di un utente devono essere elevati dal sistema operativo prima che un'applicazione possa scrivere nella cartella Programmi. Per evitare questo problema, è necessario classificare i file di dati del gioco in base all'ambito e all'accessibilità e usare la funzione [**SHGetFolderPath,**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) insieme alle costanti CSIDL fornite dalla shell di Windows, per generare i percorsi di file appropriati. Le costanti CSIDL corrispondono alle cartelle note nel file system che il sistema operativo usa e alza di livello per partizionare file globali e specifici dell'utente.

Il tentativo di creare o scrivere un file o una directory in una cartella che non concede l'autorizzazione di scrittura al processo avrà esito negativo Windows Vista se l'applicazione non dispone di privilegi amministrativi. Se l'eseguibile del gioco a 32 bit è in esecuzione in modalità legacy, perché non ha dichiarato un livello di esecuzione richiesto, le operazioni di scrittura avranno esito positivo, ma saranno soggette alla virtualizzazione come descritto nella sezione "Compatibilità del controllo dell'account utente con i giochi meno recenti" più avanti in questo articolo.

**Tabella 1. Cartelle note**



| Nome CSIDL             | Percorso tipico (Windows Vista)                                                   | Diritti utente standard | Diritti di amministratore | Ambito di accesso | Descrizione                                                                                                                      | Esempi                                                          |
|------------------------|--------------------------------------------------------------------------------|----------------------|----------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| CSIDL \_ PERSONAL        | C: \\ Utenti nome utente \\ \\ Documenti                                                | Lettura/Scrittura           | Lettura/Scrittura           | Per-User     | File di gioco specifici dell'utente che vengono letti e modificati e possono essere modificati all'esterno del contesto del gioco.                          | Schermate. File di gioco salvati con un'associazione di estensione di file. |
| CSIDL \_ LOCAL \_ APPDATA  | C: \\ Nome utente degli utenti \\ \\ AppData \\ Local                                           | Lettura/Scrittura           | Lettura/Scrittura           | Per-User     | File di gioco specifici dell'utente che vengono letti e modificati e vengono utilizzati solo all'interno del contesto del gioco.                                 | File della cache dei giochi. Configurazioni del lettore.                          |
| CSIDL \_ COMMON \_ APPDATA | C: \\ ProgramData                                                                | Lettura/scrittura se proprietario  | Lettura/Scrittura           | Tutti gli utenti    | File di gioco che possono essere creati da un utente e letti da tutti gli utenti. L'accesso in scrittura viene concesso solo all'autore del file (proprietario). | Profili utente                                                     |
| FILE DI PROGRAMMA \_ \_ CSIDL  | C: \\ Programmi<br/> oppure<br/> C: \\ Programmi (x86) <br/> | Sola lettura            | Lettura/Scrittura           | Tutti gli utenti    | File di gioco statici scritti dal programma di installazione del gioco che vengono letti da tutti gli utenti.                                                    | Asset di gioco, ad esempio materiali e mesh.                        |



 

Il gioco verrà in genere installato in una cartella nella cartella rappresentata dalla costante CSIDL \_ PROGRAM \_ FILES. Questo meccanismo non viene, tuttavia, sempre applicato. È invece consigliabile usare un percorso relativo dal file eseguibile quando si generano stringhe di percorso in file o directory che si trovano nella cartella di installazione.

È anche consigliabile evitare presupposti hard-coded sui percorsi di cartella noti. Ad esempio, in Windows XP Professional Edizione a 64 bit e Windows Vista x64, il percorso dei file di programma è C: Programmi (x86) per i programmi a 32 bit e C: Programmi per i programmi a \\ \\ 64 bit. Questi percorsi noti vengono modificati da Windows XP e gli utenti possono riconfigurare il percorso di molte di queste cartelle e persino individuarle in unità diverse. Usare quindi sempre le costanti CSIDL per evitare confusione e potenziali problemi. Windows Il programma di installazione comprende questi percorsi di cartelle note e sposta i dati durante l'aggiornamento del sistema operativo da Windows XP; al contrario, l'uso di percorsi non standard o hard-coded potrebbe non riuscire dopo un aggiornamento del sistema operativo.

È necessario prestare attenzione alle sottili differenze di usabilità tra le cartelle specifiche dell'utente specificate da CSIDL \_ PERSONAL e CSIDL \_ LOCAL \_ APPDATA. La procedura consigliata per selezionare la costante CSIDL da usare per la scrittura di un file consiste nell'usare CSIDL PERSONAL se si prevede che l'utente interagisca con il file, ad esempio facendo doppio clic su di esso per aprirlo in uno strumento o in un'applicazione e usare \_ CSIDL LOCAL APPDATA per \_ altri \_ file. Entrambe le cartelle possono essere sfruttate dall'applicazione per archiviare e organizzare file di dati specifici dell'utente, in quanto non esiste alcuna differenza nell'ambito di accesso o nel livello di privilegio. È necessario fare attenzione a creare nomi di percorso sufficientemente univoci da non collidere con altre applicazioni, ma sufficientemente brevi da mantenere il numero di caratteri nel percorso completo inferiore al valore di MAX \_ PATH, 260.

Il codice seguente fornisce un esempio di come scrivere un file in una cartella nota:

``` syntax
#include <windows.h>
#include <shlobj.h>
#include <shlwapi.h>
        ...
        ...
        ...
        TCHAR strPath[MAX_PATH];
        if( SUCCEEDED(
        SHGetFolderPath( NULL, CSIDL_PERSONAL, NULL, SHGFP_TYPE_CURRENT, strPath ) ) )
        {
        PathAppend( strPath, TEXT( "Company Name\\Title" ) );

        if( !PathFileExists( strPath ) )
        {
        if( ERROR_SUCCESS != SHCreateDirectoryEx( NULL, strPath, NULL ) )
        return E_FAIL;
        }

        PathAppend( strPath, TEXT( "gamefile.txt" ) );

        // strPath is now something like:
        // C:\Users\<current user>\Documents\Company Name\Title\gamefile.txt
        // Open the file for writing
        HANDLE hFile = CreateFile(strPath, GENERIC_WRITE, NULL, NULL, CREATE_ALWAYS, FILE_ATTRIBUTE_NORMAL, NULL);

        if( INVALID_HANDLE_VALUE != hFile )
        {
        // TODO: Write to file
        CloseHandle(hFile);
        }
        }
```

## <a name="registry-access-as-a-standard-user"></a>Accesso al Registro di sistema come utente standard

L'accesso al Registro di sistema da parte di un utente standard è limitato in modo analogo a quello file system. A un utente standard è consentito l'accesso in lettura a tutte le chiavi nel Registro di sistema. Tuttavia, l'accesso in scrittura viene concesso solo al sottoalbero HKEY CURRENT USER (HKCU), mappato internamente alla sottochiave specifica dell'utente \_ \_ HKEY \_ USERS Security ID (SID) dell'utente \\ corrente. Un'applicazione che deve scrivere in qualsiasi percorso del Registro di sistema diverso da HKEY \_ CURRENT USER richiede privilegi \_ amministrativi.

Se l'applicazione a 32 bit non contiene un livello di esecuzione richiesto nel manifesto, tutte le scritture in HKEY LOCAL MACHINE Software verranno virtualizzate, mentre le scritture in altre posizioni esterne a HKEY CURRENT USER avranno esito \_ \_ \\ \_ \_ negativo.

Non è consigliabile archiviare dati persistenti nel Registro di sistema, come la configurazione di un utente. Il metodo preferito per archiviare dati persistenti dal gioco è scrivere i dati nel file system chiamando [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) e ottenere il valore di una costante CSIDL, descritta nella sezione precedente.

## <a name="privilege-elevation"></a>Elevazione dei privilegi

In Windows Vista, qualsiasi applicazione che richiede privilegi amministrativi deve dichiarare una richiesta per un livello di esecuzione amministrativa nel manifesto (descritto nella sezione successiva, Impostazione del livello di esecuzione nel manifesto [dell'applicazione](#setting-the-execution-level-in-the-application-manifest)).

L'elevazione dei privilegi, come è noto, è la procedura guidata dal controllo dell'account utente per promuovere un processo a un processo amministrativo. I privilegi di un processo possono essere elevati solo in fase di creazione. Una volta creato, un processo non verrà mai promosso a un livello di privilegi più elevato. Per questo motivo. Le operazioni che richiedono credenziali amministrative devono essere isolate per separare i programmi di installazione e altri programmi ausiliari.

Al momento dell'esecuzione di un programma, Controllo dell'account utente controlla il livello di esecuzione richiesto nel manifesto e, se sono necessari privilegi elevati, richiede all'utente corrente una delle due finestre di dialogo standard: una per un utente standard e una per un amministratore.

Se l'utente corrente è un utente standard, il controllo dell'account utente richiede all'utente le credenziali di un amministratore prima di consentire l'esecuzione del programma.

**Figura 1. Richiedere a un utente Standard di immettere le credenziali per un account amministrativo**

![richiedere a un utente standard di immettere le credenziali per un account amministrativo](images/uac-prompt-elevation.jpg)

Se l'utente corrente è un amministratore, il controllo dell'account utente richiede l'autorizzazione prima di consentire l'esecuzione del programma.

**Figura 2. Richiedere a un amministratore di autorizzare le modifiche al computer**

![richiedere a un amministratore di autorizzare le modifiche al computer](images/uac-prompt-authorization.jpg)

All'applicazione verranno concessi privilegi amministrativi solo se un utente standard fornisce le credenziali amministrative appropriate o un utente amministratore fornisce l'acknowledgement. Qualsiasi altro elemento causerà la terminazione dell'applicazione.

È importante notare che un processo con privilegi elevati viene eseguito come utente amministratore che ha immesso le credenziali nel prompt del controllo dell'account utente anziché come utente standard che è attualmente connesso. Simile a **RunAs** in Windows XP, il processo con privilegi elevati ottiene le chiavi del Registro di sistema e della cartella dell'amministratore quando accede ai dati per utente e tutti i programmi avviati dal processo con privilegi elevati ereditano anche i diritti amministrativi e i percorsi degli account utente. Per gli amministratori a cui viene richiesto di confermare (**Continua** o **Annulla**), queste posizioni corrisponderanno alle posizioni dell'utente corrente. In generale, tuttavia, i processi che richiedono l'elevazione dei privilegi non devono funzionare sui dati per utente. Si noti che ciò può influire in modo sostanziale sul funzionamento del programma di installazione. Se il programma di installazione, in esecuzione come amministratore, scrive in HKCU o nel profilo di un utente, potrebbe essere scritto nella posizione errata. Prendere in considerazione la creazione di questi valori per utente alla prima esecuzione del gioco.

## <a name="uac-implications-with-createprocess"></a>Implicazioni del controllo dell'account utente con CreateProcess()

Il meccanismo di elevazione del controllo dell'account utente non verrà richiamato da una chiamata alla funzione [**Win32 CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)() per avviare un eseguibile configurato per richiedere un livello di esecuzione superiore rispetto al processo corrente. Di conseguenza, la chiamata a **CreateProcess**() avrà esito negativo con [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)() che restituisce ERROR \_ ELEVATION \_ REQUIRED. **CreateProcess**() avrà esito positivo solo quando il livello di esecuzione del chiamato è uguale o minore di quello del chiamante. Un processo non con privilegi elevati che deve generare processi elevati deve eseguire questa operazione usando la funzione [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)(), che causerà l'attivazione del meccanismo di elevazione del controllo dell'account utente tramite la shell.

## <a name="setting-the-execution-level-in-the-application-manifest"></a>Impostazione del livello di esecuzione nel manifesto dell'applicazione

Dichiarare il livello di esecuzione richiesto del gioco aggiungendo un'estensione al manifesto dell'applicazione. Il codice XML seguente illustra la configurazione minima necessaria per impostare il livello di esecuzione per un'applicazione:

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
        <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
                <ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
        </ms_asmv2:security>
    </ms_asmv2:trustInfo>
</assembly>
```

Nel codice precedente il sistema operativo viene informato che il gioco richiede solo privilegi utente standard con il tag seguente:

``` syntax
<ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
```

Impostando in modo esplicito requestedExecutionLevel su "asInvoker", questo esempio afferma al sistema operativo che il gioco si comporterà correttamente senza privilegi amministrativi. Di conseguenza, il controllo dell'account utente disabilita la virtualizzazione ed esegue il gioco con gli stessi privilegi dell'invoker, che in genere sono privilegi utente standard, poiché Windows Explorer viene eseguito come utente standard.

Il sistema operativo può essere informato che un gioco richiede l'elevazione dei privilegi amministrativi sostituendo "asInvoker" con "requireAdministrator", per creare il tag seguente:

``` syntax
<ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
```

Con questa configurazione, il sistema operativo richiede all'utente corrente una delle finestre di dialogo di elevazione del controllo dell'account utente standard ogni volta che viene eseguito il gioco. È consigliabile che nessun gioco richieda privilegi di amministratore per l'esecuzione, perché non solo questa finestra di dialogo diventerà rapidamente fastidiosa, ma rende anche il gioco incompatibile con i controlli parentali. Considerare con attenzione prima di aggiungere questo requisito a qualsiasi eseguibile.

Un errore comune è che l'aggiunta di un manifesto che imposta requestedExecutionLevel su "requireAdministrator" ignora la necessità di una richiesta di elevazione dei privilegi. Risposta errata. Impedisce semplicemente al sistema operativo di indovinare se l'applicazione di installazione o di aggiornamento necessita di privilegi amministrativi. All'utente viene comunque richiesto di autorizzare l'elevazione dei privilegi.

Windows verifica la firma di qualsiasi applicazione contrassegnata per l'elevazione dei privilegi prima di visualizzare la richiesta di controllo dell'account utente. Un eseguibile di grandi dimensioni contrassegnato per l'elevazione dei privilegi richiede più tempo per il controllo rispetto a un eseguibile di piccole dimensioni e più lungo di un eseguibile contrassegnato come "asInvoker". I file eseguibili di installazione autoestraente devono pertanto essere contrassegnati come "asInvoker" e qualsiasi parte che deve essere contrassegnata come "requireAdministrator" deve essere inserita in un eseguibile helper separato.

L'attributo uiAccess, illustrato negli esempi precedenti, deve sempre essere FALSE per i giochi. Questo attributo specifica se i client di automazione interfaccia utente hanno accesso all'interfaccia utente del sistema protetta e ha implicazioni di sicurezza speciali se impostate su TRUE.

## <a name="embedding-a-manifest-in-visual-studio"></a>Incorporamento di un manifesto in Visual Studio

Il supporto del manifesto è stato aggiunto per la Visual Studio a partire da VS2005. Per impostazione predefinita, un eseguibile compilato Visual Studio 2005 (o versione più recente) avrà un manifesto generato automaticamente incorporato in esso come parte del processo di compilazione. Il contenuto del manifesto generato automaticamente dipende da determinate configurazioni di progetto specificate nella finestra di dialogo delle proprietà del progetto.

Il manifesto generato automaticamente da Visual Studio 2005 non conterrà un blocco trustInfo perché non è possibile configurare il livello di esecuzione del controllo dell'account utente nelle proprietà &lt; &gt; del progetto. Il modo preferito per aggiungere queste informazioni è consentire a VS2005 di unire un manifesto definito dall'utente contenente il blocco trustInfo con il &lt; manifesto generato &gt; automaticamente. Questa operazione è semplice come l'aggiunta di un \* file manifesto alla soluzione che contiene il codice XML elencato nella sezione precedente. Quando Visual Studio rileva un file con estensione manifest nella soluzione, richiama automaticamente lo strumento manifesto (mt.exe) per unire i file con estensione manifest con quello generato automaticamente.

> [!Note]  
> È presente un bug nello strumento manifesto (mt.exe) fornito da Visual Studio 2005 che determina un manifesto unito e incorporato che può causare problemi quando l'eseguibile viene eseguito Windows XP prima di SP3. Il bug è il risultato del modo in cui lo strumento ridefinisce lo spazio dei nomi predefinito alla dichiarazione del &lt; blocco &gt; trustInfo. Fortunatamente, è facile ignorare completamente il problema dichiarando in modo esplicito uno spazio dei nomi diverso nel blocco trustInfo e impostando l'ambito dei nodi figlio &lt; nel nuovo spazio dei &gt; nomi. Il codice XML fornito nella sezione precedente illustra questa correzione.

 

Un'avvertenza nell'uso dello strumento mt.exe incluso in Visual Studio 2005 è che genererà un avviso durante l'elaborazione del blocco trustInfo perché lo strumento non contiene uno schema aggiornato per convalidare il codice &lt; &gt; XML. Per risolvere questo avviso, è consigliabile sostituire tutti i file mt.exe nella directory di installazione di Visual Studio 2005 (sono presenti più istanze) con il mt.exe fornito nell'SDK di Windows più recente.

A partire Visual Studio 2008, è ora possibile specificare il livello di esecuzione di un'applicazione dalla finestra di dialogo delle proprietà del progetto (figura 3) o usando il flag del linker /MANIFESTUAC. L'impostazione di queste opzioni Visual Studio 2008 genera automaticamente e incorpora un manifesto con il blocco &lt; trustInfo &gt; appropriato nel file eseguibile.

**Figura 3. Impostazione del livello di esecuzione in Visual Studio 2008**

![impostazione del livello di esecuzione in Visual Studio 2008](images/setting-execution-level-in-vs2008.jpg)

L'incorporamento di un manifesto nelle versioni precedenti di Visual Studio senza supporto del manifesto è comunque possibile, ma richiede più lavoro da parte dello sviluppatore. Per un esempio su come eseguire questa operazione, esaminare il progetto Visual Studio 2003 incluso in qualsiasi esempio in DirectX SDK prima della versione di marzo 2008.

## <a name="uac-compatibility-with-older-games"></a>Compatibilità del controllo dell'account utente con i giochi meno recenti

Se il gioco sembra salvare e caricare correttamente un file nella directory Programmi, ma nessuna evidenza del file iOn Windows Vista, qualsiasi applicazione a 32 bit che non contiene un livello di esecuzione richiesto nel manifesto viene considerata un'applicazione legacy. Prima di Windows Vista, la maggior parte delle applicazioni era in genere eseguita da utenti con privilegi amministrativi. Di conseguenza, queste applicazioni potevano leggere e scrivere liberamente i file di sistema e le chiavi del Registro di sistema e molti sviluppatori non apportavano le modifiche necessarie per funzionare correttamente sugli account utente limitati in Windows XP. Tuttavia, Windows Vista, queste stesse applicazioni avrebbero ora esito negativo a causa di privilegi di accesso insufficienti nel nuovo modello di sicurezza, che impone l'esecuzione degli utenti standard per le applicazioni legacy. Per attenuare l'impatto di questa operazione, è stata aggiunta anche la virtualizzazione Windows Vista. La virtualizzazione manterà migliaia di applicazioni legacy che funzionano bene in Windows Vista senza richiedere che tali applicazioni abbia privilegi elevati in qualsiasi momento, semplicemente per avere esito positivo in alcune operazioni secondarie. s trovato, è probabile che il gioco sia in esecuzione in modalità legacy ed è stato sottoposto a virtualizzazione.

La virtualizzazione influisce sul file system e sul Registro di sistema reindirizzando le scritture sensibili al sistema (e le operazioni successive su file o registro) a una posizione per utente all'interno del profilo dell'utente corrente. Ad esempio, se un'applicazione tenta di scrivere nel file seguente:

<dl> C: \\ Program Files Company Name Title \\ \\ \\config.ini  
</dl>

la scrittura viene reindirizzata automaticamente a:

<dl> C: \\ Users user name \\ \\ AppData Local \\ \\ VirtualStore Program Files Company Name \\ Title \\ \\ \\config.ini  
</dl>

Analogamente, se un'applicazione tenta di scrivere un valore del Registro di sistema simile al seguente:

<dl> HKEY \_ LOCAL MACHINE Software Nome società \_ \\ \\ \\ Titolo  
</dl>

verrà reindirizzato invece a:

<dl> HKEY \_ CURRENT \_ USER \\ Software \\ Classes \\ VirtualStore \\ MACHINE \\ Software \\ Company Name \\ Title  
</dl>

I file e le chiavi del Registro di sistema interessati dalla virtualizzazione sono accessibili solo da operazioni di file e registro da applicazioni virtualizzate in esecuzione come utente corrente.

Esistono tuttavia molte restrizioni per la virtualizzazione. Uno è che le applicazioni a 64 bit non vengono mai eseguite in modalità legacy per le operazioni di compatibilità soggette a virtualizzazione nelle applicazioni a 32 bit avranno esito negativo solo a 64 bit. Inoltre, se un'applicazione legacy in esecuzione come utente standard tenta di scrivere qualsiasi tipo di file eseguibile in un percorso che richiede credenziali amministrative, la virtualizzazione non verrà eseguita e la scrittura avrà esito negativo.

**Figura 4. Processo di virtualizzazione**

![processo di virtualizzazione](images/uac-virtualization-process.jpg)

Quando un'applicazione legacy tenta di eseguire un'operazione di lettura in percorsi sensibili al sistema nel file system o nel Registro di sistema, la ricerca viene eseguita per prima nei percorsi virtuali. Se il file o la chiave del Registro di sistema non viene trovata, il sistema operativo accede ai percorsi di sistema predefiniti.

La virtualizzazione verrà rimossa dalle versioni successive Windows quindi è importante non basarsi su questa funzionalità. È invece consigliabile configurare in modo esplicito il manifesto dell'applicazione per privilegi di utente standard o amministrativi, in quanto la virtualizzazione verrà disabilitata. La virtualizzazione non è neanche ovvia per gli utenti finali, quindi anche se la virtualizzazione può consentire l'esecuzione dell'applicazione, può generare chiamate di supporto e rendere difficile la risoluzione dei problemi per questi clienti.

Si noti che se controllo dell'account utente è disabilitato, viene disabilitata anche la virtualizzazione. Se la virtualizzazione è disabilitata, gli account utente standard si comportano esattamente come gli account utente limitati in Windows XP e le applicazioni legacy potrebbero non funzionare correttamente per gli utenti standard che altrimenti avrebbero avuto esito positivo a causa della virtualizzazione.

## <a name="legacy-scenarios-and-manifests"></a>Manifesti e scenari legacy

Per la maggior parte degli scenari di utilizzo, contrassegnare semplicemente il .exe con gli elementi del manifesto di Controllo dell'account utente corretti e verificare che l'applicazione funzioni correttamente come utente standard è sufficiente per garantire un'eccellente compatibilità con il controllo dell'account utente. La maggior parte dei giocatori esegue Windows Vista o Windows 7 con Controllo dell'account utente abilitato. Per Windows XP e gli utenti in Windows Vista o Windows7 con la funzionalità Controllo account utente disabilitata, in genere vengono eseguiti usando account amministratore. Anche se si tratta di una modalità di funzionamento meno sicura, in genere non si verificano problemi di compatibilità aggiuntivi anche se, come indicato in precedenza, la disabilitazione di Controllo dell'account utente disabilita anche la virtualizzazione.

Esiste un caso speciale da notare quando il programma è contrassegnato come "requireAdministrator" nel manifesto di Controllo dell'account utente. In Windows XP e in Windows Vista o Windows 7 con Controllo dell'account utente disabilitato, gli elementi manifesto di Controllo dell'account utente vengono ignorati dal sistema. In questo caso, gli utenti con account amministratore eseguiranno sempre tutti i programmi con diritti di amministratore completi e pertanto questi programmi funzioneranno come previsto. Windows Gli utenti con restrizioni xp e gli utenti standard in esecuzione in Windows Vista o Windows 7, tuttavia, eseguiranno sempre questi programmi con diritti limitati e tutte le operazioni a livello di amministratore avranno esito negativo. È pertanto consigliabile che i programmi contrassegnati come "requiretAdministrator" [**chiamino IsUserAnAdmin**](/windows/win32/api/shlobj_core/nf-shlobj_core-isuseranadmin) all'avvio e visualizzano un messaggio di errore irreversibile se restituisce FALSE. Per lo scenario di maggioranza precedente, questa operazione avrà sempre esito positivo, ma offre un'esperienza utente migliore e un messaggio di errore chiaro per questa rara situazione.

## <a name="conclusion"></a>Conclusione

In quanto sviluppatore di giochi Windows ambiente multi-utente, è fondamentale progettare il gioco in modo che funzioni in modo efficace e responsabile. Il file eseguibile principale del gioco non deve dipendere dai privilegi amministrativi. Ciò non solo impedisce la visualizzazione di richieste di elevazione dei privilegi ogni volta che viene eseguito il gioco, con un impatto negativo sull'esperienza utente complessiva, ma consente anche al gioco di sfruttare altre funzionalità che richiedono l'esecuzione con privilegi utente standard, ad esempio controllo genitori.

Le applicazioni progettate correttamente per funzionare come con le credenziali di un utente standard (o di un utente limitato) nelle versioni precedenti di Windows non saranno interessate dal controllo dell'account utente che verranno eseguite senza elevazione dei privilegi. Tuttavia, devono includere un manifesto con il livello di esecuzione richiesto impostato su "asInvoker" per la conformità agli standard dell'applicazione per Vista.

## <a name="further-reading"></a>Altre informazioni

Per assistenza nella progettazione di applicazioni per Windows Vista conformi a Controllo account utente, scaricare il white paper seguente: [Windows Vista Application Development Requirements for User Account Control Compatibility](/previous-versions/dotnet/articles/bb530410(v=msdn.10)).

Questo white paper procedure dettagliate sul processo di progettazione, insieme a esempi di codice, requisiti e procedure consigliate. Questo documento fornisce anche informazioni dettagliate su aggiornamenti tecnici e modifiche all'esperienza utente in Windows Vista.

Per altre informazioni su Controllo dell'account utente, [Windows Vista: Controllo dell'account utente](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) in [Microsoft TechNet.](https://www.microsoft.com/technet/)

Un'altra risorsa utile è l'articolo [Teach Your Apps To Play Nicely with Windows Vista User Account Control](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control)(Insegnare alle app a riprodurre bene con il controllo dell'account utente di Windows Vista) di [MSDN Magazine](/archive/msdn-magazine/msdn-magazine-issues), gennaio 2007. Questo articolo illustra i problemi generali di compatibilità delle applicazioni, nonché i vantaggi e i problemi relativi all'uso di pacchetti Windows Installer in Windows Vista.

Per altre informazioni sul bug e sulla correzione per mt.exe, lo strumento usato da Visual Studio 2005 per unire e incorporare automaticamente un manifesto in un file eseguibile, vedere [Exploring Manifests Part 2: Default Namespaces and UAC Manifests in Windows Vista](https://techcommunity.microsoft.com/t5/Windows-Blog-Archive/bg-p/Windows-Blog-Archive/2006/09/08/exploring-manifests-part-2-default-namespaces-and-uac-manifests-in-windows-vista/) (Esplorazione dei manifesti parte 2: spazi dei nomi predefiniti e manifesti di Controllo dell'account utente in Windows Vista) nel blog di Chris Michael su [MSDN.](/archive/blogs/)

 

