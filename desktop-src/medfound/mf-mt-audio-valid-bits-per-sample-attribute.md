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
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a>\_ \_ Bit validi per l'audio MF mt \_ \_ \_ per ogni \_ attributo di esempio

Numero di bit validi di dati audio in ogni esempio audio.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Per i formati audio che contengono spaziatura interna dopo ogni esempio di audio, viene usato l'attributo di **\_ bit valido di MF mt \_ \_ \_ \_ per \_ esempio** . La dimensione totale di ogni esempio di audio, inclusi i bit di riempimento, viene fornita nell'attributo [**\_ \_ \_ bit audio \_ per \_ campione MF mt**](mf-mt-audio-bits-per-sample-attribute.md) .

Se il valore di **\_ bit validi per l'attributo MF mt \_ audio \_ \_ \_ per \_ esempio** non è impostato, usare l'attributo [**\_ bit MF mt \_ audio bits per \_ \_ \_ esempio**](mf-mt-audio-bits-per-sample-attribute.md) per trovare il numero di bit validi per campione.

Se un formato audio non contiene bit di spaziatura interna, questo attributo non deve essere impostato oppure deve essere impostato sullo stesso valore di [**MF \_ mt \_ audio \_ bits \_ per ogni \_**](mf-mt-audio-bits-per-sample-attribute.md) attributo di esempio.

Questo attributo corrisponde al membro **wValidBitsPerSample** della struttura [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) .

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

 

 
