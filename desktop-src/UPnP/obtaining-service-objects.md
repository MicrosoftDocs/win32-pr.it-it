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
# <a name="obtaining-service-objects"></a><span data-ttu-id="0c46c-103">Recupero di oggetti servizio</span><span class="sxs-lookup"><span data-stu-id="0c46c-103">Obtaining Service Objects</span></span>

<span data-ttu-id="0c46c-104">Gli oggetti dispositivo espongono una proprietà denominata [**Servizi**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) che restituisce una raccolta di oggetti servizio che contiene un oggetto servizio per ogni servizio esportato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c46c-104">Device objects expose a property called [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) that returns a collection of Service objects that contains one service object for each service exported by the device.</span></span> <span data-ttu-id="0c46c-105">Le applicazioni possono attraversare questa raccolta in sequenza o richiedere un particolare servizio usando il relativo ID servizio.</span><span class="sxs-lookup"><span data-stu-id="0c46c-105">Applications are able to traverse this collection sequentially, or request a particular service by using its service ID.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="0c46c-106">Esempio di VBScript</span><span class="sxs-lookup"><span data-stu-id="0c46c-106">VBScript Example</span></span>

<span data-ttu-id="0c46c-107">L'esempio seguente è codice VBScript che estrae oggetti servizio per due dei servizi esportati da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c46c-107">The following example is VBScript code that extracts Service objects for two of the services exported by a device.</span></span>


```VB
' Get the service objects
services = device.Services
    
Set appService = services( "urn:upnp-org:serviceId:DVDVideo" )
Set xportService = services( "urn:upnp-org:serviceId:AVTransport" )
```



<span data-ttu-id="0c46c-108">La prima riga estrae la raccolta di servizi dall'oggetto dispositivo eseguendo una query sulla proprietà [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) .</span><span class="sxs-lookup"><span data-stu-id="0c46c-108">The first line extracts the services collection from the Device object by querying the [**Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) property.</span></span> <span data-ttu-id="0c46c-109">Le due righe successive ottengono i due oggetti servizio desiderati dalla raccolta specificando gli ID del servizio.</span><span class="sxs-lookup"><span data-stu-id="0c46c-109">The next two lines obtain the two desired Service objects from the collection by specifying their service IDs.</span></span> <span data-ttu-id="0c46c-110">La raccolta di servizi può anche essere attraversata in sequenza tramite un **per ogni... ciclo successivo** .</span><span class="sxs-lookup"><span data-stu-id="0c46c-110">The services collection can also be traversed sequentially by using a **for each … next** loop.</span></span>

## <a name="c-example"></a><span data-ttu-id="0c46c-111">Esempio C++</span><span class="sxs-lookup"><span data-stu-id="0c46c-111">C++ Example</span></span>

<span data-ttu-id="0c46c-112">Nell'esempio seguente viene illustrato il codice C++ necessario per ottenere oggetti servizio da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c46c-112">The following example shows the C++ code required to obtain Service objects from a device.</span></span> <span data-ttu-id="0c46c-113">In primo luogo, il codice di esempio esegue una query sulla proprietà [**IUPnPDevice:: Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) sull'interfaccia passata alla funzione.</span><span class="sxs-lookup"><span data-stu-id="0c46c-113">First, the sample code queries the [**IUPnPDevice::Services**](/windows/win32/api/upnp/nf-upnp-iupnpdevice-get_services) property on the interface that was passed to the function.</span></span> <span data-ttu-id="0c46c-114">Viene restituita una raccolta di servizi tramite l'interfaccia [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) .</span><span class="sxs-lookup"><span data-stu-id="0c46c-114">This returns a service collection using the [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) interface.</span></span> <span data-ttu-id="0c46c-115">Per ottenere singoli oggetti servizio, usare il metodo [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) e specificare gli ID servizio richiesti.</span><span class="sxs-lookup"><span data-stu-id="0c46c-115">To obtain individual Service objects, use the [**Item**](/windows/win32/api/upnp/nf-upnp-iupnpservices-get_item) method, and specify the requested service IDs.</span></span> <span data-ttu-id="0c46c-116">Per attraversare la raccolta in modo sequenziale, usare i metodi [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next)e [**IEnumVARIANT:: Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) .</span><span class="sxs-lookup"><span data-stu-id="0c46c-116">To traverse the collection sequentially, use the [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset), [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next), and [**IEnumVARIANT::Skip**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-skip) methods.</span></span> <span data-ttu-id="0c46c-117">Questo esempio è simile all'esempio usato per attraversare la raccolta [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .</span><span class="sxs-lookup"><span data-stu-id="0c46c-117">This example is similar to the example used to traverse the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) collection.</span></span>


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



 

 