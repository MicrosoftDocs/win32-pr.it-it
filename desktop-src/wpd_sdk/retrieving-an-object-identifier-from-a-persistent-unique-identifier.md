---
description: Recupero di un identificatore di oggetto da un identificatore univoco permanente
ms.assetid: 146f8943-d4e1-4b87-a812-e534082a4f14
title: Recupero di un ID oggetto da un ID univoco permanente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d4f08d496c7c03101602c945e6c27e7a2624fe84957eda932ead806f964d3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054771"
---
# <a name="retrieving-an-object-id-from-a-persistent-unique-id"></a>Recupero di un ID oggetto da un ID univoco permanente

È garantito che gli identificatori di oggetto siano univoci solo per una determinata sessione del dispositivo. se l'utente stabilisce una nuova connessione, gli identificatori di una sessione precedente potrebbero non corrispondere a identificatori per la sessione corrente. Per risolvere questo problema, l'API WPD supporta identificatori univoci persistenti (PUID), che vengono mantenuti tra le sessioni del dispositivo.

Alcuni dispositivi archiviano i propri PUID in modo nativo con un determinato oggetto. Altri possono generare il PUID in base a un hash dei dati dell'oggetto selezionato. Altri possono considerare gli identificatori di oggetto come PUID (perché possono garantire che questi identificatori non cambino mai).

La funzione GetObjectIdentifierFromPersistentUniqueIdentifier nel modulo ContentProperties.cpp illustra il recupero di un identificatore di oggetto per un PUID specificato.

L'applicazione può recuperare un identificatore di oggetto per un PUID corrispondente usando le interfacce descritte nella tabella seguente.



| Interfaccia                                                                                      | Descrizione                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**Interfaccia IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Fornisce l'accesso al metodo di recupero.                                                            |
| [**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Usato per archiviare sia l'identificatore di oggetto che l'identificatore univoco permanente (PUID) corrispondente. |



 

La prima attività eseguita dall'applicazione di esempio è ottenere un PUID dall'utente.


```C++
// Prompt user to enter an unique identifier to convert to an object idenifier.
printf("Enter the Persistant Unique Identifier of the object you wish to convert into an object identifier.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid persistent object identifier was specified, aborting the query operation\n");
}
```



Successivamente, l'applicazione di esempio recupera un [**oggetto IPortableDeviceContent,**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) che userà per richiamare il [**metodo GetObjectIDsFromPersistentUniqueIDs.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids)


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



Crea quindi un oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che contenerà il PUID fornito dall'utente.


```C++
hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPersistentUniqueIDs));
```



Dopo aver effettuato i tre passaggi precedenti, l'esempio è pronto per recuperare l'identificatore di oggetto corrispondente al PUID fornito dall'utente. Questa operazione viene eseguita chiamando il [**metodo IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) Prima di chiamare questo metodo, l'esempio inizializza una struttura PROPVARIANT, scrive il PUID fornito dall'utente in questa struttura e lo aggiunge all'oggetto IPortableDevicePropVariantCollection a cui punta pPersistentUniqueIDs. Questo puntatore viene passato come primo argomento al metodo GetObjectIDsFromPersistentUniqueIDs. Il secondo argomento di GetObjectIDsFromPersistentUniqueIDs è un oggetto IPortableDevicePropVariantCollection che riceve l'identificatore di oggetto corrispondente.


```C++
if (SUCCEEDED(hr))
{
    if (pPersistentUniqueIDs != NULL)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);

        // Initialize a PROPVARIANT structure with the object identifier string
        // that the user selected above. Notice we are allocating memory for the
        // PWSTR value.  This memory will be freed when PropVariantClear() is
        // called below.
        pv.vt      = VT_LPWSTR;
        pv.pwszVal = AtlAllocTaskWideString(szSelection);
        if (pv.pwszVal != NULL)
        {
            // Add the object identifier to the objects-to-delete list
            // (We are only deleting 1 in this example)
            hr = pPersistentUniqueIDs->Add(&pv);
            if (SUCCEEDED(hr))
            {
                // 3) Attempt to get the unique idenifier for the object from the device
                hr = pContent->GetObjectIDsFromPersistentUniqueIDs(pPersistentUniqueIDs,
                                                                   &pObjectIDs);
                if (SUCCEEDED(hr))
                {
                    PROPVARIANT pvId = {0};
                    hr = pObjectIDs->GetAt(0, &pvId);
                    if (SUCCEEDED(hr))
                    {
                        printf("The persistent unique identifier '%ws' relates to object identifier '%ws' on the device.\n", szSelection, pvId.pwszVal);
                    }
                    else
                    {
                        printf("! Failed to get the object identifier for '%ws' from the IPortableDevicePropVariantCollection, hr = 0x%lx\n",szSelection, hr);
                    }

                    // Free the returned allocated string from the GetAt() call
                    PropVariantClear(&pvId);
                }
                else
                {
                    printf("! Failed to get the object identifier from persistent object idenifier '%ws', hr = 0x%lx\n",szSelection, hr);
                }
            }
            else
            {
                printf("! Failed to get the object identifier from persistent object idenifier because we could no add the persistent object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
            printf("! Failed to get the object identifier because we could no allocate memory for the persistent object identifier string, hr = 0x%lx\n",hr);
        }

        // Free any allocated values in the PROPVARIANT before exiting
        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interfaccia IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 



