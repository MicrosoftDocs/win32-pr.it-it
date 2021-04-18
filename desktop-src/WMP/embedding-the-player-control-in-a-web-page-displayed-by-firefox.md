---
title: Incorporamento del controllo Player in una pagina Web visualizzata da Firefox
description: Incorporamento del controllo Player in una pagina Web visualizzata da Firefox
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
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
- Windows Media Player, Firefox
- Modello a oggetti di Windows Media Player, Firefox
- modello a oggetti, Firefox
- Windows Media Player Mobile, Firefox
- Controllo ActiveX di Windows Media Player, Firefox
- Controllo ActiveX Windows Media Player Mobile, Firefox
- Controllo ActiveX, Firefox
- Firefox, informazioni sull'incorporamento di pagine Web
- incorporamento, pagine Web
- Incorporamento di pagine Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16063ea07a0262ab798e58ed02e4d5a5b6b5d65
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "106299014"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="b0871-123">Incorporamento del controllo Player in una pagina Web visualizzata da Firefox</span><span class="sxs-lookup"><span data-stu-id="b0871-123">Embedding the Player Control in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="b0871-124">Per incorporare il controllo Media Player di Windows in una pagina Web che può essere visualizzata da un browser Firefox, creare un elemento oggetto o un elemento di INCORPORAmento con uno dei seguenti tipi MIME come attributo di **tipo** :</span><span class="sxs-lookup"><span data-stu-id="b0871-124">To embed the Windows Media Player control in a webpage that can be displayed by a Firefox browser, create an OBJECT element or an EMBED element that has one of the following mime types as its **type** attribute:</span></span>

-   <span data-ttu-id="b0871-125">applicazione/x-ms-WMP</span><span class="sxs-lookup"><span data-stu-id="b0871-125">application/x-ms-wmp</span></span>
-   <span data-ttu-id="b0871-126">applicazione/ASX</span><span class="sxs-lookup"><span data-stu-id="b0871-126">application/asx</span></span>
-   <span data-ttu-id="b0871-127">video/x-ms-asf-plug-in</span><span class="sxs-lookup"><span data-stu-id="b0871-127">video/x-ms-asf-plugin</span></span>
-   <span data-ttu-id="b0871-128">applicazione/x-mplayer2</span><span class="sxs-lookup"><span data-stu-id="b0871-128">application/x-mplayer2</span></span>
-   <span data-ttu-id="b0871-129">video/x-ms-asf</span><span class="sxs-lookup"><span data-stu-id="b0871-129">video/x-ms-asf</span></span>
-   <span data-ttu-id="b0871-130">video/x-ms-WM</span><span class="sxs-lookup"><span data-stu-id="b0871-130">video/x-ms-wm</span></span>
-   <span data-ttu-id="b0871-131">audio/x-ms-WMA</span><span class="sxs-lookup"><span data-stu-id="b0871-131">audio/x-ms-wma</span></span>
-   <span data-ttu-id="b0871-132">audio/x-ms-Wax</span><span class="sxs-lookup"><span data-stu-id="b0871-132">audio/x-ms-wax</span></span>
-   <span data-ttu-id="b0871-133">video/x-MS-WMV</span><span class="sxs-lookup"><span data-stu-id="b0871-133">video/x-ms-wmv</span></span>
-   <span data-ttu-id="b0871-134">video/x-ms-wvx</span><span class="sxs-lookup"><span data-stu-id="b0871-134">video/x-ms-wvx</span></span>

<span data-ttu-id="b0871-135">Il tipo MIME preferito è application/x-ms-WMP.</span><span class="sxs-lookup"><span data-stu-id="b0871-135">The preferred mime type is application/x-ms-wmp.</span></span>

<span data-ttu-id="b0871-136">Negli esempi seguenti viene illustrato come incorporare il controllo Player utilizzando un elemento oggetto o un elemento EMBED.</span><span class="sxs-lookup"><span data-stu-id="b0871-136">The following examples show how to embed the Player control using an OBJECT element or an EMBED element.</span></span>


```HTML
<OBJECT id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320">
  <PARAM name="autostart" value="false"/>
</OBJECT>

<EMBED id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320"
  autostart="false"/>

```



<span data-ttu-id="b0871-137">Gli esempi di precedente funzionano in Firefox ma non in Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b0871-137">The preceeding examples work in Firefox but not in Internet Explorer.</span></span> <span data-ttu-id="b0871-138">Per incorporare il controllo Player in una pagina Web che può essere visualizzata da Internet Explorer, è necessario creare un elemento oggetto con un attributo **ClassID** impostato sull'ID classe del controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="b0871-138">To embed the Player control in a webpage that can be displayed by Internet Explorer, you must create an OBJECT element that has a **classid** attribute set to the class ID of the Windows Media Player control.</span></span>

<span data-ttu-id="b0871-139">Nell'esempio seguente viene illustrato come incorporare il controllo Windows Media Player in una pagina Web che può essere visualizzata correttamente da Internet Explorer e Firefox.</span><span class="sxs-lookup"><span data-stu-id="b0871-139">The following example shows how to embed the Windows Media Player control in a webpage that can be displayed correctly by both Internet Explorer and Firefox.</span></span> <span data-ttu-id="b0871-140">Lo script nella pagina rileva il tipo di browser e genera il tag oggetto appropriato.</span><span class="sxs-lookup"><span data-stu-id="b0871-140">Script on the page detects the browser type and generates the appropriate OBJECT tag.</span></span>


```HTML
<HTML>
  <BODY>
    <SCRIPT type="text/javascript">
      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {
        document.write('<OBJECT id="Player"');
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');
        document.write(' width=300 height=200></OBJECT>');
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {
        document.write('<OBJECT id="Player"'); 
        document.write(' type="application/x-ms-wmp"'); 
        document.write(' width=300 height=200></OBJECT>');
      }         
    </SCRIPT>
  </BODY>
</HTML>

```



## <a name="related-topics"></a><span data-ttu-id="b0871-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0871-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0871-142">**Uso del controllo Media Player Windows con Firefox**</span><span class="sxs-lookup"><span data-stu-id="b0871-142">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




