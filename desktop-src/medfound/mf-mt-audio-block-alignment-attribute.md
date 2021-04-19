---
description: Allineamento del blocco, in byte, per un tipo di supporto audio. L'allineamento del blocco è l'unità atomica minima dei dati per il formato audio.
ms.assetid: 7d304826-ad81-4243-a675-2f55b668b348
title: Attributo MF_MT_AUDIO_BLOCK_ALIGNMENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21efb14cbb89d1773fe9bc3b5ade8d0a50555a1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314037"
---
# <a name="mf_mt_audio_block_alignment-attribute"></a><span data-ttu-id="4a203-104">\_ \_ \_ Attributo allineamento blocchi audio MF mt \_</span><span class="sxs-lookup"><span data-stu-id="4a203-104">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT attribute</span></span>

<span data-ttu-id="4a203-105">Allineamento del blocco, in byte, per un tipo di supporto audio.</span><span class="sxs-lookup"><span data-stu-id="4a203-105">Block alignment, in bytes, for an audio media type.</span></span> <span data-ttu-id="4a203-106">L'allineamento del blocco è l'unità atomica minima dei dati per il formato audio.</span><span class="sxs-lookup"><span data-stu-id="4a203-106">The block alignment is the minimum atomic unit of data for the audio format.</span></span>

## <a name="data-type"></a><span data-ttu-id="4a203-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4a203-107">Data type</span></span>

<span data-ttu-id="4a203-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4a203-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4a203-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a203-109">Remarks</span></span>

<span data-ttu-id="4a203-110">Per i formati audio PCM, l'allineamento del blocco è uguale al numero di canali audio moltiplicato per il numero di byte per esempio audio.</span><span class="sxs-lookup"><span data-stu-id="4a203-110">For PCM audio formats, the block alignment is equal to the number of audio channels multiplied by the number of bytes per audio sample.</span></span>

<span data-ttu-id="4a203-111">Questo attributo corrisponde al membro **nBlockAlign** della struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4a203-111">This attribute corresponds to the **nBlockAlign** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="4a203-112">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4a203-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a203-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a203-113">Requirements</span></span>



| <span data-ttu-id="4a203-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a203-114">Requirement</span></span> | <span data-ttu-id="4a203-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4a203-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a203-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a203-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4a203-117">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4a203-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="4a203-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a203-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4a203-119">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="4a203-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4a203-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a203-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a203-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a203-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a203-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a203-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a203-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4a203-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4a203-124">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="4a203-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4a203-125">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="4a203-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="4a203-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="4a203-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="4a203-127">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="4a203-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
