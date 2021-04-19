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
# <a name="mf_mt_audio_block_alignment-attribute"></a>\_ \_ \_ Attributo allineamento blocchi audio MF mt \_

Allineamento del blocco, in byte, per un tipo di supporto audio. L'allineamento del blocco è l'unità atomica minima dei dati per il formato audio.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Per i formati audio PCM, l'allineamento del blocco è uguale al numero di canali audio moltiplicato per il numero di byte per esempio audio.

Questo attributo corrisponde al membro **nBlockAlign** della struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

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

 

 
