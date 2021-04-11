---
description: Numero medio di byte al secondo in un tipo di supporto audio.
ms.assetid: 0ee371fb-d980-44de-a9bd-201e2b72e874
title: Attributo MF_MT_AUDIO_AVG_BYTES_PER_SECOND (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca86276e816ea1ef058946bad29f1565fe1c841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232137"
---
# <a name="mf_mt_audio_avg_bytes_per_second-attribute"></a>\_Attributo MF mt \_ audio \_ media \_ bytes \_ al \_ secondo

Numero medio di byte al secondo in un tipo di supporto audio.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo corrisponde al membro **nAvgBytesPerSec** della struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

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

 

 
