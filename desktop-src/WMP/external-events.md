---
title: Eventi esterni
description: Eventi esterni
ms.assetid: d3fd8af6-8d7e-43b8-88fd-a59cf0cef609
keywords:
- Windows Media Player Skin, eventi esterni
- interfacce, eventi esterni
- eventi, esterni
- scrittura di codice per interfacce, eventi esterni
- eventi esterni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa09a01b709f0da51d09fc2bec70cba0a1b07d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298799"
---
# <a name="external-events"></a><span data-ttu-id="59cb5-108">Eventi esterni</span><span class="sxs-lookup"><span data-stu-id="59cb5-108">External Events</span></span>

<span data-ttu-id="59cb5-109">Quando gli utenti fanno clic su un pulsante o si preme un tasto, è possibile rispondere all'input con i gestori eventi.</span><span class="sxs-lookup"><span data-stu-id="59cb5-109">When users click a button or press a key, you can respond to their input with event handlers.</span></span> <span data-ttu-id="59cb5-110">Un gestore eventi è una sezione di codice che viene eseguito ogni volta che viene attivato l'evento.</span><span class="sxs-lookup"><span data-stu-id="59cb5-110">An event handler is a section of code that runs whenever the event is triggered.</span></span>

<span data-ttu-id="59cb5-111">Gli eventi seguenti sono supportati dagli elementi Skin:</span><span class="sxs-lookup"><span data-stu-id="59cb5-111">The following events are supported by skin elements:</span></span>

-   <span data-ttu-id="59cb5-112">**carico**</span><span class="sxs-lookup"><span data-stu-id="59cb5-112">**load**</span></span>
-   <span data-ttu-id="59cb5-113">**close**</span><span class="sxs-lookup"><span data-stu-id="59cb5-113">**close**</span></span>
-   <span data-ttu-id="59cb5-114">**ridimensionare**</span><span class="sxs-lookup"><span data-stu-id="59cb5-114">**resize**</span></span>
-   <span data-ttu-id="59cb5-115">**timer**</span><span class="sxs-lookup"><span data-stu-id="59cb5-115">**timer**</span></span>
-   <span data-ttu-id="59cb5-116">**Clicca**</span><span class="sxs-lookup"><span data-stu-id="59cb5-116">**click**</span></span>
-   <span data-ttu-id="59cb5-117">**DblClick**</span><span class="sxs-lookup"><span data-stu-id="59cb5-117">**dblclick**</span></span>
-   <span data-ttu-id="59cb5-118">**error**</span><span class="sxs-lookup"><span data-stu-id="59cb5-118">**error**</span></span>
-   <span data-ttu-id="59cb5-119">**MouseDown**</span><span class="sxs-lookup"><span data-stu-id="59cb5-119">**mousedown**</span></span>
-   <span data-ttu-id="59cb5-120">**MouseUp**</span><span class="sxs-lookup"><span data-stu-id="59cb5-120">**mouseup**</span></span>
-   <span data-ttu-id="59cb5-121">**MouseMove**</span><span class="sxs-lookup"><span data-stu-id="59cb5-121">**mousemove**</span></span>
-   <span data-ttu-id="59cb5-122">**MouseOver**</span><span class="sxs-lookup"><span data-stu-id="59cb5-122">**mouseover**</span></span>
-   <span data-ttu-id="59cb5-123">**mouseout**</span><span class="sxs-lookup"><span data-stu-id="59cb5-123">**mouseout**</span></span>
-   <span data-ttu-id="59cb5-124">**KeyPress**</span><span class="sxs-lookup"><span data-stu-id="59cb5-124">**keypress**</span></span>
-   <span data-ttu-id="59cb5-125">**KeyDown**</span><span class="sxs-lookup"><span data-stu-id="59cb5-125">**keydown**</span></span>
-   <span data-ttu-id="59cb5-126">**KeyUp**</span><span class="sxs-lookup"><span data-stu-id="59cb5-126">**keyup**</span></span>

<span data-ttu-id="59cb5-127">Per ulteriori informazioni su eventi specifici, vedere la Guida di riferimento per la [programmazione dell'interfaccia](skin-programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="59cb5-127">See the [Skin Programming Reference](skin-programming-reference.md) for more details about specific events.</span></span>

<span data-ttu-id="59cb5-128">Un tipico gestore eventi esterno denominare l'evento e definire il codice che verrà eseguito.</span><span class="sxs-lookup"><span data-stu-id="59cb5-128">A typical external event handler would name the event and define the code that will run.</span></span> <span data-ttu-id="59cb5-129">Se ad esempio si vuole creare codice per avviare Windows Media Player quando l'utente fa clic su un pulsante, inserire la riga seguente nel codice del pulsante.</span><span class="sxs-lookup"><span data-stu-id="59cb5-129">For example, if you want to create code to start Windows Media Player when the user clicks on a button, you would put the following line in your button code.</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "

```



<span data-ttu-id="59cb5-130">Verrà riprodotto il file denominato Laure. WMA.</span><span class="sxs-lookup"><span data-stu-id="59cb5-130">This will play the file named laure.wma.</span></span> <span data-ttu-id="59cb5-131">Si noti che la parola "on" viene aggiunta a eventi specifici.</span><span class="sxs-lookup"><span data-stu-id="59cb5-131">Note that you add the word "on" to specific events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59cb5-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59cb5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59cb5-133">**Gestione degli eventi**</span><span class="sxs-lookup"><span data-stu-id="59cb5-133">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




