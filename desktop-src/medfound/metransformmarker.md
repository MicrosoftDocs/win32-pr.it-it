---
description: Inviato da una trasformazione di Media Foundation asincrona (MFT) in risposta a un \_ messaggio dell'indicatore del comando del messaggio MFT \_ \_ .
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: Evento METransformMarker (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab79c47e2ddb26f2366aff075548f7905807df1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309601"
---
# <a name="metransformmarker-event"></a>Evento METransformMarker

Inviato da una trasformazione di Media Foundation asincrona (MFT) in risposta a un messaggio dell' **\_ indicatore del \_ comando \_ del messaggio MFT** .

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione               |
|----------------------|---------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                      | Descrizione                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [\_ \_ contesto MFT evento \_ MF](mf-event-mft-context.md)<br/> | Il valore del parametro *ulParam* del messaggio del **\_ \_ \_ marcatore del comando del messaggio MFT** .<br/>*Necessaria*<br/> |



## <a name="remarks"></a>Commenti

Il MFTs asincrono invia questo evento tramite l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . MFTs sincroni non inviano mai questo evento.

Il client di una MFT asincrona può inserire un marcatore nel flusso chiamando [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio **del \_ \_ \_ marcatore del comando del messaggio MFT** . Il parametro *ulParam* contiene dati definiti dall'applicazione.

Al termine dell'elaborazione di tutti i dati di input disponibili al momento della chiamata [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) , il MFT Accoda un evento METransformMarker. L'attributo di [ \_ \_ \_ contesto MFT](mf-event-mft-context.md) dell'evento MF dell'evento contiene il valore del parametro *ulParam* . Per altre informazioni, vedere [MFTS asincrono](asynchronous-mfts.md).

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

 

 




