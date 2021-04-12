---
description: Proporzioni in pixel per un tipo di supporto video.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: Attributo MF_MT_PIXEL_ASPECT_RATIO (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c0d28ea11ba664208fcfe5fc356f1f57f2878e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526599"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a><span data-ttu-id="bcefd-103">Attributo proporzioni MF \_ mt \_ pixel \_ \_</span><span class="sxs-lookup"><span data-stu-id="bcefd-103">MF\_MT\_PIXEL\_ASPECT\_RATIO attribute</span></span>

<span data-ttu-id="bcefd-104">Proporzioni in pixel per un tipo di supporto video.</span><span class="sxs-lookup"><span data-stu-id="bcefd-104">Pixel aspect ratio for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="bcefd-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bcefd-105">Data type</span></span>

<span data-ttu-id="bcefd-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="bcefd-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="bcefd-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="bcefd-107">Remarks</span></span>

<span data-ttu-id="bcefd-108">I 32 bit superiori contengono il numeratore delle proporzioni in pixel e i 32 bit inferiori contengono il denominatore.</span><span class="sxs-lookup"><span data-stu-id="bcefd-108">The upper 32 bits contain the numerator of the pixel aspect ratio and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="bcefd-109">Il numeratore è il componente orizzontale della proporzioni; il denominatore è il componente verticale.</span><span class="sxs-lookup"><span data-stu-id="bcefd-109">The numerator is the horizontal component of the aspect ratio; the denominator is the vertical component.</span></span>

<span data-ttu-id="bcefd-110">Per impostare questo attributo, utilizzare la funzione [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="bcefd-110">To set this attribute, use the [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) function.</span></span> <span data-ttu-id="bcefd-111">Per ottenere questo attributo, usare la funzione [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="bcefd-111">To get this attribute, use the [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) function.</span></span>

<span data-ttu-id="bcefd-112">Le proporzioni in pixel descrivono la forma dei pixel nell'immagine video visualizzata.</span><span class="sxs-lookup"><span data-stu-id="bcefd-112">The pixel aspect ratio describes the shape of the pixels in the displayed video image.</span></span> <span data-ttu-id="bcefd-113">Impostare questo attributo se l'immagine ha pixel non quadrati.</span><span class="sxs-lookup"><span data-stu-id="bcefd-113">Set this attribute if the image has non-square pixels.</span></span> <span data-ttu-id="bcefd-114">Per visualizzare correttamente in un dispositivo di visualizzazione con pixel quadrati, l'immagine deve essere ridimensionata in base all'inverso delle proporzioni in pixel dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="bcefd-114">To display correctly on a display device with square pixels, the image must be scaled by the inverse of the image's pixel aspect ratio.</span></span>

<span data-ttu-id="bcefd-115">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="bcefd-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcefd-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcefd-116">Requirements</span></span>



| <span data-ttu-id="bcefd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcefd-117">Requirement</span></span> | <span data-ttu-id="bcefd-118">Valore</span><span class="sxs-lookup"><span data-stu-id="bcefd-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bcefd-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcefd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bcefd-120">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bcefd-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="bcefd-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcefd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bcefd-122">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="bcefd-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="bcefd-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bcefd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcefd-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcefd-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcefd-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcefd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcefd-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bcefd-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bcefd-127">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="bcefd-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="bcefd-128">Attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bcefd-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bcefd-129">Proporzioni immagine</span><span class="sxs-lookup"><span data-stu-id="bcefd-129">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> </dl>

 

 




