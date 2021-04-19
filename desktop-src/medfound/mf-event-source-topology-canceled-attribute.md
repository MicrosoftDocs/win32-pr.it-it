---
description: Specifica se l'origine del sequencer ha annullato una topologia.
ms.assetid: b7252336-1612-43fc-8f08-1fdfdbb293eb
title: Attributo MF_EVENT_SOURCE_TOPOLOGY_CANCELED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a161aec292d834b0418f59f1c26ea2f11a538e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319610"
---
# <a name="mf_event_source_topology_canceled-attribute"></a>\_Attributo per \_ la \_ topologia di origine eventi MF \_

Specifica se l' [origine del sequencer](sequencer-source.md) ha annullato una topologia.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo viene usato con gli eventi seguenti:

-   [MEEndOfPresentationSegment](meendofpresentationsegment.md)
-   [MEEndOfPresentation](meendofpresentation.md)

Se questo attributo è presente e diverso da zero, significa che il segmento di presentazione è stato terminato perché l'origine del sequencer ha annullato la topologia. In caso contrario, il segmento di presentazione termina normalmente.

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

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Eventi di origine di Sequencer](sequencer-source-events.md)
</dt> </dl>

 

 




