---
title: Gestione degli eventi in una pagina Web visualizzata da Firefox
description: Gestione degli eventi in una pagina Web visualizzata da Firefox
ms.assetid: 361c46ff-36e2-4497-a511-86b0439e9437
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Controllo ActiveX di Windows Media Player, pagine Web
- Controllo ActiveX Windows Media Player Mobile, pagine Web
- Controllo ActiveX, pagine Web
- Controllo ActiveX Windows Media Player, gestione eventi
- Controllo ActiveX Windows Media Player Mobile, gestione eventi
- Controllo ActiveX, gestione eventi
- incorporamento, pagine Web
- Incorporamento di pagine Web, gestione degli eventi
- Windows Media Player, Firefox
- Modello a oggetti di Windows Media Player, Firefox
- modello a oggetti, Firefox
- Windows Media Player Mobile, Firefox
- Controllo ActiveX di Windows Media Player, Firefox
- Controllo ActiveX Windows Media Player Mobile, Firefox
- Controllo ActiveX, Firefox
- Firefox, gestione degli eventi
- Incorporamento di pagine Web, Firefox
- eventi, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9659d1920ffc4d5e39f4cd44e15e24b08f6ddc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "104332876"
---
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="75aa3-128">Gestione degli eventi in una pagina Web visualizzata da Firefox</span><span class="sxs-lookup"><span data-stu-id="75aa3-128">Handling Events in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="75aa3-129">Quando si incorpora il controllo Windows Media Player in una pagina Web, è possibile scrivere uno script che gestisce gli eventi.</span><span class="sxs-lookup"><span data-stu-id="75aa3-129">When you embed the Windows Media Player control in a webpage, you can write script that handles events.</span></span> <span data-ttu-id="75aa3-130">Per un elenco degli eventi generati dal controllo Player, vedere [oggetto Player](player-object.md).</span><span class="sxs-lookup"><span data-stu-id="75aa3-130">For a list of events raised by the Player control, see [Player Object](player-object.md).</span></span>

<span data-ttu-id="75aa3-131">Se il tipo MIME associato a un controllo Player incorporato è application/x-ms-WMP, è possibile scrivere i gestori eventi che hanno il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="75aa3-131">If the mime type associated with an embedded Player control is application/x-ms-wmp, you can write event handlers that have the following format:</span></span>


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



<span data-ttu-id="75aa3-132">dove *EventName* è il nome di un evento Windows Media Player e *params* è un elenco dei parametri dell'evento.</span><span class="sxs-lookup"><span data-stu-id="75aa3-132">where *EventName* is the name of a Windows Media Player event, and *Params* is a list of the event's parameters.</span></span> <span data-ttu-id="75aa3-133">Il codice seguente, ad esempio, ha un gestore per l'evento [PlayStateChange](player-player-playstatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="75aa3-133">For example, the following code has a handler for the [PlayStateChange](player-player-playstatechange.md) event.</span></span>


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Seattle.wmv"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT for="Player" event="PlayStateChange(NewState)">
  document.getElementById("p1").innerHTML = "Play state: " + NewState;
</SCRIPT>
```



<span data-ttu-id="75aa3-134">Se si dispone di più istanze del controllo Player in una pagina Web e si usa il formato illustrato nell'esempio precedente, ogni gestore eventi è associato a un'istanza specifica del controllo Player.</span><span class="sxs-lookup"><span data-stu-id="75aa3-134">If you have several instances of the Player control on a webpage and if you use the format shown in the preceeding example, then each event handler is tied to a specific instance of the Player control.</span></span> <span data-ttu-id="75aa3-135">Nell'esempio precedente, il gestore eventi viene chiamato solo quando lo stato di riproduzione viene modificato per il controllo con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="75aa3-135">In the preceeding example, the event handler is called only when the play state changes for the control that has id="Player".</span></span>

<span data-ttu-id="75aa3-136">Se il tipo MIME associato a un controllo Player incorporato non è application/x-ms-WMP, è possibile scrivere i gestori eventi che hanno il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="75aa3-136">If the mime type associated with an embedded Player control is not application/x-ms-wmp, you can write event handlers that have the following format:</span></span>


```HTML
<SCRIPT language="jscript">
  function OnDSEventNameEvt(Params)
  {...}
</SCRIPT>
```



<span data-ttu-id="75aa3-137">dove *EventName* è il nome di un evento Windows Media Player e *params* è un elenco dei parametri dell'evento.</span><span class="sxs-lookup"><span data-stu-id="75aa3-137">where *EventName* is the name of a Windows Media Player event, and *Params* is a list of the event's parameters.</span></span> <span data-ttu-id="75aa3-138">Il codice seguente, ad esempio, ha un gestore per l'evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="75aa3-138">For example, the following code has a handler for the **PlayStateChange** event.</span></span>


```HTML
<OBJECT id="Player" type="application/asx" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Test.asx"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT>
  function OnDSPlayStateChangeEvt(NewState)
  {
    p1.innerHTML = "Play state: " + NewState;
  }
</SCRIPT>

```



<span data-ttu-id="75aa3-139">Se si dispone di più istanze del controllo Player in una pagina Web e si usa il formato illustrato nell'esempio precedente, ogni gestore eventi è associato a tutte le istanze del controllo lettore e il gestore eventi viene chiamato quando lo stato di riproduzione per qualsiasi controllo del lettore nella pagina.</span><span class="sxs-lookup"><span data-stu-id="75aa3-139">If you have several instances of the Player control on a webpage and if you use the format shown in the preceeding example, then each event handler is tied to all instances of the Player control and the event handler is called when the play state changes for any Player control on the page.</span></span>

> [!Note]  
> <span data-ttu-id="75aa3-140">Se il tipo MIME non è application/x-ms-WMP, l'evento **DoubleClick** viene inviato come OnDSDblClickEvt (non OnDSDoubleClickEvt) per la compatibilità con la versione 6,4 del controllo Player.</span><span class="sxs-lookup"><span data-stu-id="75aa3-140">If the mime type is not application/x-ms-wmp, the **DoubleClick** event is sent as OnDSDblClickEvt (not OnDSDoubleClickEvt) for compatibility with version 6.4 of the Player control.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="75aa3-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="75aa3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75aa3-142">**Uso del controllo Media Player Windows con Firefox**</span><span class="sxs-lookup"><span data-stu-id="75aa3-142">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




