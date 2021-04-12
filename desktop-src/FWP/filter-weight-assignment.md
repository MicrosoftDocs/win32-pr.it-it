---
title: Assegnazione di pesi dei filtri
description: A ogni filtro della piattaforma filtro Windows è associato un peso, che viene utilizzato durante l'arbitraggio dei filtri.
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c77982258bb9c8ef14e22b20e28b6a3039456ae
ms.sourcegitcommit: 013de6f5280f28a9b04c3cce9387e629b07d70fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/26/2020
ms.locfileid: "104398774"
---
# <a name="filter-weight-assignment"></a><span data-ttu-id="bc2f3-103">Assegnazione di pesi dei filtri</span><span class="sxs-lookup"><span data-stu-id="bc2f3-103">Filter Weight Assignment</span></span>

<span data-ttu-id="bc2f3-104">A ogni filtro della piattaforma filtro Windows è associato un peso, che viene utilizzato durante l' [arbitraggio dei filtri](filter-arbitration.md).</span><span class="sxs-lookup"><span data-stu-id="bc2f3-104">Every filter in the Windows Filtering Platform (WFP) has an associated weight, which is used during [filter arbitration](filter-arbitration.md).</span></span>

<span data-ttu-id="bc2f3-105">Il peso del filtro utilizzato dal motore di filtro di base (BFE) è di tipo [**FWP \_ UInt64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="bc2f3-105">The filter weight used by the Base Filtering Engine (BFE) is of type [**FWP\_UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="bc2f3-106">Nei chiamanti sono disponibili tre opzioni per l'aggiunta di filtri.</span><span class="sxs-lookup"><span data-stu-id="bc2f3-106">Callers have three options when adding filters.</span></span>

-   <span data-ttu-id="bc2f3-107">Impostare il peso su un [**FWP \_ UInt64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="bc2f3-107">Set the weight to an [**FWP\_UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="bc2f3-108">BFE usa il peso fornito così com'è.</span><span class="sxs-lookup"><span data-stu-id="bc2f3-108">BFE uses the supplied weight as is.</span></span>
-   <span data-ttu-id="bc2f3-109">Impostare Weight su [**FWP \_ empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="bc2f3-109">Set the weight to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="bc2f3-110">BFE genera automaticamente un peso compreso nell'intervallo \[ 0, 2 ⁶ ⁰).</span><span class="sxs-lookup"><span data-stu-id="bc2f3-110">BFE automatically generates a weight in the range \[0, 2⁶⁰).</span></span>
-   <span data-ttu-id="bc2f3-111">Impostare il peso su un [**\_ Uint8 FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) nell'intervallo compreso tra \[ 0 e 15 \] .</span><span class="sxs-lookup"><span data-stu-id="bc2f3-111">Set the weight to an [**FWP\_UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) in the range \[0, 15\].</span></span> <span data-ttu-id="bc2f3-112">BFE usa il peso fornito come identificatore dell'intervallo di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="bc2f3-112">BFE uses the supplied weight as a weight range identifier.</span></span>

    <span data-ttu-id="bc2f3-113">BFE genera automaticamente il 60 bit di ordine inferiore (esattamente come se il peso fosse stato impostato su [**FWP \_ vuoto**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)), quindi usa il valore fornito per impostare i 4 bit più significativi.</span><span class="sxs-lookup"><span data-stu-id="bc2f3-113">BFE automatically generates the low-order 60 bits (exactly as if the weight had been set to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)), and then uses the supplied value to set the 4 high-order bits.</span></span> <span data-ttu-id="bc2f3-114">Ciò consente ai chiamanti di dividere manualmente lo spazio del peso in 16 intervalli, pur continuando a utilizzare la ponderazione automatica in un intervallo.</span><span class="sxs-lookup"><span data-stu-id="bc2f3-114">This allows callers to manually divide the weight space into 16 ranges, while still using automatic weighting within a range.</span></span>

> [!Note]  
> <span data-ttu-id="bc2f3-115">Quando due o più callout sono registrati nello stesso sottolivello, possono verificarsi problemi quando lo stesso peso viene assegnato ai filtri.</span><span class="sxs-lookup"><span data-stu-id="bc2f3-115">When two or more callouts are registered at the same sublayer, problems may occur when the same weight is assigned to the filters.</span></span> <span data-ttu-id="bc2f3-116">Questo problema può essere impedito facendo in modo che i callout creino il proprio sottolivello usando [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).</span><span class="sxs-lookup"><span data-stu-id="bc2f3-116">This issue can be prevented by having callouts create their own sublayer by using [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bc2f3-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc2f3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc2f3-118">**Identificatori di peso del filtro**</span><span class="sxs-lookup"><span data-stu-id="bc2f3-118">**Filter Weight Identifiers**</span></span>](filter-weight-identifiers.md)
</dt> </dl>

 

 




