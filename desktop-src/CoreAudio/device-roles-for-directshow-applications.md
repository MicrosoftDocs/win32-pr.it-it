---
description: Ruoli del dispositivo per DirectShow applicazioni
ms.assetid: 54f42bda-b4a0-465c-9ce6-9102d2908776
title: Ruoli del dispositivo per DirectShow applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e22a86e5537f11b6b4153753841a2682b5ac77a043a3fa74538714a2540377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957360"
---
# <a name="device-roles-for-directshow-applications"></a>Ruoli del dispositivo per DirectShow applicazioni

> [!Note]  
> [L'API MMDevice](mmdevice-api.md) supporta i ruoli del dispositivo. Tuttavia, l'interfaccia utente in Windows Vista non implementa il supporto per questa funzionalità. Il supporto dell'interfaccia utente per i ruoli del dispositivo potrebbe essere implementato in una versione futura di Windows. Per altre informazioni, vedere [Ruoli del dispositivo in Windows Vista](device-roles-in-windows-vista.md).

 

L DirectShow API non fornisce un mezzo per un'applicazione per selezionare il dispositivo [endpoint audio](audio-endpoint-devices.md) assegnato a un particolare [ruolo del dispositivo.](device-roles.md) Tuttavia, in Windows Vista, le API audio di base possono essere usate insieme a un'applicazione DirectShow per abilitare la selezione dei dispositivi in base al ruolo del dispositivo. Con l'aiuto delle API audio di base, l'applicazione può:

-   Identificare il dispositivo endpoint audio assegnato dall'utente a un ruolo del dispositivo specifico.
-   Creare un filtro DirectShow rendering audio con [**un'interfaccia IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) che incapsula il dispositivo endpoint audio.
-   Creare un DirectShow grafico che incorpora il filtro.

Per altre informazioni su DirectShow [**e IBaseFilter,**](/windows/desktop/api/strmif/nn-strmif-ibasefilter)vedere la documentazione Windows SDK.

L'esempio di codice seguente illustra come creare un filtro DirectShow rendering audio che incapsula il dispositivo endpoint di rendering assegnato a un ruolo di dispositivo specifico:


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



Nell'esempio di codice precedente la funzione CreateAudioRenderer accetta un ruolo del dispositivo (eConsole, eMultimedia o eCommunications) come parametro di input. Il secondo parametro è un puntatore tramite il quale la funzione scrive l'indirizzo di [**un'istanza dell'interfaccia IBaseFilter.**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) L'esempio illustra anche come usare il metodo [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) per assegnare il flusso audio nell'istanza **di IBaseFilter** a una sessione audio cross-process con un GUID di sessione specifico dell'applicazione (specificato dalla costante **guidAudioSessionId).** Il terzo parametro nella chiamata **Activate** punta a una struttura che contiene il GUID della sessione e il flag tra processi. Se l'utente esegue più istanze dell'applicazione, i flussi audio di tutte le istanze usano lo stesso GUID di sessione e quindi appartengono alla stessa sessione.

In alternativa, il chiamante può specificare **NULL** come terzo parametro nella chiamata [**Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) per assegnare il flusso alla sessione predefinita come sessione specifica del processo con valore GUID di sessione \_ NULL. Per altre informazioni, vedere **IMMDevice::Activate**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interoperabilità con LE API audio legacy](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
