---
description: Generato da un componente della pipeline quando vengono modificati i criteri di output per il flusso. Questo evento si applica solo ai contenuti protetti.
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: Evento MEPolicyChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6827c44958e2df016365a8caa9a66f1aad9a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309627"
---
# <a name="mepolicychanged-event"></a>Evento MEPolicyChanged

Generato da un componente della pipeline quando vengono modificati i criteri di output per il flusso. Questo evento si applica solo ai contenuti protetti.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| VT \_ sconosciuto<br/> | Puntatore all'interfaccia [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) del nuovo criterio per il flusso.<br/> <br/> |



## <a name="remarks"></a>Commenti

Tutti gli output attendibili devono gestire questo evento. Le trasformazioni Media Foundation (MFTs) ricevono questo evento tramite il metodo [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) . I sink di supporto ricevono questo evento tramite il metodo [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .

L'output attendibile deve applicare il nuovo criterio o restituire il codice di errore MF \_ E \_ criteri non \_ supportati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                                                    |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




