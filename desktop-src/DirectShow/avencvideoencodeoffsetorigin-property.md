---
description: Specifica gli angoli sinistro e superiore del rettangolo di ridimensionamento, se il video è ritagliato.
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: Proprietà AVEncVideoEncodeOffsetOrigin (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db4d685942b8c21f2d5047003f2172c54b1d50d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124227"
---
# <a name="avencvideoencodeoffsetorigin-property"></a><span data-ttu-id="a1947-103">Proprietà AVEncVideoEncodeOffsetOrigin</span><span class="sxs-lookup"><span data-stu-id="a1947-103">AVEncVideoEncodeOffsetOrigin property</span></span>

<span data-ttu-id="a1947-104">Specifica gli angoli sinistro e superiore del rettangolo di ridimensionamento, se il video è ritagliato.</span><span class="sxs-lookup"><span data-stu-id="a1947-104">Specifies the left and top corners of the clipping rectangle, if the video is cropped.</span></span>

<span data-ttu-id="a1947-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a1947-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a1947-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a1947-106">Data type</span></span>

<span data-ttu-id="a1947-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a1947-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a1947-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="a1947-108">Property GUID</span></span>

<span data-ttu-id="a1947-109">**Codecapis \_ AVEncVideoEncodeOffsetOrigin**</span><span class="sxs-lookup"><span data-stu-id="a1947-109">**CODECAPI\_AVEncVideoEncodeOffsetOrigin**</span></span>

## <a name="property-value"></a><span data-ttu-id="a1947-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a1947-110">Property value</span></span>

<span data-ttu-id="a1947-111">I 16 bit superiori del valore contengono l'offset dal bordo sinistro del frame di input, espresso in pixel.</span><span class="sxs-lookup"><span data-stu-id="a1947-111">The upper 16 bits of the value contain the offset from the left edge of the input frame, in pixels.</span></span> <span data-ttu-id="a1947-112">I 16 bit inferiori contengono l'offset dal bordo superiore del fotogramma di input, espresso in pixel.</span><span class="sxs-lookup"><span data-stu-id="a1947-112">The lower 16 bits contain the offset from the top edge of the input frame, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1947-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1947-113">Remarks</span></span>

<span data-ttu-id="a1947-114">Le applicazioni possono impostare questa proprietà per ritagliare il video di input.</span><span class="sxs-lookup"><span data-stu-id="a1947-114">Applications can set this property to crop the input video.</span></span> <span data-ttu-id="a1947-115">Utilizzare la proprietà [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) per specificare la larghezza e l'altezza del rettangolo di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="a1947-115">Use the [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) property to specify the width and height of the clipping rectangle.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1947-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1947-116">Requirements</span></span>



| <span data-ttu-id="a1947-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1947-117">Requirement</span></span> | <span data-ttu-id="a1947-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a1947-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1947-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1947-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a1947-120">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="a1947-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a1947-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1947-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a1947-122">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a1947-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a1947-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1947-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1947-124"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1947-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1947-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1947-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1947-126">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="a1947-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a1947-127">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a1947-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




