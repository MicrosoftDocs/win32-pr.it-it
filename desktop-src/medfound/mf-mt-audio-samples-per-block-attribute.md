---
description: Numero di campioni audio contenuti in un blocco compresso di dati audio. Questo attributo può essere usato in formati audio compressi con un numero fisso di campioni all'interno di ogni blocco.
ms.assetid: 6ae31548-4d78-4e38-9cfc-01b611a6022d
title: Attributo MF_MT_AUDIO_SAMPLES_PER_BLOCK (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c453fa4daeaa310b5e41add44b63b0fb45372d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315036"
---
# <a name="mf_mt_audio_samples_per_block-attribute"></a><span data-ttu-id="a35ca-104">\_ \_ Esempi audio MF \_ mt \_ per \_ blocco</span><span class="sxs-lookup"><span data-stu-id="a35ca-104">MF\_MT\_AUDIO\_SAMPLES\_PER\_BLOCK attribute</span></span>

<span data-ttu-id="a35ca-105">Numero di campioni audio contenuti in un blocco compresso di dati audio.</span><span class="sxs-lookup"><span data-stu-id="a35ca-105">Number of audio samples contained in one compressed block of audio data.</span></span> <span data-ttu-id="a35ca-106">Questo attributo può essere usato in formati audio compressi con un numero fisso di campioni all'interno di ogni blocco.</span><span class="sxs-lookup"><span data-stu-id="a35ca-106">This attribute can be used in compressed audio formats that have a fixed number of samples within each block.</span></span>

## <a name="data-type"></a><span data-ttu-id="a35ca-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a35ca-107">Data type</span></span>

<span data-ttu-id="a35ca-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a35ca-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a35ca-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="a35ca-109">Remarks</span></span>

<span data-ttu-id="a35ca-110">Questo attributo corrisponde al membro **wSamplesPerBlock** della struttura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a35ca-110">This attribute corresponds to the **wSamplesPerBlock** member of the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span>

<span data-ttu-id="a35ca-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a35ca-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a35ca-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a35ca-112">Requirements</span></span>



| <span data-ttu-id="a35ca-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a35ca-113">Requirement</span></span> | <span data-ttu-id="a35ca-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a35ca-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a35ca-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a35ca-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a35ca-116">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a35ca-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a35ca-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a35ca-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a35ca-118">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="a35ca-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a35ca-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a35ca-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a35ca-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a35ca-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a35ca-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a35ca-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a35ca-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a35ca-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a35ca-123">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="a35ca-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a35ca-124">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="a35ca-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a35ca-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a35ca-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a35ca-126">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="a35ca-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
