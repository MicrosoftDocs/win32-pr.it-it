---
description: Questa proprietà esegue una query sul decodificatore per ottenere la frequenza massima dei frame completa supportata dal decodificatore. Il tipo di dati di questa proprietà è una \_ struttura am QueryRate.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: Proprietà AM_RATE_QueryFullFrameRate (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2c99564caa09253198b101a3e2467ec88c7e34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330331"
---
# <a name="am_rate_queryfullframerate-property"></a><span data-ttu-id="a9bfc-104">\_Proprietà rate \_ QueryFullFrameRate</span><span class="sxs-lookup"><span data-stu-id="a9bfc-104">AM\_RATE\_QueryFullFrameRate Property</span></span>

<span data-ttu-id="a9bfc-105">Questa proprietà esegue una query sul decodificatore per ottenere la frequenza massima dei frame completa supportata dal decodificatore.</span><span class="sxs-lookup"><span data-stu-id="a9bfc-105">This property queries the decoder for the maximum full-frame rate that the decoder supports.</span></span> <span data-ttu-id="a9bfc-106">Il tipo di dati di questa proprietà è una struttura **am \_ QueryRate** .</span><span class="sxs-lookup"><span data-stu-id="a9bfc-106">The data type for this property is an **AM\_QueryRate** structure.</span></span>

<span data-ttu-id="a9bfc-107">Questa proprietà è definita per la versione 1,1 di questo set di proprietà. vedere [**am \_ rate \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="a9bfc-107">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



|                   |                                       |
|-------------------|---------------------------------------|
| <span data-ttu-id="a9bfc-108">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="a9bfc-108">Property Set GUID</span></span> | <span data-ttu-id="a9bfc-109">\_TSRateChange KSPROPSETID \_</span><span class="sxs-lookup"><span data-stu-id="a9bfc-109">AM\_KSPROPSETID\_TSRateChange</span></span>         |
| <span data-ttu-id="a9bfc-110">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="a9bfc-110">Property ID</span></span>       | <span data-ttu-id="a9bfc-111">\_Proprietà rate \_ QueryFullFrameRate</span><span class="sxs-lookup"><span data-stu-id="a9bfc-111">AM\_RATE\_QueryFullFrameRate Property</span></span> |
| <span data-ttu-id="a9bfc-112">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a9bfc-112">Data Type</span></span>         | [<span data-ttu-id="a9bfc-113">**AM \_ QueryRate**</span><span class="sxs-lookup"><span data-stu-id="a9bfc-113">**AM\_QueryRate**</span></span>](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a><span data-ttu-id="a9bfc-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9bfc-114">Remarks</span></span>

<span data-ttu-id="a9bfc-115">Se la velocità di riproduzione supera la frequenza massima del decodificatore, il filtro di origine invia gruppi di campioni continui separati da discontinuità.</span><span class="sxs-lookup"><span data-stu-id="a9bfc-115">If the playback rate exceeds the decoder's maximum rate, the source filter sends groups of continuous samples separated by discontinuities.</span></span> <span data-ttu-id="a9bfc-116">Il timestamp passa attraverso le discontinuità.</span><span class="sxs-lookup"><span data-stu-id="a9bfc-116">The time stamps jump across the discontinuities.</span></span> <span data-ttu-id="a9bfc-117">Il filtro di origine può eseguire questa operazione anche se la velocità di riproduzione rientra nella frequenza massima del decodificatore, perché potrebbero esserci altri fattori, ad esempio l'i/o del disco, che limitano la velocità di riproduzione completa.</span><span class="sxs-lookup"><span data-stu-id="a9bfc-117">The source filter might do this even if the playback rate is within the decoder's maximum rate, because there may be other factors, such as disk IO, that limit the full playback rate.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9bfc-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9bfc-118">Requirements</span></span>



| <span data-ttu-id="a9bfc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9bfc-119">Requirement</span></span> | <span data-ttu-id="a9bfc-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a9bfc-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9bfc-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9bfc-121">Header</span></span><br/> | <dl> <span data-ttu-id="a9bfc-122"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9bfc-122"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9bfc-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9bfc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9bfc-124">**Set di proprietà di modifica della frequenza**</span><span class="sxs-lookup"><span data-stu-id="a9bfc-124">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




