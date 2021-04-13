---
title: Traccia di rete in Windows 7
description: Windows 7 si espande sul Framework di diagnostica di rete (NDF) per fornire un metodo rapido per la risoluzione dei problemi di connettività di rete abilitando la raccolta di tutte le informazioni necessarie in un unico passaggio e sfruttando Event Tracing for Windows (ETW) per registrare i pacchetti di eventi di rete in un unico file.
ms.assetid: 7d331362-ff26-4ca0-aa45-07cc97304c7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e3abb4283262703123f8e7060a09af0b810477b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399693"
---
# <a name="network-tracing-in-windows-7"></a><span data-ttu-id="6c1fc-103">Traccia di rete in Windows 7</span><span class="sxs-lookup"><span data-stu-id="6c1fc-103">Network Tracing in Windows 7</span></span>

<span data-ttu-id="6c1fc-104">Con l'aumentare della complessità dello stack di rete, è spesso difficile tracciare e diagnosticare rapidamente i problemi all'interno dello stack.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-104">As the complexity of the networking stack increases, it is often difficult to quickly trace and diagnose issues within the stack.</span></span> <span data-ttu-id="6c1fc-105">Windows 7 si espande sul Framework di diagnostica di rete (NDF) per fornire un metodo rapido per la risoluzione dei problemi di connettività di rete abilitando la raccolta di tutte le informazioni necessarie in un unico passaggio e sfruttando [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) per registrare gli eventi di rete & pacchetti in un unico file.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-105">Windows 7 expands on the Network Diagnostic Framework (NDF) to provide a quick method for troubleshooting network connectivity issues by enabling collection of all the needed information in one step, and by leveraging [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) to log network events & packets in a single file.</span></span>

<span data-ttu-id="6c1fc-106">Gli eventi e i pacchetti correlati vengono raggruppati per una determinata attività, ad esempio l'esplorazione di un sito Web, tra i vari componenti nello stack di rete.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-106">Related events and packets are grouped together for a given activity, such as browsing a website, across the various components in the networking stack.</span></span> <span data-ttu-id="6c1fc-107">L'output di questo processo è un file di log di traccia eventi (ETL).</span><span class="sxs-lookup"><span data-stu-id="6c1fc-107">The output of this process is an Event Trace Log (ETL) file.</span></span> <span data-ttu-id="6c1fc-108">Consentendo la visualizzazione di tutti gli eventi correlati a un'attività specifica in una sola volta in questo file, è possibile ridurre notevolmente il tempo necessario per isolare e diagnosticare i problemi di rete.</span><span class="sxs-lookup"><span data-stu-id="6c1fc-108">By allowing all of the events related to a specific activity to be viewed at once in this file, the time required to isolate and diagnose network issues can be greatly reduced.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6c1fc-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="6c1fc-109">In This Section</span></span>



| <span data-ttu-id="6c1fc-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="6c1fc-110">Topic</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c1fc-111">Traccia di rete in Windows 7: architettura</span><span class="sxs-lookup"><span data-stu-id="6c1fc-111">Network Tracing in Windows 7: Architecture</span></span>](network-tracing-in-windows-7-architecture.md)                                |
| [<span data-ttu-id="6c1fc-112">Strumenti per la risoluzione dei problemi tramite la traccia di rete in Windows 7</span><span class="sxs-lookup"><span data-stu-id="6c1fc-112">Tools for Troubleshooting using Network Tracing in Windows 7</span></span>](tools-for-troubleshooting-network-tracing-in-windows-7.md) |
| [<span data-ttu-id="6c1fc-113">Traccia di rete in Windows 7: scenari</span><span class="sxs-lookup"><span data-stu-id="6c1fc-113">Network Tracing in Windows 7: Scenarios</span></span>](network-tracing-in-windows-7-scenarios.md)                                      |



 

 

 