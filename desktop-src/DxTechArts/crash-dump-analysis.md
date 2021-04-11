---
title: Analisi del dump di arresto anomalo
description: Questo articolo tecnico fornisce informazioni su come scrivere e usare un minidump.
ms.assetid: 575c4716-18c2-7b11-7308-aa2e3d8efac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7558e47d08cb0183b8d9cefa5f22f0750fd1c598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046997"
---
# <a name="crash-dump-analysis"></a>Analisi del dump di arresto anomalo

Non tutti i bug possono essere trovati prima del rilascio, il che significa che non tutti i bug che generano eccezioni possono essere trovati prima del rilascio. Fortunatamente, Microsoft ha incluso in Platform SDK una funzione per aiutare gli sviluppatori a raccogliere informazioni sulle eccezioni individuate dagli utenti. La funzione [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) scrive le informazioni del dump di arresto anomalo necessarie in un file senza salvare l'intero spazio del processo. Il file di informazioni del dump di arresto anomalo del sistema è denominato minidump. Questo articolo tecnico fornisce informazioni su come scrivere e usare un minidump.

-   [Scrittura di un minidump](#writing-a-minidump)
-   [Thread safety](#thread-safety)
-   [Scrittura di un minidump con codice](#writing-a-minidump-with-code)
-   [Utilizzo di Dumpchk.exe](#using-dumpchkexe)
-   [Analisi di un minidump](#analyzing-a-minidump)
    -   [Uso del server dei simboli pubblici Microsoft](#using-the-microsoft-public-symbol-server)
    -   [Debug di un minidump con WinDbg](#debugging-a-minidump-with-windbg)
    -   [Uso di strumenti di Copy-Protection con minidump](#using-copy-protection-tools-with-minidumps)
-   [Summary](#summary)

## <a name="writing-a-minidump"></a>Scrittura di un minidump

Le opzioni di base per la scrittura di un minidump sono le seguenti:

-   Non eseguire alcuna operazione. Windows genera automaticamente un minidump ogni volta che un programma genera un'eccezione non gestita. La generazione automatica di un minidump è disponibile a partire da Windows XP. Se l'utente lo consente, il minidump verrà inviato a Microsoft e non allo sviluppatore tramite Segnalazione errori Windows (WER). Gli sviluppatori possono accedere a questi minidump tramite il [programma applicativo desktop di Windows](../appxpkg/windows-desktop-application-program.md).

    L'uso di WER richiede:

    -   Sviluppatori per la firma delle applicazioni tramite Authenticode
    -   Le applicazioni hanno una risorsa VERSIONINFO valida in ogni eseguibile e DLL

    Se si implementa una routine personalizzata per le eccezioni non gestite, è consigliabile utilizzare la funzione [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) nel gestore di eccezioni per inviare anche un minidump automatico a wer. La funzione **ReportFault** gestisce tutti i problemi di connessione e invio del MINIDUMP a wer. Se non si inviano minidump a WER, i requisiti dei giochi per Windows vengono violati.

    Per altre informazioni sul funzionamento di WER, vedere funzionamento di [segnalazione errori Windows](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx). Per una spiegazione dei dettagli di registrazione, vedere [introduzione segnalazione errori Windows](https://msdn.microsoft.com/) sulla [zona ISV](https://msdn.microsoft.com/)di MSDN.

-   Utilizzare un prodotto del Team System Microsoft Visual Studio. Scegliere **Salva dump con nome** dal menu **debug** per salvare una copia di un dump. L'uso di un dump salvato localmente è solo un'opzione per i test e il debug interni.
-   Aggiungere codice al progetto. Aggiungere la funzione [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) e il codice di gestione delle eccezioni appropriato per salvare e inviare un minidump direttamente allo sviluppatore. Questo articolo illustra come implementare questa opzione. Si noti tuttavia che **MiniDumpWriteDump** attualmente non funziona con il codice gestito ed è disponibile solo in Windows XP, Windows Vista, Windows 7.

## <a name="thread-safety"></a>Thread safety

[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) fa parte della libreria DbgHelp. Questa libreria non è thread-safe, pertanto qualsiasi programma che usa **MiniDumpWriteDump** deve sincronizzare tutti i thread prima di provare a chiamare **MiniDumpWriteDump**.

## <a name="writing-a-minidump-with-code"></a>Scrittura di un minidump con codice

L'implementazione effettiva è semplice. Di seguito è riportato un esempio semplice di utilizzo di [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).


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



Questo esempio illustra l'utilizzo di base di [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) e le informazioni minime necessarie per chiamarlo. Il nome del file di dump spetta allo sviluppatore; Tuttavia, per evitare conflitti di nomi di file, è consigliabile generare il nome del file dal nome e dal numero di versione dell'applicazione, dagli ID processo e thread e dalla data e dall'ora. Ciò consentirà inoltre di proteggere i minidump raggruppati per applicazione e versione. Spetta allo sviluppatore decidere la quantità di informazioni utilizzata per distinguere i nomi dei file di minidump.

Si noti che il nome del percorso nell'esempio precedente è stato generato chiamando la funzione [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) per recuperare il percorso della directory designata per i file temporanei. L'uso di questa directory funziona anche con gli account utente con privilegi minimi e impedisce inoltre al minidump di occupare lo spazio su disco rigido dopo che non è più necessario.

Se si archivia il prodotto durante il processo di compilazione giornaliero, assicurarsi anche di includere i simboli per la compilazione in modo che sia possibile eseguire il debug di una versione precedente del prodotto, se necessario. È anche necessario eseguire le operazioni per gestire le ottimizzazioni complete del compilatore durante la generazione di simboli. Questa operazione può essere eseguita aprendo le proprietà del progetto nell'ambiente di sviluppo e, per la configurazione della versione, eseguire le operazioni seguenti:

1.  Sul lato sinistro della pagina delle proprietà del progetto fare clic su C/C++. Per impostazione predefinita, vengono visualizzate le impostazioni **generali** . Sul lato destro della pagina delle proprietà del progetto impostare **formato informazioni di debug** su **database di programma (/Zi)**.
2.  Sul lato sinistro della pagina delle proprietà, espandere **linker**, quindi fare clic su **debug**. Sul lato destro della pagina delle proprietà impostare **genera informazioni di debug** su **Sì (/debug)**.
3.  Fare clic su **ottimizzazione** e impostare i **riferimenti** a e **liminate i dati senza riferimenti (/opt: Ref)**.
4.  Impostare **Enable COMDAT Folding** per **rimuovere COMDAT ridondanti (/opt: ICF)**.

In MSDN sono disponibili informazioni più dettagliate sulla struttura delle [**\_ \_ informazioni sulle eccezioni di MINIDUMP**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) e sulla funzione [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) .

## <a name="using-dumpchkexe"></a>Utilizzo di Dumpchk.exe

Dumpchk.exe è un'utilità da riga di comando che può essere utilizzata per verificare che un file di dump sia stato creato correttamente. Se Dumpchk.exe genera un errore, il file di dump è danneggiato e non può essere analizzato. Per informazioni sull'uso di Dumpchk.exe, vedere [come usare Dumpchk.exe per controllare un file di dump della memoria](https://support.microsoft.com/kb/315271/).

Dumpchk.exe è incluso nel CD di Windows XP e può essere installato \\ negli strumenti di supporto per i file di programma dell'unità \\ di sistema \\ eseguendo Setup.exe nella cartella strumenti di supporto del \\ CD di \\ Windows XP. Per ottenere la versione più recente di Dumpchk.exe, è anche possibile scaricare e installare gli strumenti di debug disponibili in [strumenti di debug di Windows](https://www.microsoft.com/whdc/devtools/debugging/) in [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).

## <a name="analyzing-a-minidump"></a>Analisi di un minidump

L'apertura di un minidump per l'analisi è semplice come crearne una.

**Per analizzare un minidump**

1.  Aprire Visual Studio.
2.  Scegliere **Apri progetto** dal menu **file** .
3.  Impostare **i file di tipo** su **file di dump**, passare al file dump, selezionarlo e fare clic su **Apri.**
4.  Eseguire il debugger.

Il debugger creerà un processo simulato. Il processo simulato verrà interrotto in corrispondenza dell'istruzione che ha causato l'arresto anomalo.

### <a name="using-the-microsoft-public-symbol-server"></a>Uso del server dei simboli pubblici Microsoft

Per ottenere lo stack per i driver o gli arresti anomali a livello di sistema, potrebbe essere necessario configurare Visual Studio in modo che punti al server dei simboli pubblici Microsoft.

**Per impostare un percorso per il server di simboli Microsoft**

1.  Scegliere **Opzioni** dal menu **debug** .
2.  Nella finestra di dialogo **Opzioni** aprire il nodo **debug** e fare clic su **simboli**.
3.  Assicurarsi di eseguire **la ricerca nei percorsi precedenti solo quando i simboli caricati manualmente** non sono selezionati, a meno che non si desideri caricare manualmente i simboli durante il debug.
4.  Se si utilizzano simboli in un server di simboli remoto, è possibile migliorare le prestazioni specificando una directory locale in cui è possibile copiare i simboli. A tale scopo, immettere un percorso per i **simboli della cache dal server dei simboli in questa directory**. Per connettersi al server dei simboli pubblici Microsoft, è necessario abilitare questa impostazione. Si noti che se si esegue il debug di un programma in un computer remoto, la directory della cache fa riferimento a una directory nel computer remoto.
5.  Fare clic su **OK**.
6.  Poiché si utilizza il server dei simboli pubblici Microsoft, viene visualizzata la finestra di dialogo contratto di licenza con l'utente finale. Fare clic su **Sì** per accettare il contratto e scaricare i simboli nella cache locale.

### <a name="debugging-a-minidump-with-windbg"></a>Debug di un minidump con WinDbg

È inoltre possibile utilizzare WinDbg, un debugger che fa parte degli strumenti di debug di Windows, per eseguire il debug di un minidump. WinDbg consente di eseguire il debug senza dover utilizzare Visual Studio. Per scaricare gli strumenti di debug di Windows, vedere [strumenti di debug](https://www.microsoft.com/whdc/devtools/debugging/) di Windows in [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).

Dopo l'installazione degli strumenti di debug di Windows, è necessario immettere il percorso dei simboli in WinDbg.

**Per immettere un percorso di simboli in WinDbg**

1.  Scegliere **percorso simboli** dal menu **file** .
2.  Nella finestra **percorso ricerca simboli** immettere quanto segue:

    "SRV \* c: \\ cache \* https://msdl.microsoft.com/download/symbols ;"

### <a name="using-copy-protection-tools-with-minidumps"></a>Uso di strumenti di Copy-Protection con minidump

Gli sviluppatori devono inoltre tenere presente il modo in cui lo schema di protezione della copia potrebbe influire sul minidump. La maggior parte degli schemi di protezione da copia hanno i propri strumenti di decodifica e spetta allo sviluppatore imparare a usare questi strumenti con [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).

## <a name="summary"></a>Riepilogo

La funzione [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) può essere uno strumento estremamente utile per la raccolta e la risoluzione dei bug dopo il rilascio del prodotto. La scrittura di un gestore di eccezioni personalizzato che usa **MiniDumpWriteDump** consente allo sviluppatore di personalizzare la raccolta di informazioni e migliorare il processo di debug. La funzione è sufficientemente flessibile da poter essere utilizzata in qualsiasi progetto basato su C++ e deve essere considerata parte del processo di stabilità di qualsiasi progetto.

 

 