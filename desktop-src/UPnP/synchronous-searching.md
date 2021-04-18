---
title: Ricerca sincrona
description: L'oggetto di ricerca del dispositivo Abilita le ricerche sincrone e asincrone. Le ricerche sincrone vengono completate e restituiscono il controllo all'applicazione chiamante solo dopo che sono stati trovati tutti i dispositivi disponibili.
ms.assetid: fa22cd53-6468-4958-b4e3-b1a41b3cb2f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1890829dfe8386cd79627dde039264dc81e473c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298659"
---
# <a name="synchronous-searching"></a>Ricerca sincrona

L'oggetto di ricerca del dispositivo Abilita le ricerche sincrone e asincrone. Le ricerche sincrone vengono completate e restituiscono il controllo all'applicazione chiamante solo dopo che sono stati trovati tutti i dispositivi disponibili. Per eseguire una ricerca sincrona, usare uno dei metodi di ricerca sincroni dell'interfaccia [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) .

> [!Note]  
> Per la restituzione delle ricerche sincrone sono necessario almeno nove secondi. Il ritardo è dovuto al fatto che il messaggio di ricerca UDP iniziale deve essere inviato più volte. Questa duplicazione rappresenta la non attendibilità del protocollo di rete sottostante. Le ricerche sincrone sono ideali per le interfacce della riga di comando. Non sono consigliate per le interfacce utente grafiche.

 

Il metodo [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) Cerca in base al dispositivo o al tipo di servizio. Questo metodo accetta un URI di tipo come parametro di input e restituisce una raccolta di oggetti dispositivo. Un oggetto dispositivo rappresenta un singolo dispositivo.

Gli esempi seguenti illustrano come eseguire una ricerca sincrona per i dispositivi in VBScript. Ogni script usa [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), chiamato con l'URI del tipo (ID servizio) per il tipo di dispositivo Media Player, *urn: schemas-UPnP-org: Device: MediaPlayer. v 1.00.00*. Il metodo restituisce una raccolta di oggetti dispositivo che corrisponde ai dispositivi Media Player trovati. Per informazioni sull'estrazione di singoli oggetti dispositivo da una raccolta, vedere la pagina relativa alle [raccolte di dispositivi restituite da ricerche sincrone](device-collections-returned-by-synchronous-searches.md).

## <a name="search-for-devices-by-type-in-vbscript"></a>Cerca i dispositivi per tipo in VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a>Cercare il dispositivo in base al tipo in C++

Nell'esempio seguente viene illustrata una ricerca sincrona per i dispositivi multimediali con C++. La funzione accetta come input un puntatore all'interfaccia [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) e restituisce il puntatore all'interfaccia [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .

Nell'esempio viene innanzitutto allocato un **BSTR** per rappresentare l'URI del tipo di dispositivo, quindi questo viene passato al metodo [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) . Passa anche l'indirizzo di un puntatore [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) locale nel buffer in cui il metodo archivia la raccolta di dispositivi trovati. Se la chiamata di funzione ha esito positivo, restituisce il puntatore a questa raccolta.


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



 

 




