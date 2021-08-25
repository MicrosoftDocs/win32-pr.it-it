---
description: Generato dopo il completamento asincrono del metodo IMFMediaSession::SetTopology. La sessione multimediale genera questo evento dopo aver risolto la topologia in una topologia completa e accodato la topologia per la riproduzione.
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: Evento MESessionTopologySet (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2b5454309855ff472c633388cddabe0c12fab09e2ae462aacd2de49c3c9bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957401"
---
# <a name="mesessiontopologyset-event"></a>EVENTO MESessionTopologySet

Generato dopo il completamento asincrono del metodo [**IMFMediaSession::SetTopology.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) La sessione multimediale genera questo evento dopo aver risolto la topologia in una topologia completa e accodato la topologia per la riproduzione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                                              |
|------------------------|----------------------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/>   | Nessun dato dell'evento.<br/> <br/>                                                                    |
| VT \_ UNKNOWN<br/> | Puntatore [**all'interfaccia IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) della topologia completa.<br/> <br/> |



## <a name="examples"></a>Esempio

Nell'esempio seguente viene recuperato il [**puntatore IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) da un evento MESessionTopologySet.


```
HRESULT GetTopologyFromEvent(IMFMediaEvent *pEvent, IMFTopology **ppTopology)
{
    HRESULT hr = S_OK;
    PROPVARIANT var;

    PropVariantInit(&var);
    hr = pEvent->GetValue(&var);
    if (SUCCEEDED(hr))
    {
        if (var.vt != VT_UNKNOWN)
        {
            hr = E_UNEXPECTED;
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = var.punkVal->QueryInterface(__uuidof(IMFTopology), (void**)ppTopology);
    }
    PropVariantClear(&var);
    return hr;
}
```



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

 

 




