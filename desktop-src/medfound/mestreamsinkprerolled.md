---
description: Generato da un sink del flusso quando il flusso ha ricevuto un numero sufficiente di dati di pre-roll per avviare il rendering. Questo evento viene generato dai sink di supporto che supportano l'interfaccia IMFMediaSinkPreroll.
ms.assetid: 1ecb1805-73ce-4741-b969-6eb88982ee26
title: Evento MEStreamSinkPrerolled (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312daa90c995ccbbe8667cfa5acdf47975248474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754290"
---
# <a name="mestreamsinkprerolled-event"></a>Evento MEStreamSinkPrerolled

Generato da un sink del flusso quando il flusso ha ricevuto un numero sufficiente di dati di pre-roll per avviare il rendering. Questo evento viene generato dai sink di supporto che supportano l'interfaccia [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) .

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

 

 




