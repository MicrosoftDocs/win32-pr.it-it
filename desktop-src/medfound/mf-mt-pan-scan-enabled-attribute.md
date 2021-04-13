---
description: Specifica se la modalità Pan/Scan è abilitata.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: Attributo MF_MT_PAN_SCAN_ENABLED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b347c898ce827ff37796a9698e843f6321db8a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528753"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a><span data-ttu-id="89bc7-103">\_ \_ \_ \_ Attributo abilitata per l'analisi della panoramica MF mt</span><span class="sxs-lookup"><span data-stu-id="89bc7-103">MF\_MT\_PAN\_SCAN\_ENABLED attribute</span></span>

<span data-ttu-id="89bc7-104">Specifica se la modalità Pan/Scan è abilitata.</span><span class="sxs-lookup"><span data-stu-id="89bc7-104">Specifies whether pan/scan mode is enabled.</span></span>

## <a name="data-type"></a><span data-ttu-id="89bc7-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="89bc7-105">Data type</span></span>

<span data-ttu-id="89bc7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="89bc7-106">**UINT32**</span></span>

<span data-ttu-id="89bc7-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="89bc7-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="89bc7-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="89bc7-108">Remarks</span></span>

<span data-ttu-id="89bc7-109">Se questo attributo è **true**, verrà visualizzata solo l'area di Pan/Scan del video.</span><span class="sxs-lookup"><span data-stu-id="89bc7-109">If this attribute is **TRUE**, only the pan/scan region of the video should be displayed.</span></span> <span data-ttu-id="89bc7-110">L'area di Pan/Scan è specificata dall'attributo di [**\_ \_ \_ \_ apertura della Panoramica di MF mt**](mf-mt-pan-scan-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="89bc7-110">The pan/scan region is specified by the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="89bc7-111">Se questo attributo è **false** o non impostato, verrà visualizzata l'intera apertura di visualizzazione del video.</span><span class="sxs-lookup"><span data-stu-id="89bc7-111">If this attribute is **FALSE** or not set, the entire display aperture of the video should be displayed.</span></span> <span data-ttu-id="89bc7-112">L'apertura di visualizzazione è specificata dall'attributo di [**\_ \_ \_ \_ apertura della visualizzazione minima MF mt**](mf-mt-minimum-display-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="89bc7-112">The display aperture is specified by the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="89bc7-113">Se si imposta questo attributo su **true**, impostare anche il valore dell'attributo [**MF \_ mt \_ Pan \_ Scan \_ aperture**](mf-mt-pan-scan-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="89bc7-113">If you set this attribute to **TRUE**, also set the value of the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="89bc7-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="89bc7-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="89bc7-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89bc7-115">Requirements</span></span>



| <span data-ttu-id="89bc7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="89bc7-116">Requirement</span></span> | <span data-ttu-id="89bc7-117">Valore</span><span class="sxs-lookup"><span data-stu-id="89bc7-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89bc7-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89bc7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="89bc7-119">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="89bc7-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="89bc7-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89bc7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="89bc7-121">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="89bc7-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="89bc7-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89bc7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="89bc7-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="89bc7-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89bc7-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89bc7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89bc7-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="89bc7-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="89bc7-126">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="89bc7-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="89bc7-127">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="89bc7-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="89bc7-128">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="89bc7-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="89bc7-129">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="89bc7-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="89bc7-130">Proporzioni immagine</span><span class="sxs-lookup"><span data-stu-id="89bc7-130">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> </dl>

 

 




