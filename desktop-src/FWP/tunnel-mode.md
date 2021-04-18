---
title: Modalità tunnel
description: Lo scenario dei criteri IPsec in modalità tunnel viene usato per applicare la protezione in modalità tunnel IPsec per tutto il traffico corrispondente tra due endpoint del tunnel.
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75fdecb7f959a2f95aae2649a6e3f8f94def9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331303"
---
# <a name="tunnel-mode"></a><span data-ttu-id="dc51c-103">Modalità tunnel</span><span class="sxs-lookup"><span data-stu-id="dc51c-103">Tunnel Mode</span></span>

<span data-ttu-id="dc51c-104">Lo scenario dei criteri IPsec in modalità tunnel viene usato per applicare la protezione in modalità tunnel IPsec per tutto il traffico corrispondente tra due endpoint del tunnel.</span><span class="sxs-lookup"><span data-stu-id="dc51c-104">The Tunnel Mode IPsec policy scenario is used to apply IPsec tunnel mode protection for all matching traffic between two tunnel endpoints.</span></span>

<span data-ttu-id="dc51c-105">Questo scenario di criteri viene in genere usato per proteggere il traffico tra più subnet dell'ufficio, quando viene inviato tra i gateway corrispondenti in Internet.</span><span class="sxs-lookup"><span data-stu-id="dc51c-105">This policy scenario is typically used to protect traffic between multiple branch-office subnets, when it gets forwarded between the corresponding gateways on the Internet.</span></span> <span data-ttu-id="dc51c-106">Può anche essere usato per proteggere la comunicazione end-to-end tra due computer host, detti anche tunnel da punto a punto.</span><span class="sxs-lookup"><span data-stu-id="dc51c-106">It can also be used to secure end-to-end communication between two host machines, also referred to as point-to-point tunnels.</span></span>

<span data-ttu-id="dc51c-107">Per implementare i criteri in modalità tunnel utilizzando Windows Filtering Platform (WFP), chiamare la funzione [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) che crea un'istanza dei filtri in modalità tunnel appropriati ai livelli appropriati per conto del chiamante.</span><span class="sxs-lookup"><span data-stu-id="dc51c-107">To implement Tunnel Mode policy using the Windows Filtering Platform (WFP), call the [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) function that instantiates the appropriate tunnel mode filters at the appropriate layers on behalf of the caller.</span></span> <span data-ttu-id="dc51c-108">Il chiamante deve specificare la modalità principale, i contesti del provider in modalità rapida e le condizioni di filtro che descrivono il traffico che deve essere protetto all'interno del tunnel.</span><span class="sxs-lookup"><span data-stu-id="dc51c-108">The caller needs to specify the Main Mode, Quick Mode provider contexts, and the filter conditions describing the traffic that should be secured inside the tunnel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc51c-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc51c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc51c-110">Codice di esempio: uso della modalità tunnel</span><span class="sxs-lookup"><span data-stu-id="dc51c-110">Sample code: Using Tunnel Mode</span></span>](using-tunnel-mode.md)
</dt> <dt>

[<span data-ttu-id="dc51c-111">**Filtraggio degli identificatori del livello**</span><span class="sxs-lookup"><span data-stu-id="dc51c-111">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




