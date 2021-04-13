---
description: Ruoli del dispositivo per le applicazioni DirectShow
ms.assetid: 54f42bda-b4a0-465c-9ce6-9102d2908776
title: Ruoli del dispositivo per le applicazioni DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df8b43ddd56870b65fc9ec1e3bb600e8e6b79528
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482757"
---
# <a name="device-roles-for-directshow-applications"></a><span data-ttu-id="989fd-103">Ruoli del dispositivo per le applicazioni DirectShow</span><span class="sxs-lookup"><span data-stu-id="989fd-103">Device Roles for DirectShow Applications</span></span>

> [!Note]  
> <span data-ttu-id="989fd-104">L' [API MMDevice](mmdevice-api.md) supporta i ruoli del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="989fd-104">The [MMDevice API](mmdevice-api.md) supports device roles.</span></span> <span data-ttu-id="989fd-105">Tuttavia, l'interfaccia utente in Windows Vista non implementa il supporto per questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="989fd-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="989fd-106">Il supporto dell'interfaccia utente per i ruoli del dispositivo può essere implementato in una versione futura di Windows.</span><span class="sxs-lookup"><span data-stu-id="989fd-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="989fd-107">Per ulteriori informazioni, vedere [ruoli del dispositivo in Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="989fd-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="989fd-108">L'API DirectShow non consente a un'applicazione di selezionare il [dispositivo dell'endpoint audio](audio-endpoint-devices.md) assegnato a un particolare [ruolo del dispositivo](device-roles.md).</span><span class="sxs-lookup"><span data-stu-id="989fd-108">The DirectShow API does not provide a means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that is assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="989fd-109">Tuttavia, in Windows Vista, le API di base audio possono essere usate insieme a un'applicazione DirectShow per abilitare la selezione del dispositivo in base al ruolo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="989fd-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a DirectShow application to enable device selection based on device role.</span></span> <span data-ttu-id="989fd-110">Con l'ausilio delle API di base audio, l'applicazione può:</span><span class="sxs-lookup"><span data-stu-id="989fd-110">With the help of the core audio APIs, the application can:</span></span>

-   <span data-ttu-id="989fd-111">Identificare il dispositivo dell'endpoint audio assegnato dall'utente a un particolare ruolo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="989fd-111">Identify the audio endpoint device that the user has assigned to a particular device role.</span></span>
-   <span data-ttu-id="989fd-112">Creare un filtro di rendering audio DirectShow con un'interfaccia [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) che incapsula il dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="989fd-112">Create a DirectShow audio rendering filter with an [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) interface that encapsulates the audio endpoint device.</span></span>
-   <span data-ttu-id="989fd-113">Compilare un grafo DirectShow che incorpora il filtro.</span><span class="sxs-lookup"><span data-stu-id="989fd-113">Build a DirectShow graph that incorporates the filter.</span></span>

<span data-ttu-id="989fd-114">Per ulteriori informazioni su DirectShow e [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter), vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="989fd-114">For more information about DirectShow and [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter), see the Windows SDK documentation.</span></span>

<span data-ttu-id="989fd-115">Nell'esempio di codice seguente viene illustrato come creare un filtro per il rendering audio DirectShow che incapsula il dispositivo dell'endpoint di rendering assegnato a un particolare ruolo del dispositivo:</span><span class="sxs-lookup"><span data-stu-id="989fd-115">The following code example shows how to create a DirectShow audio rendering filter that encapsulates the rendering endpoint device that is assigned to a particular device role:</span></span>


```C++
//-----------------------------------------------------------
// Create a DirectShow audio rendering filter that
// encapsulates the audio endpoint device that is currently
// assigned to the specified device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

// This application's audio session GUID
const GUID guidAudioSessionId = {
    0xb13ff52e, 0xa5cf, 0x4fca,
    {0x9f, 0xc3, 0x42, 0x26, 0x5b, 0x0b, 0x14, 0xfb}
};

HRESULT CreateAudioRenderer(ERole role, IBaseFilter** ppAudioRenderer)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;

    if (ppAudioRenderer == NULL)
    {
        return E_POINTER;
    }

    // Activate the IBaseFilter interface on the
    // audio renderer with the specified role.
    hr = CoCreateInstance(CLSID_MMDeviceEnumerator,
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    DIRECTX_AUDIO_ACTIVATION_PARAMS  daap;
    daap.cbDirectXAudioActivationParams = sizeof(daap);
    daap.guidAudioSession = guidAudioSessionId;
    daap.dwAudioStreamFlags = AUDCLNT_STREAMFLAGS_CROSSPROCESS;

    PROPVARIANT  var;
    PropVariantInit(&var);

    var.vt = VT_BLOB;
    var.blob.cbSize = sizeof(daap);
    var.blob.pBlobData = (BYTE*)&daap;

    hr = pDevice->Activate(__uuidof(IBaseFilter),
                           CLSCTX_ALL, &var,
                           (void**)ppAudioRenderer);
    EXIT_ON_ERROR(hr)

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    return hr;
}
```



<span data-ttu-id="989fd-116">Nell'esempio di codice precedente, la funzione CreateAudioRenderer accetta un ruolo del dispositivo (eConsole, eMultimedia o comunicazioni elettroniche) come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="989fd-116">In the preceding code example, the CreateAudioRenderer function accepts a device role (eConsole, eMultimedia, or eCommunications) as an input parameter.</span></span> <span data-ttu-id="989fd-117">Il secondo parametro è un puntatore tramite il quale la funzione scrive l'indirizzo di un'istanza dell'interfaccia [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="989fd-117">The second parameter is a pointer through which the function writes the address of an [**IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) interface instance.</span></span> <span data-ttu-id="989fd-118">Nell'esempio viene inoltre illustrato come utilizzare il metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) per assegnare il flusso audio nell'istanza **IBaseFilter** a una sessione audio tra processi con un GUID di sessione specifico dell'applicazione (specificato dalla costante **guidAudioSessionId** ).</span><span class="sxs-lookup"><span data-stu-id="989fd-118">In addition, the example shows how to use the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to assign the audio stream in the **IBaseFilter** instance to a cross-process audio session with an application-specific session GUID (specified by the **guidAudioSessionId** constant).</span></span> <span data-ttu-id="989fd-119">Il terzo parametro nella chiamata **Activate** punta a una struttura che contiene il GUID della sessione e il flag tra processi.</span><span class="sxs-lookup"><span data-stu-id="989fd-119">The third parameter in the **Activate** call points to a structure that contains the session GUID and cross-process flag.</span></span> <span data-ttu-id="989fd-120">Se l'utente esegue più istanze dell'applicazione, i flussi audio da tutte le istanze utilizzano lo stesso GUID della sessione e quindi appartengono alla stessa sessione.</span><span class="sxs-lookup"><span data-stu-id="989fd-120">If the user runs multiple instances of the application, then the audio streams from all the instances use the same session GUID and thus belong to the same session.</span></span>

<span data-ttu-id="989fd-121">In alternativa, il chiamante può specificare **null** come terzo parametro nella chiamata [**Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) per assegnare il flusso alla sessione predefinita come sessione specifica del processo con GUID di sessione valore \_ null.</span><span class="sxs-lookup"><span data-stu-id="989fd-121">Alternatively, the caller can specify **NULL** as the third parameter in the [**Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) call to assign the stream to the default session as the process-specific session with session GUID value GUID\_NULL.</span></span> <span data-ttu-id="989fd-122">Per ulteriori informazioni, vedere **IMMDevice:: Activate**.</span><span class="sxs-lookup"><span data-stu-id="989fd-122">For more information, see **IMMDevice::Activate**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="989fd-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="989fd-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="989fd-124">Interoperabilità con le API audio legacy</span><span class="sxs-lookup"><span data-stu-id="989fd-124">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
