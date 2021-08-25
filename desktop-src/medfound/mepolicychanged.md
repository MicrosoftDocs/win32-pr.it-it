---
description: Generato da un componente della pipeline quando i criteri di output per il flusso cambiano. Questo evento si applica solo al contenuto protetto.
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: Evento MEPolicyChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac87d3dae63b20d19c91f0fdef5471060753152901d9096b1be315cd76e9974
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957411"
---
# <a name="mepolicychanged-event"></a>Evento MEPolicyChanged

Generato da un componente della pipeline quando i criteri di output per il flusso cambiano. Questo evento si applica solo al contenuto protetto.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Puntatore [**all'interfaccia IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) dei nuovi criteri per il flusso.<br/> <br/> |



## <a name="remarks"></a>Commenti

Tutti gli output attendibili devono gestire questo evento. Media Foundation trasformazioni (MFT) ricevono questo evento tramite il [**metodo IMFTransform::P rocessEvent.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) I sink multimediali ricevono questo evento tramite il [**metodo IMFStreamSink::P laceMarker.**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)

L'output attendibile deve applicare i nuovi criteri o restituire il codice di errore MF \_ E \_ POLICY \_ UNSUPPORTED.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop Di Vista \[ \| app UWP\]<br/>                                                    |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 \[ \|\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




