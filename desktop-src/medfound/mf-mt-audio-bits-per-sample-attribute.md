---
description: Numero di bit per campione audio in un tipo di supporto audio.
ms.assetid: d78a8c4d-377e-45eb-9cf6-2d61b34e82d6
title: MF_MT_AUDIO_BITS_PER_SAMPLE attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9697ff5ce97bc7dd9066b57f94e41ff02a599fcf14d1ea8f51c9dea69efc7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104557"
---
# <a name="mf_mt_audio_bits_per_sample-attribute"></a>MF \_ MT \_ AUDIO \_ BITS PER ATTRIBUTO \_ \_ SAMPLE

Numero di bit per campione audio in un tipo di supporto audio.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo corrisponde al **membro wBitsPerSample** della [**struttura WAVEFORMATEX.**](/previous-versions/dd757713(v=vs.85))

Se alcuni bit contengono spaziatura interna, impostare l'attributo [**MF \_ MT AUDIO VALID \_ \_ \_ BITS PER \_ \_ SAMPLE**](mf-mt-audio-valid-bits-per-sample-attribute.md) per specificare il numero di bit di dati audio validi in ogni esempio.

Se l'audio contiene 8 bit per campione, gli esempi audio sono valori senza segno. Ogni campione audio ha un intervallo compreso tra 0 e 255. Se l'audio contiene 16 bit per campione o versione successiva, i campioni audio sono valori firmati.

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

 

 
