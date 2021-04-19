---
description: Numero di bit per esempio audio in un tipo di supporto audio.
ms.assetid: d78a8c4d-377e-45eb-9cf6-2d61b34e82d6
title: Attributo MF_MT_AUDIO_BITS_PER_SAMPLE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 896e77c937269b63208cb4bff73482a8df8596aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309555"
---
# <a name="mf_mt_audio_bits_per_sample-attribute"></a><span data-ttu-id="60a68-103">\_ \_ Bit audio MF \_ mt \_ per \_ attributo di esempio</span><span class="sxs-lookup"><span data-stu-id="60a68-103">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="60a68-104">Numero di bit per esempio audio in un tipo di supporto audio.</span><span class="sxs-lookup"><span data-stu-id="60a68-104">Number of bits per audio sample in an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="60a68-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="60a68-105">Data type</span></span>

<span data-ttu-id="60a68-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="60a68-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="60a68-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="60a68-107">Remarks</span></span>

<span data-ttu-id="60a68-108">Questo attributo corrisponde al membro **wBitsPerSample** della struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="60a68-108">This attribute corresponds to the **wBitsPerSample** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="60a68-109">Se alcuni bit contengono spaziatura interna, impostare l'attributo [**MF \_ mt \_ audio \_ valid \_ bit \_ per \_ Sample**](mf-mt-audio-valid-bits-per-sample-attribute.md) per specificare il numero di bit di dati audio validi in ogni esempio.</span><span class="sxs-lookup"><span data-stu-id="60a68-109">If some bits contain padding, set the [**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**](mf-mt-audio-valid-bits-per-sample-attribute.md) attribute to specify the number of bits of valid audio data in each sample.</span></span>

<span data-ttu-id="60a68-110">Se l'audio contiene 8 bit per campione, gli esempi audio sono valori senza segno.</span><span class="sxs-lookup"><span data-stu-id="60a68-110">If the audio contains 8 bits per sample, the audio samples are unsigned values.</span></span> <span data-ttu-id="60a68-111">(Ogni campione audio ha un intervallo compreso tra 0 e 255). Se l'audio contiene 16 bit per campione o superiore, gli esempi audio sono valori con segno.</span><span class="sxs-lookup"><span data-stu-id="60a68-111">(Each audio sample has the range 0–255.) If the audio contains 16 bits per sample or higher, the audio samples are signed values.</span></span>

<span data-ttu-id="60a68-112">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="60a68-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="60a68-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60a68-113">Requirements</span></span>



| <span data-ttu-id="60a68-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="60a68-114">Requirement</span></span> | <span data-ttu-id="60a68-115">Valore</span><span class="sxs-lookup"><span data-stu-id="60a68-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60a68-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60a68-116">Minimum supported client</span></span><br/> | <span data-ttu-id="60a68-117">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="60a68-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="60a68-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60a68-118">Minimum supported server</span></span><br/> | <span data-ttu-id="60a68-119">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="60a68-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="60a68-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60a68-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="60a68-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="60a68-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60a68-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60a68-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60a68-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="60a68-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="60a68-124">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="60a68-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="60a68-125">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="60a68-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="60a68-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="60a68-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="60a68-127">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="60a68-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
