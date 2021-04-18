---
description: Recupero di proprietà per più oggetti
ms.assetid: 0d0c6b3d-23bc-4628-a684-14bb9e18967f
title: Recupero di proprietà per più oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c069f6a28b923339f66f8423f211eff4704ef6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317225"
---
# <a name="retrieving-properties-for-multiple-objects"></a>Recupero di proprietà per più oggetti

Alcuni driver di dispositivo supportano il recupero di proprietà per più oggetti in una singola chiamata di funzione. Questa operazione viene definita recupero in blocco. Esistono due tipi di operazioni di recupero bulk: il primo tipo recupera le proprietà per un elenco di oggetti e il secondo tipo recupera le proprietà per tutti gli oggetti di un determinato formato. Nell'esempio descritto in questa sezione viene illustrata la prima.

L'applicazione può eseguire un recupero bulk usando le interfacce descritte nella tabella seguente.



| Interfaccia                                                                                      | Descrizione                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**Interfaccia IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Fornisce l'accesso ai metodi specifici del contenuto.                   |
| [**Interfaccia IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)                 | Utilizzato per identificare le proprietà da recuperare.                   |
| [**Interfaccia IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Utilizzato per determinare se un determinato driver supporta le operazioni bulk. |
| [**Interfaccia IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Supporta l'operazione di recupero in blocco.                             |
| [**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Utilizzato per archiviare gli identificatori di oggetto per l'operazione bulk.       |



 

La funzione ReadContentPropertiesBulk nel modulo ContentProperties. cpp dell'applicazione di esempio illustra un'operazione di recupero in blocco.

La prima attività eseguita in questo esempio è determinare se il driver specificato supporta le operazioni bulk. Questa operazione viene eseguita chiamando QueryInterface sull'interfaccia IPortableDeviceProperties e verificando l'esistenza di IPortableDevicePropertiesBulk.


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CGetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceKeyCollection>         pPropertiesToRead;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;


if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pProperties->QueryInterface(IID_PPV_ARGS(&pPropertiesBulk));
    if (FAILED(hr))
    {
        printf("This driver does not support BULK property operations.\n");
    }
}
```



Se il driver supporta le operazioni bulk, il passaggio successivo consiste nel creare un'istanza dell' [**interfaccia IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) e specificare le chiavi che corrispondono alle proprietà che l'applicazione recupererà. Per una descrizione di questo processo, vedere l'argomento [recupero delle proprietà per un singolo oggetto](retrieving-properties-for-a-single-object.md) .

Una volta specificate le chiavi appropriate, l'applicazione di esempio crea un'istanza dell' [**interfaccia IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk). L'applicazione utilizzerà i metodi in questa interfaccia per tenere traccia dello stato di avanzamento dell'operazione di recupero bulk asincrono.


```C++
if (SUCCEEDED(hr))
{
    pCallback = new CGetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CGetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



La funzione successiva chiamata dall'applicazione di esempio è la funzione di supporto CreateIPortableDevicePropVariantCollectionWithAllObjectIDs. Questa funzione crea un elenco di tutti gli identificatori di oggetto disponibili, ad esempio scopi. Un'applicazione reale limita l'elenco di identificatori a un particolare set di oggetti. Ad esempio, un'applicazione può creare un elenco di identificatori per tutti gli oggetti attualmente presenti in una determinata visualizzazione di cartelle.

Come indicato in precedenza, la funzione helper enumera in modo ricorsivo tutti gli oggetti in un determinato dispositivo. Restituisce questo elenco in un' [**interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che contiene un identificatore per ogni oggetto trovato. La funzione helper è definita nel modulo ContentEnumeration. cpp.


```C++
// 7) Call our helper function CreateIPortableDevicePropVariantCollectionWithAllObjectIDs
// to enumerate and create an IPortableDevicePropVariantCollection with the object
// identifiers needed to perform the bulk operation on.
if (SUCCEEDED(hr))
{
    hr = CreateIPortableDevicePropVariantCollectionWithAllObjectIDs(pDevice,
                                                                    pContent,
                                                                    &pObjectIDs);
}
```



Una volta eseguiti i passaggi precedenti, l'applicazione di esempio avvia il recupero asincrono della proprietà. Questa operazione viene eseguita eseguendo le operazioni seguenti:

1.  Chiamata di IPortableDevicePropertiesBulk:: QueueGetValuesByObjectList, che accoda una richiesta per il recupero della proprietà bulk. Si noti che anche se la richiesta viene accodata, non è stata avviata.
2.  Chiamata di IPortableDevicePropertiesBulk:: Start per avviare la richiesta in coda.

Questi passaggi sono illustrati nell'estratto di codice seguente nell'applicazione di esempio.


```C++
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueGetValuesByObjectList(pObjectIDs,
                                                        pPropertiesToRead,
                                                        pCallback,
                                                        &guidContext);


       if(SUCCEEDED(hr))
       {
           // Cleanup any previously created global event handles.
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               CloseHandle(g_hBulkPropertyOperationEvent);
               g_hBulkPropertyOperationEvent = NULL;
           }

           // In order to create a simpler to follow example we create and wait infinitly
           // for the bulk property operation to complete and ignore any errors.
           // Production code should be written in a more robust manner.
           // Create the global event handle to wait on for the bulk operation
           // to complete.
           g_hBulkPropertyOperationEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               // Call Start() to actually being the Asynchronous bulk operation.
               hr = pPropertiesBulk->Start(guidContext);
               if(FAILED(hr))
               {
                   printf("! Failed to start property operation, hr = 0x%lx\n", hr);
               }
           }
           else
           {
               printf("! Failed to create the global event handle to wait on for the bulk operation. Aborting operation.\n");
           }
       }
       else
       {
           printf("! QueueGetValuesByObjectList Failed, hr = 0x%lx\n", hr);
       }
   }
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interfaccia IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interfaccia IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**Interfaccia IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Interfaccia IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 



