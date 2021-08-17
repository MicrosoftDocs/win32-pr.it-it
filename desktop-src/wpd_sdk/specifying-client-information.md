---
description: Specifica delle informazioni client
ms.assetid: 275fda71-61ef-4b50-96fe-bdc0c0266646
title: Specifica delle informazioni client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b437c4d0c0ce9d04f55bb00a1fd4b666d30cf29228050151072e43f87edb11a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119445501"
---
# <a name="specifying-client-information"></a>Specifica delle informazioni client

Le informazioni client fornite nel secondo argomento vengono usate da alcuni driver di dispositivo per ottimizzare le prestazioni del dispositivo. Come minimo, l'applicazione deve fornire una stringa contenente il nome, un numero di versione principale, un numero di versione secondaria e un numero di revisione. Questi sono i campi forniti dall'applicazione di esempio.


```C++
#define CLIENT_NAME         L"WPD Sample Application"
#define CLIENT_MAJOR_VER    1
#define CLIENT_MINOR_VER    0
#define CLIENT_REVISION     2
```



La `GetClientInformation` funzione nell'applicazione di esempio crea e popola **un'interfaccia IPortableDeviceValues** con le informazioni del client. Questa funzione ha due parti principali. La prima parte crea un'istanza di un oggetto device-values portabile chiamando la funzione CoCreateInstance.


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(ppClientInformation));
```



La seconda parte imposta le informazioni sul client nell'oggetto device-values portabile.


```C++
if (SUCCEEDED(hr))
{
    // Attempt to set all bits of client information
    hr = (*ppClientInformation)->SetStringValue(WPD_CLIENT_NAME, CLIENT_NAME);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_NAME, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_MAJOR_VERSION, CLIENT_MAJOR_VER);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_MAJOR_VERSION, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_MINOR_VERSION, CLIENT_MINOR_VER);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_MINOR_VERSION, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_REVISION, CLIENT_REVISION);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_REVISION, hr = 0x%lx\n",hr);
    }

    //  Some device drivers need to impersonate the caller in order to function correctly.  Since our application does not
    //  need to restrict its identity, specify SECURITY_IMPERSONATION so that we work with all devices.
    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_SECURITY_QUALITY_OF_SERVICE, SECURITY_IMPERSONATION);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_SECURITY_QUALITY_OF_SERVICE, hr = 0x%lx\n",hr);
    }
}
else
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceValues, hr = 0x%lx\n",hr);
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 



