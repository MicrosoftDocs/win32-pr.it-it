---
description: Recupero dei tipi di contenuto supportati da un dispositivo
ms.assetid: 1cedb8d9-2476-420c-bab4-c8a032af781b
title: Recupero dei tipi di contenuto supportati da un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f85366374ec28ed44664a3b86edbee1e046e1a5ee4e331dbe041398bdc48a9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083465"
---
# <a name="retrieving-the-content-types-supported-by-a-device"></a>Recupero dei tipi di contenuto supportati da un dispositivo

Come illustrato nell'argomento Recupero delle categorie funzionali supportate da un dispositivo, Windows dispositivi portatili possono supportare una o più categorie funzionali. [](retrieving-the-functional-categories-supported-by-a-device.md) Qualsiasi categoria funzionale specificata può supportare uno o più tipi di contenuto. Ad esempio, la categoria di archiviazione può supportare tipi di contenuto di cartella, audio e immagine.

Per una descrizione dei tipi di contenuto supportati da WPD, vedi l'argomento [**WPD CONTENT TYPE ALL (TIPO DI CONTENUTO WPD \_ \_ \_ ALL).**](wpd-content-type-all.md)

La funzione ListSupportedContentTypes nel modulo DeviceCapabilities.cpp illustra il recupero dei tipi di contenuto per le categorie funzionali supportate da un dispositivo selezionato.

L'applicazione può recuperare le categorie funzionali supportate da un dispositivo usando le interfacce descritte nella tabella seguente.



| Interfaccia                                                                                      | Descrizione                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Interfaccia IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Fornisce l'accesso ai metodi di recupero della categoria funzionale. |
| [**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Usato per enumerare e archiviare i dati delle categorie funzionali.         |



 

Il codice trovato nella funzione ListSupportedContentTypes è quasi identico al codice presente nella funzione ListFunctionalCategories. Vedere [l'argomento Recupero di categorie funzionali supportate da un](retrieving-the-functional-categories-supported-by-a-device.md) dispositivo. L'unica differenza è la chiamata al metodo [**IPortableDeviceCapabilities::GetSupportedContentTypes,**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) che viene visualizzata all'interno del ciclo che scorre le categorie funzionali.


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

 

 



