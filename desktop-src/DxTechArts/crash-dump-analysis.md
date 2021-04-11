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
# <a name="crash-dump-analysis"></a><span data-ttu-id="0fceb-103">Analisi del dump di arresto anomalo</span><span class="sxs-lookup"><span data-stu-id="0fceb-103">Crash Dump Analysis</span></span>

<span data-ttu-id="0fceb-104">Non tutti i bug possono essere trovati prima del rilascio, il che significa che non tutti i bug che generano eccezioni possono essere trovati prima del rilascio.</span><span class="sxs-lookup"><span data-stu-id="0fceb-104">Not all bugs can be found prior to release, which means not all bugs that throw exceptions can be found before release.</span></span> <span data-ttu-id="0fceb-105">Fortunatamente, Microsoft ha incluso in Platform SDK una funzione per aiutare gli sviluppatori a raccogliere informazioni sulle eccezioni individuate dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="0fceb-105">Fortunately, Microsoft has included in the Platform SDK a function to help developers collect information on exceptions that are discovered by users.</span></span> <span data-ttu-id="0fceb-106">La funzione [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) scrive le informazioni del dump di arresto anomalo necessarie in un file senza salvare l'intero spazio del processo.</span><span class="sxs-lookup"><span data-stu-id="0fceb-106">The [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function writes the necessary crash dump information to a file without saving the whole process space.</span></span> <span data-ttu-id="0fceb-107">Il file di informazioni del dump di arresto anomalo del sistema è denominato minidump.</span><span class="sxs-lookup"><span data-stu-id="0fceb-107">This crash dump information file is called a minidump.</span></span> <span data-ttu-id="0fceb-108">Questo articolo tecnico fornisce informazioni su come scrivere e usare un minidump.</span><span class="sxs-lookup"><span data-stu-id="0fceb-108">This technical article provides info about how to write and use a minidump.</span></span>

-   [<span data-ttu-id="0fceb-109">Scrittura di un minidump</span><span class="sxs-lookup"><span data-stu-id="0fceb-109">Writing a Minidump</span></span>](#writing-a-minidump)
-   [<span data-ttu-id="0fceb-110">Thread safety</span><span class="sxs-lookup"><span data-stu-id="0fceb-110">Thread safety</span></span>](#thread-safety)
-   [<span data-ttu-id="0fceb-111">Scrittura di un minidump con codice</span><span class="sxs-lookup"><span data-stu-id="0fceb-111">Writing a Minidump with Code</span></span>](#writing-a-minidump-with-code)
-   [<span data-ttu-id="0fceb-112">Utilizzo di Dumpchk.exe</span><span class="sxs-lookup"><span data-stu-id="0fceb-112">Using Dumpchk.exe</span></span>](#using-dumpchkexe)
-   [<span data-ttu-id="0fceb-113">Analisi di un minidump</span><span class="sxs-lookup"><span data-stu-id="0fceb-113">Analyzing a Minidump</span></span>](#analyzing-a-minidump)
    -   [<span data-ttu-id="0fceb-114">Uso del server dei simboli pubblici Microsoft</span><span class="sxs-lookup"><span data-stu-id="0fceb-114">Using the Microsoft Public Symbol Server</span></span>](#using-the-microsoft-public-symbol-server)
    -   [<span data-ttu-id="0fceb-115">Debug di un minidump con WinDbg</span><span class="sxs-lookup"><span data-stu-id="0fceb-115">Debugging a Minidump with WinDbg</span></span>](#debugging-a-minidump-with-windbg)
    -   [<span data-ttu-id="0fceb-116">Uso di strumenti di Copy-Protection con minidump</span><span class="sxs-lookup"><span data-stu-id="0fceb-116">Using Copy-Protection Tools with Minidumps</span></span>](#using-copy-protection-tools-with-minidumps)
-   [<span data-ttu-id="0fceb-117">Summary</span><span class="sxs-lookup"><span data-stu-id="0fceb-117">Summary</span></span>](#summary)

## <a name="writing-a-minidump"></a><span data-ttu-id="0fceb-118">Scrittura di un minidump</span><span class="sxs-lookup"><span data-stu-id="0fceb-118">Writing a Minidump</span></span>

<span data-ttu-id="0fceb-119">Le opzioni di base per la scrittura di un minidump sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="0fceb-119">The basic options for writing a minidump are as follows:</span></span>

-   <span data-ttu-id="0fceb-120">Non eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="0fceb-120">Do nothing.</span></span> <span data-ttu-id="0fceb-121">Windows genera automaticamente un minidump ogni volta che un programma genera un'eccezione non gestita.</span><span class="sxs-lookup"><span data-stu-id="0fceb-121">Windows automatically generates a minidump whenever a program throws an unhandled exception.</span></span> <span data-ttu-id="0fceb-122">La generazione automatica di un minidump è disponibile a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0fceb-122">Automatic generation of a minidump is available since Windows XP.</span></span> <span data-ttu-id="0fceb-123">Se l'utente lo consente, il minidump verrà inviato a Microsoft e non allo sviluppatore tramite Segnalazione errori Windows (WER).</span><span class="sxs-lookup"><span data-stu-id="0fceb-123">If the user allows it, the minidump will be sent to Microsoft, and not to the developer, through Windows Error Reporting (WER).</span></span> <span data-ttu-id="0fceb-124">Gli sviluppatori possono accedere a questi minidump tramite il [programma applicativo desktop di Windows](../appxpkg/windows-desktop-application-program.md).</span><span class="sxs-lookup"><span data-stu-id="0fceb-124">Developers can gain access to these minidumps through the [Windows Desktop Application Program](../appxpkg/windows-desktop-application-program.md).</span></span>

    <span data-ttu-id="0fceb-125">L'uso di WER richiede:</span><span class="sxs-lookup"><span data-stu-id="0fceb-125">Use of WER requires:</span></span>

    -   <span data-ttu-id="0fceb-126">Sviluppatori per la firma delle applicazioni tramite Authenticode</span><span class="sxs-lookup"><span data-stu-id="0fceb-126">Developers to sign their applications using Authenticode</span></span>
    -   <span data-ttu-id="0fceb-127">Le applicazioni hanno una risorsa VERSIONINFO valida in ogni eseguibile e DLL</span><span class="sxs-lookup"><span data-stu-id="0fceb-127">Applications have valid VERSIONINFO resource in every executable and DLL</span></span>

    <span data-ttu-id="0fceb-128">Se si implementa una routine personalizzata per le eccezioni non gestite, è consigliabile utilizzare la funzione [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) nel gestore di eccezioni per inviare anche un minidump automatico a wer.</span><span class="sxs-lookup"><span data-stu-id="0fceb-128">If you implement a custom routine for unhandled exceptions, you are strongly urged to use the [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) function in the exception handler to also send an automated minidump to WER.</span></span> <span data-ttu-id="0fceb-129">La funzione **ReportFault** gestisce tutti i problemi di connessione e invio del MINIDUMP a wer.</span><span class="sxs-lookup"><span data-stu-id="0fceb-129">The **ReportFault** function handles all of the issues of connecting to and sending the minidump to WER.</span></span> <span data-ttu-id="0fceb-130">Se non si inviano minidump a WER, i requisiti dei giochi per Windows vengono violati.</span><span class="sxs-lookup"><span data-stu-id="0fceb-130">Not sending minidumps to WER violates the requirements of Games for Windows.</span></span>

    <span data-ttu-id="0fceb-131">Per altre informazioni sul funzionamento di WER, vedere funzionamento di [segnalazione errori Windows](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx).</span><span class="sxs-lookup"><span data-stu-id="0fceb-131">For more information on how WER works, see [How Windows Error Reporting Works](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx).</span></span> <span data-ttu-id="0fceb-132">Per una spiegazione dei dettagli di registrazione, vedere [introduzione segnalazione errori Windows](https://msdn.microsoft.com/) sulla [zona ISV](https://msdn.microsoft.com/)di MSDN.</span><span class="sxs-lookup"><span data-stu-id="0fceb-132">For an explanation of registration details, see [Introducing Windows Error Reporting](https://msdn.microsoft.com/) on MSDN's [ISV Zone](https://msdn.microsoft.com/).</span></span>

-   <span data-ttu-id="0fceb-133">Utilizzare un prodotto del Team System Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0fceb-133">Use a product from the Microsoft Visual Studio Team System.</span></span> <span data-ttu-id="0fceb-134">Scegliere **Salva dump con nome** dal menu **debug** per salvare una copia di un dump.</span><span class="sxs-lookup"><span data-stu-id="0fceb-134">On the **Debug** menu, click **Save Dump As** to save a copy of a dump.</span></span> <span data-ttu-id="0fceb-135">L'uso di un dump salvato localmente è solo un'opzione per i test e il debug interni.</span><span class="sxs-lookup"><span data-stu-id="0fceb-135">Use of a locally saved dump is only an option for in-house testing and debugging.</span></span>
-   <span data-ttu-id="0fceb-136">Aggiungere codice al progetto.</span><span class="sxs-lookup"><span data-stu-id="0fceb-136">Add code to your project.</span></span> <span data-ttu-id="0fceb-137">Aggiungere la funzione [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) e il codice di gestione delle eccezioni appropriato per salvare e inviare un minidump direttamente allo sviluppatore.</span><span class="sxs-lookup"><span data-stu-id="0fceb-137">Add the [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function and the appropriate exception handling code to save and send a minidump directly to the developer.</span></span> <span data-ttu-id="0fceb-138">Questo articolo illustra come implementare questa opzione.</span><span class="sxs-lookup"><span data-stu-id="0fceb-138">This article demonstrates how to implement this option.</span></span> <span data-ttu-id="0fceb-139">Si noti tuttavia che **MiniDumpWriteDump** attualmente non funziona con il codice gestito ed è disponibile solo in Windows XP, Windows Vista, Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0fceb-139">However, note that **MiniDumpWriteDump** does not currently work with managed code and is only available on Windows XP, Windows Vista, Windows 7.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="0fceb-140">Thread safety</span><span class="sxs-lookup"><span data-stu-id="0fceb-140">Thread safety</span></span>

<span data-ttu-id="0fceb-141">[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) fa parte della libreria DbgHelp.</span><span class="sxs-lookup"><span data-stu-id="0fceb-141">[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) is part of the DBGHELP library.</span></span> <span data-ttu-id="0fceb-142">Questa libreria non è thread-safe, pertanto qualsiasi programma che usa **MiniDumpWriteDump** deve sincronizzare tutti i thread prima di provare a chiamare **MiniDumpWriteDump**.</span><span class="sxs-lookup"><span data-stu-id="0fceb-142">This library is not thread-safe, so any program that uses **MiniDumpWriteDump** should synchronize all threads before attempting to call **MiniDumpWriteDump**.</span></span>

## <a name="writing-a-minidump-with-code"></a><span data-ttu-id="0fceb-143">Scrittura di un minidump con codice</span><span class="sxs-lookup"><span data-stu-id="0fceb-143">Writing a Minidump with Code</span></span>

<span data-ttu-id="0fceb-144">L'implementazione effettiva è semplice.</span><span class="sxs-lookup"><span data-stu-id="0fceb-144">The actual implementation is straightforward.</span></span> <span data-ttu-id="0fceb-145">Di seguito è riportato un esempio semplice di utilizzo di [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span><span class="sxs-lookup"><span data-stu-id="0fceb-145">The following is a simple example of how to use [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span></span>


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



<span data-ttu-id="0fceb-146">Questo esempio illustra l'utilizzo di base di [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) e le informazioni minime necessarie per chiamarlo.</span><span class="sxs-lookup"><span data-stu-id="0fceb-146">This example demonstrates the basic usage of [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) and the minimum information necessary to call it.</span></span> <span data-ttu-id="0fceb-147">Il nome del file di dump spetta allo sviluppatore; Tuttavia, per evitare conflitti di nomi di file, è consigliabile generare il nome del file dal nome e dal numero di versione dell'applicazione, dagli ID processo e thread e dalla data e dall'ora.</span><span class="sxs-lookup"><span data-stu-id="0fceb-147">The name of the dump file is up to the developer; however, to avoid file name collisions, it is advisable to generate the file name from the application's name and version number, the process and thread IDs, and the date and time.</span></span> <span data-ttu-id="0fceb-148">Ciò consentirà inoltre di proteggere i minidump raggruppati per applicazione e versione.</span><span class="sxs-lookup"><span data-stu-id="0fceb-148">This will also help to keep the minidumps grouped by application and version.</span></span> <span data-ttu-id="0fceb-149">Spetta allo sviluppatore decidere la quantità di informazioni utilizzata per distinguere i nomi dei file di minidump.</span><span class="sxs-lookup"><span data-stu-id="0fceb-149">It is up to the developer to decide how much information is used to differentiate minidump file names.</span></span>

<span data-ttu-id="0fceb-150">Si noti che il nome del percorso nell'esempio precedente è stato generato chiamando la funzione [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) per recuperare il percorso della directory designata per i file temporanei.</span><span class="sxs-lookup"><span data-stu-id="0fceb-150">It should be noted that the path name in the preceding example was generated by calling the [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) function to retrieve the path of the directory designated for temporary files.</span></span> <span data-ttu-id="0fceb-151">L'uso di questa directory funziona anche con gli account utente con privilegi minimi e impedisce inoltre al minidump di occupare lo spazio su disco rigido dopo che non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="0fceb-151">Use of this directory works even with least-privileged user accounts, and it also prevents the minidump from taking up hard drive space after it is no longer needed.</span></span>

<span data-ttu-id="0fceb-152">Se si archivia il prodotto durante il processo di compilazione giornaliero, assicurarsi anche di includere i simboli per la compilazione in modo che sia possibile eseguire il debug di una versione precedente del prodotto, se necessario.</span><span class="sxs-lookup"><span data-stu-id="0fceb-152">If you archive the product during your daily build process, also be sure to include symbols for the build so that you can debug an old version of the product, if necessary.</span></span> <span data-ttu-id="0fceb-153">È anche necessario eseguire le operazioni per gestire le ottimizzazioni complete del compilatore durante la generazione di simboli.</span><span class="sxs-lookup"><span data-stu-id="0fceb-153">You also need to take steps to maintain full compiler optimizations while generating symbols.</span></span> <span data-ttu-id="0fceb-154">Questa operazione può essere eseguita aprendo le proprietà del progetto nell'ambiente di sviluppo e, per la configurazione della versione, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0fceb-154">This can be done by opening your project's properties in the development environment and, for the release configuration, doing the following:</span></span>

1.  <span data-ttu-id="0fceb-155">Sul lato sinistro della pagina delle proprietà del progetto fare clic su C/C++.</span><span class="sxs-lookup"><span data-stu-id="0fceb-155">On the left side of the project's property page, click C/C++.</span></span> <span data-ttu-id="0fceb-156">Per impostazione predefinita, vengono visualizzate le impostazioni **generali** .</span><span class="sxs-lookup"><span data-stu-id="0fceb-156">By default, this displays **General** settings.</span></span> <span data-ttu-id="0fceb-157">Sul lato destro della pagina delle proprietà del progetto impostare **formato informazioni di debug** su **database di programma (/Zi)**.</span><span class="sxs-lookup"><span data-stu-id="0fceb-157">On the right side of the project's property page, set **Debug Information Format** to **Program Database (/Zi)**.</span></span>
2.  <span data-ttu-id="0fceb-158">Sul lato sinistro della pagina delle proprietà, espandere **linker**, quindi fare clic su **debug**.</span><span class="sxs-lookup"><span data-stu-id="0fceb-158">On the left side of the property page, expand **Linker**, and then click **Debugging**.</span></span> <span data-ttu-id="0fceb-159">Sul lato destro della pagina delle proprietà impostare **genera informazioni di debug** su **Sì (/debug)**.</span><span class="sxs-lookup"><span data-stu-id="0fceb-159">On the right side of the property page, set **Generate Debug Info** to **Yes (/DEBUG)**.</span></span>
3.  <span data-ttu-id="0fceb-160">Fare clic su **ottimizzazione** e impostare i **riferimenti** a e **liminate i dati senza riferimenti (/opt: Ref)**.</span><span class="sxs-lookup"><span data-stu-id="0fceb-160">Click **Optimization**, and set **References** to E **liminate Unreferenced Data (/OPT:REF)**.</span></span>
4.  <span data-ttu-id="0fceb-161">Impostare **Enable COMDAT Folding** per **rimuovere COMDAT ridondanti (/opt: ICF)**.</span><span class="sxs-lookup"><span data-stu-id="0fceb-161">Set **Enable COMDAT Folding** to **Remove Redundant COMDATs (/OPT:ICF)**.</span></span>

<span data-ttu-id="0fceb-162">In MSDN sono disponibili informazioni più dettagliate sulla struttura delle [**\_ \_ informazioni sulle eccezioni di MINIDUMP**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) e sulla funzione [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) .</span><span class="sxs-lookup"><span data-stu-id="0fceb-162">MSDN has more detailed information on the [**MINIDUMP\_EXCEPTION\_INFORMATION**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) structure and the [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function.</span></span>

## <a name="using-dumpchkexe"></a><span data-ttu-id="0fceb-163">Utilizzo di Dumpchk.exe</span><span class="sxs-lookup"><span data-stu-id="0fceb-163">Using Dumpchk.exe</span></span>

<span data-ttu-id="0fceb-164">Dumpchk.exe è un'utilità da riga di comando che può essere utilizzata per verificare che un file di dump sia stato creato correttamente.</span><span class="sxs-lookup"><span data-stu-id="0fceb-164">Dumpchk.exe is a command-line utility that can be used to verify that a dump file was created correctly.</span></span> <span data-ttu-id="0fceb-165">Se Dumpchk.exe genera un errore, il file di dump è danneggiato e non può essere analizzato.</span><span class="sxs-lookup"><span data-stu-id="0fceb-165">If Dumpchk.exe generates an error, then the dump file is corrupt and cannot be analyzed.</span></span> <span data-ttu-id="0fceb-166">Per informazioni sull'uso di Dumpchk.exe, vedere [come usare Dumpchk.exe per controllare un file di dump della memoria](https://support.microsoft.com/kb/315271/).</span><span class="sxs-lookup"><span data-stu-id="0fceb-166">For information on using Dumpchk.exe, see [How to Use Dumpchk.exe to Check a Memory Dump File](https://support.microsoft.com/kb/315271/).</span></span>

<span data-ttu-id="0fceb-167">Dumpchk.exe è incluso nel CD di Windows XP e può essere installato \\ negli strumenti di supporto per i file di programma dell'unità \\ di sistema \\ eseguendo Setup.exe nella cartella strumenti di supporto del \\ CD di \\ Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0fceb-167">Dumpchk.exe is included on the Windows XP product CD and can be installed to System Drive\\Program Files\\Support Tools\\ by running Setup.exe in the Support\\Tools\\ folder on the Windows XP product CD.</span></span> <span data-ttu-id="0fceb-168">Per ottenere la versione più recente di Dumpchk.exe, è anche possibile scaricare e installare gli strumenti di debug disponibili in [strumenti di debug di Windows](https://www.microsoft.com/whdc/devtools/debugging/) in [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span><span class="sxs-lookup"><span data-stu-id="0fceb-168">You can also get the latest version of Dumpchk.exe by download and installing the debugging tools available from [Windows Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) on [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span></span>

## <a name="analyzing-a-minidump"></a><span data-ttu-id="0fceb-169">Analisi di un minidump</span><span class="sxs-lookup"><span data-stu-id="0fceb-169">Analyzing a Minidump</span></span>

<span data-ttu-id="0fceb-170">L'apertura di un minidump per l'analisi è semplice come crearne una.</span><span class="sxs-lookup"><span data-stu-id="0fceb-170">Opening a minidump for analysis is as easy as creating one.</span></span>

<span data-ttu-id="0fceb-171">**Per analizzare un minidump**</span><span class="sxs-lookup"><span data-stu-id="0fceb-171">**To analyze a minidump**</span></span>

1.  <span data-ttu-id="0fceb-172">Aprire Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0fceb-172">Open Visual Studio.</span></span>
2.  <span data-ttu-id="0fceb-173">Scegliere **Apri progetto** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="0fceb-173">On the **File** menu, click **Open Project**.</span></span>
3.  <span data-ttu-id="0fceb-174">Impostare **i file di tipo** su **file di dump**, passare al file dump, selezionarlo e fare clic su **Apri.**</span><span class="sxs-lookup"><span data-stu-id="0fceb-174">Set **Files of type** to **Dump Files**, navigate to the dump file, select it, and click **Open.**</span></span>
4.  <span data-ttu-id="0fceb-175">Eseguire il debugger.</span><span class="sxs-lookup"><span data-stu-id="0fceb-175">Run the debugger.</span></span>

<span data-ttu-id="0fceb-176">Il debugger creerà un processo simulato.</span><span class="sxs-lookup"><span data-stu-id="0fceb-176">The debugger will create a simulated process.</span></span> <span data-ttu-id="0fceb-177">Il processo simulato verrà interrotto in corrispondenza dell'istruzione che ha causato l'arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="0fceb-177">The simulated process will be halted at the instruction that caused the crash.</span></span>

### <a name="using-the-microsoft-public-symbol-server"></a><span data-ttu-id="0fceb-178">Uso del server dei simboli pubblici Microsoft</span><span class="sxs-lookup"><span data-stu-id="0fceb-178">Using the Microsoft Public Symbol Server</span></span>

<span data-ttu-id="0fceb-179">Per ottenere lo stack per i driver o gli arresti anomali a livello di sistema, potrebbe essere necessario configurare Visual Studio in modo che punti al server dei simboli pubblici Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0fceb-179">To get the stack for driver- or system-level crashes, it might be necessary to configure Visual Studio to point to the Microsoft public symbol server.</span></span>

<span data-ttu-id="0fceb-180">**Per impostare un percorso per il server di simboli Microsoft**</span><span class="sxs-lookup"><span data-stu-id="0fceb-180">**To set a path to the Microsoft symbol server**</span></span>

1.  <span data-ttu-id="0fceb-181">Scegliere **Opzioni** dal menu **debug** .</span><span class="sxs-lookup"><span data-stu-id="0fceb-181">On the **Debug** menu, click **Options**.</span></span>
2.  <span data-ttu-id="0fceb-182">Nella finestra di dialogo **Opzioni** aprire il nodo **debug** e fare clic su **simboli**.</span><span class="sxs-lookup"><span data-stu-id="0fceb-182">In the **Options** dialog box, open the **Debugging** node, and click **Symbols**.</span></span>
3.  <span data-ttu-id="0fceb-183">Assicurarsi di eseguire **la ricerca nei percorsi precedenti solo quando i simboli caricati manualmente** non sono selezionati, a meno che non si desideri caricare manualmente i simboli durante il debug.</span><span class="sxs-lookup"><span data-stu-id="0fceb-183">Make sure **Search the above locations only when symbols are loaded manually** is not selected, unless you want to load symbols manually when you debug.</span></span>
4.  <span data-ttu-id="0fceb-184">Se si utilizzano simboli in un server di simboli remoto, è possibile migliorare le prestazioni specificando una directory locale in cui è possibile copiare i simboli.</span><span class="sxs-lookup"><span data-stu-id="0fceb-184">If you are using symbols on a remote symbol server, you can improve performance by specifying a local directory that symbols can be copied to.</span></span> <span data-ttu-id="0fceb-185">A tale scopo, immettere un percorso per i **simboli della cache dal server dei simboli in questa directory**.</span><span class="sxs-lookup"><span data-stu-id="0fceb-185">To do this, enter a path for **Cache symbols from symbol server to this directory**.</span></span> <span data-ttu-id="0fceb-186">Per connettersi al server dei simboli pubblici Microsoft, è necessario abilitare questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="0fceb-186">To connect to the Microsoft public symbol server, you need to enable this setting.</span></span> <span data-ttu-id="0fceb-187">Si noti che se si esegue il debug di un programma in un computer remoto, la directory della cache fa riferimento a una directory nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="0fceb-187">Note that if you are debugging a program on a remote computer, the cache directory refers to a directory on the remote computer.</span></span>
5.  <span data-ttu-id="0fceb-188">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="0fceb-188">Click **OK**.</span></span>
6.  <span data-ttu-id="0fceb-189">Poiché si utilizza il server dei simboli pubblici Microsoft, viene visualizzata la finestra di dialogo contratto di licenza con l'utente finale.</span><span class="sxs-lookup"><span data-stu-id="0fceb-189">Because you are using the Microsoft public symbol server, an End User License Agreement dialog box appears.</span></span> <span data-ttu-id="0fceb-190">Fare clic su **Sì** per accettare il contratto e scaricare i simboli nella cache locale.</span><span class="sxs-lookup"><span data-stu-id="0fceb-190">Click **Yes** to accept the agreement and download symbols to your local cache.</span></span>

### <a name="debugging-a-minidump-with-windbg"></a><span data-ttu-id="0fceb-191">Debug di un minidump con WinDbg</span><span class="sxs-lookup"><span data-stu-id="0fceb-191">Debugging a Minidump with WinDbg</span></span>

<span data-ttu-id="0fceb-192">È inoltre possibile utilizzare WinDbg, un debugger che fa parte degli strumenti di debug di Windows, per eseguire il debug di un minidump.</span><span class="sxs-lookup"><span data-stu-id="0fceb-192">You can also use WinDbg, a debugger that is part of the Windows Debugging Tools, to debug a minidump.</span></span> <span data-ttu-id="0fceb-193">WinDbg consente di eseguire il debug senza dover utilizzare Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0fceb-193">WinDbg allows you to debug without having to use Visual Studio.</span></span> <span data-ttu-id="0fceb-194">Per scaricare gli strumenti di debug di Windows, vedere [strumenti di debug](https://www.microsoft.com/whdc/devtools/debugging/) di Windows in [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span><span class="sxs-lookup"><span data-stu-id="0fceb-194">To download Windows Debugging Tools, see [Windows Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) on [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span></span>

<span data-ttu-id="0fceb-195">Dopo l'installazione degli strumenti di debug di Windows, è necessario immettere il percorso dei simboli in WinDbg.</span><span class="sxs-lookup"><span data-stu-id="0fceb-195">After installing Windows Debugging Tools, you must enter the symbol path in WinDbg.</span></span>

<span data-ttu-id="0fceb-196">**Per immettere un percorso di simboli in WinDbg**</span><span class="sxs-lookup"><span data-stu-id="0fceb-196">**To enter a symbol path in WinDbg**</span></span>

1.  <span data-ttu-id="0fceb-197">Scegliere **percorso simboli** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="0fceb-197">On the **File** menu, click **Symbol Path**.</span></span>
2.  <span data-ttu-id="0fceb-198">Nella finestra **percorso ricerca simboli** immettere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="0fceb-198">In the **Symbol Search Path** window, enter the following:</span></span>

    <span data-ttu-id="0fceb-199">"SRV \* c: \\ cache \* https://msdl.microsoft.com/download/symbols ;"</span><span class="sxs-lookup"><span data-stu-id="0fceb-199">"srv\*c:\\cache\*https://msdl.microsoft.com/download/symbols;"</span></span>

### <a name="using-copy-protection-tools-with-minidumps"></a><span data-ttu-id="0fceb-200">Uso di strumenti di Copy-Protection con minidump</span><span class="sxs-lookup"><span data-stu-id="0fceb-200">Using Copy-Protection Tools with Minidumps</span></span>

<span data-ttu-id="0fceb-201">Gli sviluppatori devono inoltre tenere presente il modo in cui lo schema di protezione della copia potrebbe influire sul minidump.</span><span class="sxs-lookup"><span data-stu-id="0fceb-201">Developers also need to be aware of how their copy-protection scheme might affect the minidump.</span></span> <span data-ttu-id="0fceb-202">La maggior parte degli schemi di protezione da copia hanno i propri strumenti di decodifica e spetta allo sviluppatore imparare a usare questi strumenti con [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span><span class="sxs-lookup"><span data-stu-id="0fceb-202">Most copy-protection schemes have their own descramble tools, and it is up to the developer to learn how to use those tools with [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span></span>

## <a name="summary"></a><span data-ttu-id="0fceb-203">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="0fceb-203">Summary</span></span>

<span data-ttu-id="0fceb-204">La funzione [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) può essere uno strumento estremamente utile per la raccolta e la risoluzione dei bug dopo il rilascio del prodotto.</span><span class="sxs-lookup"><span data-stu-id="0fceb-204">The [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function can be an extremely useful tool in collecting and solving bugs after the product has been released.</span></span> <span data-ttu-id="0fceb-205">La scrittura di un gestore di eccezioni personalizzato che usa **MiniDumpWriteDump** consente allo sviluppatore di personalizzare la raccolta di informazioni e migliorare il processo di debug.</span><span class="sxs-lookup"><span data-stu-id="0fceb-205">Writing a custom exception handler that uses **MiniDumpWriteDump** allows the developer to customize the information collection and improve the debugging process.</span></span> <span data-ttu-id="0fceb-206">La funzione è sufficientemente flessibile da poter essere utilizzata in qualsiasi progetto basato su C++ e deve essere considerata parte del processo di stabilità di qualsiasi progetto.</span><span class="sxs-lookup"><span data-stu-id="0fceb-206">The function is flexible enough to be used in any C++-based project and should be considered part of any project's stability process.</span></span>

 

 