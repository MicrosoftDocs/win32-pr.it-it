---
description: Recupero degli identificatori di oggetto funzionale per un dispositivo
ms.assetid: 9a13071a-95a1-4330-92d5-11fa72a8f211
title: Recupero degli identificatori di oggetto funzionale per un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d0cc686a6997c10e26e3d83190503bba09fe15afc7f4e0cf75e297f0d905f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119263001"
---
# <a name="retrieving-the-functional-object-identifiers-for-a-device"></a>Recupero degli identificatori di oggetto funzionale per un dispositivo

Come illustrato nell'argomento [Recupero](retrieving-the-functional-categories-supported-by-a-device.md) delle categorie funzionali supportate da un dispositivo, Windows dispositivi portatili possono supportare una o più categorie funzionali. Qualsiasi categoria funzionale specifica può supportare uno o più oggetti funzionali. Ad esempio, la categoria di archiviazione può supportare tre oggetti di archiviazione funzionali, ognuno dei quali è identificato da una stringa identificatore univoca. Il primo oggetto di archiviazione può quindi essere identificato dalla stringa "Storage1", il secondo dalla stringa "Storage2" e il terzo dalla stringa "Storage3".

La funzione ListFunctionalObjects nel modulo DeviceCapabilities.cpp illustra il recupero dei tipi di contenuto per le categorie funzionali supportate da un dispositivo selezionato.

L'applicazione può recuperare le categorie funzionali supportate da un dispositivo usando le interfacce descritte nella tabella seguente.



| Interfaccia                                                                                      | Descrizione                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Interfaccia IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Fornisce l'accesso ai metodi di recupero della categoria funzionale. |
| [**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Usato per enumerare e archiviare i dati della categoria funzionale.         |



 

Il codice trovato nella funzione ListFunctionalObjects è quasi identico al codice trovato nella funzione ListFunctionalCategories. Vedere [l'argomento Recupero di categorie funzionali supportate da un](retrieving-the-functional-categories-supported-by-a-device.md) dispositivo. L'unica differenza è la chiamata al metodo [**IPortableDeviceCapabilities::GetFunctionalObjects,**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) che viene visualizzato all'interno del ciclo che scorre le categorie funzionali.


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

// Loop through each functional category and get the list of
// functional object identifiers associated with a particular
// category.
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

                // Display the object identifiers for all
                // functional objects within this category
                CComPtr<IPortableDevicePropVariantCollection> pFunctionalObjectIds;
                hr = pCapabilities->GetFunctionalObjects(*pv.puuid, &pFunctionalObjectIds);
                if (SUCCEEDED(hr))
                {
                    printf("Functional Objects: ");
                    DisplayFunctionalObjectIDs(pFunctionalObjectIds);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
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

 

 



