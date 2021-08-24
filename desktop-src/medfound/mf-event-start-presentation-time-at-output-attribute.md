---
description: Ora di presentazione in cui i sink multimediali eseguiranno il rendering del primo esempio della nuova topologia.
ms.assetid: 02a8c542-b519-495e-9fb2-8db2f5384db7
title: MF_EVENT_START_PRESENTATION_TIME_AT_OUTPUT attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd5949a73244eec26fb0390805c11f630291a470b2016b5a3575311261b72a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723181"
---
# <a name="mf_event_start_presentation_time_at_output-attribute"></a>Attributo MF \_ EVENT START PRESENTATION TIME AT \_ \_ \_ \_ \_ OUTPUT

Ora di presentazione in cui i sink multimediali eseguiranno il rendering del primo esempio della nuova topologia.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considerare come **valore LONGLONG.**

## <a name="remarks"></a>Commenti

Se sono presenti oggetti pipeline nei dati memorizzati nel buffer della topologia precedente, questo valore sarà leggermente inferiore al valore nell'attributo [**MF \_ EVENT PRESENTATION \_ TIME \_ \_ OFFSET,**](mf-event-presentation-time-offset-attribute.md) perché i sink devono eseguire il rendering dei dati memorizzati nel buffer.

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

 

 




