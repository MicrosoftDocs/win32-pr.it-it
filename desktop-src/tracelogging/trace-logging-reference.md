---
title: Riferimento a TraceLogging
description: Negli argomenti seguenti vengono fornite informazioni sull'API TraceLogging nativa. TraceLogging si basa su Event Tracing for Windows (ETW) e fornisce un modo semplificato per instrumentare il codice.
ms.assetid: 9E3F2140-DDB0-4C30-B7D0-A81F11823AA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d81874e7aeb1a0618716b00d225d215c382ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399647"
---
# <a name="tracelogging-reference"></a><span data-ttu-id="b87d1-103">Riferimento a TraceLogging</span><span class="sxs-lookup"><span data-stu-id="b87d1-103">TraceLogging Reference</span></span>

<span data-ttu-id="b87d1-104">Negli argomenti seguenti vengono fornite informazioni sull'API TraceLogging nativa.</span><span class="sxs-lookup"><span data-stu-id="b87d1-104">The following topics provide information about the native TraceLogging API.</span></span>

<span data-ttu-id="b87d1-105">TraceLogging si basa su Event Tracing for Windows (ETW) e fornisce un modo semplificato per instrumentare il codice.</span><span class="sxs-lookup"><span data-stu-id="b87d1-105">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span> <span data-ttu-id="b87d1-106">TraceLogging consente di includere dati strutturati con eventi, correlare gli eventi e non richiede un file XML del manifesto di strumentazione separato.</span><span class="sxs-lookup"><span data-stu-id="b87d1-106">TraceLogging allows you to include structured data with events, correlate events, and does not require a separate instrumentation manifest XML file.</span></span>

<span data-ttu-id="b87d1-107"><span class="underline">Per gli sviluppatori WinRT</span></span><span class="sxs-lookup"><span data-stu-id="b87d1-107"><span class="underline">For WinRT developers</span></span></span>

-   <span data-ttu-id="b87d1-108">[**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) è stato esteso in Windows 10 per registrare eventi ETW (descrittivi Event Tracing for Windows) senza la necessità di un manifesto.</span><span class="sxs-lookup"><span data-stu-id="b87d1-108">[**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span>
-   <span data-ttu-id="b87d1-109">[**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) è stato esteso in Windows 10 per fornire metodi di avvio e arresto delle attività che consentono di controllare il formato e il contenuto degli eventi di avvio e arresto.</span><span class="sxs-lookup"><span data-stu-id="b87d1-109">[**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="b87d1-110">Inoltre, le attività possono essere nidificate.</span><span class="sxs-lookup"><span data-stu-id="b87d1-110">Additionally, activities can be nested.</span></span>

<span data-ttu-id="b87d1-111"><span class="underline">Per gli sviluppatori di codice gestito (Microsoft .NET Framework)</span></span><span class="sxs-lookup"><span data-stu-id="b87d1-111"><span class="underline">For managed code (Microsoft .NET Framework) developers</span></span></span>

-   <span data-ttu-id="b87d1-112">La classe [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) fornita con versioni precedenti del .NET Framework supporta già la scrittura di eventi ETW senza la necessità di un manifesto.</span><span class="sxs-lookup"><span data-stu-id="b87d1-112">The [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) class that shipped with previous versions of the .NET Framework already supports writing ETW events without the need for a manifest.</span></span> <span data-ttu-id="b87d1-113">Tuttavia, gli sviluppatori dovevano usare EventSource come classe di base e aggiungere attributi e metodi alla classe derivata che venivano automaticamente convertiti in un manifesto ETW.</span><span class="sxs-lookup"><span data-stu-id="b87d1-113">However, developers were required to use EventSource as a base class and add attributes and methods to the derived class that were turned into an ETW manifest automatically.</span></span> <span data-ttu-id="b87d1-114">A questo punto, gli sviluppatori non devono derivare da EventSource e possono invece usare EventSource direttamente per registrare eventi autodescrittivi che non richiedono un manifesto.</span><span class="sxs-lookup"><span data-stu-id="b87d1-114">Now, developers do not have to derive from EventSource and can instead use EventSource directly to log self-describing events that do not require a manifest.</span></span>

<span data-ttu-id="b87d1-115"><span class="underline">Per gli sviluppatori C/C++</span></span><span class="sxs-lookup"><span data-stu-id="b87d1-115"><span class="underline">For C/C++ developers</span></span></span>

-   <span data-ttu-id="b87d1-116">TraceLoggingProvider. h è l'API consigliata per gli sviluppatori C/C++ in modalità utente o kernel.</span><span class="sxs-lookup"><span data-stu-id="b87d1-116">TraceLoggingProvider.h is the recommended API for C/C++ developers in user or kernel mode.</span></span> <span data-ttu-id="b87d1-117">Questa API non è particolarmente adatta per l'uso in scenari dinamici (con script), ad esempio JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b87d1-117">This API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="b87d1-118">I collegamenti seguenti descrivono l'API C/C++.</span><span class="sxs-lookup"><span data-stu-id="b87d1-118">The following links describe the C/C++ API.</span></span>

<!-- -->

-   [<span data-ttu-id="b87d1-119">Classi</span><span class="sxs-lookup"><span data-stu-id="b87d1-119">Classes</span></span>](trace-logging-classes.md)
-   [<span data-ttu-id="b87d1-120">Funzioni</span><span class="sxs-lookup"><span data-stu-id="b87d1-120">Functions</span></span>](trace-logging-functions.md)
-   [<span data-ttu-id="b87d1-121">Macro</span><span class="sxs-lookup"><span data-stu-id="b87d1-121">Macros</span></span>](trace-logging-macros.md)

<span data-ttu-id="b87d1-122">Si noti che il valore di WINVER influirà sul comportamento di TraceLoggingProvider. h.</span><span class="sxs-lookup"><span data-stu-id="b87d1-122">Note that the value of WINVER will impact the way TraceLoggingProvider.h behaves.</span></span>

-   <span data-ttu-id="b87d1-123">Se WINVER non è impostato prima di includere <> Windows. h, <Windows. h> imposterà WINVER su un valore predefinito corrispondente alla versione dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="b87d1-123">If WINVER is not set before including <windows.h>, then <windows.h> will set WINVER to a default value corresponding to the SDK version.</span></span>
-   <span data-ttu-id="b87d1-124">Se si utilizza TraceLoggingProvider. h con WINVER impostato su 0x0602 (Windows 8) o versione successiva, il programma non viene eseguito in Windows Vista o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b87d1-124">Using TraceLoggingProvider.h with WINVER set to 0x0602 (Windows 8) or higher, the program will not run on Windows Vista or Windows 7.</span></span>
-   <span data-ttu-id="b87d1-125">Se si utilizza TraceLoggingProvider. h con WINVER impostato su 0x0600 (Windows Vista) o 0x0601 (Windows 7), il programma verrà configurato per la compatibilità e funzionerà nelle versioni di Windows specificate.</span><span class="sxs-lookup"><span data-stu-id="b87d1-125">Using TraceLoggingProvider.h with WINVER set to 0x0600 (Windows Vista) or 0x0601 (Windows 7), the program will be configured for compatibility and will work on the specified versions of Windows.</span></span>

 

 