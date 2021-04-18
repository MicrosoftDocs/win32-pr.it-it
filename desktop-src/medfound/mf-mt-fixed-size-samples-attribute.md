---
description: Specifica se gli esempi hanno dimensioni fisse per un tipo di supporto.
ms.assetid: 2d67864a-fd2f-400d-8a1e-e71dc1920593
title: Attributo MF_MT_FIXED_SIZE_SAMPLES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1bb5bdd4e1330e4744902ed1b37cc55b7a67a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309545"
---
# <a name="mf_mt_fixed_size_samples-attribute"></a><span data-ttu-id="24dca-103">\_Attributo degli \_ \_ esempi di dimensioni fisse MF mt \_</span><span class="sxs-lookup"><span data-stu-id="24dca-103">MF\_MT\_FIXED\_SIZE\_SAMPLES attribute</span></span>

<span data-ttu-id="24dca-104">Specifica se gli esempi hanno dimensioni fisse per un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="24dca-104">Specifies for a media type whether the samples have a fixed size.</span></span>

## <a name="data-type"></a><span data-ttu-id="24dca-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="24dca-105">Data type</span></span>

<span data-ttu-id="24dca-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="24dca-106">**UINT32**</span></span>

<span data-ttu-id="24dca-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="24dca-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="24dca-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="24dca-108">Remarks</span></span>

<span data-ttu-id="24dca-109">Se questo attributo è **true**, ogni campione nel flusso ha le stesse dimensioni (in byte).</span><span class="sxs-lookup"><span data-stu-id="24dca-109">If this attribute is **TRUE**, every sample in the stream is the same size (in bytes).</span></span> <span data-ttu-id="24dca-110">In caso contrario, la dimensione degli esempi potrebbe variare.</span><span class="sxs-lookup"><span data-stu-id="24dca-110">Otherwise, samples might vary in size.</span></span>

<span data-ttu-id="24dca-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="24dca-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="24dca-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24dca-112">Requirements</span></span>



| <span data-ttu-id="24dca-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="24dca-113">Requirement</span></span> | <span data-ttu-id="24dca-114">Valore</span><span class="sxs-lookup"><span data-stu-id="24dca-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="24dca-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24dca-115">Minimum supported client</span></span><br/> | <span data-ttu-id="24dca-116">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="24dca-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="24dca-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24dca-117">Minimum supported server</span></span><br/> | <span data-ttu-id="24dca-118">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="24dca-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="24dca-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24dca-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="24dca-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="24dca-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24dca-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24dca-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24dca-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="24dca-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="24dca-123">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="24dca-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="24dca-124">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="24dca-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="24dca-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="24dca-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="24dca-126">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="24dca-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




