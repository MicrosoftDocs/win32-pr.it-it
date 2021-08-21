---
description: Inviato da una trasformazione Media Foundation asincrona (MFT) in risposta a un messaggio MFT \_ MESSAGE \_ COMMAND \_ MARKER.
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: Evento METransformMarker (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7029119b30314e56531c0afb29accadb67e1efb343a906c2558af2157c0b1f82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827041"
---
# <a name="metransformmarker-event"></a>Evento METransformMarker

Inviato da una trasformazione Media Foundation asincrona (MFT) in risposta a un messaggio **MFT \_ MESSAGE COMMAND \_ \_ MARKER.**

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione               |
|----------------------|---------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                      | Descrizione                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [CONTESTO \_ \_ MFT DELL'EVENTO \_ MF](mf-event-mft-context.md)<br/> | Valore del parametro *ulParam* dal messaggio **MFT \_ MESSAGE COMMAND \_ \_ MARKER.**<br/>*(Obbligatorio)*<br/> |



## <a name="remarks"></a>Commenti

I MFT asincroni inviano questo evento tramite [**l'interfaccia IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) I MFT sincroni non inviano mai questo evento.

Il client di un MFT asincrono può inserire un marcatore nel flusso chiamando [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio **MFT \_ MESSAGE COMMAND \_ \_ MARKER.** Il *parametro ulParam* contiene dati definiti dall'applicazione.

Al termine dell'elaborazione di tutti i dati di input disponibili al momento della chiamata [**a ProcessMessage,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) MFT accoda un evento METransformMarker. [L'attributo \_ \_ MF EVENT MFT \_ CONTEXT](mf-event-mft-context.md) dell'evento contiene il valore del *parametro ulParam.* Per altre informazioni, vedere [MFT asincroni](asynchronous-mfts.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> <dt>

[MFT asincroni](asynchronous-mfts.md)
</dt> </dl>

 

 




