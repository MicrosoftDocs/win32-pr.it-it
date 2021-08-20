---
description: MEDeviceStreamCreated è un tipo di evento multimediale esteso generato con un evento multimediale MEUnknown da Device MFT.
ms.assetid: 8aaa6908-0f2e-4a73-9362-69f42b74f495
title: Evento MEDeviceStreamCreated (mftransform.h)
ms.topic: article
ms.date: 08/31/2018
ms.openlocfilehash: 99e13dae5db9d680909a435d5520f6b07d7d4b6c11782c340b72fcdd0eddc53a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878068"
---
# <a name="medevicestreamcreated-event"></a>EVENTO MEDeviceStreamCreated

MEDeviceStreamCreated è un tipo di evento multimediale esteso generato con un evento multimediale MEUnknown da Device MFT.

Questo tipo di evento multimediale esteso non ha payload.  Il valore HRESULT appropriato deve essere fornito [**tramite il metodo IMFMediaEvent::GetStatus.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus)




## <a name="remarks"></a>Commenti

Questo evento multimediale esteso deve essere inviato da Device MFT come parte della selezione del tipo di supporto nel flusso di output di DMFT.  Quando SetOutputStreamState viene richiamato nell'interfaccia IMFDeviceTransform, DMFT è responsabile della segnalazione della modifica negli stati del flusso di input richiesti con l'evento multimediale [METransformInputStreamStateChanged.](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) Quando la modifica dello stato del flusso di input è stata riconosciuta dalla pipeline con la chiamata a SetInputStreamState del DMFT, DMFT è responsabile del completamento della configurazione dello stato interno e della generazione del tipo di evento multimediale esteso **MEDeviceStreamCreated.**

Se questo tipo di evento multimediale esteso non viene generato, Gestione trasformazione dispositivo non recapita fotogrammi di input al DMFT.
Il tipo di evento multimediale esteso deve anche essere impostato come attributo di IMFMediaEvent, l'ID del flusso di output che usa l MF_EVENT_MFT_INPUT_STREAM_ID **attributo** .

```cpp
IMFMediaEvent* pMediaEvent = nullptr;

hr = MFCreateMediaEvent (MEUnknown,
                         MEDeviceStreamCreated,
                         S_OK,
                         nullptr,
                         &pMediaEvent);
if (SUCCEEDED(hr))
{
    hr = pMediaEvent->SetUINT32(MF_EVENT_MFT_INPUT_STREAM_ID, GetOutputStreamId());
}

if (SUCCEEDED(hr))
{
    hr = m_pEventQueue->QueueEvent(pMediaEvent);
}

if (nullptr != pMediaEvent)
{
    pMediaEvent->Release();
    pMediaEvent = nullptr;
}

return hr;
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                           |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> <dt>

[Streaming Audio Renderer](streaming-audio-renderer.md)
</dt> </dl>

 

 
