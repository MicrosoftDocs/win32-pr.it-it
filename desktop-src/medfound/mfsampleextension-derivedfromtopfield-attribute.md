---
description: Specifica se un fotogramma video deinterlacciato è stato derivato dal campo superiore o dal campo inferiore.
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: Attributo MFSampleExtension_DerivedFromTopField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f90a67edf0b08337748bc118b0aa4ff024ec0ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310243"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a><span data-ttu-id="46b9a-103">\_Attributo DerivedFromTopField di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="46b9a-103">MFSampleExtension\_DerivedFromTopField attribute</span></span>

<span data-ttu-id="46b9a-104">Specifica se un fotogramma video deinterlacciato è stato derivato dal campo superiore o dal campo inferiore.</span><span class="sxs-lookup"><span data-stu-id="46b9a-104">Specifies whether a deinterlaced video frame was derived from the upper field or the lower field.</span></span> <span data-ttu-id="46b9a-105">Questo attributo si applica agli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="46b9a-105">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="46b9a-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="46b9a-106">Data type</span></span>

<span data-ttu-id="46b9a-107">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46b9a-107">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="46b9a-108">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="46b9a-108">Get/set</span></span>

<span data-ttu-id="46b9a-109">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="46b9a-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="46b9a-110">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="46b9a-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="46b9a-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="46b9a-111">Applies to</span></span>

[<span data-ttu-id="46b9a-112">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="46b9a-112">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="46b9a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="46b9a-113">Remarks</span></span>

<span data-ttu-id="46b9a-114">Questo attributo è valido solo per gli esempi deinterlacciati.</span><span class="sxs-lookup"><span data-stu-id="46b9a-114">This attribute is valid for deinterlaced samples only.</span></span> <span data-ttu-id="46b9a-115">Impostare questo attributo se il frame è stato deinterlacciato interpolando uno dei campi.</span><span class="sxs-lookup"><span data-stu-id="46b9a-115">Set this attribute if the frame was deinterlaced by interpolating one of the fields.</span></span>

<span data-ttu-id="46b9a-116">Se il valore è **true**, il campo inferiore è stato interpolato dal campo superiore.</span><span class="sxs-lookup"><span data-stu-id="46b9a-116">If the value is **TRUE**, the lower field was interpolated from the upper field.</span></span> <span data-ttu-id="46b9a-117">Se il valore è **false**, il campo superiore è stato interpolato dal campo inferiore.</span><span class="sxs-lookup"><span data-stu-id="46b9a-117">If the value is **FALSE**, the upper field was interpolated from the lower field.</span></span>

<span data-ttu-id="46b9a-118">Se l'attributo non è impostato, il frame non è stato deinterlacciato.</span><span class="sxs-lookup"><span data-stu-id="46b9a-118">If the attribute is not set, the frame has not been deinterlaced.</span></span> <span data-ttu-id="46b9a-119">Il frame è un frame progressivo reale oppure è un frame interlacciato.</span><span class="sxs-lookup"><span data-stu-id="46b9a-119">The frame is either a true progressive frame, or it is an interlaced frame.</span></span>

<span data-ttu-id="46b9a-120">Questo attributo è informativo.</span><span class="sxs-lookup"><span data-stu-id="46b9a-120">This attribute is informational.</span></span> <span data-ttu-id="46b9a-121">Un deinterlacciatore software può impostare questo attributo.</span><span class="sxs-lookup"><span data-stu-id="46b9a-121">A software deinterlacer could set this attribute.</span></span> <span data-ttu-id="46b9a-122">Se questo attributo è impostato, fornisce un suggerimento che è possibile ripristinare il campo originale eliminando le righe di analisi interpolate.</span><span class="sxs-lookup"><span data-stu-id="46b9a-122">If this attribute is set, it provides a hint that you can recover the original field by dropping the interpolated scan lines.</span></span> <span data-ttu-id="46b9a-123">Se, ad esempio, l'attributo è **true**, è possibile ripristinare il campo superiore originale rimuovendo il campo inferiore interpolato.</span><span class="sxs-lookup"><span data-stu-id="46b9a-123">For example, if the attribute is **TRUE**, you can recover the original upper field by dropping the interpolated lower field.</span></span>

<span data-ttu-id="46b9a-124">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="46b9a-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="46b9a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46b9a-125">Requirements</span></span>



| <span data-ttu-id="46b9a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="46b9a-126">Requirement</span></span> | <span data-ttu-id="46b9a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="46b9a-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="46b9a-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46b9a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="46b9a-129">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="46b9a-129">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="46b9a-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46b9a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="46b9a-131">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="46b9a-131">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="46b9a-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46b9a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="46b9a-133"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="46b9a-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46b9a-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46b9a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46b9a-135">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="46b9a-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="46b9a-136">Attributi di esempio</span><span class="sxs-lookup"><span data-stu-id="46b9a-136">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="46b9a-137">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="46b9a-137">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="46b9a-138">Interlacciamento video</span><span class="sxs-lookup"><span data-stu-id="46b9a-138">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




