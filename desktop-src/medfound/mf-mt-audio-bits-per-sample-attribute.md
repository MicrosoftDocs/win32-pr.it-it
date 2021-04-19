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
# <a name="mf_mt_audio_bits_per_sample-attribute"></a>\_ \_ Bit audio MF \_ mt \_ per \_ attributo di esempio

Numero di bit per esempio audio in un tipo di supporto audio.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo corrisponde al membro **wBitsPerSample** della struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

Se alcuni bit contengono spaziatura interna, impostare l'attributo [**MF \_ mt \_ audio \_ valid \_ bit \_ per \_ Sample**](mf-mt-audio-valid-bits-per-sample-attribute.md) per specificare il numero di bit di dati audio validi in ogni esempio.

Se l'audio contiene 8 bit per campione, gli esempi audio sono valori senza segno. (Ogni campione audio ha un intervallo compreso tra 0 e 255). Se l'audio contiene 16 bit per campione o superiore, gli esempi audio sono valori con segno.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                              |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 
