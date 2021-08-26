---
description: Recupero di proprietà per un singolo oggetto
ms.assetid: e4e3b286-6330-4147-a367-57accf5beae6
title: Recupero di proprietà per un singolo oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0806de3da9cd3f0674057d413a071996f86f5d74a364c0f5db707965fc2220
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054721"
---
# <a name="retrieving-properties-for-a-single-object"></a>Recupero di proprietà per un singolo oggetto

Dopo che l'applicazione recupera un [](enumerating-content.md) identificatore di oggetto (vedere l'argomento Enumerazione del contenuto) per un determinato oggetto, può recuperare informazioni descrittive su tale oggetto chiamando i metodi nell'interfaccia [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) e nell'interfaccia [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md).

Il [**metodo IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) recupera un elenco di proprietà specificate per un determinato oggetto. L'applicazione può anche chiamare il metodo GetValues e specificare un valore **NULL** per il parametro pKeys per recuperare tutte le proprietà per un determinato oggetto. Tuttavia, le prestazioni di questo metodo potrebbero essere notevolmente più lente durante il recupero di tutte le proprietà.

Prima che l'applicazione chiami GetValues, tuttavia, deve identificare le proprietà da recuperare impostando le chiavi corrispondenti in un [**oggetto IPortableDeviceKeyCollection**](iportabledevicekeycollection.md). L'applicazione identificherà le proprietà di interesse chiamando il metodo [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) e fornendo un valore PROPERTYKEY che identifica ogni proprietà che recupererà.

La funzione ReadContentProperties nel modulo ContentProperties.cpp dell'applicazione di esempio illustra come sono state recuperate le cinque proprietà per un oggetto selezionato. Nella tabella seguente vengono descritte ognuna di queste proprietà e il valore REFPROPERTYKEY corrispondente.



| Proprietà                     | Descrizione                                                                                                                                      | PROPERTYKEY                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| Identificatore dell'oggetto padre     | Stringa che specifica l'identificatore per l'elemento padre dell'oggetto specificato.                                                                            | ID PADRE \_ DELL'OGGETTO WPD \_ \_             |
| Nome dell'oggetto                  | Stringa che specifica il nome dell'oggetto specificato.                                                                                            | NOME OGGETTO \_ WPD \_                   |
| Identificatore univoco permanente | Stringa che specifica un identificatore univoco per l'oggetto specificato. Questo identificatore è persistente tra le sessioni, a differenza dell'identificatore di oggetto. | \_ID UNIVOCO PERMANENTE DELL'OGGETTO WPD \_ \_ \_ |
| Formato oggetto                | Identificatore univoco globale (GUID) che specifica il formato del file corrispondente a un oggetto specificato.                                       | FORMATO \_ DELL'OGGETTO WPD \_                 |
| Tipo di contenuto dell'oggetto          | GUID che specifica il tipo di contenuto associato a un oggetto specificato.                                                                        | TIPO DI CONTENUTO \_ \_ DELL'OGGETTO \_ WPD          |



 

L'estratto seguente della funzione ReadContentProperties illustra come l'applicazione di esempio ha usato [**l'interfaccia IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) e il metodo [**IPortableDeviceKeyCollection::Add**](iportabledevicekeycollection-add.md) per identificare le proprietà recuperate.


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



Dopo che l'applicazione di esempio ha impostato le chiavi appropriate, ha chiamato il metodo [**IPortableDeviceProperties::GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) per recuperare i valori specificati per l'oggetto specificato.


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

 

 



