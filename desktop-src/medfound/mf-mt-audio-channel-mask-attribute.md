---
description: In un tipo di supporto audio specifica l'assegnazione dei canali audio alle posizioni del parlante.
ms.assetid: fa5f6baa-0a21-4162-8870-38e71763aba0
title: MF_MT_AUDIO_CHANNEL_MASK attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 544f287ad9cc8addc60245143e079f0ccdd3c1fead043198be93eed59babc98c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955931"
---
# <a name="mf_mt_audio_channel_mask-attribute"></a>Attributo \_ MF MT \_ AUDIO \_ CHANNEL \_ MASK

In un tipo di supporto audio specifica l'assegnazione dei canali audio alle posizioni del parlante.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Il valore di questo attributo è un **OR** bit per bit dei flag seguenti, definiti nel file di intestazione mmreg.h.

<dl> <dt>

<span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**VOCE \_ FRONT \_ LEFT** (0x1)
</dt> <dt>

<span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**VOCE \_ FRONT \_ RIGHT** (0x2)
</dt> <dt>

<span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**VOCE \_ FRONT \_ CENTER** (0x4)
</dt> <dt>

<span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**VOCE \_ FREQUENZA \_ BASSA** (0x8)
</dt> <dt>

<span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**VOCE \_ INDIETRO \_ A SINISTRA** (0x10)
</dt> <dt>

<span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**VOCE \_ BACK \_ RIGHT** (0x20)
</dt> <dt>

<span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**VOCE \_ FRONT \_ LEFT \_ OF \_ CENTER** (0x40)
</dt> <dt>

<span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**VOCE \_ ANTERIORE \_ A \_ DESTRA DEL \_ CENTRO** (0x80)
</dt> <dt>

<span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**VOCE \_ BACK \_ CENTER** (0x100)
</dt> <dt>

<span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**VOCE \_ LATO \_ SINISTRO** (0x200)
</dt> <dt>

<span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**VOCE \_ LATO \_ DESTRO** (0x400)
</dt> <dt>

<span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**VOCE \_ TOP \_ CENTER** (0x800)
</dt> <dt>

<span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**VOCE \_ IN \_ ALTO A \_ SINISTRA** (0x1000)
</dt> <dt>

<span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**VOCE \_ TOP \_ FRONT \_ CENTER** (0x2000)
</dt> <dt>

<span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**VOCE \_ IN \_ ALTO A \_ DESTRA** (0x4000)
</dt> <dt>

<span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**VOCE \_ IN \_ ALTO A \_ SINISTRA** (0x8000)
</dt> <dt>

<span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**VOCE \_ TOP \_ BACK \_ CENTER** (0x10000)
</dt> <dt>

<span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**VOCE \_ IN \_ ALTO A \_ DESTRA** (0x20000)
</dt> </dl>

## <a name="remarks"></a>Commenti

Questo attributo corrisponde al **membro dwChannelMask** della [**struttura WAVEFORMATEXTENSIBLE.**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop Di Vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 \[ \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 
