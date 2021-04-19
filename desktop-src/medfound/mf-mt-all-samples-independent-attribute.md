---
description: Specifica un tipo di supporto se ogni campione è indipendente dagli altri esempi nel flusso.
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: Attributo MF_MT_ALL_SAMPLES_INDEPENDENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82173e99a30e033b3d90f6cfec0dc2aa8b3af97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309558"
---
# <a name="mf_mt_all_samples_independent-attribute"></a><span data-ttu-id="2a8bf-103">\_ \_ Attributo indipendente di tutti gli esempi MF mt \_ \_</span><span class="sxs-lookup"><span data-stu-id="2a8bf-103">MF\_MT\_ALL\_SAMPLES\_INDEPENDENT attribute</span></span>

<span data-ttu-id="2a8bf-104">Specifica un tipo di supporto se ogni campione è indipendente dagli altri esempi nel flusso.</span><span class="sxs-lookup"><span data-stu-id="2a8bf-104">Specifies for a media type whether each sample is independent of the other samples in the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="2a8bf-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2a8bf-105">Data type</span></span>

<span data-ttu-id="2a8bf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2a8bf-106">**UINT32**</span></span>

<span data-ttu-id="2a8bf-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="2a8bf-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a8bf-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a8bf-108">Remarks</span></span>

<span data-ttu-id="2a8bf-109">Se questo attributo è **false**, alcuni esempi non possono essere usati senza fare riferimento ad altri esempi nel flusso.</span><span class="sxs-lookup"><span data-stu-id="2a8bf-109">If this attribute is **FALSE**, some samples cannot be used without referring to other samples in the stream.</span></span> <span data-ttu-id="2a8bf-110">Se, ad esempio, un formato video contiene frame Delta, questo attributo deve essere **false**.</span><span class="sxs-lookup"><span data-stu-id="2a8bf-110">For example, if a video format contains delta frames, this attribute should be **FALSE**.</span></span>

<span data-ttu-id="2a8bf-111">Questo attributo corrisponde al campo **bTemporalCompression** nella struttura del [**tipo di \_ supporto \_ DirectShow am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="2a8bf-111">This attribute corresponds to the **bTemporalCompression** field in the DirectShow [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="2a8bf-112">Impostare questo attributo su **true** per tutti i tipi di supporto non compressi.</span><span class="sxs-lookup"><span data-stu-id="2a8bf-112">Set this attribute to **TRUE** for all uncompressed media types.</span></span>

<span data-ttu-id="2a8bf-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="2a8bf-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a8bf-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a8bf-114">Requirements</span></span>



| <span data-ttu-id="2a8bf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a8bf-115">Requirement</span></span> | <span data-ttu-id="2a8bf-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2a8bf-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a8bf-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a8bf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2a8bf-118">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2a8bf-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="2a8bf-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a8bf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2a8bf-120">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="2a8bf-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2a8bf-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a8bf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a8bf-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a8bf-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a8bf-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a8bf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a8bf-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2a8bf-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2a8bf-125">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="2a8bf-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="2a8bf-126">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="2a8bf-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="2a8bf-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="2a8bf-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="2a8bf-128">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="2a8bf-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
