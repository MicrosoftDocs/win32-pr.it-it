---
title: Eventi secondari
description: Eventi secondari
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Windows Media Player Skin, eventi secondari
- interfacce, eventi secondari
- eventi, secondari
- scrittura di codice per interfacce, eventi secondari
- eventi secondari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e04785a7468353665083287ac1b74bce5cbf0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471595"
---
# <a name="secondary-events"></a><span data-ttu-id="c9839-108">Eventi secondari</span><span class="sxs-lookup"><span data-stu-id="c9839-108">Secondary Events</span></span>

<span data-ttu-id="c9839-109">È possibile determinare gli altri eventi che avvengono quando viene attivato un evento specifico.</span><span class="sxs-lookup"><span data-stu-id="c9839-109">You can determine what other events are taking place when a specific event is triggered.</span></span> <span data-ttu-id="c9839-110">Ad esempio, quando si fa clic su un pulsante del mouse, è possibile che si desideri sapere se il tasto ALT è stato disattivato nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="c9839-110">For example, when a mouse button is clicked, you may want to know whether the ALT key was down at the same time.</span></span>

## <a name="event-attributes"></a><span data-ttu-id="c9839-111">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="c9839-111">Event Attributes</span></span>

<span data-ttu-id="c9839-112">Per le interfacce sono supportati gli attributi di evento seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9839-112">The following event attributes are supported for skins:</span></span>

-   <span data-ttu-id="c9839-113">**altKey**</span><span class="sxs-lookup"><span data-stu-id="c9839-113">**altKey**</span></span>
-   <span data-ttu-id="c9839-114">**pulsante**</span><span class="sxs-lookup"><span data-stu-id="c9839-114">**button**</span></span>
-   <span data-ttu-id="c9839-115">**clientX**</span><span class="sxs-lookup"><span data-stu-id="c9839-115">**clientX**</span></span>
-   <span data-ttu-id="c9839-116">**clientY**</span><span class="sxs-lookup"><span data-stu-id="c9839-116">**clientY**</span></span>
-   <span data-ttu-id="c9839-117">**ctrlKey**</span><span class="sxs-lookup"><span data-stu-id="c9839-117">**ctrlKey**</span></span>
-   <span data-ttu-id="c9839-118">**fromElement**</span><span class="sxs-lookup"><span data-stu-id="c9839-118">**fromElement**</span></span>
-   <span data-ttu-id="c9839-119">**offsetX**</span><span class="sxs-lookup"><span data-stu-id="c9839-119">**offsetX**</span></span>
-   <span data-ttu-id="c9839-120">**offsetY**</span><span class="sxs-lookup"><span data-stu-id="c9839-120">**offsetY**</span></span>
-   <span data-ttu-id="c9839-121">**screenX**</span><span class="sxs-lookup"><span data-stu-id="c9839-121">**screenX**</span></span>
-   <span data-ttu-id="c9839-122">**screenY**</span><span class="sxs-lookup"><span data-stu-id="c9839-122">**screenY**</span></span>
-   <span data-ttu-id="c9839-123">**shiftKey**</span><span class="sxs-lookup"><span data-stu-id="c9839-123">**shiftKey**</span></span>
-   <span data-ttu-id="c9839-124">**srcElement**</span><span class="sxs-lookup"><span data-stu-id="c9839-124">**srcElement**</span></span>
-   <span data-ttu-id="c9839-125">**toElement**</span><span class="sxs-lookup"><span data-stu-id="c9839-125">**toElement**</span></span>
-   <span data-ttu-id="c9839-126">**x**</span><span class="sxs-lookup"><span data-stu-id="c9839-126">**x**</span></span>
-   <span data-ttu-id="c9839-127">**y**</span><span class="sxs-lookup"><span data-stu-id="c9839-127">**y**</span></span>
-   <span data-ttu-id="c9839-128">**keyCode**</span><span class="sxs-lookup"><span data-stu-id="c9839-128">**keyCode**</span></span>

<span data-ttu-id="c9839-129">Per ulteriori informazioni su questi attributi, vedere la Guida di riferimento per la [programmazione dell'interfaccia](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="c9839-129">For more information about these attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="using-secondary-events"></a><span data-ttu-id="c9839-130">Uso di eventi secondari</span><span class="sxs-lookup"><span data-stu-id="c9839-130">Using Secondary Events</span></span>

<span data-ttu-id="c9839-131">È possibile elaborare solo gli attributi di evento nel codice JScript.</span><span class="sxs-lookup"><span data-stu-id="c9839-131">You can only process event attributes in JScript code.</span></span> <span data-ttu-id="c9839-132">È necessario utilizzare la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="c9839-132">You must use the following syntax:</span></span>


```C++
event.eventattributename
```



<span data-ttu-id="c9839-133">*eventattributename* è il nome dell'attributo dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c9839-133">*eventattributename* is the name of the event attribute.</span></span> <span data-ttu-id="c9839-134">Per determinare, ad esempio, se il tasto ALT è stato premuto durante un evento di clic, è possibile utilizzare le righe seguenti nel codice JScript:</span><span class="sxs-lookup"><span data-stu-id="c9839-134">For example, to determine whether the ALT key was pressed during a click event, you could use the following lines in your JScript code:</span></span>


```C++
wasAlt = event.altKey ;
if (wasAlt = true)
{
   // Do something here.
}
```



## <a name="related-topics"></a><span data-ttu-id="c9839-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9839-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9839-136">**Gestione degli eventi**</span><span class="sxs-lookup"><span data-stu-id="c9839-136">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




