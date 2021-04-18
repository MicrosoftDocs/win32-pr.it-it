---
description: Proprietà dispositivo
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: Proprietà del dispositivo (API audio Core)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a868e4bb806bd49d934febed164bcd70fba39f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304423"
---
# <a name="device-properties-core-audio-apis"></a>Proprietà del dispositivo (API audio Core)

Durante il processo di enumerazione dei [dispositivi dell'endpoint audio](audio-endpoint-devices.md), un'applicazione client può interrogare gli oggetti endpoint per le relative proprietà del dispositivo. Le proprietà del dispositivo sono esposte nell'implementazione dell'API MMDevice dell'interfaccia **IPropertyStore** . Dato un riferimento all'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) di un oggetto endpoint, un client può ottenere un riferimento all'archivio delle proprietà dell'oggetto endpoint chiamando il metodo [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) .

L'oggetto archivio proprietà espone un'interfaccia **IPropertyStore** . I due metodi principali in questa interfaccia sono **IPropertyStore:: GetValue**, che ottiene un valore della proprietà del dispositivo e **IPropertyStore:: SetValue**, che imposta un valore della proprietà del dispositivo. Per ulteriori informazioni su **IPropertyStore**, vedere la documentazione Windows SDK.

L'implementazione dell'API MMDevice dell'archivio delle proprietà è diversa dall'oggetto archivio delle proprietà della shell standard. Per modificare il valore di una proprietà, è necessario che l'applicazione client chiami il metodo **IPropertyStore:: SetValue** . Durante questa chiamata, i nuovi valori vengono impostati e scritti nel registro di sistema. Pertanto, non è necessario che l'applicazione chiami il metodo **IPropertyStore:: commit** dopo la chiamata **SetValue** . L'handle per il registro di sistema viene chiuso solo quando il client rilascia il puntatore a interfaccia.

In genere, le applicazioni client di terze parti chiamano il metodo **GetValue** ma **non il metodo SetValue.** Gestione endpoint imposta le proprietà del dispositivo di base per gli endpoint. Gestione endpoint è il componente di Windows Vista responsabile del rilevamento della presenza di dispositivi endpoint audio.

Ogni \_ identificatore di proprietà pkey xxx nell'elenco seguente è una costante di tipo **PropertyKey** definito nel file di intestazione Functiondiscoverykeys \_ devpkey. h. Tutti i dispositivi endpoint audio hanno queste tre proprietà del dispositivo.



| Proprietà                                                                         | Descrizione                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ deviceinterface \_ FriendlyName**](pkey-deviceinterface-friendlyname.md) | Nome descrittivo della scheda audio a cui è collegato il dispositivo dell'endpoint (ad esempio, "scheda audio XYZ"). Il membro **PROPVARIANT** **VT** è impostato su VT \_ LPWSTR e il membro **pwszVal** punta a una stringa di caratteri wide con terminazione null che contiene il nome descrittivo. |
| [**\_DeviceDesc del dispositivo pkey \_**](pkey-device-devicedesc.md)                       | Descrizione del dispositivo dell'endpoint (ad esempio, "Speakers"). Il membro **PROPVARIANT** **VT** è impostato su VT \_ LPWSTR e il membro **pwszVal** punta a una stringa di caratteri wide con terminazione null che contiene la descrizione del dispositivo.                                       |
| [**PKEY \_ Device \_ FriendlyName**](pkey-device-friendlyname.md)                   | Nome descrittivo del dispositivo dell'endpoint (ad esempio, "altoparlanti (scheda audio XYZ)"). Il membro **PROPVARIANT** **VT** è impostato su VT \_ LPWSTR e il membro **pwszVal** punta a una stringa di caratteri wide con terminazione null che contiene il nome descrittivo.                             |



 

Alcuni dispositivi dell'endpoint audio potrebbero avere proprietà aggiuntive che non vengono visualizzate nell'elenco precedente. Per ulteriori informazioni sulle proprietà aggiuntive, vedere [proprietà dell'endpoint audio](audio-endpoint-properties.md). Per ulteriori informazioni su **PropertyKey**, vedere la documentazione Windows SDK.

Nell'esempio di codice seguente vengono stampati i nomi visualizzati di tutti i dispositivi dell'endpoint di rendering audio nel sistema:


```C++
//-----------------------------------------------------------
// This function enumerates all active (plugged in) audio
// rendering endpoint devices. It prints the friendly name
// and endpoint ID string of each endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

void PrintEndpointNames()
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDeviceCollection *pCollection = NULL;
    IMMDevice *pEndpoint = NULL;
    IPropertyStore *pProps = NULL;
    LPWSTR pwszID = NULL;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->EnumAudioEndpoints(
                        eRender, DEVICE_STATE_ACTIVE,
                        &pCollection);
    EXIT_ON_ERROR(hr)

    UINT  count;
    hr = pCollection->GetCount(&count);
    EXIT_ON_ERROR(hr)

    if (count == 0)
    {
        printf("No endpoints found.\n");
    }

    // Each loop prints the name of an endpoint device.
    for (ULONG i = 0; i < count; i++)
    {
        // Get pointer to endpoint number i.
        hr = pCollection->Item(i, &pEndpoint);
        EXIT_ON_ERROR(hr)

        // Get the endpoint ID string.
        hr = pEndpoint->GetId(&pwszID);
        EXIT_ON_ERROR(hr)
        
        hr = pEndpoint->OpenPropertyStore(
                          STGM_READ, &pProps);
        EXIT_ON_ERROR(hr)

        PROPVARIANT varName;
        // Initialize container for property value.
        PropVariantInit(&varName);

        // Get the endpoint's friendly-name property.
        hr = pProps->GetValue(
                       PKEY_Device_FriendlyName, &varName);
        EXIT_ON_ERROR(hr)

        // Print endpoint friendly name and endpoint ID.
        printf("Endpoint %d: \"%S\" (%S)\n",
               i, varName.pwszVal, pwszID);

        CoTaskMemFree(pwszID);
        pwszID = NULL;
        PropVariantClear(&varName);
        SAFE_RELEASE(pProps)
        SAFE_RELEASE(pEndpoint)
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    return;

Exit:
    printf("Error!\n");
    CoTaskMemFree(pwszID);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    SAFE_RELEASE(pEndpoint)
    SAFE_RELEASE(pProps)
}
```



La macro non riuscita nell'esempio di codice precedente viene definita nel file di intestazione Winerror. h.

Nell'esempio di codice precedente, il corpo del ciclo **for** nella funzione PrintEndpointNames chiama il metodo [**IMMDevice:: GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) per ottenere la [stringa dell'ID endpoint](endpoint-id-strings.md) per il dispositivo dell'endpoint audio rappresentato dall'istanza dell'interfaccia **IMMDevice** . La stringa identifica in modo univoco il dispositivo rispetto a tutti gli altri dispositivi dell'endpoint audio nel sistema. Un client può usare la stringa dell'ID endpoint per creare un'istanza del dispositivo dell'endpoint audio in un secondo momento o in un processo diverso chiamando il metodo [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) . I client devono trattare il contenuto della stringa dell'ID dell'endpoint come opaco. Ovvero i client non devono tentare di analizzare il contenuto della stringa per ottenere informazioni sul dispositivo. Il motivo è che il formato della stringa non è definito e può cambiare da un'implementazione dell'API MMDevice a quella successiva.

I nomi dei dispositivi descrittivi e le stringhe di ID endpoint ottenute dalla funzione PrintEndpointNames nell'esempio di codice precedente sono identici ai nomi dei dispositivi descrittivi e alle stringhe di ID endpoint fornite da DirectSound durante l'enumerazione del dispositivo. Per altre informazioni, vedere [eventi audio per le applicazioni audio legacy](audio-events-for-legacy-audio-applications.md).

Nell'esempio di codice precedente, la funzione PrintEndpointNames chiama la funzione **CoCreateInstance** per creare un enumeratore per i dispositivi dell'endpoint audio nel sistema. A meno che il programma chiamante abbia precedentemente chiamato la funzione **CoInitialize** o **CoInitializeEx** per inizializzare la libreria com, la chiamata **CoCreateInstance** avrà esito negativo. Per ulteriori informazioni su **CoCreateInstance**, **CoInitialize** e **CoInitializeEx**, vedere la documentazione Windows SDK.

Per altre informazioni sulle interfacce **IMMDeviceEnumerator**, **IMMDeviceCollection** e **IMMDevice** , vedere [API MMDevice](mmdevice-api.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi endpoint audio](audio-endpoint-devices.md)
</dt> </dl>

 

 



