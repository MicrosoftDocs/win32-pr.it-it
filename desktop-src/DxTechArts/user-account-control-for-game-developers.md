---
title: Controllo dell'account utente per sviluppatori di giochi
description: Questo articolo descrive le linee guida e le procedure consigliate per gli sviluppatori di giochi per lavorare in modo efficace con la funzionalità di sicurezza controllo dell'account utente introdotta in Windows Vista.
ms.assetid: dbac1c07-73dd-f2bc-3c5c-d6160368a88f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d5533a3fbdd349cc25dfde501a234bbd7b05b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399333"
---
# <a name="user-account-control-for-game-developers"></a>Controllo dell'account utente per sviluppatori di giochi

Questo articolo descrive le linee guida e le procedure consigliate per gli sviluppatori di giochi per lavorare in modo efficace con la funzionalità di sicurezza controllo dell'account utente introdotta in Windows Vista.

-   [Panoramica del controllo dell'account utente](#overview-of-user-account-control)
-   [Account utente in Windows Vista](#user-accounts-in-windows-vista)
-   [Accesso ai file come utente standard](#file-access-as-a-standard-user)
-   [Accesso al registro di sistema come utente standard](#registry-access-as-a-standard-user)
-   [Elevazione dei privilegi](#privilege-elevation)
-   [Implicazioni del controllo dell'account utente con CreateProcess ()](#uac-implications-with-createprocess)
-   [Impostazione del livello di esecuzione nel manifesto dell'applicazione](#setting-the-execution-level-in-the-application-manifest)
-   [Incorporamento di un manifesto in Visual Studio](#embedding-a-manifest-in-visual-studio)
-   [Compatibilità UAC con i giochi meno recenti](#uac-compatibility-with-older-games)
-   [Scenari e manifesti legacy](#legacy-scenarios-and-manifests)
-   [Conclusione](#conclusion)
-   [Altre informazioni](#further-reading)

## <a name="overview-of-user-account-control"></a>Panoramica del controllo dell'account utente

Il controllo dell'account utente (UAC), introdotto in Windows Vista, è una funzionalità di sicurezza progettata per impedire agli utenti malintenzionati malintenzionati di usare debolezze o bug rilevati nelle applicazioni di uso comune per modificare il sistema operativo o altri programmi installati. Questa operazione viene eseguita eseguendo la maggior parte dei programmi e dei processi come utente standard (noto anche come utente con limitazioni, utente con restrizioni o utente Least-Privileged) anche se l'account dell'utente corrente dispone di credenziali amministrative. Un processo con privilegi utente standard presenta molte restrizioni intrinseche che impediscono di apportare modifiche a livello di sistema.

Il controllo dell'account utente è inoltre responsabile dell'elevazione dei privilegi di un processo mediante l'utilizzo di uno schema di autenticazione basato su finestra di dialogo avviato durante l'esecuzione di determinati processi designati come che richiedono privilegi amministrativi. L'elevazione dei privilegi consente agli amministratori di eseguire la maggior parte delle applicazioni a un livello di privilegio sicuro (uguale a qualsiasi altro utente standard), ma anche i processi e le operazioni che richiedono privilegi amministrativi. Il controllo dell'account utente supporta l'autenticazione basata sulla spalla, in modo che un amministratore possa concedere privilegi elevati a un programma mentre un utente standard è attualmente connesso al sistema.

La funzionalità controllo dell'account utente è abilitata per impostazione predefinita. Sebbene sia possibile per un amministratore disabilitare l'UAC a livello di sistema, questa operazione ha una serie di ramificazioni negative. In primo luogo, in questo modo si indebolisce la sicurezza di tutti gli account amministrativi, poiché tutti i processi vengono eseguiti con credenziali amministrative, anche quando la maggior parte delle applicazioni non le richiede. Con UAC disabilitato, un'applicazione utente standard che espone una vulnerabilità sfruttabile nella sicurezza può essere potenzialmente utilizzata per rubare informazioni private, installare rootkit o spyware, eliminare l'integrità del sistema o ospitare attacchi zombie su altri sistemi. Mentre con UAC abilitato, l'esecuzione della maggior parte del software come utente standard limita notevolmente i potenziali danni da tale bug. In secondo luogo, la disattivazione del controllo dell'account utente disabilita molte soluzioni alternative per la compatibilità delle applicazioni che consentono agli utenti reali di eseguire correttamente un'ampia gamma di applicazioni. La disabilitazione di UAC non dovrebbe mai essere consigliata come soluzione alternativa per la compatibilità.

È importante tenere presente che, se possibile, le applicazioni devono essere in grado di utilizzare solo diritti utente standard. Sebbene gli amministratori possano facilmente elevare i privilegi di un processo, l'elevazione richiede comunque l'interazione dell'utente e il riconoscimento ogni volta che viene eseguita un'applicazione che richiede credenziali amministrative. Questa elevazione deve essere eseguita anche al momento dell'avvio del programma, quindi la richiesta di credenziali amministrative anche per una singola operazione richiede l'esposizione del sistema a un rischio maggiore per l'intero tempo di esecuzione dell'applicazione. Anche gli utenti standard senza alcuna possibilità di elevare i propri privilegi sono comuni nelle impostazioni di famiglia e business. "Esegui come amministratore" non è una soluzione efficace per la compatibilità, espone l'utente e il sistema a un maggiore rischio di sicurezza e crea frustrazione per gli utenti in molte situazioni.

> [!Note]  
> La funzionalità di controllo dell'account utente introdotta in Windows Vista è disponibile anche in Windows 7. Anche se l'esperienza utente che lavora con le varie funzionalità del sistema è stata migliorata rispetto al controllo dell'account utente, l'effetto sulle applicazioni è fondamentalmente lo stesso. Tutte le raccomandazioni di Windows Vista in questo articolo si applicano anche a Windows 7. Per informazioni dettagliate sulle modifiche dell'interfaccia utente del controllo dell'account utente per Windows 7, vedere [interfaccia utente-aggiornamenti della finestra di dialogo controllo dell'account utente](../win7appqual/user-interface---user-account-control-dialog-updates.md).

 

## <a name="user-accounts-in-windows-vista"></a>Account utente in Windows Vista

Windows Vista suddivide ogni utente in due tipi di account utente: amministratori e utenti standard.

Un account utente standard è simile a un account utente con limitazioni in Windows XP. Come in Windows XP, un utente standard non può scrivere nella cartella programmi, non è in grado di scrivere \_ nella \_ parte del registro di sistema HKEY locale e non può eseguire attività che modificano il sistema, ad esempio l'installazione di un driver in modalità kernel o l'accesso agli spazi dei processi a livello di sistema.

L'account Administrator è stato modificato in modo significativo da quando è stato rilasciato Windows XP. In precedenza, a tutti i processi avviati da un membro del gruppo Administrators venivano assegnati privilegi amministrativi. Con UAC abilitato, tutti i processi vengono eseguiti con privilegi utente standard, a meno che non siano espressamente elevati da un amministratore. Questa differenza rende più sicuri gli account nel gruppo Administrators, riducendo i rischi per la sicurezza causati da potenziali bug nella maggior parte dei programmi.

È importante che tutte le applicazioni, in particolare i giochi, funzionino in modo efficace e responsabile quando vengono eseguite come processo utente standard. Tutte le operazioni che richiedono privilegi amministrativi devono essere eseguite in fase di installazione o da programmi ausiliari che richiedono in modo esplicito le credenziali amministrative. Anche se l'elevazione dei privilegi è piuttosto semplice per un membro del gruppo Administrators, gli utenti standard devono rinviare a un utente con credenziali amministrative per immettere fisicamente la password per elevare i privilegi. Poiché gli account protetti da controlli padre devono essere utenti standard, si tratta di una situazione molto comune per i giocatori che usano Windows Vista.

Se il gioco è già in esecuzione in Windows XP con account utente limitati, il passaggio al controllo dell'account utente in Windows Vista dovrebbe essere molto semplice. La maggior parte di tali applicazioni funzionerà così com'è, anche se è consigliabile aggiungere un manifesto dell'applicazione. I manifesti sono descritti più avanti in questo argomento in [impostazione del livello di esecuzione nel manifesto dell'applicazione](#setting-the-execution-level-in-the-application-manifest).

## <a name="file-access-as-a-standard-user"></a>Accesso ai file come utente standard

L'aspetto del gioco più interessato dalle restrizioni degli utenti standard è file system organizzazione e l'accessibilità. Non presupporre mai che il gioco possa scrivere file nella cartella in cui è installato il gioco. In Windows Vista, ad esempio, è necessario che i privilegi utente siano elevati dal sistema operativo prima che un'applicazione possa scrivere nella cartella programmi. Per evitare questo problema, è necessario categorizzare i file di dati del gioco in base all'ambito e all'accessibilità e usare la funzione [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) , insieme alle costanti CSIDL fornite dalla shell di Windows, per generare i percorsi di file appropriati. Le costanti CSIDL corrispondono a cartelle note nel file system usato dal sistema operativo e promuove la partizione di file globali e specifici dell'utente.

Il tentativo di creare o scrivere un file o una directory in una cartella che non concede l'autorizzazione di scrittura al processo avrà esito negativo in Windows Vista se l'applicazione non dispone di privilegi amministrativi. Se il file eseguibile del gioco a 32 bit viene eseguito in modalità legacy, perché non dichiara un livello di esecuzione richiesto, le operazioni di scrittura avranno esito positivo, ma saranno soggette alla virtualizzazione, come descritto nella sezione "compatibilità UAC con i giochi meno recenti" più avanti in questo articolo.

**Tabella 1. Cartelle note**



| Nome CSIDL             | Percorso tipico (Windows Vista)                                                   | Diritti utente standard | Diritti di amministratore | Ambito di accesso | Descrizione                                                                                                                      | Esempi                                                          |
|------------------------|--------------------------------------------------------------------------------|----------------------|----------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| CSIDL \_ personale        | C: \\ utenti \\ nome utente \\ documenti                                                | Lettura/Scrittura           | Lettura/Scrittura           | Per-User     | File di giochi specifici dell'utente che vengono letti e modificati e possono essere modificati all'esterno del contesto del gioco.                          | Schermate. File di gioco salvati con un'associazione di estensione di file. |
| \_AppData locale \_ CSIDL  | C: \\ utenti \\ nome utente \\ AppData \\ locale                                           | Lettura/Scrittura           | Lettura/Scrittura           | Per-User     | File di gioco specifici dell'utente che vengono letti e modificati e che vengono usati solo nel contesto del gioco.                                 | File della cache dei giochi. Configurazioni del lettore.                          |
| CSIDL \_ Common \_ AppData | C: \\ ProgramData                                                                | Lettura/scrittura se il proprietario  | Lettura/Scrittura           | Tutti gli utenti    | File del gioco che possono essere creati da un utente e letti da tutti gli utenti. L'accesso in scrittura viene concesso solo al creatore del file (proprietario). | Profili utente                                                     |
| \_file di programma CSIDL \_  | C: \\ programmi<br/> oppure<br/> C: \\ programmi (x86) <br/> | Sola lettura            | Lettura/Scrittura           | Tutti gli utenti    | File di gioco statici scritti dal programma di installazione di Game s che vengono letti da tutti gli utenti.                                                    | Asset del gioco, ad esempio materiali e mesh.                        |



 

Il gioco viene in genere installato in una cartella sotto la cartella rappresentata dalla \_ costante dei file di programma CSIDL \_ . Questo meccanismo non viene, tuttavia, sempre applicato. È invece consigliabile usare un percorso relativo dal file eseguibile quando si generano stringhe di percorso in file o directory che si trovano nella cartella di installazione.

Si consiglia inoltre di evitare i presupposti hardcoded sui percorsi di cartella noti. Ad esempio, in Windows XP Professional 64-bit Edition e Windows Vista x64, il percorso dei file di programma è C: \\ programmi (x86) per i programmi a 32 bit e c: programmi \\ per programmi a 64 bit. Questi percorsi noti vengono modificati da Windows XP e gli utenti possono riconfigurare il percorso di molte di queste cartelle e persino individuarle in unità diverse. Usare sempre le costanti CSIDL per evitare confusione e potenziali problemi. Installazione di Windows riconosce questi percorsi di cartelle note e sposta i dati quando si aggiorna il sistema operativo da Windows XP; al contrario, l'uso di posizioni non standard o di percorsi hardcoded potrebbe non riuscire dopo un aggiornamento del sistema operativo.

È necessario prestare attenzione alle minime differenze di usabilità tra le cartelle specifiche dell'utente specificate da CSIDL \_ Personal e CSIDL \_ Local \_ AppData. La procedura consigliata per selezionare la costante CSIDL da usare per la scrittura di un file consiste nell'usare CSIDL \_ Personal se si prevede che l'utente interagisca con il file, ad esempio facendo doppio clic su di esso per aprirlo in uno strumento o in un'applicazione e usare CSIDL \_ Local \_ AppData per altri file. Entrambe le cartelle possono essere utilizzate dall'applicazione per archiviare e organizzare i file di dati specifici dell'utente, in quanto non esiste alcuna differenza nel loro ambito di accesso o livello di privilegio. È necessario prestare attenzione per creare nomi di percorso sufficientemente univoci da non essere in conflitto con altre applicazioni, ma sufficientemente breve da contenere il numero di caratteri nel percorso completo inferiore al valore di MAX \_ path, 260.

Il codice seguente fornisce un esempio di come scrivere un file in una cartella Nota:

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

## <a name="registry-access-as-a-standard-user"></a>Accesso al registro di sistema come utente standard

L'accesso al registro di sistema da parte di un utente standard viene limitato in modo analogo al file system. Un utente standard è autorizzato ad accedere in lettura a tutte le chiavi nel registro di sistema. Tuttavia, l'accesso in scrittura viene concesso solo al \_ \_ sottoalbero HKEY Current User (HKCU), mappato internamente alla sottochiave specifica dell'utente HKEY Users \_ \\ ID di sicurezza (SID) dell'utente corrente. Un'applicazione che deve scrivere in un percorso del registro di sistema diverso \_ dall'utente corrente di HKEY \_ richiede privilegi amministrativi.

Se l'applicazione a 32 bit non contiene un livello di esecuzione richiesto nel manifesto, tutte le scritture nel \_ software del \_ computer locale HKEY \\ verranno virtualizzate, mentre le Scritture in altre posizioni all'esterno dell' \_ utente corrente di HKEY \_ avranno esito negativo.

Non è consigliabile archiviare dati persistenti nel registro di sistema, ad esempio la configurazione di un utente. Il metodo preferito per archiviare i dati persistenti dal gioco consiste nel scrivere i dati nel file system chiamando [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) e ottenere il valore di una costante CSIDL, descritto nella sezione precedente.

## <a name="privilege-elevation"></a>Elevazione dei privilegi

In Windows Vista, qualsiasi applicazione che richiede privilegi amministrativi deve dichiarare una richiesta di un livello di esecuzione amministrativa nel relativo manifesto (descritto nella sezione successiva [impostazione del livello di esecuzione nel manifesto dell'applicazione](#setting-the-execution-level-in-the-application-manifest)).

L'elevazione dei privilegi, come è noto, è la procedura gestita da UAC per promuovere un processo a un processo amministrativo. I privilegi di un processo possono essere elevati solo in fase di creazione. Una volta creato, un processo non verrà mai promosso a un livello di privilegi più elevato. Per questo motivo. le operazioni che richiedono credenziali amministrative devono essere isolate per separare i programmi di installazione e altri programmi ausiliari.

Al momento dell'esecuzione di un programma, il controllo dell'account utente controlla il livello di esecuzione richiesto nel manifesto e, se sono necessari privilegi elevati, richiede all'utente corrente una delle due finestre di dialogo standard: una per un utente standard e una per un amministratore.

Se l'utente corrente è un utente standard, il controllo dell'account utente richiede le credenziali di un amministratore prima di consentire l'esecuzione del programma.

**Figura 1. Richiedi a un utente standard di immettere le credenziali per un account amministrativo**

![Richiedi a un utente standard di immettere le credenziali per un account amministrativo](images/uac-prompt-elevation.jpg)

Se l'utente corrente è un amministratore, il controllo dell'account utente richiede l'autorizzazione dell'utente prima di consentire l'esecuzione del programma.

**Figura 2. Richiedere a un amministratore di autorizzare le modifiche al computer**

![richiedere a un amministratore di autorizzare le modifiche al computer](images/uac-prompt-authorization.jpg)

All'applicazione verranno concessi solo i privilegi amministrativi se un utente standard fornisce le credenziali amministrative corrette oppure un utente amministratore fornisce il riconoscimento; qualsiasi altra operazione causerà l'interruzione dell'applicazione.

È importante notare che un processo con privilegi elevati viene eseguito come utente amministratore che ha immesso le credenziali nella richiesta UAC anziché come utente standard attualmente connesso. Questa operazione è simile a **RunAs** in Windows XP. il processo con privilegi elevati ottiene la cartella dell'amministratore e le chiavi del registro di sistema durante l'accesso ai dati per utente e tutti i programmi avviati dal processo con privilegi elevati ereditano anche i diritti amministrativi e le posizioni degli account utente. Per gli amministratori che riceveranno la richiesta di riconoscimento (**continua** o **Annulla**), questi percorsi corrisponderanno alle località dell'utente corrente. In generale, tuttavia, i processi che richiedono l'elevazione non devono funzionare sui dati per utente. Si noti che questo può influire sostanzialmente sulla modalità di funzionamento del programma di installazione. Se il programma di installazione, eseguito come amministratore, scrive in HKCU o nel profilo di un utente, potrebbe essere molto corretto scrivere nel percorso errato. Si consiglia di creare questi valori per utente alla prima esecuzione del gioco.

## <a name="uac-implications-with-createprocess"></a>Implicazioni del controllo dell'account utente con CreateProcess ()

Il meccanismo di elevazione del controllo dell'account utente non verrà richiamato da una chiamata alla funzione Win32 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)() per avviare un eseguibile configurato in modo da richiedere un livello di esecuzione superiore rispetto al processo corrente. Di conseguenza, la chiamata a **CreateProcess**() avrà esito negativo con [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)() che restituisce l'elevazione degli errori \_ \_ necessaria. **CreateProcess**() avrà esito positivo solo se il livello di esecuzione del chiamato è uguale o minore di quello del chiamante. Un processo non con privilegi elevati che deve generare processi con privilegi elevati dovrebbe farlo utilizzando la funzione [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)(), che determina l'attivazione del meccanismo di elevazione del controllo dell'account utente tramite la Shell.

## <a name="setting-the-execution-level-in-the-application-manifest"></a>Impostazione del livello di esecuzione nel manifesto dell'applicazione

Per dichiarare il livello di esecuzione richiesto del gioco è necessario aggiungere un'estensione al manifesto dell'applicazione. Nel codice XML seguente viene illustrata la configurazione minima necessaria per impostare il livello di esecuzione per un'applicazione:

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

Nel codice precedente, il sistema operativo viene informato che il gioco richiede solo privilegi utente standard con il seguente tag:

``` syntax
<ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
```

Impostando in modo esplicito requestedExecutionLevel su "asInvoker", questo esempio dichiara al sistema operativo che il gioco si comporterà correttamente senza privilegi amministrativi. Di conseguenza, UAC Disabilita la virtualizzazione ed esegue il gioco con gli stessi privilegi dell'invoker, che in genere è privilegi utente standard, perché Esplora risorse viene eseguito come utente standard.

Il sistema operativo può essere informato che un gioco richiede l'elevazione dei privilegi amministrativi sostituendo "asInvoker" con "requireAdministrator" per creare il tag seguente:

``` syntax
<ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
```

Con questa configurazione, il sistema operativo chiede all'utente corrente una delle finestre di dialogo di elevazione del controllo dell'account utente standard ogni volta che viene eseguito il gioco. È consigliabile che nessun gioco richieda privilegi di amministratore per l'esecuzione, perché non solo questa finestra di dialogo diventa fastidiosa, ma rende anche il gioco incompatibile con i controlli padre. Valutare attentamente prima di aggiungere questo requisito a qualsiasi eseguibile.

Un malinteso comune è che l'aggiunta di un manifesto che imposta requestedExecutionLevel su "requireAdministrator" Ignora la necessità di una richiesta di elevazione dei privilegi. Risposta errata. Impedisce semplicemente al sistema operativo di indovinare se l'applicazione di installazione o aggiornamento necessita di privilegi amministrativi. All'utente viene comunque richiesto di autorizzare l'elevazione dei privilegi.

Windows controlla la firma di qualsiasi applicazione contrassegnata per l'elevazione dei privilegi prima di visualizzare il prompt di controllo dell'account utente. Un file eseguibile di grandi dimensioni contrassegnato per l'elevazione dei privilegi richiede più tempo rispetto a un file eseguibile di piccole dimensioni e più lungo di un file eseguibile contrassegnato come "asInvoker". Gli eseguibili di installazione autoestraenti dovrebbero pertanto essere contrassegnati come "asInvoker" e qualsiasi parte che deve essere contrassegnata come "requireAdministrator" deve essere inserita in un eseguibile di helper separato.

L'attributo uiAccess, illustrato negli esempi precedenti, deve sempre essere FALSE per i giochi. Questo attributo specifica se i client di automazione interfaccia utente hanno accesso all'interfaccia utente del sistema protetto e presenta implicazioni di sicurezza speciali se impostate su TRUE.

## <a name="embedding-a-manifest-in-visual-studio"></a>Incorporamento di un manifesto in Visual Studio

Il supporto del manifesto è stato aggiunto per la prima volta a Visual Studio a partire da VS2005. Per impostazione predefinita, un file eseguibile compilato in Visual Studio 2005 (o versione successiva) avrà un manifesto generato automaticamente incorporato nell'ambito del processo di compilazione. Il contenuto del manifesto generato automaticamente dipende da determinate configurazioni di progetto specificate nella finestra di dialogo delle proprietà del progetto.

Il manifesto generato automaticamente da Visual Studio 2005 non conterrà un <trustInfo> blocco poiché non esiste alcun modo per configurare il livello di esecuzione del controllo dell'account utente nelle proprietà del progetto. Il modo migliore per aggiungere queste informazioni consiste nel consentire a VS2005 di unire un manifesto definito dall'utente contenente il <trustInfo> blocco con il manifesto generato automaticamente. Questa operazione è semplice quanto l'aggiunta \* di un file con estensione manifest alla soluzione che contiene il codice XML riportato nella sezione precedente. Quando Visual Studio rileva un file con estensione manifest nella soluzione, richiamerà automaticamente lo strumento Manifesto (mt.exe) per unire i file. manifest con quello generato automaticamente.

> [!Note]  
> È presente un bug nello strumento Manifesto (mt.exe) fornito da Visual Studio 2005 che produce un manifesto Unito e incorporato che può causare problemi quando il file eseguibile viene eseguito in Windows XP prima di SP3. Il bug è il risultato del modo in cui lo strumento ridefinisce lo spazio dei nomi predefinito alla dichiarazione del <trustInfo> blocco. Fortunatamente, è facile ignorare completamente il problema dichiarando in modo esplicito uno spazio dei nomi diverso nel <trustInfo> blocco e definendo l'ambito dei nodi figlio al nuovo spazio dei nomi. Il codice XML fornito nella sezione precedente illustra questa correzione.

 

Un avvertimento nell'uso dello strumento mt.exe incluso in Visual Studio 2005 è che genererà un avviso durante l'elaborazione del <trustInfo> blocco poiché lo strumento non contiene uno schema aggiornato per convalidare l'XML. Per risolvere il problema, è consigliabile sostituire tutti i file mt.exe nella directory di installazione di Visual Studio 2005 (sono presenti più istanze) con il mt.exe fornito nella Windows SDK più recente.

A partire da Visual Studio 2008, è ora possibile specificare il livello di esecuzione di un'applicazione nella finestra di dialogo delle proprietà del progetto (Figura 3) o usando il flag del linker/MANIFESTUAC. L'impostazione di queste opzioni causerà la generazione automatica e l'incorporamento di un manifesto con il <trustInfo> blocco appropriato nell'eseguibile da parte di Visual Studio 2008.

**Figura 3. Impostazione del livello di esecuzione in Visual Studio 2008**

![impostazione del livello di esecuzione in Visual Studio 2008](images/setting-execution-level-in-vs2008.jpg)

È ancora possibile incorporare un manifesto in versioni precedenti di Visual Studio senza supporto per il manifesto, ma richiede più lavoro da parte dello sviluppatore. Per un esempio su come eseguire questa operazione, esaminare il progetto di Visual Studio 2003 incluso in qualsiasi esempio in DirectX SDK prima della versione di marzo 2008.

## <a name="uac-compatibility-with-older-games"></a>Compatibilità UAC con i giochi meno recenti

Se il gioco sembra salvare e caricare correttamente un file nella directory programmi, ma non si verifica il file iOn Windows Vista, qualsiasi applicazione a 32 bit che non contiene un livello di esecuzione richiesto nel manifesto è considerata un'applicazione legacy. Prima di Windows Vista, la maggior parte delle applicazioni veniva in genere eseguita dagli utenti con privilegi amministrativi. Di conseguenza, queste applicazioni possono leggere e scrivere liberamente i file di sistema e le chiavi del registro di sistema e molti sviluppatori non hanno apportato le modifiche necessarie per funzionare correttamente con account utente limitati in Windows XP. Tuttavia, in Windows Vista, le stesse applicazioni ora hanno esito negativo a causa di privilegi di accesso insufficienti nel nuovo modello di sicurezza, che impone l'esecuzione dell'utente standard per le applicazioni legacy. Per attenuare l'effetto di questo problema, è stata aggiunta anche la virtualizzazione a Windows Vista. Grazie alla virtualizzazione, le migliaia di applicazioni legacy funzionano in modo ottimale in Windows Vista senza che sia necessario che tali applicazioni dispongano di privilegi elevati in qualsiasi momento semplicemente per poter eseguire alcune operazioni secondarie. trovate, è probabile che il gioco sia in esecuzione in modalità legacy ed è stato soggetto alla virtualizzazione.

La virtualizzazione influiscono sul file system e il registro di sistema reindirizzando le Scritture sensibili al sistema (e le successive operazioni del registro di sistema) a una posizione per utente all'interno del profilo dell'utente corrente. Ad esempio, se un'applicazione tenta di scrivere nel file seguente:

<dl> C: \\ Program Files \\ nome società \\ titolo \\config.ini  
</dl>

la scrittura viene reindirizzata automaticamente a:

<dl> C: \\ Users \\ nome utente \\ AppData \\ Local \\ VirtualStore \\ Program Files \\ nome società \\ titolo \\config.ini  
</dl>

Analogamente, se un'applicazione tenta di scrivere un valore del registro di sistema simile al seguente:

<dl> \_ \_ \\ \\ Titolo nome società del software del computer locale HKEY \\  
</dl>

verrà reindirizzato al posto di:

<dl> HKEY \_ \_ \\ le classi software utente corrente \\ \\ VirtualStore \\ Machine \\ software \\ nome società \\ titolo  
</dl>

I file e le chiavi del registro di sistema interessati dalla virtualizzazione sono accessibili solo da operazioni di file e registro di sistema da applicazioni virtualizzate eseguite con l'utente corrente.

Tuttavia, esistono molte restrizioni per la virtualizzazione. Uno è che le applicazioni a 64 bit non vengono mai eseguite in modalità legacy per le operazioni di compatibilità soggette alla virtualizzazione nelle applicazioni a 32 bit riusciranno a funzionare solo a 64 bit. Inoltre, se un'applicazione legacy in esecuzione come utente standard tenta di scrivere qualsiasi tipo di file eseguibile in un percorso che richiede credenziali amministrative, la virtualizzazione non verrà eseguita e la scrittura avrà esito negativo.

**Figura 4. Processo di virtualizzazione**

![processo di virtualizzazione](images/uac-virtualization-process.jpg)

Quando un'applicazione legacy tenta un'operazione di lettura in percorsi sensibili al sistema nel file system o nel registro di sistema, viene eseguita la ricerca per prima delle posizioni virtuali. Se il file o la chiave del registro di sistema non viene trovata, il sistema operativo accede ai percorsi di sistema predefiniti.

La virtualizzazione verrà rimossa dalle versioni successive di Windows, pertanto è importante non affidarsi a questa funzionalità. Al contrario, è necessario configurare in modo esplicito il manifesto dell'applicazione per i privilegi di amministratore o utente standard, in quanto questa operazione Disabilita la virtualizzazione. Anche la virtualizzazione non è ovvia agli utenti finali, quindi anche se la virtualizzazione può consentire l'esecuzione dell'applicazione, può generare chiamate di supporto e renderlo difficile da risolvere per questi clienti.

Si noti che se UAC è disabilitato, anche la virtualizzazione è disabilitata. Se la virtualizzazione è disabilitata, gli account utente standard si comportano esattamente come gli account utente limitati in Windows XP e le applicazioni legacy potrebbero non funzionare correttamente per gli utenti standard che altrimenti avrebbero avuto esito positivo a causa della virtualizzazione.

## <a name="legacy-scenarios-and-manifests"></a>Scenari e manifesti legacy

Per la maggior parte degli scenari di utilizzo, è sufficiente contrassegnare il file con estensione exe con gli elementi del manifesto del controllo dell'account utente corretti e verificare che l'applicazione funzioni correttamente perché un utente standard è sufficiente per la compatibilità con UAC. La maggior parte dei giocatori esegue Windows Vista o Windows 7 con il controllo dell'account utente abilitato. Per Windows XP e gli utenti in Windows Vista o Windows7 con la funzionalità di controllo dell'account utente disabilitata, vengono in genere eseguiti usando gli account amministratore. Sebbene si tratti di una modalità di funzionamento meno sicura, in genere non si verificano problemi di compatibilità aggiuntivi, ma come indicato in precedenza, la disabilitazione di UAC Disabilita anche la virtualizzazione.

Quando il programma è contrassegnato come "requireAdministrator" nel manifesto del controllo dell'account utente, è opportuno notare un particolare caso. In Windows XP e in Windows Vista o Windows 7 con controllo dell'account utente disabilitato, gli elementi manifesto del controllo dell'account utente vengono ignorati dal sistema. In questa situazione, gli utenti con account Administrator eseguiranno sempre tutti i programmi con diritti di amministratore completi, quindi questi programmi funzioneranno come previsto. Gli utenti con restrizioni di Windows XP e gli utenti standard in esecuzione su Windows Vista o Windows 7, tuttavia, eseguiranno sempre questi programmi con diritti limitati e tutte le operazioni a livello di amministratore avranno esito negativo. È pertanto consigliabile che i programmi contrassegnati come "requiretAdministrator" chiamino [**IsUserAnAdmin**](/windows/win32/api/shlobj_core/nf-shlobj_core-isuseranadmin) all'avvio e visualizzino un messaggio di errore irreversibile se restituisce false. Per lo scenario di maggioranza precedente, questo avrà sempre esito positivo, ma offre un'esperienza utente migliore e un messaggio di errore chiaro per questa rara situazione.

## <a name="conclusion"></a>Conclusione

Per gli sviluppatori di giochi che fanno riferimento all'ambiente multiutente di Windows, è fondamentale progettare il gioco per operare in modo efficace e responsabile. Il file eseguibile principale del gioco non deve dipendere dai privilegi amministrativi. Questo non solo impedisce l'aspetto delle richieste di elevazione ogni volta che viene eseguito il gioco, che può influire negativamente sull'esperienza utente complessiva, ma consente anche al gioco di sfruttare le altre funzionalità che richiedono l'esecuzione con privilegi utente standard, ad esempio i controlli padre.

Le applicazioni progettate correttamente per funzionare come con le credenziali di un utente standard (o un utente limitato) nelle versioni precedenti di Windows non saranno interessate dal controllo dell'account utente che verranno eseguite senza elevazione dei privilegi. Tuttavia, devono includere un manifesto con il livello di esecuzione richiesto impostato su "asInvoker" per essere conforme agli standard dell'applicazione per vista.

## <a name="further-reading"></a>Altre informazioni

Per assistenza sulla progettazione di applicazioni per Windows Vista che siano conformi a controllo dell'account utente, scaricare i white paper seguenti: [requisiti per lo sviluppo di applicazioni Windows Vista per la compatibilità con il controllo dell'account utente](/previous-versions/dotnet/articles/bb530410(v=msdn.10)).

In questa white paper vengono illustrati i passaggi dettagliati del processo di progettazione, oltre a esempi di codice, requisiti e procedure consigliate. In questo documento vengono inoltre illustrati in dettaglio gli aggiornamenti tecnici e le modifiche apportate all'esperienza utente in Windows Vista.

Per ulteriori informazioni su controllo dell'account utente, visitare [Windows Vista: controllo dell'account utente](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) in [Microsoft TechNet](https://www.microsoft.com/technet/).

Un'altra risorsa utile è l'articolo [per insegnare alle app di giocare con il controllo dell'account utente di Windows Vista](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control), da [MSDN Magazine](/archive/msdn-magazine/msdn-magazine-issues), 2007 gennaio. In questo articolo vengono illustrati i problemi generali relativi alla compatibilità delle applicazioni, nonché i vantaggi e i problemi correlati all'utilizzo di pacchetti di Windows Installer in Windows Vista.

Per altre informazioni sul bug e la correzione per mt.exe, lo strumento usato da Visual Studio 2005 per unire automaticamente e incorporare un manifesto in un eseguibile, vedere l'articolo relativo all' [esplorazione dei manifesti parte 2: spazi dei nomi predefiniti e manifesti UAC in Windows Vista](https://techcommunity.microsoft.com/t5/Windows-Blog-Archive/bg-p/Windows-Blog-Archive/2006/09/08/exploring-manifests-part-2-default-namespaces-and-uac-manifests-in-windows-vista/) nel Blog di Chris Jackson su [MSDN](/archive/blogs/).

 

