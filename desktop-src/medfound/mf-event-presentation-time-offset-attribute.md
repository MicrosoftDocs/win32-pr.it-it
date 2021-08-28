---
description: Offset tra l'ora di presentazione e i timestamp delle origini multimediali.
ms.assetid: 450f3c39-063e-4bf3-838a-0f7c240d6647
title: MF_EVENT_PRESENTATION_TIME_OFFSET attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5ff2285bc624d42f17d4662cf93e3f46a65fcbef465e731874ef255c40c076d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013081"
---
# <a name="mf_event_presentation_time_offset-attribute"></a>Attributo MF \_ EVENT \_ PRESENTATION TIME \_ \_ OFFSET

Offset tra l'ora di presentazione e i timestamp dell'origine multimediale.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

L'offset viene calcolato come segue: offset = tempo di presentazione - ora di origine. Questo attributo viene usato con gli eventi seguenti:

-   [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md)
-   [MESessionStarted](mesessionstarted.md)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi dell'evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




