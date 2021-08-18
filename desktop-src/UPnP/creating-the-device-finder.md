---
title: Creazione di Device Finder
description: Gli esempi seguenti illustrano come creare un'istanza dell'oggetto Device Finder in C++, Visual Basic e VBScript.
ms.assetid: 0084a64d-458e-471c-a6be-aeb6ed0962d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6af75ea5c267e156f89f1ae1e27a08928c097bbfea731f59add575397fbc00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137358"
---
# <a name="creating-the-device-finder"></a>Creazione di Device Finder

Gli esempi seguenti illustrano come creare un'istanza dell'oggetto Device Finder in C++, Visual Basic e VBScript. I linguaggi di script usano l'ID programmatico (ProgID) [**UPnP.UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) per identificare la classe Device Finder. Il codice C++ usa l'identificatore di classe.

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



Come indicato in questo esempio di C++, l'oggetto Device Finder espone un'interfaccia predefinita, [**IUPnPDeviceFinder.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) I metodi di questa interfaccia eseguono ricerche in base ai criteri di ricerca validi per un dispositivo basato su UPnP. Questa interfaccia supporta Automazione, quindi i relativi metodi possono essere chiamati dal codice di scripting.

## <a name="vbscript-example"></a>Esempio di VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




