---
description: Contiene IMFMediaType che descrive il tipo di formato di immagine contenuto nell' \_ attributo di anteprima MFSampleExtension.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: Attributo MFSampleExtension_PhotoThumbnailMediaType (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0e415fb0d3b062b4a5064006d3873cd42ea593
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320679"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a><span data-ttu-id="774fc-103">\_Attributo PhotoThumbnailMediaType di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="774fc-103">MFSampleExtension\_PhotoThumbnailMediaType attribute</span></span>

<span data-ttu-id="774fc-104">Contiene [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) che descrive il tipo di formato di immagine contenuto nell'attributo di [ \_ Anteprima MFSampleExtension](mfsampleextension-photothumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="774fc-104">Contains the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) which describes the image format type contained in the [MFSampleExtension\_PhotoThumbnail](mfsampleextension-photothumbnail.md) attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="774fc-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="774fc-105">Data type</span></span>

<span data-ttu-id="774fc-106">**IUnknown** archiviato come **IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="774fc-106">**IUnknown** stored as **IMFMediaType**</span></span>

## <a name="remarks"></a><span data-ttu-id="774fc-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="774fc-107">Remarks</span></span>

<span data-ttu-id="774fc-108">Se nell'esempio Photo è presente l'attributo [MFSampleExtension \_ fotothumbnail](mfsampleextension-photothumbnail.md) , il PhotoThumbnailMediaType MFSampleExtension \_ è obbligatorio e deve contenere almeno il [ \_ \_ \_ tipo principale MF mt](mf-mt-major-type-attribute.md), il [ \_ \_ sottotipo](mf-mt-subtype-attribute.md) MF mt e la dimensione del [ \_ frame MF \_ \_ mt](mf-mt-frame-size-attribute.md) che descrivono l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="774fc-108">If the [MFSampleExtension\_PhotoThumbnail](mfsampleextension-photothumbnail.md) attribute is present on the photo sample, the MFSampleExtension\_PhotoThumbnailMediaType is required and must contain, at a minimum, [MF\_MT\_MAJOR\_TYPE](mf-mt-major-type-attribute.md), [MF\_MT\_SUBTYPE](mf-mt-subtype-attribute.md) and [MF\_MT\_FRAME\_SIZE](mf-mt-frame-size-attribute.md) which describe the thumbnail.</span></span>

## <a name="requirements"></a><span data-ttu-id="774fc-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="774fc-109">Requirements</span></span>



| <span data-ttu-id="774fc-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="774fc-110">Requirement</span></span> | <span data-ttu-id="774fc-111">Valore</span><span class="sxs-lookup"><span data-stu-id="774fc-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="774fc-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="774fc-112">Minimum supported client</span></span><br/> | <span data-ttu-id="774fc-113">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="774fc-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="774fc-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="774fc-114">Minimum supported server</span></span><br/> | <span data-ttu-id="774fc-115">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="774fc-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="774fc-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="774fc-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="774fc-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="774fc-117"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="774fc-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="774fc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="774fc-119">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="774fc-119">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="774fc-120">Anteprima di MFSampleExtension \_</span><span class="sxs-lookup"><span data-stu-id="774fc-120">MFSampleExtension\_PhotoThumbnail</span></span>](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




