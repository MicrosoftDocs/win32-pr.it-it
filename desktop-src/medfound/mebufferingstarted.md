---
description: Segnala che un'origine multimediale ha iniziato a eseguire il buffer dei dati.
ms.assetid: 8637dfcd-2e0c-4cf4-a216-4089c201bfc6
title: Evento MEBufferingStarted (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55a691b723fc2e09487752ee8f5226e32504d60a6d68a4652bbb2b5b3e5aa7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724271"
---
# <a name="mebufferingstarted-event"></a>EVENTO MEBufferingStarted

Segnala che un'origine multimediale ha iniziato a eseguire il buffer dei dati.

Un'origine multimediale può inviare questo evento se l'origine esegue il buffer dei dati durante l'esecuzione della sessione multimediale. Quando la sessione multimediale riceve questo evento, sospende l'orologio della presentazione fino a quando l'origine multimediale invia l'evento [MEBufferingStopped.](mebufferingstopped.md) La sessione multimediale inoltra anche l'evento MEBufferingStarted all'applicazione.

Anche i flussi di byte che implementano [**l'interfaccia IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) inviano questo evento.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Se un'origine multimediale invia l'evento MEBufferingStarted, deve inviare l'evento [MEBufferingStopped](mebufferingstopped.md) quando interrompe il buffering dei dati. L'origine multimediale deve inviare un evento MEBufferingStopped corrispondente per ogni evento MEBufferingStarted. L'origine multimediale non deve inoltrare questi eventi prima che venga chiamato il metodo [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) dell'origine o dopo la chiamata del metodo [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) dell'origine.

Se si esegue lo streaming dall'origine Media Foundation rete, è possibile ottenere lo stato di avanzamento del buffer tramite una query sulla statistica **MFNETSOURCE \_ BUFFERPROGRESS \_ ID.** Per altre informazioni, vedere [**MFNETSOURCE \_ STATISTICS \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).

## <a name="examples"></a>Esempio


```C++
HRESULT GetBufferProgress(IMFMediaSession *pSession, DWORD *pProgress)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_BUFFERPROGRESS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pProgress = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
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
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




