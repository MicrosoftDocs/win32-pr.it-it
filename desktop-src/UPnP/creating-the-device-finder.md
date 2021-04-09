---
title: Creazione del dispositivo di ricerca
description: Gli esempi seguenti illustrano come creare un'istanza dell'oggetto di ricerca del dispositivo in C++, Visual Basic e VBScript.
ms.assetid: 0084a64d-458e-471c-a6be-aeb6ed0962d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a12fc7e269f2c0ce5b577fe2f49b6d13fe3b5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856646"
---
# <a name="creating-the-device-finder"></a><span data-ttu-id="22569-103">Creazione del dispositivo di ricerca</span><span class="sxs-lookup"><span data-stu-id="22569-103">Creating the Device Finder</span></span>

<span data-ttu-id="22569-104">Gli esempi seguenti illustrano come creare un'istanza dell'oggetto di ricerca del dispositivo in C++, Visual Basic e VBScript.</span><span class="sxs-lookup"><span data-stu-id="22569-104">The following examples demonstrate how to create an instance of the Device Finder object in C++, Visual Basic, and VBScript.</span></span> <span data-ttu-id="22569-105">I linguaggi di script usano l'ID programmatico (ProgID) [**UPnP. UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) per identificare la classe del Finder del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22569-105">The script languages use the programmatic ID (ProgID) [**UPnP.UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) to identify the Device Finder class.</span></span> <span data-ttu-id="22569-106">Il codice C++ usa l'identificatore di classe.</span><span class="sxs-lookup"><span data-stu-id="22569-106">The C++ code uses the class identifier.</span></span>

## <a name="c-example"></a><span data-ttu-id="22569-107">Esempio C++</span><span class="sxs-lookup"><span data-stu-id="22569-107">C++ Example</span></span>


```C++
HRESULT hr = S_OK;
IUPnPDeviceFinder *pDeviceFinder = NULL;

hr = CoCreateInstance(CLSID_UPnPDeviceFinder, 
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IUPnPDeviceFinder,
                      (void **) &pDeviceFinder);
```



<span data-ttu-id="22569-108">Come indicato in questo esempio di C++, l'oggetto di ricerca del dispositivo espone un'interfaccia predefinita, [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder).</span><span class="sxs-lookup"><span data-stu-id="22569-108">As this C++ example indicates, the Device Finder object exposes a default interface, [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder).</span></span> <span data-ttu-id="22569-109">I metodi di questa interfaccia eseguono ricerche in base ai criteri di ricerca validi per un dispositivo basato su UPnP.</span><span class="sxs-lookup"><span data-stu-id="22569-109">The methods of this interface perform searches according to the valid search criteria for a UPnP-based device.</span></span> <span data-ttu-id="22569-110">Questa interfaccia è in grado di supportare l'automazione, quindi i relativi metodi possono essere chiamati dal codice di scripting.</span><span class="sxs-lookup"><span data-stu-id="22569-110">This interface is Automation capable, so its methods can be called by scripting code.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="22569-111">Esempio di VBScript</span><span class="sxs-lookup"><span data-stu-id="22569-111">VBScript Example</span></span>


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




