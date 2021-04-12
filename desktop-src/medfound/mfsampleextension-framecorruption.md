---
description: Specifica se un frame video è danneggiato.
ms.assetid: 0218F6F6-6832-445C-B733-6A99E4EA2A3B
title: Attributo MFSampleExtension_FrameCorruption (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d3618e5d847833b539cdfa7f6f99ae784e96c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131118"
---
# <a name="mfsampleextension_framecorruption-attribute"></a><span data-ttu-id="120a8-103">\_Attributo FrameCorruption di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="120a8-103">MFSampleExtension\_FrameCorruption attribute</span></span>

<span data-ttu-id="120a8-104">Specifica se un frame video è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="120a8-104">Specifies whether a video frame is corrupted.</span></span>

## <a name="data-type"></a><span data-ttu-id="120a8-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="120a8-105">Data type</span></span>

<span data-ttu-id="120a8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="120a8-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="120a8-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="120a8-107">Get/set</span></span>

<span data-ttu-id="120a8-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="120a8-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="120a8-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="120a8-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="120a8-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="120a8-110">Applies to</span></span>

[<span data-ttu-id="120a8-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="120a8-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="120a8-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="120a8-112">Remarks</span></span>

<span data-ttu-id="120a8-113">Un decodificatore video può impostare questo attributo sugli esempi di output.</span><span class="sxs-lookup"><span data-stu-id="120a8-113">A video decoder can set this attribute on its output samples.</span></span> <span data-ttu-id="120a8-114">Se il valore è 1, il decodificatore ha rilevato un danneggiamento dei dati nel frame.</span><span class="sxs-lookup"><span data-stu-id="120a8-114">If the value is 1, the decoder detected data corruption in the frame.</span></span> <span data-ttu-id="120a8-115">Se il valore è 0, non si verifica alcun danneggiamento dei dati oppure non ne è stato rilevato alcuno.</span><span class="sxs-lookup"><span data-stu-id="120a8-115">If the value is 0, there is no data corruption, or none was detected.</span></span>

## <a name="requirements"></a><span data-ttu-id="120a8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="120a8-116">Requirements</span></span>



| <span data-ttu-id="120a8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="120a8-117">Requirement</span></span> | <span data-ttu-id="120a8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="120a8-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="120a8-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="120a8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="120a8-120">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="120a8-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="120a8-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="120a8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="120a8-122">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="120a8-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="120a8-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="120a8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="120a8-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="120a8-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="120a8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="120a8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="120a8-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="120a8-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="120a8-127">Attributi di esempio</span><span class="sxs-lookup"><span data-stu-id="120a8-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="120a8-128">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="120a8-128">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




