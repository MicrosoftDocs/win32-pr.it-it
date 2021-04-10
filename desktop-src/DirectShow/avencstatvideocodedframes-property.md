---
description: Restituisce il numero di fotogrammi video codificati.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Proprietà AVEncStatVideoCodedFrames (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aed3ed0a06003807a6bd0db90b8978282042daf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124806"
---
# <a name="avencstatvideocodedframes-property"></a><span data-ttu-id="6f414-103">Proprietà AVEncStatVideoCodedFrames</span><span class="sxs-lookup"><span data-stu-id="6f414-103">AVEncStatVideoCodedFrames property</span></span>

<span data-ttu-id="6f414-104">Restituisce il numero di fotogrammi video codificati.</span><span class="sxs-lookup"><span data-stu-id="6f414-104">Returns the number of video frames that were encoded.</span></span>

<span data-ttu-id="6f414-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f414-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="6f414-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6f414-106">Data type</span></span>

<span data-ttu-id="6f414-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="6f414-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6f414-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="6f414-108">Property GUID</span></span>

<span data-ttu-id="6f414-109">**Codecapis \_ AVEncStatVideoCodedFrames**</span><span class="sxs-lookup"><span data-stu-id="6f414-109">**CODECAPI\_AVEncStatVideoCodedFrames**</span></span>

## <a name="remarks"></a><span data-ttu-id="6f414-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f414-110">Remarks</span></span>

<span data-ttu-id="6f414-111">Questa proprietà è disponibile al termine della codifica.</span><span class="sxs-lookup"><span data-stu-id="6f414-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="6f414-112">Il valore di questa proprietà è uguale alla proprietà [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) meno il numero di frame eliminati.</span><span class="sxs-lookup"><span data-stu-id="6f414-112">The value of this property is equal to the [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) property minus the number of dropped frames.</span></span> <span data-ttu-id="6f414-113">Il codificatore potrebbe rilasciare frame per rimanere entro i vincoli di velocità in bit specificati.</span><span class="sxs-lookup"><span data-stu-id="6f414-113">The encoder might drop frames to stay within the specified bit rate constraints.</span></span> <span data-ttu-id="6f414-114">Potrebbe inoltre rilasciare frame alla fine del flusso (vedere la proprietà [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="6f414-114">It might also drop frames at the end of the stream (see [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) property).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f414-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f414-115">Requirements</span></span>



| <span data-ttu-id="6f414-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f414-116">Requirement</span></span> | <span data-ttu-id="6f414-117">Valore</span><span class="sxs-lookup"><span data-stu-id="6f414-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f414-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f414-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6f414-119">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="6f414-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="6f414-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f414-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6f414-121">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6f414-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6f414-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f414-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f414-123"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f414-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f414-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f414-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f414-125">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="6f414-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="6f414-126">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="6f414-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




