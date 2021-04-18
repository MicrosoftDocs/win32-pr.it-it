---
description: Generato dai sink di flusso del renderer video avanzato (EVR) se il dispositivo video viene modificato.
ms.assetid: 5b663d6b-5df8-4321-a6a5-a21b9810065a
title: Evento MEStreamSinkDeviceChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 651fc34a56ca52cfb9e0b3f20e6e4d6b5366f541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307994"
---
# <a name="mestreamsinkdevicechanged-event"></a>Evento MEStreamSinkDeviceChanged

Generato dai sink di flusso del renderer video avanzato (EVR) se il dispositivo video viene modificato. Ad esempio, EVR genera questo evento quando riceve un evento di [**\_ \_ modifica della visualizzazione EC**](../directshow/ec-display-changed.md) .

La pipeline Media Foundation risponde a questo evento inviando nuovamente tutte le richieste di esempio non riuscite durante la modifica del dispositivo.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/> |



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

[Sink di supporti](media-sinks.md)
</dt> </dl>

 

 
