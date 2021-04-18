---
description: Questa proprietà esegue una query sul decodificatore per l'ora di inizio della modifica della frequenza accodata più di recente, indipendentemente dalla posizione nella coda di cambio di frequenza.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: Proprietà AM_RATE_QueryLastRateSegPTS (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 024ac26d8307dc9b8ff8e16603dfcc61b0704390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330329"
---
# <a name="am_rate_querylastratesegpts-property"></a><span data-ttu-id="33ec2-103">\_Proprietà rate \_ QueryLastRateSegPTS</span><span class="sxs-lookup"><span data-stu-id="33ec2-103">AM\_RATE\_QueryLastRateSegPTS Property</span></span>

<span data-ttu-id="33ec2-104">Questa proprietà esegue una query sul decodificatore per l'ora di inizio della modifica della frequenza accodata più di recente, indipendentemente dalla posizione nella coda di cambio di frequenza.</span><span class="sxs-lookup"><span data-stu-id="33ec2-104">This property queries the decoder for the start time of the rate change that was queued most recently, regardless of its position in the rate-change queue.</span></span>

<span data-ttu-id="33ec2-105">Questa proprietà è definita per la versione 1,1 di questo set di proprietà. vedere [**am \_ rate \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="33ec2-105">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="33ec2-106">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="33ec2-106">Property Set GUID</span></span> | <span data-ttu-id="33ec2-107">\_TSRateChange KSPROPSETID \_</span><span class="sxs-lookup"><span data-stu-id="33ec2-107">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="33ec2-108">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="33ec2-108">Property ID</span></span>       | <span data-ttu-id="33ec2-109">\_Frequenza \_ QueryLastRateSegPTS</span><span class="sxs-lookup"><span data-stu-id="33ec2-109">AM\_RATE\_QueryLastRateSegPTS</span></span> |
| <span data-ttu-id="33ec2-110">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="33ec2-110">Data Type</span></span>         | <span data-ttu-id="33ec2-111">**\_ora riferimento**</span><span class="sxs-lookup"><span data-stu-id="33ec2-111">**REFERENCE\_TIME**</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="33ec2-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="33ec2-112">Remarks</span></span>

<span data-ttu-id="33ec2-113">Il filtro di origine può usare questa proprietà per sincronizzare le modifiche di frequenza tra diversi flussi audio e video.</span><span class="sxs-lookup"><span data-stu-id="33ec2-113">The source filter can use this property to synchronize rate changes across several audio and video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="33ec2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33ec2-114">Requirements</span></span>



| <span data-ttu-id="33ec2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="33ec2-115">Requirement</span></span> | <span data-ttu-id="33ec2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="33ec2-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33ec2-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33ec2-117">Header</span></span><br/> | <dl> <span data-ttu-id="33ec2-118"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="33ec2-118"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33ec2-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33ec2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33ec2-120">**Set di proprietà di modifica della frequenza**</span><span class="sxs-lookup"><span data-stu-id="33ec2-120">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




