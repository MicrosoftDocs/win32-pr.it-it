---
description: MEDeviceStreamCreated è un tipo di evento multimediale esteso generato con un evento multimediale MEUnknown dal dispositivo MFT.
ms.assetid: 8aaa6908-0f2e-4a73-9362-69f42b74f495
title: Evento MEDeviceStreamCreated (mftransform. h)
ms.topic: article
ms.date: 08/31/2018
ms.openlocfilehash: 632ebc305473cd596656a21f562be25d53c2bace
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226382"
---
# <a name="medevicestreamcreated-event"></a>Evento MEDeviceStreamCreated

MEDeviceStreamCreated è un tipo di evento multimediale esteso generato con un evento multimediale MEUnknown dal dispositivo MFT.

Questo tipo di evento multimediale esteso non ha payload.  Il valore HRESULT appropriato deve essere fornito tramite il metodo [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) .




## <a name="remarks"></a>Commenti

Questo evento multimediale esteso deve essere inviato dal dispositivo MFT come parte della selezione del tipo di supporto nel flusso di output di DMFT.  Quando SetOutputStreamState viene richiamato sull'interfaccia IMFDeviceTransform, DMFT è responsabile della segnalazione della modifica negli Stati del flusso di input necessari con l'evento multimediale [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) . Quando la modifica dello stato del flusso di input è stata riconosciuta dalla pipeline con la chiamata a SetInputStreamState di DMFT, DMFT è responsabile del completamento della configurazione dello stato interno e della generazione del tipo di evento dei supporti estesi **MEDeviceStreamCreated** .

Se questo tipo di evento multimediale esteso non viene generato, il gestore delle trasformazioni del dispositivo non distribuirà alcun frame di input a DMFT.
Il tipo di evento supporto esteso deve inoltre impostare come attributo di IMFMediaEvent, l'ID del flusso di output utilizzando l'attributo **MF_EVENT_MFT_INPUT_STREAM_ID** .

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
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> <dt>

[Renderer audio di streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
