---
description: Specifica la larghezza e l'altezza del video codificato, se il video è ritagliato.
ms.assetid: d6217250-63ff-4dff-a357-ff4aaa764695
title: Proprietà AVEncVideoEncodeDimension (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f63d0a5c0d1c6af7c20620c315ad25c16eac528
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303754"
---
# <a name="avencvideoencodedimension-property"></a><span data-ttu-id="25022-103">Proprietà AVEncVideoEncodeDimension</span><span class="sxs-lookup"><span data-stu-id="25022-103">AVEncVideoEncodeDimension property</span></span>

<span data-ttu-id="25022-104">Specifica la larghezza e l'altezza del video codificato, se il video è ritagliato.</span><span class="sxs-lookup"><span data-stu-id="25022-104">Specifies the width and height of the encoded video, if the video is cropped.</span></span>

<span data-ttu-id="25022-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="25022-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="25022-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="25022-106">Data type</span></span>

<span data-ttu-id="25022-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="25022-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="25022-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="25022-108">Property GUID</span></span>

<span data-ttu-id="25022-109">**Codecapis \_ AVEncVideoEncodeDimension**</span><span class="sxs-lookup"><span data-stu-id="25022-109">**CODECAPI\_AVEncVideoEncodeDimension**</span></span>

## <a name="property-value"></a><span data-ttu-id="25022-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="25022-110">Property value</span></span>

<span data-ttu-id="25022-111">I 16 bit superiori del valore contengono la larghezza in pixel e i 16 bit inferiori contengono l'altezza in pixel.</span><span class="sxs-lookup"><span data-stu-id="25022-111">The upper 16 bits of the value contain the width in pixels, and the lower 16 bits contain the height in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="25022-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="25022-112">Remarks</span></span>

<span data-ttu-id="25022-113">Le applicazioni possono impostare questa proprietà per ritagliare il video di input.</span><span class="sxs-lookup"><span data-stu-id="25022-113">Applications can set this property to crop the input video.</span></span> <span data-ttu-id="25022-114">La dimensione specificata deve essere minore della dimensione dei fotogrammi video di input.</span><span class="sxs-lookup"><span data-stu-id="25022-114">The specified size must be less than the size of the input video frames.</span></span> <span data-ttu-id="25022-115">Utilizzare la proprietà [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) per specificare gli angoli sinistro e superiore del rettangolo di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="25022-115">Use the [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) property to specify the left and top corners of the clipping rectangle.</span></span>

<span data-ttu-id="25022-116">I codificatori possono restituire questa proprietà come una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="25022-116">Encoders can return this property as a capability.</span></span>

<span data-ttu-id="25022-117">Questa proprietà viene usata anche con [codificatori della fotocamera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="25022-117">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

<span data-ttu-id="25022-118">Per i codificatori della fotocamera UVC 1,5, [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) non è supportato.</span><span class="sxs-lookup"><span data-stu-id="25022-118">For UVC 1.5 camera encoders, [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="25022-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25022-119">Requirements</span></span>



| <span data-ttu-id="25022-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="25022-120">Requirement</span></span> | <span data-ttu-id="25022-121">Valore</span><span class="sxs-lookup"><span data-stu-id="25022-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25022-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25022-122">Minimum supported client</span></span><br/> | <span data-ttu-id="25022-123">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="25022-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="25022-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25022-124">Minimum supported server</span></span><br/> | <span data-ttu-id="25022-125">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="25022-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="25022-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25022-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="25022-127"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="25022-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25022-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25022-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25022-129">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="25022-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="25022-130">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="25022-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

