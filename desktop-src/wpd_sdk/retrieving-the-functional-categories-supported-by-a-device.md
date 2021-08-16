---
description: Recupero delle categorie funzionali supportate da un dispositivo
ms.assetid: 7748e111-9987-4685-8fc8-10c5d4631080
title: Recupero delle categorie funzionali supportate da un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d410788616cc20563b914a293afcd8e2bbbd87099f738ae21463d2092c620597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842693"
---
# <a name="retrieving-the-functional-categories-supported-by-a-device"></a>Recupero delle categorie funzionali supportate da un dispositivo

Windows I dispositivi portatili possono supportare una o più categorie funzionali. Queste categorie sono descritte nella tabella seguente.



| Category                    | Descrizione                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------|
| Acquisizione audio               | Il dispositivo può essere usato per registrare l'audio.                                              |
| Informazioni sul rendering       | Il dispositivo fornisce dati che descrivono i file multimediali di cui è in grado di eseguire il rendering. |
| Servizio messaggi brevi (SMS) | Il dispositivo supporta la messaggistica di testo.                                                  |
| Acquisizione di immagini non ancorate         | Il dispositivo può essere usato per acquisire immagini fisse.                                      |
| Archiviazione                     | Il dispositivo può essere usato per archiviare i file.                                               |



 

La funzione ListFunctionalCategories nel modulo DeviceCapabilities.cpp illustra il recupero delle categorie funzionali per un dispositivo selezionato.

L'applicazione può recuperare le categorie funzionali supportate da un dispositivo usando le interfacce descritte nella tabella seguente.



| Interfaccia                                                                                      | Descrizione                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Interfaccia IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Fornisce l'accesso ai metodi di recupero della categoria funzionale. |
| [**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Usato per enumerare e archiviare i dati della categoria funzionale.         |



 

La prima attività eseguita dall'applicazione di esempio è il recupero di un [**oggetto IPortableDeviceCapabilities,**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) usato per recuperare le categorie funzionali nel dispositivo selezionato.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}

// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get all functional categories supported by the device.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}
```



Le categorie recuperate vengono archiviate in [**un oggetto IPortableDevicePropVariantCollection.**](iportabledevicepropvariantcollection.md)

Il passaggio successivo è l'enumerazione e la visualizzazione delle categorie supportate. Il primo passaggio che viene eseguita dall'applicazione di esempio consiste nel recuperare il numero di categorie supportate. Usa quindi questo conteggio per scorrere [**l'oggetto IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che contiene le categorie supportate.


```C++
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumCategories; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pCategories->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have a functional category.  It is assumed that
            // functional categories are returned as VT_CLSID
            // VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the functional category name
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interfaccia IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 



