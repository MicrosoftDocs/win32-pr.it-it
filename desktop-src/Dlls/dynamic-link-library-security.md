---
description: Quando un'applicazione carica dinamicamente una libreria a collegamento dinamico senza specificare un nome di percorso completo, Windows tenta di individuare la DLL eseguendo una ricerca in un set ben definito di directory in un ordine specifico, come descritto in Ordine di ricerca nella libreria di Dynamic-Link. Se un utente malintenzionato ottiene il controllo di una delle directory nel percorso di ricerca della DLL, può inserire una copia dannosa della DLL in tale directory. Questo tipo di attacco viene talvolta definito attacco di precaricamento di DLL o binary planting attacco.
ms.assetid: 9493F299-789D-4CBC-9822-96EEAE39B494
title: Dynamic-Link della libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582122debce68ade593c007e431e62a91a7fa07f395f148b7eaa05cac13bc56a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290401"
---
# <a name="dynamic-link-library-security"></a>Dynamic-Link della libreria

Quando un'applicazione carica dinamicamente una libreria a collegamento dinamico senza specificare un nome di percorso completo, Windows tenta di individuare la DLL eseguendo una ricerca in un set ben definito di directory in un ordine specifico, come descritto in [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md). Se un utente malintenzionato ottiene il controllo di una delle directory nel percorso di ricerca della DLL, può inserire una copia dannosa della DLL in tale directory. Questo tipo di attacco viene talvolta *definito attacco di precaricamento di DLL* o binary planting attacco *.* Se il sistema non trova una copia legittima della DLL prima di eseguire la ricerca nella directory compromessa, carica la DLL dannosa. Se l'applicazione viene eseguita con privilegi di amministratore, l'utente malintenzionato potrebbe riuscire a eseguire l'elevazione dei privilegi locale.

Si supponga, ad esempio, che un'applicazione sia progettata per caricare una DLL dalla directory corrente dell'utente e non riesca correttamente se la DLL non viene trovata. L'applicazione [**chiama LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) solo con il nome della DLL, che fa in modo che il sistema esequisi la DLL. Supponendo che sia abilitata la modalità di ricerca DLL sicura e che l'applicazione non utilizzi un ordine di ricerca alternativo, il sistema esegue la ricerca nelle directory nell'ordine seguente:

1.  Directory da cui è stata caricata l'applicazione.
2.  Directory di sistema.
3.  Directory di sistema a 16 bit.
4.  Directory Windows.
5.  La directory corrente.
6.  Directory elencate nella variabile di ambiente PATH.

Continuando l'esempio, un utente malintenzionato con conoscenza dell'applicazione ottiene il controllo della directory corrente e inserisce una copia dannosa della DLL in tale directory. Quando l'applicazione esegue **la chiamata a LoadLibrary,** il sistema cerca la DLL, trova la copia dannosa della DLL nella directory corrente e la carica. La copia dannosa della DLL viene quindi eseguita all'interno dell'applicazione e ottiene i privilegi dell'utente.

Gli sviluppatori possono proteggere le applicazioni dagli attacchi di precaricamento delle DLL seguendo queste linee guida:

-   Laddove possibile, specificare un percorso completo quando si usano le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa), [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)o [**ShellExecute.**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea)
-   Usare i flag LOAD LIBRARY SEARCH con la funzione LoadLibraryEx oppure usare questi flag con la funzione \_ \_ [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) per stabilire un ordine di ricerca dll per un processo e quindi usare le funzioni [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) o [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) [](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) per modificare l'elenco. Per altre informazioni, vedere [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).

    **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Questi flag e funzioni sono disponibili nei sistemi in cui è installato [KB2533623.](https://support.microsoft.com/kb/2533623)

-   Nei sistemi in cui è installato [KB2533623](https://support.microsoft.com/kb/2533623) usare i flag LOAD LIBRARY SEARCH con la funzione LoadLibraryEx oppure usare questi flag con la \_ funzione \_ [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) [](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) per stabilire un ordine di ricerca dll per un processo e quindi usare le funzioni [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) [**o SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) per modificare l'elenco. Per altre informazioni, vedere [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).
-   È [consigliabile usare il reindirizzamento DLL](dynamic-link-library-redirection.md) o [un manifesto](/windows/desktop/SbsCs/manifests) per assicurarsi che l'applicazione usi la DLL corretta.
-   Quando si usa l'ordine di ricerca standard, assicurarsi che sia abilitata la modalità di ricerca dll sicura. In questo modo la directory corrente dell'utente viene posta in un secondo momento nell'ordine di ricerca, aumentando le probabilità che Windows trovi una copia legittima della DLL prima di una copia dannosa. Cassaforte La modalità di ricerca DLL è abilitata per impostazione predefinita a partire da Windows XP con Service Pack 2 (SP2) ed è controllata dal valore del Registro di sistema **\_ HKEY LOCAL \_ MACHINE System \\ \\ CurrentControlSet \\ Control Session \\ Manager** \\ **SafeDllSearchMode.** Per altre informazioni, vedere [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).
-   Provare a rimuovere la directory corrente dal percorso di ricerca standard chiamando [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) con una stringa vuota (""). Questa operazione deve essere eseguita una volta all'inizio dell'inizializzazione del processo, non prima e dopo le chiamate a [**LoadLibrary.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) Tenere presente che **SetDllDirectory influisce** sull'intero processo e che più thread che chiamano **SetDllDirectory** con valori diversi possono causare un comportamento indefinito. Se l'applicazione carica DLL di terze parti, eseguire un test con attenzione per identificare eventuali incompatibilità.
-   Non usare la funzione [**SearchPath per**](/windows/desktop/api/processenv/nf-processenv-searchpathw) recuperare un percorso a una DLL per una chiamata [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) successiva, a meno che non sia abilitata la modalità di ricerca del processo sicuro. Quando la modalità di ricerca del processo sicuro non è abilitata, la funzione **SearchPath** usa un ordine di ricerca diverso rispetto a **LoadLibrary** ed è probabile che la DLL specificata sia stata cercata prima nella directory corrente dell'utente. Per abilitare la modalità di ricerca di processi sicuri per la **funzione SearchPath,** usare la [**funzione SetSearchPathMode**](/windows/desktop/api/winbase/nf-winbase-setsearchpathmode) con BASE \_ SEARCH PATH ENABLE SAFE \_ \_ \_ \_ SEARCHMODE. La directory corrente viene spostata alla fine dell'elenco di ricerca **SearchPath** per tutta la durata del processo. Si noti che la directory corrente non viene rimossa dal percorso di ricerca, quindi se il sistema non trova una copia legittima della DLL prima che raggiunga la directory corrente, l'applicazione è ancora vulnerabile. Come con [**SetDllDirectory, la**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) **chiamata a SetSearchPathMode** deve essere eseguita all'inizio dell'inizializzazione del processo e influisce sull'intero processo. Se l'applicazione carica DLL di terze parti, eseguire un test con attenzione per identificare eventuali incompatibilità.
-   Non fare ipotesi sulla versione del sistema operativo in base a una chiamata [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) che cerca una DLL. Se l'applicazione è in esecuzione in un ambiente in cui la DLL non è legittimamente presente ma una copia dannosa della DLL si trova nel percorso di ricerca, è possibile che venga caricata la copia dannosa della DLL. Usare invece le tecniche consigliate descritte in [Ottenere la versione del sistema](/windows/desktop/SysInfo/getting-the-system-version).

Lo strumento Monitoraggio processi può essere usato per identificare le operazioni di caricamento dll che potrebbero essere vulnerabili. Lo strumento Monitoraggio processi può essere scaricato da <https://technet.microsoft.com/sysinternals/bb896645.aspx> .

La procedura seguente descrive come usare Monitoraggio processi per esaminare le operazioni di caricamento dll nell'applicazione.

**Per usare Monitoraggio processi per esaminare le operazioni di caricamento dll nell'applicazione**

1.  Avviare Monitoraggio processo.
2.  In Monitoraggio processi includere i filtri seguenti:
    -   L'operazione è CreateFile
    -   L'operazione è LoadImage
    -   Il percorso contiene .cpl
    -   Il percorso contiene .dll
    -   Il percorso contiene .drv
    -   Il percorso contiene .exe
    -   Il percorso contiene .ocx
    -   Il percorso contiene .scr
    -   Il percorso contiene .sys
3.  Escludere i filtri seguenti:
    -   Il nome del processo è procmon.exe
    -   Il nome del processo è Procmon64.exe
    -   Il nome del processo è System
    -   L'operazione inizia con MJ IRP \_\_
    -   L'operazione inizia con FASTIO\_
    -   Il risultato è SUCCESS
    -   Il percorso termina con pagefile.sys
4.  Provare ad avviare l'applicazione con la directory corrente impostata su una directory specifica. Ad esempio, fare doppio clic su un file con un'estensione il cui gestore di file è assegnato all'applicazione.
5.  Controllare l'output di Process Monitor per i percorsi che sembrano sospetti, ad esempio una chiamata alla directory corrente per caricare una DLL. Questo tipo di chiamata potrebbe indicare una vulnerabilità nell'applicazione.

 

 
