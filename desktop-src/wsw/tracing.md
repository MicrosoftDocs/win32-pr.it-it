---
title: Traccia
description: La traccia utilizza Event Tracing for Windows (ETW).
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Traccia dei servizi Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c660884667cefae8067376075a30cbc41f70d4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399946"
---
# <a name="tracing"></a><span data-ttu-id="2f439-106">Traccia</span><span class="sxs-lookup"><span data-stu-id="2f439-106">Tracing</span></span>

<span data-ttu-id="2f439-107">La traccia utilizza Event Tracing for Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="2f439-107">Tracing uses Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="2f439-108">Per sfruttare i vantaggi degli strumenti di traccia disponibili con Windows Server 2008 R2, installare il Microsoft Windows SDK dal sito di [download di MSDN](https://www.microsoft.com/download/details.aspx?id=8279) .</span><span class="sxs-lookup"><span data-stu-id="2f439-108">To take advantage of the tracing tools available with Windows Server 2008 R2, install the Microsoft Windows SDK from the [MSDN Downloads](https://www.microsoft.com/download/details.aspx?id=8279) site.</span></span>


<span data-ttu-id="2f439-109">Sono supportati tre livelli di traccia:</span><span class="sxs-lookup"><span data-stu-id="2f439-109">There are three tracing levels supported:</span></span>

-   <span data-ttu-id="2f439-110">Verbose (tutte le tracce disponibili).</span><span class="sxs-lookup"><span data-stu-id="2f439-110">Verbose (all available traces).</span></span>
-   <span data-ttu-id="2f439-111">Informazioni (tracce informative).</span><span class="sxs-lookup"><span data-stu-id="2f439-111">Info (informational traces).</span></span>
-   <span data-ttu-id="2f439-112">Errore (tracce di errore).</span><span class="sxs-lookup"><span data-stu-id="2f439-112">Error (error traces).</span></span>

<span data-ttu-id="2f439-113">Vengono tracciati gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2f439-113">The following events are traced:</span></span>

-   <span data-ttu-id="2f439-114">Eventuali errori (Level = Error, Level = info o level = verbose).</span><span class="sxs-lookup"><span data-stu-id="2f439-114">Any errors (Level=Error, Level=Info or Level=Verbose).</span></span>
-   <span data-ttu-id="2f439-115">Ingresso/uscita di un'API (Level = info o level = verbose).</span><span class="sxs-lookup"><span data-stu-id="2f439-115">Entry/Exit of an API (Level=Info or Level=Verbose).</span></span>
-   <span data-ttu-id="2f439-116">Inizio e completamento di qualsiasi IO (Level = info o level = verbose)</span><span class="sxs-lookup"><span data-stu-id="2f439-116">Start and completion of any IO (Level=Info or Level=Verbose)</span></span>
-   <span data-ttu-id="2f439-117">Messaggi SOAP scambiati (level = verbose, disponibile in Windows 2003 SP1 e versioni successive)</span><span class="sxs-lookup"><span data-stu-id="2f439-117">Exchanged SOAP messages (Level=Verbose, available on Windows 2003 SP1 and later)</span></span>

## <a name="generating-and-viewing-wwsapi-traces"></a><span data-ttu-id="2f439-118">Generazione e visualizzazione di tracce WWSAPI</span><span class="sxs-lookup"><span data-stu-id="2f439-118">Generating and Viewing WWSAPI Traces</span></span>

<span data-ttu-id="2f439-119">WWSAPI utilizza gli eventi basati su manifesto in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2f439-119">WWSAPI uses the manifest based events on Windows Vista and above.</span></span> <span data-ttu-id="2f439-120">Di conseguenza, l'esperienza di traccia presenta alcune differenze in base alla versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2f439-120">As a result, the tracing experience has some differences based on the operating system version.</span></span> <span data-ttu-id="2f439-121">La generazione di tracce ETW può essere eseguita tramite gli strumenti ETW predefiniti in tutte le piattaforme supportate.</span><span class="sxs-lookup"><span data-stu-id="2f439-121">Generating ETW traces can be done by using the in-box ETW tools on all supported platforms.</span></span> <span data-ttu-id="2f439-122">Tuttavia, la visualizzazione delle tracce ETW in un formato gradevole richiede strumenti personalizzati in Windows XP SP2 e Windows 2003 SP1.</span><span class="sxs-lookup"><span data-stu-id="2f439-122">However viewing the ETW traces in a nice format requires custom tools on Windows XP SP2 and Windows 2003 SP1.</span></span> <span data-ttu-id="2f439-123">Esistono diversi modi per raccogliere e visualizzare le tracce degli eventi ETW WWSAPI a seconda della versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2f439-123">There are few different ways of collecting and viewing WWSAPI ETW event traces depending on the operating system version.</span></span>

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a><span data-ttu-id="2f439-124">Abilitazione e visualizzazione di tracce WWSAPI in Visualizzatore eventi (funziona in Windows Vista e versioni successive)</span><span class="sxs-lookup"><span data-stu-id="2f439-124">Enabling and Viewing WWSAPI traces in Event Viewer (works on Windows Vista and above)</span></span>

-   <span data-ttu-id="2f439-125">Eseguire eventvwr. msc dalla riga di comando o dal menu Esegui.</span><span class="sxs-lookup"><span data-stu-id="2f439-125">Run eventvwr.msc from command line or run menu.</span></span>
-   <span data-ttu-id="2f439-126">Fare clic sul collegamento Visualizza nel riquadro azioni a destra e abilitare l'opzione Mostra log analitici e debug.</span><span class="sxs-lookup"><span data-stu-id="2f439-126">Click the view link on the Actions pane on the right and enable Show Analytic and Debug logs option.</span></span>
-   <span data-ttu-id="2f439-127">Passare a registri applicazioni e servizi \\ \\ \\ provider di servizi di Microsoft Windows nel riquadro sinistro.</span><span class="sxs-lookup"><span data-stu-id="2f439-127">Browse to Application and Service Logs\\Microsoft\\Windows\\WebServices providers on the left pane.</span></span>
-   <span data-ttu-id="2f439-128">Fare clic con il pulsante destro del mouse sul provider di traccia e selezionare Abilita log.</span><span class="sxs-lookup"><span data-stu-id="2f439-128">Right click the Tracing provider and select Enable log.</span></span>
-   <span data-ttu-id="2f439-129">Eseguire lo scenario.</span><span class="sxs-lookup"><span data-stu-id="2f439-129">Run your scenario.</span></span>
-   <span data-ttu-id="2f439-130">Quando si aggiorna la pagina Visualizzatore eventi, è necessario iniziare a visualizzare le voci di traccia WWSAPI.</span><span class="sxs-lookup"><span data-stu-id="2f439-130">When you refresh the event viewer page, you should start seeing the WWSAPI tracing entries.</span></span>

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a><span data-ttu-id="2f439-131">Abilitazione e visualizzazione di tracce WWSAPI usando Wstrace.bat script (funziona in XPSP2 e versioni successive)</span><span class="sxs-lookup"><span data-stu-id="2f439-131">Enabling and Viewing WWSAPI traces using Wstrace.bat Script (works on XPSP2 and above)</span></span>

<span data-ttu-id="2f439-132">Il file batch wstrace.bat offre un modo pratico per:</span><span class="sxs-lookup"><span data-stu-id="2f439-132">The wstrace.bat batch file provides a convenient way to:</span></span>

-   <span data-ttu-id="2f439-133">Creazione di un registro di traccia</span><span class="sxs-lookup"><span data-stu-id="2f439-133">Create a trace log</span></span>
-   <span data-ttu-id="2f439-134">Eliminare un registro di traccia</span><span class="sxs-lookup"><span data-stu-id="2f439-134">Delete a trace log</span></span>
-   <span data-ttu-id="2f439-135">Abilitare e disabilitare la traccia</span><span class="sxs-lookup"><span data-stu-id="2f439-135">Enable and disable tracing</span></span>
-   <span data-ttu-id="2f439-136">Aggiornare il livello di traccia (info/Error/verbose)</span><span class="sxs-lookup"><span data-stu-id="2f439-136">Update the tracing level (info/error/verbose)</span></span>
-   <span data-ttu-id="2f439-137">Conversione dei log di traccia in file CSV</span><span class="sxs-lookup"><span data-stu-id="2f439-137">Converting trace logs to CSV files</span></span>

<span data-ttu-id="2f439-138">Il file batch USA logman.exe per tutti i comandi, ad eccezione della conversione dei log in un file CSV, che richiede uno strumento personalizzato (wstracedump.exe).</span><span class="sxs-lookup"><span data-stu-id="2f439-138">The batch file uses logman.exe for all commands, with the exception of converting the logs to CSV file, which requires a custom tool (wstracedump.exe).</span></span>

## <a name="using-tracing-commands"></a><span data-ttu-id="2f439-139">Uso di comandi di traccia</span><span class="sxs-lookup"><span data-stu-id="2f439-139">Using tracing commands</span></span>

<span data-ttu-id="2f439-140">Il comando che segue crea un log che usa il livello info, Error o Verbose.</span><span class="sxs-lookup"><span data-stu-id="2f439-140">The following command creates a log that uses info, error or verbose level.</span></span> <span data-ttu-id="2f439-141">Questo comando richiede privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="2f439-141">This command requires elevated privileges.</span></span>

<span data-ttu-id="2f439-142">**wstrace.bat crea \[ informazioni \| \| dettagliate errore\]**</span><span class="sxs-lookup"><span data-stu-id="2f439-142">**wstrace.bat create \[info \| error \| verbose\]**</span></span>

<span data-ttu-id="2f439-143">Il comando che segue elimina il log.</span><span class="sxs-lookup"><span data-stu-id="2f439-143">The following command deletes the log.</span></span> <span data-ttu-id="2f439-144">Questo comando richiede privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="2f439-144">This command requires elevated privileges.</span></span>

<span data-ttu-id="2f439-145">**Eliminazionewstrace.bat**</span><span class="sxs-lookup"><span data-stu-id="2f439-145">**wstrace.bat delete**</span></span>

<span data-ttu-id="2f439-146">Il comando seguente abilita la traccia.</span><span class="sxs-lookup"><span data-stu-id="2f439-146">The following command enables tracing.</span></span> <span data-ttu-id="2f439-147">È necessario innanzitutto creare un log.</span><span class="sxs-lookup"><span data-stu-id="2f439-147">You must first create a log.</span></span>

<span data-ttu-id="2f439-148">**wstrace.bat**</span><span class="sxs-lookup"><span data-stu-id="2f439-148">**wstrace.bat on**</span></span>

<span data-ttu-id="2f439-149">Il livello di traccia (info, Error o verbose) può essere modificato come segue:</span><span class="sxs-lookup"><span data-stu-id="2f439-149">The tracing level (info, error or verbose) can be modified as follows:</span></span>

<span data-ttu-id="2f439-150">**wstrace.bat \[ \| Dettagli errore informazioni \| aggiornamento\]**</span><span class="sxs-lookup"><span data-stu-id="2f439-150">**wstrace.bat update \[info \| error \| verbose\]**</span></span>

<span data-ttu-id="2f439-151">Per eseguire il dump dell'output della traccia, utilizzare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="2f439-151">To dump the trace output, use the following command:</span></span>

<span data-ttu-id="2f439-152">**wstrace.bat dump > temp.csv**</span><span class="sxs-lookup"><span data-stu-id="2f439-152">**wstrace.bat dump > temp.csv**</span></span>

<span data-ttu-id="2f439-153">Gli eventi verranno scaricati nel file CSV fino a quando non viene premuto CTRL + C o la traccia è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="2f439-153">The events will be dumped to the CSV file until Ctrl-C is pressed or tracing is disabled.</span></span>

## <a name="tracing-file-format"></a><span data-ttu-id="2f439-154">Formato file di traccia</span><span class="sxs-lookup"><span data-stu-id="2f439-154">Tracing File format</span></span>

<span data-ttu-id="2f439-155">I file CSV creati da wstrace.bat sono semplici file di testo con variabili separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="2f439-155">The CSV files created by wstrace.bat are simple comma-separated-variable text files.</span></span> <span data-ttu-id="2f439-156">Questi file possono essere aperti in Excel, blocco note e così via.</span><span class="sxs-lookup"><span data-stu-id="2f439-156">These files may be opened in Excel, Notepad, etc.</span></span>

<span data-ttu-id="2f439-157">Le colonne del file sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="2f439-157">The columns of the file are as follows:</span></span>

-   <span data-ttu-id="2f439-158">TimeStamp: TimeStamp del momento in cui è stato registrato l'evento</span><span class="sxs-lookup"><span data-stu-id="2f439-158">TimeStamp - Time stamp of when the event was recorded</span></span>
-   <span data-ttu-id="2f439-159">ProcessID-ID ULONG del processo che registra l'evento</span><span class="sxs-lookup"><span data-stu-id="2f439-159">ProcessID - ULONG ID of the process recording the event</span></span>
-   <span data-ttu-id="2f439-160">ThreadID-ID ULONG del thread che registra l'evento</span><span class="sxs-lookup"><span data-stu-id="2f439-160">ThreadID - ULONG ID of the thread recording the event</span></span>
-   <span data-ttu-id="2f439-161">Il valore enumerato per l'evento del tipo di evento può essere ("API Enter" " \| API Pending" \| "API ExitSyncSuccess" \| "API ExitSyncFailure" \| "API ExitAsyncSuccess" \| "API ExitAsyncFailure" " \| io Started" \| "io completed" \| "io failed" \| "Error" \| "received message Start" \| "received message" \| "received message stop" "invio del messaggio" "invio del messaggio" \| \| \| "invio del messaggio STOP")</span><span class="sxs-lookup"><span data-stu-id="2f439-161">Event - Enumerated value of the event type may be ("api enter" \| "api pending" \| "api ExitSyncSuccess" \| "api ExitSyncFailure" \| "api ExitAsyncSuccess" \| "api ExitAsyncFailure" \| "io started" \| "io completed" \| "io failed" \| "error" \| "received message start" \| "received message" \| "received message stop" \| "sending message start" \| "sending message" \| "sending message stop")</span></span>
-   <span data-ttu-id="2f439-162">Operation: il nome dell'operazione richiamata.</span><span class="sxs-lookup"><span data-stu-id="2f439-162">Operation - The name of the operation being invoked.</span></span> <span data-ttu-id="2f439-163">In genere viene eseguito il mapping all'API chiamata.</span><span class="sxs-lookup"><span data-stu-id="2f439-163">Typically this maps to the API being called.</span></span>
-   <span data-ttu-id="2f439-164">Errore-numero di errore HRESULT facoltativo</span><span class="sxs-lookup"><span data-stu-id="2f439-164">Error - Optional HRESULT error number</span></span>
-   <span data-ttu-id="2f439-165">Info: informazioni facoltative sull'evento</span><span class="sxs-lookup"><span data-stu-id="2f439-165">Info - Optional information about the event</span></span>

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a><span data-ttu-id="2f439-166">Raccolta del file di traccia WWSAPI ETW mediante gli strumenti ETW (funziona in XPSP2 e versioni successive)</span><span class="sxs-lookup"><span data-stu-id="2f439-166">Collecting WWSAPI ETW Trace File using ETW tools (works on XPSP2 and above)</span></span>

<span data-ttu-id="2f439-167">Abilitazione della traccia ETW per WWSAPI</span><span class="sxs-lookup"><span data-stu-id="2f439-167">Enabling ETW tracing for WWSAPI</span></span>

<span data-ttu-id="2f439-168">**logman start wstrace-BS 64-ft 1-RT-p Microsoft-Windows-WebServices \[ flags \[ level \] \] \[ -o <EtlLogFileName> \] -ETS**</span><span class="sxs-lookup"><span data-stu-id="2f439-168">**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices \[flags \[level\]\] \[-o <EtlLogFileName>\] -ets**</span></span>

<span data-ttu-id="2f439-169">per creare e avviare la sessione di traccia ETW.</span><span class="sxs-lookup"><span data-stu-id="2f439-169">to create and start the ETW tracing session.</span></span> <span data-ttu-id="2f439-170">Logman.exe è uno strumento ETW interno disponibile su tutte le piattaforme supportate.</span><span class="sxs-lookup"><span data-stu-id="2f439-170">Logman.exe is an in-box ETW tool available on all supported platforms.</span></span> <span data-ttu-id="2f439-171">Si noti che è necessario usare \_ \_ i servizi WebService di Microsoft Windows come nome del provider in xpsp2 e W2K3.</span><span class="sxs-lookup"><span data-stu-id="2f439-171">Note that you need to use Microsoft\_Windows\_WebServices as the provider name on XPSP2 and W2K3.</span></span> <span data-ttu-id="2f439-172">È possibile eseguire Logman query providers per visualizzare l'elenco dei provider registrati.</span><span class="sxs-lookup"><span data-stu-id="2f439-172">You can run logman query providers to see the list of registered providers.</span></span> <span data-ttu-id="2f439-173">È necessario elencare il provider Microsoft-Windows-WebServices (o Microsoft \_ Windows \_ WebServices), a meno che non sia registrato.</span><span class="sxs-lookup"><span data-stu-id="2f439-173">Microsoft-Windows-WebServices (or Microsoft\_Windows\_WebServices) provider should be listed unless it is not registered.</span></span> <span data-ttu-id="2f439-174">Il provider viene normalmente registrato durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="2f439-174">The provider is normally registered during setup.</span></span> <span data-ttu-id="2f439-175">Tuttavia, può anche essere registrato manualmente eseguendo wevtutil.exe im <ManifestFileName> (in Windows Vista e versioni successive) o mofcomp.exe <MofFileName> (in xpsp2 e W2K3).</span><span class="sxs-lookup"><span data-stu-id="2f439-175">However it can also be manually registered by running wevtutil.exe im <ManifestFileName> (on Windows Vista and Later) or mofcomp.exe <MofFileName> (on XPSP2 and W2K3).</span></span>

<span data-ttu-id="2f439-176">I flag possono essere utilizzati per filtrare le tracce in base al tipo.</span><span class="sxs-lookup"><span data-stu-id="2f439-176">Flags can be used to filter the traces by their kind.</span></span> <span data-ttu-id="2f439-177">Può essere o un valore dei seguenti tipi di traccia.</span><span class="sxs-lookup"><span data-stu-id="2f439-177">It can be OR'd value of the following trace kinds.</span></span> <span data-ttu-id="2f439-178">Se non è specificato, tutti i tipi di traccia sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="2f439-178">If not supplied, all trace kinds are enabled.</span></span>

-   <span data-ttu-id="2f439-179">0x1: tracce di ingresso/uscita API.</span><span class="sxs-lookup"><span data-stu-id="2f439-179">0x1 - API entry/exit traces.</span></span>
-   <span data-ttu-id="2f439-180">0x2-tracce di errore.</span><span class="sxs-lookup"><span data-stu-id="2f439-180">0x2 - Error traces.</span></span>
-   <span data-ttu-id="2f439-181">tracce di 0x4-IO.</span><span class="sxs-lookup"><span data-stu-id="2f439-181">0x4 - IO traces.</span></span>
-   <span data-ttu-id="2f439-182">0x8: tracce di messaggi SOAP.</span><span class="sxs-lookup"><span data-stu-id="2f439-182">0x8 - SOAP message traces.</span></span>
-   <span data-ttu-id="2f439-183">0x10: tracce di messaggi binari.</span><span class="sxs-lookup"><span data-stu-id="2f439-183">0x10 - Binary message traces.</span></span>

<span data-ttu-id="2f439-184">Il livello può essere utilizzato per filtrare le tracce in base al relativo livello.</span><span class="sxs-lookup"><span data-stu-id="2f439-184">Level can be used to filter the traces by their level.</span></span> <span data-ttu-id="2f439-185">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2f439-185">It should be one of the following values.</span></span> <span data-ttu-id="2f439-186">Se non è specificato, tutti i livelli di traccia sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="2f439-186">If not supplied, all trace levels are enabled.</span></span>

-   <span data-ttu-id="2f439-187">0x1-tracce irreversibili.</span><span class="sxs-lookup"><span data-stu-id="2f439-187">0x1 - Fatal traces.</span></span>
-   <span data-ttu-id="2f439-188">0x2-tracce di errore.</span><span class="sxs-lookup"><span data-stu-id="2f439-188">0x2 - Error traces.</span></span>
-   <span data-ttu-id="2f439-189">0x3-tracce di avviso.</span><span class="sxs-lookup"><span data-stu-id="2f439-189">0x3 - Warning traces.</span></span>
-   <span data-ttu-id="2f439-190">0x4-tracce informative.</span><span class="sxs-lookup"><span data-stu-id="2f439-190">0x4 - Informational traces.</span></span>
-   <span data-ttu-id="2f439-191">0x5-tracce dettagliate.</span><span class="sxs-lookup"><span data-stu-id="2f439-191">0x5 - Verbose traces.</span></span>

<span data-ttu-id="2f439-192">EtlLogFileName è il percorso del file di log eventi ETW da creare (usare l'estensione ETL).</span><span class="sxs-lookup"><span data-stu-id="2f439-192">EtlLogFileName is the path to the ETW event log file to be created (use .etl extension).</span></span> <span data-ttu-id="2f439-193">Se non viene specificato, ETW sceglie un nome casuale su cui è possibile eseguire query in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="2f439-193">If not provided, ETW will pick a random name which can be queried later.</span></span> <span data-ttu-id="2f439-194">Il file non deve trovarsi nella directory del profilo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2f439-194">This file should not reside on user's profile directory.</span></span> <span data-ttu-id="2f439-195">Il file di registro eventi ETW (file con estensione ETL) è in formato binario.</span><span class="sxs-lookup"><span data-stu-id="2f439-195">ETW event log file (.etl file) is in binary format.</span></span> <span data-ttu-id="2f439-196">Può essere utilizzato dalle applicazioni ETW, ma non è in formato leggibile.</span><span class="sxs-lookup"><span data-stu-id="2f439-196">It can be consumed by ETW applications, but it is not in human readable format.</span></span> <span data-ttu-id="2f439-197">Il passaggio successivo descrive come visualizzarne il contenuto.</span><span class="sxs-lookup"><span data-stu-id="2f439-197">Next step describes how to view its content.</span></span>

<span data-ttu-id="2f439-198">Eseguire lo scenario</span><span class="sxs-lookup"><span data-stu-id="2f439-198">Run your scenario</span></span>

<span data-ttu-id="2f439-199">Raccolta del file di registro eventi ETW.</span><span class="sxs-lookup"><span data-stu-id="2f439-199">Collecting ETW event log file.</span></span>

<span data-ttu-id="2f439-200">**logman stop wstrace-ETS**</span><span class="sxs-lookup"><span data-stu-id="2f439-200">**logman stop wstrace -ets**</span></span>

<span data-ttu-id="2f439-201">per arrestare la sessione di traccia ETW.</span><span class="sxs-lookup"><span data-stu-id="2f439-201">to stop the ETW tracing session.</span></span> <span data-ttu-id="2f439-202">Questo è il momento in cui ETW interrompe la registrazione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="2f439-202">This is when ETW stops logging the events.</span></span> <span data-ttu-id="2f439-203">Il file di registro eventi ETW (specificato nel parametro EtlLogFileName) è pronto per essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="2f439-203">ETW event log file (specified in EtlLogFileName parameter) is ready to consume.</span></span> <span data-ttu-id="2f439-204">Può essere visualizzato localmente (le istruzioni sono fornite di seguito) o inviato al gruppo di prodotti per l'analisi.</span><span class="sxs-lookup"><span data-stu-id="2f439-204">It can either be viewed locally (instructions are given below) or sent to the product group for investigation.</span></span>

<span data-ttu-id="2f439-205">Esempio end-to-end con gli strumenti ETW:</span><span class="sxs-lookup"><span data-stu-id="2f439-205">End to end example using ETW tools:</span></span>

<span data-ttu-id="2f439-206">**logman start wstrace-BS 64-ft 1-RT-p Microsoft-Windows-WebServices-o Trace. etl-ETS**</span><span class="sxs-lookup"><span data-stu-id="2f439-206">**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices -o mytrace.etl -ets**</span></span>

<span data-ttu-id="2f439-207">**Echo... eseguire lo scenario.**</span><span class="sxs-lookup"><span data-stu-id="2f439-207">**echo .. run your scenario..**</span></span>

<span data-ttu-id="2f439-208">**logman stop wstrace-ETS**</span><span class="sxs-lookup"><span data-stu-id="2f439-208">**logman stop wstrace -ets**</span></span>

<span data-ttu-id="2f439-209">**tracerpt di traccia. etl-o mytrace.xml**</span><span class="sxs-lookup"><span data-stu-id="2f439-209">**tracerpt mytrace.etl -o mytrace.xml**</span></span>

<span data-ttu-id="2f439-210">**wstrace.htm**</span><span class="sxs-lookup"><span data-stu-id="2f439-210">**wstrace.htm**</span></span>

<span data-ttu-id="2f439-211">**Echo... utilizzare mytrace.xml e wstrace. xsl nella pagina aperta.**</span><span class="sxs-lookup"><span data-stu-id="2f439-211">**echo .. use mytrace.xml and wstrace.xsl in the opened page ..**</span></span>

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a><span data-ttu-id="2f439-212">Visualizzazione delle tracce del file di traccia WWSAPI ETW mediante lo strumento wstracedump.exe (funziona in Windows XP e versioni successive)</span><span class="sxs-lookup"><span data-stu-id="2f439-212">Viewing WWSAPI ETW Trace File traces using wstracedump.exe tool (works on Windows XP and above)</span></span>

<span data-ttu-id="2f439-213">Wstracedump.exe è uno strumento di consumer ETW sviluppato personalizzato che elabora gli eventi nel file di traccia WWSAPI ETW e produce un output leggibile.</span><span class="sxs-lookup"><span data-stu-id="2f439-213">Wstracedump.exe is a custom developed ETW consumer tool which processes events in the WWSAPI ETW trace file and produces human readable output.</span></span> <span data-ttu-id="2f439-214">Può produrre output da tutte le piattaforme supportate.</span><span class="sxs-lookup"><span data-stu-id="2f439-214">It can produce output from all supported platforms.</span></span> <span data-ttu-id="2f439-215">Per ulteriori informazioni, vedere l'utilizzo (wstracedump.exe-?).</span><span class="sxs-lookup"><span data-stu-id="2f439-215">See its usage (wstracedump.exe -?) for more information.</span></span>

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a><span data-ttu-id="2f439-216">Visualizzazione delle tracce del file di traccia di WWSAPI ETW mediante gli strumenti ETW (funziona in Windows Vista e versioni successive)</span><span class="sxs-lookup"><span data-stu-id="2f439-216">Viewing WWSAPI ETW Trace File traces using ETW tools (works on Windows Vista and above)</span></span>

<span data-ttu-id="2f439-217">Tracerpt.exe è lo strumento per visualizzare il contenuto di un file di log eventi ETW e disponibile in tutte le piattaforme supportate.</span><span class="sxs-lookup"><span data-stu-id="2f439-217">Tracerpt.exe is the tool to view the content of an ETW event log file and available on all supported platforms.</span></span> <span data-ttu-id="2f439-218">Può essere utilizzato per generare file di dump CSV, EVTX o XML da un file di log eventi ETW.</span><span class="sxs-lookup"><span data-stu-id="2f439-218">It can be used to generate CSV, EVTX or XML dump files from an ETW event log file.</span></span> <span data-ttu-id="2f439-219">Tuttavia, il file di output generato ha tracce leggibili solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2f439-219">However the generated output file has human readable traces only on Windows Vista and later.</span></span> <span data-ttu-id="2f439-220">Queste istruzioni illustrano come generare il file di dump XML e usarlo insieme a un file XSL per visualizzare le tracce in un formato gradevole (il file XSL è molto semplice e può essere modificato se si desiderano formati diversi).</span><span class="sxs-lookup"><span data-stu-id="2f439-220">These instructions describes how to generate the XML dump file and use it along with an xsl file to display the traces in a nice format (xsl file is very trivial and may be altered if different formats are desired).</span></span>

-   <span data-ttu-id="2f439-221">Esegui</span><span class="sxs-lookup"><span data-stu-id="2f439-221">Run</span></span>

    <span data-ttu-id="2f439-222">**tracerpt <EtlLogFileName> -o <OutputXMLFileName>**</span><span class="sxs-lookup"><span data-stu-id="2f439-222">**tracerpt <EtlLogFileName> -o <OutputXMLFileName>**</span></span>

    <span data-ttu-id="2f439-223">per creare un dump XML dal file ETL binario (tracerpt.exe crea il file di output in formato XML per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2f439-223">to create an XML dump from the binary ETL file (tracerpt.exe creates the output file in XML format by default.</span></span> <span data-ttu-id="2f439-224">Eseguire tracerpt-?</span><span class="sxs-lookup"><span data-stu-id="2f439-224">Run tracerpt -?</span></span> <span data-ttu-id="2f439-225">Per visualizzare altri formati disponibili).</span><span class="sxs-lookup"><span data-stu-id="2f439-225">To see other available formats).</span></span>

-   <span data-ttu-id="2f439-226">A questo punto, è possibile visualizzare le informazioni di traccia nel file XML.</span><span class="sxs-lookup"><span data-stu-id="2f439-226">At this point, you can see the tracing information in the XML file.</span></span> <span data-ttu-id="2f439-227">Inoltre, è possibile aprire il file di wstrace.htm e utilizzare il file di dump XML e il file wstrace. xsl per visualizzare le tracce in un formato più gradevole.</span><span class="sxs-lookup"><span data-stu-id="2f439-227">Additionally, you can open the wstrace.htm file and use the xml dump file and the wstrace.xsl file to see the traces in a nicer format.</span></span> <span data-ttu-id="2f439-228">Si noti che i file devono trovarsi nel computer locale per poter usare questo file HTML in IE.</span><span class="sxs-lookup"><span data-stu-id="2f439-228">Note that the files need to be on the local machine to be able to use this html file on IE.</span></span>

## <a name="security"></a><span data-ttu-id="2f439-229">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="2f439-229">Security</span></span>

<span data-ttu-id="2f439-230">Quando si Abilita la funzionalità di traccia, gli amministratori devono tenere in considerazione il consumo di spazio su disco e la potenza di calcolo.</span><span class="sxs-lookup"><span data-stu-id="2f439-230">When enabling tracing, administrators should take into account that it consumes additional disk space and computation power.</span></span> <span data-ttu-id="2f439-231">Un'applicazione o un client dannoso può esaurire le risorse di sistema a meno che le impostazioni di traccia non siano configurate con limiti</span><span class="sxs-lookup"><span data-stu-id="2f439-231">A malicious client or application may exhaust system resources unless tracing settings are configured with reasonable limits.</span></span> <span data-ttu-id="2f439-232">Quando si utilizza la funzionalità di traccia dei messaggi, i messaggi che contengono informazioni riservate, ad esempio credenziali, informazioni personali e così via, possono essere salvati in modo permanente sul disco o essere visualizzati da chiunque abbia accesso al Visualizzatore eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="2f439-232">When using message tracing feature, messages carrying sensitive information such as credentials, personal information, etc. may be persisted to the disk or be viewed by anyone who has access to the system event viewer.</span></span> <span data-ttu-id="2f439-233">Per ovviare a questo problema, la traccia può essere abilitata dagli utenti di sistema o amministratore in Windows 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2f439-233">As a mitigation to this issue, tracing can be enabled by System or Administrator users on Windows 2003 and later.</span></span> <span data-ttu-id="2f439-234">La traccia dei messaggi è disabilitata in Windows XP su cui qualsiasi utente può attivare la traccia.</span><span class="sxs-lookup"><span data-stu-id="2f439-234">Message tracing is disabled on Windows XP on which any user can turn tracing on.</span></span>

<span data-ttu-id="2f439-235">La seguente enumerazione viene utilizzata con la traccia:</span><span class="sxs-lookup"><span data-stu-id="2f439-235">The following enumeration is used with tracing:</span></span>

-   [<span data-ttu-id="2f439-236">**\_API di traccia WS \_**</span><span class="sxs-lookup"><span data-stu-id="2f439-236">**WS\_TRACE\_API**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




