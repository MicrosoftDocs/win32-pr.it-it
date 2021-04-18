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
# <a name="getting-format-capabilities-through-iwmdmdevice"></a>Ottenere le funzionalità di formattazione tramite IWMDMDevice

Il metodo consigliato per l'esecuzione di query su un dispositivo per le funzionalità di riproduzione è [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability). Tuttavia, se un dispositivo non supporta questo metodo, l'applicazione può invece chiamare [**IWMDMDevice:: GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) per recuperare una matrice di formati audio supportati come strutture [**\_ WAVEFORMATEX**](-waveformatex.md) e formati MIME come stringhe dal dispositivo.

Nei passaggi seguenti viene illustrato come un'applicazione può utilizzare questo metodo per eseguire una query su un dispositivo per i formati supportati:

1.  Chiamare **GetFormatSupport** per recuperare matrici di formati audio e MIME.
2.  Scorrere i formati audio recuperati ed esaminare ogni struttura [**\_ WAVEFORMATEX**](-waveformatex.md) per provare a trovare un formato audio accettabile
3.  Scorrere le stringhe di formato MIME recuperate (se necessario) per trovare un tipo di file accettabile. L'SDK non definisce le costanti per i formati MIME. è consigliabile usare i valori standard del settore (disponibili nel sito Web iana.org). Un dispositivo dovrebbe elencare i tipi MIME specifici supportati.

Il codice C++ seguente illustra come recuperare le funzionalità di formattazione da un dispositivo, usando **GetFormatSupport**.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Individuazione delle funzionalità del formato del dispositivo**](discovering-device-format-capabilities.md)
</dt> <dt>

[**Ottenere le funzionalità di formato nei dispositivi che supportano IWMDMDevice3**](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
</dt> </dl>

 

 




