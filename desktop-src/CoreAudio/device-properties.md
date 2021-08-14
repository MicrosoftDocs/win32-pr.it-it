---
description: Proprietà dispositivo
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: Proprietà dispositivo (API audio di base)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e1a5068329ea2da794b68b777aa989a2e8b4a665df082982916942aa15b56e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407019"
---
# <a name="device-properties-core-audio-apis"></a>Proprietà dispositivo (API audio di base)

Durante il processo di enumerazione dei dispositivi [endpoint audio,](audio-endpoint-devices.md)un'applicazione client può interrogare gli oggetti endpoint per le relative proprietà del dispositivo. Le proprietà del dispositivo vengono esposte nell'implementazione dell'API MMDevice **dell'interfaccia IPropertyStore.** Dato un riferimento [**all'interfaccia IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) di un oggetto endpoint, un client può ottenere un riferimento all'archivio delle proprietà dell'oggetto endpoint chiamando il [**metodo IMMDevice::OpenPropertyStore.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore)

L'oggetto archivio proprietà espone **un'interfaccia IPropertyStore.** I due metodi principali in questa interfaccia sono **IPropertyStore::GetValue**, che ottiene un valore della proprietà del dispositivo, e **IPropertyStore::SetValue**, che imposta un valore della proprietà del dispositivo. Per altre informazioni su **IPropertyStore,** vedere la documentazione Windows SDK.

L'implementazione dell'API MMDevice dell'archivio delle proprietà è diversa dall'oggetto archivio delle proprietà della shell standard. Per modificare il valore di una proprietà, l'applicazione client deve chiamare il **metodo IPropertyStore::SetValue.** Durante questa chiamata, i nuovi valori vengono impostati e scritti nel Registro di sistema. Non è quindi necessario che l'applicazione chiami il **metodo IPropertyStore::Commit** dopo la **chiamata a SetValue.** L'handle per il Registro di sistema viene chiuso solo quando il client rilascia il puntatore di interfaccia.

In genere, le applicazioni client di terze parti chiamano **il metodo GetValue,** ma non il **metodo SetValue.** Gestione endpoint imposta le proprietà di base del dispositivo per gli endpoint. Gestione endpoint è il componente Windows Vista responsabile del rilevamento della presenza di dispositivi endpoint audio.

Ogni identificatore di proprietà PKEY Xxx nell'elenco seguente è una costante di tipo PROPERTYKEY definita nel file di intestazione \_ Functiondiscoverykeys  \_ devpkey.h. Tutti i dispositivi endpoint audio hanno queste tre proprietà del dispositivo.



| Proprietà                                                                         | Descrizione                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ DeviceInterface \_ FriendlyName**](pkey-deviceinterface-friendlyname.md) | Nome descrittivo della scheda audio a cui è collegato il dispositivo endpoint, ad esempio "Scheda audio XYZ". Il membro **PROPVARIANT** **vt** è impostato su VT LPWSTR e il membro \_ **pwszVal** punta a una stringa di caratteri wide con terminazione Null che contiene il nome descrittivo. |
| [**PKEY \_ Device \_ DeviceDesc**](pkey-device-devicedesc.md)                       | Descrizione del dispositivo endpoint, ad esempio "Speakers". Il membro **PROPVARIANT** **vt** è impostato su VT LPWSTR e il membro \_ **pwszVal** punta a una stringa di caratteri wide con terminazione Null che contiene la descrizione del dispositivo.                                       |
| [**PKEY \_ Device \_ FriendlyName**](pkey-device-friendlyname.md)                   | Nome descrittivo del dispositivo endpoint, ad esempio "Speakers (XYZ Audio Adapter)". Il membro **PROPVARIANT** **vt** è impostato su VT LPWSTR e il membro \_ **pwszVal** punta a una stringa di caratteri wide con terminazione Null che contiene il nome descrittivo.                             |



 

Alcuni dispositivi endpoint audio potrebbero avere proprietà aggiuntive che non vengono visualizzate nell'elenco precedente. Per altre informazioni sulle proprietà aggiuntive, vedere [Proprietà degli endpoint audio.](audio-endpoint-properties.md) Per altre informazioni su **PROPERTYKEY,** vedere la documentazione Windows SDK.

L'esempio di codice seguente stampa i nomi visualizzati di tutti i dispositivi endpoint di rendering audio nel sistema:


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



La macro FAILED nell'esempio di codice precedente è definita nel file di intestazione Winerror.h.

Nell'esempio di codice precedente il corpo del ciclo **for** nella funzione PrintEndpointNames chiama il metodo [**IMMDevice::GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) per ottenere la stringa [dell'ID endpoint](endpoint-id-strings.md) per il dispositivo endpoint audio rappresentato dall'istanza dell'interfaccia **IMMDevice.** La stringa identifica in modo univoco il dispositivo rispetto a tutti gli altri dispositivi endpoint audio nel sistema. Un client può usare la stringa dell'ID endpoint per creare un'istanza del dispositivo endpoint audio in un secondo momento o in un processo diverso chiamando il [**metodo IMMDeviceEnumerator::GetDevice.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) I client devono considerare il contenuto della stringa dell'ID endpoint come opaco. Ciò significa che i client non devono tentare di analizzare il contenuto della stringa per ottenere informazioni sul dispositivo. Il motivo è che il formato della stringa non è definito e potrebbe passare da un'implementazione dell'API MMDevice a quella successiva.

I nomi descrittivi dei dispositivi e le stringhe ID endpoint ottenuti dalla funzione PrintEndpointNames nell'esempio di codice precedente sono identici ai nomi descrittivi dei dispositivi e alle stringhe ID endpoint fornite da DirectSound durante l'enumerazione del dispositivo. Per altre informazioni, vedere [Eventi audio per applicazioni audio legacy.](audio-events-for-legacy-audio-applications.md)

Nell'esempio di codice precedente la funzione PrintEndpointNames chiama la **funzione CoCreateInstance** per creare un enumeratore per i dispositivi endpoint audio nel sistema. A meno che il programma chiamante non chiami in precedenza la funzione **CoInitialize** o **CoInitializeEx** per inizializzare la libreria COM, la **chiamata a CoCreateInstance** avrà esito negativo. Per altre informazioni su **CoCreateInstance,** **CoInitialize** e **CoInitializeEx,** vedere la documentazione Windows SDK.

Per altre informazioni sulle **interfacce IMMDeviceEnumerator,** **IMMDeviceCollection** e **IMMDevice,** vedere [API MMDevice.](mmdevice-api.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi endpoint audio](audio-endpoint-devices.md)
</dt> </dl>

 

 



