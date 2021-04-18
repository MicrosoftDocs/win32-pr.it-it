---
description: Lo strumento di configurazione della traccia Microsoft Windows HTTP Services (WinHTTP), WinHttpTraceCfg.exe, viene usato per configurare le funzionalità di traccia per il debug e l'analisi dei pacchetti.
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe, uno strumento di configurazione della traccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c6423c581a51f0cf6b55856f2e8cd0ea670515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307088"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a><span data-ttu-id="cc043-103">WinHttpTraceCfg.exe, uno strumento di configurazione della traccia</span><span class="sxs-lookup"><span data-stu-id="cc043-103">WinHttpTraceCfg.exe, a Trace Configuration Tool</span></span>

<span data-ttu-id="cc043-104">Lo strumento di configurazione della traccia [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) , WinHttpTraceCfg.exe, viene usato per configurare le funzionalità di traccia per il debug e l'analisi dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="cc043-104">The [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) trace configuration tool, WinHttpTraceCfg.exe, is used to configure trace capabilities for debugging and packet-sniffing purposes.</span></span> <span data-ttu-id="cc043-105">La possibilità di monitorare le funzioni WinHTTP e il traffico di rete corrispondente è importante.</span><span class="sxs-lookup"><span data-stu-id="cc043-105">The ability to monitor WinHTTP functions and their corresponding network traffic is important.</span></span> <span data-ttu-id="cc043-106">Il debug di applicazioni che utilizzano protocolli di Wire crittografati, ad esempio Secure Sockets Layer (SSL), impedisce l'analisi dei pacchetti a livello di trasporto di rete e richiede la possibilità di intercettare il traffico tra il client e il server dopo che è stato decrittografato.</span><span class="sxs-lookup"><span data-stu-id="cc043-106">Debugging applications that utilize encrypted wire protocols, such as Secure Sockets Layer (SSL), preclude sniffing packets at the network transport layer and require the ability to intercept traffic between the client and server after it has been decrypted.</span></span> <span data-ttu-id="cc043-107">I servizi HTTP di Microsoft Windows (WinHTTP) forniscono una funzionalità di traccia con una vasta gamma di funzionalità per intercettare il flusso di traffico tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="cc043-107">Microsoft Windows HTTP Services (WinHTTP) provides a trace facility that has a range of capabilities for intercepting the traffic stream between the client and server.</span></span>

<span data-ttu-id="cc043-108">Questa funzionalità di traccia può essere uno strumento utile per eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="cc043-108">This trace facility can be a valuable tool for debugging.</span></span> <span data-ttu-id="cc043-109">Può essere usato, ad esempio, per visualizzare i parametri passati a diverse chiamate di funzione, nonché per visualizzare i dati effettivi inviati e ricevuti da un'applicazione WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="cc043-109">It can be used, for example, to view parameters passed to various function calls, as well as to view actual data sent and received by a WinHTTP application.</span></span>

-   [<span data-ttu-id="cc043-110">Utilizzo della funzionalità di traccia</span><span class="sxs-lookup"><span data-stu-id="cc043-110">Using the Trace Facility</span></span>](#using-the-trace-facility)
-   [<span data-ttu-id="cc043-111">Interpretazione dei dati di traccia</span><span class="sxs-lookup"><span data-stu-id="cc043-111">Interpreting Trace Data</span></span>](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a><span data-ttu-id="cc043-112">Utilizzo della funzionalità di traccia</span><span class="sxs-lookup"><span data-stu-id="cc043-112">Using the Trace Facility</span></span>

<span data-ttu-id="cc043-113">WinHTTP ottiene i parametri di controllo della traccia dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="cc043-113">WinHTTP obtains tracing control parameters from the registry.</span></span> <span data-ttu-id="cc043-114">Questi parametri di controllo influiscono sul modo in cui WinHTTP produce l'output di traccia e la formattazione dell'output.</span><span class="sxs-lookup"><span data-stu-id="cc043-114">These control parameters affect how WinHTTP produces trace output, and how that output is formatted.</span></span> <span data-ttu-id="cc043-115">Tutte le applicazioni che utilizzano WinHTTP condividono le stesse impostazioni.</span><span class="sxs-lookup"><span data-stu-id="cc043-115">All applications that use WinHTTP share the same settings.</span></span>

<span data-ttu-id="cc043-116">Uno strumento di configurazione della funzionalità di traccia, WinHttpTraceCfg.exe, è disponibile come download nel sito Web [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) .</span><span class="sxs-lookup"><span data-stu-id="cc043-116">A trace facility configuration tool, WinHttpTraceCfg.exe, is available as a download on the [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) website.</span></span> <span data-ttu-id="cc043-117">Lo strumento di configurazione consente di impostare o recuperare le impostazioni del registro di sistema della funzionalità di traccia basate sui parametri della riga di comando specificati.</span><span class="sxs-lookup"><span data-stu-id="cc043-117">The configuration tool sets or retrieves the trace facility registry settings based on the specified command line parameters.</span></span>

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

<span data-ttu-id="cc043-118">Nella tabella seguente sono elencati i parametri possibili per lo strumento di configurazione di.</span><span class="sxs-lookup"><span data-stu-id="cc043-118">The following table lists possible parameters for the configuration tool.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cc043-119">Parametro</span><span class="sxs-lookup"><span data-stu-id="cc043-119">Parameter</span></span></th>
<th><span data-ttu-id="cc043-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc043-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc043-121">-?</span><span class="sxs-lookup"><span data-stu-id="cc043-121">-?</span></span></td>
<td><span data-ttu-id="cc043-122">Visualizza i dati di sintassi.</span><span class="sxs-lookup"><span data-stu-id="cc043-122">Displays syntax data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc043-123">-E</span><span class="sxs-lookup"><span data-stu-id="cc043-123">-e</span></span></td>
<td><span data-ttu-id="cc043-124">Specifica se la funzionalità di traccia è abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="cc043-124">Specifies whether the trace facility is enabled or disabled.</span></span> <br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc043-125">0</span><span class="sxs-lookup"><span data-stu-id="cc043-125">0</span></span></td>
<td><span data-ttu-id="cc043-126">Impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cc043-126">Default setting.</span></span> <span data-ttu-id="cc043-127">Disabilita la traccia.</span><span class="sxs-lookup"><span data-stu-id="cc043-127">Disables tracing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc043-128">1</span><span class="sxs-lookup"><span data-stu-id="cc043-128">1</span></span></td>
<td><span data-ttu-id="cc043-129">Abilita la traccia.</span><span class="sxs-lookup"><span data-stu-id="cc043-129">Enables tracing.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc043-130">-l</span><span class="sxs-lookup"><span data-stu-id="cc043-130">-l</span></span></td>
<td><p><span data-ttu-id="cc043-131">Specifica un prefisso per il file di log.</span><span class="sxs-lookup"><span data-stu-id="cc043-131">Specifies a prefix for the log file.</span></span> <span data-ttu-id="cc043-132">Il prefisso può includere un percorso.</span><span class="sxs-lookup"><span data-stu-id="cc043-132">The prefix can include a path.</span></span> <span data-ttu-id="cc043-133">Il file di log viene scritto nella directory corrente o nella directory specificata nel prefisso e ha il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="cc043-133">The log file is written to the current directory or the directory specified in the prefix and has the following format.</span></span></p>
<p><span data-ttu-id="cc043-134"><<em></em> > prefisso -< <em>nome dell'applicazione</em> > . <<em>Time</em> > . log</span><span class="sxs-lookup"><span data-stu-id="cc043-134"><<em>prefix</em>>-<<em>application name</em>>.<<em>time</em>>.log</span></span></p>
<p><span data-ttu-id="cc043-135">Se non si specifica un prefisso, viene utilizzata una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="cc043-135">If a prefix is not specified, an empty string is used.</span></span> <span data-ttu-id="cc043-136">Specificare &quot; \* &quot; per eliminare un prefisso esistente.</span><span class="sxs-lookup"><span data-stu-id="cc043-136">Specify &quot;\*&quot; to delete an existing prefix.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc043-137">-d</span><span class="sxs-lookup"><span data-stu-id="cc043-137">-d</span></span></td>
<td><p><span data-ttu-id="cc043-138">Specifica se l'output di traccia viene visualizzato in un debugger o viene scritto in un file.</span><span class="sxs-lookup"><span data-stu-id="cc043-138">Specifies whether the trace output is displayed in a debugger or written to a file.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc043-139">0</span><span class="sxs-lookup"><span data-stu-id="cc043-139">0</span></span></td>
<td><span data-ttu-id="cc043-140">Impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cc043-140">Default setting.</span></span> <span data-ttu-id="cc043-141">Scrive nel file di log.</span><span class="sxs-lookup"><span data-stu-id="cc043-141">Writes to log file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc043-142">1</span><span class="sxs-lookup"><span data-stu-id="cc043-142">1</span></span></td>
<td><span data-ttu-id="cc043-143">Viene visualizzato in un debugger.</span><span class="sxs-lookup"><span data-stu-id="cc043-143">Displays in a debugger.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc043-144">-S</span><span class="sxs-lookup"><span data-stu-id="cc043-144">-s</span></span></td>
<td><p><span data-ttu-id="cc043-145">Specifica il modo in cui viene visualizzato il traffico di rete (richieste e risposte).</span><span class="sxs-lookup"><span data-stu-id="cc043-145">Specifies how network traffic (requests and responses) is displayed.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc043-146">0</span><span class="sxs-lookup"><span data-stu-id="cc043-146">0</span></span></td>
<td><span data-ttu-id="cc043-147">Visualizza solo le intestazioni HTTP.</span><span class="sxs-lookup"><span data-stu-id="cc043-147">Only displays HTTP headers.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc043-148">1</span><span class="sxs-lookup"><span data-stu-id="cc043-148">1</span></span></td>
<td><span data-ttu-id="cc043-149">Impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cc043-149">Default setting.</span></span> <span data-ttu-id="cc043-150">Mostra il traffico di rete in formato American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="cc043-150">Shows network traffic in American National Standards Institute (ANSI) format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc043-151">2</span><span class="sxs-lookup"><span data-stu-id="cc043-151">2</span></span></td>
<td><span data-ttu-id="cc043-152">Mostra il traffico di rete in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="cc043-152">Shows network traffic in hexadecimal format.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc043-153">-T</span><span class="sxs-lookup"><span data-stu-id="cc043-153">-t</span></span></td>
<td><p><span data-ttu-id="cc043-154">Specifica se le chiamate di funzione di primo livello vengono registrate nella traccia.</span><span class="sxs-lookup"><span data-stu-id="cc043-154">Specifies whether top-level function calls are recorded in the trace.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc043-155">0</span><span class="sxs-lookup"><span data-stu-id="cc043-155">0</span></span></td>
<td><span data-ttu-id="cc043-156">Impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cc043-156">Default setting.</span></span> <span data-ttu-id="cc043-157">Le chiamate di funzione non vengono registrate.</span><span class="sxs-lookup"><span data-stu-id="cc043-157">Function calls are not recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc043-158">1</span><span class="sxs-lookup"><span data-stu-id="cc043-158">1</span></span></td>
<td><span data-ttu-id="cc043-159">Vengono registrate le chiamate di funzione di primo livello.</span><span class="sxs-lookup"><span data-stu-id="cc043-159">Top-level function calls are recorded.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc043-160">-M</span><span class="sxs-lookup"><span data-stu-id="cc043-160">-m</span></span></td>
<td><p><span data-ttu-id="cc043-161">Specifica la dimensione massima, in byte, di un file di log generato dalla funzionalità di traccia.</span><span class="sxs-lookup"><span data-stu-id="cc043-161">Specifies the maximum size, in bytes, of a log file generated by the tracing facility.</span></span> <span data-ttu-id="cc043-162">Se questa opzione viene specificata senza una dimensione, il valore minimo è 65.535 byte.</span><span class="sxs-lookup"><span data-stu-id="cc043-162">If this option is specified without a size, the minimum value is 65,535 bytes.</span></span> <span data-ttu-id="cc043-163">Se un file di log raggiunge la dimensione massima, il contenuto del file verrà cancellato.</span><span class="sxs-lookup"><span data-stu-id="cc043-163">If a log file reaches the maximum size, the contents of the file are erased.</span></span> <span data-ttu-id="cc043-164">I dati di traccia continuano a essere scritti nel file di log.</span><span class="sxs-lookup"><span data-stu-id="cc043-164">Trace data continues to be written to the log file.</span></span></p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cc043-165">L'esecuzione dello strumento di configurazione della funzionalità Trace e la specifica di nessun parametro consente di recuperare e visualizzare le impostazioni correnti del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="cc043-165">Running the trace facility configuration tool and specifying no parameters retrieves and displays the current registry settings.</span></span>

> [!Note]  
> <span data-ttu-id="cc043-166">I file di log aumentano rapidamente e peggiorano le prestazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cc043-166">Log files grow rapidly and degrade application performance.</span></span> <span data-ttu-id="cc043-167">Prima di abilitare la funzionalità di traccia, verificare che lo spazio su disco rigido richiesto sia disponibile.</span><span class="sxs-lookup"><span data-stu-id="cc043-167">Ensure that the required hard disk drive space is available before enabling the trace facility.</span></span>

 

## <a name="interpreting-trace-data"></a><span data-ttu-id="cc043-168">Interpretazione dei dati di traccia</span><span class="sxs-lookup"><span data-stu-id="cc043-168">Interpreting Trace Data</span></span>

<span data-ttu-id="cc043-169">Il flusso di dati della funzionalità di traccia riflette le funzioni WinHTTP chiamate nell'applicazione e qualsiasi dato HTTP inviato o ricevuto.</span><span class="sxs-lookup"><span data-stu-id="cc043-169">The trace facility data stream reflects WinHTTP functions called in the application and any HTTP data sent or received.</span></span> <span data-ttu-id="cc043-170">In alcuni casi, vengono visualizzate anche le funzioni chiamate internamente da WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="cc043-170">In some cases, functions called internally by WinHTTP are also shown.</span></span>

<span data-ttu-id="cc043-171">Nell'immagine seguente viene illustrata una parte di un file di log generato dalla funzionalità Trace.</span><span class="sxs-lookup"><span data-stu-id="cc043-171">The following image shows a portion of a log file generated by the trace facility.</span></span> <span data-ttu-id="cc043-172">Diversi elementi vengono evidenziati e contrassegnati con l'etichetta.</span><span class="sxs-lookup"><span data-stu-id="cc043-172">Several items are highlighted and labeled.</span></span>

![traccia di esempio](images/ss-tracer-wco.png)

<span data-ttu-id="cc043-174">Ogni riga dell'output di traccia contiene informazioni in tre colonne.</span><span class="sxs-lookup"><span data-stu-id="cc043-174">Each line of trace output contains information in three columns.</span></span> <span data-ttu-id="cc043-175">La prima colonna indica la data e l'ora in cui è stata registrata la voce.</span><span class="sxs-lookup"><span data-stu-id="cc043-175">The first column shows the date and time when the entry was recorded.</span></span> <span data-ttu-id="cc043-176">La seconda colonna Mostra un identificatore (ID) di richiesta che può essere usato per distinguere più richieste.</span><span class="sxs-lookup"><span data-stu-id="cc043-176">The second column shows a request identifier (ID) that can be used to differentiate between multiple requests.</span></span> <span data-ttu-id="cc043-177">Se la voce di log non corrisponde a una richiesta specifica, \* \* in questa colonna viene visualizzato "Session".</span><span class="sxs-lookup"><span data-stu-id="cc043-177">If the log entry does not correspond to a specific request, "\*Session\*" is displayed in this column.</span></span> <span data-ttu-id="cc043-178">Può essere utile ordinare il file di log in base a questo ID per visualizzare solo gli eventi che si verificano per una singola richiesta.</span><span class="sxs-lookup"><span data-stu-id="cc043-178">It can be useful to sort the log file based on this ID to see only events that occur for a single request.</span></span> <span data-ttu-id="cc043-179">Nell'esempio seguente viene illustrato un comando che è possibile utilizzare per ordinare il file di log.</span><span class="sxs-lookup"><span data-stu-id="cc043-179">The following example shows a command you can use to sort the log file.</span></span>

<span data-ttu-id="cc043-180">**findstr 00000001 LogFile. log**</span><span class="sxs-lookup"><span data-stu-id="cc043-180">**findstr 00000001 LogFile.log**</span></span>

<span data-ttu-id="cc043-181">La terza colonna Mostra una chiamata di funzione, il traffico HTTP o un messaggio di stato incluso per facilitare l'interpretazione della traccia.</span><span class="sxs-lookup"><span data-stu-id="cc043-181">The third column shows a function call, HTTP traffic, or a status message included to help interpret the trace.</span></span>

<span data-ttu-id="cc043-182">Quando una voce di log corrisponde a una chiamata di funzione, vengono registrati anche i parametri della funzione.</span><span class="sxs-lookup"><span data-stu-id="cc043-182">When a log entry corresponds to a function call, the parameters of the function are also recorded.</span></span> <span data-ttu-id="cc043-183">Gli indirizzi di memoria vengono visualizzati in formato esadecimale, mentre tutti gli altri valori vengono visualizzati come stringa ASCII.</span><span class="sxs-lookup"><span data-stu-id="cc043-183">Memory addresses are displayed in hexadecimal while all other values are displayed as an ASCII string.</span></span> <span data-ttu-id="cc043-184">La funzionalità di traccia registra anche il valore e l'ora di ritorno per ogni funzione.</span><span class="sxs-lookup"><span data-stu-id="cc043-184">The trace facility also records the return time and value for each function.</span></span>

<span data-ttu-id="cc043-185">Il formato dei dati HTTP dipende dalle impostazioni del registro di sistema specificate con lo strumento di configurazione della funzionalità Trace.</span><span class="sxs-lookup"><span data-stu-id="cc043-185">The format of HTTP data depends on the registry settings specified with the trace facility configuration tool.</span></span> <span data-ttu-id="cc043-186">Quando i dati HTTP vengono crittografati, anche i dati decrittografati vengono visualizzati nell'output di traccia.</span><span class="sxs-lookup"><span data-stu-id="cc043-186">When HTTP data is encrypted, the decrypted data is also shown in the trace output.</span></span>

 

 




