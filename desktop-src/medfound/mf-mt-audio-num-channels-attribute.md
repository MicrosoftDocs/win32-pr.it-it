---
description: Numero di canali audio in un tipo di supporto audio.
ms.assetid: 524283fb-d046-4f8c-a30f-4fe7ddb43174
title: Attributo MF_MT_AUDIO_NUM_CHANNELS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09020ef540b6a3b02eecc6a6d788c18d07358ce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314032"
---
# <a name="mf_mt_audio_num_channels-attribute"></a>\_Attributo MF mt \_ audio \_ num \_ Channels

Numero di canali audio in un tipo di supporto audio.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo corrisponde al membro **nChannels** della struttura [WAVEFORMATEX](mf-mt-audio-prefer-waveformatex-attribute.md) .

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

 

 




