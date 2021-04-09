---
description: Ruoli del dispositivo per le applicazioni DirectSound
ms.assetid: 7d82d67f-aad8-4e5b-ac65-87d75774e613
title: Ruoli del dispositivo per le applicazioni DirectSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3829817f8b00c7288aceb8d0b6d418d5793ae580
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965896"
---
# <a name="device-roles-for-directsound-applications"></a><span data-ttu-id="a2d51-103">Ruoli del dispositivo per le applicazioni DirectSound</span><span class="sxs-lookup"><span data-stu-id="a2d51-103">Device Roles for DirectSound Applications</span></span>

> [!Note]  
> <span data-ttu-id="a2d51-104">L' [API MMDevice](mmdevice-api.md) supporta i ruoli del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a2d51-104">The [MMDevice API](mmdevice-api.md) supports device roles.</span></span> <span data-ttu-id="a2d51-105">Tuttavia, l'interfaccia utente in Windows Vista non implementa il supporto per questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a2d51-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="a2d51-106">Il supporto dell'interfaccia utente per i ruoli del dispositivo può essere implementato in una versione futura di Windows.</span><span class="sxs-lookup"><span data-stu-id="a2d51-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="a2d51-107">Per ulteriori informazioni, vedere [ruoli del dispositivo in Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="a2d51-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="a2d51-108">L'API DirectSound non fornisce un mezzo per consentire a un'applicazione di selezionare il [dispositivo dell'endpoint audio](audio-endpoint-devices.md) assegnato dall'utente a un particolare [ruolo del dispositivo](device-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a2d51-108">The DirectSound API does not provide a means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that the user has assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="a2d51-109">Tuttavia, in Windows Vista, le API di base audio possono essere usate insieme a un'applicazione DirectSound per abilitare la selezione dei dispositivi in base al ruolo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a2d51-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a DirectSound application to enable device selection based on device role.</span></span> <span data-ttu-id="a2d51-110">Con l'ausilio delle API di base audio, l'applicazione è in grado di identificare il dispositivo dell'endpoint audio assegnato a un ruolo specifico, ottenere il GUID del dispositivo DirectSound per il dispositivo endpoint e chiamare la funzione **DirectSoundCreate** o **DirectSoundCaptureCreate** per creare un'istanza dell'interfaccia **IDirectSound** o **IDirectSoundCapture** che incapsula il dispositivo dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="a2d51-110">With the help of the core audio APIs, the application can identify the audio endpoint device that is assigned to a particular role, get the DirectSound device GUID for the endpoint device, and call the **DirectSoundCreate** or **DirectSoundCaptureCreate** function to create an **IDirectSound** or **IDirectSoundCapture** interface instance that encapsulates the endpoint device.</span></span> <span data-ttu-id="a2d51-111">Per ulteriori informazioni su DirectSound, vedere la documentazione di Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a2d51-111">For more information about DirectSound, see the Windows SDK documentation.</span></span>

<span data-ttu-id="a2d51-112">Nell'esempio di codice seguente viene illustrato come ottenere il GUID del dispositivo DirectSound per il dispositivo di rendering o acquisizione attualmente assegnato a un particolare ruolo del dispositivo:</span><span class="sxs-lookup"><span data-stu-id="a2d51-112">The following code example shows how to obtain the DirectSound device GUID for the rendering or capture device that is currently assigned to a particular device role:</span></span>


```C++
//-----------------------------------------------------------
// Get the DirectSound or DirectSoundCapture device GUID for
// an audio endpoint device. If flow = eRender, the function
// gets the DirectSound device GUID for the rendering device
// with the specified device role. If flow = eCapture, the
// function gets the DirectSoundCapture device GUID for the
// capture device with the specified device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetDirectSoundGuid(EDataFlow flow, ERole role, GUID* pDevGuid)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    if (pDevGuid == NULL)
    {
        return E_POINTER;
    }

    // Get a device enumerator for the audio endpoint
    // devices in the system.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the endpoint device with the specified dataflow
    // direction (eRender or eCapture) and device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(flow, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    EXIT_ON_ERROR(hr)

    // Get the DirectSound or DirectSoundCapture device GUID
    // (in WCHAR string format) for the endpoint device.
    hr = pProps->GetValue(PKEY_AudioEndpoint_GUID, &var);
    EXIT_ON_ERROR(hr)

    // Convert the WCHAR string to a GUID structure.
    hr = CLSIDFromString(var.pwszVal, pDevGuid);
    EXIT_ON_ERROR(hr)

Exit:
    PropVariantClear(&var);
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    SAFE_RELEASE(pProps);
    return hr;
}
```



<span data-ttu-id="a2d51-113">Nell'esempio di codice precedente, la funzione GetDirectSoundGuid accetta una direzione del flusso di dati (eRender o eCapture) e un ruolo del dispositivo (eConsole, eMultimedia o comunicazioni elettroniche) come parametri di input.</span><span class="sxs-lookup"><span data-stu-id="a2d51-113">In the preceding code example, the GetDirectSoundGuid function accepts a data-flow direction (eRender or eCapture) and a device role (eConsole, eMultimedia, or eCommunications) as input parameters.</span></span> <span data-ttu-id="a2d51-114">Il terzo parametro è un puntatore tramite il quale la funzione scrive un GUID del dispositivo che l'applicazione può fornire come parametro di input per la funzione **DirectSoundCreate** o **DirectSoundCaptureCreate** .</span><span class="sxs-lookup"><span data-stu-id="a2d51-114">The third parameter is a pointer through which the function writes a device GUID that the application can supply as an input parameter to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function.</span></span>

<span data-ttu-id="a2d51-115">Nell'esempio di codice precedente viene ottenuto il GUID del dispositivo DirectSound da:</span><span class="sxs-lookup"><span data-stu-id="a2d51-115">The preceding code example obtains the DirectSound device GUID by:</span></span>

-   <span data-ttu-id="a2d51-116">Creazione di un'istanza dell'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) che rappresenta il dispositivo dell'endpoint audio con la direzione del flusso di dati e il ruolo del dispositivo specificati.</span><span class="sxs-lookup"><span data-stu-id="a2d51-116">Creating an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface instance that represents the audio endpoint device that has the specified data-flow direction and device role.</span></span>
-   <span data-ttu-id="a2d51-117">Apertura dell'archivio delle proprietà del dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="a2d51-117">Opening the property store of the audio endpoint device.</span></span>
-   <span data-ttu-id="a2d51-118">Recupero della proprietà [**pkey \_ AudioEndpoint \_ GUID**](pkey-audioendpoint-guid.md) dall'archivio delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="a2d51-118">Getting the [**PKEY\_AudioEndpoint\_GUID**](pkey-audioendpoint-guid.md) property from the property store.</span></span> <span data-ttu-id="a2d51-119">Il valore della proprietà è una rappresentazione in forma di stringa del GUID del dispositivo DirectSound per il dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="a2d51-119">The property value is a string representation of the DirectSound device GUID for the audio endpoint device.</span></span>
-   <span data-ttu-id="a2d51-120">Chiamata della funzione [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) per convertire la rappresentazione di stringa del GUID del dispositivo in una struttura Guid.</span><span class="sxs-lookup"><span data-stu-id="a2d51-120">Calling the [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) function to convert the string representation of the device GUID to a GUID structure.</span></span> <span data-ttu-id="a2d51-121">Per ulteriori informazioni su **CLSIDFromString**, vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a2d51-121">For more information about **CLSIDFromString**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="a2d51-122">Dopo aver ottenuto un GUID di dispositivo dalla funzione GetDirectSoundGuid, l'applicazione può chiamare **DirectSoundCreate** o **DIRECTSOUNDCAPTURECREATE** con questo GUID per creare il dispositivo di rendering o acquisizione DirectSound che incapsula il dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="a2d51-122">After obtaining a device GUID from the GetDirectSoundGuid function, the application can call **DirectSoundCreate** or **DirectSoundCaptureCreate** with this GUID to create the DirectSound rendering or capture device that encapsulates the audio endpoint device.</span></span> <span data-ttu-id="a2d51-123">Quando DirectSound crea un dispositivo in questo modo, assegna sempre il flusso audio del dispositivo alla sessione predefinita, ovvero la sessione audio specifica del processo identificata dal GUID del valore GUID della sessione \_ null.</span><span class="sxs-lookup"><span data-stu-id="a2d51-123">When DirectSound creates a device in this way, it always assigns the device's audio stream to the default session—the process-specific audio session that is identified by the session GUID value GUID\_NULL.</span></span>

<span data-ttu-id="a2d51-124">Se l'applicazione richiede DirectSound per assegnare il flusso a una sessione audio tra processi o a una sessione con un GUID di sessione non **null** , deve chiamare il metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) per creare un oggetto **IDirectSound** o **IDirectSoundCapture** invece di usare la tecnica illustrata nell'esempio di codice precedente.</span><span class="sxs-lookup"><span data-stu-id="a2d51-124">If the application requires DirectSound to assign the stream to a cross-process audio session or to a session with a non-**NULL** session GUID, it should call the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to create an **IDirectSound** or **IDirectSoundCapture** object instead of using the technique shown in the preceding code example.</span></span> <span data-ttu-id="a2d51-125">Per un esempio di codice che illustra come usare il metodo **Activate** per specificare una sessione audio tra processi o un GUID di sessione non **null** per un flusso, vedere [ruoli del dispositivo per le applicazioni DirectShow](device-roles-for-directshow-applications.md).</span><span class="sxs-lookup"><span data-stu-id="a2d51-125">For a code example that shows how to use the **Activate** method to specify a cross-process audio session or a non-**NULL** session GUID for a stream, see [Device Roles for DirectShow Applications](device-roles-for-directshow-applications.md).</span></span> <span data-ttu-id="a2d51-126">Nell'esempio di codice riportato in questa sezione viene illustrato come creare un filtro DirectShow, ma, con modifiche minime, il codice può essere adattato per creare un dispositivo DirectSound.</span><span class="sxs-lookup"><span data-stu-id="a2d51-126">The code example in that section shows how to create a DirectShow filter, but, with minor modifications, the code can be adapted to create a DirectSound device.</span></span>

<span data-ttu-id="a2d51-127">La funzione GetDirectSoundGuid nell'esempio di codice precedente chiama la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un enumeratore per i dispositivi dell'endpoint audio nel sistema.</span><span class="sxs-lookup"><span data-stu-id="a2d51-127">The GetDirectSoundGuid function in the preceding code example calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="a2d51-128">A meno che il programma chiamante abbia precedentemente chiamato la funzione [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare la libreria com, la chiamata **CoCreateInstance** avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="a2d51-128">Unless the calling program previously called either the [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="a2d51-129">Per ulteriori informazioni su **CoCreateInstance**, **CoInitialize** e **CoInitializeEx**, vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a2d51-129">For more information about **CoCreateInstance**, **CoInitialize**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2d51-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a2d51-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2d51-131">Interoperabilità con le API audio legacy</span><span class="sxs-lookup"><span data-stu-id="a2d51-131">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
