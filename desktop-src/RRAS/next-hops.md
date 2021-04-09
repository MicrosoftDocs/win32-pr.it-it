---
title: Hop successivi
description: Alle route sono associati uno o più hop successivi.
ms.assetid: 90e5a79b-4fee-479c-9888-fcb3b6d38c1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fcbc13ea7ad7c886ebd9f6f945f7cf6d6efe6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044193"
---
# <a name="next-hops"></a><span data-ttu-id="53f08-103">Hop successivi</span><span class="sxs-lookup"><span data-stu-id="53f08-103">Next Hops</span></span>

<span data-ttu-id="53f08-104">Alle route sono associati uno o più hop successivi.</span><span class="sxs-lookup"><span data-stu-id="53f08-104">Routes have one or more next hops associated with them.</span></span> <span data-ttu-id="53f08-105">Se la destinazione non si trova in una rete connessa direttamente, l'hop successivo è l'indirizzo del router (o rete) successivo nella rete in uscita che può indirizzare i dati alla destinazione in modo ottimale.</span><span class="sxs-lookup"><span data-stu-id="53f08-105">If the destination is not on a directly connected network, the next hop is the address of the next router (or network) on the outgoing network that can best route data to the destination.</span></span> <span data-ttu-id="53f08-106">Il percorso migliore è la route con il costo inferiore, in base ai criteri di routing in uso.</span><span class="sxs-lookup"><span data-stu-id="53f08-106">The best route is the route that has the least cost, based on the routing policy in use.</span></span> <span data-ttu-id="53f08-107">Ogni hop successivo può essere utilizzato per l'invio dei dati nel percorso alla destinazione.</span><span class="sxs-lookup"><span data-stu-id="53f08-107">Each next hop can be used to forward data on the path to the destination.</span></span> <span data-ttu-id="53f08-108">Tutte le route di proprietà di un client condividono un insieme comune di voci di hop successivo aggiunte dal client.</span><span class="sxs-lookup"><span data-stu-id="53f08-108">All routes owned by a client share a common set of next-hop entries that were added by the client.</span></span>

<span data-ttu-id="53f08-109">Ogni hop successivo viene identificato in modo univoco dall'indirizzo dell'hop successivo e dall'indice dell'interfaccia utilizzato per raggiungere l'hop successivo.</span><span class="sxs-lookup"><span data-stu-id="53f08-109">Each next hop is uniquely identified by the address of the next hop and the interface index used to reach the next hop.</span></span>

<span data-ttu-id="53f08-110">Se l'hop successivo non è direttamente connesso, viene contrassegnato come hop successivo "remoto".</span><span class="sxs-lookup"><span data-stu-id="53f08-110">If the next hop itself is not directly connected, it is marked as a "remote" next hop.</span></span> <span data-ttu-id="53f08-111">In questo caso, il server d'esecuzione deve eseguire un'altra ricerca usando l'indirizzo di rete dell'hop successivo.</span><span class="sxs-lookup"><span data-stu-id="53f08-111">In this case, the forwarder must perform another lookup using the next hop's network address.</span></span> <span data-ttu-id="53f08-112">Questa ricerca è necessaria per trovare l'hop successivo "locale" usato per raggiungere l'hop successivo remoto e la destinazione.</span><span class="sxs-lookup"><span data-stu-id="53f08-112">This lookup is necessary to find the "local" next hop used to reach the remote next hop and the destination.</span></span>

<span data-ttu-id="53f08-113">Una voce di hop successivo nella tabella di routing include:</span><span class="sxs-lookup"><span data-stu-id="53f08-113">A next-hop entry in the routing table includes:</span></span>

-   <span data-ttu-id="53f08-114">Indirizzo di rete dell'hop successivo</span><span class="sxs-lookup"><span data-stu-id="53f08-114">The network address of the next hop</span></span>
-   <span data-ttu-id="53f08-115">Proprietario dell'hop successivo</span><span class="sxs-lookup"><span data-stu-id="53f08-115">The owner of the next hop</span></span>
-   <span data-ttu-id="53f08-116">Identificatore dell'interfaccia in uscita.</span><span class="sxs-lookup"><span data-stu-id="53f08-116">The identifier of the outgoing interface</span></span>
-   <span data-ttu-id="53f08-117">Stato dell'hop successivo</span><span class="sxs-lookup"><span data-stu-id="53f08-117">The state of the next hop</span></span>
-   <span data-ttu-id="53f08-118">Flag associati all'hop successivo</span><span class="sxs-lookup"><span data-stu-id="53f08-118">Flags associated with the next hop</span></span>
-   <span data-ttu-id="53f08-119">Informazioni private del proprietario dell'hop successivo</span><span class="sxs-lookup"><span data-stu-id="53f08-119">Information that is private to the owner of the next hop</span></span>
-   <span data-ttu-id="53f08-120">Handle per la destinazione corrispondente all'hop successivo remoto</span><span class="sxs-lookup"><span data-stu-id="53f08-120">A handle to the destination corresponding to the remote next hop</span></span>

 

 




