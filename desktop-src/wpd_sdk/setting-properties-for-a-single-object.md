---
description: Impostazione delle proprietà per un singolo oggetto
ms.assetid: 1c003534-96b4-419b-94d1-73b5ffa2eba1
title: Impostazione delle proprietà per un singolo oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5649d05ccadfeaef0dd8805abd7d556f7725f175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318675"
---
# <a name="setting-properties-for-a-single-object"></a>Impostazione delle proprietà per un singolo oggetto

Dopo che l'applicazione ha recuperato un identificatore di oggetto (vedere l'argomento relativo all' [enumerazione del contenuto](enumerating-content.md) ) per un determinato oggetto, può impostare le proprietà di tale oggetto chiamando i metodi nelle interfacce descritte nella tabella seguente.



| Interfaccia                                                                | Descrizione                                                                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interfaccia IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | Utilizzato per determinare se una determinata proprietà può essere scritta e inviare l'operazione di scrittura.                                                                  |
| [**Interfaccia IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | Fornisce l'accesso ai metodi specifici del contenuto.                                                                                                            |
| [**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)         | Utilizzato per contenere i valori da scrivere, determinare i risultati dell'operazione di scrittura e recuperare gli attributi delle proprietà (quando si determina la funzionalità di scrittura). |



 

Le applicazioni impostano le proprietà su un oggetto creando innanzitutto un contenitore di proprietà che specifica i nuovi valori usando l' [**interfaccia IPortableDeviceValues**](iportabledevicevalues.md). Una volta creato il contenitore delle proprietà, un'applicazione imposta tali proprietà chiamando il metodo [**IPortableDeviceProperties:: SetValue**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-setvalues) .

La `WriteContentProperties` funzione nel modulo ContentProperties. cpp dell'applicazione di esempio illustra come un'applicazione può impostare una nuova proprietà nome oggetto per un oggetto selezionato.

La prima attività eseguita dalla `WriteContentProperties` funzione consiste nel richiedere all'utente di immettere un identificatore di oggetto per l'oggetto per cui l'applicazione scriverà il nuovo nome.


```C++
HRESULT                               hr                   = S_OK;
WCHAR                                 szSelection[81]      = {0};
WCHAR                                 szNewObjectName[81]  = {0};
CComPtr<IPortableDeviceProperties>    pProperties;
CComPtr<IPortableDeviceContent>       pContent;
CComPtr<IPortableDeviceValues>        pObjectPropertiesToWrite;
CComPtr<IPortableDeviceValues>        pPropertyWriteResults;
CComPtr<IPortableDeviceValues>        pAttributes;
BOOL                                  bCanWrite            = FALSE;

// Prompt user to enter an object identifier on the device to write properties on.
printf("Enter the identifer of the object you wish to write properties on.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting property reading\n");
}
```



Al termine di questa operazione, l'applicazione recupera l' \_ attributo della proprietà WPD \_ \_ in grado di scrivere un \_ valore per la \_ \_ proprietà nome oggetto WPD per determinare se la proprietà può essere scritta. Si noti che l'applicazione potrebbe impostare qualsiasi proprietà per la quale WPD \_ L' \_ attributo Property \_ può \_ scrivere un valore true.


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent interface
// to access the property-specific methods.
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 3) Check the property attributes to see if we can write/change the WPD_OBJECT_NAME property.
if (SUCCEEDED(hr))
{
    hr = pProperties->GetPropertyAttributes(szSelection,
                                            WPD_OBJECT_NAME,
                                            &pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetBoolValue(WPD_PROPERTY_ATTRIBUTE_CAN_WRITE, &bCanWrite);
        if (SUCCEEDED(hr))
        {
            if (bCanWrite)
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports TRUE\nThis means that the property can be changed/updated\n\n");
            }
            else
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports FALSE\nThis means that the property cannot be changed/updated\n\n");
            }
        }
        else
        {
            printf("! Failed to get the WPD_PROPERTY_ATTRIBUTE_CAN_WRITE value from WPD_OBJECT_NAME on object '%ws', hr = 0x%lx\n",szSelection, hr);
        }
    }
}
```



Il passaggio successivo consiste nel richiedere all'utente la nuova stringa del nome. Si noti che la chiamata al metodo [**IPortableDeviceValues:: SetStringValue**](iportabledevicevalues-setstringvalue.md) crea semplicemente il contenitore delle proprietà. la proprietà effettiva non è stata ancora scritta.


```C++
if (bCanWrite)
{
    printf("Enter the new WPD_OBJECT_NAME for the object '%ws'.\n>",szSelection);
    hr = StringCbGetsW(szNewObjectName,sizeof(szNewObjectName));
    if (FAILED(hr))
    {
        printf("An invalid object name was specified, aborting property writing\n");
    }

    // 5) CoCreate an IPortableDeviceValues interface to hold the property values
    // we wish to write.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pObjectPropertiesToWrite));
        if (SUCCEEDED(hr))
        {
            if (pObjectPropertiesToWrite != NULL)
            {
                hr = pObjectPropertiesToWrite->SetStringValue(WPD_OBJECT_NAME, szNewObjectName);
                if (FAILED(hr))
                {
                    printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceValues, hr= 0x%lx\n", hr);
                }
            }
        }
    }
```



Infine, il nuovo valore, specificato dall'utente, viene applicato all'oggetto.


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->SetValues(szSelection,                // The object whose properties we are reading
                                pObjectPropertiesToWrite,   // The properties we want to read
                                &pPropertyWriteResults);    // Driver supplied property result values for the property read operation
    if (FAILED(hr))
    {
        printf("! Failed to set properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
    else
    {
        printf("The WPD_OBJECT_NAME property on object '%ws' was written successfully (Read the properties again to see the updated value)\n", szSelection);
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

 

 



