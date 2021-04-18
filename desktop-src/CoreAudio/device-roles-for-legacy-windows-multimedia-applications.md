---
description: Ruoli del dispositivo per applicazioni multimediali Windows legacy
ms.assetid: 54dcaa0e-2652-406d-ba24-c8885924acc6
title: Ruoli del dispositivo per applicazioni multimediali Windows legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a4ad6728659e4c865aed773575268844fe330e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320739"
---
# <a name="device-roles-for-legacy-windows-multimedia-applications"></a><span data-ttu-id="4a4f9-103">Ruoli del dispositivo per applicazioni multimediali Windows legacy</span><span class="sxs-lookup"><span data-stu-id="4a4f9-103">Device Roles for Legacy Windows Multimedia Applications</span></span>

> [!Note]  
> <span data-ttu-id="4a4f9-104">L'API MMDevice supporta i ruoli del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-104">The MMDevice API supports device roles.</span></span> <span data-ttu-id="4a4f9-105">Tuttavia, l'interfaccia utente in Windows Vista non implementa il supporto per questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-105">However, the user interface in Windows Vista does not implement support for this feature.</span></span> <span data-ttu-id="4a4f9-106">Il supporto dell'interfaccia utente per i ruoli del dispositivo può essere implementato in una versione futura di Windows.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-106">User interface support for device roles might be implemented in a future version of Windows.</span></span> <span data-ttu-id="4a4f9-107">Per ulteriori informazioni, vedere [ruoli del dispositivo in Windows Vista](device-roles-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="4a4f9-107">For more information, see [Device Roles in Windows Vista](device-roles-in-windows-vista.md).</span></span>

 

<span data-ttu-id="4a4f9-108">Le funzioni legacy di **waveOutXxx** e **WaveInXxx** multimediali di Windows non consentono a un'applicazione di selezionare il [dispositivo dell'endpoint audio](audio-endpoint-devices.md) assegnato dall'utente a un particolare [ruolo del dispositivo](device-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4a4f9-108">The legacy Windows multimedia **waveOutXxx** and **waveInXxx** functions provide no means for an application to select the [audio endpoint device](audio-endpoint-devices.md) that the user has assigned to a particular [device role](device-roles.md).</span></span> <span data-ttu-id="4a4f9-109">Tuttavia, in Windows Vista, le API di base audio possono essere utilizzate insieme a un'applicazione multimediale Windows per abilitare la selezione dei dispositivi in base al ruolo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-109">However, in Windows Vista, the core audio APIs can be used in conjunction with a Windows multimedia application to enable device selection based on device role.</span></span> <span data-ttu-id="4a4f9-110">Ad esempio, con l'aiuto dell' [API MMDevice](mmdevice-api.md), un'applicazione **waveOutXxx** è in grado di identificare il dispositivo dell'endpoint audio assegnato a un ruolo, identificare il dispositivo di output della forma d'onda corrispondente e chiamare la funzione **waveOutOpen** per aprire un'istanza del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-110">For example, with the help of the [MMDevice API](mmdevice-api.md), a **waveOutXxx** application can identify the audio endpoint device that is assigned to a role, identify the corresponding waveform output device, and call the **waveOutOpen** function to open an instance of the device.</span></span> <span data-ttu-id="4a4f9-111">Per ulteriori informazioni su **waveOutXxx** e **waveInXxx**, vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-111">For more information about **waveOutXxx** and **waveInXxx**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="4a4f9-112">Nell'esempio di codice seguente viene illustrato come ottenere l'ID del dispositivo waveform per il dispositivo dell'endpoint di rendering assegnato a un particolare ruolo del dispositivo:</span><span class="sxs-lookup"><span data-stu-id="4a4f9-112">The following code example shows how to obtain the waveform device ID for the rendering endpoint device that is assigned to a particular device role:</span></span>


```C++
//-----------------------------------------------------------
// This function gets the waveOut ID of the audio endpoint
// device that is currently assigned to the specified device
// role. The caller can use the waveOut ID to open the
// waveOut device that corresponds to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetWaveOutId(ERole role, int *pWaveOutId)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    WCHAR *pstrEndpointIdKey = NULL;
    WCHAR *pstrEndpointId = NULL;

    if (pWaveOutId == NULL)
    {
        return E_POINTER;
    }

    // Create an audio endpoint device enumerator.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the audio endpoint device that the user has
    // assigned to the specified device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    // Get the endpoint ID string of the audio endpoint device.
    hr = pDevice->GetId(&pstrEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Get the size of the endpoint ID string.
    size_t  cbEndpointIdKey;

    hr = StringCbLength(pstrEndpointIdKey,
                        STRSAFE_MAX_CCH * sizeof(WCHAR),
                        &cbEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Include terminating null in string size.
    cbEndpointIdKey += sizeof(WCHAR);

    // Allocate a buffer for a second string of the same size.
    pstrEndpointId = (WCHAR*)CoTaskMemAlloc(cbEndpointIdKey);
    if (pstrEndpointId == NULL)
    {
        EXIT_ON_ERROR(hr = E_OUTOFMEMORY)
    }

    // Each for-loop iteration below compares the endpoint ID
    // string of the audio endpoint device to the endpoint ID
    // string of an enumerated waveOut device. If the strings
    // match, then we've found the waveOut device that is
    // assigned to the specified device role.
    int waveOutId;
    int cWaveOutDevices = waveOutGetNumDevs();

    for (waveOutId = 0; waveOutId < cWaveOutDevices; waveOutId++)
    {
        MMRESULT mmr;
        size_t cbEndpointId;

        // Get the size (including the terminating null) of
        // the endpoint ID string of the waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEIDSIZE,
                             (DWORD_PTR)&cbEndpointId, NULL);
        if (mmr != MMSYSERR_NOERROR ||
            cbEndpointIdKey != cbEndpointId)  // do sizes match?
        {
            continue;  // not a matching device
        }

        // Get the endpoint ID string for this waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEID,
                             (DWORD_PTR)pstrEndpointId,
                             cbEndpointId);
        if (mmr != MMSYSERR_NOERROR)
        {
            continue;
        }

        // Check whether the endpoint ID string of this waveOut
        // device matches that of the audio endpoint device.
        if (lstrcmpi(pstrEndpointId, pstrEndpointIdKey) == 0)
        {
            *pWaveOutId = waveOutId;  // found match
            hr = S_OK;
            break;
        }
    }

    if (waveOutId == cWaveOutDevices)
    {
        // We reached the end of the for-loop above without
        // finding a waveOut device with a matching endpoint
        // ID string. This behavior is quite unexpected.
        hr = E_UNEXPECTED;
    }

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    CoTaskMemFree(pstrEndpointIdKey);  // NULL pointer okay
    CoTaskMemFree(pstrEndpointId);
    return hr;
}
```



<span data-ttu-id="4a4f9-113">Nell'esempio di codice precedente, la funzione GetWaveOutId accetta un ruolo del dispositivo (eConsole, eMultimedia o comunicazioni elettroniche) come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-113">In the preceding code example, the GetWaveOutId function accepts a device role (eConsole, eMultimedia, or eCommunications) as an input parameter.</span></span> <span data-ttu-id="4a4f9-114">Il secondo parametro è un puntatore tramite il quale la funzione scrive l'ID del dispositivo di forma d'onda per il dispositivo di output della forma d'onda assegnato al ruolo specificato.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-114">The second parameter is a pointer through which the function writes the waveform device ID for the waveform output device that is assigned to the specified role.</span></span> <span data-ttu-id="4a4f9-115">L'applicazione può quindi chiamare **waveOutOpen** con questo ID per aprire il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-115">The application can then call **waveOutOpen** with this ID to open the device.</span></span>

<span data-ttu-id="4a4f9-116">Il ciclo principale nell'esempio di codice precedente contiene due chiamate alla funzione **waveOutMessage** .</span><span class="sxs-lookup"><span data-stu-id="4a4f9-116">The main loop in the preceding code example contains two calls to the **waveOutMessage** function.</span></span> <span data-ttu-id="4a4f9-117">La prima chiamata invia un \_ messaggio DRV QUERYFUNCTIONINSTANCEIDSIZE per recuperare la dimensione, in byte, della [stringa ID dell'endpoint](endpoint-id-strings.md) del dispositivo waveform identificato dal parametro *waveOutId* .</span><span class="sxs-lookup"><span data-stu-id="4a4f9-117">The first call sends a DRV\_QUERYFUNCTIONINSTANCEIDSIZE message to retrieve the size, in bytes, of the [endpoint ID string](endpoint-id-strings.md) of the waveform device that is identified by the *waveOutId* parameter.</span></span> <span data-ttu-id="4a4f9-118">La stringa ID endpoint identifica il dispositivo dell'endpoint audio sottostante l'astrazione del dispositivo di forma d'onda. La dimensione indicata da questa chiamata include lo spazio per il carattere null di terminazione alla fine della stringa.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-118">(The endpoint ID string identifies the audio endpoint device that underlies the waveform device abstraction.) The size reported by this call includes the space for the terminating null character at the end of the string.</span></span> <span data-ttu-id="4a4f9-119">Il programma può utilizzare le informazioni sulle dimensioni per allocare un buffer sufficientemente grande da contenere l'intera stringa ID endpoint.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-119">The program can use the size information to allocate a buffer that is large enough to contain the entire endpoint ID string.</span></span>

<span data-ttu-id="4a4f9-120">La seconda chiamata a **waveOutMessage** Invia un \_ messaggio DRV QUERYFUNCTIONINSTANCEID per recuperare la stringa ID dispositivo del dispositivo di output della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-120">The second call to **waveOutMessage** sends a DRV\_QUERYFUNCTIONINSTANCEID message to retrieve the device ID string of the waveform output device.</span></span> <span data-ttu-id="4a4f9-121">Il codice di esempio Confronta questa stringa con la stringa ID dispositivo del dispositivo dell'endpoint audio con il ruolo del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-121">The example code compares this string to the device ID string of the audio endpoint device with the specified device role.</span></span> <span data-ttu-id="4a4f9-122">Se le stringhe corrispondono, la funzione scrive l'ID del dispositivo waveform nella posizione a cui punta il parametro *pWaveOutId*.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-122">If the strings match, then the function writes the waveform device ID to the location pointed to by parameter *pWaveOutId*.</span></span> <span data-ttu-id="4a4f9-123">Il chiamante può usare questo ID per aprire il dispositivo di output della forma d'onda con il ruolo del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-123">The caller can use this ID to open the waveform output device that has the specified device role.</span></span>

<span data-ttu-id="4a4f9-124">Windows Vista supporta i \_ messaggi DRV QUERYFUNCTIONINSTANCEIDSIZE e DRV \_ QUERYFUNCTIONINSTANCEID.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-124">Windows Vista supports the DRV\_QUERYFUNCTIONINSTANCEIDSIZE and DRV\_QUERYFUNCTIONINSTANCEID messages.</span></span> <span data-ttu-id="4a4f9-125">Non sono supportate nelle versioni precedenti di Windows, tra cui Windows Server 2003, Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-125">They are not supported in earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000.</span></span>

<span data-ttu-id="4a4f9-126">La funzione nell'esempio di codice precedente Ottiene l'ID del dispositivo di forma d'onda per un dispositivo di rendering, ma, con alcune modifiche, può essere adattato per ottenere l'ID del dispositivo waveform per un dispositivo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-126">The function in the preceding code example obtains the waveform device ID for a rendering device, but, with a few modifications, it can be adapted to obtain the waveform device ID for a capture device.</span></span> <span data-ttu-id="4a4f9-127">L'applicazione può quindi chiamare **waveInOpen** con questo ID per aprire il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-127">The application can then call **waveInOpen** with this ID to open the device.</span></span> <span data-ttu-id="4a4f9-128">Per modificare l'esempio di codice precedente per ottenere l'ID del dispositivo di forma d'onda per il dispositivo dell'endpoint di acquisizione audio assegnato a un ruolo specifico, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="4a4f9-128">To change the preceding code example to get the waveform device ID for the audio-capture endpoint device that is assigned to a particular role, do the following:</span></span>

-   <span data-ttu-id="4a4f9-129">Sostituire tutte le chiamate di funzione **waveOutXxx** nell'esempio precedente con le chiamate di funzione **waveInXxx** corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-129">Replace all of the **waveOutXxx** function calls in the preceding example with the corresponding **waveInXxx** function calls.</span></span>
-   <span data-ttu-id="4a4f9-130">Modificare il tipo di handle HWAVEOUT in HWAVEIN.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-130">Change handle type HWAVEOUT to HWAVEIN.</span></span>
-   <span data-ttu-id="4a4f9-131">Sostituire la costante di enumerazione [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ERender con eCapture.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-131">Replace [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration constant eRender with eCapture.</span></span>

<span data-ttu-id="4a4f9-132">In Windows Vista, le funzioni **waveOutOpen** e **waveInOpen** assegnano sempre i flussi audio creati nella sessione predefinita, ovvero la sessione specifica del processo identificata dal GUID del valore GUID della sessione \_ null.</span><span class="sxs-lookup"><span data-stu-id="4a4f9-132">In Windows Vista, the **waveOutOpen** and **waveInOpen** functions always assign the audio streams that they create to the default session—the process-specific session that is identified by the session GUID value GUID\_NULL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a4f9-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4a4f9-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a4f9-134">Interoperabilità con le API audio legacy</span><span class="sxs-lookup"><span data-stu-id="4a4f9-134">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



