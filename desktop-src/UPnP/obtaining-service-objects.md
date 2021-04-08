---
title: Recupero di oggetti servizio
description: Gli oggetti dispositivo espongono una proprietà denominata servizi che restituisce una raccolta di oggetti servizio che contiene un oggetto servizio per ogni servizio esportato dal dispositivo.
ms.assetid: 8ef12b6e-cb9b-4406-95be-002117b8fc3f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf951c9c620c23c2d4919dc4a8bcf082159fa7a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872797"
---
# <a name="obtaining-service-objects"></a>Recupero di oggetti servizio

Gli oggetti dispositivo espongono una proprietà denominata [**Servizi**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) che restituisce una raccolta di oggetti servizio che contiene un oggetto servizio per ogni servizio esportato dal dispositivo. Le applicazioni possono attraversare questa raccolta in sequenza o richiedere un particolare servizio usando il relativo ID servizio.

## <a name="vbscript-example"></a>Esempio di VBScript

L'esempio seguente è codice VBScript che estrae oggetti servizio per due dei servizi esportati da un dispositivo.


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



La prima riga estrae la raccolta di servizi dall'oggetto dispositivo eseguendo una query sulla proprietà [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) . Le due righe successive ottengono i due oggetti servizio desiderati dalla raccolta specificando gli ID del servizio. La raccolta di servizi può anche essere attraversata in sequenza tramite un **per ogni... ciclo successivo** .

## <a name="c-example"></a>Esempio C++

Nell'esempio seguente viene illustrato il codice C++ necessario per ottenere oggetti servizio da un dispositivo. In primo luogo, il codice di esempio esegue una query sulla proprietà [**IUPnPDevice:: Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) sull'interfaccia passata alla funzione. Viene restituita una raccolta di servizi tramite l'interfaccia [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) . Per ottenere singoli oggetti servizio, usare il metodo [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) e specificare gli ID servizio richiesti. Per attraversare la raccolta in modo sequenziale, usare i metodi [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)e [**IEnumVARIANT:: Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) . Questo esempio è simile all'esempio usato per attraversare la raccolta [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .


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



 

 