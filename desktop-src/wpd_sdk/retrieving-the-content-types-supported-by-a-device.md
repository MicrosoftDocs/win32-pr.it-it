---
description: Recupero dei tipi di contenuto supportati da un dispositivo
ms.assetid: 1cedb8d9-2476-420c-bab4-c8a032af781b
title: Recupero dei tipi di contenuto supportati da un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e1b37160065be3130fca687f5f3277d9108a6ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315534"
---
# <a name="retrieving-the-content-types-supported-by-a-device"></a>Recupero dei tipi di contenuto supportati da un dispositivo

Come indicato nell'argomento [recupero delle categorie funzionali supportate da un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) , i dispositivi portatili Windows possono supportare una o più categorie funzionali. Una determinata categoria funzionale può supportare uno o più tipi di contenuto. Ad esempio, la categoria archiviazione può supportare tipi di contenuto di cartelle, audio e immagini.

Per una descrizione dei tipi di contenuto supportati da WPD, vedere l' [**argomento \_ tipo di contenuto WPD \_ \_ All**](wpd-content-type-all.md) .

La funzione ListSupportedContentTypes nel modulo DeviceCapabilities. cpp illustra il recupero dei tipi di contenuto per le categorie funzionali supportate da un dispositivo selezionato.

L'applicazione può recuperare le categorie funzionali supportate da un dispositivo usando le interfacce descritte nella tabella seguente.



| Interfaccia                                                                                      | Descrizione                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Interfaccia IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Fornisce l'accesso ai metodi di recupero della categoria funzionale. |
| [**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Utilizzato per enumerare e archiviare i dati della categoria funzionale.         |



 

Il codice trovato nella funzione ListSupportedContentTypes è quasi identico al codice trovato nella funzione ListFunctionalCategories. Vedere l'argomento [recupero delle categorie funzionali supportate da un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) . L'unica differenza è rappresentata dalla chiamata al metodo [**IPortableDeviceCapabilities:: GetSupportedContentTypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) , che viene visualizzato all'interno del ciclo che scorre le categorie funzionali.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories   = 0;

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
// We will use these categories to enumerate functional objects
// that fall within them.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}

// Get the number of functional categories found on the device.
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name and supported content types.
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

            if ((pv.puuid != NULL)      &&
                (pv.vt    == VT_CLSID))
            {
                // Display the functional category name
                printf("Functional Category: ");
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");

                // Display the content types supported for this category
                CComPtr<IPortableDevicePropVariantCollection> pContentTypes;
                hr = pCapabilities->GetSupportedContentTypes(*pv.puuid, &pContentTypes);
                if (SUCCEEDED(hr))
                {
                    printf("Supported Content Types: ");
                    DisplayContentTypes(pContentTypes);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get supported content types from the device, hr = 0x%lx\n",hr);
                }
            }
            else
            {
                printf("! Invalid functional category found\n");
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

 

 



