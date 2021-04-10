---
title: Interfaccia (RRAS)
description: Un'interfaccia è una connessione logica a una rete. Ogni interfaccia è identificata da un indice univoco. I protocolli di routing multicast (ad esempio MOSPF) gestiscono tutti i tipi di interfacce in modo analogo.
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd1e3988eac75bd465bf9a9b890f360f850a0d7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103963658"
---
# <a name="interface-rras"></a><span data-ttu-id="b9cc6-105">Interfaccia (RRAS)</span><span class="sxs-lookup"><span data-stu-id="b9cc6-105">Interface (RRAS)</span></span>

<span data-ttu-id="b9cc6-106">Un'interfaccia è una connessione logica a una rete.</span><span class="sxs-lookup"><span data-stu-id="b9cc6-106">An interface is a logical connection to a network.</span></span> <span data-ttu-id="b9cc6-107">Ogni interfaccia è identificata da un indice univoco.</span><span class="sxs-lookup"><span data-stu-id="b9cc6-107">Each interface is identified by a unique index.</span></span> <span data-ttu-id="b9cc6-108">I protocolli di routing multicast (ad esempio MOSPF) gestiscono tutti i tipi di interfacce in modo analogo.</span><span class="sxs-lookup"><span data-stu-id="b9cc6-108">Multicast routing protocols (such as MOSPF) deal with all types of interfaces similarly.</span></span>

<span data-ttu-id="b9cc6-109">Nel caso di un'interfaccia LAN, l'interfaccia corrisponde a un dispositivo fisico reale nel computer (scheda LAN).</span><span class="sxs-lookup"><span data-stu-id="b9cc6-109">In the case of a LAN interface, the interface corresponds to an actual physical device in the computer (the LAN adapter).</span></span> <span data-ttu-id="b9cc6-110">Nel caso di un'interfaccia WAN, viene eseguito il mapping dell'interfaccia a una porta quando viene stabilita una connessione.</span><span class="sxs-lookup"><span data-stu-id="b9cc6-110">In the case of a WAN interface, the interface is mapped to a port when a connection is established.</span></span> <span data-ttu-id="b9cc6-111">Le interfacce WAN possono essere basate sui tunnel e la porta potrebbe essere una porta di rete privata virtuale (VPN).</span><span class="sxs-lookup"><span data-stu-id="b9cc6-111">WAN interfaces can be based on tunnels and the port could be a virtual private network (VPN) port.</span></span>

<span data-ttu-id="b9cc6-112">I sistemi operativi Windows 2000 e versioni successive supportano un'interfaccia "da punto a multipoint".</span><span class="sxs-lookup"><span data-stu-id="b9cc6-112">Windows 2000 and later operating systems support a "point-to-multipoint" interface.</span></span> <span data-ttu-id="b9cc6-113">Questo tipo di interfaccia può essere visualizzato come una raccolta di collegamenti Point-to-Point che condividono un singolo punto di terminazione.</span><span class="sxs-lookup"><span data-stu-id="b9cc6-113">This type of interface can be viewed as a collection of point-to-point links that share a single termination point.</span></span>

<span data-ttu-id="b9cc6-114">Per identificare in modo univoco un collegamento esatto in un'interfaccia Point-to-multipoint, l'API MGM usa l'indirizzo hop successivo dell'ID di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b9cc6-114">To uniquely identify an exact link in a point-to-multipoint interface, the MGM API uses the next hop address of the interface ID.</span></span> <span data-ttu-id="b9cc6-115">Per supportare questa identificazione, l'API MGM usa un ID di interfaccia esteso, che include un indirizzo [hop successivo](next-hop.md) .</span><span class="sxs-lookup"><span data-stu-id="b9cc6-115">To support this identification, the MGM API uses an extended interface ID, which includes a [next hop](next-hop.md) address.</span></span>

 

 




