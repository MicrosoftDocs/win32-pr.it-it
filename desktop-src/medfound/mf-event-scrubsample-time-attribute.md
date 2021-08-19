---
description: Ora di presentazione per un esempio di cui è stato eseguito il rendering durante lo scrubbing.
ms.assetid: 6ce52cf5-014b-49a2-abf7-2c9cc5340a42
title: MF_EVENT_SCRUBSAMPLE_TIME attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a57045fcf5fd4faf20d2207778b91aa8ff0fd959dd42571882a21b5a1dceacba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104817"
---
# <a name="mf_event_scrubsample_time-attribute"></a>Attributo MF \_ EVENT \_ SCRUBSAMPLE \_ TIME

Ora di presentazione per un esempio di cui è stato eseguito il rendering durante lo scrubbing.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considerare come **valore LONGLONG.**

## <a name="remarks"></a>Commenti

Questo attributo viene usato con [l'evento MEStreamSinkScrubSampleComplete.](mestreamsinkscrubsamplecomplete.md)

Questo attributo è un valore con segno, anche se viene archiviato come **UINT64.**

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi dell'evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




