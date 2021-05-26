---
description: Scrittura delle proprietà dell'oggetto
ms.assetid: f762a571-83ea-4999-ad49-a51044bc790d
title: Scrittura delle proprietà dell'oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 726501c986e73033437de3bee0c11b3beb66150d
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423931"
---
# <a name="writing-object-properties"></a>Scrittura delle proprietà dell'oggetto

I servizi contengono spesso oggetti figlio appartenenti a uno dei formati supportati da ogni servizio. Ad esempio, un servizio Contatti può supportare più oggetti contatto nel formato Contatto astratto. Ogni oggetto contatto è descritto dalle proprietà correlate (nome del contatto, numero di telefono, indirizzo di posta elettronica e così via).

L'applicazione WpdServicesApiSample include codice che illustra come un'applicazione può aggiornare la proprietà name per un oggetto figlio del servizio Contatti specificato. Questo esempio usa le interfacce WPD seguenti.



| Interfaccia                                                      | Descrizione                                                                                                                                                          |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)       | Usato per recuperare **l'interfaccia IPortableDeviceContent2** per accedere ai metodi di servizio supportati.                                                                  |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)     | Fornisce l'accesso ai metodi specifici del contenuto.                                                                                                                     |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | Usato per scrivere i valori delle proprietà dell'oggetto e per determinare se una determinata proprietà può essere scritta                                                                    |
| [**IPortableDeviceValues**](iportabledevicevalues.md)         | Usato per contenere i valori delle proprietà da scrivere, determinare i risultati dell'operazione di scrittura e recuperare gli attributi delle proprietà (quando si determina la funzionalità di scrittura). |



 

Quando l'utente sceglie l'opzione "8" dalla riga di comando, l'applicazione richiama il metodo **WriteContentProperties** disponibile nel modulo ContentProperties.cpp. Questo metodo richiede all'utente di immettere un identificatore di oggetto per la proprietà da aggiornare. L'utente identifica l'oggetto e il metodo richiede all'utente di specificare un nuovo nome. Dopo aver specificato questo nome, il metodo aggiorna la proprietà Name per l'oggetto specificato.

Si noti che prima di scrivere le proprietà dell'oggetto, l'applicazione di esempio apre un servizio Contatti in un dispositivo connesso.

Il codice seguente per il **metodo WriteContentProperties** illustra come l'applicazione usa l'interfaccia [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) per recuperare [**un'interfaccia IPortableDeviceProperties.**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) Passando propertyKEYS delle proprietà richieste al metodo [**IPortableDeviceProperties::SetValues,**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) **WriteContentProperties** aggiorna la proprietà name.


```C++
void WriteContentProperties(
 IPortableDeviceService* pService)
{
 if (pService == NULL)
 {
  printf("! A NULL IPortableDeviceService interface pointer was received\n");
  return;
 }

 HRESULT          hr       = S_OK;
 WCHAR         wszSelection[81]  = {0};
 WCHAR         wszNewObjectName[81] = {0};
 CComPtr<IPortableDeviceProperties> pProperties;
 CComPtr<IPortableDeviceContent2>   pContent;
 CComPtr<IPortableDeviceValues>  pObjectPropertiesToWrite;
 CComPtr<IPortableDeviceValues>  pPropertyWriteResults;
 CComPtr<IPortableDeviceValues>  pAttributes;
 BOOL          bCanWrite   = FALSE;

 // Prompt user to enter an object identifier on the device to write properties on.
 printf("Enter the identifer of the object you wish to write properties on.\n>");
 hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
 if (FAILED(hr))
 {
  printf("An invalid object identifier was specified, aborting property reading\n");
 }

 // 1) Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
 // access the content-specific methods.
 if (SUCCEEDED(hr))
 {
  hr = pService->Content(&pContent);
  if (FAILED(hr))
  {
   printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
  }
 }

 // 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent2 interface
 // to access the property-specific methods.
 if (SUCCEEDED(hr))
 {
  hr = pContent->Properties(&pProperties);
  if (FAILED(hr))
  {
   printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent2, hr = 0x%lx\n",hr);
  }
 }

 // 3) Check the property attributes to see if we can write/change the NAME_GenericObj_Name property.
 if (SUCCEEDED(hr))
 {
  hr = pProperties->GetPropertyAttributes(wszSelection,
            PKEY_GenericObj_Name,
            &pAttributes);
  if (SUCCEEDED(hr))
  {
   hr = pAttributes->GetBoolValue(WPD_PROPERTY_ATTRIBUTE_CAN_WRITE, &bCanWrite);
   if (SUCCEEDED(hr))
   {
    if (bCanWrite)
    {
     printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for PKEY_GenericObj_Name reports TRUE\nThis means that the property can be changed/updated\n\n");
    }
    else
    {
     printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for PKEY_GenericObj_Name reports FALSE\nThis means that the property cannot be changed/updated\n\n");
    }
   }
   else
   {
    printf("! Failed to get the WPD_PROPERTY_ATTRIBUTE_CAN_WRITE value for PKEY_GenericObj_Name on object '%ws', hr = 0x%lx\n", wszSelection, hr);
   }
  }
 }

 // 4) Prompt the user for the new value of the NAME_GenericObj_Name property only if the property attributes report
 // that it can be changed/updated.
 if (bCanWrite)
 {
  printf("Enter the new PKEY_GenericObj_Name property for the object '%ws'.\n>",wszSelection);
  hr = StringCbGetsW(wszNewObjectName,sizeof(wszNewObjectName));
  if (FAILED(hr))
  {
   printf("An invalid PKEY_GenericObj_Name was specified, aborting property writing\n");
  }

  // 5) CoCreate an IPortableDeviceValues interface to hold the property values
  // we wish to write.
  if (SUCCEEDED(hr))
  {
   hr = CoCreateInstance(CLSID_PortableDeviceValues,
          NULL,
          CLSCTX_INPROC_SERVER,
          IID_IPortableDeviceValues,
          (VOID**) &pObjectPropertiesToWrite);
   if (SUCCEEDED(hr))
   {
    if (pObjectPropertiesToWrite != NULL)
    {
     hr = pObjectPropertiesToWrite->SetStringValue(PKEY_GenericObj_Name, wszNewObjectName);
     if (FAILED(hr))
     {
      printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceValues, hr= 0x%lx\n", hr);
     }
    }
   }
  }

  // 6) Call SetValues() passing the collection of specified PROPERTYKEYs.
  if (SUCCEEDED(hr))
  {
   hr = pProperties->SetValues(wszSelection,      // The object whose properties we are reading
          pObjectPropertiesToWrite,   // The properties we want to read
          &pPropertyWriteResults); // Driver supplied property result values for the property read operation
   if (FAILED(hr))
   {
    printf("! Failed to set properties for object '%ws', hr= 0x%lx\n", wszSelection, hr);
   }
   else
   {
    printf("The PKEY_GenericObj_Name property on object '%ws' was written successfully (Read the properties again to see the updated value)\n", wszSelection);
   }
  }
 }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



