---
description: Considerato in genere più semplice da usare per la rete rispetto a una trasmissione all-Route, una trasmissione diretta si limita alla rete locale specificata.
ms.assetid: e2358580-5a65-434d-ba4c-a6b0615bccc3
title: Trasmissione diretta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3a47bd47e9800e1f9c93cffa555b76feb77373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306992"
---
# <a name="directed-broadcast"></a><span data-ttu-id="f3567-103">Trasmissione diretta</span><span class="sxs-lookup"><span data-stu-id="f3567-103">Directed Broadcast</span></span>

<span data-ttu-id="f3567-104">Considerato in genere più semplice da usare per la rete rispetto a una trasmissione all-Route, una trasmissione diretta si limita alla rete locale specificata.</span><span class="sxs-lookup"><span data-stu-id="f3567-104">Generally considered more network friendly than an all-routes broadcast, a directed broadcast limits itself to the local network that you specify.</span></span> <span data-ttu-id="f3567-105">Compilare **sa \_ netnum** con il numero di rete di destinazione e il **\_ nodenum SA** con quelli binari.</span><span class="sxs-lookup"><span data-stu-id="f3567-105">Fill **sa\_netnum** with the target network number and **sa\_nodenum** with binary ones.</span></span> <span data-ttu-id="f3567-106">I router inoltrano questa richiesta alla rete di destinazione in cui diventerà una trasmissione locale.</span><span class="sxs-lookup"><span data-stu-id="f3567-106">Routers forward this request to the destination network where it becomes a local broadcast.</span></span> <span data-ttu-id="f3567-107">Le reti intermedie non visualizzano questo pacchetto come broadcast.</span><span class="sxs-lookup"><span data-stu-id="f3567-107">Intermediate networks do not see this packet as a broadcast.</span></span>

 

 



