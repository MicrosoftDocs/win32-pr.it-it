---
title: Ottenere le funzionalità di formattazione tramite IWMDMDevice
description: Ottenere le funzionalità di formato nei dispositivi che supportano solo IWMDMDevice
ms.assetid: bff079a1-d192-4e53-9b1d-9ad3b5dcca51
keywords:
- Windows Media Gestione dispositivi, funzionalità del dispositivo
- Gestione dispositivi, funzionalità del dispositivo
- Guida per programmatori, funzionalità del dispositivo
- applicazioni desktop, funzionalità del dispositivo
- creazione di applicazioni Windows Media Gestione dispositivi, funzionalità del dispositivo
- scrittura di file nei dispositivi, funzionalità del dispositivo
- Metodo IWMDMDevice
- Windows Media Gestione dispositivi, metodo IWMDMDevice
- Gestione dispositivi, metodo IWMDMDevice
- Guida per programmatori, metodo IWMDMDevice
- applicazioni desktop, metodo IWMDMDevice
- creazione di applicazioni Windows Media Gestione dispositivi, metodo IWMDMDevice
- scrittura di file nei dispositivi, metodo IWMDMDevice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a923919611b40197b1deed30e781042e008ef41
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/27/2019
ms.locfileid: "104335756"
---
# <a name="getting-format-capabilities-through-iwmdmdevice"></a><span data-ttu-id="5b773-116">Ottenere le funzionalità di formattazione tramite IWMDMDevice</span><span class="sxs-lookup"><span data-stu-id="5b773-116">Getting format capabilities through IWMDMDevice</span></span>

<span data-ttu-id="5b773-117">Il metodo consigliato per l'esecuzione di query su un dispositivo per le funzionalità di riproduzione è [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span><span class="sxs-lookup"><span data-stu-id="5b773-117">The recommended method for querying a device for its playback capabilities is [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span></span> <span data-ttu-id="5b773-118">Tuttavia, se un dispositivo non supporta questo metodo, l'applicazione può invece chiamare [**IWMDMDevice:: GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) per recuperare una matrice di formati audio supportati come strutture [**\_ WAVEFORMATEX**](-waveformatex.md) e formati MIME come stringhe dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5b773-118">However, if a device does not support this method, the application instead can call [**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) to retrieve an array of supported audio formats as [**\_WAVEFORMATEX**](-waveformatex.md) structures and MIME formats as strings from the device.</span></span>

<span data-ttu-id="5b773-119">Nei passaggi seguenti viene illustrato come un'applicazione può utilizzare questo metodo per eseguire una query su un dispositivo per i formati supportati:</span><span class="sxs-lookup"><span data-stu-id="5b773-119">The following steps show how an application can use this method to query a device for supported formats:</span></span>

1.  <span data-ttu-id="5b773-120">Chiamare **GetFormatSupport** per recuperare matrici di formati audio e MIME.</span><span class="sxs-lookup"><span data-stu-id="5b773-120">Call **GetFormatSupport** to retrieve arrays of both audio and mime formats.</span></span>
2.  <span data-ttu-id="5b773-121">Scorrere i formati audio recuperati ed esaminare ogni struttura [**\_ WAVEFORMATEX**](-waveformatex.md) per provare a trovare un formato audio accettabile</span><span class="sxs-lookup"><span data-stu-id="5b773-121">Loop through the retrieved audio formats and examine each [**\_WAVEFORMATEX**](-waveformatex.md) structure to try to find an acceptable audio format</span></span>
3.  <span data-ttu-id="5b773-122">Scorrere le stringhe di formato MIME recuperate (se necessario) per trovare un tipo di file accettabile.</span><span class="sxs-lookup"><span data-stu-id="5b773-122">Loop through the retrieved MIME format strings (if desired) to find an acceptable file type.</span></span> <span data-ttu-id="5b773-123">L'SDK non definisce le costanti per i formati MIME. è consigliabile usare i valori standard del settore (disponibili nel sito Web iana.org).</span><span class="sxs-lookup"><span data-stu-id="5b773-123">The SDK does not define constants for MIME formats; you should use industry standard values (which can be found at the iana.org Web site).</span></span> <span data-ttu-id="5b773-124">Un dispositivo dovrebbe elencare i tipi MIME specifici supportati.</span><span class="sxs-lookup"><span data-stu-id="5b773-124">A device should list the specific MIME types that it supports.</span></span>

<span data-ttu-id="5b773-125">Il codice C++ seguente illustra come recuperare le funzionalità di formattazione da un dispositivo, usando **GetFormatSupport**.</span><span class="sxs-lookup"><span data-stu-id="5b773-125">The following C++ code demonstrates retrieving format capabilities from a device, using **GetFormatSupport**.</span></span>


```C++
// Function to print out device caps for a device 
// that supports only IWMDMDevice.
void CWMDMController::GetCaps(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get all capabilities for audio and mime support.
    _WAVEFORMATEX* pAudioFormats;
    LPWSTR* pMimeFormats;
    UINT numAudioFormats = 0;
    UINT numMimeFormats = 0;
    hr = pDevice->GetFormatSupport(
        &pAudioFormats,
        &numAudioFormats,
        &pMimeFormats,
        &numMimeFormats);
    if (FAILED(hr)) return;

    // Print out audio format data.
    if (numAudioFormats > 0)
    {
        // TODO: Display a banner for the supported audio-format listing.
    }
    else
    {
        // TODO: Display a message indicating that no audio formats are supported.
    }
    for (int i = 0; i < numAudioFormats; i++)
    {
       // TODO: For each valid audio format, display the max channel, 
       // max samples/second, avg. bytes/sec, block alignment, and 
       // max bits/sample values.
    }

    // Print out MIME formats.
    if (numMimeFormats > 0)
        // TODO: Display a banner to precede the MIME format listing.
    else
        // TODO: Display a banner indicating that no MIME formats are supported.
    for (i = 0; i < numMimeFormats; i++)
    {
        // TODO: Display the specified MIME format.
    }
    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="5b773-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5b773-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b773-127">**Individuazione delle funzionalità del formato del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="5b773-127">**Discovering Device Format Capabilities**</span></span>](discovering-device-format-capabilities.md)
</dt> <dt>

[<span data-ttu-id="5b773-128">**Ottenere le funzionalità di formato nei dispositivi che supportano IWMDMDevice3**</span><span class="sxs-lookup"><span data-stu-id="5b773-128">**Getting Format Capabilities on Devices That Support IWMDMDevice3**</span></span>](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
</dt> </dl>

 

 




