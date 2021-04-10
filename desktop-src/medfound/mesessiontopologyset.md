---
description: 'Generato dopo che il metodo IMFMediaSession:: SetValue viene completato in modo asincrono. La sessione multimediale genera questo evento dopo che la topologia è stata risolta in una topologia completa ed è stata accodata la topologia per la riproduzione.'
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: Evento MESessionTopologySet (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338668b0ec9b4dd81140edfb55a823a5a595459b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967052"
---
# <a name="mesessiontopologyset-event"></a>Evento MESessionTopologySet

Generato dopo che il metodo [**IMFMediaSession::**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) SetValue viene completato in modo asincrono. La sessione multimediale genera questo evento dopo che la topologia è stata risolta in una topologia completa ed è stata accodata la topologia per la riproduzione.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                                              |
|------------------------|----------------------------------------------------------------------------------------------------------|
| VT \_ vuoto<br/>   | Nessun dato dell'evento.<br/> <br/>                                                                    |
| VT \_ sconosciuto<br/> | Puntatore all'interfaccia [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) della topologia completa.<br/> <br/> |



## <a name="examples"></a>Esempio

Nell'esempio seguente viene recuperato il puntatore [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) da un evento MESessionTopologySet.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




