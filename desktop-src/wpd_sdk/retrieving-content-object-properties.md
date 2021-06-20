---
title: Recupero delle proprietà degli oggetti WPD
description: L'applicazione WpdServiceApiSample illustra come un'applicazione può recuperare le proprietà dell'oggetto contenuto supportate da un determinato servizio Contatti.
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e57258993d0a81f68042195db2caf338c97c53
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404314"
---
# <a name="retrieving-wpd-object-properties"></a>Recupero delle proprietà degli oggetti WPD

I servizi contengono spesso oggetti figlio appartenenti a uno dei formati supportati da ogni servizio. Ad esempio, un servizio Contatti può supportare più oggetti contatto nel formato Contatto astratto. Ogni oggetto contatto è descritto dalle proprietà correlate (nome del contatto, numero di telefono, indirizzo di posta elettronica e così via).

L'applicazione WpdServiceApiSample include codice che illustra come un'applicazione può recuperare le proprietà dell'oggetto contenuto supportate da un determinato servizio Contatti. In questo esempio vengono utilizzate le interfacce seguenti.



| Interfaccia | Descrizione    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | Recupera **l'interfaccia IPortableDeviceContent2** per accedere ai metodi del servizio supportati. |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | Fornisce l'accesso ai metodi specifici del contenuto.                                             |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | Recupera i valori delle proprietà dell'oggetto.                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)               | Contiene i valori delle proprietà letti per l'oggetto.                                    |
| [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) | Contiene i parametri per un determinato metodo.                                                  |



 

Quando l'utente sceglie l'opzione "7" nella riga di comando, l'applicazione richiama il metodo **ReadContentProperties** disponibile nel modulo ContentProperties.cpp.

Questo metodo recupera le quattro proprietà seguenti per l'oggetto contatto specificato.



| Proprietà                     | Descrizione                                                                                                                                                                                                      | PROPERTYKEY di Servizi dispositivi     | PROPERTYKEY WPD \_ equivalente         |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| Identificatore dell'oggetto padre     | Stringa che specifica l'identificatore per l'elemento padre dell'oggetto specificato.                                                                                                                                            | PKEY \_ GenericObj \_ ParentID      | ID PADRE \_ DELL'OGGETTO WPD \_ \_             |
| Nome dell'oggetto                  | Stringa che specifica il nome dell'oggetto specificato.                                                                                                                                                             | PKEY \_ GenericObj \_ Name          | NOME OGGETTO \_ WPD \_                   |
| Identificatore univoco permanente | Stringa che specifica un identificatore univoco per l'oggetto specificato. Questo identificatore è persistente tra le sessioni, a differenza dell'identificatore di oggetto. Per i servizi, deve essere una rappresentazione di stringa di un GUID. | PKEY \_ GenericObj \_ PersistentUID | \_ID UNIVOCO \_ PERSISTENTE \_ DELL'OGGETTO \_ WPD |
| Formato oggetto                | Identificatore univoco globale (GUID) che specifica il formato del file corrispondente a un determinato oggetto                                                                                                        | PKEY \_ GenericObj \_ ObjectFormat  | FORMATO OGGETTO \_ WPD \_                 |



 

-   ID padre
-   Nome
-   PersistentUID
-   Formato

Si noti che prima di recuperare le proprietà del contenuto, l'applicazione di esempio apre un servizio Contatti in un dispositivo connesso.

Il codice seguente per il **metodo ReadContentProperties** illustra come l'applicazione usa l'interfaccia [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) per recuperare [**un'interfaccia IPortableDeviceProperties.**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) Passando le proprietà PROPERTYKEYS delle proprietà richieste al metodo [**IPortableDeviceProperties::GetValues,**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) **ReadContentProperties** recupera i valori richiesti e li visualizza nella finestra della console.


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

 

 



