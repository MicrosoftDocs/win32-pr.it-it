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
# <a name="describing-devices"></a>Descrizione dei dispositivi

Esistono due modi per ottenere gli oggetti dispositivo:

-   Utilizzando l'interfaccia [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) . L'interfaccia **IUPnPDescriptionDocument** è l'unica interfaccia sicura per lo scripting.
-   Utilizzo dell'interfaccia [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) per ottenere un'interfaccia [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .

Entrambi i metodi restituiscono raccolte di dispositivi. Le applicazioni usano quindi i metodi del dispositivo per recuperare le proprietà sui dispositivi.

Le applicazioni sono in grado di recuperare i tipi di informazioni seguenti:

-   Informazioni sulla gerarchia dei dispositivi, inclusi i dispositivi radice, i dispositivi padre e i dispositivi figlio.
-   Proprietà del dispositivo, tra cui UDNs, URI (Uniform Resource Identifier) e nomi leggibili dall'utente.
-   Informazioni sul produttore, inclusi i nomi e le pagine Web correlate.
-   Informazioni sul modello, inclusi il nome, il numero, l'UPC, i numeri di serie e le descrizioni dei dispositivi.
-   Visualizzare le informazioni, incluso l'URL per controllare il dispositivo e gli URL da cui vengono scaricate le icone.
-   Servizi forniti da un particolare dispositivo.

Le applicazioni ottengono anche l'URL del documento di descrizione del dispositivo usando l'interfaccia [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess) . L'applicazione carica quindi il documento di descrizione e utilizza le proprietà del dispositivo e del servizio che non sono esposte dall'interfaccia [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) . Questa interfaccia non può essere utilizzata nello scripting, perché non è l'interfaccia predefinita.

## <a name="visual-basic-example"></a>Esempio di Visual Basic

Il codice di esempio seguente illustra l'uso di [**IUPnPDeviceDocumentAccess:: GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).


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



## <a name="c-example"></a>Esempio C++

Il codice di esempio seguente illustra l'uso di [**IUPnPDeviceDocumentAccess:: GetDocumentURL**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl).


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



 

 




