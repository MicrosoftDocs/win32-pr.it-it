---
description: Funzioni di output di debug
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Funzioni di output di debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87470b44717bb76c1a029bd885bb9149a4636b5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304318"
---
# <a name="debug-output-functions"></a><span data-ttu-id="3671c-103">Funzioni di output di debug</span><span class="sxs-lookup"><span data-stu-id="3671c-103">Debug Output Functions</span></span>

<span data-ttu-id="3671c-104">Le [classi base di DirectShow](directshow-base-classes.md) forniscono diverse macro per la visualizzazione delle informazioni di debug.</span><span class="sxs-lookup"><span data-stu-id="3671c-104">The [DirectShow Base Classes](directshow-base-classes.md) provide several macros for displaying debugging information.</span></span>



| <span data-ttu-id="3671c-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="3671c-105">Function</span></span>                                               | <span data-ttu-id="3671c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3671c-106">Description</span></span>                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3671c-107">**DbgCheckModuleLevel**</span><span class="sxs-lookup"><span data-stu-id="3671c-107">**DbgCheckModuleLevel**</span></span>](dbgcheckmodulelevel.md)     | <span data-ttu-id="3671c-108">Controlla se la registrazione è abilitata per i tipi di messaggio e il livello specificati.</span><span class="sxs-lookup"><span data-stu-id="3671c-108">Checks whether logging is enabled for the given message types and level.</span></span>                             |
| [<span data-ttu-id="3671c-109">**DbgDumpObjectRegister**</span><span class="sxs-lookup"><span data-stu-id="3671c-109">**DbgDumpObjectRegister**</span></span>](dbgdumpobjectregister.md) | <span data-ttu-id="3671c-110">Visualizza informazioni sugli oggetti attivi.</span><span class="sxs-lookup"><span data-stu-id="3671c-110">Displays information about active objects.</span></span>                                                           |
| [<span data-ttu-id="3671c-111">**DbgInitialise**</span><span class="sxs-lookup"><span data-stu-id="3671c-111">**DbgInitialise**</span></span>](dbginitialise.md)                 | <span data-ttu-id="3671c-112">Inizializza la libreria di debug.</span><span class="sxs-lookup"><span data-stu-id="3671c-112">Initializes the debug library.</span></span>                                                                       |
| [<span data-ttu-id="3671c-113">**DbgLog**</span><span class="sxs-lookup"><span data-stu-id="3671c-113">**DbgLog**</span></span>](dbglog.md)                               | <span data-ttu-id="3671c-114">Invia una stringa al percorso di output di debug, se la registrazione è abilitata per il tipo e il livello specificati.</span><span class="sxs-lookup"><span data-stu-id="3671c-114">Sends a string to the debug output location, if logging is enabled for the specified type and level.</span></span> |
| [<span data-ttu-id="3671c-115">**DbgOutString**</span><span class="sxs-lookup"><span data-stu-id="3671c-115">**DbgOutString**</span></span>](dbgoutstring.md)                   | <span data-ttu-id="3671c-116">Invia una stringa al percorso di output di debug.</span><span class="sxs-lookup"><span data-stu-id="3671c-116">Sends a string to the debug output location.</span></span>                                                         |
| [<span data-ttu-id="3671c-117">**DbgSetModuleLevel**</span><span class="sxs-lookup"><span data-stu-id="3671c-117">**DbgSetModuleLevel**</span></span>](dbgsetmodulelevel.md)         | <span data-ttu-id="3671c-118">Imposta il livello di registrazione per uno o più tipi di messaggio.</span><span class="sxs-lookup"><span data-stu-id="3671c-118">Sets the logging level for one or more message types.</span></span>                                                |
| [<span data-ttu-id="3671c-119">**DbgTerminate**</span><span class="sxs-lookup"><span data-stu-id="3671c-119">**DbgTerminate**</span></span>](dbgterminate.md)                   | <span data-ttu-id="3671c-120">Pulisce la libreria di debug.</span><span class="sxs-lookup"><span data-stu-id="3671c-120">Cleans up the debug library.</span></span>                                                                         |
| [<span data-ttu-id="3671c-121">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="3671c-121">**DisplayType**</span></span>](displaytype.md)                     | <span data-ttu-id="3671c-122">Invia informazioni su un tipo di supporto al percorso di output di debug.</span><span class="sxs-lookup"><span data-stu-id="3671c-122">Sends information about a media type to the debug output location.</span></span>                                   |
| [<span data-ttu-id="3671c-123">**DumpGraph**</span><span class="sxs-lookup"><span data-stu-id="3671c-123">**DumpGraph**</span></span>](dumpgraph.md)                         | <span data-ttu-id="3671c-124">Invia informazioni su un grafico di filtro al percorso di output di debug.</span><span class="sxs-lookup"><span data-stu-id="3671c-124">Sends information about a filter graph to the debug output location.</span></span>                                 |
| [<span data-ttu-id="3671c-125">**GuidNames**</span><span class="sxs-lookup"><span data-stu-id="3671c-125">**GuidNames**</span></span>](guidnames.md)                         | <span data-ttu-id="3671c-126">Matrice globale che contiene le stringhe che rappresentano i GUID definiti in UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="3671c-126">Global array that contains strings representing the GUIDs defined in Uuids.h.</span></span>                        |
| [<span data-ttu-id="3671c-127">**NOME**</span><span class="sxs-lookup"><span data-stu-id="3671c-127">**NAME**</span></span>](name.md)                                   | <span data-ttu-id="3671c-128">Genera una stringa di solo debug.</span><span class="sxs-lookup"><span data-stu-id="3671c-128">Generates a debug-only string.</span></span>                                                                       |
| [<span data-ttu-id="3671c-129">**Si noti**</span><span class="sxs-lookup"><span data-stu-id="3671c-129">**NOTE**</span></span>](note.md)                                   | <span data-ttu-id="3671c-130">Invia una stringa al percorso di output di debug.</span><span class="sxs-lookup"><span data-stu-id="3671c-130">Sends a string to the debug output location.</span></span>                                                         |
| [<span data-ttu-id="3671c-131">**RICORDARE**</span><span class="sxs-lookup"><span data-stu-id="3671c-131">**REMIND**</span></span>](remind.md)                               | <span data-ttu-id="3671c-132">Genera un promemoria in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="3671c-132">Generates a reminder at compile time.</span></span>                                                                |



 

<span data-ttu-id="3671c-133">**Chiavi del registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="3671c-133">**Registry Keys**</span></span>

<span data-ttu-id="3671c-134">La funzione di output di debug in DirectShow usa un set di chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="3671c-134">The debug output function in DirectShow use a set of registry keys.</span></span> <span data-ttu-id="3671c-135">Il percorso di queste chiavi del registro di sistema dipende dalla versione di Windows.</span><span class="sxs-lookup"><span data-stu-id="3671c-135">The location of these registry keys depends on the version of Windows.</span></span>

<span data-ttu-id="3671c-136">*Prima di Windows Vista*, le chiavi di debug si trovano nel percorso seguente:</span><span class="sxs-lookup"><span data-stu-id="3671c-136">*Prior to Windows Vista*, the debugging keys are located under the following path:</span></span>

<span data-ttu-id="3671c-137">**HKEY \_ Debug \_ del software del computer locale** \\  \\ </span><span class="sxs-lookup"><span data-stu-id="3671c-137">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Debug**</span></span>

<span data-ttu-id="3671c-138">In Windows Vista o versioni successive si trovano nel percorso seguente:</span><span class="sxs-lookup"><span data-stu-id="3671c-138">In Windows Vista or later, they are located under the following path:</span></span>

<span data-ttu-id="3671c-139">**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **DirectShow** \\ **debug**</span><span class="sxs-lookup"><span data-stu-id="3671c-139">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**DirectShow**\\**Debug**</span></span>

<span data-ttu-id="3671c-140">Per i filtri di terze parti, la posizione dipende dalla versione delle [classi di base di DirectShow](directshow-base-classes.md) utilizzata per compilare il filtro.</span><span class="sxs-lookup"><span data-stu-id="3671c-140">For third-party filters, the location depends on which version of the [DirectShow Base Classes](directshow-base-classes.md) was used to build the filter.</span></span> <span data-ttu-id="3671c-141">La versione inclusa nel Windows SDK per Windows Vista usa il percorso più recente.</span><span class="sxs-lookup"><span data-stu-id="3671c-141">The version included in the Windows SDK for Windows Vista uses the newer path.</span></span> <span data-ttu-id="3671c-142">Le versioni precedenti usavano il percorso precedente.</span><span class="sxs-lookup"><span data-stu-id="3671c-142">Previous versions used the older path.</span></span>

<span data-ttu-id="3671c-143">Nelle osservazioni che seguono, l'etichetta *<DebugRoot>* viene usata per indicare questi due percorsi.</span><span class="sxs-lookup"><span data-stu-id="3671c-143">In the remarks that follow, the label *<DebugRoot>* is used to indicate these two paths.</span></span> <span data-ttu-id="3671c-144">Sostituire il percorso corretto, a seconda della versione di Windows o della versione delle classi di base.</span><span class="sxs-lookup"><span data-stu-id="3671c-144">Substitute the correct path, depending on the version of Windows or the version of the base classes.</span></span>

<span data-ttu-id="3671c-145">**Registrazione debug**</span><span class="sxs-lookup"><span data-stu-id="3671c-145">**Debug Logging**</span></span>

<span data-ttu-id="3671c-146">DirectShow definisce diversi tipi di messaggi, illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3671c-146">DirectShow defines several message types, shown in the following table.</span></span>



| <span data-ttu-id="3671c-147">Valore</span><span class="sxs-lookup"><span data-stu-id="3671c-147">Value</span></span>                   | <span data-ttu-id="3671c-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3671c-148">Description</span></span>                                             |
|-------------------------|---------------------------------------------------------|
| <span data-ttu-id="3671c-149">errore di registrazione \_</span><span class="sxs-lookup"><span data-stu-id="3671c-149">LOG\_ERROR</span></span>              | <span data-ttu-id="3671c-150">Notifica di errore.</span><span class="sxs-lookup"><span data-stu-id="3671c-150">Error notification.</span></span>                                     |
| <span data-ttu-id="3671c-151">blocco del LOG \_</span><span class="sxs-lookup"><span data-stu-id="3671c-151">LOG\_LOCKING</span></span>            | <span data-ttu-id="3671c-152">Blocco e sblocco di sezioni critiche.</span><span class="sxs-lookup"><span data-stu-id="3671c-152">Locking and unlocking of critical sections.</span></span>             |
| <span data-ttu-id="3671c-153">\_memoria log</span><span class="sxs-lookup"><span data-stu-id="3671c-153">LOG\_MEMORY</span></span>             | <span data-ttu-id="3671c-154">Allocazione di memoria e creazione e distruzione di oggetti.</span><span class="sxs-lookup"><span data-stu-id="3671c-154">Memory allocation, and object creation and destruction.</span></span> |
| <span data-ttu-id="3671c-155">\_temporizzazione log</span><span class="sxs-lookup"><span data-stu-id="3671c-155">LOG\_TIMING</span></span>             | <span data-ttu-id="3671c-156">Misurazione delle prestazioni e delle tempistiche.</span><span class="sxs-lookup"><span data-stu-id="3671c-156">Timing and performance measurements.</span></span>                    |
| <span data-ttu-id="3671c-157">traccia del LOG \_</span><span class="sxs-lookup"><span data-stu-id="3671c-157">LOG\_TRACE</span></span>              | <span data-ttu-id="3671c-158">Traccia generale delle chiamate.</span><span class="sxs-lookup"><span data-stu-id="3671c-158">General call tracing.</span></span>                                   |
| <span data-ttu-id="3671c-159">Da PERSONALIZZATA1 a CUSTOM5</span><span class="sxs-lookup"><span data-stu-id="3671c-159">CUSTOM1 through CUSTOM5</span></span> | <span data-ttu-id="3671c-160">Disponibile per i messaggi di debug personalizzati</span><span class="sxs-lookup"><span data-stu-id="3671c-160">Available for custom debug messages</span></span>                     |



 

<span data-ttu-id="3671c-161">Ogni funzione di registrazione del debug DirectShow specifica un tipo di messaggio e un livello di registrazione.</span><span class="sxs-lookup"><span data-stu-id="3671c-161">Each of the DirectShow debug logging functions specifies a message type and a log level.</span></span> <span data-ttu-id="3671c-162">Il messaggio di debug viene visualizzato solo quando il livello di debug corrente per quel tipo di messaggio è uguale o maggiore del livello specificato nella funzione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="3671c-162">The debug message is displayed only when the current debugging level for that message type is equal to or greater than the level specified in the logging function.</span></span> <span data-ttu-id="3671c-163">In caso contrario, il messaggio viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="3671c-163">Otherwise, the message is ignored.</span></span>

<span data-ttu-id="3671c-164">Il codice seguente, ad esempio, restituisce la stringa "questo è un messaggio di debug" Se il livello di traccia del LOG \_ è 3 o superiore:</span><span class="sxs-lookup"><span data-stu-id="3671c-164">For example, the following code outputs the string "This is a debug message" if the LOG\_TRACE level is 3 or higher:</span></span>

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

<span data-ttu-id="3671c-165">Ogni modulo può impostare il proprio livello di debug per ogni tipo di messaggio.</span><span class="sxs-lookup"><span data-stu-id="3671c-165">Every module can set its own debugging level for each message type.</span></span> <span data-ttu-id="3671c-166">Un *modulo* è un file eseguibile o dll che è possibile caricare utilizzando la funzione **LoadLibrary** . I livelli di debug di un modulo vengono visualizzati nel registro di sistema nella chiave seguente:</span><span class="sxs-lookup"><span data-stu-id="3671c-166">(A *module* is a DLL or executable that can be loaded using the **LoadLibrary** function.) A module's debugging levels appear in the registry under the following key:</span></span>

<span data-ttu-id="3671c-167">**\_computer locale \_ HKEY**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**</span><span class="sxs-lookup"><span data-stu-id="3671c-167">**HKEY\_LOCAL\_MACHINE**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**</span></span>

<span data-ttu-id="3671c-168">dove *<Message Type>* è il tipo di messaggio meno il "log \_ " iniziale, ad esempio il **blocco** per \_ i messaggi di blocco del log.</span><span class="sxs-lookup"><span data-stu-id="3671c-168">where *<Message Type>* is the message type minus the initial "LOG\_"; for example, **LOCKING** for LOG\_LOCKING messages.</span></span> <span data-ttu-id="3671c-169">Quando viene caricato un modulo, la libreria di debug trova i livelli di registrazione del modulo nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="3671c-169">When a module is loaded, the debug library finds the module's logging levels in the registry.</span></span> <span data-ttu-id="3671c-170">Se le chiavi del registro di sistema non esistono, vengono create dalla libreria di debug.</span><span class="sxs-lookup"><span data-stu-id="3671c-170">If the registry keys do not exist, the debug library creates them.</span></span>

<span data-ttu-id="3671c-171">Un modulo può inoltre impostare i propri livelli in fase di esecuzione tramite la funzione [**DbgSetModuleLevel**](dbgsetmodulelevel.md) .</span><span class="sxs-lookup"><span data-stu-id="3671c-171">A module can also set its own levels at run time, using the [**DbgSetModuleLevel**](dbgsetmodulelevel.md) function.</span></span> <span data-ttu-id="3671c-172">Per inviare un messaggio all'output di debug, chiamare la macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="3671c-172">To send a message to the debug output, call the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="3671c-173">Nell'esempio seguente viene creato un messaggio di livello 3 di tipo \_ traccia log:</span><span class="sxs-lookup"><span data-stu-id="3671c-173">The following example creates a level 3 message of type LOG\_TRACE:</span></span>

<span data-ttu-id="3671c-174">È anche possibile specificare i livelli di registrazione globali, con la chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="3671c-174">You can also specify global logging levels, with the following registry key:</span></span>


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



<span data-ttu-id="3671c-175">La libreria di debug usa qualsiasi livello maggiore, il livello globale o il livello del modulo.</span><span class="sxs-lookup"><span data-stu-id="3671c-175">The debug library uses whichever level is greater, the global level or the module level.</span></span>

<span data-ttu-id="3671c-176">**Percorso di output di debug**</span><span class="sxs-lookup"><span data-stu-id="3671c-176">**Debug Output Location**</span></span>

<span data-ttu-id="3671c-177">Il percorso di output di debug è determinato da un'altra chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="3671c-177">The debug output location is determined by another registry key:</span></span>

<span data-ttu-id="3671c-178">**HKEY \_ LogToFile \_ computer locale** \\ **<DebugRoot>** \\ **<Modile Name>** \\ </span><span class="sxs-lookup"><span data-stu-id="3671c-178">**HKEY\_LOCAL\_MACHINE**\\**<DebugRoot>**\\**<Modile Name>**\\**LogToFile**</span></span>

<span data-ttu-id="3671c-179">Se il valore di questa chiave è `Console` , l'output passa alla finestra della console.</span><span class="sxs-lookup"><span data-stu-id="3671c-179">If the value of this key is `Console`, the output goes to the console window.</span></span> <span data-ttu-id="3671c-180">Se il valore è `Deb` , `Debug` , `Debugger` o una stringa vuota, l'output passa alla finestra del debugger.</span><span class="sxs-lookup"><span data-stu-id="3671c-180">If the value is `Deb`, `Debug`, `Debugger`, or an empty string, the output goes to the debugger window.</span></span> <span data-ttu-id="3671c-181">In caso contrario, l'output viene scritto in un file specificato dalla chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="3671c-181">Otherwise, the output is written to a file specified by the registry key.</span></span>

<span data-ttu-id="3671c-182">Prima che un eseguibile usi la libreria di debug DirectShow, deve chiamare la funzione [**DbgInitialise**](dbginitialise.md) .</span><span class="sxs-lookup"><span data-stu-id="3671c-182">Before an executable uses the DirectShow debug library, it must call the [**DbgInitialise**](dbginitialise.md) function.</span></span> <span data-ttu-id="3671c-183">Successivamente, deve chiamare la funzione [**DbgTerminate**](dbgterminate.md) .</span><span class="sxs-lookup"><span data-stu-id="3671c-183">Afterward, it must call the [**DbgTerminate**](dbgterminate.md) function.</span></span> <span data-ttu-id="3671c-184">Le dll non devono chiamare queste funzioni, perché il punto di ingresso della DLL (definito nella libreria di classi base) li chiama automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3671c-184">DLLs do not need to call these functions, because the DLL entry point (defined in the base class library) calls them automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3671c-185">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3671c-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3671c-186">Utilità di debug</span><span class="sxs-lookup"><span data-stu-id="3671c-186">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



