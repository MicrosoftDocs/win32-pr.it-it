---
description: Le funzioni di debug possono essere utilizzate per creare un debugger di base basato su eventi.
ms.assetid: 3c9e186b-6844-4126-b035-a3541880e109
title: Informazioni sul debug di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daa3e2889d860d747978f2e8866094b0f866910c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877465"
---
# <a name="about-basic-debugging"></a><span data-ttu-id="525eb-103">Informazioni sul debug di base</span><span class="sxs-lookup"><span data-stu-id="525eb-103">About Basic Debugging</span></span>

<span data-ttu-id="525eb-104">Le [funzioni di debug](debugging-functions.md) possono essere utilizzate per creare un debugger di base basato su eventi.</span><span class="sxs-lookup"><span data-stu-id="525eb-104">The [debugging functions](debugging-functions.md) can be used to create a basic, event-driven debugger.</span></span> <span data-ttu-id="525eb-105">La guida basata sugli *eventi* indica che il debugger riceve una notifica ogni volta che si verificano determinati eventi nel processo di cui è in corso il debug.</span><span class="sxs-lookup"><span data-stu-id="525eb-105">*Event-driven* means that the debugger is notified every time certain events occur in the process being debugged.</span></span> <span data-ttu-id="525eb-106">La notifica consente al debugger di eseguire l'azione appropriata in risposta agli eventi.</span><span class="sxs-lookup"><span data-stu-id="525eb-106">Notification enables the debugger to take appropriate action in response to the events.</span></span>

<span data-ttu-id="525eb-107">Per una panoramica dei termini di debug, vedere [terminologia di debug](debugging-terminology.md).</span><span class="sxs-lookup"><span data-stu-id="525eb-107">For an overview of debugging terms, see [Debugging Terminology](debugging-terminology.md).</span></span>

<span data-ttu-id="525eb-108">Il [supporto del debug da funzioni di processo, thread e di eccezione](debug-support-from-process-thread-and-exception-functions.md) descrive le funzionalità specifiche del debug di determinate funzioni di elaborazione, thread e gestione delle eccezioni.</span><span class="sxs-lookup"><span data-stu-id="525eb-108">[Debug Support from Process, Thread, and Exception Functions](debug-support-from-process-thread-and-exception-functions.md) describes the debugging-specific features of certain process, thread, and exception-handling functions.</span></span>

<span data-ttu-id="525eb-109">La [creazione di un debugger di base](creating-a-basic-debugger.md) descrive l'utilizzo delle funzioni di debug di base per creare un debugger semplice.</span><span class="sxs-lookup"><span data-stu-id="525eb-109">[Creating a Basic Debugger](creating-a-basic-debugger.md) describes using the basic debugging functions to create a simple debugger.</span></span> <span data-ttu-id="525eb-110">Queste funzioni consentono a un'applicazione di attendere gli eventi di debug, causare eccezioni del punto di interruzione, trasferire il controllo di esecuzione al debugger e così via.</span><span class="sxs-lookup"><span data-stu-id="525eb-110">These functions enable an application to wait for debugging events, cause breakpoint exceptions, transfer execution control to the debugger, and so on.</span></span>

<span data-ttu-id="525eb-111">[Gli eventi di debug](debugging-events.md) descrivono il meccanismo dell'evento di debug.</span><span class="sxs-lookup"><span data-stu-id="525eb-111">[Debugging Events](debugging-events.md) describes the debug event mechanism.</span></span> <span data-ttu-id="525eb-112">Gli eventi di debug fanno sì che il sistema invii una notifica al debugger.</span><span class="sxs-lookup"><span data-stu-id="525eb-112">Debugging events cause the system to notify the debugger.</span></span>

 

 



