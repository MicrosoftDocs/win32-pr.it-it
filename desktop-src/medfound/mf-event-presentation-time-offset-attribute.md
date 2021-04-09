---
description: Offset tra l'ora di presentazione e i timestamp dei sorgenti multimediali.
ms.assetid: 450f3c39-063e-4bf3-838a-0f7c240d6647
title: Attributo MF_EVENT_PRESENTATION_TIME_OFFSET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030d9d10eb5daf4fa1c920ad027397710b937881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879602"
---
# <a name="mf_event_presentation_time_offset-attribute"></a>\_ \_ \_ Attributo offset ora presentazione evento MF \_

Offset tra l'ora di presentazione e i timestamp dell'origine multimediale.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

L'offset viene calcolato come segue: offset = tempo di presentazione-ora di origine. Questo attributo viene usato con gli eventi seguenti:

-   [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md)
-   [MESessionStarted](mesessionstarted.md)

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

 

 




