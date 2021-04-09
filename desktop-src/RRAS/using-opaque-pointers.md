---
title: Utilizzo di puntatori opachi
description: I client spesso devono archiviare informazioni aggiuntive specifiche del client sulle destinazioni.
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9893b3a8b8e8a69ab78f33156efbe872b86d83ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856533"
---
# <a name="using-opaque-pointers"></a><span data-ttu-id="1bd14-103">Utilizzo di puntatori opachi</span><span class="sxs-lookup"><span data-stu-id="1bd14-103">Using Opaque Pointers</span></span>

<span data-ttu-id="1bd14-104">I client spesso devono archiviare informazioni aggiuntive specifiche del client sulle destinazioni.</span><span class="sxs-lookup"><span data-stu-id="1bd14-104">Clients often must store additional, client-specific information about destinations.</span></span> <span data-ttu-id="1bd14-105">Gestione tabelle di routing consente ai client di archiviare queste informazioni in strutture di destinazione nella tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="1bd14-105">The routing table manager enables clients to store this information in destination structures in the routing table.</span></span> <span data-ttu-id="1bd14-106">Le informazioni vengono archiviate e recuperate tramite *puntatori opachi*.</span><span class="sxs-lookup"><span data-stu-id="1bd14-106">The information is stored and retrieved by using *opaque pointers*.</span></span> <span data-ttu-id="1bd14-107">Le informazioni archiviate sono private e accessibili solo al client proprietario del puntatore opaco.</span><span class="sxs-lookup"><span data-stu-id="1bd14-107">The information stored is private, and accessible only to the client that owns the opaque pointer.</span></span>

<span data-ttu-id="1bd14-108">Il gestore del gruppo multicast, ad esempio, mantiene un elenco di voci di invio multicast che dipendono da una determinata destinazione.</span><span class="sxs-lookup"><span data-stu-id="1bd14-108">For example, the multicast group manager keeps a list of multicast forwarding entries that are dependent on a particular destination.</span></span> <span data-ttu-id="1bd14-109">Il gestore del gruppo multicast utilizza un puntatore opaco in tale destinazione.</span><span class="sxs-lookup"><span data-stu-id="1bd14-109">The multicast group manager uses an opaque pointer in that destination.</span></span> <span data-ttu-id="1bd14-110">In un altro esempio, un protocollo di routing che annuncia una determinata destinazione può contenere informazioni correlate alla propria inserzione di route della destinazione utilizzando un puntatore opaco, anche se non è il proprietario della route migliore.</span><span class="sxs-lookup"><span data-stu-id="1bd14-110">In another example, a routing protocol that advertises a particular destination can keep information related to its own route advertisement of the destination using an opaque pointer, even though it does not own the best route.</span></span>

<span data-ttu-id="1bd14-111">Il numero di puntatori opachi è limitato; questi puntatori vengono allocati ai client in base a una prima, prima di tutto.</span><span class="sxs-lookup"><span data-stu-id="1bd14-111">The number of opaque pointers is limited; these pointers are allocated to clients on a first-come, first-served basis.</span></span> <span data-ttu-id="1bd14-112">L'amministratore del router deve allocare il numero corretto di puntatori durante la configurazione del router; Pertanto, i protocolli di routing e gli altri client devono documentare l'utilizzo di puntatori opachi.</span><span class="sxs-lookup"><span data-stu-id="1bd14-112">The router administrator must allocate the correct number of pointers during the router configuration; therefore, routing protocols and other clients must document their use of opaque pointers.</span></span>

 

 




