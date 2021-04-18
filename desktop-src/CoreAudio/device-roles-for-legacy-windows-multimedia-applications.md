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
# <a name="device-roles-for-legacy-windows-multimedia-applications"></a>Ruoli del dispositivo per applicazioni multimediali Windows legacy

> [!Note]  
> L'API MMDevice supporta i ruoli del dispositivo. Tuttavia, l'interfaccia utente in Windows Vista non implementa il supporto per questa funzionalità. Il supporto dell'interfaccia utente per i ruoli del dispositivo può essere implementato in una versione futura di Windows. Per ulteriori informazioni, vedere [ruoli del dispositivo in Windows Vista](device-roles-in-windows-vista.md).

 

Le funzioni legacy di **waveOutXxx** e **WaveInXxx** multimediali di Windows non consentono a un'applicazione di selezionare il [dispositivo dell'endpoint audio](audio-endpoint-devices.md) assegnato dall'utente a un particolare [ruolo del dispositivo](device-roles.md). Tuttavia, in Windows Vista, le API di base audio possono essere utilizzate insieme a un'applicazione multimediale Windows per abilitare la selezione dei dispositivi in base al ruolo del dispositivo. Ad esempio, con l'aiuto dell' [API MMDevice](mmdevice-api.md), un'applicazione **waveOutXxx** è in grado di identificare il dispositivo dell'endpoint audio assegnato a un ruolo, identificare il dispositivo di output della forma d'onda corrispondente e chiamare la funzione **waveOutOpen** per aprire un'istanza del dispositivo. Per ulteriori informazioni su **waveOutXxx** e **waveInXxx**, vedere la documentazione Windows SDK.

Nell'esempio di codice seguente viene illustrato come ottenere l'ID del dispositivo waveform per il dispositivo dell'endpoint di rendering assegnato a un particolare ruolo del dispositivo:


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



Nell'esempio di codice precedente, la funzione GetWaveOutId accetta un ruolo del dispositivo (eConsole, eMultimedia o comunicazioni elettroniche) come parametro di input. Il secondo parametro è un puntatore tramite il quale la funzione scrive l'ID del dispositivo di forma d'onda per il dispositivo di output della forma d'onda assegnato al ruolo specificato. L'applicazione può quindi chiamare **waveOutOpen** con questo ID per aprire il dispositivo.

Il ciclo principale nell'esempio di codice precedente contiene due chiamate alla funzione **waveOutMessage** . La prima chiamata invia un \_ messaggio DRV QUERYFUNCTIONINSTANCEIDSIZE per recuperare la dimensione, in byte, della [stringa ID dell'endpoint](endpoint-id-strings.md) del dispositivo waveform identificato dal parametro *waveOutId* . La stringa ID endpoint identifica il dispositivo dell'endpoint audio sottostante l'astrazione del dispositivo di forma d'onda. La dimensione indicata da questa chiamata include lo spazio per il carattere null di terminazione alla fine della stringa. Il programma può utilizzare le informazioni sulle dimensioni per allocare un buffer sufficientemente grande da contenere l'intera stringa ID endpoint.

La seconda chiamata a **waveOutMessage** Invia un \_ messaggio DRV QUERYFUNCTIONINSTANCEID per recuperare la stringa ID dispositivo del dispositivo di output della forma d'onda. Il codice di esempio Confronta questa stringa con la stringa ID dispositivo del dispositivo dell'endpoint audio con il ruolo del dispositivo specificato. Se le stringhe corrispondono, la funzione scrive l'ID del dispositivo waveform nella posizione a cui punta il parametro *pWaveOutId*. Il chiamante può usare questo ID per aprire il dispositivo di output della forma d'onda con il ruolo del dispositivo specificato.

Windows Vista supporta i \_ messaggi DRV QUERYFUNCTIONINSTANCEIDSIZE e DRV \_ QUERYFUNCTIONINSTANCEID. Non sono supportate nelle versioni precedenti di Windows, tra cui Windows Server 2003, Windows XP e Windows 2000.

La funzione nell'esempio di codice precedente Ottiene l'ID del dispositivo di forma d'onda per un dispositivo di rendering, ma, con alcune modifiche, può essere adattato per ottenere l'ID del dispositivo waveform per un dispositivo di acquisizione. L'applicazione può quindi chiamare **waveInOpen** con questo ID per aprire il dispositivo. Per modificare l'esempio di codice precedente per ottenere l'ID del dispositivo di forma d'onda per il dispositivo dell'endpoint di acquisizione audio assegnato a un ruolo specifico, procedere come segue:

-   Sostituire tutte le chiamate di funzione **waveOutXxx** nell'esempio precedente con le chiamate di funzione **waveInXxx** corrispondenti.
-   Modificare il tipo di handle HWAVEOUT in HWAVEIN.
-   Sostituire la costante di enumerazione [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ERender con eCapture.

In Windows Vista, le funzioni **waveOutOpen** e **waveInOpen** assegnano sempre i flussi audio creati nella sessione predefinita, ovvero la sessione specifica del processo identificata dal GUID del valore GUID della sessione \_ null.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interoperabilità con le API audio legacy](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



