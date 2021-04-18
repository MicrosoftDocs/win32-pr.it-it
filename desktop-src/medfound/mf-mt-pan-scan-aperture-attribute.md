---
description: Definisce l'apertura di Pan/Scan, ovvero la 4&\# 215; 3 area del video che deve essere visualizzata in modalità Pan/Scan.
ms.assetid: faa577fd-6572-46b9-9c6c-f91c47832cb5
title: Attributo MF_MT_PAN_SCAN_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a798ba96315126daab94ba92e8791bfeac77db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308466"
---
# <a name="mf_mt_pan_scan_aperture-attribute"></a><span data-ttu-id="1c8d9-103">\_Attributo di \_ apertura della panoramica dell' \_ analisi MF mt \_</span><span class="sxs-lookup"><span data-stu-id="1c8d9-103">MF\_MT\_PAN\_SCAN\_APERTURE attribute</span></span>

<span data-ttu-id="1c8d9-104">Definisce l'apertura di Pan/Scan, ovvero l'area di 4 × 3 del video che deve essere visualizzata in modalità Pan/Scan.</span><span class="sxs-lookup"><span data-stu-id="1c8d9-104">Defines the pan/scan aperture, which is the 4×3 region of video that should be displayed in pan/scan mode.</span></span>

## <a name="data-type"></a><span data-ttu-id="1c8d9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1c8d9-105">Data type</span></span>

<span data-ttu-id="1c8d9-106">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="1c8d9-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="1c8d9-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c8d9-107">Remarks</span></span>

<span data-ttu-id="1c8d9-108">Il valore dell'attributo è una struttura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .</span><span class="sxs-lookup"><span data-stu-id="1c8d9-108">The attribute value is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="1c8d9-109">Questo attributo viene usato per ritagliare un video widescreen in proporzioni di 4:3.</span><span class="sxs-lookup"><span data-stu-id="1c8d9-109">This attribute is used to crop widescreen video to a 4:3 aspect ratio.</span></span> <span data-ttu-id="1c8d9-110">L'apertura di Pan/Scan viene usata solo in modalità Pan/Scan, che è abilitata impostando l'attributo [**MF \_ mt \_ Pan \_ Scan \_ Enabled**](mf-mt-pan-scan-enabled-attribute.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="1c8d9-110">The pan/scan aperture is used only in pan/scan mode, which is enabled by setting the [**MF\_MT\_PAN\_SCAN\_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="1c8d9-111">Se la modalità Pan/Scan non è abilitata, usare l'apertura di visualizzazione, specificata dall'attributo di [**\_ \_ \_ \_ apertura della visualizzazione minima MF mt**](mf-mt-minimum-display-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="1c8d9-111">If pan/scan mode is not enabled, use the display aperture, specified by the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="1c8d9-112">Se questo attributo non è impostato, si presuppone che l'apertura di Pan/Scan sia l'intero frame video.</span><span class="sxs-lookup"><span data-stu-id="1c8d9-112">If this attribute is not set, the pan/scan aperture is assumed to be the entire video frame.</span></span>

<span data-ttu-id="1c8d9-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1c8d9-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c8d9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c8d9-114">Requirements</span></span>



| <span data-ttu-id="1c8d9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c8d9-115">Requirement</span></span> | <span data-ttu-id="1c8d9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1c8d9-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1c8d9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c8d9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1c8d9-118">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1c8d9-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1c8d9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c8d9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1c8d9-120">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="1c8d9-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1c8d9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c8d9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c8d9-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c8d9-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c8d9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c8d9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c8d9-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1c8d9-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1c8d9-125">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="1c8d9-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="1c8d9-126">Proporzioni immagine</span><span class="sxs-lookup"><span data-stu-id="1c8d9-126">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="1c8d9-127">Tipi di supporti video</span><span class="sxs-lookup"><span data-stu-id="1c8d9-127">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="1c8d9-128">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="1c8d9-128">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="1c8d9-129">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="1c8d9-129">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="1c8d9-130">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="1c8d9-130">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="1c8d9-131">**\_ \_ apertura geometrica MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="1c8d9-131">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="1c8d9-132">**\_ \_ \_ apertura minima schermo \_ MF mt**</span><span class="sxs-lookup"><span data-stu-id="1c8d9-132">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="1c8d9-133">**\_ \_ Analisi panoramica MF \_ mt \_ abilitata**</span><span class="sxs-lookup"><span data-stu-id="1c8d9-133">**MF\_MT\_PAN\_SCAN\_ENABLED**</span></span>](mf-mt-pan-scan-enabled-attribute.md)
</dt> </dl>

 

 




