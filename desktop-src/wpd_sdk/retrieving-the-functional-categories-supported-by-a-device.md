---
description: Recupero delle categorie funzionali supportate da un dispositivo
ms.assetid: 7748e111-9987-4685-8fc8-10c5d4631080
title: Recupero delle categorie funzionali supportate da un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6514c6255fa089dc235b5edd8a25b5ef581aee84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883386"
---
# <a name="retrieving-the-functional-categories-supported-by-a-device"></a>Recupero delle categorie funzionali supportate da un dispositivo

I dispositivi portatili Windows possono supportare una o più categorie funzionali. Queste categorie sono descritte nella tabella seguente.



| Category                    | Descrizione                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------|
| Acquisizione audio               | Il dispositivo può essere usato per registrare l'audio.                                              |
| Informazioni sul rendering       | Il dispositivo fornisce dati che descrivono i file multimediali che è in grado di eseguire il rendering. |
| SMS (Short Message Service) | Il dispositivo supporta la messaggistica testuale.                                                  |
| Acquisizione immagini ancora         | Il dispositivo può essere usato per acquisire le immagini ancora.                                      |
| Archiviazione                     | Il dispositivo può essere usato per archiviare i file.                                               |



 

La funzione ListFunctionalCategories nel modulo DeviceCapabilities. cpp illustra il recupero delle categorie funzionali per un dispositivo selezionato.

L'applicazione può recuperare le categorie funzionali supportate da un dispositivo usando le interfacce descritte nella tabella seguente.



| Interfaccia                                                                                      | Descrizione                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Interfaccia IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Fornisce l'accesso ai metodi di recupero della categoria funzionale. |
| [**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Utilizzato per enumerare e archiviare i dati della categoria funzionale.         |



 

La prima attività eseguita dall'applicazione di esempio è il recupero di un oggetto [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , che viene usato per recuperare le categorie funzionali sul dispositivo selezionato.


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



Le categorie recuperate vengono archiviate in un oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .

Il passaggio successivo è l'enumerazione e la visualizzazione delle categorie supportate. Il primo passaggio da eseguire per l'applicazione di esempio è recuperare il numero di categorie supportate. USA quindi questo conteggio per scorrere l'oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che contiene le categorie supportate.


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

 

 



