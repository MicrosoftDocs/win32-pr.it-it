---
description: Imposta il numero di livelli temporali video per un codificatore video.
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: Proprietà CODECAPI_AVEncVideoTemporalLayerCount (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85402b57c0eaf5c5fe61290eabdfd3e34a64ca4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484116"
---
# <a name="codecapi_avencvideotemporallayercount-property"></a><span data-ttu-id="5407f-103">Proprietà AVEncVideoTemporalLayerCount di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="5407f-103">CODECAPI\_AVEncVideoTemporalLayerCount property</span></span>

<span data-ttu-id="5407f-104">Imposta il numero di livelli temporali video per un codificatore video.</span><span class="sxs-lookup"><span data-stu-id="5407f-104">Sets the video temporal layer count for a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="5407f-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5407f-105">Data type</span></span>

<span data-ttu-id="5407f-106">**ULONG (VT \_ UI4)**</span><span class="sxs-lookup"><span data-stu-id="5407f-106">**ULONG (VT\_UI4)**</span></span>

## <a name="property-guid"></a><span data-ttu-id="5407f-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="5407f-107">Property GUID</span></span>

<span data-ttu-id="5407f-108">**Codecapis \_ AVEncVideoTemporalLayerCount**</span><span class="sxs-lookup"><span data-stu-id="5407f-108">**CODECAPI\_AVEncVideoTemporalLayerCount**</span></span>

## <a name="remarks"></a><span data-ttu-id="5407f-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="5407f-109">Remarks</span></span>

<span data-ttu-id="5407f-110">Questa proprietà viene usata anche con [codificatori della fotocamera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="5407f-110">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="5407f-111">Codecapis \_ AVEncVideoTemporalLayerCount, [codecapites \_ AVENCVIDEOUSAGE](codecapi-avencvideousage.md)e [codecapi \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) sono proprietà del codificatore statiche.</span><span class="sxs-lookup"><span data-stu-id="5407f-111">CODECAPI\_AVEncVideoTemporalLayerCount, [CODECAPI\_AVEncVideoUsage](codecapi-avencvideousage.md), and [CODECAPI\_AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) are static encoder properties.</span></span> <span data-ttu-id="5407f-112">Una volta impostate, queste diverranno effettive solo dopo la chiamata di un tipo di supporto set sul pin di output della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="5407f-112">Once set, these will only take effect after a set media type is called on the camera s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="5407f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5407f-113">Requirements</span></span>



| <span data-ttu-id="5407f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5407f-114">Requirement</span></span> | <span data-ttu-id="5407f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5407f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5407f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5407f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5407f-117">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5407f-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="5407f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5407f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5407f-119">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="5407f-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5407f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5407f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5407f-121"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="5407f-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5407f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5407f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5407f-123">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5407f-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

