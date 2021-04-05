---
title: TraceLogging
description: .
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975c2f70cc645cc04d6b1461e32bb3b899097d1c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103733647"
---
# <a name="tracelogging"></a><span data-ttu-id="101e0-103">TraceLogging</span><span class="sxs-lookup"><span data-stu-id="101e0-103">TraceLogging</span></span>

## <a name="purpose"></a><span data-ttu-id="101e0-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="101e0-104">Purpose</span></span>

<span data-ttu-id="101e0-105">TraceLogging è il nuovo Framework di analisi degli eventi di Windows 10 per le applicazioni in modalità utente e i driver in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="101e0-105">TraceLogging is the new Windows 10 event tracing framework for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="101e0-106">TraceLogging si basa su Event Tracing for Windows (ETW) e fornisce un modo semplificato per instrumentare il codice.</span><span class="sxs-lookup"><span data-stu-id="101e0-106">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="101e0-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="101e0-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="101e0-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="101e0-108">Topic</span></span></th>
<th><span data-ttu-id="101e0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="101e0-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="101e0-110"><a href="trace-logging-about.md">Informazioni su TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="101e0-110"><a href="trace-logging-about.md">About TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="101e0-111">TraceLogging è la nuova traccia eventi di Windows 10 per le applicazioni in modalità utente e i driver in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="101e0-111">TraceLogging is the new Windows 10 event tracing for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="101e0-112">TraceLogging è un formato per il Event Tracing for Windows (ETW) autodescrittivo.</span><span class="sxs-lookup"><span data-stu-id="101e0-112">TraceLogging is a format for self-describing Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="101e0-113">TraceLogging si basa su Event Tracing for Windows (ETW) e fornisce un modo semplificato per instrumentare il codice.</span><span class="sxs-lookup"><span data-stu-id="101e0-113">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="101e0-114"><a href="tracelogging-using-tracelogging.md">Uso di TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="101e0-114"><a href="tracelogging-using-tracelogging.md">Using TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="101e0-115">Gli argomenti seguenti forniscono una guida introduttiva a TraceLogging per il codice nativo e gestito, con esempi.</span><span class="sxs-lookup"><span data-stu-id="101e0-115">The following topics provide a TraceLogging quick start for native and managed code, with examples.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="101e0-116"><a href="trace-logging-reference.md">Riferimento a TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="101e0-116"><a href="trace-logging-reference.md">TraceLogging Reference</a></span></span><br/></td>
<td><span data-ttu-id="101e0-117">Negli argomenti seguenti vengono fornite informazioni sull'API TraceLogging nativa.</span><span class="sxs-lookup"><span data-stu-id="101e0-117">The following topics provide information about the native TraceLogging API.</span></span><br/> <span data-ttu-id="101e0-118">TraceLogging si basa su Event Tracing for Windows (ETW) e fornisce un modo semplificato per instrumentare il codice.</span><span class="sxs-lookup"><span data-stu-id="101e0-118">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span> <span data-ttu-id="101e0-119">TraceLogging consente di includere dati strutturati con eventi, correlare gli eventi e non richiede un file XML del manifesto di strumentazione separato.</span><span class="sxs-lookup"><span data-stu-id="101e0-119">TraceLogging allows you to include structured data with events, correlate events, and does not require a separate instrumentation manifest XML file.</span></span><br/> <span data-ttu-id="101e0-120"><span class="underline">Per gli sviluppatori WinRT</span></span><span class="sxs-lookup"><span data-stu-id="101e0-120"><span class="underline">For WinRT developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="101e0-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> è stato esteso in Windows 10 per registrare eventi ETW (descrittivi Event Tracing for Windows) senza la necessità di un manifesto.</span><span class="sxs-lookup"><span data-stu-id="101e0-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span></li>
<li><span data-ttu-id="101e0-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> è stato esteso in Windows 10 per fornire metodi di avvio e arresto delle attività che consentono di controllare il formato e il contenuto degli eventi di avvio e arresto.</span><span class="sxs-lookup"><span data-stu-id="101e0-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="101e0-123">Inoltre, le attività possono essere nidificate.</span><span class="sxs-lookup"><span data-stu-id="101e0-123">Additionally, activities can be nested.</span></span></li>
</ul><span data-ttu-id="101e0-124">
<span class="underline">Per gli sviluppatori di codice gestito (Microsoft .NET Framework)</span></span><span class="sxs-lookup"><span data-stu-id="101e0-124">
<span class="underline">For managed code (Microsoft .NET Framework) developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="101e0-125">La classe <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> fornita con versioni precedenti del .NET Framework supporta già la scrittura di eventi ETW senza la necessità di un manifesto.</span><span class="sxs-lookup"><span data-stu-id="101e0-125">The <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> class that shipped with previous versions of the .NET Framework already supports writing ETW events without the need for a manifest.</span></span> <span data-ttu-id="101e0-126">Tuttavia, gli sviluppatori dovevano usare EventSource come classe di base e aggiungere attributi e metodi alla classe derivata che venivano automaticamente convertiti in un manifesto ETW.</span><span class="sxs-lookup"><span data-stu-id="101e0-126">However, developers were required to use EventSource as a base class and add attributes and methods to the derived class that were turned into an ETW manifest automatically.</span></span> <span data-ttu-id="101e0-127">A questo punto, gli sviluppatori non devono derivare da EventSource e possono invece usare EventSource direttamente per registrare eventi autodescrittivi che non richiedono un manifesto.</span><span class="sxs-lookup"><span data-stu-id="101e0-127">Now, developers do not have to derive from EventSource and can instead use EventSource directly to log self-describing events that do not require a manifest.</span></span></li>
</ul><span data-ttu-id="101e0-128">
<span class="underline">Per gli sviluppatori C/C++</span></span><span class="sxs-lookup"><span data-stu-id="101e0-128">
<span class="underline">For C/C++ developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="101e0-129">TraceLoggingProvider. h è l'API consigliata per gli sviluppatori C/C++ in modalità utente o kernel.</span><span class="sxs-lookup"><span data-stu-id="101e0-129">TraceLoggingProvider.h is the recommended API for C/C++ developers in user or kernel mode.</span></span> <span data-ttu-id="101e0-130">Questa API non è particolarmente adatta per l'uso in scenari dinamici (con script), ad esempio JavaScript.</span><span class="sxs-lookup"><span data-stu-id="101e0-130">This API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="101e0-131">I collegamenti seguenti descrivono l'API C/C++.</span><span class="sxs-lookup"><span data-stu-id="101e0-131">The following links describe the C/C++ API.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a><span data-ttu-id="101e0-132">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="101e0-132">Developer audience</span></span>

<span data-ttu-id="101e0-133">TraceLogging è progettato per essere utilizzato dagli sviluppatori di applicazioni in modalità utente e dagli sviluppatori di driver in modalità kernel che desiderano aggiungere la traccia al codice.</span><span class="sxs-lookup"><span data-stu-id="101e0-133">TraceLogging is designed for use by user-mode application developers and kernel-mode driver developers who want to add tracing to their code.</span></span>

