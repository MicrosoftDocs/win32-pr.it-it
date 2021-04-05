---
title: Utilizzo dell'elemento Handles
description: Utilizzo dell'elemento Handles
ms.assetid: d748f74c-40e5-499a-bb61-94862eb3811c
keywords:
- Web Workshop, Handles-elemento
- progettazione di pagine Web, Handles-elemento
- Vector Markup Language (la), Handles-elemento
- LA (Vector Markup Language), Handles-elemento
- Vector graphics, Handles-elemento
- Handles-elemento
- Elementi la, handle
- Forme la, Handles-elemento
- Vector Markup Language (la), associazione di testo a forme
- LA (Vector Markup Language), associazione di testo a forme
- grafica vettoriale, associazione di testo a forme
- LA forme, associazione di testo
- associazione di testo a forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54c721d50f51c46cd4bf08393e85ad83307fc1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046802"
---
# <a name="using-the-handles-element"></a><span data-ttu-id="da33b-116">Utilizzo dell'elemento Handles</span><span class="sxs-lookup"><span data-stu-id="da33b-116">Using the Handles Element</span></span>

<span data-ttu-id="da33b-117">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="da33b-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="da33b-118">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="da33b-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="da33b-119">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="da33b-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="da33b-120">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="da33b-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="da33b-121">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="da33b-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="da33b-122">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="da33b-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="da33b-123">In questo argomento verrà illustrato come utilizzare l' `<handles>` elemento per aggiungere testo a una forma.</span><span class="sxs-lookup"><span data-stu-id="da33b-123">In this topic, we will illustrate how to use the `<handles>` element to attach text to a shape.</span></span>

<span data-ttu-id="da33b-124">È possibile inserire il `<handles>` sottoelemento all'interno `<shape>` o `<shapetype>` per definire gli elementi dell'interfaccia utente che possono variare i valori di **ADJ** sulla forma.</span><span class="sxs-lookup"><span data-stu-id="da33b-124">You can place the `<handles>` sub-element inside `<shape>` or `<shapetype>` to define user interface elements that can vary the **adj** values on the shape.</span></span>

<span data-ttu-id="da33b-125">Ad esempio, come illustrato nella seguente rappresentazione la, è possibile specificare un handle di regolazione (casella gialla) che gli utenti possono semplicemente trascinare per regolare la forma.</span><span class="sxs-lookup"><span data-stu-id="da33b-125">For example, as shown the following VML representation, you can provide an adjust handle (yellow box) that users can simply drag to adjust the shape.</span></span>

<span data-ttu-id="da33b-126">Nota: gli handle sono disponibili quando questa forma la viene visualizzata nelle applicazioni Microsoft Office, in cui la forma è progettata per essere manipolabile.</span><span class="sxs-lookup"><span data-stu-id="da33b-126">Note: the handles are available when this VML shape is viewed in Microsoft Office applications, where the shape is intended to be manipulable.</span></span>

![shape1.gif (564 byte)](images/shape1h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="16200,5400"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





<span data-ttu-id="da33b-128">Si noti che l'unica differenza tra la rappresentazione la precedente e quella seguente è il valore **ADJ** .</span><span class="sxs-lookup"><span data-stu-id="da33b-128">Notice that the only difference between the preceding VML representation and the following one is the **adj** value.</span></span>

![shape2.gif (1361 byte)](images/shape2h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="11304,6600"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





<span data-ttu-id="da33b-130">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858393) .</span><span class="sxs-lookup"><span data-stu-id="da33b-130">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858393) .</span></span>

 

 