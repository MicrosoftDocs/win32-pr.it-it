---
description: Questi flag definiscono le impostazioni del processore video (ProcAmp).
ms.assetid: 60d97b9e-d77c-4e53-94ea-ebd59c2601df
title: Impostazioni ProcAmp (Dxva2api. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0181d7491d948a4ec4219ada4241397b8a721b0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309030"
---
# <a name="procamp-settings"></a><span data-ttu-id="30618-103">Impostazioni ProcAmp</span><span class="sxs-lookup"><span data-stu-id="30618-103">ProcAmp Settings</span></span>

<span data-ttu-id="30618-104">Questi flag definiscono le impostazioni del processore video (ProcAmp).</span><span class="sxs-lookup"><span data-stu-id="30618-104">These flags define video processor (ProcAmp) settings.</span></span>



| <span data-ttu-id="30618-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="30618-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="30618-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30618-106">Description</span></span>           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------|
| <span id="DXVA2_ProcAmp_None"></span><span id="dxva2_procamp_none"></span><span id="DXVA2_PROCAMP_NONE"></span><dl> <span data-ttu-id="30618-107"><dt>**DXVA2 \_ ProcAmp \_ None**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="30618-107"><dt>**DXVA2\_ProcAmp\_None**</dt> <dt>0x0000</dt></span></span> </dl>                         | <span data-ttu-id="30618-108">nessuno</span><span class="sxs-lookup"><span data-stu-id="30618-108">None</span></span><br/>       |
| <span id="DXVA2_ProcAmp_Brightness"></span><span id="dxva2_procamp_brightness"></span><span id="DXVA2_PROCAMP_BRIGHTNESS"></span><dl> <span data-ttu-id="30618-109"><dt>**DXVA2 \_ 0x0001 \_ luminosità ProcAmp**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="30618-109"><dt>**DXVA2\_ProcAmp\_Brightness**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="30618-110">Luminosità</span><span class="sxs-lookup"><span data-stu-id="30618-110">Brightness</span></span><br/> |
| <span id="DXVA2_ProcAmp_Contrast"></span><span id="dxva2_procamp_contrast"></span><span id="DXVA2_PROCAMP_CONTRAST"></span><dl> <span data-ttu-id="30618-111"><dt>**DXVA2 \_ ProcAmp \_ contrasto**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="30618-111"><dt>**DXVA2\_ProcAmp\_Contrast**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="30618-112">Si confronti</span><span class="sxs-lookup"><span data-stu-id="30618-112">Contrast</span></span><br/>   |
| <span id="DXVA2_ProcAmp_Hue"></span><span id="dxva2_procamp_hue"></span><span id="DXVA2_PROCAMP_HUE"></span><dl> <span data-ttu-id="30618-113"><dt>**DXVA2 \_ ProcAmp \_ Hue**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="30618-113"><dt>**DXVA2\_ProcAmp\_Hue**</dt> <dt>0x0004</dt></span></span> </dl>                             | <span data-ttu-id="30618-114">Tonalità</span><span class="sxs-lookup"><span data-stu-id="30618-114">Hue</span></span><br/>        |
| <span id="DXVA2_ProcAmp_Saturation"></span><span id="dxva2_procamp_saturation"></span><span id="DXVA2_PROCAMP_SATURATION"></span><dl> <span data-ttu-id="30618-115"><dt>**DXVA2 \_ 0x0008 \_ saturazione ProcAmp**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="30618-115"><dt>**DXVA2\_ProcAmp\_Saturation**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="30618-116">Saturazione</span><span class="sxs-lookup"><span data-stu-id="30618-116">Saturation</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="30618-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30618-117">Requirements</span></span>



| <span data-ttu-id="30618-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="30618-118">Requirement</span></span> | <span data-ttu-id="30618-119">Valore</span><span class="sxs-lookup"><span data-stu-id="30618-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30618-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30618-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30618-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30618-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="30618-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30618-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30618-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="30618-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30618-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30618-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="30618-125"><dt>Dxva2api. h</dt></span><span class="sxs-lookup"><span data-stu-id="30618-125"><dt>Dxva2api.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30618-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30618-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30618-127">Costanti Media Foundation</span><span class="sxs-lookup"><span data-stu-id="30618-127">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




