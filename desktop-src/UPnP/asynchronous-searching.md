---
title: Ricerca asincrona
description: L'oggetto di ricerca del dispositivo Abilita le ricerche sincrone e asincrone. Le ricerche asincrone restituiscono immediatamente il controllo all'applicazione chiamante.
ms.assetid: 809cfb65-9d08-427b-90d9-b8a836176341
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57377eb8ae5a49fc9bafe81f90b9ee7c602ae4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955747"
---
# <a name="asynchronous-searching"></a>Ricerca asincrona

L'oggetto di ricerca del dispositivo Abilita le ricerche sincrone e asincrone. Le ricerche asincrone restituiscono immediatamente il controllo all'applicazione chiamante. Quindi, l'applicazione riceve una notifica su ogni singolo dispositivo come viene trovato, usando un'interfaccia di callback che l'applicazione ha registrato.

La ricerca asincrona è ideale per le interfacce utente grafiche e per le applicazioni che eseguono il monitoraggio continuo.

La struttura generale di una ricerca asincrona è la seguente:

1.  Creare un oggetto di ricerca
2.  Avvia la ricerca
3.  Ricevere le notifiche di callback e intraprendere i passaggi di elaborazione appropriati.
4.  Quando la ricerca non è più necessaria, annullare la ricerca e rilasciare gli oggetti associati.

> [!Note]  
> Nel codice di callback, un'applicazione non può rilasciare l'oggetto a cui riceve la notifica, ad esempio un nuovo dispositivo, né l'applicazione annulla la ricerca.

 

## <a name="c-example"></a>Esempio C++

Le applicazioni C++ devono implementare un oggetto callback da passare alla ricerca. Per il codice di esempio che illustra questa azione, vedere [ricerca asincrona in C++](searching-asynchronously-in-c-.md) .

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



 

 




