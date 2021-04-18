---
description: Enumerazione del contenuto
ms.assetid: 86782a09-4fca-4ae0-beaf-296069e061dc
title: Enumerazione del contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2e724b451d714516c4723edcd56936b71e4e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306647"
---
# <a name="enumerating-content"></a>Enumerazione del contenuto

Il contenuto di un dispositivo (indipendentemente dal fatto che il contenuto sia una cartella, una rubrica, un video o un'immagine ancora) viene chiamato oggetto nell'API WPD. A questi oggetti viene fatto riferimento dagli identificatori di oggetto e descritti dalle proprietà. È possibile enumerare gli oggetti in un dispositivo chiamando i metodi nell' [**interfaccia IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), l' [**interfaccia IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)e l' [**interfaccia IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).

Nell'applicazione di esempio viene illustrata l'enumerazione del contenuto nella funzione EnumerateAllContent trovata nel modulo ContentEnumeration. cpp. Questa funzione, a sua volta, chiama una funzione RecursiveEnumerate che esamina la gerarchia di oggetti trovati nel dispositivo selezionato e restituisce un identificatore di oggetto per ogni oggetto.

Come indicato, la funzione RecursiveEnumerate recupera un identificatore di oggetto per ogni oggetto trovato nel dispositivo. L'identificatore dell'oggetto è un valore stringa. Quando l'applicazione recupera questo identificatore, può ottenere informazioni più descrittive sugli oggetti, ad esempio il nome dell'oggetto, l'identificatore per l'elemento padre dell'oggetto e così via. Queste informazioni descrittive sono denominate proprietà o metadati dell'oggetto. L'applicazione può recuperare queste proprietà chiamando membri dell' [**interfaccia IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties).

La funzione EnumerateAllContent inizia con il recupero di un puntatore a un' [**interfaccia IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent). Recupera questo puntatore chiamando il metodo [**IPortableDevice:: content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .


```C++
void EnumerateAllContent(
    IPortableDevice* pDevice)
{
    HRESULT                         hr = S_OK;
    CComPtr<IPortableDeviceContent> pContent;

    if (pDevice == NULL)
    {
        printf("! A NULL IPortableDevice interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent interface from the IPortableDevice interface to
    // access the content-specific methods.
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



Una volta recuperato il puntatore all'interfaccia IPortableDeviceContent, la funzione EnumerateAllContent chiama la funzione RecursiveEnumerate, che esamina la gerarchia di oggetti trovati nel dispositivo specificato e restituisce un identificatore di oggetto per ogni.

La funzione RecursiveEnumerate inizia con il recupero di un puntatore a un' [**interfaccia IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids). Questa interfaccia espone i metodi utilizzati da un'applicazione per spostarsi nell'elenco di oggetti individuati in un determinato dispositivo.

In questo esempio, la funzione RecursiveEnumerate chiama il metodo [**IEnumPortableDeviceObjectIDs:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) per scorrere l'elenco di oggetti.

Ogni chiamata al metodo [**IEnumPortableDeviceObjects:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) richiede un batch di 10 identificatori. (Questo valore è specificato dal \_ numero OGGETTI \_ da \_ richiedere una costante fornita come primo argomento.


```C++
#define NUM_OBJECTS_TO_REQUEST  10

// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                  pszObjectID,
    IPortableDeviceContent* pContent)
{
    CComPtr<IEnumPortableDeviceObjectIDs> pEnumObjectIDs;

    // Print the object identifier being used as the parent during enumeration.
    printf("%ws\n",pszObjectID);

    // Get an IEnumPortableDeviceObjectIDs interface by calling EnumObjects with the
    // specified parent object identifier.
    HRESULT hr = pContent->EnumObjects(0,               // Flags are unused
                                       pszObjectID,     // Starting from the passed in object
                                       NULL,            // Filter is unused
                                       &pEnumObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // Loop calling Next() while S_OK is being returned.
    while(hr == S_OK)
    {
        DWORD  cFetched = 0;
        PWSTR  szObjectIDArray[NUM_OBJECTS_TO_REQUEST] = {0};
        hr = pEnumObjectIDs->Next(NUM_OBJECTS_TO_REQUEST,   // Number of objects to request on each NEXT call
                                  szObjectIDArray,          // Array of PWSTR array which will be populated on each NEXT call
                                  &cFetched);               // Number of objects written to the PWSTR array
        if (SUCCEEDED(hr))
        {
            // Traverse the results of the Next() operation and recursively enumerate
            // Remember to free all returned object identifiers using CoTaskMemFree()
            for (DWORD dwIndex = 0; dwIndex < cFetched; dwIndex++)
            {
                RecursiveEnumerate(szObjectIDArray[dwIndex],pContent);

                // Free allocated PWSTRs after the recursive enumeration call has completed.
                CoTaskMemFree(szObjectIDArray[dwIndex]);
                szObjectIDArray[dwIndex] = NULL;
            }
        }
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[**Interfaccia IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interfaccia IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interfaccia IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 



