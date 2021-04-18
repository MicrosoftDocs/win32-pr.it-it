---
description: Specifica il parametro di quantizzazione (QP) per la codifica video.
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: Proprietà CODECAPI_AVEncVideoEncodeQP (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec6c746f2f3c902ca416097571abaf5953956cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305490"
---
# <a name="codecapi_avencvideoencodeqp-property"></a><span data-ttu-id="5bea5-103">Proprietà AVEncVideoEncodeQP di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="5bea5-103">CODECAPI\_AVEncVideoEncodeQP property</span></span>

<span data-ttu-id="5bea5-104">Specifica il parametro di quantizzazione (QP) per la codifica video.</span><span class="sxs-lookup"><span data-stu-id="5bea5-104">Specifies the quantization parameter (QP) for video encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="5bea5-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5bea5-105">Data type</span></span>

<span data-ttu-id="5bea5-106">**ULONGLONG** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="5bea5-106">**ULONGLONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5bea5-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="5bea5-107">Property GUID</span></span>

<span data-ttu-id="5bea5-108">**Codecapis \_ AVEncVideoEncodeQP**</span><span class="sxs-lookup"><span data-stu-id="5bea5-108">**CODECAPI\_AVEncVideoEncodeQP**</span></span>

## <a name="property-value"></a><span data-ttu-id="5bea5-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5bea5-109">Property value</span></span>

<span data-ttu-id="5bea5-110">Set di campi a 4 16 bit utilizzato per specificare il frame query al secondo nella codifica Fixed-QP.</span><span class="sxs-lookup"><span data-stu-id="5bea5-110">A set of four 16-bit fields used to specify the frame QPs in fixed-QP encoding.</span></span>

<span data-ttu-id="5bea5-111">I campi sono:</span><span class="sxs-lookup"><span data-stu-id="5bea5-111">The fields are:</span></span>

-   <span data-ttu-id="5bea5-112">BITS 0-15: QP predefinito</span><span class="sxs-lookup"><span data-stu-id="5bea5-112">Bits 0-15: Default QP</span></span>
-   <span data-ttu-id="5bea5-113">BITS 16-31: QP usato per I frame I</span><span class="sxs-lookup"><span data-stu-id="5bea5-113">Bits 16-31: QP used for I frames</span></span>
-   <span data-ttu-id="5bea5-114">BITS 32-47: QP usato per i frame P</span><span class="sxs-lookup"><span data-stu-id="5bea5-114">Bits 32-47: QP used for P frames</span></span>
-   <span data-ttu-id="5bea5-115">BITS 48-63: QP usato per i frame B</span><span class="sxs-lookup"><span data-stu-id="5bea5-115">Bits 48-63: QP used for B frames</span></span>

## <a name="remarks"></a><span data-ttu-id="5bea5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="5bea5-116">Remarks</span></span>

<span data-ttu-id="5bea5-117">Questa proprietà viene usata anche con [codificatori della fotocamera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="5bea5-117">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="5bea5-118">Per garantire un utilizzo coerente tra codificatori diversi, è necessario presupporre che i codificatori considerino solo il QP predefinito e possano ignorare i valori QP per le immagini I/P/B.</span><span class="sxs-lookup"><span data-stu-id="5bea5-118">To insure consistent usage across different encoders, you should assume encoders will only look at the default QP and can ignore QP values for I/P/B pictures.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bea5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bea5-119">Requirements</span></span>



| <span data-ttu-id="5bea5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bea5-120">Requirement</span></span> | <span data-ttu-id="5bea5-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5bea5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5bea5-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bea5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5bea5-123">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5bea5-123">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="5bea5-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bea5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5bea5-125">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="5bea5-125">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5bea5-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5bea5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bea5-127"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bea5-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bea5-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5bea5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bea5-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5bea5-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="5bea5-130">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="5bea5-130">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

