---
title: Raccolte di dispositivi restituite da ricerche sincrone
description: Le raccolte di dispositivi sono oggetti che contengono uno o più oggetti dispositivo. Una raccolta dispositivi espone l'interfaccia IUPnPDevices che fornisce i metodi e le proprietà per attraversare la raccolta ed estrarre i singoli oggetti dispositivo.
ms.assetid: 45455c3f-7281-4f96-a609-2efd2cf36aa2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd581b7c79fe67a825e411d53e8c44c0f3d4326
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118162"
---
# <a name="device-collections-returned-by-synchronous-searches"></a>Raccolte di dispositivi restituite da ricerche sincrone

Le raccolte di dispositivi sono oggetti che contengono uno o più oggetti dispositivo. Una raccolta dispositivi espone l'interfaccia [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) che fornisce i metodi e le proprietà per attraversare la raccolta ed estrarre i singoli oggetti dispositivo.

## <a name="vbscript-example"></a>Esempio di VBScript

Le applicazioni VBScript possono accedere agli oggetti nella raccolta in due modi. In primo luogo, possono attraversare gli elementi in sequenza usando un per... ogni... ciclo successivo, come illustrato nell'esempio seguente:


```VB
for each deviceObj in devices
    MsgBox(deviceObj.FriendlyName)
next
```



In questo esempio, si presuppone che la variabile Devices sia stata inizializzata con il risultato di una ricerca precedente. Il ciclo passa attraverso gli oggetti dispositivo della raccolta, assegnando la variabile deviceObj, a sua volta, il valore di ogni oggetto dispositivo. Il corpo del ciclo può contenere codice che elabora l'oggetto dispositivo.

## <a name="c-example"></a>Esempio C++

Nell'esempio seguente viene illustrato il codice C++ necessario per accedere agli oggetti in una raccolta di oggetti dispositivo. La funzione mostrata, **TraverseCollection**, riceve un puntatore all'interfaccia [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) come parametro di input. Questo puntatore di interfaccia può essere restituito dal metodo [**FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) o da altri metodi **Find** dell'oggetto Finder del dispositivo.


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")

HRESULT TraverseCollection(IUPnPDevices * pDevices)
{
    IUnknown * pUnk = NULL;
    HRESULT hr = pDevices->get__NewEnum(&pUnk);
    if (SUCCEEDED(hr))
    {
        IEnumVARIANT * pEnumVar = NULL;
        hr = pUnk->QueryInterface(IID_IEnumVARIANT, (void **) &pEnumVar);
        if (SUCCEEDED(hr))
        {
            VARIANT varCurDevice;
            VariantInit(&varCurDevice);
            pEnumVar->Reset();
            // Loop through each device in the collection
            while (S_OK == pEnumVar->Next(1, &varCurDevice, NULL))
            {
                IUPnPDevice * pDevice = NULL;
                IDispatch * pdispDevice = V_DISPATCH(&varCurDevice);
                if (SUCCEEDED(pdispDevice->QueryInterface(IID_IUPnPDevice, (void **) &pDevice)))
                {
                    // Do something interesting with pDevice
                    BSTR bstrName = NULL;
                    if (SUCCEEDED(pDevice->get_FriendlyName(&bstrName)))
                    {
                        OutputDebugStringW(bstrName);
                        SysFreeString(bstrName);
                    }
                }
                VariantClear(&varCurDevice);
                pDevice->Release();
            }
            pEnumVar->Release();
        }
        pUnk->Release();
    }
    return hr;
}
```



Il primo passaggio consiste nel richiedere un nuovo enumeratore per la raccolta usando la proprietà [**\_ NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) . Viene restituito un enumeratore come interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Il codice di esempio richiama [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere l'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) . Il codice di esempio imposta quindi l'enumeratore all'inizio della raccolta richiamando il metodo [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) . Infine, il codice di esempio richiama il metodo [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) per attraversare la raccolta. Gli oggetti dispositivo nella raccolta sono contenuti all'interno di strutture **Variant** . Queste strutture contengono puntatori alle interfacce [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) sugli oggetti dispositivo. Per ottenere l'interfaccia [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) , il codice di esempio richiama **QueryInterface** sull'interfaccia **IDispatch** .

 

 