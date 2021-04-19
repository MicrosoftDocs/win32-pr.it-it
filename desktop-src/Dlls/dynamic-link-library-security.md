---
description: Quando un'applicazione carica dinamicamente una libreria a collegamento dinamico senza specificare un nome di percorso completo, Windows tenta di individuare la DLL eseguendo una ricerca in un set di directory ben definito in un ordine specifico, come descritto in Dynamic-Link ordine di ricerca della libreria. Se un utente malintenzionato ottiene il controllo di una delle directory nel percorso di ricerca della DLL, può inserire una copia dannosa della DLL in tale directory. Questa operazione viene a volte definita attacco di precaricamento DLL o attacco binary planting.
ms.assetid: 9493F299-789D-4CBC-9822-96EEAE39B494
title: Sicurezza della libreria Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4016139762461784702ac0190c1ee65d8bc6e72d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317818"
---
# <a name="dynamic-link-library-security"></a>Sicurezza della libreria Dynamic-Link

Quando un'applicazione carica dinamicamente una libreria a collegamento dinamico senza specificare un nome di percorso completo, Windows tenta di individuare la DLL eseguendo una ricerca in un set di directory ben definito in un ordine specifico, come descritto in [ordine di ricerca nella libreria a collegamento dinamico](dynamic-link-library-search-order.md). Se un utente malintenzionato ottiene il controllo di una delle directory nel percorso di ricerca della DLL, può inserire una copia dannosa della DLL in tale directory. Questa operazione viene a volte definita *attacco di precaricamento dll* o *attacco Binary planting*. Se il sistema non trova una copia legittima della DLL prima di eseguire ricerche nella directory compromessa, carica la DLL dannosa. Se l'applicazione è in esecuzione con privilegi di amministratore, l'utente malintenzionato potrebbe avere esito positivo nell'elevazione dei privilegi locali.

Si supponga, ad esempio, che un'applicazione sia progettata per caricare una DLL dalla directory corrente dell'utente e abbia esito negativo correttamente se la DLL non viene trovata. L'applicazione chiama [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) solo con il nome della dll, che determina la ricerca della dll da parte del sistema. Supponendo che la modalità di ricerca DLL sicura sia abilitata e che l'applicazione non usi un ordine di ricerca alternativo, il sistema cerca le directory nell'ordine seguente:

1.  Directory da cui è stata caricata l'applicazione.
2.  Directory di sistema.
3.  Directory di sistema a 16 bit.
4.  Directory di Windows.
5.  La directory corrente.
6.  Directory elencate nella variabile di ambiente PATH.

Continuando l'esempio, un utente malintenzionato con conoscenza dell'applicazione acquisisce il controllo della directory corrente e inserisce una copia dannosa della DLL in tale directory. Quando l'applicazione emette la chiamata a **LoadLibrary** , il sistema cerca la dll, individua la copia dannosa della dll nella directory corrente e la carica. La copia dannosa della DLL viene quindi eseguita all'interno dell'applicazione e ottiene i privilegi dell'utente.

Gli sviluppatori possono contribuire a proteggere le proprie applicazioni dagli attacchi di precaricamento DLL attenendosi alle seguenti linee guida:

-   Laddove possibile, specificare un percorso completo quando si utilizzano le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa), [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)o [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) .
-   Usare i flag di ricerca di LOAD \_ Library \_ con la funzione [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) oppure usare questi flag con la funzione [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) per stabilire un ordine di ricerca dll per un processo e quindi usare le funzioni [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) o [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) per modificare l'elenco. Per ulteriori informazioni, vedere l' [ordine di ricerca della libreria a collegamento dinamico](dynamic-link-library-search-order.md).

    **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questi flag e funzioni sono disponibili nei sistemi in cui è installato [KB2533623](https://support.microsoft.com/kb/2533623) .

-   Nei sistemi in cui è installato [KB2533623](https://support.microsoft.com/kb/2533623) usare i \_ flag di ricerca di Load Library \_ con la funzione [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) oppure usare questi flag con la funzione [**SETDEFAULTDLLDIRECTORIES**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) per stabilire un ordine di ricerca dll per un processo e quindi usare le funzioni [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) o [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) per modificare l'elenco. Per ulteriori informazioni, vedere l' [ordine di ricerca della libreria a collegamento dinamico](dynamic-link-library-search-order.md).
-   Si consiglia di usare il [Reindirizzamento dll](dynamic-link-library-redirection.md) o un [manifesto](/windows/desktop/SbsCs/manifests) per assicurarsi che l'applicazione usi la DLL corretta.
-   Quando si usa l'ordine di ricerca standard, verificare che la modalità di ricerca DLL sicura sia abilitata. In questo modo la directory corrente dell'utente viene posizionata in un secondo momento nell'ordine di ricerca, aumentando la probabilità che Windows trovi una copia legittima della DLL prima di una copia dannosa. La modalità di ricerca delle dll sicure è abilitata per impostazione predefinita a partire da Windows XP con Service Pack 2 (SP2) ed è controllata dal valore del registro di **\_ sistema HKEY LOCAL \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager** \\ **SafeDllSearchMode** . Per ulteriori informazioni, vedere l' [ordine di ricerca della libreria a collegamento dinamico](dynamic-link-library-search-order.md).
-   Provare a rimuovere la directory corrente dal percorso di ricerca standard chiamando [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) con una stringa vuota (""). Questa operazione deve essere eseguita una volta all'inizio dell'inizializzazione del processo, non prima e dopo le chiamate a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). Tenere presente che **SetDllDirectory** influiscono sull'intero processo e che più thread che chiamano **SetDllDirectory** con valori diversi possono causare un comportamento non definito. Se l'applicazione carica dll di terze parti, eseguire un test con attenzione per identificare eventuali incompatibilità.
-   Non usare la funzione [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) per recuperare un percorso di una dll per una chiamata [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) successiva, a meno che non sia abilitata la modalità di ricerca processo sicura. Quando la modalità di ricerca del processo sicuro non è abilitata, la funzione **SearchPath** utilizza un ordine di ricerca diverso da **LoadLibrary** ed è probabile che prima venga cercata la DLL specificata nella directory corrente dell'utente. Per abilitare la modalità di ricerca del processo sicuro per la funzione **SearchPath** , usare la funzione [**SetSearchPathMode**](/windows/desktop/api/winbase/nf-winbase-setsearchpathmode) con il percorso di ricerca di base \_ \_ \_ enable \_ Safe \_ SEARCHMODE. In questo modo la directory corrente viene spostata alla fine dell'elenco di ricerca di **SearchPath** per la durata del processo. Si noti che la directory corrente non viene rimossa dal percorso di ricerca, pertanto se il sistema non trova una copia legittima della DLL prima che raggiunga la directory corrente, l'applicazione è ancora vulnerabile. Come per [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya), la chiamata di **SetSearchPathMode** deve essere eseguita all'inizio dell'inizializzazione del processo e influire sull'intero processo. Se l'applicazione carica dll di terze parti, eseguire un test con attenzione per identificare eventuali incompatibilità.
-   Non creare presupposti sulla versione del sistema operativo in base a una chiamata [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) che cerca una dll. Se l'applicazione è in esecuzione in un ambiente in cui la DLL non è presente, ma una copia dannosa della DLL si trova nel percorso di ricerca, è possibile che venga caricata la copia dannosa della DLL. Usare invece le tecniche consigliate descritte in [recupero della versione del sistema](/windows/desktop/SysInfo/getting-the-system-version).

Lo strumento di monitoraggio del processo può essere usato per identificare le operazioni di caricamento DLL che potrebbero essere vulnerabili. Lo strumento di monitoraggio del processo può essere scaricato da <https://technet.microsoft.com/sysinternals/bb896645.aspx> .

Nella procedura seguente viene descritto come utilizzare Process Monitor per esaminare le operazioni di caricamento delle DLL nell'applicazione.

**Per utilizzare Process Monitor per esaminare le operazioni di caricamento delle DLL nell'applicazione**

1.  Avviare il monitoraggio del processo.
2.  In elaborazione monitoraggio includere i filtri seguenti:
    -   L'operazione è CreateFile
    -   L'operazione è LoadImage
    -   Il percorso contiene. cpl
    -   Il percorso contiene. dll
    -   Il percorso contiene. drv
    -   Il percorso contiene. exe
    -   Il percorso contiene. ocx
    -   Il percorso contiene. SCR
    -   Il percorso contiene. sys
3.  Escludere i filtri seguenti:
    -   Il nome del processo è procmon.exe
    -   Il nome del processo è Procmon64.exe
    -   Il nome del processo è System
    -   L'operazione inizia con IRP \_ MJ\_
    -   L'operazione inizia con FASTIO\_
    -   Il risultato è SUCCESS
    -   Il percorso termina con pagefile.sys
4.  Tentare di avviare l'applicazione con la directory corrente impostata su una directory specifica. Ad esempio, fare doppio clic su un file con un'estensione il cui gestore file è assegnato all'applicazione.
5.  Controllare l'output di Process Monitor per individuare i percorsi sospetti, ad esempio una chiamata alla directory corrente per caricare una DLL. Questo tipo di chiamata potrebbe indicare una vulnerabilità nell'applicazione.

 

 
