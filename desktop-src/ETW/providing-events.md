---
description: I provider sono applicazioni che contengono la strumentazione di traccia eventi.
ms.assetid: b522f16d-8d61-4db3-9194-d965b6d859ec
title: Invio di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc53daa602662dfabd163560e8e9d69a888be610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977634"
---
# <a name="providing-events"></a><span data-ttu-id="a5664-103">Invio di eventi</span><span class="sxs-lookup"><span data-stu-id="a5664-103">Providing Events</span></span>

<span data-ttu-id="a5664-104">I provider sono applicazioni che contengono la strumentazione di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="a5664-104">Providers are applications that contain event tracing instrumentation.</span></span> <span data-ttu-id="a5664-105">Dopo la registrazione di un provider, un controller può quindi abilitare o disabilitare la traccia eventi nel provider.</span><span class="sxs-lookup"><span data-stu-id="a5664-105">After a provider registers itself, a controller can then enable or disable event tracing in the provider.</span></span> <span data-ttu-id="a5664-106">Il provider definisce l'interpretazione dell'abilitazione o disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="a5664-106">The provider defines its interpretation of being enabled or disabled.</span></span> <span data-ttu-id="a5664-107">In genere, un provider abilitato genera eventi e un provider disabilitato non lo consente.</span><span class="sxs-lookup"><span data-stu-id="a5664-107">Generally, an enabled provider generates events, and a disabled provider does not.</span></span> <span data-ttu-id="a5664-108">In questo modo è possibile aggiungere la traccia eventi all'applicazione senza che sia necessario generare eventi sempre.</span><span class="sxs-lookup"><span data-stu-id="a5664-108">This lets you add event tracing to your application without requiring that it generate events all the time.</span></span>

<span data-ttu-id="a5664-109">Questa sezione illustra come eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a5664-109">This section shows you how to:</span></span>

-   [<span data-ttu-id="a5664-110">Eventi di scrittura</span><span class="sxs-lookup"><span data-stu-id="a5664-110">Write events</span></span>](writing-events.md)
-   [<span data-ttu-id="a5664-111">Scrivi eventi correlati</span><span class="sxs-lookup"><span data-stu-id="a5664-111">Write related events</span></span>](writing-related-events-in-an-end-to-end-scenario.md)
-   [<span data-ttu-id="a5664-112">Pubblicare lo schema dell'evento da condividere con gli utenti</span><span class="sxs-lookup"><span data-stu-id="a5664-112">Publish your event schema to share with consumers</span></span>](publishing-your-event-schema.md)

<span data-ttu-id="a5664-113">Per informazioni sul controllo delle sessioni di traccia eventi, vedere [controllo delle sessioni di traccia eventi](controlling-event-tracing-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="a5664-113">For information about controlling event tracing sessions, see [Controlling Event Tracing Sessions](controlling-event-tracing-sessions.md).</span></span> <span data-ttu-id="a5664-114">Per informazioni sull'utilizzo di eventi da un provider di traccia eventi, vedere [utilizzo degli eventi](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="a5664-114">For information about consuming events from an event trace provider, see [Consuming Events](consuming-events.md).</span></span>

 

 



