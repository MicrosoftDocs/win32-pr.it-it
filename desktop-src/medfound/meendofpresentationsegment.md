---
description: Generato dall'origine del sequencer quando un segmento viene completato ed è seguito da un altro segmento. Al termine del segmento finale, l'origine del sequencer genera un evento MEEndOfPresentation.
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: Evento MEEndOfPresentationSegment (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d3608f51f3ff66e21261cc40d1f8cf690c92c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880265"
---
# <a name="meendofpresentationsegment-event"></a>Evento MEEndOfPresentationSegment

Generato dall'origine del sequencer quando un segmento viene completato ed è seguito da un altro segmento. Al termine del segmento finale, l'origine del sequencer genera un evento [MEEndOfPresentation](meendofpresentation.md) .

La sessione multimediale trasmette questo evento all'applicazione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                                               | Descrizione                                                                          |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**\_ \_ topologia di origine evento MF \_ \_ annullata**](mf-event-source-topology-canceled-attribute.md)<br/> | Specifica se l'origine del sequencer ha annullato il segmento.<br/> <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> <dt>

[Informazioni sull'origine del sequencer](about-the-sequencer-source.md)
</dt> <dt>

[Eventi di origine di Sequencer](sequencer-source-events.md)
</dt> </dl>

 

 




