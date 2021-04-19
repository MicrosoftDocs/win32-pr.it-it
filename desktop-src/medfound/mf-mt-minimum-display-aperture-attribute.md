---
description: Definisce l'apertura di visualizzazione, ovvero l'area di un frame video che contiene dati di immagine validi.
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: Attributo MF_MT_MINIMUM_DISPLAY_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d13252378422081044d7f2cb21e5a31098702a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307505"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a><span data-ttu-id="817da-103">\_ \_ \_ Attributo apertura minima schermo MF mt \_</span><span class="sxs-lookup"><span data-stu-id="817da-103">MF\_MT\_MINIMUM\_DISPLAY\_APERTURE attribute</span></span>

<span data-ttu-id="817da-104">Definisce l'apertura di visualizzazione, ovvero l'area di un frame video che contiene dati di immagine validi.</span><span class="sxs-lookup"><span data-stu-id="817da-104">Defines the display aperture, which is the region of a video frame that contains valid image data.</span></span>

## <a name="data-type"></a><span data-ttu-id="817da-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="817da-105">Data type</span></span>

<span data-ttu-id="817da-106">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="817da-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="817da-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="817da-107">Remarks</span></span>

<span data-ttu-id="817da-108">Il valore dell'attributo è una struttura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .</span><span class="sxs-lookup"><span data-stu-id="817da-108">The attribute value is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="817da-109">Il diaframma di visualizzazione minimo è l'area che contiene la parte valida del segnale.</span><span class="sxs-lookup"><span data-stu-id="817da-109">The minimum display aperture is the region that contains the valid portion of the signal.</span></span> <span data-ttu-id="817da-110">I pixel al di fuori dell'apertura contengono dati non validi e non devono essere visualizzati.</span><span class="sxs-lookup"><span data-stu-id="817da-110">The pixels outside the aperture contain invalid data and should not be displayed.</span></span>

<span data-ttu-id="817da-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="817da-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="817da-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="817da-112">Requirements</span></span>



| <span data-ttu-id="817da-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="817da-113">Requirement</span></span> | <span data-ttu-id="817da-114">Valore</span><span class="sxs-lookup"><span data-stu-id="817da-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="817da-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="817da-115">Minimum supported client</span></span><br/> | <span data-ttu-id="817da-116">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="817da-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="817da-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="817da-117">Minimum supported server</span></span><br/> | <span data-ttu-id="817da-118">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="817da-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="817da-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="817da-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="817da-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="817da-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="817da-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="817da-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="817da-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="817da-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="817da-123">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="817da-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="817da-124">Proporzioni immagine</span><span class="sxs-lookup"><span data-stu-id="817da-124">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="817da-125">Tipi di supporti video</span><span class="sxs-lookup"><span data-stu-id="817da-125">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="817da-126">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="817da-126">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="817da-127">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="817da-127">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="817da-128">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="817da-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="817da-129">**\_ \_ apertura geometrica MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="817da-129">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="817da-130">**\_apertura dell' \_ analisi della panoramica MF mt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="817da-130">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




