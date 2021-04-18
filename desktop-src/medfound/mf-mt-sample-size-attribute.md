---
description: Specifica la dimensione di ciascun campione, in byte, in un tipo di supporto.
ms.assetid: 4c28f73d-ff40-4eb9-a45f-57a60df719c6
title: Attributo MF_MT_SAMPLE_SIZE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bb897524dac5f73f4d4553f8e77e02ef473f611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309538"
---
# <a name="mf_mt_sample_size-attribute"></a><span data-ttu-id="1e20c-103">\_ \_ Attributo dimensioni campione MF mt \_</span><span class="sxs-lookup"><span data-stu-id="1e20c-103">MF\_MT\_SAMPLE\_SIZE attribute</span></span>

<span data-ttu-id="1e20c-104">Specifica la dimensione di ciascun campione, in byte, in un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="1e20c-104">Specifies the size of each sample, in bytes, in a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="1e20c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1e20c-105">Data type</span></span>

<span data-ttu-id="1e20c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1e20c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1e20c-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e20c-107">Remarks</span></span>

<span data-ttu-id="1e20c-108">Questo attributo è valido solo se l'attributo degli [**\_ \_ \_ \_ esempi di dimensioni fisse MF mt**](mf-mt-fixed-size-samples-attribute.md) è **true**.</span><span class="sxs-lookup"><span data-stu-id="1e20c-108">This attribute is valid only if the [**MF\_MT\_FIXED\_SIZE\_SAMPLES**](mf-mt-fixed-size-samples-attribute.md) attribute is **TRUE**.</span></span>

<span data-ttu-id="1e20c-109">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1e20c-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e20c-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e20c-110">Requirements</span></span>



| <span data-ttu-id="1e20c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e20c-111">Requirement</span></span> | <span data-ttu-id="1e20c-112">Valore</span><span class="sxs-lookup"><span data-stu-id="1e20c-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e20c-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e20c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1e20c-114">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1e20c-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1e20c-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e20c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1e20c-116">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="1e20c-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1e20c-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e20c-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e20c-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e20c-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e20c-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e20c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e20c-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1e20c-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1e20c-121">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="1e20c-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1e20c-122">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="1e20c-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="1e20c-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="1e20c-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="1e20c-124">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="1e20c-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




