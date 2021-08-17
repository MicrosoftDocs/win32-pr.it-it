---
description: Specifica se l'origine sequencer ha annullato una topologia.
ms.assetid: b7252336-1612-43fc-8f08-1fdfdbb293eb
title: MF_EVENT_SOURCE_TOPOLOGY_CANCELED attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef612c8a1081ecc26eaa9dc593a5906ff965d0387ab02490eedd68f7fbf5e813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060658"
---
# <a name="mf_event_source_topology_canceled-attribute"></a>Attributo MF \_ EVENT \_ SOURCE \_ TOPOLOGY \_ CANCELED

Specifica se [l'origine sequencer](sequencer-source.md) ha annullato una topologia.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo viene usato con gli eventi seguenti:

-   [MEEndOfPresentationSegment](meendofpresentationsegment.md)
-   [MEEndOfPresentation](meendofpresentation.md)

Se questo attributo è presente e diverso da zero, significa che il segmento di presentazione è terminato perché l'origine sequencer ha annullato la topologia. In caso contrario, il segmento di presentazione termina normalmente.

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Eventi di origine sequencer](sequencer-source-events.md)
</dt> </dl>

 

 




