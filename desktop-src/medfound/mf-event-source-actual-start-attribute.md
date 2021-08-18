---
description: Contiene l'ora di inizio in cui un'origine multimediale viene riavviata dalla posizione corrente.
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: MF_EVENT_SOURCE_ACTUAL_START attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ce39e8a9f90ad0cd7f0cbd590b32719ab10dbd8e498c396e86772ce333e94c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104837"
---
# <a name="mf_event_source_actual_start-attribute"></a>Attributo \_ MF EVENT \_ SOURCE \_ ACTUAL \_ START

Contiene l'ora di inizio in cui un'origine multimediale viene riavviata dalla posizione corrente.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considera come **valore LONGLONG.**

## <a name="remarks"></a>Commenti

Questo attributo viene usato con [l'evento MESourceStarted.](mesourcestarted.md) L'attributo è rilevante quando i dati dell'evento sono vuoti (**VT \_ EMPTY**), che indica che l'origine multimediale è stata avviata dalla posizione di riproduzione corrente. In tal caso, **l'attributo \_ MF EVENT \_ SOURCE ACTUAL \_ \_ START** specifica l'ora di inizio effettiva. Se i dati dell'evento **sono VT \_ EMPTY** e questo attributo non è impostato, si presuppone che l'ora di inizio sia zero.

Quando i [dati dell'evento MESourceStarted](mesourcestarted.md) contengono l'ora di inizio (**VT \_ I8),** questo attributo non deve essere impostato.

Questo attributo è un valore con segno, anche se viene archiviato come **UINT64.**

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

 

 




