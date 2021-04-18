---
title: Oggetto Request
description: Oggetto Request
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a50d554a5799af9a434b456113d7c826d2a0aa2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299648"
---
# <a name="the-request-object"></a><span data-ttu-id="8e980-103">Oggetto Request</span><span class="sxs-lookup"><span data-stu-id="8e980-103">The Request Object</span></span>

<span data-ttu-id="8e980-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8e980-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="8e980-105">Il server elabora alcuni metodi in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="8e980-105">The server processes some methods asynchronously.</span></span> <span data-ttu-id="8e980-106">Ciò consente al codice dell'applicazione di continuare mentre è in corso il completamento del metodo.</span><span class="sxs-lookup"><span data-stu-id="8e980-106">This enables your application code to continue while the method is completing.</span></span> <span data-ttu-id="8e980-107">Quando un'applicazione client chiama uno di questi metodi, il controllo Crea e restituisce un oggetto [**Request**](/windows/desktop/lwef/the-request-object) per la richiesta.</span><span class="sxs-lookup"><span data-stu-id="8e980-107">When a client application calls one of these methods, the control creates and returns a [**Request**](/windows/desktop/lwef/the-request-object) object for the request.</span></span> <span data-ttu-id="8e980-108">È possibile usare l'oggetto **Request** per tenere traccia dello stato del metodo assegnando una variabile oggetto al metodo.</span><span class="sxs-lookup"><span data-stu-id="8e980-108">You can use the **Request** object to track the status of the method by assigning an object variable to the method.</span></span> <span data-ttu-id="8e980-109">In Visual Basic dichiarare prima una variabile oggetto:</span><span class="sxs-lookup"><span data-stu-id="8e980-109">In Visual Basic, first declare an object variable:</span></span>


```
   Dim MyRequest as Object
```



<span data-ttu-id="8e980-110">In VBScript non è incluso il tipo di variabile nella dichiarazione:</span><span class="sxs-lookup"><span data-stu-id="8e980-110">In VBScript, you don't include the variable type in your declaration:</span></span>


```
   Dim MyRequest
```



<span data-ttu-id="8e980-111">Usare l'istruzione set di Visual Basic per assegnare la variabile alla chiamata al metodo:</span><span class="sxs-lookup"><span data-stu-id="8e980-111">And use Visual Basic's Set statement to assign the variable to the method call:</span></span>


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



<span data-ttu-id="8e980-112">Viene aggiunto un riferimento all'oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="8e980-112">This adds a reference to the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="8e980-113">L'oggetto **richiesta** verrà eliminato definitivamente quando non vi sono altri riferimenti.</span><span class="sxs-lookup"><span data-stu-id="8e980-113">The **Request** object will be destroyed when there are no more references to it.</span></span> <span data-ttu-id="8e980-114">La posizione in cui si dichiara l'oggetto **richiesta** e la relativa modalità di utilizzo determina la relativa durata.</span><span class="sxs-lookup"><span data-stu-id="8e980-114">Where you declare the **Request** object and how you use it determines its lifetime.</span></span> <span data-ttu-id="8e980-115">Se l'oggetto è dichiarato localmente a una subroutine o a una funzione, viene eliminato definitivamente quando esce dall'ambito. ovvero, al termine della subroutine o della funzione.</span><span class="sxs-lookup"><span data-stu-id="8e980-115">If the object is declared local to a subroutine or function, it will be destroyed when it goes out of scope; that is, when the subroutine or function ends.</span></span> <span data-ttu-id="8e980-116">Se l'oggetto viene dichiarato a livello globale, non verrà eliminato definitivamente fino a quando il programma non termina o un nuovo valore (o un valore impostato su "Empty") viene assegnato all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8e980-116">If the object is declared globally, it will not be destroyed until either the program terminates or a new value (or a value set to "empty") is assigned to the object.</span></span>

<span data-ttu-id="8e980-117">L'oggetto [**Request**](/windows/desktop/lwef/the-request-object) fornisce diverse proprietà su cui è possibile eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="8e980-117">The [**Request**](/windows/desktop/lwef/the-request-object) object provides several properties you can query.</span></span> <span data-ttu-id="8e980-118">Ad esempio, la proprietà [**status**](status-property.md) restituisce lo stato corrente della richiesta.</span><span class="sxs-lookup"><span data-stu-id="8e980-118">For example, the [**Status**](status-property.md) property returns the current status of the request.</span></span> <span data-ttu-id="8e980-119">È possibile usare questa proprietà per verificare lo stato della richiesta:</span><span class="sxs-lookup"><span data-stu-id="8e980-119">You can use this property to check the status of your request:</span></span>


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



<span data-ttu-id="8e980-120">La proprietà [**status**](status-property.md) restituisce lo stato di un oggetto [**Request**](/windows/desktop/lwef/the-request-object) come valore long integer.</span><span class="sxs-lookup"><span data-stu-id="8e980-120">The [**Status**](status-property.md) property returns the status of a [**Request**](/windows/desktop/lwef/the-request-object) object as a Long integer value.</span></span>



| <span data-ttu-id="8e980-121">Stato</span><span class="sxs-lookup"><span data-stu-id="8e980-121">Status</span></span> | <span data-ttu-id="8e980-122">Definizione</span><span class="sxs-lookup"><span data-stu-id="8e980-122">Definition</span></span>                                        |
|--------|---------------------------------------------------|
| <span data-ttu-id="8e980-123">0</span><span class="sxs-lookup"><span data-stu-id="8e980-123">0</span></span>      | <span data-ttu-id="8e980-124">La richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="8e980-124">Request successfully completed.</span></span>                   |
| <span data-ttu-id="8e980-125">1</span><span class="sxs-lookup"><span data-stu-id="8e980-125">1</span></span>      | <span data-ttu-id="8e980-126">Richiesta non riuscita.</span><span class="sxs-lookup"><span data-stu-id="8e980-126">Request failed.</span></span>                                   |
| <span data-ttu-id="8e980-127">2</span><span class="sxs-lookup"><span data-stu-id="8e980-127">2</span></span>      | <span data-ttu-id="8e980-128">Richiesta in sospeso (nella coda, ma non completata).</span><span class="sxs-lookup"><span data-stu-id="8e980-128">Request pending (in the queue, but not complete).</span></span> |
| <span data-ttu-id="8e980-129">3</span><span class="sxs-lookup"><span data-stu-id="8e980-129">3</span></span>      | <span data-ttu-id="8e980-130">Richiesta interrotta.</span><span class="sxs-lookup"><span data-stu-id="8e980-130">Request interrupted.</span></span>                              |
| <span data-ttu-id="8e980-131">4</span><span class="sxs-lookup"><span data-stu-id="8e980-131">4</span></span>      | <span data-ttu-id="8e980-132">Richiesta in corso.</span><span class="sxs-lookup"><span data-stu-id="8e980-132">Request in progress.</span></span>                              |



 

<span data-ttu-id="8e980-133">L'oggetto [**Request**](/windows/desktop/lwef/the-request-object) include anche un valore long integer nella proprietà [**Number**](https://www.bing.com/search?q=**Number**) che restituisce l'errore [**o la sua**](status-property.md) origine.</span><span class="sxs-lookup"><span data-stu-id="8e980-133">The [**Request**](/windows/desktop/lwef/the-request-object) object also includes a Long integer value in the [**Number**](https://www.bing.com/search?q=**Number**) property that returns the error or cause of the [**Status**](status-property.md) code.</span></span> <span data-ttu-id="8e980-134">Se None, questo valore è zero (0).</span><span class="sxs-lookup"><span data-stu-id="8e980-134">If none, this value is zero (0).</span></span> <span data-ttu-id="8e980-135">La proprietà [**Description**](description-property.md) contiene un valore stringa corrispondente al numero di errore.</span><span class="sxs-lookup"><span data-stu-id="8e980-135">The [**Description**](description-property.md) property contains a string value that corresponds to the error number.</span></span> <span data-ttu-id="8e980-136">Se la stringa non esiste, la **Descrizione** contiene "errore definito dall'applicazione o definito dall'oggetto".</span><span class="sxs-lookup"><span data-stu-id="8e980-136">If the string doesn't exist, **Description** contains "Application-defined or object-defined error".</span></span>

<span data-ttu-id="8e980-137">Per i valori e il significato restituiti dalla proprietà [**Number**](https://www.bing.com/search?q=**Number**) , vedere [codici di errore](microsoft-agent-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8e980-137">For the values and meaning returned by the [**Number**](https://www.bing.com/search?q=**Number**) property, see [Error Codes](microsoft-agent-error-codes.md).</span></span>

<span data-ttu-id="8e980-138">Il server inserisce le richieste di animazione nella coda del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="8e980-138">The server places animation requests in the specified character's queue.</span></span> <span data-ttu-id="8e980-139">Ciò consente al server di riprodurre l'animazione in un thread separato e il codice dell'applicazione può continuare mentre le animazioni vengono riprodotte.</span><span class="sxs-lookup"><span data-stu-id="8e980-139">This enables the server to play the animation on a separate thread, and your application's code can continue while animations play.</span></span> <span data-ttu-id="8e980-140">Se si crea un riferimento a un oggetto [**richiesta**](/windows/desktop/lwef/the-request-object) , il server invia automaticamente una notifica quando una richiesta di animazione viene avviata o completata tramite gli eventi [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) e [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) .</span><span class="sxs-lookup"><span data-stu-id="8e980-140">If you create a [**Request**](/windows/desktop/lwef/the-request-object) object reference, the server automatically notifies you when an animation request has started or completed through the [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) and [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) events.</span></span> <span data-ttu-id="8e980-141">Poiché i metodi che restituiscono oggetti **richiesta** sono asincroni e potrebbero non essere completati durante l'ambito della funzione chiamante, dichiarare il riferimento all'oggetto **Request** a livello globale.</span><span class="sxs-lookup"><span data-stu-id="8e980-141">Because methods that return **Request** objects are asynchronous and may not complete during the scope of the calling function, declare your reference to the **Request** object globally.</span></span>

<span data-ttu-id="8e980-142">Per restituire un oggetto [**Request**](/windows/desktop/lwef/the-request-object) , è possibile usare i metodi seguenti: [**GestureAt**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**interrupt**](interrupt-method.md), [**Load**](load-method.md), [**MoveTo**](moveto-method.md), [**Play**](play-method.md), [**show**](show-method.md), [**Speak**](speak-method.md)e [**wait**](https://www.bing.com/search?q=**Wait**).</span><span class="sxs-lookup"><span data-stu-id="8e980-142">The following methods can be used to return a [**Request**](/windows/desktop/lwef/the-request-object) object: [**GestureAt**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**Interrupt**](interrupt-method.md), [**Load**](load-method.md), [**MoveTo**](moveto-method.md), [**Play**](play-method.md), [**Show**](show-method.md), [**Speak**](speak-method.md), and [**Wait**](https://www.bing.com/search?q=**Wait**).</span></span>

 

 