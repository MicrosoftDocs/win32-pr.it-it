---
description: Inviato da una trasformazione di Media Foundation asincrona (MFT) per richiedere un nuovo esempio di input.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: Evento METransformNeedInput (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbdea648e4dc7d90b1321958eebb6c544ebb88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129806"
---
# <a name="metransformneedinput-event"></a>Evento METransformNeedInput

Inviato da una trasformazione di Media Foundation asincrona (MFT) per richiedere un nuovo esempio di input.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione               |
|----------------------|---------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                        | Descrizione                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [ID del flusso di input per l' \_ evento \_ MFT MF \_ \_ \_](mf-event-mft-input-stream-id.md)<br/> | Identificatore del flusso che necessita di dati di input.<br/>*Necessaria*<br/> |



## <a name="remarks"></a>Commenti

Il MFTs asincrono invia questo evento tramite l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . MFTs sincroni non inviano mai questo evento.

Quando il client di MFT riceve questo evento, deve chiamare [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) per recapitare l'esempio successivo. L'attributo [MF \_ Event \_ MFT \_ input \_ Stream \_ ID](mf-event-mft-input-stream-id.md) dell'oggetto evento specifica il flusso di input che richiede i dati.

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

 

 




