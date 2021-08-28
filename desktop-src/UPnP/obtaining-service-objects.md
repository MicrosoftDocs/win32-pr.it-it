---
title: Recupero di oggetti servizio
description: Gli oggetti dispositivo espongono una proprietà denominata Services che restituisce una raccolta di oggetti Service che contiene un oggetto servizio per ogni servizio esportato dal dispositivo.
ms.assetid: 8ef12b6e-cb9b-4406-95be-002117b8fc3f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b7fca24bfc79a9458cfb964af28edba813a90ef17924a68fd0d1689e047884c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999571"
---
# <a name="obtaining-service-objects"></a>Recupero di oggetti servizio

Gli oggetti dispositivo espongono una proprietà denominata [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) che restituisce una raccolta di oggetti Service che contiene un oggetto servizio per ogni servizio esportato dal dispositivo. Le applicazioni possono attraversare questa raccolta in sequenza o richiedere un particolare servizio usando il relativo ID servizio.

## <a name="vbscript-example"></a>Esempio di VBScript

L'esempio seguente è il codice VBScript che estrae gli oggetti Service per due dei servizi esportati da un dispositivo.


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



La prima riga estrae la raccolta di servizi dall'oggetto Device tramite query sulla [**proprietà Services.**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) Le due righe seguenti ottengono i due oggetti Service desiderati dalla raccolta specificando i relativi ID servizio. La raccolta di servizi può anche essere attraversata in sequenza usando **un oggetto per ogni ... ciclo** next.

## <a name="c-example"></a>Esempio C++

L'esempio seguente illustra il codice C++ necessario per ottenere gli oggetti Service da un dispositivo. In primo luogo, il codice di esempio esegue una query sulla proprietà [**IUPnPDevice::Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) sull'interfaccia passata alla funzione. Viene restituita una raccolta di servizi tramite [**l'interfaccia IUPnPServices.**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) Per ottenere singoli oggetti Service, usare il [**metodo Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) e specificare gli ID servizio richiesti. Per attraversare la raccolta in sequenza, usare i metodi [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)e [**IEnumVARIANT::Skip.**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) Questo esempio è simile all'esempio usato per attraversare la [**raccolta IUPnPDevices.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")


HRESULT ExtractServices(IUPnPDevice * pDevice)
{
    // Create a BSTR to hold the service name
    BSTR bstrServiceName = SysAllocString(L"urn:upnp-org:servicId:DVDVideo");
    if (NULL == bstrServiceName)
    {
        return E_OUTOFMEMORY;
    }
    // Get the list of services available on the device
    IUPnPServices * pServices = NULL;
    HRESULT hr = pDevice->get_Services(&pServices);
    if (SUCCEEDED(hr))
    {
        // Retrieve the service we are interested in
        IUPnPService * pAppService = NULL;
        hr = pServices->get_Item(bstrServiceName, &pAppService);
        if (SUCCEEDED(hr))
        {
            // Do something interesting with the service object
            pAppService->Release();
        }
        pServices->Release();
    }
    SysFreeString(bstrServiceName);
    return hr;
}
```



 

 