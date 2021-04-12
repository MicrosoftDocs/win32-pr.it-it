---
title: Funzioni hook In-Context
ms.assetid: bf12bda6-b00e-4fbe-a576-b989aa428b54
description: 'Altre informazioni su: funzioni hook In-Context'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe25bd64234cfbfd92f054565aa7c675328b435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233997"
---
# <a name="in-context-hook-functions"></a><span data-ttu-id="7bbf4-103">Funzioni hook In-Context</span><span class="sxs-lookup"><span data-stu-id="7bbf4-103">In-Context Hook Functions</span></span>

<span data-ttu-id="7bbf4-104">Nell'elenco seguente vengono descritti gli aspetti chiave delle funzioni hook nel contesto:</span><span class="sxs-lookup"><span data-stu-id="7bbf4-104">The following list outlines the key aspects of in-context hook functions:</span></span>

-   <span data-ttu-id="7bbf4-105">Le funzioni hook nel contesto devono trovarsi in una libreria di collegamento dinamico (DLL) di cui il sistema esegue il mapping nello spazio degli indirizzi del server.</span><span class="sxs-lookup"><span data-stu-id="7bbf4-105">In-context hooks functions must be located in a dynamic-link library (DLL) that the system maps into the server's address space.</span></span>
-   <span data-ttu-id="7bbf4-106">Le funzioni hook nel contesto condividono lo spazio degli indirizzi con il server.</span><span class="sxs-lookup"><span data-stu-id="7bbf4-106">In-context hook functions share the address space with the server.</span></span>
-   <span data-ttu-id="7bbf4-107">Quando il server attiva un evento, il sistema chiama una funzione hook senza marshalling (creazione di pacchetti e invio di parametri di interfaccia tra i limiti del processo).</span><span class="sxs-lookup"><span data-stu-id="7bbf4-107">When the server triggers an event, the system calls a hook function without marshaling (packaging and sending interface parameters across process boundaries).</span></span>
-   <span data-ttu-id="7bbf4-108">Le funzioni hook nel contesto tendono a essere molto veloci e a ricevere notifiche di eventi in modo sincrono perché non è presente alcun marshalling.</span><span class="sxs-lookup"><span data-stu-id="7bbf4-108">In-context hook functions tend to be very fast and receive event notifications synchronously because there is no marshaling.</span></span>
-   <span data-ttu-id="7bbf4-109">Alcuni eventi possono essere recapitati out-of-process, anche se si richiede che vengano recapitati in-process (usando il \_ flag INCONTEXT WINEVENT).</span><span class="sxs-lookup"><span data-stu-id="7bbf4-109">Some events may be delivered out-of-process, even though you request that they be delivered in-process (using the WINEVENT\_INCONTEXT flag).</span></span> <span data-ttu-id="7bbf4-110">Questa situazione può verificarsi con problemi di interoperabilità delle applicazioni a 64 bit e a 32 bit e con eventi della console di Windows.</span><span class="sxs-lookup"><span data-stu-id="7bbf4-110">You might see this situation with 64-bit and 32-bit application interoperability issues and with Windows console events.</span></span>

 

 




