---
description: Stride della superficie predefinita, per un tipo di supporto video non compresso. Stride indica il numero di byte necessari per passare da una riga di pixel a quella successiva.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: Attributo MF_MT_DEFAULT_STRIDE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2b9633e14c8d414355ca41be29a9c6c2f8886
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226636"
---
# <a name="mf_mt_default_stride-attribute"></a><span data-ttu-id="6a9b4-104">\_ \_ Attributo stride predefinito MF mt \_</span><span class="sxs-lookup"><span data-stu-id="6a9b4-104">MF\_MT\_DEFAULT\_STRIDE attribute</span></span>

<span data-ttu-id="6a9b4-105">Stride della superficie predefinita, per un tipo di supporto video non compresso.</span><span class="sxs-lookup"><span data-stu-id="6a9b4-105">Default surface stride, for an uncompressed video media type.</span></span> <span data-ttu-id="6a9b4-106">Stride indica il numero di byte necessari per passare da una riga di pixel a quella successiva.</span><span class="sxs-lookup"><span data-stu-id="6a9b4-106">Stride is the number of bytes needed to go from one row of pixels to the next.</span></span>

## <a name="data-type"></a><span data-ttu-id="6a9b4-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6a9b4-107">Data type</span></span>

<span data-ttu-id="6a9b4-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6a9b4-108">**UINT32**</span></span>

<span data-ttu-id="6a9b4-109">Considera come un valore **Int32** .</span><span class="sxs-lookup"><span data-stu-id="6a9b4-109">Treat as a **INT32** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a9b4-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a9b4-110">Remarks</span></span>

<span data-ttu-id="6a9b4-111">Il valore dell'attributo viene archiviato come **UInt32**, ma deve essere eseguito il cast a un valore intero con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="6a9b4-111">The attribute value is stored as a **UINT32**, but should be cast to a 32-bit signed integer value.</span></span> <span data-ttu-id="6a9b4-112">Stride può essere negativo.</span><span class="sxs-lookup"><span data-stu-id="6a9b4-112">Stride can be negative.</span></span>

<span data-ttu-id="6a9b4-113">Stride è un valore positivo per le immagini dall'alto verso il basso e negativo per le immagini dal basso verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="6a9b4-113">Stride is positive for top-down images, and negative for bottom-up images.</span></span>

<span data-ttu-id="6a9b4-114">Questo attributo fornisce lo stride per una rappresentazione *contigua* dell'immagine in memoria; ovvero una rappresentazione senza ulteriori byte di riempimento dopo ogni riga.</span><span class="sxs-lookup"><span data-stu-id="6a9b4-114">This attribute gives the stride for a *contiguous* representation of the image in memory; that is, a representation with no additional padding bytes after each row.</span></span> <span data-ttu-id="6a9b4-115">Se un buffer multimediale supporta l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , usare il metodo [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) per ottenere lo stride effettivo della superficie, che può includere byte di riempimento aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="6a9b4-115">If a media buffer supports the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface, use the [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) method to get the actual stride of the surface, which might include extra padding bytes.</span></span>

<span data-ttu-id="6a9b4-116">Per altre informazioni sullo stride della superficie, vedere [immagine stride](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="6a9b4-116">For more information about surface stride, see [Image Stride](image-stride.md).</span></span>

<span data-ttu-id="6a9b4-117">Per un esempio di come calcolare lo stride predefinito, vedere [buffer video non compressi](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="6a9b4-117">For an example of how to calculate the default stride, see [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

<span data-ttu-id="6a9b4-118">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6a9b4-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a9b4-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a9b4-119">Requirements</span></span>



| <span data-ttu-id="6a9b4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a9b4-120">Requirement</span></span> | <span data-ttu-id="6a9b4-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6a9b4-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6a9b4-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a9b4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6a9b4-123">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6a9b4-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6a9b4-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a9b4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6a9b4-125">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="6a9b4-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6a9b4-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a9b4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a9b4-127"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a9b4-127"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a9b4-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a9b4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a9b4-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6a9b4-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6a9b4-130">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="6a9b4-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="6a9b4-131">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="6a9b4-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="6a9b4-132">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6a9b4-132">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="6a9b4-133">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="6a9b4-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="6a9b4-134">Stride immagine</span><span class="sxs-lookup"><span data-stu-id="6a9b4-134">Image Stride</span></span>](image-stride.md)
</dt> </dl>

 

 




