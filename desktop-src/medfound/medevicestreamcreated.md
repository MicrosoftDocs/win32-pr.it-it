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
# <a name="medevicestreamcreated-event"></a><span data-ttu-id="c6c78-103">Evento MEDeviceStreamCreated</span><span class="sxs-lookup"><span data-stu-id="c6c78-103">MEDeviceStreamCreated event</span></span>

<span data-ttu-id="c6c78-104">MEDeviceStreamCreated è un tipo di evento multimediale esteso generato con un evento multimediale MEUnknown dal dispositivo MFT.</span><span class="sxs-lookup"><span data-stu-id="c6c78-104">MEDeviceStreamCreated is an extended media event type generated with an MEUnknown media event by the Device MFT.</span></span>

<span data-ttu-id="c6c78-105">Questo tipo di evento multimediale esteso non ha payload.</span><span class="sxs-lookup"><span data-stu-id="c6c78-105">This extended media event type has no payload.</span></span>  <span data-ttu-id="c6c78-106">Il valore HRESULT appropriato deve essere fornito tramite il metodo [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) .</span><span class="sxs-lookup"><span data-stu-id="c6c78-106">Appropriate HRESULT should be provided via the [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) method.</span></span>




## <a name="remarks"></a><span data-ttu-id="c6c78-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6c78-107">Remarks</span></span>

<span data-ttu-id="c6c78-108">Questo evento multimediale esteso deve essere inviato dal dispositivo MFT come parte della selezione del tipo di supporto nel flusso di output di DMFT.</span><span class="sxs-lookup"><span data-stu-id="c6c78-108">This extended media event must be sent by the Device MFT as a part of the media type selection on the output stream of the DMFT.</span></span>  <span data-ttu-id="c6c78-109">Quando SetOutputStreamState viene richiamato sull'interfaccia IMFDeviceTransform, DMFT è responsabile della segnalazione della modifica negli Stati del flusso di input necessari con l'evento multimediale [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) .</span><span class="sxs-lookup"><span data-stu-id="c6c78-109">When the SetOutputStreamState is invoked on the IMFDeviceTransform interface, the DMFT is responsible for signaling the change in the required input stream states with the [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) media event.</span></span> <span data-ttu-id="c6c78-110">Quando la modifica dello stato del flusso di input è stata riconosciuta dalla pipeline con la chiamata a SetInputStreamState di DMFT, DMFT è responsabile del completamento della configurazione dello stato interno e della generazione del tipo di evento dei supporti estesi **MEDeviceStreamCreated** .</span><span class="sxs-lookup"><span data-stu-id="c6c78-110">When the input stream state change has been acknowledged by the pipeline with the call into SetInputStreamState of the DMFT, the DMFT is responsible for completing its internal state configuration and raising the **MEDeviceStreamCreated** extended media event type.</span></span>

<span data-ttu-id="c6c78-111">Se questo tipo di evento multimediale esteso non viene generato, il gestore delle trasformazioni del dispositivo non distribuirà alcun frame di input a DMFT.</span><span class="sxs-lookup"><span data-stu-id="c6c78-111">If this extended media event type is not raised, the Device Transform Manager will not deliver any input frames to the DMFT.</span></span>
<span data-ttu-id="c6c78-112">Il tipo di evento supporto esteso deve inoltre impostare come attributo di IMFMediaEvent, l'ID del flusso di output utilizzando l'attributo **MF_EVENT_MFT_INPUT_STREAM_ID** .</span><span class="sxs-lookup"><span data-stu-id="c6c78-112">The extended media event type must also set as an attribute of the IMFMediaEvent, the output stream ID using the **MF_EVENT_MFT_INPUT_STREAM_ID** attribute.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="c6c78-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6c78-113">Requirements</span></span>



| <span data-ttu-id="c6c78-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6c78-114">Requirement</span></span> | <span data-ttu-id="c6c78-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c6c78-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c78-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6c78-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c6c78-117">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c6c78-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c6c78-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6c78-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c6c78-119">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="c6c78-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c6c78-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6c78-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6c78-121"><dt>mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6c78-121"><dt>mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6c78-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6c78-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c78-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6c78-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="c6c78-124">Renderer audio di streaming</span><span class="sxs-lookup"><span data-stu-id="c6c78-124">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
