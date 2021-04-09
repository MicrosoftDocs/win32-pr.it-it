---
description: Tempo di presentazione per un esempio di cui è stato eseguito il rendering durante lo scrubbing.
ms.assetid: 6ce52cf5-014b-49a2-abf7-2c9cc5340a42
title: Attributo MF_EVENT_SCRUBSAMPLE_TIME (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7c4fb1a8015367fa3d48edb066cdb135983926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967044"
---
# <a name="mf_event_scrubsample_time-attribute"></a>\_ \_ Attributo tempo SCRUBSAMPLE evento MF \_

Tempo di presentazione per un esempio di cui è stato eseguito il rendering durante lo scrubbing.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considera come valore **LONGLONG** .

## <a name="remarks"></a>Commenti

Questo attributo viene utilizzato con l'evento [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) .

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

 

 




