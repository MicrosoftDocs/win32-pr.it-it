---
description: A partire da Windows Vista, il servizio WMI non utilizza i file di log WMI. USA invece Event Tracing for Windows (ETW) ed eventi sono disponibili tramite Visualizzatore eventi o lo strumento da riga di comando wevtutil.
ms.assetid: bb6401e8-caf7-4f39-ab64-b7532723ce9a
ms.tgt_platform: multiple
title: Traccia dell'attività WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14371a4f18b81019073cd2b428500b12385719e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758006"
---
# <a name="tracing-wmi-activity"></a><span data-ttu-id="daeb3-104">Traccia dell'attività WMI</span><span class="sxs-lookup"><span data-stu-id="daeb3-104">Tracing WMI Activity</span></span>

<span data-ttu-id="daeb3-105">A partire da Windows Vista, il servizio WMI non utilizza i [file di log WMI](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="daeb3-105">Starting with Windows Vista, the WMI service does not use the [WMI Log Files](wmi-log-files.md).</span></span> <span data-ttu-id="daeb3-106">USA invece [Event Tracing for Windows (ETW)](/windows/desktop/ETW/event-tracing-portal) ed eventi sono disponibili tramite **Visualizzatore eventi** o lo strumento da riga di comando wevtutil.</span><span class="sxs-lookup"><span data-stu-id="daeb3-106">Instead, it uses [Event Tracing for Windows (ETW)](/windows/desktop/ETW/event-tracing-portal) and events are available through **Event Viewer** or the Wevtutil command-line tool.</span></span>

<span data-ttu-id="daeb3-107">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="daeb3-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="daeb3-108">Recupero di eventi WMI tramite Visualizzatore eventi</span><span class="sxs-lookup"><span data-stu-id="daeb3-108">Obtaining WMI Events Through Event Viewer</span></span>](#obtaining-wmi-events-through-event-viewer)
-   [<span data-ttu-id="daeb3-109">Abilitazione della traccia WMI al prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="daeb3-109">Enabling WMI Tracing at Command Prompt</span></span>](#enabling-wmi-tracing-at-command-prompt)
-   [<span data-ttu-id="daeb3-110">Uso della traccia WMI basata su WPP</span><span class="sxs-lookup"><span data-stu-id="daeb3-110">Using WPP-based WMI Tracing</span></span>](#using-wpp-based-wmi-tracing)
-   [<span data-ttu-id="daeb3-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="daeb3-111">Related topics</span></span>](#related-topics)

## <a name="obtaining-wmi-events-through-event-viewer"></a><span data-ttu-id="daeb3-112">Recupero di eventi WMI tramite Visualizzatore eventi</span><span class="sxs-lookup"><span data-stu-id="daeb3-112">Obtaining WMI Events Through Event Viewer</span></span>

<span data-ttu-id="daeb3-113">Il file WMITracing. log contiene gli eventi tracciati da WMI.</span><span class="sxs-lookup"><span data-stu-id="daeb3-113">The WMITracing.log file contains the events that WMI traces.</span></span> <span data-ttu-id="daeb3-114">Tuttavia, si tratta di un file binario.</span><span class="sxs-lookup"><span data-stu-id="daeb3-114">However, this is a binary file.</span></span> <span data-ttu-id="daeb3-115">Per visualizzare questi eventi in un formato leggibile dagli utenti, utilizzare il **Visualizzatore eventi**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-115">To see these events in a format readable by humans, use the **Event Viewer**.</span></span>

<span data-ttu-id="daeb3-116">Per impostazione predefinita, gli eventi WMI non vengono tracciati.</span><span class="sxs-lookup"><span data-stu-id="daeb3-116">By default, WMI events are not traced.</span></span> <span data-ttu-id="daeb3-117">In questa procedura viene descritto come utilizzare **Visualizzatore eventi** per abilitare la traccia eventi WMI e individuare gli eventi WMI.</span><span class="sxs-lookup"><span data-stu-id="daeb3-117">This procedure describes how to use **Event Viewer** to enable WMI event tracing and locate WMI events.</span></span> <span data-ttu-id="daeb3-118">È possibile eseguire le stesse operazioni tramite lo strumento da riga di comando wevtutil.</span><span class="sxs-lookup"><span data-stu-id="daeb3-118">You can do the same operations through the wevtutil command-line tool.</span></span>

<span data-ttu-id="daeb3-119">**Per visualizzare gli eventi WMI in Visualizzatore eventi**</span><span class="sxs-lookup"><span data-stu-id="daeb3-119">**To view WMI Events in Event Viewer**</span></span>

1.  <span data-ttu-id="daeb3-120">Aprire **Visualizzatore eventi**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-120">Open **Event Viewer**.</span></span> <span data-ttu-id="daeb3-121">Dal menu **Visualizza** scegliere **Visualizza registri analitici e di debug**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-121">On the **View** menu, click **Show Analytic and Debug Logs**.</span></span> <span data-ttu-id="daeb3-122">Individuare il registro del canale di **traccia** per WMI in registri applicazioni e servizi \| \| attività Microsoft Windows \| WMI.</span><span class="sxs-lookup"><span data-stu-id="daeb3-122">Locate the **Trace** channel log for WMI under Applications and Service Logs \| Microsoft \| Windows \| WMI Activity.</span></span>
2.  <span data-ttu-id="daeb3-123">Fare clic con il pulsante destro del mouse sul registro **traccia** e selezionare **proprietà log**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-123">Right-click the **Trace** log and select **Log Properties**.</span></span> <span data-ttu-id="daeb3-124">Fare clic sulla casella di controllo **Abilita registrazione** per avviare la traccia eventi WMI.</span><span class="sxs-lookup"><span data-stu-id="daeb3-124">Click the **Enable Logging** check box to start the WMI event tracing.</span></span> <span data-ttu-id="daeb3-125">Per ulteriori informazioni sui canali, vedere [log eventi e canali nel registro eventi di Windows](/previous-versions//aa385225(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="daeb3-125">For more information about channels, see [Event Logs and Channels in Windows Event Log](/previous-versions//aa385225(v=vs.85)).</span></span>
3.  <span data-ttu-id="daeb3-126">Gli eventi WMI vengono visualizzati nella finestra evento per **WMI-Activity**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-126">WMI events appear in the event window for **WMI-Activity**.</span></span> <span data-ttu-id="daeb3-127">Fare doppio clic su un evento nell'elenco per visualizzare le informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="daeb3-127">Double-click an event in the list to see the detailed information.</span></span> <span data-ttu-id="daeb3-128">È possibile visualizzare un evento in una **visualizzazione XML** o in un formato di **visualizzazione descrittivo** .</span><span class="sxs-lookup"><span data-stu-id="daeb3-128">You can view an event in **XML View** or in **Friendly View** format.</span></span>

<span data-ttu-id="daeb3-129">Nel campo **ID evento** viene visualizzato un valore che contiene le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="daeb3-129">The **Event ID** field displays a value that contains the following information.</span></span>

<dl> <dt>

<span data-ttu-id="daeb3-130"><span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Evento 1</span><span class="sxs-lookup"><span data-stu-id="daeb3-130"><span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Event 1</span></span>
</dt> <dd>

<span data-ttu-id="daeb3-131">Inizio della sequenza di eventi per un'operazione specifica.</span><span class="sxs-lookup"><span data-stu-id="daeb3-131">Start of the event sequence for a specific operation.</span></span> <span data-ttu-id="daeb3-132">Una occorrenza per ogni sequenza.</span><span class="sxs-lookup"><span data-stu-id="daeb3-132">One occurrence for each sequence.</span></span>

<span data-ttu-id="daeb3-133">I campi evento per un evento 1 sono:</span><span class="sxs-lookup"><span data-stu-id="daeb3-133">The event fields for an Event 1 are:</span></span>

-   <span data-ttu-id="daeb3-134">**GroupOperationID** è un identificatore univoco usato per tutti gli eventi segnalati per un client specifico.</span><span class="sxs-lookup"><span data-stu-id="daeb3-134">**GroupOperationID** is a unique identifier that is used for all events reported for a specific client.</span></span>
-   <span data-ttu-id="daeb3-135">**OperationId** indica la sequenza di operazioni.</span><span class="sxs-lookup"><span data-stu-id="daeb3-135">**OperationId** indicates the operation sequence.</span></span>
-   <span data-ttu-id="daeb3-136">L' **operazione** specifica la connessione o la richiesta a WMI.</span><span class="sxs-lookup"><span data-stu-id="daeb3-136">**Operation** specifies the connection or request to WMI.</span></span>
-   <span data-ttu-id="daeb3-137">L' **utente** indica l'account che effettua una richiesta a WMI eseguendo uno script o CIM Studio.</span><span class="sxs-lookup"><span data-stu-id="daeb3-137">**User** indicates the account that makes a request to WMI by running a script or through CIM Studio.</span></span>
-   <span data-ttu-id="daeb3-138">**Spazio dei nomi** Mostra lo spazio dei nomi WMI a cui viene eseguita la connessione.</span><span class="sxs-lookup"><span data-stu-id="daeb3-138">**Namespace** shows the WMI namespace to which the connection is made.</span></span>

<span data-ttu-id="daeb3-139">Uno script può ad esempio richiedere tutte le istanze di una classe WMI, ad esempio il [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="daeb3-139">For example, a script may request all the instances of a WMI class, such as [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span> <span data-ttu-id="daeb3-140">La prima operazione può essere una connessione a WMI.</span><span class="sxs-lookup"><span data-stu-id="daeb3-140">The first operation may be a connection to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="daeb3-141"><span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Evento 2</span><span class="sxs-lookup"><span data-stu-id="daeb3-141"><span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Event 2</span></span>
</dt> <dd>

<span data-ttu-id="daeb3-142">Eventi che costituiscono l'operazione.</span><span class="sxs-lookup"><span data-stu-id="daeb3-142">Events that make up the operation.</span></span> <span data-ttu-id="daeb3-143">Una o più occorrenze nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="daeb3-143">One or more occurrences in the sequence.</span></span>

<span data-ttu-id="daeb3-144">I campi evento per un evento 2 sono:</span><span class="sxs-lookup"><span data-stu-id="daeb3-144">The event fields for an Event 2 are:</span></span>

-   <span data-ttu-id="daeb3-145">**GroupOperationID** indica la sequenza in cui si verifica l'evento.</span><span class="sxs-lookup"><span data-stu-id="daeb3-145">**GroupOperationID** indicates the sequence in which the event occurs.</span></span>
-   <span data-ttu-id="daeb3-146">**GroupOperationID** indica la sequenza in cui si verifica l'evento.</span><span class="sxs-lookup"><span data-stu-id="daeb3-146">**GroupOperationID** indicates the sequence in which the event occurs.</span></span>
-   <span data-ttu-id="daeb3-147">**ProviderName** indica il nome del provider che fornisce i dati.</span><span class="sxs-lookup"><span data-stu-id="daeb3-147">**ProviderName** indicates the name of the provider which supplies the data.</span></span>
-   <span data-ttu-id="daeb3-148">**Path** è il percorso WMI dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="daeb3-148">**Path** is the WMI path to the object.</span></span>

<span data-ttu-id="daeb3-149">Ad esempio, l'operazione può essere un'enumerazione del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="daeb3-149">For example, the operation may be an enumeration of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="daeb3-150"><span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Evento 3</span><span class="sxs-lookup"><span data-stu-id="daeb3-150"><span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Event 3</span></span>
</dt> <dd>

<span data-ttu-id="daeb3-151">Fine della sequenza di eventi per un'operazione specifica.</span><span class="sxs-lookup"><span data-stu-id="daeb3-151">End of the event sequence for a specific operation.</span></span> <span data-ttu-id="daeb3-152">Una occorrenza per ogni sequenza.</span><span class="sxs-lookup"><span data-stu-id="daeb3-152">One occurrence for each sequence.</span></span>

<span data-ttu-id="daeb3-153">Viene visualizzato solo **GroupOperationID** .</span><span class="sxs-lookup"><span data-stu-id="daeb3-153">Only the **GroupOperationID** is shown.</span></span>

</dd> </dl>

## <a name="enabling-wmi-tracing-at-command-prompt"></a><span data-ttu-id="daeb3-154">Abilitazione della traccia WMI al prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="daeb3-154">Enabling WMI Tracing at Command Prompt</span></span>

<span data-ttu-id="daeb3-155">È inoltre possibile abilitare la traccia eventi WMI tramite lo strumento da riga di comando wevtutil.</span><span class="sxs-lookup"><span data-stu-id="daeb3-155">You can also enable WMI event tracing through the Wevtutil command-line tool.</span></span> <span data-ttu-id="daeb3-156">Usare il comando seguente: **Wevtutil.exe SL Microsoft-Windows-WMI-Activity/Trace/e: true**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-156">Use the following command: **Wevtutil.exe sl Microsoft-Windows-WMI-Activity/Trace /e:true**.</span></span> <span data-ttu-id="daeb3-157">L'origine evento WMI è Microsoft-Windows-WMI.</span><span class="sxs-lookup"><span data-stu-id="daeb3-157">The WMI event source is Microsoft-Windows-WMI.</span></span> <span data-ttu-id="daeb3-158">Per ulteriori informazioni su Wevtutil.exe, vedere [informazioni sul registro eventi di Windows](/previous-versions//aa382610(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="daeb3-158">For more information about Wevtutil.exe, see [About Windows Event Log](/previous-versions//aa382610(v=vs.85)).</span></span>

## <a name="using-wpp-based-wmi-tracing"></a><span data-ttu-id="daeb3-159">Uso della traccia WMI basata su WPP</span><span class="sxs-lookup"><span data-stu-id="daeb3-159">Using WPP-based WMI Tracing</span></span>

<span data-ttu-id="daeb3-160">Nei sistemi operativi Windows a partire da Windows Vista, WMI crea un canale di traccia attivo durante il processo di avvio.</span><span class="sxs-lookup"><span data-stu-id="daeb3-160">In Windows operating systems starting with Windows Vista, WMI creates an active trace channel during the boot process.</span></span> <span data-ttu-id="daeb3-161">Il nome del canale è la \_ sessione di traccia WMI \_ .</span><span class="sxs-lookup"><span data-stu-id="daeb3-161">The name of the channel is WMI\_Trace\_Session.</span></span> <span data-ttu-id="daeb3-162">Solo gli errori vengono registrati nel canale.</span><span class="sxs-lookup"><span data-stu-id="daeb3-162">Only errors are logged to the channel.</span></span>

<span data-ttu-id="daeb3-163">Il preprocessore di traccia software Windows (WPP) registra le informazioni in un file binario.</span><span class="sxs-lookup"><span data-stu-id="daeb3-163">The Windows software trace preprocessor (WPP) records information in a binary file.</span></span> <span data-ttu-id="daeb3-164">Per leggere il file, è innanzitutto necessario convertirlo in un formato di testo leggibile.</span><span class="sxs-lookup"><span data-stu-id="daeb3-164">To read the file, you must first translate it into a readable, text format.</span></span> <span data-ttu-id="daeb3-165">Per eseguire la traduzione, utilizzare uno strumento denominato tracefmt.exe dal [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) .</span><span class="sxs-lookup"><span data-stu-id="daeb3-165">You use a tool called tracefmt.exe from the [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) to do the translation.</span></span> <span data-ttu-id="daeb3-166">Lo strumento richiede informazioni archiviate in alcuni file associati.</span><span class="sxs-lookup"><span data-stu-id="daeb3-166">The tool requires information stored in some associated files.</span></span> <span data-ttu-id="daeb3-167">I file si trovano nella directory% SystemRoot% \\ system32 \\ WBEM \\ MDF e hanno l'estensione del nome di file MDF.</span><span class="sxs-lookup"><span data-stu-id="daeb3-167">The files are located in the %SystemRoot%\\System32\\wbem\\tmf directory and have a .tmf file name extension.</span></span> <span data-ttu-id="daeb3-168">Lo strumento richiede effettivamente un solo file con estensione MDF.</span><span class="sxs-lookup"><span data-stu-id="daeb3-168">The tool actually requires a single .tmf file .</span></span> <span data-ttu-id="daeb3-169">Il file viene creato concatenando tutti i file con estensione MDF in un altro file con estensione MDF.</span><span class="sxs-lookup"><span data-stu-id="daeb3-169">You make that single file by concatenating all of the .tmf files into another .tmf file.</span></span> <span data-ttu-id="daeb3-170">Per ulteriori informazioni sui file con estensione MDF, vedere [file di formato del messaggio di traccia](/windows-hardware/drivers/devtest/trace-message-format-file).</span><span class="sxs-lookup"><span data-stu-id="daeb3-170">For more information about .tmf files, see [Trace Message Format File](/windows-hardware/drivers/devtest/trace-message-format-file).</span></span>

<span data-ttu-id="daeb3-171">Dopo l'installazione di [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) per ottenere la tracelog.exe e tracefmt.exe gli strumenti da riga di comando, eseguire la procedura seguente per raccogliere una traccia WMI basata su WPP.</span><span class="sxs-lookup"><span data-stu-id="daeb3-171">After installing the [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) to get the tracelog.exe and tracefmt.exe command-line tools, perform the following steps to collect a WPP-based WMI trace.</span></span>

<span data-ttu-id="daeb3-172">**Per visualizzare una traccia WMI basata su WPP**</span><span class="sxs-lookup"><span data-stu-id="daeb3-172">**To view a WPP-based WMI trace**</span></span>

1.  <span data-ttu-id="daeb3-173">Per creare il singolo file con estensione MDF, aprire una finestra del prompt dei comandi con privilegi elevati e passare alla directory% SystemRoot% \\ system32 \\ WBEM \\ MDF.</span><span class="sxs-lookup"><span data-stu-id="daeb3-173">To create the single .tmf file, open an elevated Command Prompt window and navigate to the %SystemRoot%\\System32\\wbem\\tmf directory.</span></span>

2.  <span data-ttu-id="daeb3-174">Digitare **copy/y% SystemRoot% \\ system32 \\ WBEM \\ MDF \\ \* . MDF% SystemRoot% \\ system32 \\ WBEM \\ MDF \\ WMI. MDF**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-174">Type **copy /y %SystemRoot%\\System32\\wbem\\tmf\\\*.tmf %SystemRoot%\\System32\\wbem\\tmf\\wmi.tmf**.</span></span> <span data-ttu-id="daeb3-175">Verrà creato un file denominato WMI. mdf che include il contenuto di tutti gli altri file con estensione MDF.</span><span class="sxs-lookup"><span data-stu-id="daeb3-175">This will create a file named wmi.tmf that includes the contents of all of the other .tmf files.</span></span>

3.  <span data-ttu-id="daeb3-176">Digitare **tracelog-Flush WMI \_ trace \_ Session**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-176">Type **tracelog -flush WMI\_Trace\_Session**.</span></span> <span data-ttu-id="daeb3-177">I buffer WPP sul disco vengono scaricati.</span><span class="sxs-lookup"><span data-stu-id="daeb3-177">This will flush the WPP buffers on the disk.</span></span>
4.  <span data-ttu-id="daeb3-178">Digitare il **prefisso del formato di traccia \_ \_ = \[ %9! d! \] %8! 04X!. %3! 04X!. %3! 04X!:: %4! s! \[ %1! s! \] (%! COMPname!:%! FUNC!: %2! s!)**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-178">Type **set TRACE\_FORMAT\_PREFIX = \[%9!d!\]%8!04X!.%3!04X!.%3!04X!::%4!s!\[%1!s!\](%!COMPNAME!:%!FUNC !:%2!s!)**.</span></span> <span data-ttu-id="daeb3-179">Lo strumento tracefmt aggiunge alcune informazioni predefinite a ogni messaggio di traccia.</span><span class="sxs-lookup"><span data-stu-id="daeb3-179">The tracefmt tool adds some default information to each trace message.</span></span> <span data-ttu-id="daeb3-180">È possibile configurare le informazioni incluse impostando la variabile di \_ \_ ambiente prefisso formato traccia.</span><span class="sxs-lookup"><span data-stu-id="daeb3-180">You can configure what information is included by setting the TRACE\_FORMAT\_PREFIX environment variable.</span></span> <span data-ttu-id="daeb3-181">Per ulteriori informazioni sulla sintassi utilizzata, vedere il [prefisso del messaggio di traccia](https://msdn.microsoft.com/library/aa139695.aspx).</span><span class="sxs-lookup"><span data-stu-id="daeb3-181">To learn about the syntax used, see [Trace Message Prefix](https://msdn.microsoft.com/library/aa139695.aspx).</span></span>
5.  <span data-ttu-id="daeb3-182">Digitare **tracefmt-MDF% SystemRoot% \\ system32 \\ WBEM \\ MDF \\ wmi. MDF-o OUTPUT.TXT% SystemRoot% \\ system32 \\ \\ log \\ WMITracing. log**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-182">Type **tracefmt -tmf %systemroot%\\system32\\wbem\\tmf\\wmi.tmf -o OUTPUT.TXT %systemroot%\\system32\\wbem\\logs\\WMITracing.log**.</span></span> <span data-ttu-id="daeb3-183">In questo modo viene eseguita la conversione dal formato binario al formato testo leggibile.</span><span class="sxs-lookup"><span data-stu-id="daeb3-183">This performs the translation from binary format to readable text format.</span></span>
6.  <span data-ttu-id="daeb3-184">Digitare **notepad% systemroot% \\ system32 \\ WBEM \\ MDF \\OUTPUT.TXT**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-184">Type **notepad %systemroot%\\system32\\wbem\\tmf\\OUTPUT.TXT**.</span></span> <span data-ttu-id="daeb3-185">Il file di traccia verrà aperto nel blocco note.</span><span class="sxs-lookup"><span data-stu-id="daeb3-185">This will open the trace file in Notepad.</span></span>

<span data-ttu-id="daeb3-186">Di seguito sono riportate alcune altre attività correlate a WPP che può essere necessario eseguire.</span><span class="sxs-lookup"><span data-stu-id="daeb3-186">The following are some other WPP-related tasks you might need to perform.</span></span>

<span data-ttu-id="daeb3-187">**Per arrestare la traccia WMI basata su WPP**</span><span class="sxs-lookup"><span data-stu-id="daeb3-187">**To stop WPP-based WMI tracing**</span></span>

-   <span data-ttu-id="daeb3-188">Digitare **tracelog-stop WMI \_ trace \_ Session**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-188">Type **tracelog -stop WMI\_Trace\_Session**.</span></span>

<span data-ttu-id="daeb3-189">**Per avviare la traccia WMI basata su WPP**</span><span class="sxs-lookup"><span data-stu-id="daeb3-189">**To start WPP-based WMI tracing**</span></span>

-   <span data-ttu-id="daeb3-190">Digitare **tracelog-Start WMI \_ trace \_ Session-GUID \# 1FF6B227-2CA7-40F9-9A66-980EADAA602E-RT-Level 5-flag 0x7-f Trace. CONTENITORE** di</span><span class="sxs-lookup"><span data-stu-id="daeb3-190">Type **tracelog -start WMI\_Trace\_Session -guid \#1FF6B227-2CA7-40f9-9A66-980EADAA602E -rt -level 5 -flag 0x7 -f MYTRACE.BIN**</span></span>

<span data-ttu-id="daeb3-191">**Windows Vista:** Per impostazione predefinita, la traccia WMI basata su WPP è impostata sul livello 2, che include solo i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="daeb3-191">**Windows Vista:** By default, WPP-based WMI tracing is set to level 2 which includes only error messages.</span></span> <span data-ttu-id="daeb3-192">Per includere anche i messaggi informativi, impostare il livello su 4.</span><span class="sxs-lookup"><span data-stu-id="daeb3-192">To include informational messages as well, set the level to 4.</span></span> <span data-ttu-id="daeb3-193">Per impostazione predefinita, tutte le aree di WMI sono tracciate.</span><span class="sxs-lookup"><span data-stu-id="daeb3-193">All areas of WMI are traced by default.</span></span> <span data-ttu-id="daeb3-194">Sono disponibili tre aree distinte che è possibile tracciare: Core (flag = 0x1), ESS (flag = 0x2) e prov (flag = 0x4).</span><span class="sxs-lookup"><span data-stu-id="daeb3-194">There are three distinct areas that can be traced: Core (flag=0x1), ESS (flag=0x2) and Prov (flag=0x4).</span></span> <span data-ttu-id="daeb3-195">Nel comando di avvio sopra riportato, il **flag 0x7** causa la traccia di tutte e tre le aree.</span><span class="sxs-lookup"><span data-stu-id="daeb3-195">In the start command above, **flag 0x7** causes all three areas to be traced.</span></span>

<span data-ttu-id="daeb3-196">**Windows 7:** Per impostazione predefinita, la traccia WMI basata su WPP è disabilitata e impostata sul livello 0.</span><span class="sxs-lookup"><span data-stu-id="daeb3-196">**Windows 7:** By default, WPP-based WMI tracing is disabled and set to level 0.</span></span> <span data-ttu-id="daeb3-197">Per utilizzare la traccia WMI basata su WPP, questa funzionalità deve essere abilitata e impostata su livello 2 per i messaggi di errore o livello 4 per i messaggi di errore e informativi.</span><span class="sxs-lookup"><span data-stu-id="daeb3-197">To use WPP-based WMI tracing, this feature must be enabled and set to either level 2 for error messages or level 4 for both error and informational messages.</span></span>

<span data-ttu-id="daeb3-198">**Per elencare tutte le sessioni di traccia WPP**</span><span class="sxs-lookup"><span data-stu-id="daeb3-198">**To list all WPP trace sessions**</span></span>

-   <span data-ttu-id="daeb3-199">Digitare **tracelog-l**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-199">Type **tracelog -l**.</span></span>

<span data-ttu-id="daeb3-200">**Per elencare le informazioni sulla sessione di traccia WMI WPP**</span><span class="sxs-lookup"><span data-stu-id="daeb3-200">**To list info about the WMI WPP trace session**</span></span>

-   <span data-ttu-id="daeb3-201">Digitare **tracelog-l \| findstr/i "WMI \_ Trace"**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-201">Type **tracelog -l \| findstr /i "wmi\_trace"**.</span></span>

<span data-ttu-id="daeb3-202">**Per visualizzare i parametri della sessione di traccia WMI WPP**</span><span class="sxs-lookup"><span data-stu-id="daeb3-202">**To view the WMI WPP trace session parameters**</span></span>

-   <span data-ttu-id="daeb3-203">Digitare **tracelog-q WMI \_ trace \_ Session**.</span><span class="sxs-lookup"><span data-stu-id="daeb3-203">Type **tracelog -q WMI\_Trace\_Session**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="daeb3-204">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="daeb3-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daeb3-205">Risoluzione dei problemi WMI</span><span class="sxs-lookup"><span data-stu-id="daeb3-205">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="daeb3-206">File di log WMI</span><span class="sxs-lookup"><span data-stu-id="daeb3-206">WMI Log Files</span></span>](wmi-log-files.md)
</dt> </dl>

 

 
