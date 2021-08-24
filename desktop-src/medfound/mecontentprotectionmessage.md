---
description: Generato da un componente della pipeline quando la configurazione viene modificata per uno degli schemi di protezione dell'output. Questo evento si applica solo al contenuto protetto.
ms.assetid: 0a13fc08-2bbe-46d8-a076-6165cca6ea36
title: Evento MEContentProtectionMessage (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0316767025fe4446909146b92cfcea8abcc3e0511990c19485a50c94dbc3fa59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013831"
---
# <a name="mecontentprotectionmessage-event"></a>EVENTO MEContentProtectionMessage

Generato da un componente della pipeline quando la configurazione viene modificata per uno degli schemi di protezione dell'output. Questo evento si applica solo al contenuto protetto.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Tutti gli output attendibili devono gestire questo evento. Media Foundation trasformazioni (MFT) ricevono questo evento tramite il [**metodo IMFTransform::P rocessEvent.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) I sink multimediali ricevono questo evento tramite il [**metodo IMFStreamSink::P laceMarker.**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)

L'output attendibile deve applicare le modifiche ai criteri o restituire il codice di errore MF \_ E \_ POLICY \_ UNSUPPORTED.

I dati e gli attributi degli eventi dipendono dal sistema di protezione del contenuto in uso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop vista \[ \| app UWP\]<br/>                                                    |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 \[ \| app UWP\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




