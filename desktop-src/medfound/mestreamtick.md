---
description: Segnala che in un flusso multimediale non sono disponibili dati in un momento specificato.
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: Evento MEStreamTick (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42b72a61964e296ac5f7aa69eb2be6773b622f7b44df8300affa0150af2f8a77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974060"
---
# <a name="mestreamtick-event"></a>EVENTO MEStreamTick

Segnala che in un flusso multimediale non sono disponibili dati in un momento specificato.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE           | Descrizione                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| VT \_ I8<br/> | Ora in cui si verifica il gap, in unità di 100 nanosecondi.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento segnala una lacune nei dati. L'evento notifica ai componenti downstream di non prevedere dati all'ora specificata.

L'evento deve essere inviato da qualsiasi oggetto che genera i timestamp per i campioni multimediali nel flusso. A seconda del formato dei dati, è possibile:

-   Flusso multimediale nell'origine multimediale [**(interfaccia IMFMediaStream)**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) o
-   Trasformazione del decodificatore [**(interfaccia IMFTransform).**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Durante il gap, l'oggetto deve inviare l'evento con la frequenza con cui normalmente produce campioni. Per il video, inviare un evento per ogni fotogramma mancante. Per l'audio, inviare l'evento almeno una volta al secondo durante il gap. Il valore dell'evento è il timestamp dell'esempio mancante. Inviare tutti gli eventi MEStreamTick necessari per riempire la lacune nei dati.

Se un'origine multimediale ha diversi flussi e si verifica un gap in più di un flusso, ogni flusso deve inviare eventi MEStreamTick. Ad esempio, se si verifica un gap nei dati audio e video, entrambi i flussi inviano l'evento.

L'evento MEStreamTick non completa una [**richiesta IMFMediaStream::RequestSample.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) L'origine multimediale deve comunque inviare un [evento MEMediaSample](memediasample.md) per ogni chiamata a **RequestSample.**

I sink multimediali non possono utilizzare direttamente questo evento. Per segnalare un gap nel flusso a un sink multimediale, chiamare [**IMFStreamSink::P laceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) con un marcatore TICK marcatore **MFSTREAMSINK. \_ \_** La pipeline Media Foundation converte gli eventi MEStreamTick in **marcatori MFSTREAMSINK \_ MARKER \_ TICK** quando necessario.

Non impostare [**l'attributo MFSampleExtension \_ Discontinuity**](mfsampleextension-discontinuity-attribute.md) nell'esempio multimediale successivo dopo un evento MEStreamTick. **L'attributo \_ Discontinuity di MFSampleExtension** implica che il timestamp è discontinuo con i timestamp precedenti, mentre MEStreamTick implica che i timestamp sono continui, ma alcuni dati sono mancanti.

> [!Note]  
> Una versione precedente della documentazione indica erroneamente che l'esempio dopo un evento MEStreamTick deve avere [**l'attributo MFSampleExtension \_ Discontinuity.**](mfsampleextension-discontinuity-attribute.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




