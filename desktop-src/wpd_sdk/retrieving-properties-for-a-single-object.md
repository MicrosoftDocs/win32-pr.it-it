---
description: Recupero di proprietà per un singolo oggetto
ms.assetid: e4e3b286-6330-4147-a367-57accf5beae6
title: Recupero di proprietà per un singolo oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5851b31256659c2ca036bac504a53fa51a20ee14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315535"
---
# <a name="retrieving-properties-for-a-single-object"></a>Recupero di proprietà per un singolo oggetto

Dopo che l'applicazione ha recuperato un identificatore di oggetto (vedere l'argomento relativo all' [enumerazione del contenuto](enumerating-content.md) ) per un determinato oggetto, può recuperare informazioni descrittive sull'oggetto chiamando i metodi nell' [**interfaccia IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) e l' [**interfaccia IPortableDeviceKeyCollection**](iportabledevicekeycollection.md).

Il metodo [**IPortableDeviceProperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) recupera un elenco di proprietà specificate per un oggetto specificato. L'applicazione può anche chiamare il metodo GetValues e specificare un valore **null** per il parametro pKeys per recuperare tutte le proprietà per un determinato oggetto. Tuttavia, le prestazioni di questo metodo possono risultare significativamente più lente durante il recupero di tutte le proprietà.

Prima che l'applicazione chiami GetValues, tuttavia, deve identificare le proprietà da recuperare impostando le chiavi corrispondenti in un [**oggetto IPortableDeviceKeyCollection**](iportabledevicekeycollection.md). L'applicazione identificherà le proprietà di interesse chiamando il metodo [**IPortableDeviceKeyCollection:: Add**](iportabledevicekeycollection-add.md) e specificando un valore PropertyKey che identifichi ogni proprietà che verrà recuperata.

La funzione ReadContentProperties nel modulo ContentProperties. cpp dell'applicazione di esempio illustra come sono state recuperate le cinque proprietà per un oggetto selezionato. Nella tabella seguente vengono descritte le proprietà e il valore REFPROPERTYKEY corrispondente.



| Proprietà                     | Descrizione                                                                                                                                      | PROPERTYKEY                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| Identificatore oggetto padre     | Stringa che specifica l'identificatore per l'elemento padre dell'oggetto specificato.                                                                            | \_ \_ ID padre dell'oggetto WPD \_             |
| Nome dell'oggetto                  | Stringa che specifica il nome dell'oggetto specificato.                                                                                            | \_nome dell'oggetto WPD \_                   |
| Identificatore univoco permanente | Stringa che specifica un identificatore univoco per l'oggetto specificato. (Questo identificatore è persistente tra le sessioni, a differenza dell'identificatore dell'oggetto). | \_ \_ \_ ID univoco permanente dell'oggetto WPD \_ |
| Formato oggetto                | Identificatore univoco globale (GUID) che specifica il formato del file corrispondente a un oggetto specificato.                                       | \_formato oggetto \_ WPD                 |
| Tipo di contenuto Object          | GUID che specifica il tipo di contenuto associato a un oggetto specificato.                                                                        | \_tipo di \_ contenuto dell'oggetto WPD \_          |



 

Nell'estratto seguente della funzione ReadContentProperties viene illustrato il modo in cui l'applicazione di esempio utilizza l' [**interfaccia IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) e il metodo [**IPortableDeviceKeyCollection:: Add**](iportabledevicekeycollection-add.md) per identificare le proprietà recuperate.


```C++
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPropertiesToRead));
if (SUCCEEDED(hr))
{
    // 4) Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PARENT_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PARENT_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_NAME);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PERSISTENT_UNIQUE_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PERSISTENT_UNIQUE_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_FORMAT);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_FORMAT to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_CONTENT_TYPE);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_CONTENT_TYPE to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



Una volta che l'applicazione di esempio ha impostato le chiavi appropriate, ha chiamato il metodo [**IPortableDeviceProperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) per recuperare i valori specificati per l'oggetto specificato.


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(szSelection,         // The object whose properties we are reading
                                pPropertiesToRead,   // The properties we want to read
                                &pObjectProperties); // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interfaccia IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**Interfaccia IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 



