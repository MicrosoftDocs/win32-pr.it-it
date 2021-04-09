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
# <a name="device-roles-for-directsound-applications"></a>Ruoli del dispositivo per le applicazioni DirectSound

> [!Note]  
> L' [API MMDevice](mmdevice-api.md) supporta i ruoli del dispositivo. Tuttavia, l'interfaccia utente in Windows Vista non implementa il supporto per questa funzionalità. Il supporto dell'interfaccia utente per i ruoli del dispositivo può essere implementato in una versione futura di Windows. Per ulteriori informazioni, vedere [ruoli del dispositivo in Windows Vista](device-roles-in-windows-vista.md).

 

L'API DirectSound non fornisce un mezzo per consentire a un'applicazione di selezionare il [dispositivo dell'endpoint audio](audio-endpoint-devices.md) assegnato dall'utente a un particolare [ruolo del dispositivo](device-roles.md). Tuttavia, in Windows Vista, le API di base audio possono essere usate insieme a un'applicazione DirectSound per abilitare la selezione dei dispositivi in base al ruolo del dispositivo. Con l'ausilio delle API di base audio, l'applicazione è in grado di identificare il dispositivo dell'endpoint audio assegnato a un ruolo specifico, ottenere il GUID del dispositivo DirectSound per il dispositivo endpoint e chiamare la funzione **DirectSoundCreate** o **DirectSoundCaptureCreate** per creare un'istanza dell'interfaccia **IDirectSound** o **IDirectSoundCapture** che incapsula il dispositivo dell'endpoint. Per ulteriori informazioni su DirectSound, vedere la documentazione di Windows SDK.

Nell'esempio di codice seguente viene illustrato come ottenere il GUID del dispositivo DirectSound per il dispositivo di rendering o acquisizione attualmente assegnato a un particolare ruolo del dispositivo:


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



Nell'esempio di codice precedente, la funzione GetDirectSoundGuid accetta una direzione del flusso di dati (eRender o eCapture) e un ruolo del dispositivo (eConsole, eMultimedia o comunicazioni elettroniche) come parametri di input. Il terzo parametro è un puntatore tramite il quale la funzione scrive un GUID del dispositivo che l'applicazione può fornire come parametro di input per la funzione **DirectSoundCreate** o **DirectSoundCaptureCreate** .

Nell'esempio di codice precedente viene ottenuto il GUID del dispositivo DirectSound da:

-   Creazione di un'istanza dell'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) che rappresenta il dispositivo dell'endpoint audio con la direzione del flusso di dati e il ruolo del dispositivo specificati.
-   Apertura dell'archivio delle proprietà del dispositivo dell'endpoint audio.
-   Recupero della proprietà [**pkey \_ AudioEndpoint \_ GUID**](pkey-audioendpoint-guid.md) dall'archivio delle proprietà. Il valore della proprietà è una rappresentazione in forma di stringa del GUID del dispositivo DirectSound per il dispositivo dell'endpoint audio.
-   Chiamata della funzione [**CLSIDFromString**](https://www.bing.com/search?q=**CLSIDFromString**) per convertire la rappresentazione di stringa del GUID del dispositivo in una struttura Guid. Per ulteriori informazioni su **CLSIDFromString**, vedere la documentazione Windows SDK.

Dopo aver ottenuto un GUID di dispositivo dalla funzione GetDirectSoundGuid, l'applicazione può chiamare **DirectSoundCreate** o **DIRECTSOUNDCAPTURECREATE** con questo GUID per creare il dispositivo di rendering o acquisizione DirectSound che incapsula il dispositivo dell'endpoint audio. Quando DirectSound crea un dispositivo in questo modo, assegna sempre il flusso audio del dispositivo alla sessione predefinita, ovvero la sessione audio specifica del processo identificata dal GUID del valore GUID della sessione \_ null.

Se l'applicazione richiede DirectSound per assegnare il flusso a una sessione audio tra processi o a una sessione con un GUID di sessione non **null** , deve chiamare il metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) per creare un oggetto **IDirectSound** o **IDirectSoundCapture** invece di usare la tecnica illustrata nell'esempio di codice precedente. Per un esempio di codice che illustra come usare il metodo **Activate** per specificare una sessione audio tra processi o un GUID di sessione non **null** per un flusso, vedere [ruoli del dispositivo per le applicazioni DirectShow](device-roles-for-directshow-applications.md). Nell'esempio di codice riportato in questa sezione viene illustrato come creare un filtro DirectShow, ma, con modifiche minime, il codice può essere adattato per creare un dispositivo DirectSound.

La funzione GetDirectSoundGuid nell'esempio di codice precedente chiama la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un enumeratore per i dispositivi dell'endpoint audio nel sistema. A meno che il programma chiamante abbia precedentemente chiamato la funzione [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare la libreria com, la chiamata **CoCreateInstance** avrà esito negativo. Per ulteriori informazioni su **CoCreateInstance**, **CoInitialize** e **CoInitializeEx**, vedere la documentazione Windows SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interoperabilità con le API audio legacy](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
