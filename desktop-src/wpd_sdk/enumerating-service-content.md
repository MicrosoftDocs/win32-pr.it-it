---
description: Enumerazione del contenuto del servizio
ms.assetid: 4af4201c-d3f6-4630-91ec-6509c51871a5
title: Enumerazione del contenuto del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd9846565b7cdc4b0a4475cb99806b671452dcbe134e40d4b1e3d70df249c510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083565"
---
# <a name="enumerating-service-content"></a>Enumerazione del contenuto del servizio

Dopo l'apertura di un servizio, l'applicazione può iniziare a eseguire operazioni correlate al servizio. Nel caso dell'applicazione WpdServicesApiSample, una di queste operazioni è l'enumerazione del contenuto per un determinato servizio Contatti. Nella tabella seguente vengono descritte le interfacce utilizzate.



| Interfaccia                                                            | Descrizione                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | Usato per recuperare l'interfaccia IPortableDeviceContent2 per accedere al contenuto nel servizio.         |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | Usato per recuperare l'interfaccia IEnumPortableDeviceObjectIDs per enumerare gli oggetti nel servizio. |
| [**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids) | Utilizzato per enumerare gli oggetti nel servizio.                                                        |



 

Il codice di enumerazione del contenuto si trova nel modulo ContentEnumeration.cpp. Questo codice si trova nei **metodi EnumerateAllContent** e **RecursiveEnumerate.** Il primo metodo chiama il secondo.

Il **metodo EnumerateContent** accetta un puntatore a [**un oggetto IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) come unico parametro. Questo oggetto corrisponde a un servizio aperto in precedenza dall'applicazione quando ha chiamato il [**metodo IPortableDeviceService::Open.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open)

Il **metodo EnumerateContent** crea un [**oggetto IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) e lo passa al metodo [**IPortableDeviceService::Content.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) Questo metodo, a sua volta, recupera il contenuto al livello radice del servizio e quindi inizia in modo ricorsivo a recuperare il contenuto trovato sotto la radice.

Il codice seguente corrisponde al **metodo EnumerateContent.**


```C++
// Enumerate all content on the service starting with the
// "DEVICE" object
void EnumerateAllContent(
    IPortableDeviceService* pService)
{
    HRESULT                          hr = S_OK;
    CComPtr<IPortableDeviceContent2> pContent;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    hr = pService->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



Il codice seguente corrisponde al **metodo RecursiveEnumerate.** Il metodo RecursiveEnumerate crea un'istanza di un'interfaccia **IEnumPortableDeviceObjectIDs** per l'oggetto padre fornito e chiama **IEnumPortableDeviceObjectIDs::Next**, recuperando un batch di oggetti figlio immediati. Per ogni oggetto figlio, recursiveEnumerate viene chiamato nuovamente per restituire i relativi oggetti figlio discendenti e così via.


```C++
// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                   pszObjectID,
    IPortableDeviceContent2* pContent)
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
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent2, hr = 0x%lx\n",hr);
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

[**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[**Interfaccia IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**Interfaccia IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[Apertura di un servizio](opening-a-service.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



