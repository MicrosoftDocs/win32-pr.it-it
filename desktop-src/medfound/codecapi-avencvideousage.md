---
description: Imposta l'utilizzo del video per un codificatore video.
ms.assetid: 2A6941A3-CCA0-467C-AC8A-DADC2CD1D405
title: Proprietà CODECAPI_AVEncVideoUsage (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27568412613702846e99d0ca556cc59cdc4fc77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305482"
---
# <a name="codecapi_avencvideousage-property"></a><span data-ttu-id="0cb3a-103">Proprietà AVEncVideoUsage di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="0cb3a-103">CODECAPI\_AVEncVideoUsage property</span></span>

<span data-ttu-id="0cb3a-104">Imposta l'utilizzo del video per un codificatore video.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-104">Sets the video usage for a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="0cb3a-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0cb3a-105">Data type</span></span>

<span data-ttu-id="0cb3a-106">**ULONG (VT \_ UI4)**</span><span class="sxs-lookup"><span data-stu-id="0cb3a-106">**ULONG (VT\_UI4)**</span></span>

## <a name="property-guid"></a><span data-ttu-id="0cb3a-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="0cb3a-107">Property GUID</span></span>

<span data-ttu-id="0cb3a-108">**Codecapis \_ AVEncVideoUsage**</span><span class="sxs-lookup"><span data-stu-id="0cb3a-108">**CODECAPI\_AVEncVideoUsage**</span></span>

## <a name="remarks"></a><span data-ttu-id="0cb3a-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="0cb3a-109">Remarks</span></span>

<span data-ttu-id="0cb3a-110">Questa proprietà viene usata anche con [codificatori della fotocamera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="0cb3a-110">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="0cb3a-111">[CODEcapi \_ AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md), CODEcapit \_ AVEncVideoUsage e [codecapi \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) sono proprietà del codificatore statiche.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-111">[CODECAPI\_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md), CODECAPI\_AVEncVideoUsage, and [CODECAPI\_AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) are static encoder properties.</span></span> <span data-ttu-id="0cb3a-112">Una volta impostate, queste diverranno effettive solo dopo la chiamata di un tipo di supporto set sul pin di output della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="0cb3a-112">Once set, these will only take effect after a set media type is called on the camera s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb3a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cb3a-113">Requirements</span></span>



| <span data-ttu-id="0cb3a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cb3a-114">Requirement</span></span> | <span data-ttu-id="0cb3a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0cb3a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb3a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cb3a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb3a-117">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0cb3a-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="0cb3a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cb3a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb3a-119">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="0cb3a-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0cb3a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0cb3a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cb3a-121"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cb3a-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cb3a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0cb3a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb3a-123">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0cb3a-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

