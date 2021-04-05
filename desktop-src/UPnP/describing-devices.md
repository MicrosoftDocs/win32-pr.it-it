---
title: Descrizione dei dispositivi
description: Esistono due modi per ottenere gli oggetti dispositivo.
ms.assetid: a83fbf21-586e-4b92-9875-476d820c377d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abc84f15f6b52328585e05abfd95503087124b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856645"
---
# <a name="describing-devices"></a><span data-ttu-id="7c0a8-103">Descrizione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="7c0a8-103">Describing Devices</span></span>

<span data-ttu-id="7c0a8-104">Esistono due modi per ottenere gli oggetti dispositivo:</span><span class="sxs-lookup"><span data-stu-id="7c0a8-104">There are two ways to obtain device objects:</span></span>

-   <span data-ttu-id="7c0a8-105">Utilizzando l'interfaccia [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) .</span><span class="sxs-lookup"><span data-stu-id="7c0a8-105">Using the [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) interface.</span></span> <span data-ttu-id="7c0a8-106">L'interfaccia **IUPnPDescriptionDocument** è l'unica interfaccia sicura per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-106">The **IUPnPDescriptionDocument** interface is the only interface that is safe for scripting.</span></span>
-   <span data-ttu-id="7c0a8-107">Utilizzo dell'interfaccia [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) per ottenere un'interfaccia [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .</span><span class="sxs-lookup"><span data-stu-id="7c0a8-107">Using the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface to obtain an [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface.</span></span>

<span data-ttu-id="7c0a8-108">Entrambi i metodi restituiscono raccolte di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-108">Both methods return Devices collections.</span></span> <span data-ttu-id="7c0a8-109">Le applicazioni usano quindi i metodi del dispositivo per recuperare le proprietà sui dispositivi.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-109">Applications then use the Device methods to retrieve properties about devices.</span></span>

<span data-ttu-id="7c0a8-110">Le applicazioni sono in grado di recuperare i tipi di informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7c0a8-110">Applications are able to retrieve the following types of information:</span></span>

-   <span data-ttu-id="7c0a8-111">Informazioni sulla gerarchia dei dispositivi, inclusi i dispositivi radice, i dispositivi padre e i dispositivi figlio.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-111">Device hierarchy information, including root devices, parent devices, and child devices.</span></span>
-   <span data-ttu-id="7c0a8-112">Proprietà del dispositivo, tra cui UDNs, URI (Uniform Resource Identifier) e nomi leggibili dall'utente.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-112">Device properties, including UDNs, uniform resource identifiers (URIs), and user-readable names.</span></span>
-   <span data-ttu-id="7c0a8-113">Informazioni sul produttore, inclusi i nomi e le pagine Web correlate.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-113">Manufacturer information, including names and related Web pages.</span></span>
-   <span data-ttu-id="7c0a8-114">Informazioni sul modello, inclusi il nome, il numero, l'UPC, i numeri di serie e le descrizioni dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-114">Model information, including the name, number, UPC, serial numbers and device descriptions.</span></span>
-   <span data-ttu-id="7c0a8-115">Visualizzare le informazioni, incluso l'URL per controllare il dispositivo e gli URL da cui vengono scaricate le icone.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-115">Display information, including the URL to control the device, and URLs from which icons are downloaded.</span></span>
-   <span data-ttu-id="7c0a8-116">Servizi forniti da un particolare dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-116">Services provided by a particular device.</span></span>

<span data-ttu-id="7c0a8-117">Le applicazioni ottengono anche l'URL del documento di descrizione del dispositivo usando l'interfaccia [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) .</span><span class="sxs-lookup"><span data-stu-id="7c0a8-117">Applications also obtain the URL of the device description document using the [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) interface.</span></span> <span data-ttu-id="7c0a8-118">L'applicazione carica quindi il documento di descrizione e utilizza le proprietà del dispositivo e del servizio che non sono esposte dall'interfaccia [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) .</span><span class="sxs-lookup"><span data-stu-id="7c0a8-118">The application then load the description document and work with device and service properties that are not exposed by the [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) interface.</span></span> <span data-ttu-id="7c0a8-119">Questa interfaccia non può essere utilizzata nello scripting, perché non è l'interfaccia predefinita.</span><span class="sxs-lookup"><span data-stu-id="7c0a8-119">This interface cannot be used in scripting, because it is not the default interface.</span></span>

## <a name="visual-basic-example"></a><span data-ttu-id="7c0a8-120">Esempio di Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7c0a8-120">Visual Basic Example</span></span>

<span data-ttu-id="7c0a8-121">Il codice di esempio seguente illustra l'uso di [**IUPnPDeviceDocumentAccess:: GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span><span class="sxs-lookup"><span data-stu-id="7c0a8-121">The following sample code shows the usage of [**IUPnPDeviceDocumentAccess::GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span></span>


```VB
Sub GetDocumentURL()
Dim pDescDoc As IUPnPDeviceDocumentAccess
Dim strDescDocURL As String

'currentDevice is UPnPDevice object containing the current UPnP Device 
'We are trying to get IUPnPDeviceDocumentAccess interface in the UPnP Device object
Set pDescDoc = currentDevice

If Not (pDescDoc is Nothing) Then
  'Description Document URL is got from device
  strDescDocURL = pDescDoc.GetDocumentURL 
End If
```



## <a name="c-example"></a><span data-ttu-id="7c0a8-122">Esempio C++</span><span class="sxs-lookup"><span data-stu-id="7c0a8-122">C++ Example</span></span>

<span data-ttu-id="7c0a8-123">Il codice di esempio seguente illustra l'uso di [**IUPnPDeviceDocumentAccess:: GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span><span class="sxs-lookup"><span data-stu-id="7c0a8-123">The following sample code shows the usage of [**IUPnPDeviceDocumentAccess::GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

int GetDeviceDocumentUrl () 
{
  HRESULT hr = S_OK;
  // List of interfaces needed
  IUPnPDeviceFinder *pDevFinder=NULL;
  IUPnPDevice *pDevice =NULL;
  IUPnPDeviceDocumentAccess* pDeviceDocument=NULL;
  BSTR bstrDeviceUDN =NULL;
  BSTR bstrDeviceDocumentURL = NULL; 

  bstrDeviceUDN = SysAllocString(L"uuid:234324234324");
  if(bstrDeviceUDN == NULL){
    printf("ERROR: Could not allocate memory\n");
    return -1;
  }  

  //CoInitialize the program so that we can create COM objects
  CoInitializeEx(NULL, COINIT_MULTITHREADED);

  //now try to instantiate the DeviceFinder object
  hr = CoCreateInstance(  CLSID_UPnPDeviceFinder, 
              NULL,
              CLSCTX_INPROC_SERVER,
              IID_IUPnPDeviceFinder,
              (LPVOID *) &pDevFinder); 

  if(!SUCCEEDED(hr)){
    printf("\nERROR: CoCreateInstance on IUPnPDeviceFinder returned HRESULT %x",hr);
    goto cleanup;
  }

  printf("\nGot a pointer to the IUPnPDeviceFinder Interface");

  printf("\n Finding the device of given UDN\n");
  hr =pDevFinder->FindByUDN(bstrDeviceUDN, &pDevice);
  if(hr!=S_OK)
  {
    printf("\nERROR: FindByUDN for %S returned HRESULT %x", bstrDeviceUDN, hr);
    goto cleanup;
  }

  printf("\n\tFindByUDN for device of UDN %S succeeded", bstrDeviceUDN);
  //Now query pDevice for IUPnPDeviceDocumentAccess
  hr = pDevice->QueryInterface(IID_IUPnPDeviceDocumentAccess, (VOID **)&pDeviceDocument);
  if(SUCCEEDED(hr)){
    // We have got a pointer to the IUPnPDeviceDocumentAccess interface.
    // GetDocumentURL is available only in Windows XP. 
    hr = pDeviceDocument->GetDocumentURL(&bstrDeviceDocumentURL);
    if(SUCCEEDED(hr))
      printf("\nThe Device Document URL is %S \n", bstrDeviceDocumentURL);
  }
    
cleanup:
  //release references to all interfaces 
  if(pDevFinder)
    pDevFinder->Release();
  if(pDevice)
    pDevice->Release();
  if(pDeviceDocument)
    pDeviceDocument->Release();
  
  // Free the bstr strings
  if(bstrDeviceDocumentURL)
    SysFreeString(bstrDeviceDocumentURL);
  if(bstrDeviceUDN)
    SysFreeString(bstrDeviceUDN);
  CoUninitialize();
  return 0;
}
```



 

 




