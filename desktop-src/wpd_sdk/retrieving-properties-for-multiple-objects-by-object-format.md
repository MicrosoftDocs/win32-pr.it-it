---
description: Recupero di proprietà per più oggetti in base al formato oggetto
ms.assetid: c3f5edfd-8a6a-4bbd-9787-a4268c38f18f
title: Recupero di proprietà per più oggetti in base al formato oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a352704b3ce5d063c544a41c467f372554bc901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485460"
---
# <a name="retrieving-properties-for-multiple-objects-by-object-format"></a>Recupero di proprietà per più oggetti in base al formato oggetto

Oltre al recupero in blocco delle proprietà di una raccolta di identificatori di oggetto, un'applicazione può anche eseguire un recupero in blocco delle proprietà di tutti gli oggetti di un determinato tipo. Come nell'esempio precedente, il recupero bulk per un tipo specificato richiede che il driver di dispositivo supporti il recupero in blocco.

L'applicazione può eseguire un recupero bulk usando le interfacce descritte nella tabella seguente.



| Interfaccia                                                                                      | Descrizione                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**Interfaccia IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Fornisce l'accesso ai metodi specifici del contenuto.                   |
| [**Interfaccia IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)                 | Utilizzato per identificare le proprietà da recuperare.                   |
| [**Interfaccia IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Utilizzato per determinare se un determinato driver supporta le operazioni bulk. |
| [**Interfaccia IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Supporta l'operazione di recupero in blocco.                             |
| [**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Utilizzato per archiviare gli identificatori di oggetto per l'operazione bulk.       |



 

La funzione ReadContentPropertiesBulkFilteringFormat nel modulo ContentProperties. cpp dell'applicazione di esempio illustra un'operazione di recupero bulk per oggetti di un tipo o formato specifico.

Il codice trovato nella funzione ReadContentPropertiesBulkFilteringFormat è quasi identico al codice trovato nella funzione ReadContentPropertiesBulk. Per una descrizione completa di questa funzione, vedere l'argomento [recupero delle proprietà per più oggetti](retrieving-properties-for-multiple-objects.md) .

La differenza principale si verifica quando l'operazione viene accodata. Quando si applica il filtro in base al tipo o al formato, viene chiamato il metodo [**IPortableDevicePropertiesBulk:: QueueGetValuesByObjectFormat**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectformat) anziché il metodo [**IPortableDevicePropertiesBulk:: QueueGetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist) .


```C++
hr = pPropertiesBulk->QueueGetValuesByObjectFormat(WPD_OBJECT_FORMAT_WMA,
                                                   WPD_DEVICE_OBJECT_ID,
                                                   100,
                                                   pPropertiesToRead,
                                                   pCallback,
                                                   &guidContext);
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

 

 



