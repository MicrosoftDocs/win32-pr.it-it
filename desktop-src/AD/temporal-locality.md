---
title: Località temporale
description: La località temporale è una strategia di prevenzione che riduce la finestra per gli aggiornamenti parziali.
ms.assetid: 8f454087-46cb-4fa6-b83a-65b2393029c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceecff05d031875178b6192e7c633f70e4c91c50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470835"
---
# <a name="temporal-locality"></a><span data-ttu-id="c9f53-103">Località temporale</span><span class="sxs-lookup"><span data-stu-id="c9f53-103">Temporal Locality</span></span>

<span data-ttu-id="c9f53-104">La *località temporale* è una strategia di prevenzione che riduce la finestra per gli aggiornamenti parziali.</span><span class="sxs-lookup"><span data-stu-id="c9f53-104">*Temporal locality* is an avoidance strategy that reduces the window for partial updates.</span></span> <span data-ttu-id="c9f53-105">La replica delle modifiche da una replica di origine specificata continua in ordine crescente di USN.</span><span class="sxs-lookup"><span data-stu-id="c9f53-105">Replication of changes from a given source replica proceeds in ascending USN order.</span></span> <span data-ttu-id="c9f53-106">Le Scritture che si verificano in un periodo di tempo ravvicinato avranno USNs che si avvicinano tra loro e verranno propagate insieme nel tempo.</span><span class="sxs-lookup"><span data-stu-id="c9f53-106">Writes that occur close together in time will have USNs that are "near" each other, and will be propagated close together in time.</span></span> <span data-ttu-id="c9f53-107">Le applicazioni che creano o aggiornano più oggetti correlati devono scrivere gli oggetti più vicini nel tempo possibile.</span><span class="sxs-lookup"><span data-stu-id="c9f53-107">Applications that create or update multiple, related objects should write the objects as close together in time as possible.</span></span> <span data-ttu-id="c9f53-108">Ad esempio, l'applicazione può raccogliere tutti gli input necessari dall'utente e applicarli alla directory quando l'utente fa clic su un pulsante "applica".</span><span class="sxs-lookup"><span data-stu-id="c9f53-108">For example, the application could gather all necessary input from the user and apply it to the directory when the user clicks an "Apply" button.</span></span>

<span data-ttu-id="c9f53-109">La località temporale riduce anche le probabilità di risoluzione dei conflitti introducendo incoerenze intra-Object.</span><span class="sxs-lookup"><span data-stu-id="c9f53-109">Temporal locality also reduces the odds of collision resolution introducing intra-object inconsistencies.</span></span>

 

 




