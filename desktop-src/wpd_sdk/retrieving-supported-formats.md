---
description: Recupero dei formati di servizio supportati
ms.assetid: b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec
title: Recupero dei formati di servizio supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed8021d8feefaaad3da7905e17e8c658dfb19e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317222"
---
# <a name="retrieving-supported-service-formats"></a>Recupero dei formati di servizio supportati

L'applicazione WpdServicesApiSample include codice che illustra come un'applicazione può recuperare i formati supportati da un determinato servizio Contatti chiamando i metodi delle interfacce nella tabella seguente.



|                                                                                      |                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Interfaccia                                                                            | Descrizione                                                                                           |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Utilizzato per recuperare l'interfaccia **IPortableDeviceServiceCapabilities** per accedere agli eventi supportati. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Fornisce l'accesso agli eventi e agli attributi di evento supportati.                                         |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Contiene l'elenco dei formati supportati.                                                               |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Contiene gli attributi per un formato specificato.                                                           |



 

Quando l'utente sceglie l'opzione "3" dalla riga di comando, l'applicazione richiama il metodo **ListSupportedFormats** trovato nel modulo ServiceCapabilities. cpp.

Si noti che prima di recuperare l'elenco di eventi, l'applicazione di esempio apre un servizio contatti in un dispositivo connesso.

In WPD un formato è descritto dagli attributi che specificano il nome e, facoltativamente, il tipo MIME di un determinato formato. Questi attributi sono definiti nel file di intestazione thePortableDevice. h. Per una descrizione degli attributi supportati, vedere l'argomento [attributi](attributes.md) .

Nel caso dell'applicazione di esempio, se WpdServiceSampleDriver è l'unico dispositivo installato, il driver restituisce due formati supportati per il servizio di contatto: "AbstractContactFormat" e "VCard2Format". Questi formati corrispondono al **\_ \_ \_ \_ contatto astratto del formato oggetto WPD** e al **\_ formato oggetto \_ WPD \_ VCARD2** attributi disponibili in portabledevice. h.

Due metodi del modulo ServiceCapabilities. cpp supportano il recupero dei formati supportati per il servizio Contacts: **ListSupportedFormats** e **DisplayFormat**. Il primo recupera l'identificatore GUID per ogni formato supportato. Il secondo converte questo GUID in una stringa intuitiva.

Il metodo **ListSupportedFormats** richiama il metodo [**IPortableDeviceService:: capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) per recuperare un'interfaccia [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . Utilizzando questa interfaccia, vengono recuperati i formati supportati chiamando il metodo [**IPortableDeviceServiceCapabilities:: GetSupportedFormats**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) . Il metodo **GetSupportedFormats** Recupera il GUID per ogni formato supportato dal servizio e copia il GUID in un oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .

Il codice seguente usa il metodo **ListSupportedFormats** .


```C++
// List all supported formats on the service
void ListSupportedFormats(
    IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumFormats    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pFormats;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all formats supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedFormats(&pFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get supported formats from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported formats found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pFormats->GetCount(&dwNumFormats);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported formats, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Formats Found on the service\n\n", dwNumFormats);

    // Loop through each format and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumFormats; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pFormats->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a format.  It is assumed that
                // formats are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayFormat(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }
}
```



Dopo che il metodo **ListSupportedFormats** Recupera il GUID per ogni formato supportato dal servizio specificato, richiama il metodo **DisplayFormat** per visualizzare il nome descrittivo dello script per ogni formato. ad esempio, "VCard2".

Il metodo **DisplayFormat** richiama il metodo [**IPortableDeviceServiceCapabilities:: GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) per recuperare una raccolta di attributi per il GUID di formato specificato. Chiama quindi il metodo [**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) e richiede che il driver restituisca un nome descrittivo per il formato specificato.

Il codice seguente usa il metodo **DisplayFormat** .


```C++
// Display basic information about a format
void DisplayFormat(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Format)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    HRESULT hr = pCapabilities->GetFormatAttributes(Format, &pAttributes);

    if (SUCCEEDED(hr))
    {
        PWSTR pszFormatName = NULL;
        hr = pAttributes->GetStringValue(WPD_FORMAT_ATTRIBUTE_NAME, &pszFormatName);

        // Display the name of the format if it is available, otherwise fall back to displaying the GUID.
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszFormatName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Format));
        }       

        CoTaskMemFree(pszFormatName);
        pszFormatName = NULL;
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



