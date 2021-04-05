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
# <a name="device-collections-returned-by-synchronous-searches"></a><span data-ttu-id="49b0b-104">Raccolte di dispositivi restituite da ricerche sincrone</span><span class="sxs-lookup"><span data-stu-id="49b0b-104">Device Collections Returned By Synchronous Searches</span></span>

<span data-ttu-id="49b0b-105">Le raccolte di dispositivi sono oggetti che contengono uno o più oggetti dispositivo.</span><span class="sxs-lookup"><span data-stu-id="49b0b-105">Device collections are objects that contain one or more Device objects.</span></span> <span data-ttu-id="49b0b-106">Una raccolta dispositivi espone l'interfaccia [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) che fornisce i metodi e le proprietà per attraversare la raccolta ed estrarre i singoli oggetti dispositivo.</span><span class="sxs-lookup"><span data-stu-id="49b0b-106">A Device collection exposes the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface that provides methods and properties for traversing the collection and extracting individual device objects.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="49b0b-107">Esempio di VBScript</span><span class="sxs-lookup"><span data-stu-id="49b0b-107">VBScript Example</span></span>

<span data-ttu-id="49b0b-108">Le applicazioni VBScript possono accedere agli oggetti nella raccolta in due modi.</span><span class="sxs-lookup"><span data-stu-id="49b0b-108">VBScript applications can access the objects in the collection in two ways.</span></span> <span data-ttu-id="49b0b-109">In primo luogo, possono attraversare gli elementi in sequenza usando un per...</span><span class="sxs-lookup"><span data-stu-id="49b0b-109">First, they can traverse the elements sequentially using a for …</span></span> <span data-ttu-id="49b0b-110">ogni... ciclo successivo, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="49b0b-110">each ... next loop as shown in the following example:</span></span>


```VB
for each deviceObj in devices
    MsgBox(deviceObj.FriendlyName)
next
```



<span data-ttu-id="49b0b-111">In questo esempio, si presuppone che la variabile Devices sia stata inizializzata con il risultato di una ricerca precedente.</span><span class="sxs-lookup"><span data-stu-id="49b0b-111">In this example, the devices variable is assumed to have been initialized with the result of a prior search.</span></span> <span data-ttu-id="49b0b-112">Il ciclo passa attraverso gli oggetti dispositivo della raccolta, assegnando la variabile deviceObj, a sua volta, il valore di ogni oggetto dispositivo.</span><span class="sxs-lookup"><span data-stu-id="49b0b-112">The loop steps through the Device objects in the collection, assigning the variable deviceObj the value of each Device object in turn.</span></span> <span data-ttu-id="49b0b-113">Il corpo del ciclo può contenere codice che elabora l'oggetto dispositivo.</span><span class="sxs-lookup"><span data-stu-id="49b0b-113">The body of the loop can contain code that processes the Device object.</span></span>

## <a name="c-example"></a><span data-ttu-id="49b0b-114">Esempio C++</span><span class="sxs-lookup"><span data-stu-id="49b0b-114">C++ Example</span></span>

<span data-ttu-id="49b0b-115">Nell'esempio seguente viene illustrato il codice C++ necessario per accedere agli oggetti in una raccolta di oggetti dispositivo.</span><span class="sxs-lookup"><span data-stu-id="49b0b-115">The following example shows the C++ code required to access the objects in a collection of device objects.</span></span> <span data-ttu-id="49b0b-116">La funzione mostrata, **TraverseCollection**, riceve un puntatore all'interfaccia [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="49b0b-116">The function shown, **TraverseCollection**, receives a pointer to the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface as an input parameter.</span></span> <span data-ttu-id="49b0b-117">Questo puntatore di interfaccia può essere restituito dal metodo [**FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) o da altri metodi **Find** dell'oggetto Finder del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="49b0b-117">This interface pointer could be returned by the [**FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method, or other **Find** methods, of the Device Finder object.</span></span>


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



<span data-ttu-id="49b0b-118">Il primo passaggio consiste nel richiedere un nuovo enumeratore per la raccolta usando la proprietà [**\_ NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) .</span><span class="sxs-lookup"><span data-stu-id="49b0b-118">The first step is to request a new enumerator for the collection using the [**\_NewEnum**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) property.</span></span> <span data-ttu-id="49b0b-119">Viene restituito un enumeratore come interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="49b0b-119">This returns an enumerator as the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="49b0b-120">Il codice di esempio richiama [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere l'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="49b0b-120">The sample code invokes [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain the [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface.</span></span> <span data-ttu-id="49b0b-121">Il codice di esempio imposta quindi l'enumeratore all'inizio della raccolta richiamando il metodo [**IEnumVARIANT:: Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) .</span><span class="sxs-lookup"><span data-stu-id="49b0b-121">The sample code then sets the enumerator to the beginning of the collection by invoking the [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) method.</span></span> <span data-ttu-id="49b0b-122">Infine, il codice di esempio richiama il metodo [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) per attraversare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="49b0b-122">Finally, the sample code invokes the [**IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) method to traverse the collection.</span></span> <span data-ttu-id="49b0b-123">Gli oggetti dispositivo nella raccolta sono contenuti all'interno di strutture **Variant** .</span><span class="sxs-lookup"><span data-stu-id="49b0b-123">The device objects in the collection are contained within **VARIANT** structures.</span></span> <span data-ttu-id="49b0b-124">Queste strutture contengono puntatori alle interfacce [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) sugli oggetti dispositivo.</span><span class="sxs-lookup"><span data-stu-id="49b0b-124">These structures contain pointers to [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces on the device objects.</span></span> <span data-ttu-id="49b0b-125">Per ottenere l'interfaccia [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) , il codice di esempio richiama **QueryInterface** sull'interfaccia **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="49b0b-125">To obtain the [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) interface, the sample code invokes **QueryInterface** on the **IDispatch** interface.</span></span>

 

 