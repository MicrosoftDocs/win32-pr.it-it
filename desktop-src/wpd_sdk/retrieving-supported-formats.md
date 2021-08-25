---
description: Recupero dei formati di servizio supportati
ms.assetid: b54dfeda-c2a3-42ec-895f-9abbbd4dd2ec
title: Recupero dei formati di servizio supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccbaa5678d12e4393f377bb0ae0a399634b247ceb9bd54e1d815d4e9f7e5a763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806671"
---
# <a name="retrieving-supported-service-formats"></a>Recupero dei formati di servizio supportati

L'applicazione WpdServicesApiSample include codice che illustra come un'applicazione può recuperare i formati supportati da un determinato servizio Contatti chiamando i metodi delle interfacce nella tabella seguente.



| Interfaccia | Descrizione   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Usato per recuperare **l'interfaccia IPortableDeviceServiceCapabilities** per accedere agli eventi supportati. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Fornisce l'accesso agli eventi supportati e agli attributi degli eventi.                                         |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Contiene l'elenco dei formati supportati.                                                               |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Contiene gli attributi per un formato specificato.                                                           |



 

Quando l'utente sceglie l'opzione "3" dalla riga di comando, l'applicazione richiama il metodo **ListSupportedFormats** disponibile nel modulo ServiceCapabilities.cpp.

Si noti che prima di recuperare l'elenco di eventi, l'applicazione di esempio apre un servizio Contatti in un dispositivo connesso.

In WPD, un formato è descritto dagli attributi che specificano il nome e (facoltativamente) il tipo MIME di un determinato formato. Questi attributi sono definiti nel file di intestazionePortableDevice.h. Per una descrizione degli attributi supportati, vedere [l'argomento](attributes.md) Attributi.

Nel caso dell'applicazione di esempio, se WpdServiceSampleDriver è l'unico dispositivo installato, il driver restituisce due formati supportati per il servizio Contact: "AbstractContactFormat" e "VCard2Format". Questi formati corrispondono agli attributi **WPD \_ OBJECT FORMAT ABSTRACT \_ \_ \_ CONTACT** e **WPD \_ OBJECT FORMAT \_ \_ VCARD2** disponibili in PortableDevice.h.

Due metodi nel modulo ServiceCapabilities.cpp supportano il recupero dei formati supportati per il servizio Contatti: **ListSupportedFormats** e **DisplayFormat**. Il primo recupera l'identificatore GUID per ogni formato supportato. Quest'ultimo converte questo GUID in una stringa descrittiva.

Il **metodo ListSupportedFormats** richiama il [**metodo IPortableDeviceService::Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) per recuperare [**un'interfaccia IPortableDeviceServiceCapabilities.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Usando questa interfaccia, recupera i formati supportati chiamando il metodo [**IPortableDeviceServiceCapabilities::GetSupportedFormats.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedformats) Il **metodo GetSupportedFormats** recupera il GUID per ogni formato supportato dal servizio e lo copia in un [**oggetto IPortableDevicePropVariantCollection.**](iportabledevicepropvariantcollection.md)

Il codice seguente usa il **metodo ListSupportedFormats.**


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



Dopo che **il metodo ListSupportedFormats** ha recuperato il GUID per ogni formato supportato dal servizio specificato, richiama il **metodo DisplayFormat** per visualizzare il nome descrittivo dello script per ogni formato. ad esempio "VCard2".

Il **metodo DisplayFormat** richiama il metodo [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) per recuperare una raccolta di attributi per il GUID di formato specificato. Chiama quindi il metodo [**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md) e richiede che il driver restituirà un nome descrittivo per lo script per il formato specificato.

Il codice seguente usa il **metodo DisplayFormat.**


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

 

 



