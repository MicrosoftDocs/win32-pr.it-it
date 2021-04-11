---
description: I cloud vengono usati dalle infrastrutture di raggruppamento e Graphing peer.
ms.assetid: 01327211-0461-4922-925e-67bebe3e6158
title: Cloud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743d668387c78b3c22e49e98585494a36506cc74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131695"
---
# <a name="clouds"></a><span data-ttu-id="7a837-103">Cloud</span><span class="sxs-lookup"><span data-stu-id="7a837-103">Clouds</span></span>

<span data-ttu-id="7a837-104">I cloud vengono usati dalle infrastrutture di [raggruppamento](grouping-api.md) e [Graphing](graphing-api.md) peer.</span><span class="sxs-lookup"><span data-stu-id="7a837-104">Clouds are used by the Peer [Grouping](grouping-api.md) and [Graphing](graphing-api.md) Infrastructures.</span></span> <span data-ttu-id="7a837-105">Il [protocollo PNRP (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) identifica un cloud come un set di peer che possono comunicare nello stesso ambito IPv6.</span><span class="sxs-lookup"><span data-stu-id="7a837-105">The [Peer Name Resolution Protocol (PNRP)](pnrp-namespace-provider-api.md) identifies a cloud as a set of peers that can communicate within the same IPv6 scope.</span></span> <span data-ttu-id="7a837-106">I cloud sono strettamente correlati agli ambiti IPv6.</span><span class="sxs-lookup"><span data-stu-id="7a837-106">Clouds are closely related to the IPv6 scopes.</span></span> <span data-ttu-id="7a837-107">L'elenco seguente identifica alcune delle funzionalità cloud univoche:</span><span class="sxs-lookup"><span data-stu-id="7a837-107">The following list identifies some of the unique cloud features:</span></span>

-   <span data-ttu-id="7a837-108">Un cloud è identificato da un nome e i cloud disponibili possono essere enumerati usando [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).</span><span class="sxs-lookup"><span data-stu-id="7a837-108">A cloud is identified by a name, and available clouds can be enumerated by using [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md).</span></span>
-   <span data-ttu-id="7a837-109">Se un computer è connesso a Internet, fa parte di un cloud globale, identificato dalla stringa "globale \_ ".</span><span class="sxs-lookup"><span data-stu-id="7a837-109">If a computer is connected to the Internet, it is part of a global cloud, which is identified by the string "Global\_".</span></span>
-   <span data-ttu-id="7a837-110">Se un computer è connesso a una o più reti locali (LAN), per ogni collegamento sono disponibili singoli cloud.</span><span class="sxs-lookup"><span data-stu-id="7a837-110">If a computer is connected to one or more local area networks (LAN), individual clouds are available for each link.</span></span>
-   <span data-ttu-id="7a837-111">Un computer può essere connesso a molte reti con più schede di rete o tramite una rete privata virtuale (VPN), il che significa che un computer con un'interfaccia può essere visibile in molti cloud.</span><span class="sxs-lookup"><span data-stu-id="7a837-111">One computer can be connected to many networks by having multiple network adapters or by using a virtual private network (VPN), which means that a computer with one interface can be visible in many clouds.</span></span>
-   <span data-ttu-id="7a837-112">È possibile usare PNRP per registrare e risolvere i nomi di peer in un cloud specifico.</span><span class="sxs-lookup"><span data-stu-id="7a837-112">You can use PNRP to register and resolve peer names in a specific cloud.</span></span>

 

 



