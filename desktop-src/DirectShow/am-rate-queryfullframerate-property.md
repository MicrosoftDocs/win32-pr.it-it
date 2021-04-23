---
description: Questa proprietà esegue una query sul decodificatore per la frequenza massima dei fotogrammi completi supportati dal decodificatore. Il tipo di dati per questa proprietà è una struttura \_ AM QueryRate.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: AM_RATE_QueryFullFrameRate proprietà (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70bc096e5b68737ca877a037571223d673284dab
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910279"
---
# <a name="am_rate_queryfullframerate-property"></a><span data-ttu-id="6bdc6-104">Am \_ RATE \_ QueryFullFrameRate - proprietà</span><span class="sxs-lookup"><span data-stu-id="6bdc6-104">AM\_RATE\_QueryFullFrameRate Property</span></span>

<span data-ttu-id="6bdc6-105">Questa proprietà esegue una query sul decodificatore per la frequenza massima dei fotogrammi completi supportati dal decodificatore.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-105">This property queries the decoder for the maximum full-frame rate that the decoder supports.</span></span> <span data-ttu-id="6bdc6-106">Il tipo di dati per questa proprietà è una **struttura \_ AM QueryRate.**</span><span class="sxs-lookup"><span data-stu-id="6bdc6-106">The data type for this property is an **AM\_QueryRate** structure.</span></span>

<span data-ttu-id="6bdc6-107">Questa proprietà è definita per la versione 1.1 di questo set di proprietà. vedere [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="6bdc6-107">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



| <span data-ttu-id="6bdc6-108">Label</span><span class="sxs-lookup"><span data-stu-id="6bdc6-108">Label</span></span> | <span data-ttu-id="6bdc6-109">Valore</span><span class="sxs-lookup"><span data-stu-id="6bdc6-109">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="6bdc6-110">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="6bdc6-110">Property Set GUID</span></span> | <span data-ttu-id="6bdc6-111">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="6bdc6-111">AM\_KSPROPSETID\_TSRateChange</span></span>         |
| <span data-ttu-id="6bdc6-112">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="6bdc6-112">Property ID</span></span>       | <span data-ttu-id="6bdc6-113">Am \_ RATE \_ QueryFullFrameRate - proprietà</span><span class="sxs-lookup"><span data-stu-id="6bdc6-113">AM\_RATE\_QueryFullFrameRate Property</span></span> |
| <span data-ttu-id="6bdc6-114">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6bdc6-114">Data Type</span></span>         | [<span data-ttu-id="6bdc6-115">**AM \_ QueryRate**</span><span class="sxs-lookup"><span data-stu-id="6bdc6-115">**AM\_QueryRate**</span></span>](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a><span data-ttu-id="6bdc6-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6bdc6-116">Remarks</span></span>

<span data-ttu-id="6bdc6-117">Se la velocità di riproduzione supera la velocità massima del decodificatore, il filtro di origine invia gruppi di campioni continui separati da discontinuità.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-117">If the playback rate exceeds the decoder's maximum rate, the source filter sends groups of continuous samples separated by discontinuities.</span></span> <span data-ttu-id="6bdc6-118">I timestamp passano attraverso le discontinuità.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-118">The time stamps jump across the discontinuities.</span></span> <span data-ttu-id="6bdc6-119">Il filtro di origine potrebbe eseguire questa operazione anche se la velocità di riproduzione rientra nella velocità massima del decodificatore, perché potrebbero esserci altri fattori, ad esempio l'I/O del disco, che limitano la velocità di riproduzione completa.</span><span class="sxs-lookup"><span data-stu-id="6bdc6-119">The source filter might do this even if the playback rate is within the decoder's maximum rate, because there may be other factors, such as disk IO, that limit the full playback rate.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bdc6-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6bdc6-120">Requirements</span></span>



| <span data-ttu-id="6bdc6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bdc6-121">Requirement</span></span> | <span data-ttu-id="6bdc6-122">Valore</span><span class="sxs-lookup"><span data-stu-id="6bdc6-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6bdc6-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6bdc6-123">Header</span></span><br/> | <dl> <span data-ttu-id="6bdc6-124"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="6bdc6-124"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bdc6-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6bdc6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bdc6-126">**Impostare la proprietà Rate Change**</span><span class="sxs-lookup"><span data-stu-id="6bdc6-126">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




