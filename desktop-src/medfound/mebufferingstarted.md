---
description: Segnala che un'origine multimediale è stata avviata per il buffer dei dati.
ms.assetid: 8637dfcd-2e0c-4cf4-a216-4089c201bfc6
title: Evento MEBufferingStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb3baf8e66d44eb67ee4c1bbc54ae2e197db081
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308743"
---
# <a name="mebufferingstarted-event"></a>Evento MEBufferingStarted

Segnala che un'origine multimediale è stata avviata per il buffer dei dati.

Un'origine multimediale può inviare questo evento se l'origine memorizza i dati nel buffer mentre è in esecuzione la sessione multimediale. Quando la sessione multimediale riceve questo evento, sospende il clock di presentazione finché l'origine multimediale non invia l'evento [MEBufferingStopped](mebufferingstopped.md) . La sessione multimediale trasmette inoltre l'evento MEBufferingStarted all'applicazione.

Anche i flussi di byte che implementano l'interfaccia [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) inviano questo evento.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Se un'origine multimediale invia l'evento MEBufferingStarted, deve inviare l'evento [MEBufferingStopped](mebufferingstopped.md) quando smette di memorizzare i dati nel buffer. L'origine multimediale deve inviare un evento MEBufferingStopped corrispondente per ogni evento MEBufferingStarted. L'origine multimediale non deve trasmettere questi eventi prima che venga chiamato il metodo [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) dell'origine o dopo la chiamata del metodo [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) dell'origine.

Se si esegue lo streaming dall'origine della rete Media Foundation, è possibile ottenere lo stato di avanzamento del buffer eseguendo una query sulla statistica **\_ \_ ID BUFFERPROGRESS MFNETSOURCE** . Per ulteriori informazioni, vedere [**MFNETSOURCE \_ Statistics \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




