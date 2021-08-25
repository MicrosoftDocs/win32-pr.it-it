---
title: Ottenere funzionalità di formato tramite IWMDMDevice
description: Recupero delle funzionalità di formato nei dispositivi che supportano solo IWMDMDevice
ms.assetid: bff079a1-d192-4e53-9b1d-9ad3b5dcca51
keywords:
- Windows Gestione dispositivi multimediali, funzionalità del dispositivo
- Gestione dispositivi, funzionalità del dispositivo
- guida per programmatori, funzionalità del dispositivo
- applicazioni desktop, funzionalità dei dispositivi
- creazione Windows applicazioni di Gestione dispositivi multimediali, funzionalità del dispositivo
- scrittura di file in dispositivi, funzionalità del dispositivo
- Metodo IWMDMDevice
- Windows Media Device Manager,Metodo IWMDMDevice
- Gestione dispositivi, metodo IWMDMDevice
- Guida per programmatori,metodo IWMDMDevice
- applicazioni desktop, metodo IWMDMDevice
- creazione Windows applicazioni di Gestione dispositivi multimediali,metodo IWMDMDevice
- scrittura di file nei dispositivi, metodo IWMDMDevice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fe71969b48ded5616ee34e90a3420a77f468dfd9fb7f2cf0c6d14168a6fbb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957526"
---
# <a name="getting-format-capabilities-through-iwmdmdevice"></a>Ottenere funzionalità di formato tramite IWMDMDevice

Il metodo consigliato per eseguire query su un dispositivo per le funzionalità di riproduzione è [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability). Tuttavia, se un dispositivo non supporta questo metodo, l'applicazione può chiamare [**invece IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) per recuperare una matrice di formati audio supportati come [**\_ strutture WAVEFORMATEX**](-waveformatex.md) e formati MIME come stringhe dal dispositivo.

La procedura seguente illustra come un'applicazione può usare questo metodo per eseguire query su un dispositivo per trovare i formati supportati:

1.  Chiamare **GetFormatSupport** per recuperare matrici di formati audio e mime.
2.  Scorrere i formati audio recuperati ed esaminare ogni [**\_ struttura WAVEFORMATEX**](-waveformatex.md) per provare a trovare un formato audio accettabile
3.  Scorrere le stringhe di formato MIME recuperate (se necessario) per trovare un tipo di file accettabile. L'SDK non definisce costanti per i formati MIME. È consigliabile usare i valori standard del settore (disponibili nel iana.org Web). Un dispositivo deve elencare i tipi MIME specifici supportati.

Il codice C++ seguente illustra il recupero di funzionalità di formato da un dispositivo usando **GetFormatSupport**.


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

[**Recupero delle funzionalità di formato nei dispositivi che supportano IWMDMDevice3**](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
</dt> </dl>

 

 




