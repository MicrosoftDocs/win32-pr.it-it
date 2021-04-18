---
description: I file di log WMI non sono più supportati.
ms.assetid: 4ba80063-7aa6-42df-a620-1b366b795034
ms.tgt_platform: multiple
title: Registrazione dell'attività WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ced8645eb7ad9005e6ba751d011ae7f0ccb3dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314598"
---
# <a name="logging-wmi-activity"></a><span data-ttu-id="e24a9-103">Registrazione dell'attività WMI</span><span class="sxs-lookup"><span data-stu-id="e24a9-103">Logging WMI Activity</span></span>

<span data-ttu-id="e24a9-104">I file di log WMI non sono più supportati.</span><span class="sxs-lookup"><span data-stu-id="e24a9-104">The WMI log files are no longer supported.</span></span> <span data-ttu-id="e24a9-105">A partire da Windows Vista, WMI utilizza [Event Tracing for Windows (ETW](/windows/desktop/ETW/event-tracing-portal)) ed eventi disponibili tramite l'interfaccia utente **Visualizzatore eventi** o lo strumento da riga di comando wevtutil.</span><span class="sxs-lookup"><span data-stu-id="e24a9-105">Starting with Windows Vista, WMI uses [Event Tracing for Windows (ETW](/windows/desktop/ETW/event-tracing-portal)) and events that are available through the **Event Viewer** UI or the Wevtutil command line tool.</span></span> <span data-ttu-id="e24a9-106">Per ulteriori informazioni, vedere il provider ETW e la documentazione della riga di comando [programma](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="e24a9-106">For more information, see the ETW provider and the [Wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) command-line documentation.</span></span>

<span data-ttu-id="e24a9-107">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="e24a9-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="e24a9-108">File di log WMI precedenti a Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e24a9-108">WMI Log Files Before Windows Vista</span></span>](#wmi-log-files-before-windows-vista)
-   [<span data-ttu-id="e24a9-109">Registrazione delle attività per i componenti di base di WMI prima di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e24a9-109">Logging Activities for WMI Core Components Before Windows Vista</span></span>](#logging-activities-for-wmi-core-components-before-windows-vista)
-   [<span data-ttu-id="e24a9-110">Registrazione di attività per i componenti del provider WMI precedenti a Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e24a9-110">Logging Activities for WMI Provider Components Before Windows Vista</span></span>](#logging-activities-for-wmi-provider-components-before-windows-vista)
-   [<span data-ttu-id="e24a9-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e24a9-111">Related topics</span></span>](#related-topics)

## <a name="wmi-log-files-before-windows-vista"></a><span data-ttu-id="e24a9-112">File di log WMI precedenti a Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e24a9-112">WMI Log Files Before Windows Vista</span></span>

<span data-ttu-id="e24a9-113">I file di log creati da WMI e da diversi provider registrano: eventi, dati di traccia o di diagnostica, errori e varie attività.</span><span class="sxs-lookup"><span data-stu-id="e24a9-113">The log files created by WMI and various providers record: events, trace or diagnostic data, errors, and various activities.</span></span> <span data-ttu-id="e24a9-114">Solo gli amministratori hanno accesso in lettura alla cartella dei log WMI presente nei log di% windir% \\ system32 \\ WBEM \\ .</span><span class="sxs-lookup"><span data-stu-id="e24a9-114">Only administrators have read access to the WMI log folder found at %windir%\\system32\\wbem\\logs.</span></span>

<span data-ttu-id="e24a9-115">Solo i componenti di base WMI o i provider WMI scrivono nei file di log.</span><span class="sxs-lookup"><span data-stu-id="e24a9-115">Only WMI core components or WMI providers write to log files.</span></span> <span data-ttu-id="e24a9-116">È possibile leggere o visualizzare solo i dati presenti nei log per scopi diagnostici.</span><span class="sxs-lookup"><span data-stu-id="e24a9-116">You can only read or view the data in these logs for diagnostic purposes.</span></span> <span data-ttu-id="e24a9-117">È possibile creare e archiviare i propri file di log nella directory dei log WMI.</span><span class="sxs-lookup"><span data-stu-id="e24a9-117">You can create and store your own log files in the WMI log directory.</span></span>

## <a name="logging-activities-for-wmi-core-components-before-windows-vista"></a><span data-ttu-id="e24a9-118">Registrazione delle attività per i componenti di base di WMI prima di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e24a9-118">Logging Activities for WMI Core Components Before Windows Vista</span></span>

<span data-ttu-id="e24a9-119">Questi file non contengono un formato coerente adatto per la lettura a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="e24a9-119">These files do not contain a consistent format that is suitable for reading programmatically.</span></span> <span data-ttu-id="e24a9-120">Per ulteriori informazioni su log specifici, vedere [file di log WMI](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="e24a9-120">For more information about specific logs, see [WMI Log Files](wmi-log-files.md).</span></span>

<span data-ttu-id="e24a9-121">Quando vengono impostate le chiavi del registro di sistema seguenti, le attività di registrazione per i componenti di base di WMI:</span><span class="sxs-lookup"><span data-stu-id="e24a9-121">Logging activities for WMI core components occurs when the following registry keys are set:</span></span>

-   <span data-ttu-id="e24a9-122">Livello di registrazione</span><span class="sxs-lookup"><span data-stu-id="e24a9-122">Logging level</span></span>

    <span data-ttu-id="e24a9-123">Le modifiche al valore del registro di sistema a livello di registrazione diventano effettive immediatamente.</span><span class="sxs-lookup"><span data-stu-id="e24a9-123">Changes to the logging level registry value take effect immediately.</span></span> <span data-ttu-id="e24a9-124">Non è necessario riavviare il servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="e24a9-124">No restart of the WMI service is necessary.</span></span>

    <span data-ttu-id="e24a9-125">**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Logging** = 2</span><span class="sxs-lookup"><span data-stu-id="e24a9-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Logging** = 2</span></span>

    <span data-ttu-id="e24a9-126">Nell'elenco seguente sono elencati i livelli di registrazione che possono essere definiti nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e24a9-126">The following list lists the logging levels that can be defined in the registry.</span></span>

    

    | <span data-ttu-id="e24a9-127">Livello di registrazione</span><span class="sxs-lookup"><span data-stu-id="e24a9-127">Logging level</span></span> | <span data-ttu-id="e24a9-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e24a9-128">Description</span></span>               |
    |---------------|---------------------------|
    | <span data-ttu-id="e24a9-129">0</span><span class="sxs-lookup"><span data-stu-id="e24a9-129">0</span></span>             | <span data-ttu-id="e24a9-130">Nessuna registrazione</span><span class="sxs-lookup"><span data-stu-id="e24a9-130">No Logging</span></span>                |
    | <span data-ttu-id="e24a9-131">1</span><span class="sxs-lookup"><span data-stu-id="e24a9-131">1</span></span>             | <span data-ttu-id="e24a9-132">Registra solo gli errori</span><span class="sxs-lookup"><span data-stu-id="e24a9-132">Log only errors</span></span>           |
    | <span data-ttu-id="e24a9-133">2</span><span class="sxs-lookup"><span data-stu-id="e24a9-133">2</span></span>             | <span data-ttu-id="e24a9-134">Registrazione dettagliata (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e24a9-134">Verbose Logging (default)</span></span> |

    

     

-   <span data-ttu-id="e24a9-135">Posizione dei file di log</span><span class="sxs-lookup"><span data-stu-id="e24a9-135">Log file location</span></span>

    <span data-ttu-id="e24a9-136">Per rendere effettive le modifiche al percorso del file di log, riavviare il servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="e24a9-136">For changes to log file location to take effect, restart the WMI service.</span></span>

    <span data-ttu-id="e24a9-137">**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Logging directory** =% windir% \\ system32 \\ WBEM \\ logs</span><span class="sxs-lookup"><span data-stu-id="e24a9-137">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Logging Directory** = %windir%\\system32\\wbem\\logs</span></span>

-   <span data-ttu-id="e24a9-138">Dimensioni massime del file di log, in byte</span><span class="sxs-lookup"><span data-stu-id="e24a9-138">Maximum log file size, in bytes</span></span>

    <span data-ttu-id="e24a9-139">**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **dimensioni massime file di log** = 65536</span><span class="sxs-lookup"><span data-stu-id="e24a9-139">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Log File Max Size** = 65536</span></span>

<span data-ttu-id="e24a9-140">È possibile modificare questi valori della chiave del registro di sistema tramite l'editor del registro di sistema o tramite lo snap-in WMI per Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="e24a9-140">You can change these registry key values through the Registry Editor or through the WMI snap-in for the Microsoft Management Console.</span></span>

<span data-ttu-id="e24a9-141">**Per impostare il livello di registrazione per WMI prima di Windows Vista**</span><span class="sxs-lookup"><span data-stu-id="e24a9-141">**To set the logging level for WMI before Windows Vista**</span></span>

1.  <span data-ttu-id="e24a9-142">Fare clic sul pulsante **Start** e quindi scegliere **Esegui**.</span><span class="sxs-lookup"><span data-stu-id="e24a9-142">Click **Start**, and then click **Run**.</span></span>
2.  <span data-ttu-id="e24a9-143">Digitare **wmimgmt. msc**</span><span class="sxs-lookup"><span data-stu-id="e24a9-143">Type **wmimgmt.msc**</span></span>
3.  <span data-ttu-id="e24a9-144">Nel menu **Azione** fare clic su **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="e24a9-144">On the **Action** menu, click **Properties**.</span></span>
4.  <span data-ttu-id="e24a9-145">Nella scheda **registrazione** impostare il livello di registrazione su **disabilitato**, **abilitato** o **dettagliato**.</span><span class="sxs-lookup"><span data-stu-id="e24a9-145">On the **Logging** tab, set the logging level to **Disabled**, **Enabled**, or **Verbose**.</span></span>
5.  <span data-ttu-id="e24a9-146">In **percorso:** Digitare il percorso della cartella del file di log e in **dimensioni massime (byte):**, impostare la dimensione massima, in byte, del file di log.</span><span class="sxs-lookup"><span data-stu-id="e24a9-146">In **Location:**, type the path to the log file folder and in **Maximum size (bytes):**, set the maximum size, in bytes, of the log file.</span></span>

<span data-ttu-id="e24a9-147">Per ulteriori informazioni sull'impostazione delle proprietà dei file di log, vedere la Guida in linea per l'applicazione di controllo WMI.</span><span class="sxs-lookup"><span data-stu-id="e24a9-147">For more information about setting the log file properties, see the online Help for the WMI Control application.</span></span>

## <a name="logging-activities-for-wmi-provider-components-before-windows-vista"></a><span data-ttu-id="e24a9-148">Registrazione di attività per i componenti del provider WMI precedenti a Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e24a9-148">Logging Activities for WMI Provider Components Before Windows Vista</span></span>

<span data-ttu-id="e24a9-149">Quando è abilitata la registrazione per i componenti di base di WMI, la registrazione viene abilitata anche per qualsiasi provider con funzionalità di registrazione.</span><span class="sxs-lookup"><span data-stu-id="e24a9-149">When logging for WMI core components is enabled, logging is also enabled for any provider with logging capabilities.</span></span>

<span data-ttu-id="e24a9-150">Nell'elenco seguente sono elencati i valori necessari.</span><span class="sxs-lookup"><span data-stu-id="e24a9-150">The following list lists the required values.</span></span>

<dl> <dt>

<span data-ttu-id="e24a9-151"><span id="File"></span><span id="file"></span><span id="FILE"></span>**File**</span><span class="sxs-lookup"><span data-stu-id="e24a9-151"><span id="File"></span><span id="file"></span><span id="FILE"></span>**File**</span></span>
</dt> <dd>

<span data-ttu-id="e24a9-152">Percorso completo e nome file del file di log.</span><span class="sxs-lookup"><span data-stu-id="e24a9-152">Full path and file name of the log file.</span></span> <span data-ttu-id="e24a9-153">Il valore predefinito è% windir% \\ system32 \\ \\ log WBEM.</span><span class="sxs-lookup"><span data-stu-id="e24a9-153">The default value is %windir%\\system32\\wbem\\logs.</span></span> <span data-ttu-id="e24a9-154">Il **tipo** denominato value deve essere impostato su = file affinché questo valore denominato venga usato.</span><span class="sxs-lookup"><span data-stu-id="e24a9-154">The **Type** named value must be set to = File for this named value to be used.</span></span>

</dd> <dt>

<span data-ttu-id="e24a9-155"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Livello**</span><span class="sxs-lookup"><span data-stu-id="e24a9-155"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Level**</span></span>
</dt> <dd>

<span data-ttu-id="e24a9-156">Maschera logica a 32 bit che definisce il tipo di output di debug generato dal provider.</span><span class="sxs-lookup"><span data-stu-id="e24a9-156">A 32-bit logical mask that defines the type of debugging output generated by the provider.</span></span> <span data-ttu-id="e24a9-157">Questo valore dipende dal provider.</span><span class="sxs-lookup"><span data-stu-id="e24a9-157">This value is provider-dependent.</span></span> <span data-ttu-id="e24a9-158">Il valore predefinito è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e24a9-158">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="e24a9-159"><span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**</span><span class="sxs-lookup"><span data-stu-id="e24a9-159"><span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**</span></span>
</dt> <dd>

<span data-ttu-id="e24a9-160">Dimensioni massime del file di log in byte.</span><span class="sxs-lookup"><span data-stu-id="e24a9-160">Maximum file size, in bytes, of the log file.</span></span> <span data-ttu-id="e24a9-161">Il valore intero deve essere compreso tra 1024 e 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="e24a9-161">This integer value must be in the range 1024 to 2^32-1.</span></span> <span data-ttu-id="e24a9-162">Quando le dimensioni del file superano questo valore, il file viene rinominato in **~ filename** e viene creato un nuovo file di log vuoto.</span><span class="sxs-lookup"><span data-stu-id="e24a9-162">When the file size exceeds this value, the file is renamed to **~filename** and a new, empty log file is created.</span></span> <span data-ttu-id="e24a9-163">Lo spazio su disco necessario per il file di log è il doppio del valore di **MaxFileSize**.</span><span class="sxs-lookup"><span data-stu-id="e24a9-163">The disk space required for the log file is twice the value of **MaxFileSize**.</span></span> <span data-ttu-id="e24a9-164">Il valore predefinito è 65.535.</span><span class="sxs-lookup"><span data-stu-id="e24a9-164">The default value is 65,535.</span></span>

</dd> <dt>

<span data-ttu-id="e24a9-165"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e24a9-165"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span>
</dt> <dd>

<span data-ttu-id="e24a9-166">Può essere impostato su = file o = debugger.</span><span class="sxs-lookup"><span data-stu-id="e24a9-166">Can be set to = File or = Debugger.</span></span> <span data-ttu-id="e24a9-167">Se impostato su = file, le informazioni di traccia vengono scritte nel file di log specificato nel **file** denominato value.</span><span class="sxs-lookup"><span data-stu-id="e24a9-167">If set to = File, the trace information is written to the log file specified in the **File** named value.</span></span> <span data-ttu-id="e24a9-168">Il valore predefinito è = file.</span><span class="sxs-lookup"><span data-stu-id="e24a9-168">The default value is = File.</span></span>

</dd> </dl>

<span data-ttu-id="e24a9-169">Ad esempio, per registrare la query e ottenere le chiamate di istanza dal provider di visualizzazione, usare i valori della chiave del registro di sistema seguenti.</span><span class="sxs-lookup"><span data-stu-id="e24a9-169">For example, to log query and get instance calls from the View Provider, use the following registry key values.</span></span> <span data-ttu-id="e24a9-170">Il log verrà inserito nella cartella log e sarà la dimensione predefinita del file.</span><span class="sxs-lookup"><span data-stu-id="e24a9-170">The log will be located in the log folder and will be the default file size.</span></span>

<span data-ttu-id="e24a9-171">**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **providers** \\ **Logging** \\ **ViewProvider** \\ **file** = C: \\ Windows \\ system32 \\ WBEM \\ logs \\ ViewProvider. log</span><span class="sxs-lookup"><span data-stu-id="e24a9-171">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**File** = C:\\Windows\\system32\\WBEM\\Logs\\ViewProvider.log</span></span>

<span data-ttu-id="e24a9-172">**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **providers** \\ **registrazione** \\  \\ **livello** ViewProvider = 2</span><span class="sxs-lookup"><span data-stu-id="e24a9-172">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**Level** = 2</span></span>

<span data-ttu-id="e24a9-173">**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **providers** \\ **Logging** \\ **ViewProvider** \\ **MaxFileSize** = 65535</span><span class="sxs-lookup"><span data-stu-id="e24a9-173">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**MaxFileSize** = 65535</span></span>

<span data-ttu-id="e24a9-174">**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **providers** \\ **Logging** \\ **ViewProvider** \\ **Type** = file</span><span class="sxs-lookup"><span data-stu-id="e24a9-174">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**Type** = File</span></span>

> [!Note]  
> <span data-ttu-id="e24a9-175">Per i provider con funzionalità di registrazione, è necessario scrivere le chiavi e i valori del registro di sistema necessari per abilitare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="e24a9-175">For your own providers with logging capabilities, you need to write the necessary registry keys and values to enable logging.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e24a9-176">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e24a9-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e24a9-177">Risoluzione dei problemi WMI</span><span class="sxs-lookup"><span data-stu-id="e24a9-177">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="e24a9-178">File di log WMI</span><span class="sxs-lookup"><span data-stu-id="e24a9-178">WMI Log Files</span></span>](wmi-log-files.md)
</dt> <dt>

[<span data-ttu-id="e24a9-179">Classi di risoluzione dei problemi WMI</span><span class="sxs-lookup"><span data-stu-id="e24a9-179">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> <dt>

[<span data-ttu-id="e24a9-180">Traccia dell'attività WMI</span><span class="sxs-lookup"><span data-stu-id="e24a9-180">Tracing WMI Activity</span></span>](tracing-wmi-activity.md)
</dt> </dl>

 

 
