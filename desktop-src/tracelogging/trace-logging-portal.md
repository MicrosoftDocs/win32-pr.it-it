---
title: TraceLogging
description: TraceLogging
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7bd83c608d2ac98fdccce760c851496af80c217
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116719"
---
# <a name="tracelogging"></a><span data-ttu-id="058a8-103">TraceLogging</span><span class="sxs-lookup"><span data-stu-id="058a8-103">TraceLogging</span></span>

## <a name="purpose"></a><span data-ttu-id="058a8-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="058a8-104">Purpose</span></span>

<span data-ttu-id="058a8-105">TraceLogging è il nuovo framework Windows 10 di traccia eventi per le applicazioni in modalità utente e i driver in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="058a8-105">TraceLogging is the new Windows 10 event tracing framework for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="058a8-106">TraceLogging si basa su Event Tracing for Windows (ETW) e offre un modo semplificato per instrumentare il codice.</span><span class="sxs-lookup"><span data-stu-id="058a8-106">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="058a8-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="058a8-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="058a8-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="058a8-108">Topic</span></span></th>
<th><span data-ttu-id="058a8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="058a8-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="058a8-110"><a href="trace-logging-about.md">Informazioni su TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="058a8-110"><a href="trace-logging-about.md">About TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="058a8-111">TraceLogging è il nuovo Windows 10 traccia degli eventi per le applicazioni in modalità utente e i driver in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="058a8-111">TraceLogging is the new Windows 10 event tracing for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="058a8-112">TraceLogging è un formato per la descrizione Event Tracing for Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="058a8-112">TraceLogging is a format for self-describing Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="058a8-113">TraceLogging si basa su Event Tracing for Windows (ETW) e offre un modo semplificato per instrumentare il codice.</span><span class="sxs-lookup"><span data-stu-id="058a8-113">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="058a8-114"><a href="tracelogging-using-tracelogging.md">Uso di TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="058a8-114"><a href="tracelogging-using-tracelogging.md">Using TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="058a8-115">Gli argomenti seguenti forniscono una guida introduttiva traceLogging per il codice nativo e gestito, con esempi.</span><span class="sxs-lookup"><span data-stu-id="058a8-115">The following topics provide a TraceLogging quick start for native and managed code, with examples.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="058a8-116"><a href="trace-logging-reference.md">Informazioni di riferimento su TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="058a8-116"><a href="trace-logging-reference.md">TraceLogging Reference</a></span></span><br/></td>
<td><span data-ttu-id="058a8-117">Gli argomenti seguenti forniscono informazioni sull'API TraceLogging nativa.</span><span class="sxs-lookup"><span data-stu-id="058a8-117">The following topics provide information about the native TraceLogging API.</span></span><br/> <span data-ttu-id="058a8-118">TraceLogging si basa su Event Tracing for Windows (ETW) e offre un modo semplificato per instrumentare il codice.</span><span class="sxs-lookup"><span data-stu-id="058a8-118">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span> <span data-ttu-id="058a8-119">TraceLogging consente di includere dati strutturati con eventi, correlare eventi e non richiede un file XML manifesto di strumentazione separato.</span><span class="sxs-lookup"><span data-stu-id="058a8-119">TraceLogging allows you to include structured data with events, correlate events, and does not require a separate instrumentation manifest XML file.</span></span><br/> <span data-ttu-id="058a8-120"><span class="underline">Per gli sviluppatori WinRT</span></span><span class="sxs-lookup"><span data-stu-id="058a8-120"><span class="underline">For WinRT developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="058a8-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> è stato esteso in Windows 10 per registrare eventi ETW (Self-describing Event Tracing for Windows) senza la necessità di un manifesto.</span><span class="sxs-lookup"><span data-stu-id="058a8-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span></li>
<li><span data-ttu-id="058a8-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> è stato esteso in Windows 10 per fornire metodi di avvio e arresto delle attività che forniscono il controllo sul formato e sul contenuto degli eventi Start e Stop.</span><span class="sxs-lookup"><span data-stu-id="058a8-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="058a8-123">Inoltre, le attività possono essere annidate.</span><span class="sxs-lookup"><span data-stu-id="058a8-123">Additionally, activities can be nested.</span></span></li>
</ul><span data-ttu-id="058a8-124">
<span class="underline">Per sviluppatori di codice gestito (Microsoft .NET Framework)</span></span><span class="sxs-lookup"><span data-stu-id="058a8-124">
<span class="underline">For managed code (Microsoft .NET Framework) developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="058a8-125">La <a href="/dotnet/api/system.diagnostics.tracing.eventsource">classe EventSource</a> fornita con le versioni precedenti del .NET Framework supporta già la scrittura di eventi ETW senza la necessità di un manifesto.</span><span class="sxs-lookup"><span data-stu-id="058a8-125">The <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> class that shipped with previous versions of the .NET Framework already supports writing ETW events without the need for a manifest.</span></span> <span data-ttu-id="058a8-126">Tuttavia, gli sviluppatori dovevano usare EventSource come classe di base e aggiungere attributi e metodi alla classe derivata che venivano automaticamente trasformati in un manifesto ETW.</span><span class="sxs-lookup"><span data-stu-id="058a8-126">However, developers were required to use EventSource as a base class and add attributes and methods to the derived class that were turned into an ETW manifest automatically.</span></span> <span data-ttu-id="058a8-127">A questo punto, gli sviluppatori non devono derivare da EventSource e possono invece usare Direttamente EventSource per registrare eventi autodescrittori che non richiedono un manifesto.</span><span class="sxs-lookup"><span data-stu-id="058a8-127">Now, developers do not have to derive from EventSource and can instead use EventSource directly to log self-describing events that do not require a manifest.</span></span></li>
</ul><span data-ttu-id="058a8-128">
<span class="underline">Per sviluppatori C/C++</span></span><span class="sxs-lookup"><span data-stu-id="058a8-128">
<span class="underline">For C/C++ developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="058a8-129">TraceLoggingProvider.h è l'API consigliata per gli sviluppatori C/C++ in modalità utente o kernel.</span><span class="sxs-lookup"><span data-stu-id="058a8-129">TraceLoggingProvider.h is the recommended API for C/C++ developers in user or kernel mode.</span></span> <span data-ttu-id="058a8-130">Questa API non è adatta per l'uso in scenari dinamici (con script), ad esempio Javascript.</span><span class="sxs-lookup"><span data-stu-id="058a8-130">This API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="058a8-131">I collegamenti seguenti descrivono l'API C/C++.</span><span class="sxs-lookup"><span data-stu-id="058a8-131">The following links describe the C/C++ API.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a><span data-ttu-id="058a8-132">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="058a8-132">Developer audience</span></span>

<span data-ttu-id="058a8-133">TraceLogging è progettato per l'uso da parte degli sviluppatori di applicazioni in modalità utente e degli sviluppatori di driver in modalità kernel che vogliono aggiungere la traccia al codice.</span><span class="sxs-lookup"><span data-stu-id="058a8-133">TraceLogging is designed for use by user-mode application developers and kernel-mode driver developers who want to add tracing to their code.</span></span>

