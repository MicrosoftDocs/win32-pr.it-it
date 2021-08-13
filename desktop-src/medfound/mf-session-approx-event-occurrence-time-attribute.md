---
description: Ora approssimativa in cui la sessione multimediale ha generato un evento.
ms.assetid: 58083bc8-59cc-4503-8fae-36fcd864921a
title: MF_SESSION_APPROX_EVENT_OCCURRENCE_TIME attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce6cbaa7d12cebe14b015c4d568b36b081930ef4b302797dba76fc728e92cf01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740025"
---
# <a name="mf_session_approx_event_occurrence_time-attribute"></a>Attributo MF \_ SESSION \_ APPROX \_ EVENT OCCURRENCE \_ \_ TIME

Ora approssimativa in cui la sessione multimediale ha generato un evento.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considerare come **valore LONGLONG.**

## <a name="remarks"></a>Commenti

Alcuni eventi della sessione multimediale hanno questo attributo. Il valore indica l'ora approssimativa di presentazione in cui è stato generato l'evento.

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

 

 




