---
title: Funzioni hook fuori contesto
ms.assetid: c0156485-db1e-42d3-bbbd-c51835a597ed
description: 'Altre informazioni su: funzioni hook fuori contesto'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5837c39850c5821d44146498f62d4c874e7802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883798"
---
# <a name="out-of-context-hook-functions"></a><span data-ttu-id="90c69-103">Funzioni hook fuori contesto</span><span class="sxs-lookup"><span data-stu-id="90c69-103">Out-of-Context Hook Functions</span></span>

<span data-ttu-id="90c69-104">Nell'elenco seguente vengono illustrati gli aspetti chiave delle funzioni hook fuori contesto:</span><span class="sxs-lookup"><span data-stu-id="90c69-104">The following list outlines the key aspects of out-of-context hook functions:</span></span>

-   <span data-ttu-id="90c69-105">Le funzioni hook fuori contesto si trovano nello spazio degli indirizzi del client, se si trova nel corpo del codice o in una DLL.</span><span class="sxs-lookup"><span data-stu-id="90c69-105">Out-of-context hook functions are located in the client's address space, whether it is in the code body or in a DLL.</span></span>
-   <span data-ttu-id="90c69-106">Non è stato eseguito il mapping delle funzioni hook out-of-Context nello spazio degli indirizzi del server.</span><span class="sxs-lookup"><span data-stu-id="90c69-106">Out-of-context hook functions are not mapped into the server's address space.</span></span>
-   <span data-ttu-id="90c69-107">Quando viene attivato un evento, i parametri per la funzione hook vengono sottoposti a marshalling tra i limiti del processo.</span><span class="sxs-lookup"><span data-stu-id="90c69-107">When an event is triggered, the parameters for the hook function are marshaled across process boundaries.</span></span>
-   <span data-ttu-id="90c69-108">Le funzioni hook fuori contesto sono notevolmente più lente rispetto alle funzioni hook nel contesto a causa del marshalling.</span><span class="sxs-lookup"><span data-stu-id="90c69-108">Out-of-context hook functions are noticeably slower than in-context hook functions due to marshaling.</span></span>
-   <span data-ttu-id="90c69-109">Il sistema accoda le notifiche degli eventi in modo che arrivino in modo asincrono (a causa del tempo necessario per eseguire il marshalling).</span><span class="sxs-lookup"><span data-stu-id="90c69-109">The system queues the event notifications so that they arrive asynchronously (because of the time required to perform marshaling).</span></span>

<span data-ttu-id="90c69-110">Sebbene le notifiche degli eventi siano asincrone, Microsoft Active Accessibility garantisce che la funzione di callback riceva tutti gli eventi nell'ordine in cui vengono generati.</span><span class="sxs-lookup"><span data-stu-id="90c69-110">Although the event notifications are asynchronous, Microsoft Active Accessibility assures that the callback function receives all events in the order in which they are generated.</span></span>

<span data-ttu-id="90c69-111">Il componente utente del sistema operativo alloca memoria per gli eventi gestiti da funzioni hook fuori contesto.</span><span class="sxs-lookup"><span data-stu-id="90c69-111">The USER component of the operating system allocates memory for events that are handled by out-of-context hook functions.</span></span> <span data-ttu-id="90c69-112">La memoria viene liberata quando le funzioni hook restituiscono.</span><span class="sxs-lookup"><span data-stu-id="90c69-112">The memory is freed when the hook functions return.</span></span> <span data-ttu-id="90c69-113">Se una funzione hook non elabora gli eventi in modo sufficientemente rapido, le risorse utente vengono ridotte, causando un errore o tempi di risposta estremamente lenti.</span><span class="sxs-lookup"><span data-stu-id="90c69-113">If a hook function does not process events quickly enough, USER resources are lowered, eventually resulting in a fault or extremely slow response times.</span></span> <span data-ttu-id="90c69-114">Questi problemi possono verificarsi se:</span><span class="sxs-lookup"><span data-stu-id="90c69-114">These problems may occur if:</span></span>

-   <span data-ttu-id="90c69-115">Gli eventi vengono generati molto rapidamente.</span><span class="sxs-lookup"><span data-stu-id="90c69-115">Events are fired very rapidly.</span></span>
-   <span data-ttu-id="90c69-116">Il sistema è lento.</span><span class="sxs-lookup"><span data-stu-id="90c69-116">The system is slow.</span></span>
-   <span data-ttu-id="90c69-117">La funzione hook elabora gli eventi lentamente.</span><span class="sxs-lookup"><span data-stu-id="90c69-117">The hook function processes events slowly.</span></span>
-   <span data-ttu-id="90c69-118">Il client è in esecuzione in Windows 9x.</span><span class="sxs-lookup"><span data-stu-id="90c69-118">The client is running on Windows 9x.</span></span>

 

 




