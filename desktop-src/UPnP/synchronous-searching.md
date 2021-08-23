---
title: Ricerca sincrona
description: L'oggetto Device Finder abilita sia ricerche sincrone che asincrone. Le ricerche sincrone vengono completate e restituiscono il controllo all'applicazione chiamante solo dopo che sono stati trovati tutti i dispositivi disponibili.
ms.assetid: fa22cd53-6468-4958-b4e3-b1a41b3cb2f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f852957bed4bb73d9b31d0e26e099eb545b804953718d8cfd4e3cb44ea5f6c62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999501"
---
# <a name="synchronous-searching"></a>Ricerca sincrona

L'oggetto Device Finder abilita sia ricerche sincrone che asincrone. Le ricerche sincrone vengono completate e restituiscono il controllo all'applicazione chiamante solo dopo che sono stati trovati tutti i dispositivi disponibili. Per eseguire una ricerca sincrona, usare uno dei metodi di ricerca sincroni [**dell'interfaccia IUPnPDeviceFinder.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)

> [!Note]  
> La restituzione delle ricerche sincrone può richiedere almeno nove secondi. Il ritardo è causato dal fatto che il messaggio di ricerca UDP iniziale deve essere inviato più volte. Questa duplicazione rappresenta l'inaffiabilità del protocollo di rete sottostante. Le ricerche sincrone sono ottimali per le interfacce della riga di comando. Non sono consigliate per le interfacce utente grafiche.

 

Il [**metodo IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) esegue la ricerca in base al dispositivo o al tipo di servizio. Questo metodo accetta un URI di tipo come parametro di input e restituisce una raccolta di oggetti Device. Un oggetto Device rappresenta un singolo dispositivo.

Gli esempi seguenti illustrano come eseguire una ricerca sincrona dei dispositivi in VBScript. Ogni script usa [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), chiamato con l'URI del tipo (ID servizio) per il tipo di dispositivo lettore multimediale, *urn:schemas-upnp-org:device:mediaplayer.v1.00.00*. Il metodo restituisce una raccolta di oggetti Device che corrisponde ai dispositivi lettore multimediale trovati. Per informazioni sull'estrazione di singoli oggetti dispositivo da una raccolta, vedere Raccolte di dispositivi [restituite da ricerche sincrone.](device-collections-returned-by-synchronous-searches.md)

## <a name="search-for-devices-by-type-in-vbscript"></a>Cercare dispositivi per tipo in VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a>Cercare Dispositivo per tipo in C++

L'esempio seguente illustra una ricerca sincrona dei dispositivi lettore multimediale con C++. La funzione accetta un puntatore [**all'interfaccia IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) come input e restituisce il puntatore a interfaccia [**IUPnPDevices.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)

L'esempio alloca prima **un BSTR** per rappresentare l'URI del tipo di dispositivo e quindi lo passa al metodo [**IUPnPDeviceFinder::FindByType.**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) Passa anche l'indirizzo di un puntatore [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) locale nel buffer in cui il metodo archivia quindi la raccolta di dispositivi trovati. Se la chiamata di funzione ha esito positivo, restituisce il puntatore a questa raccolta.


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

IUPnPDevices *FindMediaPlayerDevices(IUPnPDeviceFinder *pDeviceFinder)
{
    HRESULT         hr = S_OK;
    IUPnPDevices    * pFoundDevices = NULL;
    BSTR            bstrTypeURI = NULL;

    bstrTypeURI = 
        SysAllocString(L"urn:schemas-upnp-org:device:multidisk-dvd");

    if (bstrTypeURI)
    {
        hr = pDeviceFinder->FindByType(bstrTypeURI, 
                                       0,
                                       &pFoundDevices);

        if (SUCCEEDED(hr))
        {
            wprintf(L"FindMediaPlayerDevices(): "
                    L"Search returned successfully\n");
        }
        else
        {
            fwprintf(stderr, L"FindMediaPlayerDevices(): "
                     L"FindByType search failed - returned "
                     L"HRESULT 0x%x\n",
                     hr);
            pFoundDevices = NULL;
        }
        SysFreeString(bstrTypeURI);
    }
    else
    {
        fwprintf(stderr, L"FindMediaPlayerDevices(): "
                 L"Could not allocate BSTR for type URI\n");
    }

    return pFoundDevices;
}
```



 

 




