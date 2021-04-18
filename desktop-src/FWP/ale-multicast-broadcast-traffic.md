---
title: Traffico di broadcast/multicast ALE
description: Viene eseguito il mapping di tutto il traffico in ingresso multicast e broadcast a livello di applicazione (ALE) a un flusso di ALE globale.
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30b56a6e2a27a209baf66d34948b704ae321644
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329708"
---
# <a name="ale-multicastbroadcast-traffic"></a><span data-ttu-id="519ed-103">Traffico di broadcast/multicast ALE</span><span class="sxs-lookup"><span data-stu-id="519ed-103">ALE Multicast/Broadcast Traffic</span></span>

<span data-ttu-id="519ed-104">Viene eseguito il mapping di tutto il traffico in ingresso multicast e broadcast a livello di applicazione (ALE) a un [flusso di ale](ale-stateful-filtering.md)globale.</span><span class="sxs-lookup"><span data-stu-id="519ed-104">All inbound multicast and broadcast traffic at the Application Layer Enforcement (ALE) layers is mapped to one global [ALE flow](ale-stateful-filtering.md).</span></span> <span data-ttu-id="519ed-105">Il traffico di risposta per i pacchetti multicast e broadcast in ingresso è Classificato al livello [**FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) e vengono creati flussi ale distinti per ogni risposta.</span><span class="sxs-lookup"><span data-stu-id="519ed-105">Response traffic for inbound multicast and broadcast packets is classified at the [**FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer and separate ALE flows are created for each response.</span></span>

<span data-ttu-id="519ed-106">Il traffico multicast e broadcast in uscita a livello di ALE crea un flusso ALE di 4 secondi.</span><span class="sxs-lookup"><span data-stu-id="519ed-106">Outbound multicast and broadcast traffic at the ALE layers creates a 4-second ALE flow.</span></span> <span data-ttu-id="519ed-107">Per impostazione predefinita, l'autorizzazione di un pacchetto multicast o broadcast in uscita consentirà il traffico in ingresso, sia unicast, multicast o broadcast, da qualsiasi indirizzo remoto per un massimo di 4 secondi.</span><span class="sxs-lookup"><span data-stu-id="519ed-107">By default, the authorization of an outbound multicast or broadcast ALE packet will permit inbound traffic, whether unicast, multicast, or broadcast, from any remote address for up to 4 seconds.</span></span> <span data-ttu-id="519ed-108">Questo flusso di ALE può essere aggiornato o mantenuto attivo solo dal traffico in uscita successivo corrispondente al flusso ALE.</span><span class="sxs-lookup"><span data-stu-id="519ed-108">Such an ALE flow can only be refreshed or kept alive by subsequent outbound traffic that matches the ALE flow.</span></span>

> [!Note]  
> <span data-ttu-id="519ed-109">Il ciclo di vita di 4 secondi viene specificato dalle opzioni di callout FWPM del callout predefinite di [**\_ \_ \_ \_ auth \_ Connect \_ Layer \_ V {4 \| 6}**](built-in-callout-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="519ed-109">The 4-second lifetime is specified by the built-in callout [**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V{4\|6}**](built-in-callout-identifiers.md).</span></span> <span data-ttu-id="519ed-110">Per modificare la durata predefinita di 4 secondi, aggiungere un filtro che faccia riferimento **alle \_ Opzioni del set di callout FWPM autenticazione di \_ \_ \_ \_ \_ livello \_ V {4 \| 6}** callout.</span><span class="sxs-lookup"><span data-stu-id="519ed-110">To alter the 4-second default lifetime, add a filter that references the **FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V{4\|6}** callout.</span></span> <span data-ttu-id="519ed-111">Per ulteriori informazioni, vedere [personalizzazione del flusso di ale](ale-flow-customization.md) .</span><span class="sxs-lookup"><span data-stu-id="519ed-111">See [ALE Flow Customization](ale-flow-customization.md) for more information.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="519ed-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="519ed-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="519ed-113">Application Layer Enforcement (ALE)</span><span class="sxs-lookup"><span data-stu-id="519ed-113">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="519ed-114">Livelli ALE</span><span class="sxs-lookup"><span data-stu-id="519ed-114">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="519ed-115">Filtro con stato ALE</span><span class="sxs-lookup"><span data-stu-id="519ed-115">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="519ed-116">Riautorizzazione ALE</span><span class="sxs-lookup"><span data-stu-id="519ed-116">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="519ed-117">Personalizzazione del flusso di ALE</span><span class="sxs-lookup"><span data-stu-id="519ed-117">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> </dl>

 

 




