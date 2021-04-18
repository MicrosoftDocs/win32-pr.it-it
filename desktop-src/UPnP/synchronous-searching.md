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
# <a name="synchronous-searching"></a><span data-ttu-id="46f03-104">Ricerca sincrona</span><span class="sxs-lookup"><span data-stu-id="46f03-104">Synchronous Searching</span></span>

<span data-ttu-id="46f03-105">L'oggetto di ricerca del dispositivo Abilita le ricerche sincrone e asincrone.</span><span class="sxs-lookup"><span data-stu-id="46f03-105">The Device Finder object enables both synchronous and asynchronous searches.</span></span> <span data-ttu-id="46f03-106">Le ricerche sincrone vengono completate e restituiscono il controllo all'applicazione chiamante solo dopo che sono stati trovati tutti i dispositivi disponibili.</span><span class="sxs-lookup"><span data-stu-id="46f03-106">Synchronous searches are completed and return control to the calling application only after all available devices are found.</span></span> <span data-ttu-id="46f03-107">Per eseguire una ricerca sincrona, usare uno dei metodi di ricerca sincroni dell'interfaccia [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) .</span><span class="sxs-lookup"><span data-stu-id="46f03-107">To perform a synchronous search, use one of the synchronous search methods of the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface.</span></span>

> [!Note]  
> <span data-ttu-id="46f03-108">Per la restituzione delle ricerche sincrone sono necessario almeno nove secondi.</span><span class="sxs-lookup"><span data-stu-id="46f03-108">Synchronous searches take at least nine seconds to return.</span></span> <span data-ttu-id="46f03-109">Il ritardo è dovuto al fatto che il messaggio di ricerca UDP iniziale deve essere inviato più volte.</span><span class="sxs-lookup"><span data-stu-id="46f03-109">The delay is caused because the initial UDP search message must be sent multiple times.</span></span> <span data-ttu-id="46f03-110">Questa duplicazione rappresenta la non attendibilità del protocollo di rete sottostante.</span><span class="sxs-lookup"><span data-stu-id="46f03-110">This duplication accounts for the unreliability of the underlying network protocol.</span></span> <span data-ttu-id="46f03-111">Le ricerche sincrone sono ideali per le interfacce della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="46f03-111">Synchronous searches are best for command-line interfaces.</span></span> <span data-ttu-id="46f03-112">Non sono consigliate per le interfacce utente grafiche.</span><span class="sxs-lookup"><span data-stu-id="46f03-112">They are not recommended for graphical user interfaces.</span></span>

 

<span data-ttu-id="46f03-113">Il metodo [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) Cerca in base al dispositivo o al tipo di servizio.</span><span class="sxs-lookup"><span data-stu-id="46f03-113">The [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method searches by device or service type.</span></span> <span data-ttu-id="46f03-114">Questo metodo accetta un URI di tipo come parametro di input e restituisce una raccolta di oggetti dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46f03-114">This method takes a type URI as an input parameter and returns a collection of Device objects.</span></span> <span data-ttu-id="46f03-115">Un oggetto dispositivo rappresenta un singolo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46f03-115">A Device object represents an individual device.</span></span>

<span data-ttu-id="46f03-116">Gli esempi seguenti illustrano come eseguire una ricerca sincrona per i dispositivi in VBScript.</span><span class="sxs-lookup"><span data-stu-id="46f03-116">The following examples demonstrate how to perform a synchronous search for devices in VBScript.</span></span> <span data-ttu-id="46f03-117">Ogni script usa [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), chiamato con l'URI del tipo (ID servizio) per il tipo di dispositivo Media Player, *urn: schemas-UPnP-org: Device: MediaPlayer. v 1.00.00*.</span><span class="sxs-lookup"><span data-stu-id="46f03-117">Each script uses [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), called with the type URI (service ID) for the media player device type, *urn:schemas-upnp-org:device:mediaplayer.v1.00.00*.</span></span> <span data-ttu-id="46f03-118">Il metodo restituisce una raccolta di oggetti dispositivo che corrisponde ai dispositivi Media Player trovati.</span><span class="sxs-lookup"><span data-stu-id="46f03-118">The method returns a collection of Device objects that corresponds to media player devices that were found.</span></span> <span data-ttu-id="46f03-119">Per informazioni sull'estrazione di singoli oggetti dispositivo da una raccolta, vedere la pagina relativa alle [raccolte di dispositivi restituite da ricerche sincrone](device-collections-returned-by-synchronous-searches.md).</span><span class="sxs-lookup"><span data-stu-id="46f03-119">For information on extracting individual device objects from a collection, see [Device Collections Returned By Synchronous Searches](device-collections-returned-by-synchronous-searches.md).</span></span>

## <a name="search-for-devices-by-type-in-vbscript"></a><span data-ttu-id="46f03-120">Cerca i dispositivi per tipo in VBScript</span><span class="sxs-lookup"><span data-stu-id="46f03-120">Search for Devices by Type in VBScript</span></span>


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a><span data-ttu-id="46f03-121">Cercare il dispositivo in base al tipo in C++</span><span class="sxs-lookup"><span data-stu-id="46f03-121">Search for Device by Type in C++</span></span>

<span data-ttu-id="46f03-122">Nell'esempio seguente viene illustrata una ricerca sincrona per i dispositivi multimediali con C++.</span><span class="sxs-lookup"><span data-stu-id="46f03-122">The following example demonstrates a synchronous search for media player devices using C++.</span></span> <span data-ttu-id="46f03-123">La funzione accetta come input un puntatore all'interfaccia [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) e restituisce il puntatore all'interfaccia [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) .</span><span class="sxs-lookup"><span data-stu-id="46f03-123">The function takes a pointer to the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface as input, and returns the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface pointer.</span></span>

<span data-ttu-id="46f03-124">Nell'esempio viene innanzitutto allocato un **BSTR** per rappresentare l'URI del tipo di dispositivo, quindi questo viene passato al metodo [**IUPnPDeviceFinder:: FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) .</span><span class="sxs-lookup"><span data-stu-id="46f03-124">The example first allocates a **BSTR** to represent the device type URI and then passes this to the [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method.</span></span> <span data-ttu-id="46f03-125">Passa anche l'indirizzo di un puntatore [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) locale nel buffer in cui il metodo archivia la raccolta di dispositivi trovati.</span><span class="sxs-lookup"><span data-stu-id="46f03-125">It also passes the address of a local [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) pointer in the buffer in which the method then stores the collection of devices found.</span></span> <span data-ttu-id="46f03-126">Se la chiamata di funzione ha esito positivo, restituisce il puntatore a questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="46f03-126">If the function call is successful, it returns the pointer to this collection.</span></span>


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



 

 




