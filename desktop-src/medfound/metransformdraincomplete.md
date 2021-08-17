---
description: Inviato da una trasformazione Media Foundation asincrona (MFT) al termine di un'operazione di svuotamento.
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: Evento METransformDrainComplete (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd5ab03ac5027d1dc7549e7b7f0b8494cd8066b07afb64c5df17415a4986866e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974030"
---
# <a name="metransformdraincomplete-event"></a>EVENTO METransformDrainComplete

Inviato da una trasformazione Media Foundation asincrona (MFT) al termine di un'operazione di svuotamento.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione               |
|----------------------|---------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                        | Descrizione                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [ID FLUSSO DI \_ \_ INPUT MFT DELL'EVENTO MF \_ \_ \_](mf-event-mft-input-stream-id.md)<br/> | Identificatore del flusso svuotato.<br/>*(Obbligatorio)*<br/> |



## <a name="remarks"></a>Commenti

I MFT asincroni inviano questo evento tramite [**l'interfaccia IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) I MFT sincroni non inviano mai questo evento.

Per svuotare un messaggio MFT, chiamare [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il **messaggio MFT \_ MESSAGE COMMAND \_ \_ DRAIN.** Specificare il flusso di input da svuotare nel *parametro ulParam.* Al termine dell'operazione di svuotamento, un MFT asincrono invia l'evento METransformDrainComplete. [L'attributo \_ \_ MF EVENT MFT INPUT STREAM \_ \_ \_ ID](mf-event-mft-input-stream-id.md) dell'evento contiene l'identificatore di flusso specificato nel *parametro ulParam.*

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

 

 




