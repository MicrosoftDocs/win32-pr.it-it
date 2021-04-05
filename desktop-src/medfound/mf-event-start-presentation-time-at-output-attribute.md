---
description: Ora di presentazione in cui i sink dei supporti eseguiranno il rendering del primo campione della nuova topologia.
ms.assetid: 02a8c542-b519-495e-9fb2-8db2f5384db7
title: Attributo MF_EVENT_START_PRESENTATION_TIME_AT_OUTPUT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a588bc6604deed6c6865cd8283390d28e3ffd49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882833"
---
# <a name="mf_event_start_presentation_time_at_output-attribute"></a>\_ \_ \_ \_ Ora di presentazione dell'avvio \_ dell'evento MF all' \_ attributo di output

Ora di presentazione in cui i sink dei supporti eseguiranno il rendering del primo campione della nuova topologia.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considera come valore **LONGLONG** .

## <a name="remarks"></a>Commenti

Se tutti gli oggetti pipeline nella topologia precedente hanno memorizzato nel buffer i dati, questo valore sarà leggermente inferiore al valore nell'attributo dell' [**offset dell'ora di \_ presentazione dell'evento \_ \_ \_ MF**](mf-event-presentation-time-offset-attribute.md) , perché i sink devono eseguire il rendering dei dati memorizzati nel buffer.

Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi dell'evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes:: UINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




