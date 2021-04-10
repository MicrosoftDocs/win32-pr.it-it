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
# <a name="asynchronous-searching"></a><span data-ttu-id="08110-104">Ricerca asincrona</span><span class="sxs-lookup"><span data-stu-id="08110-104">Asynchronous Searching</span></span>

<span data-ttu-id="08110-105">L'oggetto di ricerca del dispositivo Abilita le ricerche sincrone e asincrone.</span><span class="sxs-lookup"><span data-stu-id="08110-105">The Device Finder object enables both synchronous and asynchronous searches.</span></span> <span data-ttu-id="08110-106">Le ricerche asincrone restituiscono immediatamente il controllo all'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="08110-106">Asynchronous searches return control to the calling application immediately.</span></span> <span data-ttu-id="08110-107">Quindi, l'applicazione riceve una notifica su ogni singolo dispositivo come viene trovato, usando un'interfaccia di callback che l'applicazione ha registrato.</span><span class="sxs-lookup"><span data-stu-id="08110-107">Then, the application is notified about each individual device as it is found, using a callback interface that the application has registered.</span></span>

<span data-ttu-id="08110-108">La ricerca asincrona è ideale per le interfacce utente grafiche e per le applicazioni che eseguono il monitoraggio continuo.</span><span class="sxs-lookup"><span data-stu-id="08110-108">Asynchronous searching is best for graphical user interfaces, and applications that perform continuous monitoring.</span></span>

<span data-ttu-id="08110-109">La struttura generale di una ricerca asincrona è la seguente:</span><span class="sxs-lookup"><span data-stu-id="08110-109">The general structure of an asynchronous search is:</span></span>

1.  <span data-ttu-id="08110-110">Creare un oggetto di ricerca</span><span class="sxs-lookup"><span data-stu-id="08110-110">Create a search object</span></span>
2.  <span data-ttu-id="08110-111">Avvia la ricerca</span><span class="sxs-lookup"><span data-stu-id="08110-111">Start the search</span></span>
3.  <span data-ttu-id="08110-112">Ricevere le notifiche di callback e intraprendere i passaggi di elaborazione appropriati.</span><span class="sxs-lookup"><span data-stu-id="08110-112">Receive callback notifications and take the appropriate processing steps.</span></span>
4.  <span data-ttu-id="08110-113">Quando la ricerca non è più necessaria, annullare la ricerca e rilasciare gli oggetti associati.</span><span class="sxs-lookup"><span data-stu-id="08110-113">When the search is no longer needed, cancel the search and release the associated objects.</span></span>

> [!Note]  
> <span data-ttu-id="08110-114">Nel codice di callback, un'applicazione non può rilasciare l'oggetto a cui riceve la notifica, ad esempio un nuovo dispositivo, né l'applicazione annulla la ricerca.</span><span class="sxs-lookup"><span data-stu-id="08110-114">In the callback code, an application cannot release the object it is receiving notification about, such as a new device, nor can the application cancel the search.</span></span>

 

## <a name="c-example"></a><span data-ttu-id="08110-115">Esempio C++</span><span class="sxs-lookup"><span data-stu-id="08110-115">C++ Example</span></span>

<span data-ttu-id="08110-116">Le applicazioni C++ devono implementare un oggetto callback da passare alla ricerca.</span><span class="sxs-lookup"><span data-stu-id="08110-116">C++ applications must implement a callback object to pass to the search.</span></span> <span data-ttu-id="08110-117">Per il codice di esempio che illustra questa azione, vedere [ricerca asincrona in C++](searching-asynchronously-in-c-.md) .</span><span class="sxs-lookup"><span data-stu-id="08110-117">See [Searching Asynchronously in C++](searching-asynchronously-in-c-.md) for sample code that illustrates this action.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="08110-118">Esempio di VBScript</span><span class="sxs-lookup"><span data-stu-id="08110-118">VBScript Example</span></span>

<span data-ttu-id="08110-119">Il codice VBScript deve passare l'indirizzo della funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="08110-119">VBScript code must pass the address of the callback function.</span></span>


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



 

 




