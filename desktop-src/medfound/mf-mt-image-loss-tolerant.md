---
description: Specifica se un flusso di immagini ASF è un tipo JPEG degradabile.
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: Attributo MF_MT_IMAGE_LOSS_TOLERANT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea33f9f5f49725d164bd26ba21b9602bffef2b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879390"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a><span data-ttu-id="d2001-103">\_Attributo a \_ \_ tolleranza di perdita immagine MF mt \_</span><span class="sxs-lookup"><span data-stu-id="d2001-103">MF\_MT\_IMAGE\_LOSS\_TOLERANT attribute</span></span>

<span data-ttu-id="d2001-104">Specifica se un flusso di immagini ASF è un tipo JPEG degradabile.</span><span class="sxs-lookup"><span data-stu-id="d2001-104">Specifies whether an ASF image stream is a degradable JPEG type.</span></span>

## <a name="data-type"></a><span data-ttu-id="d2001-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d2001-105">Data type</span></span>

<span data-ttu-id="d2001-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d2001-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="d2001-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="d2001-107">Get/set</span></span>

<span data-ttu-id="d2001-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="d2001-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="d2001-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="d2001-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d2001-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="d2001-110">Applies to</span></span>

[<span data-ttu-id="d2001-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d2001-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="d2001-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2001-112">Remarks</span></span>

<span data-ttu-id="d2001-113">Questo attributo si applica al tipo di supporto per i flussi di immagine in ASF.</span><span class="sxs-lookup"><span data-stu-id="d2001-113">This attribute applies to the media type for image streams in ASF.</span></span> <span data-ttu-id="d2001-114">Se il valore è **true**, il flusso è un tipo di immagine JPEG degradabile.</span><span class="sxs-lookup"><span data-stu-id="d2001-114">If the value is **TRUE**, the stream is a degradable JPEG image type.</span></span> <span data-ttu-id="d2001-115">In caso contrario, il flusso è un tipo di immagine JFIF.</span><span class="sxs-lookup"><span data-stu-id="d2001-115">Otherwise, the stream is a JFIF image type.</span></span> <span data-ttu-id="d2001-116">Per ulteriori informazioni su questi tipi di flusso, vedere la specifica ASF.</span><span class="sxs-lookup"><span data-stu-id="d2001-116">For more information about these stream types, see the ASF specification.</span></span>

<span data-ttu-id="d2001-117">Oltre all' \_ attributo MF mt \_ Image \_ Loss \_ tolerance, il tipo di supporto per un flusso di immagini ASF contiene gli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d2001-117">In addition to the MF\_MT\_IMAGE\_LOSS\_TOLERANT attribute, the media type for an ASF image stream contains the following attributes:</span></span>



| <span data-ttu-id="d2001-118">Attributo</span><span class="sxs-lookup"><span data-stu-id="d2001-118">Attribute</span></span>                                                 | <span data-ttu-id="d2001-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2001-119">Description</span></span>                                |
|-----------------------------------------------------------|--------------------------------------------|
| [<span data-ttu-id="d2001-120">**\_ \_ tipo principale MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="d2001-120">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="d2001-121">Contiene il valore **MFMediaType \_ Image**.</span><span class="sxs-lookup"><span data-stu-id="d2001-121">Contains the value **MFMediaType\_Image**.</span></span> |
| [<span data-ttu-id="d2001-122">**\_dimensioni del \_ frame MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="d2001-122">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md) | <span data-ttu-id="d2001-123">Restituisce le dimensioni dell'immagine in pixel.</span><span class="sxs-lookup"><span data-stu-id="d2001-123">Gives the image size in pixels.</span></span>            |



 

<span data-ttu-id="d2001-124">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d2001-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2001-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2001-125">Requirements</span></span>



| <span data-ttu-id="d2001-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2001-126">Requirement</span></span> | <span data-ttu-id="d2001-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d2001-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d2001-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2001-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d2001-129">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d2001-129">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d2001-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2001-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d2001-131">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d2001-131">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d2001-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2001-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2001-133"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2001-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2001-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2001-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2001-135">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d2001-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d2001-136">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="d2001-136">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




