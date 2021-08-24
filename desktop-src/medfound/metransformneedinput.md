---
description: Inviato da una trasformazione Media Foundation asincrona (MFT) per richiedere un nuovo esempio di input.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: Evento METransformNeedInput (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cc15bdffebfd22b4aecac2818da85e39379f681aec0e12fe92f895824edb78f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013501"
---
# <a name="metransformneedinput-event"></a>EVENTO METransformNeedInput

Inviato da una trasformazione Media Foundation asincrona (MFT) per richiedere un nuovo esempio di input.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione               |
|----------------------|---------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                        | Descrizione                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [ID FLUSSO DI \_ \_ INPUT MFT DELL'EVENTO MF \_ \_ \_](mf-event-mft-input-stream-id.md)<br/> | Identificatore del flusso che necessita di dati di input.<br/>*(Obbligatorio)*<br/> |



## <a name="remarks"></a>Commenti

I MFT asincroni inviano questo evento tramite [**l'interfaccia IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) I MFT sincroni non inviano mai questo evento.

Quando il client di MFT riceve questo evento, deve chiamare [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) per recapitare l'esempio successivo. [L'attributo \_ \_ MF EVENT MFT INPUT STREAM \_ \_ \_ ID](mf-event-mft-input-stream-id.md) dell'oggetto evento specifica quale flusso di input richiede dati.

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

 

 




