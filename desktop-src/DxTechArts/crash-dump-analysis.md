---
title: Analisi dei dump di arresto anomalo del sistema
description: Questo articolo tecnico fornisce informazioni su come scrivere e usare un minidump.
ms.assetid: 575c4716-18c2-7b11-7308-aa2e3d8efac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c68891e2e20938036bd016e6e786a2cdad0096ae44af0e8974a88052963be0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075521"
---
# <a name="crash-dump-analysis"></a>Analisi dei dump di arresto anomalo del sistema

Non tutti i bug sono disponibili prima del rilascio, il che significa che non tutti i bug che generano eccezioni possono essere trovati prima del rilascio. Fortunatamente, Microsoft ha incluso in Platform SDK una funzione che consente agli sviluppatori di raccogliere informazioni sulle eccezioni individuate dagli utenti. La [**funzione MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) scrive le informazioni necessarie sul dump di arresto anomalo del sistema in un file senza salvare l'intero spazio del processo. Questo file di informazioni sui dump di arresto anomalo del sistema è denominato minidump. Questo articolo tecnico fornisce informazioni su come scrivere e usare un minidump.

-   [Scrittura di un minidump](#writing-a-minidump)
-   [Thread safety](#thread-safety)
-   [Scrittura di un minidump con codice](#writing-a-minidump-with-code)
-   [Uso di Dumpchk.exe](#using-dumpchkexe)
-   [Analisi di un minidump](#analyzing-a-minidump)
    -   [Uso del server di simboli pubblico Microsoft](#using-the-microsoft-public-symbol-server)
    -   [Debug di un minidump con WinDbg](#debugging-a-minidump-with-windbg)
    -   [Uso Copy-Protection strumenti con minidump](#using-copy-protection-tools-with-minidumps)
-   [Summary](#summary)

## <a name="writing-a-minidump"></a>Scrittura di un minidump

Le opzioni di base per la scrittura di un minidump sono le seguenti:

-   Non eseguire alcuna operazione. Windows genera automaticamente un minidump ogni volta che un programma genera un'eccezione non gestita. La generazione automatica di un minidump è disponibile Windows XP. Se l'utente lo consente, il minidump verrà inviato a Microsoft e non allo sviluppatore tramite Segnalazione errori Windows (WER). Gli sviluppatori possono ottenere l'accesso a questi minidump [tramite Windows Desktop Application Program](../appxpkg/windows-desktop-application-program.md).

    L'uso di WeR richiede:

    -   Sviluppatori per firmare le applicazioni con Authenticode
    -   Le applicazioni hanno una risorsa VERSIONINFO valida in ogni file eseguibile e DLL

    Se si implementa una routine personalizzata per le eccezioni non gestite, si è fortemente consigliati di usare la funzione [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) nel gestore eccezioni per inviare anche un minidump automatizzato a Segnalazione errori Windows. La **funzione ReportFault** gestisce tutti i problemi di connessione e invio del minidump a Segnalazione errori Windows. Il fatto di non inviare minidump a WeR viola i requisiti di Games per Windows.

    Per altre informazioni sul funzionamento di WeR, vedere [How Segnalazione errori Windows Works](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx). Per una spiegazione dei dettagli della registrazione, vedere [Introducing Segnalazione errori Windows](https://msdn.microsoft.com/) on MSDN's ISV Zone (Introduzione Segnalazione errori Windows nella zona [ISV di](https://msdn.microsoft.com/)MSDN).

-   Usare un prodotto di Microsoft Visual Studio Team System. Scegliere **Salva dump** con nome **dal** menu Debug per salvare una copia di un dump. L'uso di un dump salvato in locale è solo un'opzione per il test e il debug interno.
-   Aggiungere codice al progetto. Aggiungere la [**funzione MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) e il codice di gestione delle eccezioni appropriato per salvare e inviare un minidump direttamente allo sviluppatore. Questo articolo illustra come implementare questa opzione. Si noti tuttavia che **MiniDumpWriteDump** attualmente non funziona con il codice gestito ed è disponibile solo in Windows XP, Windows Vista, Windows 7.

## <a name="thread-safety"></a>Thread safety

[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) fa parte della libreria DBGHELP. Questa libreria non è thread-safe, pertanto qualsiasi programma che usa **MiniDumpWriteDump** deve sincronizzare tutti i thread prima di tentare **di chiamare MiniDumpWriteDump.**

## <a name="writing-a-minidump-with-code"></a>Scrittura di un minidump con codice

L'implementazione effettiva è semplice. Di seguito è riportato un semplice esempio di come usare [**MiniDumpWriteDump.**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)


```C++
#include <dbghelp.h>
#include <shellapi.h>
#include <shlobj.h>

int GenerateDump(EXCEPTION_POINTERS* pExceptionPointers)
{
    BOOL bMiniDumpSuccessful;
    WCHAR szPath[MAX_PATH]; 
    WCHAR szFileName[MAX_PATH]; 
    WCHAR* szAppName = L"AppName";
    WCHAR* szVersion = L"v1.0";
    DWORD dwBufferSize = MAX_PATH;
    HANDLE hDumpFile;
    SYSTEMTIME stLocalTime;
    MINIDUMP_EXCEPTION_INFORMATION ExpParam;

    GetLocalTime( &stLocalTime );
    GetTempPath( dwBufferSize, szPath );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s", szPath, szAppName );
    CreateDirectory( szFileName, NULL );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s\\%s-%04d%02d%02d-%02d%02d%02d-%ld-%ld.dmp", 
               szPath, szAppName, szVersion, 
               stLocalTime.wYear, stLocalTime.wMonth, stLocalTime.wDay, 
               stLocalTime.wHour, stLocalTime.wMinute, stLocalTime.wSecond, 
               GetCurrentProcessId(), GetCurrentThreadId());
    hDumpFile = CreateFile(szFileName, GENERIC_READ|GENERIC_WRITE, 
                FILE_SHARE_WRITE|FILE_SHARE_READ, 0, CREATE_ALWAYS, 0, 0);

    ExpParam.ThreadId = GetCurrentThreadId();
    ExpParam.ExceptionPointers = pExceptionPointers;
    ExpParam.ClientPointers = TRUE;

    bMiniDumpSuccessful = MiniDumpWriteDump(GetCurrentProcess(), GetCurrentProcessId(), 
                    hDumpFile, MiniDumpWithDataSegs, &ExpParam, NULL, NULL);

    return EXCEPTION_EXECUTE_HANDLER;
}


void SomeFunction()
{
    __try
    {
        int *pBadPtr = NULL;
        *pBadPtr = 0;
    }
    __except(GenerateDump(GetExceptionInformation()))
    {
    }
}
```



Questo esempio illustra l'utilizzo di [**base di MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) e le informazioni minime necessarie per chiamarlo. Il nome del file di dump è per lo sviluppatore. Tuttavia, per evitare conflitti di nome file, è consigliabile generare il nome file dal nome e dal numero di versione dell'applicazione, dagli ID di processo e thread e da data e ora. Ciò consente anche di mantenere i minidump raggruppati per applicazione e versione. È lo sviluppatore a decidere la quantità di informazioni usata per distinguere i nomi dei file di minidump.

Si noti che il nome del percorso nell'esempio precedente è stato generato chiamando la [**funzione GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) per recuperare il percorso della directory designata per i file temporanei. L'uso di questa directory funziona anche con gli account utente con privilegi minimi e impedisce al minidump di occupare spazio su disco rigido quando non è più necessario.

Se si archivia il prodotto durante il processo di compilazione giornaliero, assicurarsi di includere anche i simboli per la build in modo che sia possibile eseguire il debug di una versione precedente del prodotto, se necessario. È anche necessario eseguire passaggi per mantenere le ottimizzazioni complete del compilatore durante la generazione dei simboli. A tale scopo, aprire le proprietà del progetto nell'ambiente di sviluppo e, per la configurazione della versione, eseguire le operazioni seguenti:

1.  Sul lato sinistro della pagina delle proprietà del progetto fare clic su C/C++. Per impostazione predefinita, vengono visualizzate **le impostazioni** generali. Sul lato destro della pagina delle proprietà del progetto impostare Formato informazioni di **debug** su **Database di programma (/Zi).**
2.  Sul lato sinistro della pagina delle proprietà espandere **Linker** e quindi fare clic su **Debug.** Sul lato destro della pagina delle proprietà impostare **Genera informazioni di debug** su Sì **(/DEBUG).**
3.  Fare **clic su** Ottimizzazione e impostare **Riferimenti** su Dati senza **riferimenti (/OPT:REF)**.
4.  Impostare **Enable COMDAT Folding (Abilita la folding COMDAT)** su **Remove Redundant COMDATs (/OPT:ICF) (Rimuovi COMDAT ridondanti -/OPT:ICF).**

MSDN include informazioni più dettagliate sulla struttura DELLE INFORMAZIONI SULLE [**\_ ECCEZIONI \_ MINIDUMP**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) e sulla [**funzione MiniDumpWriteDump.**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)

## <a name="using-dumpchkexe"></a>Uso di Dumpchk.exe

Dumpchk.exe è un'utilità della riga di comando che può essere usata per verificare che un file dump sia stato creato correttamente. Se Dumpchk.exe genera un errore, il file di dump è danneggiato e non può essere analizzato. Per informazioni sull'uso Dumpchk.exe, vedere [How to Use Dumpchk.exe to Check a Memory Dump File](https://support.microsoft.com/kb/315271/).

Dumpchk.exe è incluso nel CD del prodotto Windows XP e può essere installato in System Drive Program Files Support Tools eseguendo Setup.exe nella cartella Strumenti di supporto del CD del \\ \\ prodotto Windows \\ \\ \\ XP. È anche possibile ottenere la versione più recente di Dumpchk.exe scaricando e installando gli strumenti di debug disponibili in Windows [Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) in Windows Hardware [Developer Central.](https://www.microsoft.com/whdc/)

## <a name="analyzing-a-minidump"></a>Analisi di un minidump

L'apertura di un minidump per l'analisi è semplice quanto crearne uno.

**Per analizzare un minidump**

1.  Aprire Visual Studio.
2.  Scegliere **Apri** dal menu File **Project**.
3.  Impostare **File di tipo su** File **dump**, passare al file dump, selezionarlo e fare clic su **Apri.**
4.  Eseguire il debugger.

Il debugger creerà un processo simulato. Il processo simulato verrà interrotto in corrispondenza dell'istruzione che ha causato l'arresto anomalo.

### <a name="using-the-microsoft-public-symbol-server"></a>Uso del server di simboli pubblico Microsoft

Per ottenere lo stack per gli arresti anomali a livello di driver o di sistema, potrebbe essere necessario configurare Visual Studio in modo che punti al server dei simboli pubblico Microsoft.

**Per impostare un percorso per il server di simboli Microsoft**

1.  Scegliere **Opzioni** dal menu **Debug**.
2.  Nella finestra **di** dialogo Opzioni aprire il **nodo Debug** e fare clic su **Simboli**.
3.  Assicurarsi che **l'opzione Cerca nei** percorsi precedenti solo quando i simboli vengono caricati manualmente non sia selezionata, a meno che non si voglia caricare manualmente i simboli durante il debug.
4.  Se si usano simboli in un server di simboli remoto, è possibile migliorare le prestazioni specificando una directory locale in cui è possibile copiare i simboli. A tale scopo, immettere un percorso per **Memorizzare nella cache i simboli dal server dei simboli a questa directory**. Per connettersi al server di simboli pubblico Microsoft, è necessario abilitare questa impostazione. Si noti che se si esegue il debug di un programma in un computer remoto, la directory della cache fa riferimento a una directory nel computer remoto.
5.  Fare clic su **OK**.
6.  Poiché si usa il server di simboli pubblico Microsoft, viene visualizzata la finestra di dialogo Contratto di licenza con l'utente finale. Fare **clic su** Sì per accettare il contratto e scaricare i simboli nella cache locale.

### <a name="debugging-a-minidump-with-windbg"></a>Debug di un minidump con WinDbg

Per eseguire il debug di un minidump, è anche possibile usare WinDbg, un debugger in Windows strumenti di debug di . WinDbg consente di eseguire il debug senza dover usare Visual Studio. Per scaricare gli Windows di debug, vedere Windows [Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) in Windows Hardware [Developer Central.](https://www.microsoft.com/whdc/)

Dopo aver installato Windows di debug, è necessario immettere il percorso del simbolo in WinDbg.

**Per immettere un percorso di simboli in WinDbg**

1.  Scegliere **Percorso** simboli dal menu **File**.
2.  Nella finestra **Symbol Search Path (Percorso** di ricerca simboli) immettere quanto segue:

    "srv \* c: \\ cache \* https://msdl.microsoft.com/download/symbols ;"

### <a name="using-copy-protection-tools-with-minidumps"></a>Uso Copy-Protection tools con minidump

Gli sviluppatori devono anche essere consapevoli di come lo schema di protezione della copia potrebbe influire sul minidump. La maggior parte degli schemi di protezione della copia ha strumenti descramble personalizzati ed è lo sviluppatore a imparare a usare tali strumenti con [**MiniDumpWriteDump.**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)

## <a name="summary"></a>Riepilogo

La [**funzione MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) può essere uno strumento estremamente utile per raccogliere e risolvere i bug dopo il rilascio del prodotto. La scrittura di un gestore di eccezioni personalizzato che usa **MiniDumpWriteDump** consente allo sviluppatore di personalizzare la raccolta di informazioni e migliorare il processo di debug. La funzione è sufficientemente flessibile da essere usata in qualsiasi progetto basato su C++e deve essere considerata parte del processo di stabilità di qualsiasi progetto.

 

 