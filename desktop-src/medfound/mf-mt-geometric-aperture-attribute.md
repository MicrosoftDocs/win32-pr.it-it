---
description: Definisce l'apertura geometrica per un tipo di supporto video.
ms.assetid: a2489ba1-f322-4b63-a479-0d9879c30a8c
title: Attributo MF_MT_GEOMETRIC_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e194408dd8b6bf4a4dac717c7d41aaecbb06f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967038"
---
# <a name="mf_mt_geometric_aperture-attribute"></a><span data-ttu-id="b645f-103">\_Attributo di \_ apertura geometrico MF mt \_</span><span class="sxs-lookup"><span data-stu-id="b645f-103">MF\_MT\_GEOMETRIC\_APERTURE attribute</span></span>

<span data-ttu-id="b645f-104">Definisce l'apertura geometrica per un tipo di supporto video.</span><span class="sxs-lookup"><span data-stu-id="b645f-104">Defines the geometric aperture for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="b645f-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b645f-105">Data type</span></span>

<span data-ttu-id="b645f-106">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="b645f-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="b645f-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="b645f-107">Remarks</span></span>

<span data-ttu-id="b645f-108">Il valore di questo attributo è una struttura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .</span><span class="sxs-lookup"><span data-stu-id="b645f-108">The value of this attribute is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="b645f-109">Le proporzioni dell'immagine vengono calcolate in relazione all'apertura geometrica, usando la formula seguente: proporzioni immagine = (larghezza aperture geometrica/altezza diaframma geometrica) × proporzioni pixel.</span><span class="sxs-lookup"><span data-stu-id="b645f-109">The picture aspect ratio is calculated relative to the geometric aperture, using the following formula: Picture aspect ratio = (geometric aperture width / geometric aperture height) × pixel aspect ratio.</span></span>

<span data-ttu-id="b645f-110">Se questo attributo non è impostato, si presuppone che l'apertura geometrica sia l'intero frame video.</span><span class="sxs-lookup"><span data-stu-id="b645f-110">If this attribute is not set, the geometric aperture is assumed to be the entire video frame.</span></span> <span data-ttu-id="b645f-111">Questo attributo deve essere impostato solo quando il tipo di supporto descrive uno standard video con un'area attiva definita.</span><span class="sxs-lookup"><span data-stu-id="b645f-111">You should set this attribute only when the media type describes a video standard with a defined active area.</span></span>

<span data-ttu-id="b645f-112">Ad esempio, in NTSC Television il fotogramma video è 720 × 480 con un'area attiva di 704 × 480 e una percentuale di proporzioni di pixel 10:11.</span><span class="sxs-lookup"><span data-stu-id="b645f-112">For example, in NTSC television the video frame is 720 × 480 with an active area of 704 × 480 and a 10:11 pixel aspect ratio.</span></span> <span data-ttu-id="b645f-113">L'immagine risultante ha una proporzioni di (704/480) × (10/11) = 4:3.</span><span class="sxs-lookup"><span data-stu-id="b645f-113">The resulting picture has an aspect ratio of (704/480) × (10/11) = 4:3.</span></span>

> [!Note]  
> <span data-ttu-id="b645f-114">Il Presenter predefinito per il [renderer video avanzato](enhanced-video-renderer.md) (EVR) Mostra l'apertura geometrica del video, se specificato.</span><span class="sxs-lookup"><span data-stu-id="b645f-114">The default presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) shows the geometric aperture of the video, if specified.</span></span>

 

<span data-ttu-id="b645f-115">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b645f-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="b645f-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="b645f-116">Examples</span></span>


```
HRESULT SetGeometricAperture(
    IMFMediaType *pMediaType, 
    const MFVideoArea& area
    )
{
    return pMediaType->SetBlob(
        MF_MT_GEOMETRIC_APERTURE, 
        (UINT8*)&area, 
        sizeof(MFVideoArea)
        );
}
```



## <a name="requirements"></a><span data-ttu-id="b645f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b645f-117">Requirements</span></span>



| <span data-ttu-id="b645f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b645f-118">Requirement</span></span> | <span data-ttu-id="b645f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b645f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b645f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b645f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b645f-121">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b645f-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b645f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b645f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b645f-123">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="b645f-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b645f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b645f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b645f-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b645f-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b645f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b645f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b645f-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b645f-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b645f-128">Attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b645f-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b645f-129">Proporzioni immagine</span><span class="sxs-lookup"><span data-stu-id="b645f-129">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="b645f-130">Tipi di supporti video</span><span class="sxs-lookup"><span data-stu-id="b645f-130">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="b645f-131">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="b645f-131">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="b645f-132">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="b645f-132">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="b645f-133">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="b645f-133">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="b645f-134">**\_ \_ \_ apertura minima schermo \_ MF mt**</span><span class="sxs-lookup"><span data-stu-id="b645f-134">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="b645f-135">**\_apertura dell' \_ analisi della panoramica MF mt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b645f-135">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




