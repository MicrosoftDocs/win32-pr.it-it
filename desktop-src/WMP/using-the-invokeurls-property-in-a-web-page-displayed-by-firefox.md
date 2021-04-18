---
title: Uso della proprietà invokeURLs in una pagina Web visualizzata da Firefox
description: Uso della proprietà invokeURLs in una pagina Web visualizzata da Firefox
ms.assetid: cec2ba89-b08f-4c83-bcb2-a4df1ce6f179
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX di Windows Media Player, pagine Web
- Controllo ActiveX Windows Media Player Mobile, pagine Web
- Controllo ActiveX Windows Media Player, proprietà invokeURLs
- Controllo ActiveX Windows Media Player Mobile, proprietà invokeURLs
- incorporamento, pagine Web
- Incorporamento di pagine Web, proprietà invokeURLs
- Windows Media Player, Firefox
- Modello a oggetti di Windows Media Player, Firefox
- modello a oggetti, Firefox
- Controllo ActiveX di Windows Media Player, Firefox
- Controllo ActiveX, Firefox
- Firefox, proprietà invokeURLs
- Incorporamento di pagine Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0a2eb96e65d8fa6d2758669e3c844b2d13c0bc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "106299010"
---
# <a name="using-the-invokeurls-property-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="41cfd-122">Uso della proprietà invokeURLs in una pagina Web visualizzata da Firefox</span><span class="sxs-lookup"><span data-stu-id="41cfd-122">Using the invokeURLs Property in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="41cfd-123">Alcuni file multimediali contengono URL incorporati per i quali Windows Media Player Visualizza le pagine Web in una finestra o un frame Web browser quando il file multimediale viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="41cfd-123">Some media files contain embedded URLs for which Windows Media Player displays webpages in a Web browser window or frame as the media file plays.</span></span> <span data-ttu-id="41cfd-124">In Windows Internet Explorer è possibile utilizzare la proprietà [Settings. invokeURLs](settings-invokeurls.md) per specificare se le pagine vengono visualizzate per gli URL incorporati ed è possibile utilizzare la proprietà [Settings. defaultFrame](settings-defaultframe.md) per specificare un frame per la visualizzazione di tali pagine.</span><span class="sxs-lookup"><span data-stu-id="41cfd-124">In Windows Internet Explorer, you can use the [Settings.invokeURLs](settings-invokeurls.md) property to specify whether pages are displayed for embedded URLs, and you can use the [Settings.defaultFrame](settings-defaultframe.md) property to specify a frame for displaying such pages.</span></span>

<span data-ttu-id="41cfd-125">In Firefox sono necessarie alcune soluzioni alternative per impostare la proprietà **invokeURLs** e per specificare un frame per la visualizzazione di pagine per gli URL incorporati.</span><span class="sxs-lookup"><span data-stu-id="41cfd-125">In Firefox, some workarounds are required to set the **invokeURLs** property and to specify a frame for displaying pages for embedded URLs.</span></span>

## <a name="setting-the-invokeurls-property"></a><span data-ttu-id="41cfd-126">Impostazione della proprietà invokeURLs</span><span class="sxs-lookup"><span data-stu-id="41cfd-126">Setting the invokeURLs property</span></span>

<span data-ttu-id="41cfd-127">Il valore predefinito della proprietà **Settings. invokeURLs** è true, pertanto se si desidera che il valore sia false, è necessario impostarlo in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="41cfd-127">The default value of the **Settings.invokeURLs** property is true, so if you want the value to be false, you must set it explicitly.</span></span> <span data-ttu-id="41cfd-128">In Internet Explorer è possibile impostare **invokeURLs** su false in un elemento param all'interno dell'elemento Object del controllo Player.</span><span class="sxs-lookup"><span data-stu-id="41cfd-128">In Internet Explorer, you can set **invokeURLs** to false in a PARAM element inside the Player control's OBJECT element.</span></span>

<span data-ttu-id="41cfd-129">Il plug-in di Firefox non supporta l'impostazione della proprietà **invokeURLs** in un elemento param.</span><span class="sxs-lookup"><span data-stu-id="41cfd-129">The Firefox plug-in does not support setting the **invokeURLs** property in a PARAM element.</span></span>

<span data-ttu-id="41cfd-130">È possibile ovviare a questa limitazione impostando la proprietà **invokeURLs** nello script.</span><span class="sxs-lookup"><span data-stu-id="41cfd-130">You can work around this limitation by setting the **invokeURLs** property in script.</span></span> <span data-ttu-id="41cfd-131">Il codice seguente illustra come impostare la proprietà **invokeURLs** su false in una pagina Web che può essere visualizzata da Internet Explorer e Firefox.</span><span class="sxs-lookup"><span data-stu-id="41cfd-131">The following code shows how to set the **invokeURLs** property to false in a webpage that can be displayed by both Internet Explorer and Firefox.</span></span>


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

  </BODY>
</HTML>

```



## <a name="displaying-webpages-in-a-frame"></a><span data-ttu-id="41cfd-132">Visualizzazione di pagine Web in un frame</span><span class="sxs-lookup"><span data-stu-id="41cfd-132">Displaying webpages in a frame</span></span>

<span data-ttu-id="41cfd-133">Un file multimediale può contenere URL che visualizzano pagine Web in una finestra del browser o un frame quando viene riprodotto il file multimediale.</span><span class="sxs-lookup"><span data-stu-id="41cfd-133">A media file can contain URLs that display webpages in a browser window or frame as the media file is played.</span></span> <span data-ttu-id="41cfd-134">In Internet Explorer è possibile utilizzare la proprietà [Settings. defaultFrame](settings-defaultframe.md) per specificare il frame in cui vengono visualizzate tali pagine.</span><span class="sxs-lookup"><span data-stu-id="41cfd-134">In Internet Explorer, you can use the [Settings.defaultFrame](settings-defaultframe.md) property to specify the frame in which those pages are displayed.</span></span> <span data-ttu-id="41cfd-135">Se non si imposta la proprietà **DefaultFrame** , gli URL vengono visualizzati in una finestra separata del browser predefinito.</span><span class="sxs-lookup"><span data-stu-id="41cfd-135">If you do not set the **defaultFrame** property, URLs are displayed in a separate window of the default browser.</span></span> <span data-ttu-id="41cfd-136">Tuttavia, il plug-in di Firefox non supporta la proprietà **Settings. defaultFrame** .</span><span class="sxs-lookup"><span data-stu-id="41cfd-136">However, the Firefox plug-in does not support the **Settings.defaultFrame** property.</span></span> <span data-ttu-id="41cfd-137">Per ovviare a questa limitazione, impostare la proprietà **Settings. invokeURLs** su false e scrivere un gestore eventi [ScriptCommand](player-player-scriptcommand.md) che imposta il percorso del frame di destinazione.</span><span class="sxs-lookup"><span data-stu-id="41cfd-137">To work around this limitation, set the **Settings.invokeURLs** property to false and write a [ScriptCommand](player-player-scriptcommand.md) event handler that sets the location of the target frame.</span></span> <span data-ttu-id="41cfd-138">Questa tecnica è illustrata nell'esempio seguente, che funziona in Internet Explorer e Firefox.</span><span class="sxs-lookup"><span data-stu-id="41cfd-138">The following example, which works in Internet Explorer and Firefox, illustrates this technique.</span></span> <span data-ttu-id="41cfd-139">Si supponga che la pagina web mostrata nell'esempio sia in frame \[ 0 \] e che si desideri che la pagina dell'URL venga visualizzata in frame \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="41cfd-139">Assume that the webpage shown in the example is in frames\[0\] and you want the URL's page to be displayed in frames\[1\].</span></span>


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

    <SCRIPT for="Player" event="ScriptCommand(scType, scParam)">
      if( scType == "URL" )
      {
        parent.frames[1].location = scParam;
      }
    </script>

  </BODY>
</HTML>

```



## <a name="related-topics"></a><span data-ttu-id="41cfd-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41cfd-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41cfd-141">**Uso del controllo Media Player Windows con Firefox**</span><span class="sxs-lookup"><span data-stu-id="41cfd-141">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




