---
description: ETW fornisce un modo per raggruppare gli eventi correlati da più di un componente.
ms.assetid: 2a85e4af-a1fe-4c28-8ce2-14d15deaa820
title: Scrittura di eventi correlati in uno scenario end-to-end
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d27b3455ffe71c6d657e935e6f93dc2dc39392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977767"
---
# <a name="writing-related-events-in-an-end-to-end-scenario"></a><span data-ttu-id="35074-103">Scrittura di eventi correlati in uno scenario end-to-end</span><span class="sxs-lookup"><span data-stu-id="35074-103">Writing Related Events in an End-to-End Scenario</span></span>

<span data-ttu-id="35074-104">ETW fornisce un modo per raggruppare gli eventi correlati da più di un componente.</span><span class="sxs-lookup"><span data-stu-id="35074-104">ETW provides a way to group related events from more than one component.</span></span> <span data-ttu-id="35074-105">Se, ad esempio, diversi componenti, nello stesso computer o in computer diversi, sono interessati all'elaborazione degli stessi dati e ogni componente registra gli eventi per la parte dell'attività, è possibile raggruppare tutti gli eventi correlati.</span><span class="sxs-lookup"><span data-stu-id="35074-105">For example, if several components (either on the same computer or on different computers) are involved in processing the same data, and each component logs events for their portion of the activity, you can group all of the related events together.</span></span> <span data-ttu-id="35074-106">Ciò consentirà a un consumer di utilizzare tutti gli eventi, dall'inizio del processo fino alla fine del processo.</span><span class="sxs-lookup"><span data-stu-id="35074-106">This will allow a consumer to consume all of the events, from the beginning of the process to the end of the process.</span></span>

<span data-ttu-id="35074-107">Per scrivere eventi correlati in un provider [basato su manifesto](about-event-tracing.md) , vedere [scrittura di eventi correlati in un provider basato su manifesto](writing-related-events-in-a-manifest-base-provider.md).</span><span class="sxs-lookup"><span data-stu-id="35074-107">To write related events in a [manifest-based](about-event-tracing.md) provider, see [Writing Related Events in a Manifest-based Provider](writing-related-events-in-a-manifest-base-provider.md).</span></span>

<span data-ttu-id="35074-108">Per scrivere eventi correlati in un provider [classico](about-event-tracing.md) , vedere [scrittura di eventi correlati in un provider classico](tracing-event-instances.md).</span><span class="sxs-lookup"><span data-stu-id="35074-108">To write related events in a [classic](about-event-tracing.md) provider, see [Writing Related Events in a Classic Provider](tracing-event-instances.md).</span></span>

 

 



