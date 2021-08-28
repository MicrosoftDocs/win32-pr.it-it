---
title: Ricerca asincrona
description: L'oggetto Device Finder consente ricerche sincrone e asincrone. Le ricerche asincrone restituiscono immediatamente il controllo all'applicazione chiamante.
ms.assetid: 809cfb65-9d08-427b-90d9-b8a836176341
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3482e041798db929d1719e1a404823f161f9bf5b0e499f4eca1694df24b38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058139"
---
# <a name="asynchronous-searching"></a>Ricerca asincrona

L'oggetto Device Finder consente ricerche sincrone e asincrone. Le ricerche asincrone restituiscono immediatamente il controllo all'applicazione chiamante. L'applicazione viene quindi notificata a ogni singolo dispositivo non appena viene trovato, usando un'interfaccia di callback registrata dall'applicazione.

La ricerca asincrona è ideale per le interfacce utente grafiche e le applicazioni che eseguono il monitoraggio continuo.

La struttura generale di una ricerca asincrona è:

1.  Creare un oggetto di ricerca
2.  Avviare la ricerca
3.  Ricevere notifiche di callback ed eseguire i passaggi di elaborazione appropriati.
4.  Quando la ricerca non è più necessaria, annulla la ricerca e rilascia gli oggetti associati.

> [!Note]  
> Nel codice di callback, un'applicazione non può rilasciare l'oggetto per cui sta ricevendo una notifica, ad esempio un nuovo dispositivo, né può annullare la ricerca.

 

## <a name="c-example"></a>Esempio C++

Le applicazioni C++ devono implementare un oggetto callback da passare alla ricerca. Vedere [Ricerca asincrona in C++ per](searching-asynchronously-in-c-.md) il codice di esempio che illustra questa azione.

## <a name="vbscript-example"></a>Esempio di VBScript

Il codice VBScript deve passare l'indirizzo della funzione di callback.


```VB
Sub DeviceFinderCallback (device, UDN, calltype)

  select case calltype
    Case 0
      output = "Found: " & vbCrLf
      output = output & "DisplayName: " & device.FriendlyName & vbCrLf
      output = output & "Type: " & device.Type & vbCrLf
      output = output & "UDN: " & device.UniqueDeviceName & vbCrLf
      MsgBox output

    Case 1
      MsgBox "device removed: " & UDN

    Case 2
      MsgBox "search complete"

    end select
End Sub

Dim devicefinder
Dim findData

Set devicefinder = CreateObject("UPnP.UPnPDeviceFinder")

Sub StartFind()
  findData = devicefinder.CreateAsyncFind("upnp:rootdevice", 0, _
   GetRef("DeviceFinderCallback"))

  devicefinder.StartAsyncFind(findData)
End Sub

Sub StopFind()
  deviceFinder.CancelAsyncFind(findData)
End Sub
```



 

 




