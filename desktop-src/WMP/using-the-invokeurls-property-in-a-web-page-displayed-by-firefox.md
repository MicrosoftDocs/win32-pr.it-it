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
# <a name="using-the-invokeurls-property-in-a-web-page-displayed-by-firefox"></a>Uso della proprietà invokeURLs in una pagina Web visualizzata da Firefox

Alcuni file multimediali contengono URL incorporati per i quali Windows Media Player Visualizza le pagine Web in una finestra o un frame Web browser quando il file multimediale viene riprodotto. In Windows Internet Explorer è possibile utilizzare la proprietà [Settings. invokeURLs](settings-invokeurls.md) per specificare se le pagine vengono visualizzate per gli URL incorporati ed è possibile utilizzare la proprietà [Settings. defaultFrame](settings-defaultframe.md) per specificare un frame per la visualizzazione di tali pagine.

In Firefox sono necessarie alcune soluzioni alternative per impostare la proprietà **invokeURLs** e per specificare un frame per la visualizzazione di pagine per gli URL incorporati.

## <a name="setting-the-invokeurls-property"></a>Impostazione della proprietà invokeURLs

Il valore predefinito della proprietà **Settings. invokeURLs** è true, pertanto se si desidera che il valore sia false, è necessario impostarlo in modo esplicito. In Internet Explorer è possibile impostare **invokeURLs** su false in un elemento param all'interno dell'elemento Object del controllo Player.

Il plug-in di Firefox non supporta l'impostazione della proprietà **invokeURLs** in un elemento param.

È possibile ovviare a questa limitazione impostando la proprietà **invokeURLs** nello script. Il codice seguente illustra come impostare la proprietà **invokeURLs** su false in una pagina Web che può essere visualizzata da Internet Explorer e Firefox.


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



## <a name="displaying-webpages-in-a-frame"></a>Visualizzazione di pagine Web in un frame

Un file multimediale può contenere URL che visualizzano pagine Web in una finestra del browser o un frame quando viene riprodotto il file multimediale. In Internet Explorer è possibile utilizzare la proprietà [Settings. defaultFrame](settings-defaultframe.md) per specificare il frame in cui vengono visualizzate tali pagine. Se non si imposta la proprietà **DefaultFrame** , gli URL vengono visualizzati in una finestra separata del browser predefinito. Tuttavia, il plug-in di Firefox non supporta la proprietà **Settings. defaultFrame** . Per ovviare a questa limitazione, impostare la proprietà **Settings. invokeURLs** su false e scrivere un gestore eventi [ScriptCommand](player-player-scriptcommand.md) che imposta il percorso del frame di destinazione. Questa tecnica è illustrata nell'esempio seguente, che funziona in Internet Explorer e Firefox. Si supponga che la pagina web mostrata nell'esempio sia in frame \[ 0 \] e che si desideri che la pagina dell'URL venga visualizzata in frame \[ 1 \] .


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del controllo Media Player Windows con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




