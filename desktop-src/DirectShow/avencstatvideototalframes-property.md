---
description: Restituisce il numero di fotogrammi video ricevuti dal codificatore.
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: Proprietà AVEncStatVideoTotalFrames (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76adda51e6d16676a2a957fd16a5aac2a15691e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303874"
---
# <a name="avencstatvideototalframes-property"></a><span data-ttu-id="7d5de-103">Proprietà AVEncStatVideoTotalFrames</span><span class="sxs-lookup"><span data-stu-id="7d5de-103">AVEncStatVideoTotalFrames property</span></span>

<span data-ttu-id="7d5de-104">Restituisce il numero di fotogrammi video ricevuti dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="7d5de-104">Returns the number of video frames that the encoder received.</span></span>

<span data-ttu-id="7d5de-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="7d5de-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="7d5de-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7d5de-106">Data type</span></span>

<span data-ttu-id="7d5de-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="7d5de-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="7d5de-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="7d5de-108">Property GUID</span></span>

<span data-ttu-id="7d5de-109">**Codecapis \_ AVEncStatVideoTotalFrames**</span><span class="sxs-lookup"><span data-stu-id="7d5de-109">**CODECAPI\_AVEncStatVideoTotalFrames**</span></span>

## <a name="remarks"></a><span data-ttu-id="7d5de-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d5de-110">Remarks</span></span>

<span data-ttu-id="7d5de-111">Questa proprietà è disponibile al termine della codifica.</span><span class="sxs-lookup"><span data-stu-id="7d5de-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="7d5de-112">Il valore di questa proprietà è il numero totale di frame inviati al codificatore, inclusi i frame eliminati.</span><span class="sxs-lookup"><span data-stu-id="7d5de-112">The value of this property is the total number of frames sent to the encoder, including frames that were dropped.</span></span> <span data-ttu-id="7d5de-113">Per ottenere il numero di frame codificati, leggere la proprietà [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) .</span><span class="sxs-lookup"><span data-stu-id="7d5de-113">To get the number of encoded frames, read the [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d5de-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d5de-114">Requirements</span></span>



| <span data-ttu-id="7d5de-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d5de-115">Requirement</span></span> | <span data-ttu-id="7d5de-116">Valore</span><span class="sxs-lookup"><span data-stu-id="7d5de-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d5de-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d5de-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7d5de-118">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="7d5de-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7d5de-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d5de-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7d5de-120">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7d5de-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7d5de-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d5de-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d5de-122"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d5de-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d5de-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d5de-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d5de-124">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="7d5de-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="7d5de-125">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="7d5de-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




