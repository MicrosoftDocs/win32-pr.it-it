---
description: Offset tra il timestamp di ogni campione ricevuto dal grabber di esempio e l'ora in cui il campione grabber presenta l'esempio.
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad8086d7820a9f7c642fb049af8696521f675be3f7606ff19166a4570ee8000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875991"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a>Attributo MF \_ SAMPLEGRABBERSINK \_ SAMPLE \_ TIME \_ OFFSET

Offset tra il timestamp di ogni campione ricevuto dal grabber di esempio e l'ora in cui il campione grabber presenta l'esempio.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

È possibile impostare questo attributo [**sull'oggetto IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituito dalla [**funzione MFCreateSampleGrabberSinkActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) Questo attributo consente alla funzione di callback di grabber di esempio di ricevere esempi prima dell'ora di presentazione.

Quando il grabber di esempio riceve un nuovo esempio, presenta l'esempio in fase *t* - *offset*, dove *t* è il timestamp del campione e *offset* è il valore di questo attributo. Se questo attributo non è impostato, il valore predefinito è zero.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**IMFSampleGrabberSinkCallback**](/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback)
</dt> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> </dl>

 

 




