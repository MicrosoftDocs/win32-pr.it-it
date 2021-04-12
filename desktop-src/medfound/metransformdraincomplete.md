---
description: Inviato da una trasformazione di Media Foundation asincrona (MFT) quando un'operazione di svuotamento è stata completata.
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: Evento METransformDrainComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed291f9edacb11ba6edf7f5bd50a0715ae61a281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348746"
---
# <a name="metransformdraincomplete-event"></a>Evento METransformDrainComplete

Inviato da una trasformazione di Media Foundation asincrona (MFT) quando un'operazione di svuotamento è stata completata.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione               |
|----------------------|---------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                        | Descrizione                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [ID del flusso di input per l' \_ evento \_ MFT MF \_ \_ \_](mf-event-mft-input-stream-id.md)<br/> | Identificatore del flusso che è stato svuotato.<br/>*Necessaria*<br/> |



## <a name="remarks"></a>Commenti

Il MFTs asincrono invia questo evento tramite l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . MFTs sincroni non inviano mai questo evento.

Per svuotare un MFT, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio di **svuotamento del \_ \_ comando \_ del messaggio MFT** . Specificare il flusso di input da svuotare nel parametro *ulParam* . Al termine dell'operazione di svuotamento, un MFT asincrono invia l'evento METransformDrainComplete. L'attributo [MF \_ Event \_ MFT \_ input \_ Stream \_ ID](mf-event-mft-input-stream-id.md) dell'evento contiene l'identificatore di flusso specificato nel parametro *ulParam* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> <dt>

[MFTs asincrono](asynchronous-mfts.md)
</dt> </dl>

 

 




