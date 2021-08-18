---
description: Specifica la struttura di formato legacy preferita da usare per la conversione di un tipo di supporto audio.
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: MF_MT_AUDIO_PREFER_WAVEFORMATEX attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23e2aeb00e2967b3f031a2aafe3a01f3846d7db077ba344a59680508bd385fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035299"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a>Attributo MF \_ MT \_ AUDIO PREFER \_ \_ WAVEFORMATEX

Specifica la struttura di formato legacy preferita da usare per la conversione di un tipo di supporto audio.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo fornisce un suggerimento alla [**funzione MFCreateWaveFormatExFromMFMediaType.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) Se l'attributo è **TRUE,** la funzione converte il tipo di supporto audio in una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) quando possibile, anziché convertirlo in una [**struttura WAVEFORMATEXTENSIBLE.**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))

La [**funzione MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) imposta questo attributo. È possibile eseguire l'override del valore di questo attributo, ma l'impostazione di questo attributo su **TRUE** non garantisce che un tipo di supporto audio possa essere convertito in [**formato WAVEFORMATEX.**](/previous-versions/dd757713(v=vs.85))

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 \[ \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 
