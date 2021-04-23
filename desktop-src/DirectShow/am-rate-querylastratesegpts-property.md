---
description: Questa proprietà esegue una query sul decodificatore per l'ora di inizio della modifica della frequenza accodata più di recente, indipendentemente dalla posizione nella coda di modifica della frequenza.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: AM_RATE_QueryLastRateSegPTS proprietà (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c6e3e00985ba6e714bf48d349fd5af5c9593b9
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910269"
---
# <a name="am_rate_querylastratesegpts-property"></a><span data-ttu-id="661f0-103">Proprietà AM \_ RATE \_ QueryLastRateSegPTS</span><span class="sxs-lookup"><span data-stu-id="661f0-103">AM\_RATE\_QueryLastRateSegPTS Property</span></span>

<span data-ttu-id="661f0-104">Questa proprietà esegue una query sul decodificatore per l'ora di inizio della modifica della frequenza accodata più di recente, indipendentemente dalla posizione nella coda di modifica della frequenza.</span><span class="sxs-lookup"><span data-stu-id="661f0-104">This property queries the decoder for the start time of the rate change that was queued most recently, regardless of its position in the rate-change queue.</span></span>

<span data-ttu-id="661f0-105">Questa proprietà è definita per la versione 1.1 di questo set di proprietà. vedere [**AM \_ RATE \_ UseRateVersion.**](am-rate-userateversion-property.md)</span><span class="sxs-lookup"><span data-stu-id="661f0-105">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



| <span data-ttu-id="661f0-106">Label</span><span class="sxs-lookup"><span data-stu-id="661f0-106">Label</span></span> | <span data-ttu-id="661f0-107">Valore</span><span class="sxs-lookup"><span data-stu-id="661f0-107">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="661f0-108">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="661f0-108">Property Set GUID</span></span> | <span data-ttu-id="661f0-109">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="661f0-109">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="661f0-110">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="661f0-110">Property ID</span></span>       | <span data-ttu-id="661f0-111">AM \_ RATE \_ QueryLastRateSegPTS</span><span class="sxs-lookup"><span data-stu-id="661f0-111">AM\_RATE\_QueryLastRateSegPTS</span></span> |
| <span data-ttu-id="661f0-112">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="661f0-112">Data Type</span></span>         | <span data-ttu-id="661f0-113">**TEMPO DI \_ RIFERIMENTO**</span><span class="sxs-lookup"><span data-stu-id="661f0-113">**REFERENCE\_TIME**</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="661f0-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="661f0-114">Remarks</span></span>

<span data-ttu-id="661f0-115">Il filtro di origine può usare questa proprietà per sincronizzare le modifiche della frequenza in diversi flussi audio e video.</span><span class="sxs-lookup"><span data-stu-id="661f0-115">The source filter can use this property to synchronize rate changes across several audio and video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="661f0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="661f0-116">Requirements</span></span>



| <span data-ttu-id="661f0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="661f0-117">Requirement</span></span> | <span data-ttu-id="661f0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="661f0-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="661f0-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="661f0-119">Header</span></span><br/> | <dl> <span data-ttu-id="661f0-120"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="661f0-120"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="661f0-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="661f0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="661f0-122">**Rate Change Property Set**</span><span class="sxs-lookup"><span data-stu-id="661f0-122">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




