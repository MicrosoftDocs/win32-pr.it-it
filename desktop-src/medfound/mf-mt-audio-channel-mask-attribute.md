---
description: In un tipo di supporto audio, specifica l'assegnazione dei canali audio alle posizioni del relatore.
ms.assetid: fa5f6baa-0a21-4162-8870-38e71763aba0
title: Attributo MF_MT_AUDIO_CHANNEL_MASK (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5293f5387a2c293b97ee32db54fcfb3f3ff304d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049710"
---
# <a name="mf_mt_audio_channel_mask-attribute"></a><span data-ttu-id="152d9-103">\_Attributo della \_ \_ maschera di canale audio MF mt \_</span><span class="sxs-lookup"><span data-stu-id="152d9-103">MF\_MT\_AUDIO\_CHANNEL\_MASK attribute</span></span>

<span data-ttu-id="152d9-104">In un tipo di supporto audio, specifica l'assegnazione dei canali audio alle posizioni del relatore.</span><span class="sxs-lookup"><span data-stu-id="152d9-104">In an audio media type, specifies the assignment of audio channels to speaker positions.</span></span>

## <a name="data-type"></a><span data-ttu-id="152d9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="152d9-105">Data type</span></span>

<span data-ttu-id="152d9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="152d9-106">**UINT32**</span></span>

<span data-ttu-id="152d9-107">Il valore di questo attributo è **un operatore OR** bit per bit dei flag seguenti, definiti nel file di intestazione mmreg. h.</span><span class="sxs-lookup"><span data-stu-id="152d9-107">The value of this attribute is a bitwise **OR** of the following flags, which are defined in the header file mmreg.h.</span></span>

<dl> <dt>

<span data-ttu-id="152d9-108"><span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**Relatore \_ FRONT- \_ Left** (0x1)</span><span class="sxs-lookup"><span data-stu-id="152d9-108"><span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**SPEAKER\_FRONT\_LEFT** (0x1)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-109"><span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**Relatore \_ ANTERIORE \_ destro** (0x2)</span><span class="sxs-lookup"><span data-stu-id="152d9-109"><span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**SPEAKER\_FRONT\_RIGHT** (0x2)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-110"><span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**Relatore \_ \_Centro front** (0x4)</span><span class="sxs-lookup"><span data-stu-id="152d9-110"><span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**SPEAKER\_FRONT\_CENTER** (0x4)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-111"><span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**Relatore \_ \_Frequenza bassa** (0x8)</span><span class="sxs-lookup"><span data-stu-id="152d9-111"><span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**SPEAKER\_LOW\_FREQUENCY** (0x8)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-112"><span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**Relatore \_ INDIETRO a \_ sinistra** (0x10)</span><span class="sxs-lookup"><span data-stu-id="152d9-112"><span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**SPEAKER\_BACK\_LEFT** (0x10)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-113"><span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**Relatore \_ INDIETRO a \_ destra** (0x20)</span><span class="sxs-lookup"><span data-stu-id="152d9-113"><span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**SPEAKER\_BACK\_RIGHT** (0x20)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-114"><span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**Relatore \_ Parte anteriore \_ sinistra \_ del \_ centro** (0x40)</span><span class="sxs-lookup"><span data-stu-id="152d9-114"><span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**SPEAKER\_FRONT\_LEFT\_OF\_CENTER** (0x40)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-115"><span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**Relatore \_ Parte anteriore \_ destra \_ di \_ Center** (0x80)</span><span class="sxs-lookup"><span data-stu-id="152d9-115"><span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**SPEAKER\_FRONT\_RIGHT\_OF\_CENTER** (0x80)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-116"><span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**Relatore \_ \_Centro back** (0x100)</span><span class="sxs-lookup"><span data-stu-id="152d9-116"><span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**SPEAKER\_BACK\_CENTER** (0x100)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-117"><span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**Relatore \_ LATO \_ sinistro** (0x200)</span><span class="sxs-lookup"><span data-stu-id="152d9-117"><span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**SPEAKER\_SIDE\_LEFT** (0x200)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-118"><span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**Relatore \_ LATO \_ destro** (0x400)</span><span class="sxs-lookup"><span data-stu-id="152d9-118"><span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**SPEAKER\_SIDE\_RIGHT** (0x400)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-119"><span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**Relatore \_ In alto al \_ centro** (0x800)</span><span class="sxs-lookup"><span data-stu-id="152d9-119"><span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**SPEAKER\_TOP\_CENTER** (0x800)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-120"><span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**Relatore \_ Parte \_ superiore \_ sinistra** (0x1000)</span><span class="sxs-lookup"><span data-stu-id="152d9-120"><span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**SPEAKER\_TOP\_FRONT\_LEFT** (0x1000)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-121"><span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**Relatore \_ TOP \_ front \_ Center** (0x2000)</span><span class="sxs-lookup"><span data-stu-id="152d9-121"><span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**SPEAKER\_TOP\_FRONT\_CENTER** (0x2000)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-122"><span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**Relatore \_ In alto a \_ \_ destra** (0x4000)</span><span class="sxs-lookup"><span data-stu-id="152d9-122"><span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**SPEAKER\_TOP\_FRONT\_RIGHT** (0x4000)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-123"><span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**Relatore \_ Parte \_ superiore \_ sinistra** (0x8000)</span><span class="sxs-lookup"><span data-stu-id="152d9-123"><span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**SPEAKER\_TOP\_BACK\_LEFT** (0x8000)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-124"><span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**Relatore \_ TOP \_ back \_ Center** (0x10000)</span><span class="sxs-lookup"><span data-stu-id="152d9-124"><span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**SPEAKER\_TOP\_BACK\_CENTER** (0x10000)</span></span>
</dt> <dt>

<span data-ttu-id="152d9-125"><span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**Relatore \_ TOP \_ back \_ right** (0x20000)</span><span class="sxs-lookup"><span data-stu-id="152d9-125"><span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**SPEAKER\_TOP\_BACK\_RIGHT** (0x20000)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="152d9-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="152d9-126">Remarks</span></span>

<span data-ttu-id="152d9-127">Questo attributo corrisponde al membro **dwChannelMask** della struttura [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) .</span><span class="sxs-lookup"><span data-stu-id="152d9-127">This attribute corresponds to the **dwChannelMask** member of the [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) structure.</span></span>

<span data-ttu-id="152d9-128">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="152d9-128">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="152d9-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="152d9-129">Requirements</span></span>



| <span data-ttu-id="152d9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="152d9-130">Requirement</span></span> | <span data-ttu-id="152d9-131">Valore</span><span class="sxs-lookup"><span data-stu-id="152d9-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="152d9-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="152d9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="152d9-133">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="152d9-133">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="152d9-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="152d9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="152d9-135">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="152d9-135">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="152d9-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="152d9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="152d9-137"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="152d9-137"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="152d9-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="152d9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152d9-139">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="152d9-139">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="152d9-140">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="152d9-140">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="152d9-141">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="152d9-141">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="152d9-142">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="152d9-142">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="152d9-143">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="152d9-143">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
