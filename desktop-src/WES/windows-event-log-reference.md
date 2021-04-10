---
title: Riferimento al registro eventi di Windows
description: Di seguito sono riportati gli elementi di programmazione usati per creare un manifesto di strumentazione, creare risorse dal manifesto usato dal provider, ottenere i metadati di strumentazione in fase di esecuzione ed eseguire query sugli eventi da canali e file di log
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fef1af82cdab1ab92b4ea4768479541053fe65d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049121"
---
# <a name="windows-event-log-reference"></a><span data-ttu-id="3095d-103">Riferimento al registro eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="3095d-103">Windows Event Log Reference</span></span>

<span data-ttu-id="3095d-104">Di seguito sono riportati gli elementi di programmazione usati per creare un manifesto di strumentazione, creare risorse dal manifesto usato dal provider, ottenere i metadati di strumentazione in fase di esecuzione ed eseguire query sugli eventi da canali e file di log:</span><span class="sxs-lookup"><span data-stu-id="3095d-104">The following are the programming elements that you use to create an instrumentation manifest, create resources from the manifest that your provider uses, get instrumentation metadata at run time, and query events from channels and log files:</span></span>

-   [<span data-ttu-id="3095d-105">Schema EventManifest</span><span class="sxs-lookup"><span data-stu-id="3095d-105">EventManifest Schema</span></span>](eventmanifestschema-schema.md)
-   [<span data-ttu-id="3095d-106">Schema dell'evento</span><span class="sxs-lookup"><span data-stu-id="3095d-106">Event Schema</span></span>](eventschema-schema.md)
-   [<span data-ttu-id="3095d-107">Schema di query</span><span class="sxs-lookup"><span data-stu-id="3095d-107">Query Schema</span></span>](queryschema-schema.md)
-   [<span data-ttu-id="3095d-108">Costanti registro eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="3095d-108">Windows Event Log Constants</span></span>](windows-event-log-constants.md)
-   [<span data-ttu-id="3095d-109">Tipi di dati del registro eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="3095d-109">Windows Event Log Data Types</span></span>](windows-event-log-data-types.md)
-   [<span data-ttu-id="3095d-110">Enumerazioni del registro eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="3095d-110">Windows Event Log Enumerations</span></span>](windows-event-log-enumerations.md)
-   [<span data-ttu-id="3095d-111">Funzioni del registro eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="3095d-111">Windows Event Log Functions</span></span>](windows-event-log-functions.md)
-   [<span data-ttu-id="3095d-112">Strutture del registro eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="3095d-112">Windows Event Log Structures</span></span>](windows-event-log-structures.md)
-   [<span data-ttu-id="3095d-113">Strumenti del registro eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="3095d-113">Windows Event Log Tools</span></span>](windows-event-log-tools.md)

<span data-ttu-id="3095d-114">Per le applicazioni scritte con un linguaggio .NET, ad esempio C# o Visual Basic, vedere gli spazi dei nomi seguenti:</span><span class="sxs-lookup"><span data-stu-id="3095d-114">For applications written using a .NET language, such as C# or Visual Basic, see the following namespaces:</span></span>

-   <span data-ttu-id="3095d-115">Per scrivere eventi, usare le classi e i metodi definiti nello spazio dei nomi [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) .</span><span class="sxs-lookup"><span data-stu-id="3095d-115">To write events, use the classes and methods defined in the [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) namespace.</span></span>
-   <span data-ttu-id="3095d-116">Per utilizzare eventi da un canale o da un registro eventi di Windows, utilizzare le classi e i metodi definiti nello spazio dei nomi [System. Diagnostics. Eventing. Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="3095d-116">To consume events from a Windows Event Log channel or log, use the classes and methods defined in the [System.Diagnostics.Eventing.Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.</span></span>

<span data-ttu-id="3095d-117">In alternativa all'utilizzo dello spazio dei nomi [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) per la scrittura di eventi, è possibile utilizzare l'argomento **-CS** o **-CSS** per fare in modo che il compilatore del messaggio generi il codice per la scrittura degli eventi.</span><span class="sxs-lookup"><span data-stu-id="3095d-117">As an alternative to using the [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) namespace to write events, you can use the **-cs** or **-css** argument to have the message compiler generate the code to write the events.</span></span> <span data-ttu-id="3095d-118">Per informazioni dettagliate, vedere [**compilatore di messaggi**](message-compiler--mc-exe-.md).</span><span class="sxs-lookup"><span data-stu-id="3095d-118">For details, see [**Message Compiler**](message-compiler--mc-exe-.md).</span></span>
