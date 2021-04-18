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
# <a name="mebufferingstarted-event"></a><span data-ttu-id="bf23c-103">Evento MEBufferingStarted</span><span class="sxs-lookup"><span data-stu-id="bf23c-103">MEBufferingStarted event</span></span>

<span data-ttu-id="bf23c-104">Segnala che un'origine multimediale è stata avviata per il buffer dei dati.</span><span class="sxs-lookup"><span data-stu-id="bf23c-104">Signals that a media source has started to buffer data.</span></span>

<span data-ttu-id="bf23c-105">Un'origine multimediale può inviare questo evento se l'origine memorizza i dati nel buffer mentre è in esecuzione la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="bf23c-105">A media source can send this event if the source buffers data while the Media Session is running.</span></span> <span data-ttu-id="bf23c-106">Quando la sessione multimediale riceve questo evento, sospende il clock di presentazione finché l'origine multimediale non invia l'evento [MEBufferingStopped](mebufferingstopped.md) .</span><span class="sxs-lookup"><span data-stu-id="bf23c-106">When the Media Session receives this event, it pauses the presentation clock until the media source sends the [MEBufferingStopped](mebufferingstopped.md) event.</span></span> <span data-ttu-id="bf23c-107">La sessione multimediale trasmette inoltre l'evento MEBufferingStarted all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bf23c-107">The Media Session also forwards the MEBufferingStarted event to the application.</span></span>

<span data-ttu-id="bf23c-108">Anche i flussi di byte che implementano l'interfaccia [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) inviano questo evento.</span><span class="sxs-lookup"><span data-stu-id="bf23c-108">Byte streams that implement the [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) interface also send this event.</span></span>

## <a name="event-values"></a><span data-ttu-id="bf23c-109">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="bf23c-109">Event values</span></span>

<span data-ttu-id="bf23c-110">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="bf23c-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="bf23c-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="bf23c-111">VARTYPE</span></span>              | <span data-ttu-id="bf23c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf23c-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="bf23c-113">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="bf23c-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="bf23c-114">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="bf23c-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="bf23c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf23c-115">Remarks</span></span>

<span data-ttu-id="bf23c-116">Se un'origine multimediale invia l'evento MEBufferingStarted, deve inviare l'evento [MEBufferingStopped](mebufferingstopped.md) quando smette di memorizzare i dati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="bf23c-116">If a media source sends the MEBufferingStarted event, it must send the [MEBufferingStopped](mebufferingstopped.md) event when it stops buffering data.</span></span> <span data-ttu-id="bf23c-117">L'origine multimediale deve inviare un evento MEBufferingStopped corrispondente per ogni evento MEBufferingStarted.</span><span class="sxs-lookup"><span data-stu-id="bf23c-117">The media source must send a matching MEBufferingStopped event for every MEBufferingStarted event.</span></span> <span data-ttu-id="bf23c-118">L'origine multimediale non deve trasmettere questi eventi prima che venga chiamato il metodo [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) dell'origine o dopo la chiamata del metodo [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) dell'origine.</span><span class="sxs-lookup"><span data-stu-id="bf23c-118">The media source should not forward these events before the source's [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called, or after the source's [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method is called.</span></span>

<span data-ttu-id="bf23c-119">Se si esegue lo streaming dall'origine della rete Media Foundation, è possibile ottenere lo stato di avanzamento del buffer eseguendo una query sulla statistica **\_ \_ ID BUFFERPROGRESS MFNETSOURCE** .</span><span class="sxs-lookup"><span data-stu-id="bf23c-119">If you are streaming from the Media Foundation network source, you can get the buffering progress by querying the **MFNETSOURCE\_BUFFERPROGRESS\_ID** statistic.</span></span> <span data-ttu-id="bf23c-120">Per ulteriori informazioni, vedere [**MFNETSOURCE \_ Statistics \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span><span class="sxs-lookup"><span data-stu-id="bf23c-120">For more information, see [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>

## <a name="examples"></a><span data-ttu-id="bf23c-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="bf23c-121">Examples</span></span>


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



## <a name="requirements"></a><span data-ttu-id="bf23c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf23c-122">Requirements</span></span>



| <span data-ttu-id="bf23c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf23c-123">Requirement</span></span> | <span data-ttu-id="bf23c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="bf23c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf23c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf23c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bf23c-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf23c-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bf23c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf23c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bf23c-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bf23c-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bf23c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf23c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf23c-130"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf23c-130"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf23c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf23c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf23c-132">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bf23c-132">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="bf23c-133">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bf23c-133">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




