---
description: Tipi di thread del dispenser di risorse COM+
ms.assetid: 3ab67adb-311f-404c-a3ca-d274af53f91c
title: Tipi di thread del dispenser di risorse COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761d85edc3105785ded904fd2dc6083a9aea30cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401403"
---
# <a name="com-resource-dispenser-thread-types"></a><span data-ttu-id="7796c-103">Tipi di thread del dispenser di risorse COM+</span><span class="sxs-lookup"><span data-stu-id="7796c-103">COM+ Resource Dispenser Thread Types</span></span>

<span data-ttu-id="7796c-104">Le chiamate a un dispenser di risorse COM+ possono avere origine in uno dei seguenti tipi di thread:</span><span class="sxs-lookup"><span data-stu-id="7796c-104">Calls into a COM+ resource dispenser may originate in one of the following thread types:</span></span>

-   <span data-ttu-id="7796c-105">Thread Apartment (STA)</span><span class="sxs-lookup"><span data-stu-id="7796c-105">Apartment thread (STA)</span></span>
-   <span data-ttu-id="7796c-106">Thread libero (MTA)</span><span class="sxs-lookup"><span data-stu-id="7796c-106">Free thread (MTA)</span></span>
-   <span data-ttu-id="7796c-107">Thread non COM (applicazione o thread del Garbage Collector di [Gestione dispenser](com--dispenser-manager.md) )</span><span class="sxs-lookup"><span data-stu-id="7796c-107">Non-COM thread (application or the [dispenser manager](com--dispenser-manager.md) garbage-collector thread)</span></span>

<span data-ttu-id="7796c-108">Se un dispenser di risorse non è un oggetto COM, deve essere in grado di gestire le chiamate provenienti da qualsiasi thread in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="7796c-108">If a resource dispenser is not a COM object, it must be able to handle calls arriving from any thread at any time.</span></span> <span data-ttu-id="7796c-109">Se un dispenser di risorse è un oggetto COM, l'oggetto COM deve essere registrato con un modello di threading di **entrambi**.</span><span class="sxs-lookup"><span data-stu-id="7796c-109">If a resource dispenser is a COM object, the COM object should be registered with a threading model of **Both**.</span></span> <span data-ttu-id="7796c-110">Questo consente ai thread STA o MTA di creare e usare il dispenser di risorse senza un cambio di thread.</span><span class="sxs-lookup"><span data-stu-id="7796c-110">This allows STA or MTA threads to create and use the resource dispenser without a thread switch.</span></span>

<span data-ttu-id="7796c-111">Se un dispenser di risorse crea e usa un altro oggetto COM (ad esempio, un gestore di risorse out-of-process), il dispenser di risorse potrebbe dover gestire più proxy per questo altro oggetto COM e assicurarsi che le chiamate all'oggetto vengano effettuate usando il proxy appropriato per il thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="7796c-111">If a resource dispenser creates and uses another COM object (for example, an out-of-process resource manager), the resource dispenser might need to maintain multiple proxies to this other COM object and ensure that calls to the object are made using the appropriate proxy for the calling thread.</span></span> <span data-ttu-id="7796c-112">Quando il dispenser di risorse crea questo oggetto, esegue il marshalling e salva il riferimento.</span><span class="sxs-lookup"><span data-stu-id="7796c-112">When the resource dispenser creates this object, it marshals and saves the reference.</span></span> <span data-ttu-id="7796c-113">Prima di chiamare di nuovo l'oggetto, è necessario eseguire l'unmarshalling per creare un proxy per il thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="7796c-113">Before calling the object again, it must unmarshal to create a proxy for the calling thread.</span></span>

<span data-ttu-id="7796c-114">Potrebbe essere più efficiente memorizzare nella cache questi proxy per thread mantenendo una mappa dall'ID thread a un puntatore proxy.</span><span class="sxs-lookup"><span data-stu-id="7796c-114">It might be more efficient to cache these per-thread proxies by keeping a map from the thread ID to a proxy pointer.</span></span> <span data-ttu-id="7796c-115">Questa mappa si espande quando si utilizzano nuovi thread nel processo.</span><span class="sxs-lookup"><span data-stu-id="7796c-115">This map expands as new threads are used in the process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7796c-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7796c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7796c-117">Concetti relativi al dispenser di risorse COM+</span><span class="sxs-lookup"><span data-stu-id="7796c-117">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



