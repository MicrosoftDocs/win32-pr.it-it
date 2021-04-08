---
title: Recupero delle proprietà dell'oggetto WPD
description: Recupero delle proprietà dell'oggetto
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3c6eba4435b23ef5c637feaca7c2d4ab6b160e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057984"
---
# <a name="retrieving-wpd-object-properties"></a>Recupero delle proprietà dell'oggetto WPD

I servizi spesso contengono oggetti figlio che appartengono a uno dei formati supportati da ogni servizio. Un servizio contatti, ad esempio, può supportare più oggetti contatto del formato di contatto astratto. Ogni oggetto contatto è descritto da proprietà correlate (nome contatto, numero di telefono, indirizzo di posta elettronica e così via).

L'applicazione WpdServiceApiSample include codice che illustra come un'applicazione può recuperare le proprietà Content-Object supportate da un determinato servizio contatti. In questo esempio vengono utilizzate le interfacce seguenti.



|                                                                      |                                                                                              |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Interfaccia                                                            | Descrizione                                                                                  |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | Recupera l'interfaccia **IPortableDeviceContent2** per accedere ai metodi del servizio supportati. |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | Fornisce l'accesso ai metodi specifici del contenuto.                                             |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | Recupera i valori della proprietà dell'oggetto.                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)               | Include i valori della proprietà letti per l'oggetto.                                    |
| [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) | Contiene i parametri per un determinato metodo.                                                  |



 

Quando l'utente sceglie l'opzione "7" nella riga di comando, l'applicazione richiama il metodo **ReadContentProperties** trovato nel modulo ContentProperties. cpp.

Questo metodo recupera le quattro proprietà seguenti per l'oggetto contatto specificato.



|                              |                                                                                                                                                                                                                  |                                 |                                     |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| Proprietà                     | Descrizione                                                                                                                                                                                                      | Servizi per dispositivi PROPERTYKEY     | PropertyKey WPD equivalente \_         |
| Identificatore oggetto padre     | Stringa che specifica l'identificatore per l'elemento padre dell'oggetto specificato.                                                                                                                                            | PKEY \_ GenericObj \_ parentID      | \_ \_ ID padre dell'oggetto WPD \_             |
| Nome dell'oggetto                  | Stringa che specifica il nome dell'oggetto specificato.                                                                                                                                                             | \_Nome GENERICOBJ \_ pkey          | \_nome dell'oggetto WPD \_                   |
| Identificatore univoco permanente | Stringa che specifica un identificatore univoco per l'oggetto specificato. Questo identificatore è persistente tra le sessioni, a differenza dell'identificatore dell'oggetto. Per i servizi, deve essere una rappresentazione in forma di stringa di un GUID. | PKEY \_ GenericObj \_ PersistentUID | \_ \_ \_ ID univoco permanente dell'oggetto WPD \_ |
| Formato oggetto                | Identificatore univoco globale (GUID) che specifica il formato del file corrispondente a un oggetto specificato.                                                                                                        | PKEY \_ GenericObj \_ ObjectFormat  | \_formato oggetto \_ WPD                 |



 

-   ID padre
-   Nome
-   PersistentUID
-   Formato

Si noti che prima di recuperare le proprietà del contenuto, l'applicazione di esempio apre un servizio contatti in un dispositivo connesso.

Il codice seguente per il metodo **ReadContentProperties** illustra in che modo l'applicazione usa l'interfaccia [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) per recuperare un'interfaccia [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) . Passando il PROPERTYKEYS delle proprietà richieste al metodo [**IPortableDeviceProperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) , **ReadContentProperties** recupera i valori richiesti e li Visualizza nella finestra della console.


```C++
// Reads properties for the user specified object.
void ReadContentProperties(
    IPortableDeviceService*    pService)
{
    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    HRESULT                               hr              = S_OK;
    WCHAR                                 szSelection[81] = {0};
    CComPtr<IPortableDeviceProperties>    pProperties;
    CComPtr<IPortableDeviceValues>        pObjectProperties;
    CComPtr<IPortableDeviceContent2>      pContent;
    CComPtr<IPortableDeviceKeyCollection> pPropertiesToRead;

    // Prompt user to enter an object identifier on the device to read properties from.
    printf("Enter the identifer of the object you wish to read properties from.\n>");
    hr = StringCbGetsW(szSelection,sizeof(szSelection));
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

    // 3) CoCreate an IPortableDeviceKeyCollection interface to hold the property keys
    // we wish to read.
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
            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ParentID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ParentID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_Name);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_PersistentUID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_PersistentUID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ObjectFormat);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ObjectFormat to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

        }
    }

    // 5) Call GetValues() passing the collection of specified PROPERTYKEYs.
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

    // 6) Display the returned property values to the user
    if (SUCCEEDED(hr))
    {
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_ParentID,        NAME_GenericObj_ParentID);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_Name,            NAME_GenericObj_Name);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_PersistentUID,   NAME_GenericObj_PersistentUID);
        DisplayGuidProperty  (pObjectProperties, PKEY_GenericObj_ObjectFormat,    NAME_GenericObj_ObjectFormat);
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

 

 



