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
# <a name="creating-the-device-finder"></a>Creazione del dispositivo di ricerca

Gli esempi seguenti illustrano come creare un'istanza dell'oggetto di ricerca del dispositivo in C++, Visual Basic e VBScript. I linguaggi di script usano l'ID programmatico (ProgID) [**UPnP. UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) per identificare la classe del Finder del dispositivo. Il codice C++ usa l'identificatore di classe.

## <a name="c-example"></a>Esempio C++


```C++
HRESULT hr = S_OK;
IUPnPDeviceFinder *pDeviceFinder = NULL;

hr = CoCreateInstance(CLSID_UPnPDeviceFinder, 
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IUPnPDeviceFinder,
                      (void **) &pDeviceFinder);
```



Come indicato in questo esempio di C++, l'oggetto di ricerca del dispositivo espone un'interfaccia predefinita, [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder). I metodi di questa interfaccia eseguono ricerche in base ai criteri di ricerca validi per un dispositivo basato su UPnP. Questa interfaccia è in grado di supportare l'automazione, quindi i relativi metodi possono essere chiamati dal codice di scripting.

## <a name="vbscript-example"></a>Esempio di VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




