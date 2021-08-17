---
description: Numero di bit validi di dati audio in ogni campione audio.
ms.assetid: b5b97700-c98a-4394-a184-661852add0b4
title: MF_MT_AUDIO_VALID_BITS_PER_SAMPLE attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f84fa3938e4d74473da70bd28e5ccbb1bab71441c694b670cdb8b54bead31c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973580"
---
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a>MF \_ MT AUDIO VALID \_ \_ \_ BITS PER SAMPLE \_ \_ ATTRIBUTE

Numero di bit validi di dati audio in ogni campione audio.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

**L'attributo \_ MF MT AUDIO VALID \_ \_ \_ BITS PER \_ \_ SAMPLE** viene usato per i formati audio che contengono spaziatura interna dopo ogni campione audio. Le dimensioni totali di ogni campione audio, inclusi i bit di riempimento, sono specificate nell'attributo [**\_ MF MT \_ AUDIO \_ BITS \_ PER \_ SAMPLE.**](mf-mt-audio-bits-per-sample-attribute.md)

Se **l'attributo MF \_ MT \_ AUDIO VALID \_ \_ BITS PER \_ \_ SAMPLE** non è impostato, usare l'attributo [**MF MT AUDIO \_ \_ \_ BITS PER \_ \_ SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) per trovare il numero di bit validi per campione.

Se un formato audio non contiene bit di riempimento, questo attributo non deve essere impostato o deve essere impostato sullo stesso valore dell'attributo [**\_ MF MT \_ AUDIO \_ BITS \_ PER \_ SAMPLE.**](mf-mt-audio-bits-per-sample-attribute.md)

Questo attributo corrisponde al **membro wValidBitsPerSample** della [**struttura WAVEFORMATEXTENSIBLE.**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible)

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

 

 
