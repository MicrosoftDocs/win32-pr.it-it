---
description: Numero di bit validi di dati audio in ogni esempio audio.
ms.assetid: b5b97700-c98a-4394-a184-661852add0b4
title: Attributo MF_MT_AUDIO_VALID_BITS_PER_SAMPLE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4e5efb41bf3b79d4feded2872b601eea43723a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349921"
---
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a><span data-ttu-id="2d8e1-103">\_ \_ Bit validi per l'audio MF mt \_ \_ \_ per ogni \_ attributo di esempio</span><span class="sxs-lookup"><span data-stu-id="2d8e1-103">MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="2d8e1-104">Numero di bit validi di dati audio in ogni esempio audio.</span><span class="sxs-lookup"><span data-stu-id="2d8e1-104">Number of valid bits of audio data in each audio sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="2d8e1-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2d8e1-105">Data type</span></span>

<span data-ttu-id="2d8e1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2d8e1-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2d8e1-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d8e1-107">Remarks</span></span>

<span data-ttu-id="2d8e1-108">Per i formati audio che contengono spaziatura interna dopo ogni esempio di audio, viene usato l'attributo di **\_ bit valido di MF mt \_ \_ \_ \_ per \_ esempio** .</span><span class="sxs-lookup"><span data-stu-id="2d8e1-108">The **MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE** attribute is used for audio formats that contain padding after each audio sample.</span></span> <span data-ttu-id="2d8e1-109">La dimensione totale di ogni esempio di audio, inclusi i bit di riempimento, viene fornita nell'attributo [**\_ \_ \_ bit audio \_ per \_ campione MF mt**](mf-mt-audio-bits-per-sample-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="2d8e1-109">The total size of each audio sample, including padding bits, is given in the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute.</span></span>

<span data-ttu-id="2d8e1-110">Se il valore di **\_ bit validi per l'attributo MF mt \_ audio \_ \_ \_ per \_ esempio** non è impostato, usare l'attributo [**\_ bit MF mt \_ audio bits per \_ \_ \_ esempio**](mf-mt-audio-bits-per-sample-attribute.md) per trovare il numero di bit validi per campione.</span><span class="sxs-lookup"><span data-stu-id="2d8e1-110">If the **MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE** attribute is not set, use the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute to find the number of valid bits per sample.</span></span>

<span data-ttu-id="2d8e1-111">Se un formato audio non contiene bit di spaziatura interna, questo attributo non deve essere impostato oppure deve essere impostato sullo stesso valore di [**MF \_ mt \_ audio \_ bits \_ per ogni \_**](mf-mt-audio-bits-per-sample-attribute.md) attributo di esempio.</span><span class="sxs-lookup"><span data-stu-id="2d8e1-111">If an audio format does not contain any padding bits, then this attribute should not be set, or should be set to the same value as the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute.</span></span>

<span data-ttu-id="2d8e1-112">Questo attributo corrisponde al membro **wValidBitsPerSample** della struttura [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) .</span><span class="sxs-lookup"><span data-stu-id="2d8e1-112">This attribute corresponds to the **wValidBitsPerSample** member of the [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) structure.</span></span>

<span data-ttu-id="2d8e1-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="2d8e1-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d8e1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d8e1-114">Requirements</span></span>



| <span data-ttu-id="2d8e1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d8e1-115">Requirement</span></span> | <span data-ttu-id="2d8e1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2d8e1-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2d8e1-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d8e1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2d8e1-118">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2d8e1-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="2d8e1-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d8e1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2d8e1-120">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="2d8e1-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2d8e1-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d8e1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d8e1-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d8e1-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d8e1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d8e1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d8e1-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2d8e1-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2d8e1-125">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="2d8e1-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="2d8e1-126">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="2d8e1-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="2d8e1-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="2d8e1-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="2d8e1-128">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="2d8e1-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
